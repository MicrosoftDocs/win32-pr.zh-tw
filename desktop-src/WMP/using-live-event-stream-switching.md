---
title: 使用即時事件串流切換
description: 使用即時事件串流切換
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
keywords:
- Windows Media 中繼檔播放清單，實況活動資料流切換
- 播放清單、實況活動資料流切換
- 中繼檔播放清單，即時事件資料流程切換
- Windows Media 中繼檔播放清單，事件資料流程切換
- 播放清單、事件資料流程切換
- 中繼檔播放清單，事件資料流程切換
- Windows Media 中繼檔播放清單，廣告插入
- 播放清單、廣告插入
- 中繼檔播放清單，廣告插入
- Windows Media Player，即時事件串流切換
- Windows Media Player，事件資料流程切換
- Windows Media Player，ad 插入
- 即時事件資料流程切換
- 事件資料流程切換
- 廣告插入
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd5c586e0f1ef2b36913dee822e461daeffbfcbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183211"
---
# <a name="using-live-event-stream-switching"></a><span data-ttu-id="f6b4b-118">使用即時事件串流切換</span><span class="sxs-lookup"><span data-stu-id="f6b4b-118">Using Live Event Stream Switching</span></span>

<span data-ttu-id="f6b4b-119">串流媒體也可以透過中繼檔播放清單中具有 Windows Media 中繼檔元素的媒體串流中的指令碼命令互動來控制。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-119">Streaming media can also be controlled by the interaction of script commands embedded in a media stream with Windows Media metafile elements in a metafile playlist.</span></span>

<span data-ttu-id="f6b4b-120">事件是內嵌于媒體資料流程或媒體檔案中的特定指令碼命令類型。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-120">An event is a particular type of script command embedded in a media stream or media file.</span></span> <span data-ttu-id="f6b4b-121">當 Windows Media Player 控制項收到指令碼命令時，它會依照中繼檔播放清單中的 **事件** 專案所定義的方式來處理事件。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-121">When the Windows Media Player control receives the script command, it processes the event as defined by the **EVENT** element in the metafile playlist.</span></span> <span data-ttu-id="f6b4b-122">Windows Media Player 從目前正在轉譯的資料流程切換，並轉譯中繼檔播放清單 **事件** 專案中參考的內容。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-122">Windows Media Player switches from the current stream it is rendering and renders the content referenced in the metafile playlist **EVENT** element.</span></span> <span data-ttu-id="f6b4b-123">**事件** 元素通常用於即時生產環境。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-123">The **EVENT** element is usually used in live production.</span></span>

<span data-ttu-id="f6b4b-124">**事件** 元素看起來類似 **專案專案**，但每個專案都以不同的方式處理資料流程和媒體檔案的播放。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-124">An **EVENT** element looks similar to an **ENTRY** element, but each handles the playback of streams and media files differently.</span></span> <span data-ttu-id="f6b4b-125">**ENTRY** 元素用來建立播放清單。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-125">The **ENTRY** element is used to create playlists.</span></span> <span data-ttu-id="f6b4b-126">當前一個 **專案** 中所參考的資料流程或媒體檔案完成時，**專案專案** 中所參考的資料流程或媒體檔案就會開始播放。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-126">A stream or media file referenced in an **ENTRY** element starts playing when the stream or media file referenced in the previous **ENTRY** finishes.</span></span> <span data-ttu-id="f6b4b-127">只有在收到特定指令碼命令時，才會播放 **事件** 中所參考的資料流程。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-127">A stream referenced in an **EVENT** plays only when a specific script command is received.</span></span> <span data-ttu-id="f6b4b-128">例如，當 Windows Media Player 收到 "EVENT" 類型的指令碼命令和命令字串 "Adlink" 時，它會搜尋播放清單中的下列元素。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-128">For example, when Windows Media Player receives a script command with type string "EVENT" and the command string "Adlink", it searches the playlist for the following elements.</span></span>


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



