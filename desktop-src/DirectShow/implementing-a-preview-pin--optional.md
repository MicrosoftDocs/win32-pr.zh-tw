---
description: 本主題說明如何在 DirectShow 捕獲篩選器上執行預覽圖釘。
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: " (選用) 來執行預覽 Pin"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e09d070be2aa154428cb8684ff1c405fac959
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385765"
---
# <a name="implementing-a-preview-pin-optional"></a><span data-ttu-id="785d3-103"> (選用) 來執行預覽 Pin</span><span class="sxs-lookup"><span data-stu-id="785d3-103">Implementing a Preview Pin (Optional)</span></span>

<span data-ttu-id="785d3-104">本主題說明如何在 DirectShow 捕獲篩選器上執行預覽圖釘。</span><span class="sxs-lookup"><span data-stu-id="785d3-104">This topic describes how to implement a preview pin on a DirectShow capture filter.</span></span>

<span data-ttu-id="785d3-105">如果您的篩選準則有預覽 pin，預覽 pin 必須傳送由 capture pin 所傳遞的資料複本。</span><span class="sxs-lookup"><span data-stu-id="785d3-105">If your filter has a preview pin, the preview pin must send a copy of the data delivered by the capture pin.</span></span> <span data-ttu-id="785d3-106">當您這樣做時，只會從預覽 pin 傳送資料，並不會導致 capture 釘選框架。</span><span class="sxs-lookup"><span data-stu-id="785d3-106">Only send data from the preview pin when doing so will not cause the capture pin to drop frames.</span></span> <span data-ttu-id="785d3-107">捕捉 pin 一律優先于預覽 pin。</span><span class="sxs-lookup"><span data-stu-id="785d3-107">The capture pin always has priority over the preview pin.</span></span>

<span data-ttu-id="785d3-108">捕捉 pin 和預覽 pin 必須傳送相同格式的資料。</span><span class="sxs-lookup"><span data-stu-id="785d3-108">The capture pin and the preview pin must send data with the same format.</span></span> <span data-ttu-id="785d3-109">因此，他們必須使用相同的媒體類型進行連接。</span><span class="sxs-lookup"><span data-stu-id="785d3-109">Therefore, they must connect using identical media types.</span></span> <span data-ttu-id="785d3-110">如果捕捉 pin 先連接，預覽 pin 應提供相同的媒體類型，並拒絕任何其他類型。</span><span class="sxs-lookup"><span data-stu-id="785d3-110">If the capture pin connects first, the preview pin should offer the same media type, and reject any others types.</span></span> <span data-ttu-id="785d3-111">如果預覽 pin 會先連線，而且捕捉 pin 與不同的媒體類型連接，預覽 pin 應使用新的媒體類型重新連接。</span><span class="sxs-lookup"><span data-stu-id="785d3-111">If the preview pin connects first, and the capture pin connects with a different media type, the preview pin should reconnect using the new media type.</span></span> <span data-ttu-id="785d3-112">如果預覽 pin 的下游篩選器拒絕新的類型，則捕捉 pin 也應該拒絕類型。</span><span class="sxs-lookup"><span data-stu-id="785d3-112">If the filter downstream from the preview pin rejects the new type, the capture pin should also reject the type.</span></span> <span data-ttu-id="785d3-113">您可以使用 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 方法來查詢來自預覽 pin 的下游篩選，並使用 [**IFilterGraph：： reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) 方法來重新連接 pin。</span><span class="sxs-lookup"><span data-stu-id="785d3-113">Use the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method to query the filter downstream from the preview pin, and use the [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) method to reconnect the pin.</span></span> <span data-ttu-id="785d3-114">如果篩選圖形管理員重新連接捕捉 pin，也適用這些規則。</span><span class="sxs-lookup"><span data-stu-id="785d3-114">These rules also apply if the Filter Graph Manager reconnects the capture pin.</span></span>

<span data-ttu-id="785d3-115">下列範例顯示此程式的大綱：</span><span class="sxs-lookup"><span data-stu-id="785d3-115">The following example shows an outline of this process:</span></span>


```C++
// Override CBasePin::CheckMediaType.
CCapturePin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so query the pin it is
        // connected to. If the other pin rejects it, so do we.
        hr = m_pMyPreviewPin->GetConnected()->QueryAccept(pmt);
        if (hr != S_OK) 
        {
            // The preview pin cannot reconnect with this media type.
            return E_INVALIDARG;
        }
        // The preview pin will reconnect when SetMediaType is called.
    }
    // Decide whether the capture pin accepts the format. 
    BOOL fAcceptThisType = ...  // (Not shown.)
    return (fAcceptThisType? S_OK : E_FAIL);
}

// Override CBasePin::SetMediaType.
CCapturePin::SetMediaType(CMediaType *pmt);
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so it must reconnect.
        if (m_pMyPreviewPin->GetConnected()->QueryAccept(pmt) == S_OK)
        {
            // The downstream pin will accept the new type, so it's safe
            // to reconnect. 
            m_pFilter->m_pGraph->Reconnect(m_pMyPreviewPin);
        }
        else
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }
    // Now do anything that the capture pin needs to set the type.
    hr = MyInternalSetMediaType(pmt);

    // And finally, call the base-class method.
    return CBasePin::SetMediaType(pmt);
}

CPreviewPin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyCapturePin->IsConnected())
    {
       // The preview pin must connect with the same type.
       CMediaType cmt = m_pMyCapturePin->m_mt;
       return (*pmt == cmt ? S_OK : VFW_E_INVALIDMEDIATYPE);
    }
    // Decide whether the preview pin accepts the format. You can use your 
    // knowledge of which types the capture pin will accept. Regardless,
    // when the capture pin connects, the preview pin will reconnect.
    return (fAcceptThisType? S_OK : E_FAIL);
}
```



## <a name="related-topics"></a><span data-ttu-id="785d3-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="785d3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="785d3-117">篩選準則的連接方式</span><span class="sxs-lookup"><span data-stu-id="785d3-117">How Filters Connect</span></span>](how-filters-connect.md)
</dt> <dt>

[<span data-ttu-id="785d3-118">寫入捕獲篩選器</span><span class="sxs-lookup"><span data-stu-id="785d3-118">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



