---
title: 在網頁中編寫腳本的簡單範例
description: 在網頁中編寫腳本的簡單範例
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player ActiveX 控制項、網頁
- Windows Media Player 的行動 ActiveX 控制項、網頁
- ActiveX 控制項，網頁
- Windows Media Player ActiveX 控制項，腳本範例
- Windows Media Player Mobile ActiveX 控制項，腳本範例
- ActiveX 控制項，腳本範例
- 內嵌、網頁
- 網頁內嵌、腳本範例
- 網頁內嵌的腳本範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "106996359"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a>在網頁中編寫腳本的簡單範例

您可以使用瀏覽器辨識的任何指令碼語言，輕鬆地將 Windows Media Player 控制項內嵌在 HTML 檔案中。 下列簡單的範例會使用 Microsoft JScript 來建立頁面，當您按一下按鈕時，就會播放該檔案，然後在您按一下另一個按鈕時停止播放該檔案。

您可以使用下列四個步驟，將 Windows Media Player 的 ActiveX 控制項內嵌到網頁中：

1.  建立網頁。
2.  加入物件標記。
3.  新增使用者介面。 在此案例中，有兩個按鈕。
4.  新增幾行程式碼，以便在使用者按一下您所建立的其中一個按鈕時回應。

## <a name="creating-the-web-page"></a>建立網頁

第一個步驟是建立有效的 HTML 網頁。 若要建立空白但有效的 HTML 網頁，至少需要下列程式碼：


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a>加入物件標記

建立網頁之後，您需要新增物件標記。 這會識別瀏覽器的 ActiveX 控制項，並設定任何初始定義。 您必須將物件標記放在程式碼主體中。 如果您將它放在主體中，就會顯示 Windows Media Player 的預設使用者介面。 如果您想要建立自己的使用者介面，請將 [高度] 和 [寬度] 屬性設定為 0 (零) 。 您也可以設定 *播放機*。當您想要隱藏控制項，但仍在頁面上保留空間時， **uiMode** 屬性為「隱藏」。 當您提供自訂使用者介面時，建議使用下列程式碼：


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



以下是必要的物件標記屬性：

識別碼

程式碼的其他部分將用來識別和使用 ActiveX 控制項的名稱。 您可以選擇任何想要的名稱，只要它是 HTML、HTML 延伸名或您所使用的指令碼語言尚未使用的名稱。 在此範例中，會使用名稱 "Player"，但您也可以將它稱為 "MyPlayer" 或其他名稱。 只挑選該網頁的唯一名稱。

CLASSID

非常大的十六進位數位，對控制項而言是唯一的。 只有一個控制項具有此數目，而這是 Windows Media Player 的 ActiveX 控制項。 若要避免打字錯誤，您可以從檔中複製並貼上此編號。 7.0 版之前的 Windows Media Player 控制項版本具有不同的 CLASSID。

## <a name="adding-a-user-interface"></a>新增消費者介面

HTML 允許大量的使用者介面元素，讓使用者可以按一下、按下按鍵和其他使用者動作，與您的網頁互動。 新增幾個輸入按鈕是提供快速使用者介面最簡單的方式。 下列程式碼會建立可回應使用者的兩個按鈕。 按一下其中一個按鈕會啟動媒體資料流程播放，另一個按鈕則會將它停止：


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



按鈕的名稱是用來識別程式碼的按鈕;值是將會出現在按鈕上的標籤，而 OnClick 屬性會識別在按下按鈕時，會呼叫腳本程式碼的哪個部分。

## <a name="adding-scripting-code"></a>新增腳本程式碼

腳本程式碼可將互動功能新增至您的網頁。 腳本程式碼可以回應事件、呼叫方法，以及變更執行時間屬性。 擴充的腳本會包含在腳本標記集內。 腳本標記會告知瀏覽器您的腳本處理常式代碼，並識別指令碼語言。 如果您未識別語言，則預設語言會是 Microsoft JScript。

將腳本放在 HTML 註解標記中是不錯的撰寫作法，因此不支援腳本的瀏覽器不會將您的程式碼轉譯為文字。 將腳本標記放在 HTML 檔案主體內的任何位置，然後將批註括住的程式碼內嵌在開頭和結尾腳本標記內。

下列 Microsoft JScript 程式碼範例會呼叫 Windows Media Player 控制項，並執行適當的動作來回應對應的按鈕點擊。


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



當按一下標示為播放的按鈕時，會呼叫 StartMeUp 函式，並在按下 [停止] 按鈕時呼叫 ShutMeDown 函數。

StartMeUp 內的程式碼會使用 URL 屬性來定義媒體的路徑。 媒體將立即開始播放。

ShutMeDown 程式碼會呼叫 **Controls** 物件的 **stop** 方法。 請注意，**控制項** 物件是透過 **Player** 物件的 **controls** 屬性來呼叫，其 ID 值為 "player"。

下列程式碼顯示完整範例。


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



請注意，您必須在 [URL] 屬性中提供有效的 URL 給有效的檔案名。 在此情況下，假設檔案 laure 與 HTML 檔案位於相同的目錄中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**在 Web 網頁中使用 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




