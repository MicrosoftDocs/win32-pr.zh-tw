---
description: WM ASF 讀取器篩選器
ms.assetid: 82b9f849-b9dc-439b-8ca7-9dcd992338ab
title: " (DirectShow) 的 WM ASF 讀取器篩選器"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35cea4b6dbf8c720f3059e0317484fd2f34d10
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908866"
---
# <a name="wm-asf-reader-filter-directshow"></a> (DirectShow) 的 WM ASF 讀取器篩選器

「WM ASF 讀取器」是 Windows Media Format SDK 所提供之讀取器物件的包裝函式篩選器，也是建議用來播放 Windows Media 內容的檔案，以及使用任何 Microsoft MPEG 4 編碼器 DMOs 所建立內容的建議來源篩選器。



| 標籤 | 值 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)、 [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking)、 **IServiceProvider**，此外，此篩選器會公開下列 Windows Media 格式 SDK 介面： [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)、 [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)、 [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)、 [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) (到 **IServiceProvider**) <br/> |
| 輸入 pin 媒體類型                    | 不適用。                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 輸入 pin 介面                     | 不適用。                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 輸出 pin 媒體類型                   | 媒體媒體、媒體媒體 \_ \_ 、媒體媒體 \_ SCRIPTCOMMAND、媒體媒體 \_ FileTransfer                                                                                                                                                                                                                                                                                                                                                                                                     |
| 輸出 pin 介面                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass)、 **IServiceProvider**，此外，釘選會公開下列 Windows Media 格式 SDK 介面： **IWMStreamConfig2** (到 **IServiceProvider**) <br/>                                                                                                                                                                                                                                    |
| 篩選 CLSID                             | CLSID \_ WMAsfReader                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 屬性頁 CLSID                      | 沒有屬性頁。                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 可執行檔                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [優點](merit.md)                       | 不 \_ 太可能                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>備註

提供 ASF 檔案或 URL 的名稱時，WM ASF 讀取器會讀取壓縮的內容、剖析壓縮的資料流程，並公開每一個輸出的輸出圖釘。 此篩選器會將下游連接到音訊及/或影片編解碼器篩選器，以進行解壓縮。 如果 ASF 檔案是可搜尋的，則支援搜尋。 ASF 讀取器時間會在將範例傳送至下游之前將它們加上戳記，但不會以任何方式修改時間戳記。

不支援以 [**IMediaSeeking：： SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) 中所指定的 1.0 (速度來播放。

當 Windows Media Format SDK 執行時間將 [**WMT \_ 狀態**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_status) 消息傳送至 WM ASF 寫入器篩選器時，篩選器會將任何與 DRM 授權取得相關的訊息轉送為 [**EC \_ WMT \_ 事件**](ec-wmt-event.md) 事件。 如需詳細資訊，請參閱 [在 DirectShow 中讀取 DRM-Protected 的 ASF](reading-drm-protected-asf-files-in-directshow.md)檔案。

WM ASF 讀取器會部分執行 [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) 和 [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) 介面，以便讓應用程式能夠存取 Reader 物件上的參考方法。 篩選準則的執行只會將呼叫傳遞至讀取器物件上的介面。 因為篩選準則必須具有串流處理常式的完整控制權，所以不會實作為串流方法。 下列方法會實作為：

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced：： SetClientInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[在 DirectShow 中讀取 ASF 檔案](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
