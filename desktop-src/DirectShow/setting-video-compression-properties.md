---
description: 設定影片壓縮屬性
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: 設定影片壓縮屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d29ed7e42745ffd51fca14b7da5f72c749281e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385731"
---
# <a name="setting-video-compression-properties"></a><span data-ttu-id="1539c-103">設定影片壓縮屬性</span><span class="sxs-lookup"><span data-stu-id="1539c-103">Setting Video Compression Properties</span></span>

<span data-ttu-id="1539c-104">影片壓縮篩選器可支援其輸出圖釘上的 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) 介面。</span><span class="sxs-lookup"><span data-stu-id="1539c-104">Video compression filters can support the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface on their output pins.</span></span> <span data-ttu-id="1539c-105">使用這個介面設定壓縮屬性，例如主要畫面格速率、預測的 (P) 每個主要畫面格的畫面格數目，以及相對的壓縮品質。</span><span class="sxs-lookup"><span data-stu-id="1539c-105">Use this interface to set compression properties, such as the key frame rate, the number of predicted (P) frames per key frame, and the relative compression quality.</span></span>

<span data-ttu-id="1539c-106">首先，呼叫 [**IBaseFilter：： EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) 方法來尋找篩選的輸出圖釘，並查詢介面的 pin。</span><span class="sxs-lookup"><span data-stu-id="1539c-106">First, call the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the filter's output pin, and query the pin for the interface.</span></span> <span data-ttu-id="1539c-107">某些篩選器可能完全不支援此介面。</span><span class="sxs-lookup"><span data-stu-id="1539c-107">Some filters may not support the interface at all.</span></span> <span data-ttu-id="1539c-108">其他可能會公開介面，但不支援每個壓縮屬性。</span><span class="sxs-lookup"><span data-stu-id="1539c-108">Others may expose the interface but not support every compression property.</span></span> <span data-ttu-id="1539c-109">若要判斷支援的屬性，請呼叫 [**IAMVideoCompression：： GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo)。</span><span class="sxs-lookup"><span data-stu-id="1539c-109">To determine which properties are supported, call [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="1539c-110">這個方法會傳回數個資訊片段：</span><span class="sxs-lookup"><span data-stu-id="1539c-110">This method returns several pieces of information:</span></span>

-   <span data-ttu-id="1539c-111">一組功能旗標</span><span class="sxs-lookup"><span data-stu-id="1539c-111">A set of capabilities flags</span></span>
-   <span data-ttu-id="1539c-112">描述性字串和版本號碼字串</span><span class="sxs-lookup"><span data-stu-id="1539c-112">A descriptive string and version-number string</span></span>
-   <span data-ttu-id="1539c-113">支援的主要畫面速率、P 畫面播放速率和品質 (的預設值) </span><span class="sxs-lookup"><span data-stu-id="1539c-113">Default values for key frame rate, P frame rate, and quality (when supported)</span></span>

<span data-ttu-id="1539c-114">方法具有下列語法：</span><span class="sxs-lookup"><span data-stu-id="1539c-114">The method has the following syntax:</span></span>


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



<span data-ttu-id="1539c-115">*PszVersion* 和 *pszDesc* 參數是可接收版本字串和描述字串的寬字元緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1539c-115">The *pszVersion* and *pszDesc* parameters are wide-character buffers that receive the version string and description string.</span></span> <span data-ttu-id="1539c-116">*CbVersion* 和 *cbDesc* 參數會收到所需的緩衝區大小（以位元組為單位）， (不是字元) 。</span><span class="sxs-lookup"><span data-stu-id="1539c-116">The *cbVersion* and *cbDesc* parameters receive the required buffer sizes in bytes (not characters).</span></span> <span data-ttu-id="1539c-117">*LKeyFrame*、 *lPFrame* 和 *dblQuality* 參數會接收主要畫面速率、P 畫面播放速率和品質的預設值。</span><span class="sxs-lookup"><span data-stu-id="1539c-117">The *lKeyFrame*, *lPFrame*, and *dblQuality* parameters receive the default values for the key frame rate, P frame rate, and quality.</span></span> <span data-ttu-id="1539c-118">品質會以從0.0 到1.0 的浮點數表示。</span><span class="sxs-lookup"><span data-stu-id="1539c-118">Quality is expressed as a floating-point number from 0.0 to 1.0.</span></span> <span data-ttu-id="1539c-119">*LCap* 參數會接收由 [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps)列舉型別定義之功能旗標的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="1539c-119">The *lCap* parameter receives a bitwise **OR** of the capabilities flags, which are defined by the [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) enumerated type.</span></span>

