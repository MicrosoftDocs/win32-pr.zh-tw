---
title: 網頁問題
description: 網頁問題
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Windows Media 中繼檔播放清單，網頁
- 播放清單、網頁
- 中繼檔播放清單，網頁
- Windows Media 中繼檔播放清單，自訂 HTMLView
- 播放清單，自訂 HTMLView
- 中繼檔播放清單，自訂 HTMLView
- Windows Media 中繼檔播放清單，HTMLView 自訂
- 播放清單，HTMLView 自訂
- 中繼檔播放清單，HTMLView 自訂
- 自訂 HTMLView
- Windows Media Player，網頁
- Windows Media Player，自訂 HTMLView
- Windows Media Player，HTMLView 自訂
- HTMLView，自訂
- HTMLView，網頁
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675135"
---
# <a name="web-page-issues"></a>網頁問題

當您建立要顯示在 Windows Media Player **Now 播放** 功能的網頁時，需要考慮一些事項。 本節將討論一些您在建立 Web 內容時可能會遇到的問題。

## <a name="customizing-htmlview"></a>自訂 HTMLView

您的 HTMLView 網頁可以像您的需要一樣簡單或複雜。 您可以在 Web 內容中包含任何通常使用的元素。 如果您內嵌 Windows Media Player 控制項，您可以顯示控制項所提供的其中一個使用者介面、使用 HTML 和腳本程式碼建立您自己的使用者介面，或在所有 (不提供任何 UI，這表示使用者可以使用全模式播放程式) 的傳輸控制。

使用 HTMLView 功能所顯示之網頁的建議大小為 575 x 345 圖元。 但是，使用者可以調整 Windows Media Player 並選擇螢幕解析度。 如果 HTMLView 網頁大於「 **立即播放** 」功能所容納的大小，播放程式會顯示水準和垂直捲動條，讓使用者可以看到整個頁面。 您應使用各種螢幕解析度和播放機大小來測試您的 HTMLView 內容，以判斷您的網頁的最佳大小。

Windows Media Player 不提供可讓您指定完整模式播放程式大小的方法。

## <a name="web-page-navigation"></a>網頁流覽

Windows Media Player 不會提供 **立即播放** 功能中所顯示網頁的流覽工具列。 這表示您可以完全掌控使用者是否可以離開 HTMLView 網頁。 如果您想要讓使用者流覽至其他網頁，您必須在 HTML 程式碼中包含元素以提供該功能。

## <a name="retrieving-the-parent-window"></a>正在抓取父視窗

如果您現有的腳本使用 **window** 來取得父視窗物件，此程式碼將無法在您的 HTMLView 網頁中運作。 當您使用 HTMLView 時，不會有父視窗物件;因此，此腳本功能無法使用。

## <a name="about-the-embedded-browser"></a>關於內嵌瀏覽器

由於 Windows Media Player 使用 Internet Explorer 的內嵌實例來顯示 HTMLView 內容，因此 Internet Explorer 的使用者設定和原則會套用至播放程式中顯示的任何網頁。 例如，如果使用者已將 Internet Explorer 設定為防止網頁下載 cookie 至電腦，您的 HTMLView 網頁也會無法執行這項操作。

使用 HTMLView 功能開啟的網頁一律會在 Internet Explorer 的 **網際網路** 安全性區域中執行。

內嵌的網頁瀏覽器控制項使用相同的規則，將網頁快取為 Internet Explorer 的獨立版本。 在建立內容時使用 Active Server Pages (ASP) ，以確保每次 Windows Media Player 存取 HTMLView 網頁時，都會從 web 伺服器提供內容。 使用 ASP 頁面可以像將網頁重新命名為使用 .asp 副檔名一樣簡單。

## <a name="about-local-web-content"></a>關於本機 Web 內容

HTMLView 功能不允許您開啟儲存在使用者電腦上的網頁。

## <a name="prompting-the-user"></a>提示使用者

您可以使用 [ **視窗]** 提示使用者輸入資訊。 但是，當使用 HTMLView 時，無法使用 [**確認** **]** 。

## <a name="timing-issues"></a>計時問題

在 HTMLView 網頁中使用內嵌的 Windows Media Player 控制項時，您可能會遇到計時問題。 在 HTMLView 中，內嵌的播放機控制項會與獨立 Windows Media Player 共用其播放引擎。 獨立播放程式可能會在網頁 (之前開啟並開始播放第一個播放清單專案，因此，Player 控制項) 完成載入。 這表示，如果您處理 **OpenStateChange** 或 **PlayStateChange** 事件，腳本將不會收到這些事件的事件通知，除非已載入 Player 控制項和其相關聯的物件。

您可以在程式碼中採取步驟來延遲播放，直到 Windows Media Player 控制項具現化為止。 執行這項作業的其中一種方式是讓中繼檔播放清單中的第一個專案指向影像檔案，並將檔案的持續時間設定為允許播放程式控制項載入的時間長度。 下列範例程式碼示範這個選項：


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



當上述播放清單開啟時，Windows Media Player 等候播放清單中的第一個專案在播放程式載入 HTMLView 網頁時最多一分鐘。

接下來，在您的 HTMLView 網頁中撰寫腳本程式碼，以處理本文 **專案的** **onload** 事件。 在事件處理常式函式中，呼叫 Player **Controls. Next** 方法以開始播放播放清單中的第二個專案。


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



當上述範例中的網頁完成載入時，Windows Media Player 立即前進到播放清單中的第二個專案。 這會覆寫播放清單中第一個元素所指定的持續時間，這表示使用者不需要等待一分鐘，就能看到所需的內容。他或她只需要等待網頁載入完成。 由於 Player 控制項現在會完全具現化，因此 **OpenStateChange** 和 **PlayStateChange** 事件可以用平常的方式處理。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**顯示 Windows Media Player 中的網頁**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**PlayStateChange 事件**](player-player-playstatechange.md)
</dt> <dt>

[**OpenStateChange 事件**](player-player-openstatechange.md)
</dt> </dl>

 

 




