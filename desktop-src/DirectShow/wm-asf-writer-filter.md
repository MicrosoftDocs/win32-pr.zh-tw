---
description: WM ASF 寫入器篩選器
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: 'WM ASF 寫入器篩選器 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9281d09e609bd51bc0d0ab42291bd183e782df447e918d3c478e4e857063c21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650819"
---
# <a name="wm-asf-writer-filter-directshow"></a>WM ASF 寫入器篩選器 (DirectShow) 

WM ASF 寫入器是一種包裝函式篩選器，適用于 Windows 媒體™格式 SDK 提供的寫入器物件。 篩選器會接受數量不定的輸入資料流程，並建立 Advanced 系統格式 (ASF) 檔。 此篩選器會處理所有的壓縮和多工處理 (雖然可以略過壓縮機制) 。 您可以在各種案例中使用 WM ASF 寫入器，包括數位視訊 (DV) 捕捉、音訊 recompression，以及 Audio-Video 交錯式 (AVI) 或 MPEG 多媒體檔案的轉換，以進行網路串流處理。 此篩選器提供在 microsoft DirectShow 中建立 microsoft® Windows 媒體™音訊和 Windows Media 視訊檔案的唯一方法。

如需詳細資訊，請參閱[在 DirectShow 中建立 ASF](creating-asf-files-in-directshow.md)檔。



| 標籤 | 值 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)、 [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2)、 [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 **IPersistStream**、 **IServiceProvider**、 **ISpecifyPropertyPages**，此外，篩選器會公開下列 Windows 媒體格式 SDK 介面： **IWMIndexer2**、 **IWMHeaderInfo**、 **IWMWriterAdvanced2**<br/> |
| 輸入 pin 媒體類型                    | 相依于 ASF 設定檔。 通常未壓縮的音訊和影片類型，雖然篩選準則會在符合 ASF 設定檔的情況下接受壓縮類型。                                                                                                                                                                                                                                                                                                                                             |
| 輸入 pin 介面                     | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass)、 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 **IServiceProvider** 此外，pin 會公開下列 Windows 媒體格式 SDK 介面： **IWMStreamConfig2** (至 **IServiceProvider**) <br/>                                                                                                                                                                                 |
| 輸出 pin 媒體類型                   | 不適用。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 輸出 pin 介面                    | 不適用。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 篩選 CLSID                             | CLSID \_ WMAsfWriter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 屬性頁 CLSID                      | CLSID \_ AsfWriterProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 可執行檔                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [優點](merit.md)                       | \_ \_ 未 \_ 使用的業績                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [篩選準則分類](filter-categories.md) | 未指定                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>備註

篩選準則需要 Windows 媒體格式軟體發展工具組 (SDK) 及其基礎相依性。

在 ASF 資料流程的設定檔或設定檔識別碼上，篩選 dependings 上的輸入圖釘數目。

輸入 pin 支援來自 **IAMStreamConfig** 介面的一種方法： [**IAMStreamConfig：： >iformatprovider.getformat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat)。 所有其他方法都會傳回 E \_ >notimpl。 呼叫 **>iformatprovider.getformat** 方法來查詢釘選的目的地壓縮格式，此格式是由目前的 ASF 設定檔所定義。 使用 [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) 介面設定設定檔。

您可以使用篩選器的 **IServiceProvider** 介面來取得 **IWMWriterAdvanced2** 介面的指標，該介面是在 Windows 媒體格式 SDK 中定義。 您可以使用 **IWMWriterAdvanced2** 介面來控制來源影片交錯時的影片去交錯。 若要設定去交錯模式，請呼叫 **IWMWriterAdvanced2：： SetInputSetting**。 針對 *dwInputNum* 參數，請使用影片輸入圖釘以零為基底的索引，如 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面所列舉。

下列範例顯示如何查詢此介面：


```C++
// Assume that pAsfWriter is a valid IBaseFilter pointer.
IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = pAsfWriter->QueryInterface(
    IID_IServiceProvider, 
    (void**)&pProvider
    );
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(
        IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, 
        (void**)&pWMWA2
        );
    pProvider->Release();
    if (SUCCEEDED(hr))
    {
        // Use pWMWA2. (Not shown.)
        pWMWA2->Release();
    }
}
```



應用程式不應使用 **IWMWriterAdvanced2** 介面所繼承的任何 **IWMWriterAdvanced** 方法。 呼叫任何這些方法時，可以使用篩選準則來 interere。

此篩選器所支援的唯一檔案寫入模式是檔案 \_ \_ 覆寫。 請參閱 [**IFileSinkFilter2：： GetMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode)。

當 Windows 媒體格式 SDK 執行時間將 WMT \_ 狀態訊息傳送至 WM ASF 寫入器篩選器時，篩選器會將它們轉送為 [**EC \_ WMT \_ 事件**](ec-wmt-event.md)事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 




