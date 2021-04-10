---
title: 網頁問題
description: 網頁問題
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Windows Media 中繼檔播放清單，網頁
- 播放清單、網頁
- 中繼檔播放清單，網頁
- Windows Media 中繼檔播放清單，自訂 HTMLView
- 播放清單，自訂 HTMLView
- 中繼檔播放清單，自訂 HTMLView
- Windows Media 中繼檔播放清單，HTMLView 自訂
- 播放清單，HTMLView 自訂
- 中繼檔播放清單，HTMLView 自訂
- 自訂 HTMLView
- Windows Media Player，網頁
- Windows Media Player，自訂 HTMLView
- Windows Media Player，HTMLView 自訂
- HTMLView，自訂
- HTMLView，網頁
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675135"
---
# <a name="web-page-issues"></a><span data-ttu-id="f888a-118">網頁問題</span><span class="sxs-lookup"><span data-stu-id="f888a-118">Web Page Issues</span></span>

<span data-ttu-id="f888a-119">當您建立要顯示在 Windows Media Player **Now 播放** 功能的網頁時，需要考慮一些事項。</span><span class="sxs-lookup"><span data-stu-id="f888a-119">There are some things to consider when you create a webpage to be displayed in the Windows Media Player **Now Playing** feature.</span></span> <span data-ttu-id="f888a-120">本節將討論一些您在建立 Web 內容時可能會遇到的問題。</span><span class="sxs-lookup"><span data-stu-id="f888a-120">This section discusses some of the issues you might encounter when creating your Web-based content.</span></span>

## <a name="customizing-htmlview"></a><span data-ttu-id="f888a-121">自訂 HTMLView</span><span class="sxs-lookup"><span data-stu-id="f888a-121">Customizing HTMLView</span></span>

<span data-ttu-id="f888a-122">您的 HTMLView 網頁可以像您的需要一樣簡單或複雜。</span><span class="sxs-lookup"><span data-stu-id="f888a-122">Your HTMLView webpage can be as simple or complex as you want.</span></span> <span data-ttu-id="f888a-123">您可以在 Web 內容中包含任何通常使用的元素。</span><span class="sxs-lookup"><span data-stu-id="f888a-123">You can include any of the elements you usually use in your Web-based content.</span></span> <span data-ttu-id="f888a-124">如果您內嵌 Windows Media Player 控制項，您可以顯示控制項所提供的其中一個使用者介面、使用 HTML 和腳本程式碼建立您自己的使用者介面，或在所有 (不提供任何 UI，這表示使用者可以使用全模式播放程式) 的傳輸控制。</span><span class="sxs-lookup"><span data-stu-id="f888a-124">If you embed the Windows Media Player control, you can display one of the user interfaces supplied by the control, create your own user interface using HTML and script code, or provide no UI at all (which means that the user can use the transport controls of the full-mode Player).</span></span>

<span data-ttu-id="f888a-125">使用 HTMLView 功能所顯示之網頁的建議大小為 575 x 345 圖元。</span><span class="sxs-lookup"><span data-stu-id="f888a-125">The recommended size for webpages displayed by using the HTMLView feature is 575 x 345 pixels.</span></span> <span data-ttu-id="f888a-126">但是，使用者可以調整 Windows Media Player 並選擇螢幕解析度。</span><span class="sxs-lookup"><span data-stu-id="f888a-126">The user, however, has the ability to resize Windows Media Player and choose the screen resolution.</span></span> <span data-ttu-id="f888a-127">如果 HTMLView 網頁大於「 **立即播放** 」功能所容納的大小，播放程式會顯示水準和垂直捲動條，讓使用者可以看到整個頁面。</span><span class="sxs-lookup"><span data-stu-id="f888a-127">If the HTMLView webpage is larger than the size accommodated by the **Now Playing** feature, the Player displays horizontal and vertical scroll bars that enable the user to see the entire page.</span></span> <span data-ttu-id="f888a-128">您應使用各種螢幕解析度和播放機大小來測試您的 HTMLView 內容，以判斷您的網頁的最佳大小。</span><span class="sxs-lookup"><span data-stu-id="f888a-128">You should test your HTMLView content using a variety of screen resolutions and Player sizes to determine the best size for your webpage.</span></span>

<span data-ttu-id="f888a-129">Windows Media Player 不提供可讓您指定完整模式播放程式大小的方法。</span><span class="sxs-lookup"><span data-stu-id="f888a-129">Windows Media Player does not provide a method that enables you to specify a size for the full-mode Player.</span></span>

## <a name="web-page-navigation"></a><span data-ttu-id="f888a-130">網頁流覽</span><span class="sxs-lookup"><span data-stu-id="f888a-130">Web page navigation</span></span>

