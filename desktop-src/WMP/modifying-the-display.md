---
title: 修改顯示
description: 修改顯示
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Windows Media 中繼檔播放清單，修改顯示
- 播放清單，修改顯示
- 中繼檔播放清單，修改顯示
- Windows Media 中繼檔播放清單，顯示修改
- 播放清單，顯示修改
- 中繼檔播放清單，顯示修改
- Windows Media Player，顯示修改
- Windows Media Player，修改顯示
- Windows Media Player，文字屬性
- Windows Media Player，影像屬性
- Windows Media Player，MOREINFO 屬性
- Windows Media Player，摘要文字
- MOREINFO 屬性
- 摘要文字
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5c36c55b455b797446cde627449ea705b3bd2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021234"
---
# <a name="modifying-the-display"></a><span data-ttu-id="96d10-117">修改顯示</span><span class="sxs-lookup"><span data-stu-id="96d10-117">Modifying the Display</span></span>

<span data-ttu-id="96d10-118">播放清單可以四種主要方式改變 Windows Media Player 使用者介面：</span><span class="sxs-lookup"><span data-stu-id="96d10-118">Playlists can alter the Windows Media Player user interface in four main ways:</span></span>

-   <span data-ttu-id="96d10-119">Text 屬性</span><span class="sxs-lookup"><span data-stu-id="96d10-119">Text properties</span></span>
-   <span data-ttu-id="96d10-120">映像屬性</span><span class="sxs-lookup"><span data-stu-id="96d10-120">Image properties</span></span>
-   <span data-ttu-id="96d10-121">MOREINFO 屬性</span><span class="sxs-lookup"><span data-stu-id="96d10-121">MOREINFO properties</span></span>
-   <span data-ttu-id="96d10-122">摘要文字</span><span class="sxs-lookup"><span data-stu-id="96d10-122">ABSTRACT text</span></span>

## <a name="text-properties"></a><span data-ttu-id="96d10-123">Text 屬性</span><span class="sxs-lookup"><span data-stu-id="96d10-123">Text properties</span></span>

<span data-ttu-id="96d10-124">Windows Media Player 啟用標題、作者、著作權和描述中繼資料文字的顯示。</span><span class="sxs-lookup"><span data-stu-id="96d10-124">Windows Media Player enables the display of Title, Author, Copyright, and Description metadata text.</span></span> <span data-ttu-id="96d10-125">剪輯中繼資料可以來自資料流程或媒體檔案，也可以來自播放清單。</span><span class="sxs-lookup"><span data-stu-id="96d10-125">Clip metadata can come from the stream or media file, or it can come from a playlist.</span></span> <span data-ttu-id="96d10-126">顯示中繼資料來自播放清單。</span><span class="sxs-lookup"><span data-stu-id="96d10-126">Show metadata comes from the playlist.</span></span> <span data-ttu-id="96d10-127">一般情況下，播放清單是將文字屬性傳遞至 Windows Media Player 的較佳方法，尤其是可能變更文字元素時。</span><span class="sxs-lookup"><span data-stu-id="96d10-127">In general, playlists are a better method of passing text properties to Windows Media Player, especially if text elements are likely to change.</span></span> <span data-ttu-id="96d10-128">編輯播放清單中的文字比重新撰寫媒體檔案更容易。</span><span class="sxs-lookup"><span data-stu-id="96d10-128">It is easier to edit text in a playlist than to re-author a media file.</span></span> <span data-ttu-id="96d10-129">而且因為從播放清單中讀取的屬性會覆寫媒體檔案中包含的屬性，所以您可以將新文字加入播放清單中的對應屬性，輕鬆地更新顯示文字。</span><span class="sxs-lookup"><span data-stu-id="96d10-129">And because properties read from a playlist override those contained in the media file, you can easily update display text by adding the new text to the corresponding property in a playlist.</span></span> <span data-ttu-id="96d10-130">在下列範例中，播放清單中標題和作者中繼資料的文字會覆寫媒體檔案中所含的標題和作者文字（例如 .wma）。</span><span class="sxs-lookup"><span data-stu-id="96d10-130">In the following example, the text of the Title and Author metadata in the playlist overrides the Title and Author text contained in the media file, sample.wma.</span></span>

<span data-ttu-id="96d10-131">除非中繼檔播放清單中有一個 **抽象** 元素，否則會從 **專案專案** 中參考的 Windows Media 檔案取出 **描述** 文字。</span><span class="sxs-lookup"><span data-stu-id="96d10-131">**DESCRIPTION** text is retrieved from a Windows Media file referenced in an **ENTRY** element unless there is an **ABSTRACT** element in a metafile playlist.</span></span> <span data-ttu-id="96d10-132">如果有 **摘要** 文字，則會顯示並覆寫 **描述** 文字。</span><span class="sxs-lookup"><span data-stu-id="96d10-132">If there is **ABSTRACT** text, it will be displayed, overriding the **DESCRIPTION** text.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a><span data-ttu-id="96d10-133">映像屬性</span><span class="sxs-lookup"><span data-stu-id="96d10-133">Image properties</span></span>

<span data-ttu-id="96d10-134">橫幅影像可以新增至 Windows Media Player 的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="96d10-134">Banner images can be added to the user interface of Windows Media Player.</span></span> <span data-ttu-id="96d10-135">此圖形可用於廣告、提供資訊，以及提供網站的存取權，以提供一些可能的名稱。</span><span class="sxs-lookup"><span data-stu-id="96d10-135">The graphic can be used for advertising, providing information, and providing access to websites, to name a few possibilities.</span></span>

