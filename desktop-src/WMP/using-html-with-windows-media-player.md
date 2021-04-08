---
title: 使用 HTML 搭配 Windows Media Player
description: 使用 HTML 搭配 Windows Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Windows Media Player、HTML
- Windows Media Player 物件模型，HTML
- 物件模型、HTML
- Windows Media Player ActiveX 控制項，物件模型的 HTML
- ActiveX 控制項，物件模型的 HTML
- Windows Media Player 行動 ActiveX 控制項、物件模型的 HTML
- Windows Media Player Mobile，HTML for object model
- 具有 Windows Media Player 的 HTML
- 網頁嵌入、HTML
- 內嵌、網頁
- 指令碼命令
- URL 翻轉
- 豐富的媒體串流
- 瀏覽器支援
- 顯示網頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cd96932573802d0a75f95a437b2c7284b3de44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840147"
---
# <a name="using-html-with-windows-media-player"></a><span data-ttu-id="e74b7-118">使用 HTML 搭配 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="e74b7-118">Using HTML with Windows Media Player</span></span>

## <a name="overview"></a><span data-ttu-id="e74b7-119">概觀</span><span class="sxs-lookup"><span data-stu-id="e74b7-119">Overview</span></span>

<span data-ttu-id="e74b7-120">使用 HTML 搭配 Windows Media Player 是結合音訊和影片與文字和圖形的絕佳方式。</span><span class="sxs-lookup"><span data-stu-id="e74b7-120">Using HTML with Windows Media Player is an excellent way to combine audio and video with text and graphics.</span></span> <span data-ttu-id="e74b7-121">當您想要補充您的靜態內容或建立具有數位媒體的 Web 應用程式時，可以在網頁中內嵌 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="e74b7-121">You can embed the Windows Media Player control in a webpage when you want to supplement your static content or create Web applications with digital media.</span></span> <span data-ttu-id="e74b7-122">另一方面，如果您想要使用 HTML 來補充您的數位媒體，您可以在 Windows Media 中繼檔播放清單中參考網頁，以播放程式的完整模式顯示網頁。</span><span class="sxs-lookup"><span data-stu-id="e74b7-122">When you want to supplement your digital media with HTML, on the other hand, you can display webpages in the full mode of the Player by referencing them in Windows Media metafile playlists.</span></span>

<span data-ttu-id="e74b7-123">如果您撰寫的自訂程式是以遠端模式內嵌 Windows Media Player 控制項，您也可以在使用者取消停駐控制項時，控制播放程式完整模式的各種窗格中所顯示的網頁。</span><span class="sxs-lookup"><span data-stu-id="e74b7-123">If you write custom programs that embed the Windows Media Player control in remote mode, you can also control the webpages displayed in the various panes of the full mode of the Player when your users undock the control.</span></span> <span data-ttu-id="e74b7-124">這可讓您維持停駐和停駐狀態之間的持續性。</span><span class="sxs-lookup"><span data-stu-id="e74b7-124">This lets you preserve continuity between the docked and undocked states.</span></span>

## <a name="web-embedding"></a><span data-ttu-id="e74b7-125">Web 嵌入</span><span class="sxs-lookup"><span data-stu-id="e74b7-125">Web Embedding</span></span>