<span data-ttu-id="f888a-131">Windows Media Player 不會提供 **立即播放** 功能中所顯示網頁的流覽工具列。</span><span class="sxs-lookup"><span data-stu-id="f888a-131">Windows Media Player does not provide a navigation toolbar for webpages displayed in the **Now Playing** feature.</span></span> <span data-ttu-id="f888a-132">這表示您可以完全掌控使用者是否可以離開 HTMLView 網頁。</span><span class="sxs-lookup"><span data-stu-id="f888a-132">This means that you have complete control over whether users can navigate away from your HTMLView webpage.</span></span> <span data-ttu-id="f888a-133">如果您想要讓使用者流覽至其他網頁，您必須在 HTML 程式碼中包含元素以提供該功能。</span><span class="sxs-lookup"><span data-stu-id="f888a-133">If you want to enable users to navigate to other webpages, you must include elements in your HTML code to provide that functionality.</span></span>

## <a name="retrieving-the-parent-window"></a><span data-ttu-id="f888a-134">正在抓取父視窗</span><span class="sxs-lookup"><span data-stu-id="f888a-134">Retrieving the parent window</span></span>

<span data-ttu-id="f888a-135">如果您現有的腳本使用 **window** 來取得父視窗物件，此程式碼將無法在您的 HTMLView 網頁中運作。</span><span class="sxs-lookup"><span data-stu-id="f888a-135">If your existing script code uses **window.parent** to retrieve the parent window object, this code will not work in your HTMLView webpage.</span></span> <span data-ttu-id="f888a-136">當您使用 HTMLView 時，不會有父視窗物件;因此，此腳本功能無法使用。</span><span class="sxs-lookup"><span data-stu-id="f888a-136">When you use HTMLView, there is no parent window object; therefore, this scripting feature is unavailable.</span></span>

## <a name="about-the-embedded-browser"></a><span data-ttu-id="f888a-137">關於內嵌瀏覽器</span><span class="sxs-lookup"><span data-stu-id="f888a-137">About the embedded browser</span></span>

<span data-ttu-id="f888a-138">由於 Windows Media Player 使用 Internet Explorer 的內嵌實例來顯示 HTMLView 內容，因此 Internet Explorer 的使用者設定和原則會套用至播放程式中顯示的任何網頁。</span><span class="sxs-lookup"><span data-stu-id="f888a-138">Because Windows Media Player uses an embedded instance of Internet Explorer to display HTMLView content, the user settings and policies for Internet Explorer apply to any webpages displayed in the Player.</span></span> <span data-ttu-id="f888a-139">例如，如果使用者已將 Internet Explorer 設定為防止網頁下載 cookie 至電腦，您的 HTMLView 網頁也會無法執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="f888a-139">For example, if the user has configured Internet Explorer to prevent webpages from downloading cookies to the computer, your HTMLView webpage is also prevented from doing this.</span></span>

<span data-ttu-id="f888a-140">使用 HTMLView 功能開啟的網頁一律會在 Internet Explorer 的 **網際網路** 安全性區域中執行。</span><span class="sxs-lookup"><span data-stu-id="f888a-140">Web pages opened by using the HTMLView feature always run in the Internet Explorer **Internet** security zone.</span></span>

<span data-ttu-id="f888a-141">內嵌的網頁瀏覽器控制項使用相同的規則，將網頁快取為 Internet Explorer 的獨立版本。</span><span class="sxs-lookup"><span data-stu-id="f888a-141">The embedded Web browser control uses the same rules to cache webpages as the stand-alone version of Internet Explorer.</span></span> <span data-ttu-id="f888a-142">在建立內容時使用 Active Server Pages (ASP) ，以確保每次 Windows Media Player 存取 HTMLView 網頁時，都會從 web 伺服器提供內容。</span><span class="sxs-lookup"><span data-stu-id="f888a-142">It's a good idea to use Active Server Pages (ASP) when creating your content to ensure that the content is delivered from your web server each time Windows Media Player accesses the HTMLView webpage.</span></span> <span data-ttu-id="f888a-143">使用 ASP 頁面可以像將網頁重新命名為使用 .asp 副檔名一樣簡單。</span><span class="sxs-lookup"><span data-stu-id="f888a-143">Using ASP pages can be as simple as renaming your webpage to use an .asp file name extension.</span></span>

## <a name="about-local-web-content"></a><span data-ttu-id="f888a-144">關於本機 Web 內容</span><span class="sxs-lookup"><span data-stu-id="f888a-144">About local Web content</span></span>

<span data-ttu-id="f888a-145">HTMLView 功能不允許您開啟儲存在使用者電腦上的網頁。</span><span class="sxs-lookup"><span data-stu-id="f888a-145">The HTMLView feature does not allow you to open webpages that are stored on the user's computer.</span></span>

## <a name="prompting-the-user"></a><span data-ttu-id="f888a-146">提示使用者</span><span class="sxs-lookup"><span data-stu-id="f888a-146">Prompting the user</span></span>

<span data-ttu-id="f888a-147">您可以使用 [ **視窗]** 提示使用者輸入資訊。</span><span class="sxs-lookup"><span data-stu-id="f888a-147">You can use **window.prompt** to prompt the user for information.</span></span> <span data-ttu-id="f888a-148">但是，當使用 HTMLView 時，無法使用 [**確認** **]** 。</span><span class="sxs-lookup"><span data-stu-id="f888a-148">However, **window.alert** and **window.confirm** are not available when using HTMLView.</span></span>

