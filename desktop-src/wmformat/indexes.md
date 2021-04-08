---
title: 索引
description: 索引
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows Media Format SDK，索引
- Advanced Systems Format (ASF) 、索引
- ASF (Advanced Systems Format) ，索引
- Windows Media Format SDK，時態索引
- Advanced Systems Format (ASF) 、時態性索引
- ASF (Advanced Systems Format) ，時態索引
- Windows Media 格式 SDK，以框架為基礎的索引
- Advanced Systems Format (ASF) ，以框架為基礎的索引
- ASF (Advanced Systems Format) ，以框架為基礎的索引
- Windows Media Format SDK、SMPTE 時間碼
- Advanced Systems Format (ASF) 、SMPTE 時間碼
- ASF (Advanced Systems Format) ，SMPTE 時間碼
- 索引，關於
- 時態性索引
- 以框架為基礎的索引
- SMPTE 時間代碼，索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2e5a194f9c495720cbc40ccdb192509723eee0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840580"
---
# <a name="indexes"></a><span data-ttu-id="0cd74-119">索引</span><span class="sxs-lookup"><span data-stu-id="0cd74-119">Indexes</span></span>

<span data-ttu-id="0cd74-120">讀取數位媒體檔案的應用程式，常見的需求是能夠搜尋內容中的特定點。</span><span class="sxs-lookup"><span data-stu-id="0cd74-120">A common requirement for applications that read digital media files is the ability to seek to a specific point in the content.</span></span> <span data-ttu-id="0cd74-121">搜尋可能很困難，因為無法保證檔案中的各種資料流程都具有並行開始時間的範例。</span><span class="sxs-lookup"><span data-stu-id="0cd74-121">Seeking can be difficult because there is no guarantee that the various streams in a file have samples with concurrent start times.</span></span> <span data-ttu-id="0cd74-122">使用 *索引* 時，會解決此問題。</span><span class="sxs-lookup"><span data-stu-id="0cd74-122">This problem is addressed with the use of *indexes*.</span></span> <span data-ttu-id="0cd74-123">索引是一種 ASF 檔案中的物件，其呈現時間與影片範例相同。</span><span class="sxs-lookup"><span data-stu-id="0cd74-123">An index is an object in an ASF file that equates video samples with their presentation times.</span></span> <span data-ttu-id="0cd74-124">音訊串流不需要任何索引，因為音訊資料比影片資料更緊密地與展示時間連接。</span><span class="sxs-lookup"><span data-stu-id="0cd74-124">No index is required for audio streams because audio data is more closely connected with presentation time than video data is.</span></span>

<span data-ttu-id="0cd74-125">Windows Media 格式 SDK 的索引子物件可以建立三種不同類型的索引：時態性索引、以框架為基礎的索引，以及 SMPTE 時間碼索引。</span><span class="sxs-lookup"><span data-stu-id="0cd74-125">The indexer object of the Windows Media Format SDK can create three different types of indexes: temporal indexes, frame-based indexes, and SMPTE time code indexes.</span></span>

<span data-ttu-id="0cd74-126">時態性索引是最常見的類型。</span><span class="sxs-lookup"><span data-stu-id="0cd74-126">Temporal indexes are the most common type.</span></span> <span data-ttu-id="0cd74-127">它們只是將影片範例等同于相對應的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="0cd74-127">They simply equate video samples with the corresponding presentation times.</span></span>

<span data-ttu-id="0cd74-128">以畫面格為基礎的索引等於影片範例與影片框架數位和呈現時間。</span><span class="sxs-lookup"><span data-stu-id="0cd74-128">A frame-based index equates video samples with video frame numbers and presentation times.</span></span> <span data-ttu-id="0cd74-129">框架數位在編輯影片的應用程式中特別有用。</span><span class="sxs-lookup"><span data-stu-id="0cd74-129">Frame numbers are particularly useful in applications that edit video.</span></span>

<span data-ttu-id="0cd74-130">SMTPE 時間代碼索引是索引的碩果僅存類型。</span><span class="sxs-lookup"><span data-stu-id="0cd74-130">A SMTPE time code index is the rarest type of index.</span></span> <span data-ttu-id="0cd74-131">它會使用 SMPTE 時間碼作為索引的基礎，而且只能用於其範例內含 SMPTE 時間戳記的資料流程。</span><span class="sxs-lookup"><span data-stu-id="0cd74-131">It uses SMPTE time code as the basis of the index and can be used only on streams that have SMPTE time stamps included with their samples.</span></span> <span data-ttu-id="0cd74-132">如需有關 SMPTE 時間代碼的詳細資訊，請參閱 [Smpte 時間程式碼支援](smpte-time-code-support.md)。</span><span class="sxs-lookup"><span data-stu-id="0cd74-132">For more information about SMPTE time code, see [SMPTE Time Code Support](smpte-time-code-support.md).</span></span>

<span data-ttu-id="0cd74-133">ASF 檔案可以針對其所包含的每個影片資料流程，包含每個類型的索引。</span><span class="sxs-lookup"><span data-stu-id="0cd74-133">An ASF file can contain an index of each type for each video stream it contains.</span></span> <span data-ttu-id="0cd74-134">根據預設，在寫入器物件所建立的檔案中，每個影片資料流程都會包含時態索引。</span><span class="sxs-lookup"><span data-stu-id="0cd74-134">As a default, a temporal index is included for each video stream in files created by the writer object.</span></span> <span data-ttu-id="0cd74-135">您可以變更檔案的自動編制索引設定，以符合您的需求。</span><span class="sxs-lookup"><span data-stu-id="0cd74-135">You can change the automatic indexing settings for your files to suit your needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cd74-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="0cd74-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cd74-137">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="0cd74-137">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="0cd74-138">**使用索引**</span><span class="sxs-lookup"><span data-stu-id="0cd74-138">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="0cd74-139">**使用非同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="0cd74-139">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="0cd74-140">**使用同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="0cd74-140">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




