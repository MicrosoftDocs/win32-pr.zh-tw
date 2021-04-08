---
title: 在 DirectShow 中播放 Web 串流
description: 在 DirectShow 中播放 Web 串流
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- Windows Media Format SDK、DirectShow
- Windows Media Format SDK，Web 串流播放
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) 、Web stream 播放
- ASF (Advanced Systems Format) 、Web stream 播放
- DirectShow，Web 串流播放
- Web 串流，DirectShow
- Web 串流，在 DirectShow 中播放
- 串流，在 DirectShow 中播放 Web 串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932035"
---
# <a name="web-stream-playback-in-directshow"></a>在 DirectShow 中播放 Web 串流

Microsoft DirectShow 支援 Web 串流 (查看 [Web 串流](web-streams.md) ，以取得透過 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選檔案播放案例中) 的詳細資訊，但您必須撰寫自己的 DirectShow 篩選器來捕捉和保存資料流程。

> [!Note]  
> 若要在從執行 Windows Media Services 的伺服器串流處理的內容中播放 Web 串流，請使用內嵌在網頁中的 Windows Media Player 9 系列 ActiveX®控制項。

 

當提供包含 WMMEDIATYPE FileTransfer 類型資料流程的檔案時 \_ ，WM ASF 讀取器將會為其建立輸出圖釘。 格式區塊將會是 [**WMT \_ WEBSTREAM \_ 格式**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) 結構。 如果沒有可用來處理該媒體類型的下游篩選器，則 pin 將保持未連線，但檔案仍會播放音訊和/或影片串流。

請務必瞭解，Web stream 中的每個媒體範例都包含 [**WMT \_ WEBSTREAM \_ 範例 \_ 標頭**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) 結構，此結構的長度取決於其 **wszURL** 成員的長度。 範例資料的指標一開始會指向此結構，而您必須將指標前移到結構的上方，才能存取資料流程中的實際資料。 您的 Web 資料流程處理常式篩選應以 **CBaseRenderer** 類別為基礎。 在 **DoRenderSample** 方法中，篩選準則將需要剖析結構以取得 Web 資料流程的相關資訊，然後執行適當的動作。 一般而言，這會牽涉到將檔案儲存到磁片，然後呼叫 **CommitUrlCacheEntry** 和 **CreateUrlCacheEntry** 將檔案放入 Internet Explorer 快取中。 篩選準則必須處理多部分檔案，也就是大於一個樣本的檔案，而且也必須處理轉譯命令（由 **WMT \_ WEBSTREAM \_ 範例 \_ 標頭 wSampleType** 成員指定）。 篩選準則會將 **EC \_ OLE \_ 事件** 連同 **WMT \_ WEBSTREAM \_ 範例 \_ 標頭** 的文字傳送至應用程式。 wszURL 字串包含要轉譯的檔案名。 然後，應用程式會導致瀏覽器顯示指定的頁面。 如果已正確撰寫 Web 資料流程，檔案應該已經在快取中。

如需有關 **CBaseRenderer**、 **DoRenderSample** 和 **EC \_ OLE \_ 事件** 的詳細資訊，請參閱 DirectShow SDK 檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Web 串流**](web-streams.md)
</dt> </dl>

 

 




