---
title: 互斥
description: 互斥
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- Windows Media Format SDK，相互排除
- Advanced Systems Format (ASF) ，相互排除
- ASF (Advanced Systems Format) ，相互排除
- Windows Media Format SDK，MBR 相互排除
- Advanced Systems Format (ASF) 、MBR 相互排除
- ASF (Advanced Systems Format) ，MBR 相互排除
- Windows Media 格式 SDK， (MBR) 多位元率
- 'Advanced Systems Format (ASF) 、多位元率 (MBR) '
- 'ASF (Advanced Systems Format) 、多重位元速率 (MBR) '
- 相互排除，關於
- 多重位元速率 (MBR) ，相互排除
- MBR (多位元率) ，相互排除
- 相互排除，位元速率
- 相互排除，語言
- 相互排除，簡報
- 相互排除，未知
- 相互排除，功能
- 相互排除，先進的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd00bf5bcb544d2541a6bc5465171fe9bacc1b9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840772"
---
# <a name="mutual-exclusion"></a><span data-ttu-id="43259-121">互斥</span><span class="sxs-lookup"><span data-stu-id="43259-121">Mutual Exclusion</span></span>

<span data-ttu-id="43259-122">每個 ASF 檔案都包含一或多個資料流程，每個都包含數位媒體資料。</span><span class="sxs-lookup"><span data-stu-id="43259-122">Every ASF file contains one or more streams, each containing digital media data.</span></span> <span data-ttu-id="43259-123">在一般情況下，每個資料流程都會與單一輸出相關聯。</span><span class="sxs-lookup"><span data-stu-id="43259-123">Under normal circumstances, each stream is associated with a single output.</span></span> <span data-ttu-id="43259-124">在播放時，讀取器物件會提供每個輸出的範例。</span><span class="sxs-lookup"><span data-stu-id="43259-124">On playback, the reader object delivers samples for each output.</span></span> <span data-ttu-id="43259-125">因此，根據預設，ASF 檔案中的每個串流都是由讀取器在播放時傳遞。</span><span class="sxs-lookup"><span data-stu-id="43259-125">So, as a default, every stream in an ASF file is delivered by the reader on playback.</span></span>

<span data-ttu-id="43259-126">在某些情況下，您不希望每個串流傳遞至用戶端。</span><span class="sxs-lookup"><span data-stu-id="43259-126">There are situations where you do not want every stream delivered to the client.</span></span> <span data-ttu-id="43259-127">例如，如果您建立包含五個音訊串流的影片檔案，每五種語言各一個，您只想要一次傳遞其中一個。</span><span class="sxs-lookup"><span data-stu-id="43259-127">For example, if you create a video file with five audio streams, one for each of five languages, you want only one of them to be delivered at a time.</span></span> <span data-ttu-id="43259-128">相互排除是 Windows Media Format SDK 的一項功能，可讓您指定所有等同于相同輸出的互斥資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="43259-128">Mutual exclusion is a feature of the Windows Media Format SDK that enables you to specify a number of mutually exclusive streams that all equate to the same output.</span></span>

<span data-ttu-id="43259-129">相互排除定義在用來建立檔案的設定檔中。</span><span class="sxs-lookup"><span data-stu-id="43259-129">Mutual exclusion is defined in the profile used to create a file.</span></span> <span data-ttu-id="43259-130">您可以使用相互排除物件，在設定檔中設定相互排除。</span><span class="sxs-lookup"><span data-stu-id="43259-130">You configure mutual exclusion in a profile by using mutual exclusion objects.</span></span> <span data-ttu-id="43259-131">您可以一次將一個資料流程新增至相互排除物件、設定類型，並在設定檔中包含物件。</span><span class="sxs-lookup"><span data-stu-id="43259-131">You add streams one at a time to the mutual exclusion object, set the type, and include the object in the profile.</span></span>