<span data-ttu-id="f6b4b-129">然後 Windows Media Player 從即時串流切換，以播放 **事件** 中包含的資料流程或媒體檔案，在此案例中為 Adlink。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-129">Windows Media Player then switches from the live stream to play the stream or media file contained in the **EVENT**, in this case Adlink.wma.</span></span> <span data-ttu-id="f6b4b-130">`WHENDONE="RESUME"`當 Adlink 完成時，程式碼會指示 Windows Media Player 繼續播放先前的資料流程。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-130">The code `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous stream when Adlink.wma is finished.</span></span>

> [!Note]  
> <span data-ttu-id="f6b4b-131">無法處理內嵌于媒體資料流程或媒體檔案中的每個事件，可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-131">Failure to handle every event embedded in a media stream or media file may yield unexpected results.</span></span>

 

<span data-ttu-id="f6b4b-132">如果您想要使用即時事件串流切換，您必須在播放清單中包含一個 **事件** 元素，以處理內嵌在播放清單中媒體串流或媒體檔案中的每個事件指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-132">If you want to use live event stream switching, you must include one **EVENT** element in your playlist to handle each event script command embedded in the media streams or media files in your playlist.</span></span> <span data-ttu-id="f6b4b-133">建立播放清單之前，您必須知道哪些指令碼命令內嵌在數位媒體內容中的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-133">Before you create your playlist, you must know the details about which script commands are embedded in your digital media content.</span></span> <span data-ttu-id="f6b4b-134">如果有您想要 Windows Media Player 略過的事件指令碼命令，請在播放清單中包含 **事件** 專案來處理事件，但在事件處理常式中參考虛擬 URL。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-134">If there is an event script command that you want Windows Media Player to ignore, include an **EVENT** element in your playlist to handle the event, but reference a dummy URL in the event handler.</span></span>

## <a name="ad-insertion"></a><span data-ttu-id="f6b4b-135">廣告插入</span><span class="sxs-lookup"><span data-stu-id="f6b4b-135">Ad Insertion</span></span>

<span data-ttu-id="f6b4b-136">這項技術可用於廣告插入。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-136">This technique can be used for ad insertion.</span></span> <span data-ttu-id="f6b4b-137">例如，在廣播遊戲的即時網際網路廣播期間，會在每個商業中斷的開頭傳送一個命令，指示每個用戶端 (Windows Media Player) 播放播放清單中所列的電視廣告。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-137">For example, during a live Internet broadcast of a ball game, a command can be sent at the beginning of every commercial break that instructs each client (Windows Media Player) to play commercials listed in its playlist.</span></span> <span data-ttu-id="f6b4b-138">當用戶端完成播放電視廣告時，播放清單會指示每個用戶端剪回即時廣播。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-138">When clients finish playing the commercials, the playlist instructs each client to cut back to the live broadcast.</span></span> <span data-ttu-id="f6b4b-139">只有當所存取的串流媒體以相符的 **事件** 名稱廣播內嵌腳本時，才會轉譯 **事件** 媒體內容。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-139">The **EVENT** media content will be rendered only when the streaming media being accessed broadcasts embedded scripting with the matching **EVENT** name.</span></span>

<span data-ttu-id="f6b4b-140">透過標準、無線廣播以及 ads 如何使用 Windows Media 技術來觸達檢視器，以透過標準的無線廣播來與廣告之間的聯繫，以獲得最佳的 **事件** 切換潛力。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-140">The possibilities inherent in **EVENT** switching are best appreciated by contrasting how ads reach viewers through standard, over-the-air broadcasting with how ads can reach viewers using Windows Media Technologies.</span></span> <span data-ttu-id="f6b4b-141">在過去，廣播廣告只能以檢視器為目標，並使用評等資料作為主要準則。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-141">Historically, broadcast ads could only be roughly targeted at viewers, using ratings data as the primary criteria.</span></span> <span data-ttu-id="f6b4b-142">使用 Windows Media 技術傳送的 Ads 可以直接以目標使用者為目標，因為 **事件** 和播放清單可以根據使用者輸入即時建立。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-142">Ads sent using Windows Media Technologies can be aimed directly at the target user because **EVENTs** and playlists can be built on the fly based on user input.</span></span> <span data-ttu-id="f6b4b-143">如需詳細資訊，請參閱 [個人化媒體傳遞](personalizing-media-delivery.md)。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-143">For more information, see [Personalizing Media Delivery](personalizing-media-delivery.md).</span></span>

<span data-ttu-id="f6b4b-144">您也可以使用中繼檔播放清單來顯示自訂圖形、音訊和文字以進行廣告。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-144">You can also use metafile playlists to display customized graphics, audio and text for advertising.</span></span> <span data-ttu-id="f6b4b-145">您可以使用 **橫幅** 元素作為 **事件** 的子項目，以顯示廣告訊息圖形。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-145">You can use the **BANNER** element as a child element of an **EVENT** to display an advertising message graphic.</span></span> <span data-ttu-id="f6b4b-146">**橫幅** 元素會提供路徑和檔案，其中包含您廣告橫幅的圖形。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-146">The **BANNER** element provides the path and file containing the graphics for your advertising banner.</span></span> <span data-ttu-id="f6b4b-147">您也可以使用 **MOREINFO** 子項目提供網站或檔案的連結。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-147">You can also provide a link to a site or file using the **MOREINFO** child element.</span></span> <span data-ttu-id="f6b4b-148">**MOREINFO** 元素中的 URL 可以提供網路上更多廣告的連結。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-148">The URL in the **MOREINFO** element can provide a link to even more advertisements on the Web.</span></span> <span data-ttu-id="f6b4b-149">下列範例將示範如何使用這些元素。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-149">The following example demonstrates using these elements.</span></span>

<span data-ttu-id="f6b4b-150">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="f6b4b-150">Example Code</span></span>


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



<span data-ttu-id="f6b4b-151">下列範例會在用戶端收到 **名稱** 屬性設為 "Time Out" 的指令碼命令 **事件** 時，將 ad 廣告插入廣播單播資料流程改觀中。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-151">The following example inserts the ad Advert.wma into the broadcast unicast stream BallGame when a client receives a script command **EVENT** with the **NAME** attribute set to "Time-Out".</span></span> <span data-ttu-id="f6b4b-152">**CLIENTSKIP** 設定為 [否]，以防止略過資料流程的廣告。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-152">**CLIENTSKIP** is set to NO to prevent the streamed ad from being skipped.</span></span> <span data-ttu-id="f6b4b-153">在此範例中，必須先播放經過資料流程處理的廣告，然後再返回原始資料流程。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-153">In this example, the streamed ad must be played before returning to the original stream.</span></span> <span data-ttu-id="f6b4b-154">當廣告完成時，用戶端會繼續播放原始資料流程。</span><span class="sxs-lookup"><span data-stu-id="f6b4b-154">When the ad is finished, the client resumes playing the original stream.</span></span>

<span data-ttu-id="f6b4b-155">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="f6b4b-155">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="f6b4b-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="f6b4b-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6b4b-157">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="f6b4b-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f6b4b-158">**使用中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="f6b4b-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f6b4b-159">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="f6b4b-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f6b4b-160">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="f6b4b-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




