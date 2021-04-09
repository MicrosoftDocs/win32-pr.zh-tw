---
description: 'QueryAccept (上游) '
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: 'QueryAccept (上游) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7707c52d36c3d065c4a7277939f724aabdb73e46
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688224"
---
# <a name="queryaccept-upstream"></a>QueryAccept (上游) 

這種機制可讓輸入的 pin 提議對其上游對等的格式變更。 下游篩選器必須將媒體類型附加至上游篩選器在下一次呼叫 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)時取得的範例。 不過，若要這樣做，下游篩選器必須提供連接的自訂配置器。 此配置器必須執行下游篩選器可在下一個範例中用來設定媒體類型的私用方法。

會進行下列步驟：

1.  下游篩選器會檢查 pin 連接是否使用篩選器的自訂配置器。 如果上游篩選準則擁有配置器，下游篩選器將無法變更格式。
2.  下游篩選器會在上游輸出 pin 上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) (請參閱圖、步驟 A) 。
3.  如果傳回 `QueryAccept` S \_ ，下游篩選器會在其配置器上呼叫私用方法，以便設定媒體類型。 在此私用方法中，配置器會在下一個可用的範例 (B) 上呼叫 [**IMediaSample：： SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) 。
4.  上游篩選準則會呼叫 **GetBuffer** 以取得新的 (C) 和 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) 範例，以取得 (D) 的媒體類型。
5.  當上游篩選器傳遞範例時，它應該將媒體類型附加至該範例。 如此一來，下游篩選可以確認媒體類型已 (E) 變更。

如果上游篩選器接受格式變更，它也必須能夠切換回原始媒體類型，如下圖所示。

![queryaccept (上游) ](images/dynformat4.png)

這種格式變更的主要範例包括 DirectShow 影片轉譯器。

-   原始的 [影片](video-renderer-filter.md) 轉譯器篩選器可以在串流期間于 RGB 和 YUV 類型之間切換。 當篩選連接時，需要符合目前顯示設定的 RGB 格式。 這可保證在需要的情況下，可以切換回 GDI。 串流處理開始之後，如果有 DirectDraw 可用，則影片轉譯器會要求使用 YUV 類型的格式變更。 之後，如果有任何原因，它可能會切換回 RGB。
-   較新的影片混合轉譯器 (VMR) 篩選器會以圖形硬體支援的任何格式（包括 YUV 類型）進行連接。 不過，圖形硬體可能會變更基礎 DirectDraw 表面的 stride，以將效能優化。 VMR 篩選器 `QueryAccept` 會使用來報告新的 stride，這是在 **BITMAPINFOHEADER** 結構的 **biWidth** 成員中指定的。 **VIDEOINFOHEADER** 或 **VIDEOINFOHEADER2** 結構中的來源和目標矩形會識別應該將影片解碼的區域。

**執行附注**

您不太可能會撰寫需要要求上游格式變更的篩選準則，因為這主要是影片轉譯器的一項功能。 但是，如果您撰寫影片轉換篩選或影片解碼，您的篩選器必須正確地回應來自影片轉譯器的要求。

位於影片轉譯器與解碼器之間的就地篩選應傳遞所有 `QueryAccept` 上游的呼叫。 儲存新的格式資訊。

複製轉換篩選 (也就是說，非就地篩選) 應該執行下列其中一種行為：

-   在上游傳遞格式變更，並在到達時儲存新的格式資訊。 您的篩選準則必須使用自訂配置器，才能將格式附加至上游範例。
-   在篩選內執行格式轉換。 這可能比傳遞格式變更上游更容易。 不過，它可能會比讓解碼器篩選器解碼成正確的格式更有效率。
-   最後的手段是拒絕格式變更。  (需詳細資訊，請參閱 DirectShow 基類庫中的 [**CTransInPlaceOutputPin：： CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) 方法的原始程式碼。 ) 拒絕格式變更可能會降低效能，因為它會防止影片轉譯器使用最有效率的格式。

下列虛擬程式碼示範如何執行複製轉換篩選 (衍生自可在 YUV 和 RGB 輸出類型之間切換的 **CTransformFilter**) 。 此範例假設篩選本身會進行轉換，而不是傳遞格式變更上游。


```C++
HRESULT CMyTransform::CheckInputType(const CMediaType *pmt)
{
    if (pmt is a YUV type that you support) {
        return S_OK;
    }
    else {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
}

HRESULT CMyTransform::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    if (mtOut is a YUV or RGB type that you support)
    {
        if ((mtIn has the same video dimensions as mtOut) &&
            (you support the mtIn-to-mtOut transform))
        {
            return S_OK;
        }
    }
    // otherwise
    return VFW_E_TYPE_NOT_ACCEPTED;
}

// GetMediaType: Return a preferred output type.
HRESULT CMyTransform::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    if (iPosition < 0) {
        return E_INVALIDARG;
    }
    switch (iPosition)
    {
    case 0:
        Copy the input type (YUV) to pMediaType
        return S_OK;
    case 1:
        Construct an RGB type that matches the input type.
        return S_OK;
    default:
        return VFW_S_NO_MORE_ITEMS;
    }
}

// SetMediaType: Override from CTransformFilter. 
HRESULT CMyTransform::SetMediaType(
    PIN_DIRECTION direction, const CMediaType *pmt)
{
    // Capture this information...
    if (direction == PINDIR_OUTPUT)
    {
       m_bYuv = (pmt->subtype == MEDIASUBTYPE_UYVY);
    }
    return S_OK;
}

HRESULT CMyTransform::Transform(
    IMediaSample *pSource, IMediaSample *pDest)
{
    // Look for format changes from downstream.
    CMediaType *pMT = NULL;
    HRESULT hr = pDest->GetMediaType((AM_MEDIA_TYPE**)&pMT);
    if (hr == S_OK)
    {
        hr = m_pOutput->CheckMediaType(pMT);
        if(FAILED(hr))
        {
            DeleteMediaType(pMT);
            return E_FAIL;
        }
        // Notify our own output pin about the new type.
        m_pOutput->SetMediaType(pMT);
        DeleteMediaType(pMT);
    }
    // Process the buffers
    if (m_bYuv) {
        return ProcessFrameYUV(pSource, pDest);
    }
    else {
        return ProcessFrameRGB(pSource, pDest);
    }
}
```



 

 



