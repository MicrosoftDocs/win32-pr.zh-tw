---
title: 確保 Windows Media Player 開啟 HTMLView 內容
description: 確保 Windows Media Player 開啟 HTMLView 內容
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Windows Media 中繼檔播放清單，Windows Media Player 開啟 HTMLView 內容
- 播放清單，Windows Media Player 開啟 HTMLView 內容
- 中繼檔播放清單，Windows Media Player 開啟 HTMLView 內容
- Windows Media 中繼檔播放清單，開啟 HTMLView 內容
- 播放清單，開啟 HTMLView 內容
- 中繼檔播放清單，開啟 HTMLView 內容
- 開啟 HTMLView 內容
- Windows Media Player，開啟 HTMLView 內容
- Windows Media Player，HTMLView 內容
- HTMLView，開啟內容
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673516"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a>確保 Windows Media Player 開啟 HTMLView 內容

目前，Windows Media Player 9 系列和 Windows Media Player 10 是唯一支援 .asx 檔案中 *HTMLView* 參數的播放程式。 這表示您應該採取步驟，以確保 HTMLView 內容會在這些版本的 Windows Media Player 中播放。

您必須先判斷是否已在使用者的電腦上安裝 Windows Media Player 9 系列或 Windows Media Player 10。 Windows Media Player SDK 包含完整的範例，示範如何在不同的網頁瀏覽器中偵測不同版本的 Windows Media Player。 雖然偵測範例的完整分析已超出本節的範圍，但您可以採取一些基本步驟來判斷使用者電腦執行的 Windows Media Player 版本。

偵測 Windows Media Player 的最簡單方式，就是在網頁中內嵌 Player 控制項，以連結至您的 HTMLView 內容，然後檢查 *播放* 程式所抓取的值。**versionInfo** 屬性。 確認使用者已安裝 Windows Media Player 9 系列或 Windows Media Player 10 之後，您就可以使用 [openPlayer](player-openplayer.md) 方法來開啟全模式播放程式中的內容。 **OpenPlayer** 方法可確保您的內容一開始會顯示在全模式播放程式的「**立即播放**」功能中，而不是在面板、迷你播放程式模式下，或是另一個已註冊為 .asx 副檔名之檔案的預設程式，但不支援 HTMLView 的播放程式中顯示。 不過，在顯示內容之後，使用者可以完全掌控 Windows Media Player，這表示他或她可以選擇顯示 [ **立即播放**] 以外的功能、切換至 [面板] 模式，或甚至結束播放程式。

下列程式碼範例會建立 Internet Explorer 的網頁。 此頁面會開啟 .asx 檔案，此檔案會指定在安裝 Windows Media Player 9 系列或更新版本時，在全模式播放程式中出現的 HTMLView 網頁。


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



上述範例中的程式碼會內嵌 Windows Media Player 控制項，並將 **uiMode** 屬性設定為「隱藏」，而「播放程式高度」和「寬度」屬性則設定為零。 這是因為網頁不需要一開始就顯示播放程式控制項使用者介面，它只需要存取 Player 物件模型。 頁面也會顯示 [輸入] 按鈕，讓使用者播放 .asx 檔。

當使用者按一下 [Play .ASX] 按鈕時，會執行 Microsoft JScript 函數 PlayASX。 此函式會先取得 Player **versionInfo** 屬性的值，方法是使用 JScript **parseInt** 方法檢查所抓取字串的數值。 如果數值大於或等於 9 (表示使用者已) 安裝 Windows Media Player 9 系列，腳本會呼叫 **openPlayer** 方法，並傳遞包含 HTMLView 參數之 .asx 檔案的 URL。 這個方法會使用 [完整] 模式中的 Windows Media Player 來開啟 .asx 檔案、在 .asx 播放清單中播放數位媒體內容，並在 [ **立即播放** ] 功能中顯示 HTMLView 的網頁內容。

如果版本字串的數值不大於或等於 9 (表示使用者未在其電腦上安裝 Windows Media Player 9 系列或更新版本) 。腳本程式碼會將 Player 控制項的 **uiMode** 變更為「完整」、設定控制項的新寬度和高度，然後藉由指定 **URL** 屬性的值，在內嵌的播放程式中開啟 .asx 檔。 發生這種情況時，會在網頁中播放數位媒體內容，但會忽略在 .asx 檔案中指定的任何 HTMLView 值。

當使用者未安裝 Windows Media Player 9 系列或 Windows Media Player 10 時，如何播放內容的方式是由您自行決定。 上述範例顯示如何指定在網頁中播放內容，而不是在全模式播放程式中，忽略進程中的任何 HTMLView 內容。 還有其他您可能會採用的方法。 例如，您可以提示使用者安裝較新版本的 Windows Media Player，讓該版本的播放程式能夠播放數位媒體內容。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**顯示 Windows Media Player 中的網頁**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**UiMode**](player-uimode.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 




