---
title: 'WM ASF 讀取器篩選器 (Windows 媒體格式 11 SDK) '
description: 瞭解 Windows 媒體格式 11 SDK 的 WM ASF 讀取器篩選器。 查看篩選資訊並查看相關主題。
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows媒體格式 SDK，WM ASF 讀取器
- DirectShow，WM ASF 讀取器
- QASF 篩選，WM ASF 讀取器
- WM ASF 讀取器
- Advanced Systems Format (ASF) 、WM ASF 讀取器
- ASF (Advanced Systems Format) 、WM ASF 讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c825835e6d838a8a5d9b058f8bcf6ef52bd2a3d6a645787e0cf44da0f7573c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844921"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>WM ASF 讀取器篩選器 (Windows 媒體格式 11 SDK) 

當提供 ASF 檔案或 URL 的名稱時，WM ASF 讀取器會讀取壓縮的內容、剖析資料流程，並公開每一個的輸出圖釘。 此篩選器會將下游連接到 Windows Media 音訊或 Windows Media 視訊 DMOs，以進行解壓縮。 如果 ASF 檔案是可搜尋的，則支援搜尋。 WM ASF 讀取器會根據 ASF 檔案中的時間戳記，將時間戳記套用至媒體範例，但不會以任何方式修改時間戳記。 篩選器會在內部使用 Windows 媒體格式讀取器物件來讀取 Windows 媒體內容。

> [!Note]  
> 在 DirectX SDK 中，此篩選器不是 ASF 檔案的預設來源篩選，因此使用該 SDK 時，您不能使用此篩選搭配 **RenderFile** 方法;您必須使用 (CLSID) 的類別識別碼，明確地將它新增至篩選圖形。 這種行為與 Windows 媒體格式 SDK 不同。 當您安裝 Windows 媒體格式 SDK 執行時間程式庫時，會將 WM asf 讀取器註冊為 ASF 檔案的預設篩選器。

 

下表包含有關 WM ASF 讀取器篩選器的資訊，例如它所支援的介面和媒體類型。



|  篩選資訊                      |  類型                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面      | **IBaseFilter**、 **IFileSourceFilter**、 **IServiceProvider**、 **IWMHeaderInfo**、 **IWMReaderAdvanced** (部分實行。 請參閱備註。 ) ， **IWMReaderAdvanced2** (部分實行) 、透過 **IServiceProvider** 的 **IWMDRMReader** ()  |
| 輸入 pin 媒體類型  | 不適用                                                                                                                                                                                                                                |
| 輸入 pin 介面   | 不適用                                                                                                                                                                                                                                |
| 輸出 pin 媒體類型 | 媒體媒體、媒體媒體 \_ \_ 、媒體媒體 \_ SCRIPTCOMMAND、媒體媒體 \_ FileTransfer                                                                                                                                                         |
| 格式類型            | 如果內容是 [*交錯*](wmformat-glossary.md)的，則為 **VIDEOINFOHEADER2** ，否則為 **VIDEOINFOHEADER**                                                                                                                    |
| 輸出 pin 介面  | **IMediaSeeking**、 **IAMWMBufferPass**、 **IServiceProvider**、 **IWMStreamConfig2** (到 **IServiceProvider**)                                                                                                                              |
| 篩選 CLSID           | CLSID \_ WMAsfReader                                                                                                                                                                                                                            |
| 屬性頁 CLSID    | 沒有屬性頁                                                                                                                                                                                                                              |
| 可執行檔             | Qasf.dll                                                                                                                                                                                                                                      |
| 優點                  | 不 \_ 太可能                                                                                                                                                                                                                               |
| 篩選準則分類        | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>備註

WM ASF 讀取器會部分執行 **IWMReaderAdvanced** 和 **IWMReaderAdvanced2** 介面，以便讓應用程式能夠存取 Reader 物件上的參考方法。 篩選準則的執行只會將呼叫傳遞至讀取器物件上的介面。 因為篩選準則必須具有串流處理常式的完整控制權，所以不會實作為串流方法。 下列 **IWMReaderAdvanced** 和 **IWMReaderAdvanced2** 方法會實作為：

-   [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**IWMReaderAdvanced：： SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2::GetBufferProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2::GetDownloadProgress**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2::GetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2::GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2::SetPlayMode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DirectShowQASF 參考**](directshow-qasf-reference.md)
</dt> <dt>

[**在 DirectShow 中讀取 ASF 檔案**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




