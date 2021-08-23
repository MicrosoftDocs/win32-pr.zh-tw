---
description: 本主題說明如何在 DirectShow capture 篩選器上執行預覽 pin。
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: " (選用) 來執行預覽 Pin"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de47b86df70500c83c794fe1074dc927622d571e78ef6175b944702277da492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015556"
---
# <a name="implementing-a-preview-pin-optional"></a> (選用) 來執行預覽 Pin

本主題說明如何在 DirectShow capture 篩選器上執行預覽 pin。

如果您的篩選準則有預覽 pin，預覽 pin 必須傳送由 capture pin 所傳遞的資料複本。 當您這樣做時，只會從預覽 pin 傳送資料，並不會導致 capture 釘選框架。 捕捉 pin 一律優先于預覽 pin。

捕捉 pin 和預覽 pin 必須傳送相同格式的資料。 因此，他們必須使用相同的媒體類型進行連接。 如果捕捉 pin 先連接，預覽 pin 應提供相同的媒體類型，並拒絕任何其他類型。 如果預覽 pin 會先連線，而且捕捉 pin 與不同的媒體類型連接，預覽 pin 應使用新的媒體類型重新連接。 如果預覽 pin 的下游篩選器拒絕新的類型，則捕捉 pin 也應該拒絕類型。 您可以使用 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 方法來查詢來自預覽 pin 的下游篩選，並使用 [**IFilterGraph：： reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) 方法來重新連接 pin。 如果篩選 Graph 管理員重新連接捕捉 pin，也適用這些規則。

下列範例顯示此程式的大綱：


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選準則的連線](how-filters-connect.md)
</dt> <dt>

[寫入捕獲篩選器](writing-capture-filters.md)
</dt> </dl>

 

 



