---
title: 存取媒體
description: 存取媒體
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Windows Media 中繼檔播放清單，存取媒體
- 播放清單，存取媒體
- 中繼檔播放清單，存取媒體
- Windows Media 中繼檔播放清單，媒體存取
- 播放清單，媒體存取
- 中繼檔播放清單，媒體存取
- Windows Media 中繼檔播放清單，控制播放
- 播放清單，控制播放
- 中繼檔播放清單，控制播放
- Windows Media 中繼檔播放清單，設定持續時間
- 播放清單，設定持續時間
- 中繼檔播放清單，設定持續時間
- Windows Media Player，存取媒體
- Windows Media Player，媒體存取
- Windows Media Player，控制播放
- Windows Media Player，設定持續時間
- 存取媒體
- 媒體存取
- 控制播放
- 設定持續時間
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5a995a6816e3c46a002bd1ea924c9ea9a207000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966405"
---
# <a name="accessing-media"></a><span data-ttu-id="a50a3-123">存取媒體</span><span class="sxs-lookup"><span data-stu-id="a50a3-123">Accessing Media</span></span>

<span data-ttu-id="a50a3-124">使用播放清單來指定及控制 Windows Media Player 播放的串流媒體或媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="a50a3-124">Use playlists to specify and to control the streaming media or media files that Windows Media Player plays.</span></span>

<span data-ttu-id="a50a3-125">您可以使用 **ENTRY 專案** 來指定單一媒體元件 (媒體檔案或即時資料流) 和任何子項目 (例如影像、 **MOREINFO** 連結和 **抽象** 文字) 。</span><span class="sxs-lookup"><span data-stu-id="a50a3-125">Use the **ENTRY** element to specify a single media element (a media file or a live stream) and any child elements (such as images, **MOREINFO** links, and **ABSTRACT** text).</span></span> <span data-ttu-id="a50a3-126">使用 **ENTRYREF** 元素來指定播放清單。</span><span class="sxs-lookup"><span data-stu-id="a50a3-126">Use an **ENTRYREF** element to specify a playlist.</span></span> <span data-ttu-id="a50a3-127">播放清單可包含一或多個 **專案** 或 **ENTRYREF** 元素。</span><span class="sxs-lookup"><span data-stu-id="a50a3-127">A playlist can contain one or more **ENTRY** or **ENTRYREF** elements.</span></span> <span data-ttu-id="a50a3-128">Windows Media Player 會從第一個專案開始，然後依序播放每個專案，直到清單完成為止，以執行播放清單。</span><span class="sxs-lookup"><span data-stu-id="a50a3-128">Windows Media Player executes a playlist by starting with the first entry and then playing each entry in turn until the list is finished.</span></span>

<span data-ttu-id="a50a3-129">**專案專案** 可以指向任何 Windows Media Player 可以播放的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a50a3-129">An **ENTRY** element can point to any type of media that Windows Media Player can play.</span></span> <span data-ttu-id="a50a3-130">這不僅包括 .wma、.wmv、.asf 和 .avi 檔案，也可以命名一些但即時資料流。</span><span class="sxs-lookup"><span data-stu-id="a50a3-130">This includes not only .wma, .wmv, .asf, and .avi files, to name a few, but live streams as well.</span></span> <span data-ttu-id="a50a3-131">藉由使用一系列的專案或 **ENTRYREF** **專案** 來參考媒體內容，您可以使用播放清單來傳送由多個來源組成的單一資料流程。</span><span class="sxs-lookup"><span data-stu-id="a50a3-131">By using a series of **ENTRY** or **ENTRYREF** elements to reference media content, you can use a playlist to send a single stream that consists of multiple sources.</span></span> <span data-ttu-id="a50a3-132">參考的資料流程會依序播放，並由檢視器視為一個連續串流。</span><span class="sxs-lookup"><span data-stu-id="a50a3-132">The referenced streams will play sequentially and be seen as one continuous stream by the viewer.</span></span> <span data-ttu-id="a50a3-133">例如，播放清單可以包含兩個 **ENTRY** 元素：標準的簡介： Windows Media 檔案副檔名為 .wma，以及即時 Windows media 資料流程。</span><span class="sxs-lookup"><span data-stu-id="a50a3-133">For example, the playlist can contain two **ENTRY** elements: a standard introduction from a Windows Media file with a .wma extension, and a live Windows Media stream.</span></span>

> [!Note]  
> <span data-ttu-id="a50a3-134">播放清單不能包含媒體檔案的連結，這些媒體檔案的內容是使用不同版本的數位 Rights Management (DRM) 所建立。</span><span class="sxs-lookup"><span data-stu-id="a50a3-134">A playlist must not contain links to media files that have content created with different versions of Digital Rights Management (DRM).</span></span> <span data-ttu-id="a50a3-135">在中繼檔播放清單中，如果有包含 DRM 第1版內容的媒體檔案連結，以及以較新 DRM 版本建立的媒體檔案的連結，Windows Media Player 只會播放 DRM 第1版的內容。</span><span class="sxs-lookup"><span data-stu-id="a50a3-135">In a metafile playlist, if there are links for media files with DRM version 1 content and for media files created with later DRM versions, Windows Media Player will only play the DRM version 1 content.</span></span>

 

