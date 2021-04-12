---
title: 加入內嵌 Windows Media Player 控制項
description: 加入內嵌 Windows Media Player 控制項
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Windows Media 中繼檔播放清單，新增內嵌的 Windows Media Player 控制項
- 播放清單，加入內嵌的 Windows Media Player 控制項
- 中繼檔播放清單，新增內嵌的 Windows Media Player 控制項
- Windows Media 中繼檔播放清單，embedded Windows Media Player 控制項
- 播放清單、內嵌 Windows Media Player 控制項
- 中繼檔播放清單、內嵌 Windows Media Player 控制項
- 新增內嵌的 Windows Media Player 控制項
- 內嵌的 Windows Media Player 控制項
- Windows Media Player，加入內嵌的控制項
- Windows Media Player、內嵌控制項
- HTMLView，加入內嵌 Windows Media Player 控制項
- HTMLView、embedded Windows Media Player 控制項
- HTMLView，Windows Media Player 物件模型
- HTMLView，Player 物件模型
- Windows Media Player 物件模型，關於
- 物件模型，關於
- Player 物件
- Windows Media、Player 物件模型
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372392"
---
# <a name="adding-an-embedded-windows-media-player-control"></a><span data-ttu-id="9fcff-121">加入內嵌 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="9fcff-121">Adding an Embedded Windows Media Player Control</span></span>

<span data-ttu-id="9fcff-122">有兩個原因，您可能會考慮將 Windows Media Player 的內嵌實例新增至 HTMLView 簡報。</span><span class="sxs-lookup"><span data-stu-id="9fcff-122">There are two reasons you might consider adding an embedded instance of Windows Media Player to your HTMLView presentation.</span></span> <span data-ttu-id="9fcff-123">首先，如果您想要顯示影片內容，您需要使用 Windows Media Player ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="9fcff-123">First, if you want to display video content, you need to use the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="9fcff-124">其次，如果您想要從 HTMLView 網頁內利用 Windows Media Player 物件模型的功能，您必須使用 Player 控制項的實例來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="9fcff-124">Second, if you want to take advantage of features of the Windows Media Player object model from within your HTMLView webpage, you must use an instance the Player control to do so.</span></span>

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a><span data-ttu-id="9fcff-125">使用 Player 控制項在 HTMLView 內容中顯示影片</span><span class="sxs-lookup"><span data-stu-id="9fcff-125">Using the Player control to display video in HTMLView content</span></span>

<span data-ttu-id="9fcff-126">通常，Windows Media Player 會使用 **目前播放** 功能的 [影片和視覺效果] 窗格來顯示影片。</span><span class="sxs-lookup"><span data-stu-id="9fcff-126">Usually, Windows Media Player displays video using the Video and Visualization pane of the **Now Playing** feature.</span></span> <span data-ttu-id="9fcff-127">由於 HTMLView 會使用此區域來顯示您的網頁，因此如果您希望播放程式播放影片，則必須提供額外的影片顯示區域。</span><span class="sxs-lookup"><span data-stu-id="9fcff-127">Since HTMLView uses this area to display your webpage, you must supply an additional video display area if you want the Player to play video.</span></span> <span data-ttu-id="9fcff-128">您可以使用 Windows Media Player ActiveX 控制項來輕鬆完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="9fcff-128">This is easy to do by using the Windows Media Player ActiveX control.</span></span>

<span data-ttu-id="9fcff-129">若要使用 Player 控制項來顯示影片，請使用 **物件** 標記將控制項內嵌在您的 HTMLView 網頁中。</span><span class="sxs-lookup"><span data-stu-id="9fcff-129">To use the Player control to display video, embed the control in your HTMLView webpage by using the **OBJECT** tag.</span></span> <span data-ttu-id="9fcff-130">這是您用來將播放機控制項內嵌到您想要顯示影片之任何網頁的相同技術。</span><span class="sxs-lookup"><span data-stu-id="9fcff-130">This is the same technique you use to embed the Player control into any webpage in which you want to display video.</span></span> <span data-ttu-id="9fcff-131">下列範例程式碼顯示在 Internet Explorer 中內嵌 Player 控制項的基本語法：</span><span class="sxs-lookup"><span data-stu-id="9fcff-131">The following example code shows the basic syntax for embedding the Player control in Internet Explorer:</span></span>


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



<span data-ttu-id="9fcff-132">*AutoStart* 參數可確保每當指定新的 URL 時，內容就會自動播放。</span><span class="sxs-lookup"><span data-stu-id="9fcff-132">The *autoStart* parameter ensures that content plays automatically whenever a new URL is specified.</span></span> <span data-ttu-id="9fcff-133">您為 *uiMode* 指定的值是由您所指定，但是在建立 HTMLView 簡報的內容時，通常會想要指定「無」。</span><span class="sxs-lookup"><span data-stu-id="9fcff-133">The value you specify for *uiMode* is up to you, but you will usually want to specify "none" when creating content for HTMLView presentations.</span></span> <span data-ttu-id="9fcff-134">當您以這種方式內嵌 Windows Media Player 控制項來顯示影片時，使用者可以使用全模式播放程式的控制項來控制播放，所以不需要在網頁中提供其他傳輸控制項。</span><span class="sxs-lookup"><span data-stu-id="9fcff-134">When you embed the Windows Media Player control to display video in this manner, the user can control playback using the controls of the full-mode Player, so there's no need to provide additional transport controls in the webpage.</span></span> <span data-ttu-id="9fcff-135">您可以使用通常配置給傳輸控制項的空間，以顯示更多文字、圖形或其他內容的連結。</span><span class="sxs-lookup"><span data-stu-id="9fcff-135">You can use the space you would usually allocate for transport controls to display more text, graphics, or links to other content.</span></span>