<span data-ttu-id="43259-132">Windows Media Format SDK 會辨識四種相互排除類型：</span><span class="sxs-lookup"><span data-stu-id="43259-132">The Windows Media Format SDK recognizes four types of mutual exclusion:</span></span>

-   <span data-ttu-id="43259-133">位元速率</span><span class="sxs-lookup"><span data-stu-id="43259-133">Bit rate</span></span>
-   <span data-ttu-id="43259-134">語言</span><span class="sxs-lookup"><span data-stu-id="43259-134">Language</span></span>
-   <span data-ttu-id="43259-135">簡報</span><span class="sxs-lookup"><span data-stu-id="43259-135">Presentation</span></span>
-   <span data-ttu-id="43259-136">Unknown</span><span class="sxs-lookup"><span data-stu-id="43259-136">Unknown</span></span>

## <a name="mutual-exclusion-by-bit-rate"></a><span data-ttu-id="43259-137">依位速率的互斥</span><span class="sxs-lookup"><span data-stu-id="43259-137">Mutual Exclusion by Bit Rate</span></span>

<span data-ttu-id="43259-138">位元速率互斥是一種特殊的互斥，較常見的方式是使用 (MBR) 互斥的多重位元速率。</span><span class="sxs-lookup"><span data-stu-id="43259-138">Bit rate mutual exclusion is a special type of mutual exclusion and is more commonly referred to as multiple bit rate (MBR) mutual exclusion.</span></span> <span data-ttu-id="43259-139">MBR 相互排除包含許多資料流程，這些資料流程全都源自相同的輸入，但以不同的位元速率編碼。</span><span class="sxs-lookup"><span data-stu-id="43259-139">An MBR mutual exclusion contains a number of streams that all originate from the same input, but are encoded at different bit rates.</span></span> <span data-ttu-id="43259-140">使用 MBR 播放檔案時，讀取器會根據可用的頻寬來決定要使用的最佳串流。</span><span class="sxs-lookup"><span data-stu-id="43259-140">When playing a file with MBR, the reader determines the best stream to use based on the available bandwidth.</span></span>

<span data-ttu-id="43259-141">Windows Media Format SDK 支援適用于音訊和影片串流的 MBR。</span><span class="sxs-lookup"><span data-stu-id="43259-141">The Windows Media Format SDK supports MBR for audio and video streams.</span></span> <span data-ttu-id="43259-142">SDK 也支援一種特殊類型的 MBR 影片，稱為多個影片大小 MBR。</span><span class="sxs-lookup"><span data-stu-id="43259-142">The SDK also supports a special type of MBR video called multiple video size MBR.</span></span> <span data-ttu-id="43259-143">這就像一般的 MBR 影片，不同之處在于個別的串流可以有不同的框架大小。</span><span class="sxs-lookup"><span data-stu-id="43259-143">This is like normal MBR video except that the individual streams can have different frame sizes.</span></span> <span data-ttu-id="43259-144">例如，您可能會有一些串流處於預設的 320 x 240 影片大小，有些則具有較高的位元速率和 640 x 480 的影片大小。</span><span class="sxs-lookup"><span data-stu-id="43259-144">For example, you might have some streams at the default 320 x 240 video size and some others with higher bit rates and 640 x 480 video size.</span></span>

## <a name="mutual-exclusion-by-language"></a><span data-ttu-id="43259-145">依語言的相互排除</span><span class="sxs-lookup"><span data-stu-id="43259-145">Mutual Exclusion by Language</span></span>

<span data-ttu-id="43259-146">以語言為基礎的相互排除是設計用來搭配內容 (通常是音訊) 以數種語言錄製。</span><span class="sxs-lookup"><span data-stu-id="43259-146">Language-based mutual exclusion is designed for use with content (usually audio) recorded in several languages.</span></span> <span data-ttu-id="43259-147">以語言為基礎的互斥包含數個源自唯一輸入的資料流程。</span><span class="sxs-lookup"><span data-stu-id="43259-147">A language-based mutual exclusion includes several streams that originate from unique inputs.</span></span> <span data-ttu-id="43259-148">每個輸入都是相同的內容，但使用不同的語言。</span><span class="sxs-lookup"><span data-stu-id="43259-148">Each input is the same content, but in a different language.</span></span>