## <a name="controlling-playback"></a><span data-ttu-id="a50a3-136">控制播放</span><span class="sxs-lookup"><span data-stu-id="a50a3-136">Controlling Playback</span></span>

<span data-ttu-id="a50a3-137">使用播放清單來控制是否只播放播放的媒體剪輯，以及播放剪輯的哪些部分和操作方式。</span><span class="sxs-lookup"><span data-stu-id="a50a3-137">Use playlists to control not only which media clip is played, but also which portions of the clip are played and how.</span></span> <span data-ttu-id="a50a3-138">您可以使用播放清單來定義要進行迴圈或重複的一組剪輯、設定播放的持續時間，以及指派開始時間和每個專案的開始和結束標記。</span><span class="sxs-lookup"><span data-stu-id="a50a3-138">You can use playlists to define a set of clips to be looped or repeated, to set the duration of play, and to assign start times, and start and end markers for each entry.</span></span> <span data-ttu-id="a50a3-139">**STARTTIME**、 **STARTMARKER** 和 **ENDMARKER** 元素會與媒體檔案中的標記一起使用。</span><span class="sxs-lookup"><span data-stu-id="a50a3-139">The **STARTTIME**, **STARTMARKER**, and **ENDMARKER** elements work in conjunction with markers in the media file.</span></span>

<span data-ttu-id="a50a3-140">例如，下列播放清單會在一個 **專案** 中使用廣告橫幅和相關聯的 **MOREINFO** 連結，並參考 **STARTMARKER** 和 **ENDMARKER**。</span><span class="sxs-lookup"><span data-stu-id="a50a3-140">For example, the following playlist uses an ad banner and the associated **MOREINFO** link in one **ENTRY**, and references a **STARTMARKER** and **ENDMARKER**.</span></span>


```XML
<ASX version ="3.0">
<Title>Windows Media Example</Title>
<Abstract>Windows Media Technologies</Abstract>
<MoreInfo href = "https://www.proseware.com"/>
    <!--This is the first Entry -->
    <Entry>
        <Title>This is the ad</Title>
        <Author>Ad Department</Author>
        <Copyright>2000</Copyright>
        <Abstract>This is a description of the ad.</Abstract>
        <MoreInfo href = "https://www.proseware.com/"/>
        <Ref href="ad.wma"/>
        <Banner href ="purchase.gif">
           <Abstract>Click here to go to our website.</Abstract>
           <MoreInfo href = "https://www.litwareinc.com/" />
        </Banner>
     </Entry>        
    <!-- This is the second Entry -->
    <!-- The Windows Media file plays from Segment2 to Segment3 -->
    <Entry>
        <Title>Playlist Clip Number Two</Title>
        <Author>Windows Media</Author>
        <Copyright>2000</Copyright>
        <Ref href="show.wma"/>
        <StartMarker Name = "Segment2" />
        <EndMarker Name = "Segment3" />
    </Entry>
</ASX>

```



## <a name="setting-duration"></a><span data-ttu-id="a50a3-141">設定持續時間</span><span class="sxs-lookup"><span data-stu-id="a50a3-141">Setting Duration</span></span>

<span data-ttu-id="a50a3-142">您可以使用 **DURATION** 元素來指定播放剪輯或一組剪輯的時間長度。</span><span class="sxs-lookup"><span data-stu-id="a50a3-142">Use the **DURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="a50a3-143">您也可以搭配 **PREVIEWDURATION** 元素使用 **ASX** 元素的 **PREVIEWMODE** 屬性，以指定播放剪輯或一組剪輯的時間長度。</span><span class="sxs-lookup"><span data-stu-id="a50a3-143">You can also use the **PREVIEWMODE** attribute of the **ASX** element in conjunction with the **PREVIEWDURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="a50a3-144">將 **PREVIEWMODE** 屬性設定為 [是]，即可使用 **PREVIEWDURATION** 元素指定播放相關剪輯的時間長度。</span><span class="sxs-lookup"><span data-stu-id="a50a3-144">Set the **PREVIEWMODE** attribute to YES to use the **PREVIEWDURATION** element to specify how long to play the associated clip.</span></span> <span data-ttu-id="a50a3-145">**PREVIEWDURATION** 和 **DURATION** 元素有相同的行為。</span><span class="sxs-lookup"><span data-stu-id="a50a3-145">The **PREVIEWDURATION** and **DURATION** elements have the same behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a50a3-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="a50a3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a50a3-147">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="a50a3-147">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="a50a3-148">**使用中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="a50a3-148">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="a50a3-149">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="a50a3-149">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="a50a3-150">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="a50a3-150">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




