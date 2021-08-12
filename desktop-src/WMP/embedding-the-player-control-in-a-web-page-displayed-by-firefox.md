---
title: 將播放機控制項內嵌在 Firefox 所顯示的網頁中
description: 將播放機控制項內嵌在 Firefox 所顯示的網頁中
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- Windows Media Player，內嵌 ActiveX 控制項
- Windows Media Player 物件模型，內嵌 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media PlayerMobile、內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項、內嵌
- Windows Media PlayerMobile ActiveX 控制項，內嵌
- ActiveX 控制項，內嵌
- Windows Media Player ActiveX 控制項、網頁
- Windows Media PlayerMobile ActiveX 控制項、網頁
- ActiveX 控制項，網頁
- Windows Media Player，Firefox
- Windows Media Player 物件模型，Firefox
- 物件模型，Firefox
- Windows Media PlayerMobile、Firefox
- Windows Media Player ActiveX control、Firefox
- Windows Media PlayerMobile ActiveX control、Firefox
- ActiveX control、Firefox
- Firefox，關於網頁內嵌
- 內嵌、網頁
- 網頁內嵌、Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c1db799df78cb6c62516798f4bbd196c093f02225386f0c1009bfa11d9a668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578585"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>將播放機控制項內嵌在 Firefox 所顯示的網頁中

若要將 Windows Media Player 控制項內嵌在可由 Firefox 瀏覽器顯示的網頁中，請建立物件元素或包含下列其中一個 mime 類型的內嵌元素作為其 **類型** 屬性：

-   application/x-ms-wmp
-   應用程式/asx
-   影片/x-毫秒-asf-外掛程式
-   應用程式/x-mplayer2
-   video/x-ms-asf
-   影片/x-ms-wm
-   音訊/x-ms-wma
-   音訊/x-地板蠟
-   影片/x-ms-wmv
-   影片/x-300k.wvx

慣用的 mime 類型為 application/x----wmp。

下列範例示範如何使用物件專案或內嵌元素來內嵌播放機控制項。


```HTML
<OBJECT id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320">
  <PARAM name="autostart" value="false"/>
</OBJECT>

<EMBED id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320"
  autostart="false"/>

```



上述範例適用于 Firefox，但不在 Internet Explorer 中。 若要將播放機控制項內嵌在可由 Internet Explorer 顯示的網頁中，您必須建立一個物件專案，將 **classid** 屬性設定為 Windows Media Player 控制項的類別識別碼。

下列範例示範如何將 Windows Media Player 控制項內嵌在可由 Internet Explorer 和 Firefox 正確顯示的網頁中。 頁面上的腳本會偵測瀏覽器類型，並產生適當的物件標記。


```HTML
<HTML>
  <BODY>
    <SCRIPT type="text/javascript">
      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {
        document.write('<OBJECT id="Player"');
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');
        document.write(' width=300 height=200></OBJECT>');
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {
        document.write('<OBJECT id="Player"'); 
        document.write(' type="application/x-ms-wmp"'); 
        document.write(' width=300 height=200></OBJECT>');
      }         
    </SCRIPT>
  </BODY>
</HTML>

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**搭配 Firefox 使用 Windows Media Player 控制項**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




