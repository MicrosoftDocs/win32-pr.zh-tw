---
description: 步驟 4：
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: 步驟 4： 設定配置器屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32d5e3affba32b96dc93cb97e1886322bc6f2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981195"
---
# <a name="step-4-set-allocator-properties"></a>步驟 4： 設定配置器屬性

這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟4。

> [!Note]  
> 衍生自 **CTransInPlaceFilter** 的篩選不需要此步驟。

 

在兩個 pin 在媒體類型上同意之後，他們會選取連接的配置器和協調配置器屬性，例如緩衝區大小和緩衝區數目。

在 **CTransformFilter** 類別中，有兩個配置器，一個用於上游連線，另一個用於下游連接。 上游篩選器會選取上游配置器，也會選擇配置器屬性。 輸入 pin 會接受上游篩選器所決定的任何內容。 如果您需要修改此行為，請覆寫 [**CBaseInputPin：： NotifyAllocator**](cbaseinputpin-notifyallocator.md) 方法。

轉換篩選器的輸出釘選會選取下游配置器。 它會執行下列步驟：

1.  如果下游篩選器可以提供配置器，則輸出 pin 會使用該配置器。 否則，輸出 pin 會建立新的配置器。
2.  如果任何) 呼叫 [**IMemInputPin：： GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements)，輸出釘選會取得下游篩選器的配置器需求 (。
3.  輸出圖釘會呼叫轉換篩選器的 [**CTransformFilter：:D ecidebuffersize**](ctransformfilter-decidebuffersize.md) 方法，這是純虛擬的方法。 此方法的參數是配置器的指標，以及具有下游篩選準則需求的配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構。 如果下游篩選器沒有配置器需求，則會將結構清空。
4.  在 **DecideBufferSize** 方法中，衍生類別會藉由呼叫 [**IMemAllocator：： SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties)來設定配置器屬性。

一般而言，衍生的類別會根據輸出格式、下游篩選準則的需求，以及篩選準則本身的需求，來選取配置器屬性。 請嘗試選取與下游篩選器要求相容的屬性。 否則，下游篩選可能會拒絕連接。

在下列範例中，RLE 編碼器會設定緩衝區大小、緩衝區對齊和緩衝區計數的最小值。 針對前置詞，它會使用下游篩選要求的任何值。 前置詞通常是零個位元組，但有些篩選器需要它。 例如， [AVI Mux](avi-mux-filter.md) 篩選器會使用前置詞來寫入 RIFF 標頭。


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



配置器可能無法完全符合您的要求。 因此， **SetProperties** 方法會以個別的配置器 **\_ 屬性** 結構傳回實際的結果， () 上一個範例中的 *實際* 參數。 即使在 **SetProperties** 成功時，您也應該檢查結果，以確定它們符合您篩選準則的最低需求。

**自訂配置器**

根據預設，所有篩選準則類別都會使用 [**CMemAllocator**](cmemallocator.md) 類別進行其配置器。 這個類別會使用 **VirtualAlloc**) ，從用戶端進程的虛擬位址空間配置記憶體 (。 如果您的篩選準則需要使用其他種類的記憶體（例如 DirectDraw 表面），您可以執行自訂配置器。 您可以使用 [**CBaseAllocator**](cbaseallocator.md) 類別，或是撰寫全新的配置器類別。 如果您的篩選準則有自訂配置器，請根據使用配置器的 pin 碼覆寫下列方法：

-   輸入 pin： [**CBaseInputPin：： GetAllocator**](cbaseinputpin-getallocator.md) 和 [**CBaseInputPin：： NotifyAllocator**](cbaseinputpin-notifyallocator.md)。
-   輸出 pin： [**CBaseOutputPin：:D ecideallocator**](cbaseoutputpin-decideallocator.md)。

如果另一個篩選器拒絕使用您的自訂配置器進行連線，則您的篩選器可能會使連接失敗，或其他篩選器的配置器。 在後者的情況下，您可能需要設定一個指示配置器類型的內部旗標。 如需此方法的範例，請參閱 [**CDrawImage 類別**](cdrawimage.md)。

下一 [步：步驟5。轉換映射](step-5--transform-the-image.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 DirectShow 篩選器](writing-directshow-filters.md)
</dt> </dl>

 

 