<span data-ttu-id="43259-149">若要讓語言的相互排除運作，讀取應用程式必須包含用來選取適當語言的邏輯。</span><span class="sxs-lookup"><span data-stu-id="43259-149">For mutual exclusion by language to work, the reading application must include logic to select the appropriate language.</span></span> <span data-ttu-id="43259-150">如果您撰寫應用程式來播放 ASF 檔案，而且您想要支援以語言為基礎的相互排除的檔案，您應該在開始播放之前選取適當的資料流程。</span><span class="sxs-lookup"><span data-stu-id="43259-150">If you write an application to play ASF files, and you want to support files with language-based mutual exclusion, you should select the appropriate stream before beginning playback.</span></span>

## <a name="mutual-exclusion-by-presentation"></a><span data-ttu-id="43259-151">依簡報的相互排除</span><span class="sxs-lookup"><span data-stu-id="43259-151">Mutual Exclusion by Presentation</span></span>

<span data-ttu-id="43259-152">為了支援包含以不同外觀比例編碼之相同內容的影片串流，提供以呈現為基礎的相互排除。</span><span class="sxs-lookup"><span data-stu-id="43259-152">Presentation-based mutual exclusion is provided to support video streams that contain the same content encoded with different aspect ratios.</span></span> <span data-ttu-id="43259-153">一般來說，在黑邊版本中提供影片時，會使用這種方式 (外觀比例 16:9) ，以及針對電視螢幕格式化 (外觀比例 4:3) 。</span><span class="sxs-lookup"><span data-stu-id="43259-153">Typically, this is used when providing video in a letterbox version (aspect ratio 16:9) as well as formatted for television screens (aspect ratio 4:3).</span></span>

<span data-ttu-id="43259-154">選取要播放的簡報最常由使用者決定。</span><span class="sxs-lookup"><span data-stu-id="43259-154">The selection of a presentation for playback is most often determined by the user.</span></span> <span data-ttu-id="43259-155">如果您撰寫應用程式來播放 ASF 檔案，並且想要支援具有以標記法為基礎之相互排除的檔案，您應該讓使用者選取要進行查看的簡報類型。</span><span class="sxs-lookup"><span data-stu-id="43259-155">If you write an application to play ASF files and want to support files with presentation based mutual exclusion, you should present the user with the option of selecting a presentation type for viewing.</span></span>

## <a name="unknown-mutual-exclusion"></a><span data-ttu-id="43259-156">未知的互斥</span><span class="sxs-lookup"><span data-stu-id="43259-156">Unknown Mutual Exclusion</span></span>

<span data-ttu-id="43259-157">您可以根據任何您喜歡的準則建立相互排除。</span><span class="sxs-lookup"><span data-stu-id="43259-157">You can create mutual exclusion based on any criteria you like.</span></span> <span data-ttu-id="43259-158">所有的自訂相互排除類型都應使用未知的類型建立。</span><span class="sxs-lookup"><span data-stu-id="43259-158">All custom mutual exclusion types should be created using the unknown type.</span></span>

## <a name="advanced-mutual-exclusion-features"></a><span data-ttu-id="43259-159">先進的互斥功能</span><span class="sxs-lookup"><span data-stu-id="43259-159">Advanced Mutual Exclusion Features</span></span>

