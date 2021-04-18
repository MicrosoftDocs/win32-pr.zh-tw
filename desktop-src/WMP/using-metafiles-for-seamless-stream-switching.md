---
title: 使用中繼檔進行順暢的串流切換
description: 使用中繼檔進行順暢的串流切換
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
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
ms.openlocfilehash: 29496c71c0c849480bae029f246bfd544667071e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965566"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a><span data-ttu-id="0cffa-118">使用中繼檔進行順暢的串流切換</span><span class="sxs-lookup"><span data-stu-id="0cffa-118">Using Metafiles for Seamless Stream Switching</span></span>

<span data-ttu-id="0cffa-119">您可以使用中繼檔播放清單來加速順暢的串流切換。</span><span class="sxs-lookup"><span data-stu-id="0cffa-119">You can facilitate seamless stream switching using metafile playlists.</span></span> <span data-ttu-id="0cffa-120">通常，當內容結束時，下一個剪輯或串流在開啟之前會先進行緩衝處理，然後才會開啟 (如果是從串流媒體伺服器收到的內容) 。</span><span class="sxs-lookup"><span data-stu-id="0cffa-120">Usually, when a piece of content ends, buffering occurs for the next clip or stream before it opens (if it is content received from a streaming media server).</span></span> <span data-ttu-id="0cffa-121">Microsoft Windows Media Services 可讓您將此緩衝處理時間降至最低，或至少減少最小化，並可讓另一段經過串流處理的內容幾乎立即開始播放。</span><span class="sxs-lookup"><span data-stu-id="0cffa-121">Microsoft Windows Media Services enables you to eliminate, or at least minimize, this buffering time and have another piece of streamed content begin playing nearly immediately.</span></span> <span data-ttu-id="0cffa-122">Windows Media Player 的正常操作模式是開啟播放清單在目前轉譯的資料流程結束前20秒所參考的下一個媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="0cffa-122">The normal mode of operation for Windows Media Player is to open the next media stream referenced by the playlist 20 seconds before the end of the currently rendered stream.</span></span> <span data-ttu-id="0cffa-123">這通常會在媒體串流之間提供順暢的轉換，這取決於其他因素，例如 Web 存取時間。</span><span class="sxs-lookup"><span data-stu-id="0cffa-123">This generally provides a seamless transition between media streams, depending on other factors such as Web access times.</span></span>

<span data-ttu-id="0cffa-124">使用播放清單中的 **事件** 專案搭配編碼器中的 OPENEVENT 命令，以促進資料流程或檔案之間的流暢切換。</span><span class="sxs-lookup"><span data-stu-id="0cffa-124">Use the **EVENT** element in a playlist in conjunction with OPENEVENT commands from the encoder to facilitate seamless switching between streams or files.</span></span> <span data-ttu-id="0cffa-125">在事件命令之前的20秒或更多時間內傳送 OPENEVENT 命令可將串流切換的延遲降至最低。</span><span class="sxs-lookup"><span data-stu-id="0cffa-125">Sending an OPENEVENT command 20 seconds or more prior to the EVENT command can minimize delays in stream switching.</span></span> <span data-ttu-id="0cffa-126">然後 Windows Media Player 可以將即將推出的串流內容的一部分預先載入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0cffa-126">Then Windows Media Player is able to preload a portion of the upcoming streaming content into a buffer.</span></span>

<span data-ttu-id="0cffa-127">使用 Windows Media 編碼器，在資料流程中使用下列格式傳送指令碼命令：</span><span class="sxs-lookup"><span data-stu-id="0cffa-127">Use Windows Media Encoder to send a script command in the stream using the following format:</span></span>


```XML
OPENEVENT eventname 

```



<span data-ttu-id="0cffa-128">事件名稱必須是播放清單中 **事件** 元素中定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="0cffa-128">The event name must be the one defined in the **EVENT** element in the playlist.</span></span> <span data-ttu-id="0cffa-129">當 Windows Media Player 從編碼器接收 OPENEVENT 指令碼命令時，會查看播放清單中的 **事件** 專案，並開始緩衝處理 **事件** 元素中定義的剪輯或資料流程。</span><span class="sxs-lookup"><span data-stu-id="0cffa-129">When Windows Media Player receives an OPENEVENT script command from the encoder, it looks to the **EVENT** element in the playlist and begins buffering the clip or stream defined in the **EVENT** element.</span></span> <span data-ttu-id="0cffa-130">Windows Media Player 接著保存此資訊，直到相同名稱的實際事件為止。</span><span class="sxs-lookup"><span data-stu-id="0cffa-130">Windows Media Player then holds this information until the actual event of the same name.</span></span> <span data-ttu-id="0cffa-131">收到指名的事件時，Windows Media Player 會切換至先前已緩衝處理的內容。</span><span class="sxs-lookup"><span data-stu-id="0cffa-131">When the named event is received, Windows Media Player switches to that previously buffered content.</span></span>

> [!Note]  
> <span data-ttu-id="0cffa-132">您無法在媒體檔案或播放清單中的 **事件** 元素中使用 Unicode 字元作為 OPENEVENT 指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="0cffa-132">You cannot use Unicode characters for the OPENEVENT script command in the media file or the **EVENT** element in the playlist.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0cffa-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="0cffa-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cffa-134">**建立中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="0cffa-134">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="0cffa-135">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="0cffa-135">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="0cffa-136">**ScriptCommand 事件**</span><span class="sxs-lookup"><span data-stu-id="0cffa-136">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="0cffa-137">**使用中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="0cffa-137">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="0cffa-138">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="0cffa-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="0cffa-139">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="0cffa-139">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




