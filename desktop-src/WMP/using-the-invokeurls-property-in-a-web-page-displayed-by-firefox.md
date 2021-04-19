---
title: 在 Firefox 所顯示的網頁中使用 invokeURLs 屬性
description: 在 Firefox 所顯示的網頁中使用 invokeURLs 屬性
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- Windows Media Player ActiveX 控制項、網頁
- Windows Media Player 的行動 ActiveX 控制項、網頁
- Windows Media Player ActiveX 控制項，invokeURLs 屬性
- Windows Media Player 行動 ActiveX 控制項，invokeURLs 屬性
- 內嵌、網頁
- 網頁嵌入、invokeURLs 屬性
- Windows Media Player，Firefox
- Windows Media Player 物件模型，Firefox
- 物件模型，Firefox
- Windows Media Player ActiveX 控制項，Firefox
- ActiveX 控制項、Firefox
- Firefox，invokeURLs 屬性
- 網頁內嵌、Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0a2eb96e65d8fa6d2758669e3c844b2d13c0bc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "106966007"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="e21ea-122">在 Firefox 所顯示的網頁中使用 invokeURLs 屬性</span><span class="sxs-lookup"><span data-stu-id="e21ea-122">Using the invokeURLs Property in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="e21ea-123">有些媒體檔案包含內嵌的 Url，當媒體檔案播放時，Windows Media Player 會在網頁瀏覽器視窗或框架中顯示網頁。</span><span class="sxs-lookup"><span data-stu-id="e21ea-123">Some media files contain embedded URLs for which Windows Media Player displays webpages in a Web browser window or frame as the media file plays.</span></span> <span data-ttu-id="e21ea-124">在 Windows Internet Explorer 中，您可以使用 [invokeURLs](settings-invokeurls.md) 屬性來指定是否要針對內嵌 url 顯示頁面，而且您可以使用 [defaultFrame](settings-defaultframe.md) 屬性來指定顯示這類頁面的畫面格。</span><span class="sxs-lookup"><span data-stu-id="e21ea-124">In Windows Internet Explorer, you can use the [Settings.invokeURLs](settings-invokeurls.md) property to specify whether pages are displayed for embedded URLs, and you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify a frame for displaying such pages.</span></span>

<span data-ttu-id="e21ea-125">在 Firefox 中，需要一些因應措施才能設定 **invokeURLs** 屬性，以及指定框架來顯示內嵌 url 的頁面。</span><span class="sxs-lookup"><span data-stu-id="e21ea-125">In Firefox, some workarounds are required to set the **invokeURLs** property and to specify a frame for displaying pages for embedded URLs.</span></span>

## <a name="setting-the-invokeurls-property"></a><span data-ttu-id="e21ea-126">設定 invokeURLs 屬性</span><span class="sxs-lookup"><span data-stu-id="e21ea-126">Setting the invokeURLs property</span></span>

<span data-ttu-id="e21ea-127">**InvokeURLs** 屬性的預設值為 true，因此，如果您想要將值設為 false，則必須明確設定該值。</span><span class="sxs-lookup"><span data-stu-id="e21ea-127">The default value of the **Settings.invokeURLs** property is true, so if you want the value to be false, you must set it explicitly.</span></span> <span data-ttu-id="e21ea-128">在 Internet Explorer 中，您可以在 Player 控制項的物件專案內的 PARAM 專案中，將 **invokeURLs** 設定為 false。</span><span class="sxs-lookup"><span data-stu-id="e21ea-128">In Internet Explorer, you can set **invokeURLs** to false in a PARAM element inside the Player control's OBJECT element.</span></span>

<span data-ttu-id="e21ea-129">Firefox 外掛程式不支援在 PARAM 元素中設定 **invokeURLs** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e21ea-129">The Firefox plug-in does not support setting the **invokeURLs** property in a PARAM element.</span></span>

<span data-ttu-id="e21ea-130">您可以藉由在腳本中設定 **invokeURLs** 屬性來解決這項限制。</span><span class="sxs-lookup"><span data-stu-id="e21ea-130">You can work around this limitation by setting the **invokeURLs** property in script.</span></span> <span data-ttu-id="e21ea-131">下列程式碼會示範如何將網頁中的 **invokeURLs** 屬性設定為 false，以供 Internet Explorer 和 Firefox 同時顯示。</span><span class="sxs-lookup"><span data-stu-id="e21ea-131">The following code shows how to set the **invokeURLs** property to false in a webpage that can be displayed by both Internet Explorer and Firefox.</span></span>


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



## <a name="displaying-webpages-in-a-frame"></a><span data-ttu-id="e21ea-132">在框架中顯示網頁</span><span class="sxs-lookup"><span data-stu-id="e21ea-132">Displaying webpages in a frame</span></span>

<span data-ttu-id="e21ea-133">媒體檔案可以包含在播放媒體檔案時，在瀏覽器視窗或框架中顯示網頁的 Url。</span><span class="sxs-lookup"><span data-stu-id="e21ea-133">A media file can contain URLs that display webpages in a browser window or frame as the media file is played.</span></span> <span data-ttu-id="e21ea-134">在 Internet Explorer 中，您可以使用 [defaultFrame](settings-defaultframe.md) 屬性來指定顯示這些頁面的框架。</span><span class="sxs-lookup"><span data-stu-id="e21ea-134">In Internet Explorer, you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify the frame in which those pages are displayed.</span></span> <span data-ttu-id="e21ea-135">如果您未設定 **defaultFrame** 屬性，則會在預設瀏覽器的另一個視窗中顯示 url。</span><span class="sxs-lookup"><span data-stu-id="e21ea-135">If you do not set the **defaultFrame** property, URLs are displayed in a separate window of the default browser.</span></span> <span data-ttu-id="e21ea-136">不過，Firefox 外掛程式不支援 **defaultFrame** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e21ea-136">However, the Firefox plug-in does not support the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="e21ea-137">若要解決這項限制，請將 **invokeURLs** 屬性設定為 false，並撰寫可設定目標框架位置的 [ScriptCommand](player-player-scriptcommand.md) 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="e21ea-137">To work around this limitation, set the **Settings.invokeURLs** property to false and write a [ScriptCommand](player-player-scriptcommand.md) event handler that sets the location of the target frame.</span></span> <span data-ttu-id="e21ea-138">下列範例會在 Internet Explorer 和 Firefox 中運作，並說明這項技巧。</span><span class="sxs-lookup"><span data-stu-id="e21ea-138">The following example, which works in Internet Explorer and Firefox, illustrates this technique.</span></span> <span data-ttu-id="e21ea-139">假設範例中所顯示的網頁是在畫面格 \[ 0 \] ，而您想要 URL 的頁面顯示在畫面格 \[ 1 中 \] 。</span><span class="sxs-lookup"><span data-stu-id="e21ea-139">Assume that the webpage shown in the example is in frames\[0\] and you want the URL's page to be displayed in frames\[1\].</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e21ea-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="e21ea-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e21ea-141">**搭配 Firefox 使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="e21ea-141">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




