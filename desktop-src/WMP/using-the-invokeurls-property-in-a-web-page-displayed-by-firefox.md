---
title: 在 Firefox 所顯示的網頁中使用 invokeURLs 屬性
description: 在 Firefox 所顯示的網頁中使用 invokeURLs 屬性
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Windows Media Player，內嵌 ActiveX 控制項
- Windows Media Player 物件模型，內嵌 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media PlayerMobile、內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項、內嵌
- Windows Media PlayerMobile ActiveX 控制項，內嵌
- Windows Media Player ActiveX 控制項、網頁
- Windows Media PlayerMobile ActiveX 控制項、網頁
- Windows Media Player ActiveX control、invokeURLs 屬性
- Windows Media PlayerMobile ActiveX control、invokeURLs 屬性
- 內嵌、網頁
- 網頁嵌入、invokeURLs 屬性
- Windows Media Player，Firefox
- Windows Media Player 物件模型，Firefox
- 物件模型，Firefox
- Windows Media Player ActiveX control、Firefox
- ActiveX control、Firefox
- Firefox，invokeURLs 屬性
- 網頁內嵌、Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2487ebba1ff5664537dbaf0b0abad02a98acecf3c5985f1c09ffe9f8bbb743c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117107"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a>在 Firefox 所顯示的網頁中使用 invokeURLs 屬性

有些媒體檔案包含內嵌的 url，當媒體檔案播放時，Windows Media Player 會在網頁瀏覽器視窗或框架中顯示網頁。 在 Windows Internet Explorer 中，您可以使用[設定 [invokeURLs](settings-invokeurls.md) ] 屬性來指定是否要針對內嵌的 url 顯示頁面，而且您可以[設定使用 defaultFrame](settings-defaultframe.md)屬性來指定顯示這類頁面的畫面格。

在 Firefox 中，需要一些因應措施才能設定 **invokeURLs** 屬性，以及指定框架來顯示內嵌 url 的頁面。

## <a name="setting-the-invokeurls-property"></a>設定 invokeURLs 屬性

invokeURLs 屬性的預設 **設定** 值為 true，因此，如果您想要將值設為 false，則必須明確地設定該值。 在 Internet Explorer 中，您可以在 Player 控制項的物件專案內的 PARAM 專案中，將 **invokeURLs** 設定為 false。

Firefox 外掛程式不支援在 PARAM 元素中設定 **invokeURLs** 屬性。

您可以藉由在腳本中設定 **invokeURLs** 屬性來解決這項限制。 下列程式碼會示範如何將網頁中的 **invokeURLs** 屬性設定為 false，以供 Internet Explorer 和 Firefox 同時顯示。


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

  </BODY>
</HTML>

```



## <a name="displaying-webpages-in-a-frame"></a>在框架中顯示網頁

媒體檔案可以包含在播放媒體檔案時，在瀏覽器視窗或框架中顯示網頁的 Url。 在 Internet Explorer 中，您可以使用[設定 defaultFrame](settings-defaultframe.md)屬性來指定顯示這些頁面的框架。 如果您未設定 **defaultFrame** 屬性，則會在預設瀏覽器的另一個視窗中顯示 url。 不過，Firefox 外掛程式不支援 **設定 defaultFrame** 屬性。 若要解決這項限制，請將 **設定 invokeURLs** 屬性設定為 false，並撰寫可設定目標框架位置的 [ScriptCommand](player-player-scriptcommand.md)事件處理常式。 下列範例會在 Internet Explorer 和 Firefox 中運作，並說明這項技巧。 假設範例中所顯示的網頁是在畫面格 \[ 0 \] ，而您想要 URL 的頁面顯示在畫面格 \[ 1 中 \] 。


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

    <SCRIPT for="Player" event="ScriptCommand(scType, scParam)">
      if( scType == "URL" )
      {
        parent.frames[1].location = scParam;
      }
    </script>

  </BODY>
</HTML>

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**搭配 Firefox 使用 Windows Media Player 控制項**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




