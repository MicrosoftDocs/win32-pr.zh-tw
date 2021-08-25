---
description: 關於 WM ASF Reader 篩選器
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: 關於 WM ASF Reader 篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b71d0b25070c446ebff88f18785df7b55ba7bbcc7b1bcaa1dcf21995185252ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873698"
---
# <a name="about-the-wm-asf-reader-filter"></a>關於 WM ASF Reader 篩選器

ASF 檔案的播放是由 [WM Asf 讀取](wm-asf-reader-filter.md) 器篩選器所處理。 當 WM ASF 讀取器讀取檔案時，它會自動建立每個資料流程的輸出針腳，包括 web 資料流程、指令碼命令資料流程，以及任何其他類型的任意資料流程。 如果是多位元率檔案，則只會針對目前選取的資料流程建立 pin。 若要使用 WM ASF 讀取器篩選器來播放 ASF 檔案，請呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 或 [**IGraphBuilder：： AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)。

WM ASF 讀取器支援 DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)介面，可讓應用程式在檔案內執行時態搜尋。 但是，不支援以 [**IMediaSeeking：： SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) 中所指定的 1.0 (速度來播放。

WM ASF 讀取器篩選器也會公開數個 Windows 媒體格式 SDK 介面，如下表所述。 這些介面記載于 Windows 媒體格式 SDK 檔中。



| 介面                                             | 公開的方式                                 | 註解                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | 透過篩選器上的 **IServiceProvider** 。 | 針對需要播放由數位 Rights Management (DRM) 所保護之內容的應用程式提供。                             |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | 篩選上的 **QueryInterface** 。           | 提供讓應用程式可以讀取檔案和內容屬性，以及標記和腳本資訊和中繼資料。     |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | 篩選上的 **QueryInterface** 。           | 部分實作為篩選準則，讓應用程式可以存取 WM 讀取器物件上的資訊方法。         |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | 篩選上的 **QueryInterface** 。           | 部分實作為篩選器，讓應用程式可以存取格式 SDK 讀取器物件上的參考方法。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 中讀取 ASF 檔案](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