<span data-ttu-id="1539c-120">這些參數中的任何一個都可以是 **Null**，在此情況下，方法會忽略該參數。</span><span class="sxs-lookup"><span data-stu-id="1539c-120">Any of these parameters can be **NULL**, in which case the method ignores that parameter.</span></span> <span data-ttu-id="1539c-121">例如，若要為版本和描述字串配置緩衝區，請先使用第一個和第三個參數中的 **Null** 來呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="1539c-121">For example, to allocate buffers for the version and description strings, first call the method with **NULL** in the first and third parameters.</span></span> <span data-ttu-id="1539c-122">使用 *cbVersion* 和 *cbDesc* 傳回的值來配置緩衝區，然後再次呼叫方法：</span><span class="sxs-lookup"><span data-stu-id="1539c-122">Use the returned values for *cbVersion* and *cbDesc* to allocate the buffers and then call the method again:</span></span>


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



<span data-ttu-id="1539c-123">*LCap* 的值表示篩選準則所支援的其他 **IAMVideoCompression** 方法。</span><span class="sxs-lookup"><span data-stu-id="1539c-123">The value of *lCap* indicates which of the other **IAMVideoCompression** methods the filter supports.</span></span> <span data-ttu-id="1539c-124">例如，如果 *lCap* 包含 CompressionCaps \_ CanKeyFrame 旗標，則您可以呼叫 [**IAMVideoCompression：： get \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) 來取得主要畫面播放速率和 [**IAMVideoCompression：:p 的 \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) ，以設定主要畫面格速率。</span><span class="sxs-lookup"><span data-stu-id="1539c-124">For example, if *lCap* contains the CompressionCaps\_CanKeyFrame flag, you can call [**IAMVideoCompression::get\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) to get the key frame rate and [**IAMVideoCompression::put\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) to set the key frame rate.</span></span> <span data-ttu-id="1539c-125">負數值表示篩選將會使用預設值，如同從 [**IAMVideoCompression：： GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo)取得的值。</span><span class="sxs-lookup"><span data-stu-id="1539c-125">A negative value indicates that the filter will use the default value, as obtained from [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="1539c-126">例如：</span><span class="sxs-lookup"><span data-stu-id="1539c-126">For example:</span></span>


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



<span data-ttu-id="1539c-127">下列程式碼範例會嘗試在輸出釘選上尋找 **IAMVideoCompression** 介面。</span><span class="sxs-lookup"><span data-stu-id="1539c-127">The following code example tries to find the **IAMVideoCompression** interface on the output pin.</span></span> <span data-ttu-id="1539c-128">如果成功，則會抓取壓縮屬性的預設值和實際值：</span><span class="sxs-lookup"><span data-stu-id="1539c-128">If it succeeds, it retrieves the default and actual values for the compression properties:</span></span>


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="1539c-129">如果您使用 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)介面來建立圖形，您可以藉由呼叫 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)來取得 **IAMVideoCompression** 介面，而不是使用 **IBaseFilter：： EnumPins**。</span><span class="sxs-lookup"><span data-stu-id="1539c-129">If you are using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface to build your graph, you can obtain the **IAMVideoCompression** interface by calling [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), instead of using **IBaseFilter::EnumPins**.</span></span> <span data-ttu-id="1539c-130">**FindInterface** 方法是一個 helper 方法，可在圖形中搜尋指定介面的篩選和釘選。</span><span class="sxs-lookup"><span data-stu-id="1539c-130">The **FindInterface** method is a helper method that searches filters and pins in the graph for a specified interface.</span></span>

 

 

 