<span data-ttu-id="43259-160">您也可以使用相互排除，將資料流程指派給彼此互斥的群組。</span><span class="sxs-lookup"><span data-stu-id="43259-160">You can also use mutual exclusion to assign streams to groups that are mutually exclusive of one another.</span></span> <span data-ttu-id="43259-161">例如，您可能想要有多種語言的音訊串流，並將不同的影片串流指派給每個語言。</span><span class="sxs-lookup"><span data-stu-id="43259-161">For example, you might want to have audio streams in multiple languages and assign a different video stream to each.</span></span> <span data-ttu-id="43259-162">您可以使用相互排除，將每個音訊串流與其對應的影片資料流程群組在一起，並讓所有群組彼此互斥。</span><span class="sxs-lookup"><span data-stu-id="43259-162">You use mutual exclusion to group each audio stream with its corresponding video stream and make all groups mutually exclusive.</span></span>

<span data-ttu-id="43259-163">讀取器會自動選取所有相互排除的資料流程。</span><span class="sxs-lookup"><span data-stu-id="43259-163">The reader automatically selects streams for all mutual exclusions.</span></span> <span data-ttu-id="43259-164">對於所有相互排除的類型（MBR 和以語言為基礎的互斥除外），讀取器一律會選取預設資料流程，這是新增至設定檔中互斥物件的第一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="43259-164">For all types of mutual exclusion except MBR and language-based mutual exclusion, the reader always selects the default stream, which is the first stream added to the mutual exclusion object in the profile.</span></span> <span data-ttu-id="43259-165">若為 MBR，讀取器會選取最適合在播放時使用之頻寬的資料流程。</span><span class="sxs-lookup"><span data-stu-id="43259-165">For MBR, the reader selects the stream that best suits the available bandwidth at the time of playback.</span></span> <span data-ttu-id="43259-166">如果您不想要使用預設資料流程，您可以在開始讀取檔案之前，將資料流程選取範圍設定為 [手動]。</span><span class="sxs-lookup"><span data-stu-id="43259-166">If you do not want to use the default stream, you can set stream selection to manual before starting to read a file.</span></span>

<span data-ttu-id="43259-167">手動資料流程選取會套用至整個檔案。</span><span class="sxs-lookup"><span data-stu-id="43259-167">Manual stream selection applies to the entire file.</span></span> <span data-ttu-id="43259-168">當您在相同的檔案中有不同類型的相互排除時，可能會發生問題。</span><span class="sxs-lookup"><span data-stu-id="43259-168">Difficulties can arise when you have mutual exclusions of different types in the same file.</span></span> <span data-ttu-id="43259-169">例如，檔案可以同時包含以位速率為基礎的互斥和自訂相互排除。</span><span class="sxs-lookup"><span data-stu-id="43259-169">For example, a file can contain both bit-rate-based mutual exclusion and custom mutual exclusion.</span></span> <span data-ttu-id="43259-170">若要選取自訂互斥排除中預設值以外的資料流程，您必須使用手動選取資料流程。</span><span class="sxs-lookup"><span data-stu-id="43259-170">To select a stream other than the default in the custom mutual exclusion, you must use manual stream selection.</span></span> <span data-ttu-id="43259-171">但是，如果您使用手動資料流程選取，則讀取器不會自動選取多個位速率資料流程。</span><span class="sxs-lookup"><span data-stu-id="43259-171">If you use manual stream selection, however, the reader will not automatically select the multiple bit rate stream.</span></span> <span data-ttu-id="43259-172">如果您打算支援單一檔案中的多個相互排除類型，則必須在應用程式中規劃此可能性。</span><span class="sxs-lookup"><span data-stu-id="43259-172">You must plan for this eventuality in your application if you plan to support multiple types of mutual exclusion in a single file.</span></span> <span data-ttu-id="43259-173">這通常表示建立您自己的資料流程選取專案常式，以供一般自動的相互排除類型之用。</span><span class="sxs-lookup"><span data-stu-id="43259-173">Typically this means creating your own stream selection routines for normally automatic types of mutual exclusion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43259-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="43259-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43259-175">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="43259-175">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="43259-176">**使用相互排除**</span><span class="sxs-lookup"><span data-stu-id="43259-176">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> </dl>

 

 