<span data-ttu-id="e74b7-126">您可以使用 Windows Media Player 控制項做為您所建立網頁的一部分。</span><span class="sxs-lookup"><span data-stu-id="e74b7-126">You can use the Windows Media Player control as part of a webpage you create.</span></span> <span data-ttu-id="e74b7-127">請參閱 [將 Windows Media Player 控制項內嵌到網頁中](embedding-the-windows-media-player-control-in-a-web-page.md)。</span><span class="sxs-lookup"><span data-stu-id="e74b7-127">See [Embedding the Windows Media Player Control in a Web Page](embedding-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="script-commands-and-url-flipping"></a><span data-ttu-id="e74b7-128">指令碼命令和 URL 翻轉</span><span class="sxs-lookup"><span data-stu-id="e74b7-128">Script Commands and URL Flipping</span></span>

<span data-ttu-id="e74b7-129">指令碼命令是文字/值組，您可以將它內嵌在數位媒體檔案或資料流程中。</span><span class="sxs-lookup"><span data-stu-id="e74b7-129">Script commands are text/value pairs you can embed in your digital media files or streams.</span></span> <span data-ttu-id="e74b7-130">您可以單獨使用自訂指令碼命令來觸發腳本，同時讓 Windows Media Player 自動處理其他指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="e74b7-130">You might use custom script commands solely to trigger script code, while letting Windows Media Player handle other script commands automatically.</span></span>

<span data-ttu-id="e74b7-131">當您有數個隨附數位媒體簡報的網頁時，[URL 腳本] 命令可以在 Windows Media Player 控制項繼續于另一個框架中播放數位媒體時，自動變更一個框架中的頁面。</span><span class="sxs-lookup"><span data-stu-id="e74b7-131">When you have several webpages that accompany a digital media presentation, URL script commands can automatically change the page in one frame while the Windows Media Player control continues playing digital media in another frame.</span></span> <span data-ttu-id="e74b7-132">這稱為 URL 翻轉，是建立多媒體投影片放映的絕佳方式。</span><span class="sxs-lookup"><span data-stu-id="e74b7-132">This is called URL flipping, and is an excellent way to create a multimedia slide show.</span></span> <span data-ttu-id="e74b7-133">其他自動處理的指令碼命令可讓您將播放切換至不同的媒體檔案或資料流程、顯示字幕文字或觸發事件，例如 Windows Media 中繼檔播放清單中定義的廣告插入。</span><span class="sxs-lookup"><span data-stu-id="e74b7-133">Other automatically handled script commands let you switch playback to a different media file or stream, display captioning text, or trigger events such as ad insertions defined in a Windows Media metafile playlist.</span></span>

<span data-ttu-id="e74b7-134">如需有關 URL 翻轉的詳細資訊，請參閱 [建立 Web-Based 簡報](creating-web-based-presentations.md)。</span><span class="sxs-lookup"><span data-stu-id="e74b7-134">For more information about URL flipping, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="rich-media-streaming"></a><span data-ttu-id="e74b7-135">豐富的媒體串流</span><span class="sxs-lookup"><span data-stu-id="e74b7-135">Rich Media Streaming</span></span>

<span data-ttu-id="e74b7-136">URL 翻轉最適合用於快速載入的簡單頁面。</span><span class="sxs-lookup"><span data-stu-id="e74b7-136">URL flipping works best with simple pages that load rapidly.</span></span> <span data-ttu-id="e74b7-137">使用更複雜的頁面時，會個別傳送多個元件，因此很難將頁面顯示與數位媒體進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="e74b7-137">With more complex pages, multiple components are transferred individually, making it difficult to synchronize page display with digital media.</span></span> <span data-ttu-id="e74b7-138">若要允許複雜的多媒體簡報，可將網頁新增至媒體資料流程，並以音訊和影片的相同方式傳送至播放機。</span><span class="sxs-lookup"><span data-stu-id="e74b7-138">To allow complex rich media presentations, webpages can be added to a media stream and delivered to the Player in the same way as audio and video.</span></span> <span data-ttu-id="e74b7-139">這可讓您更輕鬆地同步處理簡報的元件，尤其是透過低速連接。</span><span class="sxs-lookup"><span data-stu-id="e74b7-139">This lets you synchronize the components of your presentation much more easily, especially over low-speed connections.</span></span>

<span data-ttu-id="e74b7-140">如需豐富媒體串流處理的詳細資訊，請參閱 [建立 Web-Based 簡報](creating-web-based-presentations.md)。</span><span class="sxs-lookup"><span data-stu-id="e74b7-140">For more information about rich media streaming, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="browser-support"></a><span data-ttu-id="e74b7-141">瀏覽器支援</span><span class="sxs-lookup"><span data-stu-id="e74b7-141">Browser Support</span></span>

<span data-ttu-id="e74b7-142">您可以在 Microsoft Internet Explorer、Firefox 和 Netscape Navigator 中內嵌 Windows Media Player 控制項，不過每個程式的流程稍微不同。</span><span class="sxs-lookup"><span data-stu-id="e74b7-142">You can embed the Windows Media Player control in Microsoft Internet Explorer, Firefox, and Netscape Navigator, although the process is slightly different for each.</span></span> <span data-ttu-id="e74b7-143">您也可以建立設計來與這三個瀏覽器搭配使用的網頁。</span><span class="sxs-lookup"><span data-stu-id="e74b7-143">You can also create webpages designed to work with all three browsers.</span></span>

<span data-ttu-id="e74b7-144">使用 Internet Explorer 和 Firefox，您可以使用 HTML 物件元素內嵌控制項。</span><span class="sxs-lookup"><span data-stu-id="e74b7-144">With Internet Explorer and Firefox, you embed the control using the HTML OBJECT element.</span></span> <span data-ttu-id="e74b7-145">不過，導覽器需要不同的方法，因為它不會直接支援 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="e74b7-145">Navigator requires a different approach, however, because it doesn't directly support ActiveX controls.</span></span> <span data-ttu-id="e74b7-146">使用 [導覽器] 時，您可以使用 APPLET 元素，將特殊的 JAVA 小程式內嵌到頁面中。</span><span class="sxs-lookup"><span data-stu-id="e74b7-146">With Navigator, you use the APPLET element to embed a special Java applet into the page.</span></span> <span data-ttu-id="e74b7-147">此小程式可處理與播放程式 ActiveX 控制項的通訊。</span><span class="sxs-lookup"><span data-stu-id="e74b7-147">This applet handles communication with the Player ActiveX control.</span></span>

<span data-ttu-id="e74b7-148">如需 Firefox 支援的詳細資訊，請參閱搭配 [Firefox 使用 Windows Media Player 控制項](using-the-windows-media-player-control-with-firefox.md)。</span><span class="sxs-lookup"><span data-stu-id="e74b7-148">For more information about Firefox support, see [Using the Windows Media Player Control with Firefox](using-the-windows-media-player-control-with-firefox.md).</span></span>

<span data-ttu-id="e74b7-149">如需 Netscape Navigator 支援的詳細資訊，請參閱 [使用 Windows Media Player 搭配 Netscape 7.1](using-windows-media-player-with-netscape-7-1.md)。</span><span class="sxs-lookup"><span data-stu-id="e74b7-149">For more information about Netscape Navigator support, see [Using Windows Media Player with Netscape 7.1](using-windows-media-player-with-netscape-7-1.md).</span></span>

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a><span data-ttu-id="e74b7-150">在播放程式的完整模式中顯示網頁</span><span class="sxs-lookup"><span data-stu-id="e74b7-150">Displaying Web Pages in the Full Mode of the Player</span></span>

<span data-ttu-id="e74b7-151">您可以擴充 Windows Media Player 的功能，或在播放程式的完整模式中顯示網頁，以提供數位媒體隨附之資訊的自訂觀點。</span><span class="sxs-lookup"><span data-stu-id="e74b7-151">You can extend the functionality of Windows Media Player or provide a custom view of information that accompanies your digital media by displaying webpages in the full mode of the Player.</span></span> <span data-ttu-id="e74b7-152">這是 Windows Media 中繼檔的 HTMLView 功能。</span><span class="sxs-lookup"><span data-stu-id="e74b7-152">This is the HTMLView feature of Windows Media metafiles.</span></span> <span data-ttu-id="e74b7-153">中繼檔可讓您充分掌控播放清單的內容，讓您能夠順暢地在剪輯之間轉換、插入廣告，以及在 Windows Media Player 中顯示靜止的影像。</span><span class="sxs-lookup"><span data-stu-id="e74b7-153">Metafiles give you great control over playlist content, allowing you to seamlessly transition between clips, insert advertisements, and display still images in Windows Media Player.</span></span> <span data-ttu-id="e74b7-154">若要在播放程式的完整模式中顯示網頁，您可以使用 PARAM 元素，將 URL 參考新增至播放清單專案或整個播放清單。</span><span class="sxs-lookup"><span data-stu-id="e74b7-154">To display webpages in the full mode of the Player, you use the PARAM element to add URL references to your playlist entries or to entire playlists.</span></span>

<span data-ttu-id="e74b7-155">如需有關在中繼檔中使用網頁的詳細資訊，請參閱 [在 Windows Media Player 中顯示網頁](displaying-web-pages-in-windows-media-player.md)。</span><span class="sxs-lookup"><span data-stu-id="e74b7-155">For more information about using webpages in metafiles, see [Displaying Web Pages in Windows Media Player](displaying-web-pages-in-windows-media-player.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e74b7-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="e74b7-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e74b7-157">**關於 Player 物件模型**</span><span class="sxs-lookup"><span data-stu-id="e74b7-157">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




