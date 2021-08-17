---
title: 在 Firefox 所顯示的網頁中處理事件
description: 在 Firefox 所顯示的網頁中處理事件
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
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
- Windows Media Player ActiveX 控制項、事件處理
- Windows Media PlayerMobile ActiveX 控制項，事件處理
- ActiveX 控制項，事件處理
- 內嵌、網頁
- 網頁嵌入、事件處理
- Windows Media Player，Firefox
- Windows Media Player 物件模型，Firefox
- 物件模型，Firefox
- Windows Media PlayerMobile、Firefox
- Windows Media Player ActiveX control、Firefox
- Windows Media PlayerMobile ActiveX control、Firefox
- ActiveX control、Firefox
- Firefox，事件處理
- 網頁內嵌、Firefox
- 事件，Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e971caef18114b670678fc76d0515858bee77a94a5e3f8b5c24ca5322177b8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748413"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>在 Firefox 所顯示的網頁中處理事件

當您在網頁中內嵌 Windows Media Player 控制項時，您可以撰寫腳本來處理事件。 如需播放程式控制項所引發的事件清單，請參閱 [Player 物件](player-object.md)。

如果與內嵌播放機控制項相關聯的 mime 類型為 application/x-------您可以撰寫具有下列格式的事件處理常式：


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



其中 *，事件名稱* 是 Windows Media Player 事件的名稱，而 *Params* 是事件的參數清單。 例如，下列程式碼具有 [PlayStateChange](player-player-playstatechange.md) 事件的處理常式。


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



如果網頁上有數個 Player 控制項的實例，而且您使用上述範例所示的格式，則每個事件處理常式都會系結至播放機控制項的特定實例。 在前面的範例中，只有當 id = "Player" 的控制項播放狀態變更時，才會呼叫事件處理常式。

如果與內嵌播放機控制項相關聯的 mime 類型不是 application/x-ms-chap，您可以撰寫具有下列格式的事件處理常式：


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



其中 *，事件名稱* 是 Windows Media Player 事件的名稱，而 *Params* 是事件的參數清單。 例如，下列程式碼具有 **PlayStateChange** 事件的處理常式。


```HTML
<OBJECT id="Player" type="application/asx" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Test.asx"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT>
  function OnDSPlayStateChangeEvt(NewState)
  {
    p1.innerHTML = "Play state: " + NewState;
  }
</SCRIPT>

```



如果網頁上有數個 Player 控制項的實例，而且您使用上述範例中所示的格式，則每個事件處理常式都會系結至播放機控制項的所有實例，並在頁面上的任何播放機控制項播放狀態變更時呼叫事件處理常式。

> [!Note]  
> 如果 mime 類型不是 application/x-ms-chap， **DoubleClick** 事件就會傳送為 OnDSDblClickEvt (not OnDSDoubleClickEvt) ，以與 Player 控制項6.4 版相容。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**搭配 Firefox 使用 Windows Media Player 控制項**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