<span data-ttu-id="9fcff-136">在設計要顯示于 HTMLView 簡報中的網頁上內嵌 Windows Media Player 控制項時，請勿指定 *URL* 參數。</span><span class="sxs-lookup"><span data-stu-id="9fcff-136">Do not specify a *URL* parameter when embedding the Windows Media Player control in a webpage designed to display in an HTMLView presentation.</span></span> <span data-ttu-id="9fcff-137">相反地，請在用來開啟內容的 .asx 檔案中指定數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="9fcff-137">Instead, specify the digital media files in the .asx file that opens the content.</span></span>

<span data-ttu-id="9fcff-138">由於您在 HTMLView 網頁中提供影片顯示區域，因此您可以決定影片的放置位置，以及您想要的顯示區域大小。</span><span class="sxs-lookup"><span data-stu-id="9fcff-138">Because you provide the video display region in your HTMLView webpage, you can decide where to position the video and how large you want the display region to be.</span></span> <span data-ttu-id="9fcff-139">例如，您可以在 HTML **DIV** 專案內包含 **Player** 物件，然後指定 **DIV** 的位置，讓影片顯示在網頁上。</span><span class="sxs-lookup"><span data-stu-id="9fcff-139">For example, you can contain the **Player** object within an HTML **DIV** element and then specify the position for the **DIV** to situate the video display on the webpage.</span></span> <span data-ttu-id="9fcff-140">您可以藉由指定 **物件** 專案的 [高度] 和 [寬度] 屬性值，來變更影片顯示的尺寸。</span><span class="sxs-lookup"><span data-stu-id="9fcff-140">You can change the dimensions of the video display by specifying values for the height and width attributes of the **OBJECT** element.</span></span> <span data-ttu-id="9fcff-141">您也可以使用腳本來指定這些值。</span><span class="sxs-lookup"><span data-stu-id="9fcff-141">You can also specify these values using script code.</span></span>

## <a name="using-the-player-object-model"></a><span data-ttu-id="9fcff-142">使用 Player 物件模型</span><span class="sxs-lookup"><span data-stu-id="9fcff-142">Using the Player object model</span></span>

<span data-ttu-id="9fcff-143">Windows Media Player 物件模型會公開您可以在 HTMLView 網頁中使用的屬性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="9fcff-143">The Windows Media Player object model exposes properties, methods, and events that you can use in your HTMLView webpages.</span></span> <span data-ttu-id="9fcff-144">當您在 HTMLView 網頁中內嵌 Windows Media Player ActiveX 控制項時，您會自動擁有 Player 物件模型的存取權。</span><span class="sxs-lookup"><span data-stu-id="9fcff-144">When you embed the Windows Media Player ActiveX control in your HTMLView webpage, you automatically have access to the Player object model.</span></span>

<span data-ttu-id="9fcff-145">如果您在 HTMLView 網頁中內嵌 Windows Media Player 控制項，請勿使用 Player 物件模型來指定要播放的數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="9fcff-145">If you embed the Windows Media Player control in your HTMLView webpage, do not use the Player object model to specify the digital media file to be played.</span></span> <span data-ttu-id="9fcff-146">例如，如果您使用腳本來指定內嵌控制項的 **URL** 屬性值，當數位媒體檔案播放時，您的 HTMLView 網頁將會從「 **立即播放** 」功能中卸載。</span><span class="sxs-lookup"><span data-stu-id="9fcff-146">For example, if you use script code to specify a value for the **URL** property of the embedded control, your HTMLView webpage will be unloaded from the **Now Playing** feature when the digital media file plays.</span></span> <span data-ttu-id="9fcff-147">若要避免發生這種情況，當您需要使用腳本從 HTMLView 網頁開啟數位媒體內容時，請一律開啟包含 HTMLView 參數的 .asx 檔。</span><span class="sxs-lookup"><span data-stu-id="9fcff-147">To prevent this from happening, always open .asx files that include HTMLView parameters when you need to use script to open digital media content from your HTMLView webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fcff-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fcff-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fcff-149">**顯示 Windows Media Player 中的網頁**</span><span class="sxs-lookup"><span data-stu-id="9fcff-149">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="9fcff-150">**UiMode**</span><span class="sxs-lookup"><span data-stu-id="9fcff-150">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="9fcff-151">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="9fcff-151">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="9fcff-152">**設定。 autoStart**</span><span class="sxs-lookup"><span data-stu-id="9fcff-152">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 