<span data-ttu-id="96d10-136">使用 **橫幅** 元素可指定 Windows Media Player 顯示的圖形影像， (32 圖元高、194圖元寬) 。</span><span class="sxs-lookup"><span data-stu-id="96d10-136">Use the **BANNER** element to specify a graphic image (32 pixels high by 194 pixels wide) for display by Windows Media Player.</span></span> <span data-ttu-id="96d10-137">圖形會顯示在任何影片內容下方。</span><span class="sxs-lookup"><span data-stu-id="96d10-137">The graphic is displayed below any video content.</span></span> <span data-ttu-id="96d10-138">您可以使用 **MOREINFO** 子項目，將超連結新增至橫幅。</span><span class="sxs-lookup"><span data-stu-id="96d10-138">A hyperlink can be added to the banner using the **MOREINFO** child element.</span></span>

<span data-ttu-id="96d10-139">工具提示可以由 **橫幅** 元素範圍內的 **抽象** 元素定義。</span><span class="sxs-lookup"><span data-stu-id="96d10-139">A ToolTip can be defined by an **ABSTRACT** element within the scope of the **BANNER** element.</span></span> <span data-ttu-id="96d10-140">您可以藉由將滑鼠指標暫停在橫幅圖形上方，來顯示任何定義的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="96d10-140">Any defined ToolTip text can be displayed by pausing the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="96d10-141">選取具有滑鼠指標的橫幅圖形將會啟動任何以 **MOREINFO** 元素定義的超連結。</span><span class="sxs-lookup"><span data-stu-id="96d10-141">Selecting the banner graphic with the mouse pointer will activate any hyperlink defined with the **MOREINFO** element.</span></span>

<span data-ttu-id="96d10-142">慣用的 **橫幅** 圖形格式為 GIF 格式。</span><span class="sxs-lookup"><span data-stu-id="96d10-142">The preferred **BANNER** graphics format is the GIF format.</span></span> <span data-ttu-id="96d10-143">如果圖形的大小正確，則可以使用 JPG 格式。</span><span class="sxs-lookup"><span data-stu-id="96d10-143">The JPG format can be used if the graphic is properly sized.</span></span>

<span data-ttu-id="96d10-144">上述範例說明如何使用 **橫幅** 元素。</span><span class="sxs-lookup"><span data-stu-id="96d10-144">The previous example illustrates use of the **BANNER** element.</span></span>

> [!Note]  
> <span data-ttu-id="96d10-145">使用 DRM 檔案時，或在網頁中內嵌 Windows Media Player 時，不支援 **橫幅** 影像。</span><span class="sxs-lookup"><span data-stu-id="96d10-145">**BANNER** images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

 

<span data-ttu-id="96d10-146">如需橫幅的詳細資訊，請參閱 [Windows Media Player 中的自訂圖形](custom-graphics-in-windows-media-player.md)。</span><span class="sxs-lookup"><span data-stu-id="96d10-146">For more information about banners, see [Custom Graphics in Windows Media Player](custom-graphics-in-windows-media-player.md).</span></span>

## <a name="moreinfo-properties"></a><span data-ttu-id="96d10-147">MOREINFO 屬性</span><span class="sxs-lookup"><span data-stu-id="96d10-147">MOREINFO properties</span></span>

<span data-ttu-id="96d10-148">使用者介面的文字和影像區域可以與 Url 相關聯。</span><span class="sxs-lookup"><span data-stu-id="96d10-148">Text and image areas of the user interface can be associated with URLs.</span></span> <span data-ttu-id="96d10-149">在播放期間，使用者可以選取其中一個區段，以連接到其網頁瀏覽器中與其相關聯的 URL。</span><span class="sxs-lookup"><span data-stu-id="96d10-149">During playback, users can select one of these sections to connect to the URL associated with it in their Web browser.</span></span> <span data-ttu-id="96d10-150">例如，您可以將廣告網站的網站與廣告橫幅影像產生關聯，如下列程式碼片段所示。</span><span class="sxs-lookup"><span data-stu-id="96d10-150">For example, you can associate an advertiser's website with an ad banner image as shown in the following code snippet.</span></span>


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a><span data-ttu-id="96d10-151">摘要文字</span><span class="sxs-lookup"><span data-stu-id="96d10-151">ABSTRACT text</span></span>

<span data-ttu-id="96d10-152">**ABSTRACT** text 可用來顯示與所關聯之使用者介面的文字或影像區域的簡短快顯描述。</span><span class="sxs-lookup"><span data-stu-id="96d10-152">**ABSTRACT** text is used to display a short pop-up description of the text or image areas of the user interface it is associated with.</span></span> <span data-ttu-id="96d10-153">在播放期間，如果滑鼠指標停留在這些區域的其中一個，則滑鼠指標旁邊會出現工具提示，顯示與區域相關聯的 **摘要** 文字。</span><span class="sxs-lookup"><span data-stu-id="96d10-153">During playback, if the mouse pointer hovers over one of these areas, a ToolTip appears beside the mouse pointer displaying the **ABSTRACT** text associated with the area.</span></span> <span data-ttu-id="96d10-154">**抽象** 文字是從中繼檔抓取，並以 **抽象** 元素定義。</span><span class="sxs-lookup"><span data-stu-id="96d10-154">**ABSTRACT** text is retrieved from a metafile and is defined with the **ABSTRACT** element.</span></span> <span data-ttu-id="96d10-155">**ABSTRACT** 元素可以是專案或 **橫幅\*\*\*\*專案** 的子項目。</span><span class="sxs-lookup"><span data-stu-id="96d10-155">The **ABSTRACT** element can be a child element of either an **ENTRY** or a **BANNER** element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96d10-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="96d10-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96d10-157">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="96d10-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="96d10-158">**使用中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="96d10-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="96d10-159">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="96d10-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="96d10-160">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="96d10-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




