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
# <a name="url-flipping"></a><span data-ttu-id="4929f-120">URL 翻轉</span><span class="sxs-lookup"><span data-stu-id="4929f-120">URL Flipping</span></span>

<span data-ttu-id="4929f-121">使用投影片放映的網頁稱為 URL 翻轉，並會在遇到內嵌于所播放數位媒體資料流程中的 URL 指令碼命令時由 Windows Media Player 自動處理。</span><span class="sxs-lookup"><span data-stu-id="4929f-121">Using webpages for slide shows is called URL flipping, and is handled automatically by Windows Media Player when it encounters URL script commands embedded in the digital media stream it is playing.</span></span> <span data-ttu-id="4929f-122">您可以在每個指令碼命令中指定頁面的目標框架，也可以藉由設定 **defaultFrame** 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="4929f-122">You can specify a target frame for your pages in each script command, or you can specify it by setting the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="4929f-123">您可以在腳本中設定此屬性，或在內嵌 Windows Media Player 控制項的 OBJECT 元素內使用 PARAM 專案。</span><span class="sxs-lookup"><span data-stu-id="4929f-123">You can set this property in script code or by using a PARAM element within the OBJECT element that embeds the Windows Media Player control.</span></span>

<span data-ttu-id="4929f-124">您可以自由處理 JScript 程式碼中的 URL 指令碼命令，就像處理自訂指令碼命令一樣。</span><span class="sxs-lookup"><span data-stu-id="4929f-124">You are free to handle the URL script commands in your JScript code just as you would handle custom script commands.</span></span> <span data-ttu-id="4929f-125">如果您希望 Windows Media Player 控制項忽略 URL 指令碼命令，讓您可以自行處理它們，請設定 *設定。* 如先前所述，在腳本中或使用 PARAM 元素， **invokeURLs** 屬性設為 false。</span><span class="sxs-lookup"><span data-stu-id="4929f-125">If you want the Windows Media Player control to ignore URL script commands so that you can handle them entirely by yourself, set the *Settings*.**invokeURLs** property to false either in script code or using a PARAM element as previously described.</span></span>

<span data-ttu-id="4929f-126">下列範例說明 URL 翻轉的一般框架。</span><span class="sxs-lookup"><span data-stu-id="4929f-126">The following example illustrates a typical frameset for URL flipping.</span></span> <span data-ttu-id="4929f-127">首先，建立描述該框架的頁面：</span><span class="sxs-lookup"><span data-stu-id="4929f-127">First, create a page that describes the frameset:</span></span>


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



<span data-ttu-id="4929f-128">接下來，使用下列程式碼來建立在框架組中參考的 player.html 檔案 (會假設將該 .wmv 檔案存在於與 HTML 檔案) 相同的目錄中：</span><span class="sxs-lookup"><span data-stu-id="4929f-128">Next, create the player.html file referenced in the frameset by using the following code (the video.wmv file is assumed to exist in the same directory as the HTML files):</span></span>


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



<span data-ttu-id="4929f-129">如果您的網頁夠小而無法快速載入，則此設定可能足以滿足您的需求。</span><span class="sxs-lookup"><span data-stu-id="4929f-129">If your webpages are small enough to load rapidly, this setup may be sufficient for your needs.</span></span> <span data-ttu-id="4929f-130">另一方面，如果您的網頁很複雜，則視物件的連線速度而定，豐富的媒體串流可能會更有效率。</span><span class="sxs-lookup"><span data-stu-id="4929f-130">If, on the other hand, your webpages are complex, rich media streaming may be more effective depending on the connection speed of your audience.</span></span>

> [!Note]  
> <span data-ttu-id="4929f-131">URL 翻轉無法在 Netscape Navigator 中看到的頁面上正確運作。</span><span class="sxs-lookup"><span data-stu-id="4929f-131">URL flipping does not work correctly with pages viewed in Netscape Navigator.</span></span> <span data-ttu-id="4929f-132">在 [導覽器] 中接收的每個 URL 指令碼命令都會在新的瀏覽器視窗中顯示 URL，而不是顯示在 **defaultFrame** 指定的框架中。</span><span class="sxs-lookup"><span data-stu-id="4929f-132">Instead of appearing in the frame specified by **defaultFrame**, each URL script command received in Navigator displays the URL in a new browser window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4929f-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="4929f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4929f-134">**建立 Web-Based 簡報**</span><span class="sxs-lookup"><span data-stu-id="4929f-134">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="4929f-135">**使用腳本來控制 URL 翻轉**</span><span class="sxs-lookup"><span data-stu-id="4929f-135">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




