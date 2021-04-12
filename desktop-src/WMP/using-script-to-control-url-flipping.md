---
title: 使用腳本來控制 URL 翻轉
description: 使用腳本來控制 URL 翻轉
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Windows Media Player，以網路為基礎的簡報
- Windows Media Player 物件模型，以網路為基礎的簡報
- 物件模型，以 Web 為基礎的簡報
- Windows Media Player 行動裝置、以網路為基礎的簡報
- Windows Media Player ActiveX 控制項，以 Web 為基礎的簡報
- Windows Media Player 的行動 ActiveX 控制項，以網路為基礎的簡報
- ActiveX 控制項，以網頁為基礎的簡報
- Windows Media Player，URL 翻轉
- Windows Media Player 物件模型，URL 翻轉
- 物件模型，URL 翻轉
- Windows Media Player 行動裝置，URL 翻轉
- Windows Media Player ActiveX 控制項，URL 翻轉
- Windows Media Player 的行動 ActiveX 控制項、URL 翻轉
- ActiveX 控制項，URL 翻轉
- 以網頁為基礎的簡報，URL 翻轉
- 建立以網路為基礎的簡報，URL 翻轉
- URL 翻轉
- Windows Media Player，豐富的媒體串流
- Windows Media Player 物件模型，多媒體串流
- 物件模型，多媒體串流
- Windows Media Player Mobile、豐富的媒體串流
- Windows Media Player ActiveX 控制項，豐富的媒體串流
- Windows Media Player 的行動 ActiveX 控制項、豐富的媒體串流
- ActiveX 控制項，豐富的媒體串流
- 以網路為基礎的簡報，豐富的媒體串流
- 建立以網路為基礎的簡報、豐富的媒體串流
- 豐富的媒體串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4815562bba92d67bb4b02ea0317d6c29accd9262
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "104372721"
---
# <a name="using-script-to-control-url-flipping"></a>使用腳本來控制 URL 翻轉

當使用者在資料流程已經在進行時連線到豐富的媒體串流時，如果 Windows Media Player 自動叫用 URL，資料流程處理的網頁就可能會顯示在所有元素之前，並快取。 發生這種情況時，使用者會看到空白或不完整的網頁，直到下一組資料抵達快取為止。

您可以使用腳本叫用 URL，而不是讓 Windows Media Player 自動進行，以避免顯示空白或不完整的網頁。 如此一來，您可以忽略第一個 URL 翻轉，然後使用腳本程式碼叫用後續的 Url。

> [!Note]  
> 本節假設您是使用 Windows Media 編碼器9系列 SDK 來串流 HTML，而且您已將 HTML 資料流程設定為重複。

 

首先，您必須建立框架網頁，以包含具有內嵌播放程式的框架，以及顯示串流 HTML 的框架。 這兩個畫面格一開始會顯示另一個網頁，因此您總共會建立三個網頁。 下列範例程式碼示範框架網頁：


```HTML
<HTML>
<HEAD>
</HEAD>

<FRAMESET cols = "350, *">
  <FRAME  name = "player" src = "embed_player.htm">
  <FRAME  name = "content" src = "blank.htm">

  <NOFRAMES>
  <BODY>

  <P>This page uses frames, but your browser doesn't support them.</P>

  </BODY>
  </NOFRAMES>

</FRAMESET>
</HTML>

```



上述的網頁範例結合兩個框架。 第一個畫面格會顯示在瀏覽器視窗的左半部，並顯示名為 [內嵌player.htm] 的網頁 \_ 。 下列程式碼範例會建立這個網頁：


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

<!-- Embed Windows Media Player and disable the invokeURLs parameter -->
<OBJECT CLASSID = "CLSID:6BF52A52-394A-11D3-B153-00C04F79FAA6" ID = "Player">
  <PARAM name = "URL"  value = "https://www.proseware.com/Media/video.wmv">
  <PARAM name = "invokeURLs"  value = "false">
</OBJECT>

<SCRIPT LANGUAGE = "JScript">
  var bFirstURL = true; // Global flag for first URL flip.
</SCRIPT>

<!-- Create an event handler for script commands. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player" EVENT = "ScriptCommand(scType, scParam)">

  if("URL" == scType)
  {
    if ( bFirstURL == false )
    {
      // Show the next URL flip.
      parent.content.location = scParam;
    }
    else
    {
      bFirstURL = false; // Set the flag.
    }
  }

</SCRIPT>

</BODY>
</HTML>

```



框架中的第二個畫面格會顯示在瀏覽器視窗的上半部，並顯示名為 "blank.htm" 的網頁。 下列程式碼範例會建立這個網頁：


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



當框架頁面在瀏覽器中載入時，左邊的框架會顯示內嵌的播放機，右邊的框架則顯示「正在載入 ...」文字通知使用者即將推出更多資料。 當第一個 URL 指令碼命令從 HTML 資料流程抵達時，事件處理常式只會變更 **布林** 值旗標的值。 當每個後續的 URL 指令碼命令從 HTML 資料流程抵達時，事件處理常式中的腳本會將新的 URL 載入名為 "content" 的框架，而完整的網頁會顯示在瀏覽器視窗上半部的框架中。

如需有關使用 Windows Media 來串流 HTML 的詳細資訊，請參閱 Windows Media 編碼器 SDK。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**豐富的媒體串流**](rich-media-streaming.md)
</dt> <dt>

[**URL 翻轉**](url-flipping.md)
</dt> </dl>

 

 




