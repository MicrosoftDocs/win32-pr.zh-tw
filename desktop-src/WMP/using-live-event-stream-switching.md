---
title: 使用即時事件串流切換
description: 使用即時事件串流切換
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
keywords:
- Windows媒體中繼檔播放清單，實況活動資料流切換
- 播放清單、實況活動資料流切換
- 中繼檔播放清單，即時事件資料流程切換
- Windows媒體中繼檔播放清單，事件資料流程切換
- 播放清單、事件資料流程切換
- 中繼檔播放清單，事件資料流程切換
- Windows媒體中繼檔播放清單，廣告插入
- 播放清單、廣告插入
- 中繼檔播放清單，廣告插入
- Windows Media Player，即時事件串流切換
- Windows Media Player，事件資料流程切換
- Windows Media Player，ad 插入
- 即時事件資料流程切換
- 事件資料流程切換
- 廣告插入
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8524fe1a83a6b3276c274726fa27fa7fcccb97b88f0384a54e5433d09380501
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134361"
---
# <a name="using-live-event-stream-switching"></a>使用即時事件串流切換

串流媒體也可以透過中繼檔播放清單中 Windows 媒體中繼檔元素的媒體串流中內嵌的指令碼命令互動來控制。

事件是內嵌于媒體資料流程或媒體檔案中的特定指令碼命令類型。 當 Windows Media Player 控制項收到指令碼命令時，它會依照中繼檔播放清單中的 **事件** 專案所定義的方式來處理事件。 Windows Media Player 從目前正在轉譯的資料流程切換，並轉譯中繼檔播放清單 **事件** 專案中參考的內容。 **事件** 元素通常用於即時生產環境。

**事件** 元素看起來類似 **專案專案**，但每個專案都以不同的方式處理資料流程和媒體檔案的播放。 **ENTRY** 元素用來建立播放清單。 當前一個 **專案** 中所參考的資料流程或媒體檔案完成時，**專案專案** 中所參考的資料流程或媒體檔案就會開始播放。 只有在收到特定指令碼命令時，才會播放 **事件** 中所參考的資料流程。 例如，當 Windows Media Player 收到 "EVENT" 類型的指令碼命令和命令字串 "Adlink" 時，它會搜尋播放清單中的下列元素。


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



然後 Windows Media Player 從即時串流切換，以播放 **事件** 中包含的資料流程或媒體檔案，在此案例中為 Adlink。 `WHENDONE="RESUME"`當 Adlink 完成時，程式碼會指示 Windows Media Player 繼續播放先前的資料流程。

> [!Note]  
> 無法處理內嵌于媒體資料流程或媒體檔案中的每個事件，可能會產生非預期的結果。

 

如果您想要使用即時事件串流切換，您必須在播放清單中包含一個 **事件** 元素，以處理內嵌在播放清單中媒體串流或媒體檔案中的每個事件指令碼命令。 建立播放清單之前，您必須知道哪些指令碼命令內嵌在數位媒體內容中的詳細資料。 如果有您想要 Windows Media Player 略過的事件指令碼命令，請在播放清單中包含 **事件** 專案來處理事件，但在事件處理常式中參考虛擬 URL。

## <a name="ad-insertion"></a>廣告插入

這項技術可用於廣告插入。 例如，在廣播遊戲的即時網際網路廣播期間，會在每個商業中斷的開頭傳送一個命令，指示每個用戶端 (Windows Media Player) 播放播放清單中所列的電視廣告。 當用戶端完成播放電視廣告時，播放清單會指示每個用戶端剪回即時廣播。 只有當所存取的串流媒體以相符的 **事件** 名稱廣播內嵌腳本時，才會轉譯 **事件** 媒體內容。

藉由對比廣告如何透過標準的無線廣播來觸達檢視器，以及廣告如何使用 Windows 媒體技術來觸達檢視器，以獲得最佳的 **事件** 切換潛力。 在過去，廣播廣告只能以檢視器為目標，並使用評等資料作為主要準則。 使用 Windows 媒體技術傳送的 Ads 可以直接以目標使用者為目標，因為 **事件** 和播放清單可以根據使用者輸入即時建立。 如需詳細資訊，請參閱 [個人化媒體傳遞](personalizing-media-delivery.md)。

您也可以使用中繼檔播放清單來顯示自訂圖形、音訊和文字以進行廣告。 您可以使用 **橫幅** 元素作為 **事件** 的子項目，以顯示廣告訊息圖形。 **橫幅** 元素會提供路徑和檔案，其中包含您廣告橫幅的圖形。 您也可以使用 **MOREINFO** 子項目提供網站或檔案的連結。 **MOREINFO** 元素中的 URL 可以提供網路上更多廣告的連結。 下列範例將示範如何使用這些元素。

範例程式碼


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



下列範例會在用戶端收到 **名稱** 屬性設為 "Time Out" 的指令碼命令 **事件** 時，將 ad 廣告插入廣播單播資料流程改觀中。 **CLIENTSKIP** 設定為 [否]，以防止略過資料流程的廣告。 在此範例中，必須先播放經過資料流程處理的廣告，然後再返回原始資料流程。 當廣告完成時，用戶端會繼續播放原始資料流程。

範例程式碼


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**使用中繼檔播放清單**](using-metafile-playlists.md)
</dt> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




