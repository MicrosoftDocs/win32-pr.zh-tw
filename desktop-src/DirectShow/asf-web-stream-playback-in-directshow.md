---
description: 在 DirectShow 中播放 ASF Web 串流
ms.assetid: c7818c62-24af-4eac-84b8-f76be4ca6c09
title: 在 DirectShow 中播放 ASF Web 串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d14a83d2baf9c11aa824f5d6358f62790c16b30
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317751"
---
# <a name="asf-web-stream-playback-in-directshow"></a>在 DirectShow 中播放 ASF Web 串流

Microsoft DirectShow 透過 [WM ASF 讀取](wm-asf-reader-filter.md) 器篩選器在檔案播放案例中支援 web 串流，但您必須撰寫自己的 DirectShow 篩選器來捕捉和保存資料流程。

> [!Note]  
> 若要在從執行 Windows Media Services 的伺服器串流處理的內容中播放 web 串流，請使用內嵌在網頁中的 Windows Media Player 9 系列 ActiveX®控制項。

 

當提供包含 WMMEDIATYPE FileTransfer 類型資料流程的檔案時 \_ ，WM ASF 讀取器將會為其建立輸出圖釘。 格式區塊將會是 [**WMT \_ WEBSTREAM \_ 格式**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) 結構。  (此結構記載于 Windows Media 格式 SDK 檔集。 ) 如果沒有可用來處理該媒體類型的下游篩選器，則 pin 將保持線上狀態，但檔案仍會播放音訊和/或影片串流。

Web stream 中的每個媒體範例都包含 [**WMT \_ WEBSTREAM \_ 範例 \_ 標頭**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) 結構，其記載于 Windows media Format SDK 檔中。 根據 **wszURL** 成員的長度而定，結構的長度會有變動。 範例資料的指標一開始會指向此結構，而您必須將指標前移到結構的上方，才能存取資料流程中的實際資料。

您的 web 資料流程處理常式篩選應以 [**CBaseRenderer**](cbaserenderer.md) 類別為基礎。 在 [**CBaseRenderer：:D orendersample**](cbaserenderer-dorendersample.md) 方法中，篩選準則將需要剖析結構以取得 web 資料流程的相關資訊，然後執行適當的動作。 一般而言，這會牽涉到將檔案儲存到磁片，然後呼叫 [**CreateUrlCacheEntry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) 和 [**CommitUrlCacheEntryW**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) 或 [**CommitUrlCacheEntryA**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) 函式，將檔案放入 Internet Explorer 快取中。 篩選準則必須處理多部分檔案，也就是大於一個樣本的檔案，而且也必須處理轉譯命令（由 **WMT \_ WEBSTREAM \_ 範例 \_ 標頭 wSampleType** 成員指定）。 篩選準則會將 [**EC \_ OLE \_ 事件**](ec-ole-event.md) 事件傳送至應用程式，以及 **WMT \_ WEBSTREAM \_ 範例標頭的文字 \_ 。 wszURL** 字串，其中包含要轉譯的檔案名。 然後，應用程式會導致瀏覽器顯示指定的頁面。 如果已正確撰寫 web 資料流程，檔案應該已經在快取中。

如需有關 WMT \_ WEBSTREAM \_ FORMAT 和 WMT \_ WEBSTREAM 範例標頭的詳細資訊 \_ \_ ，請參閱 Windows Media FORMAT SDK 檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 DirectShow 中讀取 ASF 檔案](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
