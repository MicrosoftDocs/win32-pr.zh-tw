---
description: 步驟 5。
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: 步驟 5。 轉換映射
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609acb626d00dbceea8b6f5bca6af012d8158b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194224"
---
# <a name="step-5-transform-the-image"></a>步驟 5。 轉換映射

這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟5。

上游篩選器會藉由在轉換篩選的輸入釘上呼叫 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法，將媒體範例傳遞給轉換篩選。 若要處理資料，轉換篩選會呼叫 **轉換** 方法，這是單純的虛擬。 **CTransformFilter** 和 **CTransInPlaceFilter** 類別會使用此方法的兩個不同版本：

-   [**CTransformFilter：： Transform**](ctransformfilter-transform.md) 採用輸入範例的指標和輸出範例的指標。 在篩選準則呼叫方法之前，它會將範例屬性從輸入範例複製到輸出範例（包括時間戳記）。
-   [**CTransInPlaceFilter：： Transform**](ctransinplacefilter-transform.md) 會取得輸入範例的指標。 篩選準則會就地修改資料。

如果 **轉換** 方法傳回 S \_ OK，則篩選準則會傳遞範例下游。 若要略過框架，請傳回 \_ FALSE。 如果有資料流程錯誤，則傳回失敗碼。

下列範例顯示 RLE 編碼器可能如何執行此方法。 視您的篩選準則而定，您自己的執行可能會有很大的差異。


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



此範例假設 EncodeFrame 是實作為 RLE 編碼的私用方法。 此處未描述編碼演算法本身;如需詳細資訊，請參閱 Platform SDK 檔中的「點陣圖壓縮」主題。

首先，此範例會呼叫 [**IMediaSample：： GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) 來取出基礎緩衝區的位址。 它會將這些傳遞給私用 EncoderFrame 方法。 然後，它會呼叫 [**IMediaSample：： SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) 來指定編碼資料的長度。 下游篩選器需要此資訊，才能正確地管理緩衝區。 最後，此方法會呼叫 [**IMediaSample：： SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) ，將主要畫面格旗標設定為 **TRUE**。 執行時間長度的編碼不會使用任何差異框架，因此每個畫面格都是主要畫面格。 若為 delta 框架，請將值設定為 **FALSE**。

您必須考慮的其他問題包括：

-   時間戳記。 **CTransformFilter** 類別會在呼叫 **轉換** 方法之前，先將輸出範例加上時間戳記。 它會從輸入範例複製時間戳記值，而不加以修改。 如果您的篩選準則需要變更時間戳記，請在輸出範例上呼叫 [**IMediaSample：： SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) 。
-   格式變更。 上游篩選器可以將媒體類型附加至範例，以變更中型串流的格式。 在這麼做之前，它會在您篩選的輸入 pin 上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 。 在 **CTransformFilter** 類別中，這會導致對 **CheckInputType** 的呼叫，後面接著 **CheckTransform**。 下游篩選也可以使用相同的機制來變更媒體類型。 在您自己的篩選準則中，有兩件事要注意：

    -   請確定 **QueryAccept** 不會傳回 false 接受。
    -   如果您的篩選準則接受格式變更，請呼叫 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)，在 **轉換** 方法內檢查這些變更。 如果該方法傳回 S \_ OK，則您的篩選準則必須回應格式變更。

    如需詳細資訊，請參閱 [動態格式變更](dynamic-format-changes.md)。

-   執行緒。 在 **CTransformFilter** 和 **CTransInPlaceFilter** 中，轉換篩選 **會在 Receive** 方法內同步傳遞輸出範例。 篩選不會建立任何背景工作執行緒來處理資料。 通常，轉換篩選不會建立背景工作執行緒。

下一 [步：步驟6。新增對 COM 的支援](step-6--add-support-for-com.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 DirectShow 篩選器](writing-directshow-filters.md)
</dt> </dl>

 

 



