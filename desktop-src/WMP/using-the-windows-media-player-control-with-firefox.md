---
title: 搭配 Firefox 使用 Windows Media Player 控制項
description: 搭配 Firefox 使用 Windows Media Player 控制項
ms.assetid: a95529d6-7508-4e27-adfe-bbbf4dcaffce
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
ms.openlocfilehash: 253dd21312409fe2c97bf94c36397efed8353bdb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383098"
---
# <a name="using-the-windows-media-player-control-with-firefox"></a><span data-ttu-id="36484-123">搭配 Firefox 使用 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="36484-123">Using the Windows Media Player Control with Firefox</span></span>

<span data-ttu-id="36484-124">Microsoft 提供一個外掛程式，可讓您將 Windows Media Player 的 ActiveX 控制項內嵌在網頁中，讓 Firefox 瀏覽器能夠正確地顯示該控制項。</span><span class="sxs-lookup"><span data-stu-id="36484-124">Microsoft provides a plug-in that enables you to embed the Windows Media Player ActiveX control in a webpage so that it will be displayed correctly by a Firefox browser.</span></span> <span data-ttu-id="36484-125">您可以從 [Microsoft Port25 網站](https://www.mozilla.org/)下載外掛程式（必須安裝在用戶端電腦上）。</span><span class="sxs-lookup"><span data-stu-id="36484-125">The plug-in, which must be installed on the client computer, can be downloaded from the [Microsoft Port25 website](https://www.mozilla.org/).</span></span>

<span data-ttu-id="36484-126">如需 Firefox 瀏覽器的詳細資訊，請參閱 [firefox 網站](https://www.mozilla.org/)。</span><span class="sxs-lookup"><span data-stu-id="36484-126">For information about the Firefox browser, see the [Firefox website](https://www.mozilla.org/).</span></span>

<span data-ttu-id="36484-127">如需有關搭配 Firefox 使用 Windows Media Player 的詳細資訊，請參閱 [mozillaZine 網站](http://kb.mozillazine.org/Windows_Media_Player)的 Windows Media Player 一節。</span><span class="sxs-lookup"><span data-stu-id="36484-127">For more information about using Windows Media Player with Firefox, see the Windows Media Player section of the [mozillaZine website](http://kb.mozillazine.org/Windows_Media_Player).</span></span>

<span data-ttu-id="36484-128">下列主題描述如何將 Windows Media Player 控制項內嵌在可由 Internet Explorer 和 Firefox 正確顯示的網頁中。</span><span class="sxs-lookup"><span data-stu-id="36484-128">The following topics describe how to embed the Windows Media Player control in a webpage that can be displayed correctly by both Internet Explorer and Firefox.</span></span>



| <span data-ttu-id="36484-129">主題</span><span class="sxs-lookup"><span data-stu-id="36484-129">Topic</span></span>                                                                                                                                    | <span data-ttu-id="36484-130">描述</span><span class="sxs-lookup"><span data-stu-id="36484-130">Description</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36484-131">將播放機控制項內嵌在 Firefox 所顯示的網頁中</span><span class="sxs-lookup"><span data-stu-id="36484-131">Embedding the Player Control in a Web Page Displayed by Firefox</span></span>](embedding-the-player-control-in-a-web-page-displayed-by-firefox.md)   | <span data-ttu-id="36484-132">描述如何撰寫腳本，以建立與 Internet Explorer 和 Firefox 相容的物件元素。</span><span class="sxs-lookup"><span data-stu-id="36484-132">Describes how write script that creates an OBJECT element that is compatible with both Internet Explorer and Firefox.</span></span> |
| [<span data-ttu-id="36484-133">在 Firefox 所顯示的網頁中使用 PARAM 元素</span><span class="sxs-lookup"><span data-stu-id="36484-133">Using PARAM Elements in a Web Page Displayed by Firefox</span></span>](using-param-elements-in-a-web-page-displayed-by-firefox.md)                   | <span data-ttu-id="36484-134">描述 Firefox 外掛程式所支援的 PARAM 元素。</span><span class="sxs-lookup"><span data-stu-id="36484-134">Describes the PARAM elements that are supported by the Firefox plug-in.</span></span>                                               |
| [<span data-ttu-id="36484-135">在 Firefox 所顯示的網頁中使用腳本</span><span class="sxs-lookup"><span data-stu-id="36484-135">Using Script in a Web Page Displayed by Firefox</span></span>](using-script-in-a-web-page-displayed-by-firefox.md)                                   | <span data-ttu-id="36484-136">描述 Firefox 外掛程式所支援的 Windows Media Player 物件。</span><span class="sxs-lookup"><span data-stu-id="36484-136">Describes the Windows Media Player objects that are supported by the Firefox plug-in.</span></span>                                 |
| [<span data-ttu-id="36484-137">在 Firefox 所顯示的網頁中處理事件</span><span class="sxs-lookup"><span data-stu-id="36484-137">Handling Events in a Web Page Displayed by Firefox</span></span>](handling-events-in-a-web-page-displayed-by-firefox.md)                             | <span data-ttu-id="36484-138">描述如何在由 Firefox 顯示的網頁中撰寫腳本，以處理 Windows Media Player 事件。</span><span class="sxs-lookup"><span data-stu-id="36484-138">Describes how to write script, in a webpage displayed by Firefox, that handles Windows Media Player events.</span></span>           |
| [<span data-ttu-id="36484-139">在 Firefox 所顯示的網頁中使用 invokeURLs 屬性</span><span class="sxs-lookup"><span data-stu-id="36484-139">Using the invokeURLs Property in a Web Page Displayed by Firefox</span></span>](using-the-invokeurls-property-in-a-web-page-displayed-by-firefox.md) | <span data-ttu-id="36484-140">描述如何在 Firefox 所顯示的網頁中回應 URL 類型的指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="36484-140">Describes how to respond to URL-type script commands in a webpage displayed by Firefox.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="36484-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="36484-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36484-142">**在 Web 網頁中使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="36484-142">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




