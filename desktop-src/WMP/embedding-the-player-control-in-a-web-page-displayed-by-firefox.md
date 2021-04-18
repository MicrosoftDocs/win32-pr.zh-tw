---
title: 將播放機控制項內嵌在 Firefox 所顯示的網頁中
description: 將播放機控制項內嵌在 Firefox 所顯示的網頁中
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
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
- Windows Media Player，Firefox
- Windows Media Player 物件模型，Firefox
- 物件模型，Firefox
- Windows Media Player Mobile、Firefox
- Windows Media Player ActiveX 控制項，Firefox
- Windows Media Player Mobile ActiveX 控制項，Firefox
- ActiveX 控制項、Firefox
- Firefox，關於網頁內嵌
- 內嵌、網頁
- 網頁內嵌、Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16063ea07a0262ab798e58ed02e4d5a5b6b5d65
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "106965198"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="794e6-123">將播放機控制項內嵌在 Firefox 所顯示的網頁中</span><span class="sxs-lookup"><span data-stu-id="794e6-123">Embedding the Player Control in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="794e6-124">若要將 Windows Media Player 控制項內嵌在可由 Firefox 瀏覽器顯示的網頁中，請建立物件元素或包含下列其中一個 mime 類型的內嵌元素作為其 **類型** 屬性：</span><span class="sxs-lookup"><span data-stu-id="794e6-124">To embed the Windows Media Player control in a webpage that can be displayed by a Firefox browser, create an OBJECT element or an EMBED element that has one of the following mime types as its **type** attribute:</span></span>

-   <span data-ttu-id="794e6-125">application/x-ms-wmp</span><span class="sxs-lookup"><span data-stu-id="794e6-125">application/x-ms-wmp</span></span>
-   <span data-ttu-id="794e6-126">應用程式/asx</span><span class="sxs-lookup"><span data-stu-id="794e6-126">application/asx</span></span>
-   <span data-ttu-id="794e6-127">影片/x-毫秒-asf-外掛程式</span><span class="sxs-lookup"><span data-stu-id="794e6-127">video/x-ms-asf-plugin</span></span>
-   <span data-ttu-id="794e6-128">應用程式/x-mplayer2</span><span class="sxs-lookup"><span data-stu-id="794e6-128">application/x-mplayer2</span></span>
-   <span data-ttu-id="794e6-129">video/x-ms-asf</span><span class="sxs-lookup"><span data-stu-id="794e6-129">video/x-ms-asf</span></span>
-   <span data-ttu-id="794e6-130">影片/x-ms-wm</span><span class="sxs-lookup"><span data-stu-id="794e6-130">video/x-ms-wm</span></span>
-   <span data-ttu-id="794e6-131">音訊/x-ms-wma</span><span class="sxs-lookup"><span data-stu-id="794e6-131">audio/x-ms-wma</span></span>
-   <span data-ttu-id="794e6-132">音訊/x-地板蠟</span><span class="sxs-lookup"><span data-stu-id="794e6-132">audio/x-ms-wax</span></span>
-   <span data-ttu-id="794e6-133">影片/x-ms-wmv</span><span class="sxs-lookup"><span data-stu-id="794e6-133">video/x-ms-wmv</span></span>
-   <span data-ttu-id="794e6-134">影片/x-300k.wvx</span><span class="sxs-lookup"><span data-stu-id="794e6-134">video/x-ms-wvx</span></span>

<span data-ttu-id="794e6-135">慣用的 mime 類型為 application/x----wmp。</span><span class="sxs-lookup"><span data-stu-id="794e6-135">The preferred mime type is application/x-ms-wmp.</span></span>

<span data-ttu-id="794e6-136">下列範例示範如何使用物件專案或內嵌元素來內嵌播放機控制項。</span><span class="sxs-lookup"><span data-stu-id="794e6-136">The following examples show how to embed the Player control using an OBJECT element or an EMBED element.</span></span>


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



<span data-ttu-id="794e6-137">上述範例適用于 Firefox，但不在 Internet Explorer 中。</span><span class="sxs-lookup"><span data-stu-id="794e6-137">The preceeding examples work in Firefox but not in Internet Explorer.</span></span> <span data-ttu-id="794e6-138">若要將播放機控制項內嵌在可由 Internet Explorer 顯示的網頁中，您必須建立一個物件專案，將 **classid** 屬性設定為 Windows Media Player 控制項的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="794e6-138">To embed the Player control in a webpage that can be displayed by Internet Explorer, you must create an OBJECT element that has a **classid** attribute set to the class ID of the Windows Media Player control.</span></span>

<span data-ttu-id="794e6-139">下列範例示範如何將 Windows Media Player 控制項內嵌在可由 Internet Explorer 和 Firefox 正確顯示的網頁中。</span><span class="sxs-lookup"><span data-stu-id="794e6-139">The following example shows how to embed the Windows Media Player control in a webpage that can be displayed correctly by both Internet Explorer and Firefox.</span></span> <span data-ttu-id="794e6-140">頁面上的腳本會偵測瀏覽器類型，並產生適當的物件標記。</span><span class="sxs-lookup"><span data-stu-id="794e6-140">Script on the page detects the browser type and generates the appropriate OBJECT tag.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="794e6-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="794e6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="794e6-142">**搭配 Firefox 使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="794e6-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




