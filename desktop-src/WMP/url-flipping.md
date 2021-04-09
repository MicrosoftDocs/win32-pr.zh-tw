---
title: URL 翻轉
description: URL 翻轉
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "103676015"
---
# <a name="url-flipping"></a>URL 翻轉

使用投影片放映的網頁稱為 URL 翻轉，並會在遇到內嵌于所播放數位媒體資料流程中的 URL 指令碼命令時由 Windows Media Player 自動處理。 您可以在每個指令碼命令中指定頁面的目標框架，也可以藉由設定 **defaultFrame** 屬性來指定。 您可以在腳本中設定此屬性，或在內嵌 Windows Media Player 控制項的 OBJECT 元素內使用 PARAM 專案。

您可以自由處理 JScript 程式碼中的 URL 指令碼命令，就像處理自訂指令碼命令一樣。 如果您希望 Windows Media Player 控制項忽略 URL 指令碼命令，讓您可以自行處理它們，請設定 *設定。* 如先前所述，在腳本中或使用 PARAM 元素， **invokeURLs** 屬性設為 false。

下列範例說明 URL 翻轉的一般框架。 首先，建立描述該框架的頁面：


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



接下來，使用下列程式碼來建立在框架組中參考的 player.html 檔案 (會假設將該 .wmv 檔案存在於與 HTML 檔案) 相同的目錄中：


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



如果您的網頁夠小而無法快速載入，則此設定可能足以滿足您的需求。 另一方面，如果您的網頁很複雜，則視物件的連線速度而定，豐富的媒體串流可能會更有效率。

> [!Note]  
> URL 翻轉無法在 Netscape Navigator 中看到的頁面上正確運作。 在 [導覽器] 中接收的每個 URL 指令碼命令都會在新的瀏覽器視窗中顯示 URL，而不是顯示在 **defaultFrame** 指定的框架中。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Web-Based 簡報**](creating-web-based-presentations.md)
</dt> <dt>

[**使用腳本來控制 URL 翻轉**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