## <a name="timing-issues"></a><span data-ttu-id="f888a-149">計時問題</span><span class="sxs-lookup"><span data-stu-id="f888a-149">Timing issues</span></span>

<span data-ttu-id="f888a-150">在 HTMLView 網頁中使用內嵌的 Windows Media Player 控制項時，您可能會遇到計時問題。</span><span class="sxs-lookup"><span data-stu-id="f888a-150">You may encounter timing issues when using an embedded Windows Media Player control in your HTMLView webpage.</span></span> <span data-ttu-id="f888a-151">在 HTMLView 中，內嵌的播放機控制項會與獨立 Windows Media Player 共用其播放引擎。</span><span class="sxs-lookup"><span data-stu-id="f888a-151">In HTMLView, an embedded Player control shares its playback engine with the stand-alone Windows Media Player.</span></span> <span data-ttu-id="f888a-152">獨立播放程式可能會在網頁 (之前開啟並開始播放第一個播放清單專案，因此，Player 控制項) 完成載入。</span><span class="sxs-lookup"><span data-stu-id="f888a-152">It is possible that the stand-alone Player may open and begin playing the first playlist entry before the webpage (and, therefore, the Player control) finishes loading.</span></span> <span data-ttu-id="f888a-153">這表示，如果您處理 **OpenStateChange** 或 **PlayStateChange** 事件，腳本將不會收到這些事件的事件通知，除非已載入 Player 控制項和其相關聯的物件。</span><span class="sxs-lookup"><span data-stu-id="f888a-153">This means that if you handle the **OpenStateChange** or **PlayStateChange** events, the script code will not receive event notifications for these events until the Player control and its associated objects are loaded.</span></span>

<span data-ttu-id="f888a-154">您可以在程式碼中採取步驟來延遲播放，直到 Windows Media Player 控制項具現化為止。</span><span class="sxs-lookup"><span data-stu-id="f888a-154">You can take steps in your code to delay playback until the Windows Media Player control is instantiated.</span></span> <span data-ttu-id="f888a-155">執行這項作業的其中一種方式是讓中繼檔播放清單中的第一個專案指向影像檔案，並將檔案的持續時間設定為允許播放程式控制項載入的時間長度。</span><span class="sxs-lookup"><span data-stu-id="f888a-155">One way to do this is to make the first entry in your metafile playlist point to an image file and set the duration of the file to a length of time that allows the Player control to load.</span></span> <span data-ttu-id="f888a-156">下列範例程式碼示範這個選項：</span><span class="sxs-lookup"><span data-stu-id="f888a-156">The following example code demonstrates this option:</span></span>


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="f888a-157">當上述播放清單開啟時，Windows Media Player 等候播放清單中的第一個專案在播放程式載入 HTMLView 網頁時最多一分鐘。</span><span class="sxs-lookup"><span data-stu-id="f888a-157">When the preceding playlist opens, Windows Media Player waits at the first entry in the playlist for up to one minute while the Player loads the HTMLView webpage.</span></span>

<span data-ttu-id="f888a-158">接下來，在您的 HTMLView 網頁中撰寫腳本程式碼，以處理本文 **專案的** **onload** 事件。</span><span class="sxs-lookup"><span data-stu-id="f888a-158">Next, in your HTMLView webpage, write script code to handle the **onload** event for the **BODY** element.</span></span> <span data-ttu-id="f888a-159">在事件處理常式函式中，呼叫 Player **Controls. Next** 方法以開始播放播放清單中的第二個專案。</span><span class="sxs-lookup"><span data-stu-id="f888a-159">In the event handler function, call the Player **Controls.Next** method to begin playback of the second entry in the playlist.</span></span>


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="f888a-160">當上述範例中的網頁完成載入時，Windows Media Player 立即前進到播放清單中的第二個專案。</span><span class="sxs-lookup"><span data-stu-id="f888a-160">When the webpage in the preceding example finishes loading, Windows Media Player immediately advances to the second entry in the playlist.</span></span> <span data-ttu-id="f888a-161">這會覆寫播放清單中第一個元素所指定的持續時間，這表示使用者不需要等待一分鐘，就能看到所需的內容。他或她只需要等待網頁載入完成。</span><span class="sxs-lookup"><span data-stu-id="f888a-161">This overrides the duration specified for the first element in the playlist, meaning that the user doesn't have to wait the full one minute before seeing the desired content; he or she only has to wait for the webpage to finish loading.</span></span> <span data-ttu-id="f888a-162">由於 Player 控制項現在會完全具現化，因此 **OpenStateChange** 和 **PlayStateChange** 事件可以用平常的方式處理。</span><span class="sxs-lookup"><span data-stu-id="f888a-162">Because the Player control is completely instantiated at this point, the **OpenStateChange** and **PlayStateChange** events can be handled in the usual manner.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f888a-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="f888a-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f888a-164">**顯示 Windows Media Player 中的網頁**</span><span class="sxs-lookup"><span data-stu-id="f888a-164">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="f888a-165">**PlayStateChange 事件**</span><span class="sxs-lookup"><span data-stu-id="f888a-165">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="f888a-166">**OpenStateChange 事件**</span><span class="sxs-lookup"><span data-stu-id="f888a-166">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 




