---
title: 檔案讀取功能
description: 檔案讀取功能
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Windows Media Format SDK，檔案讀取功能
- Windows Media Format SDK，非同步檔案讀取
- Windows Media Format SDK，同步檔案讀取
- Advanced Systems Format (ASF) 、檔案讀取功能
- ASF (Advanced 系統格式) 、檔案讀取功能
- Advanced Systems Format (ASF) 、非同步檔案讀取
- ASF (Advanced 系統格式) 、非同步檔案讀取
- Advanced Systems Format (ASF) ，同步檔案讀取
- ASF (Advanced Systems Format) ，同步檔案讀取
- 非同步檔案讀取
- 同步檔案讀取
- 同步讀取器，檔案讀取功能
- 檔案讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311270"
---
# <a name="file-reading-features"></a><span data-ttu-id="f6862-116">檔案讀取功能</span><span class="sxs-lookup"><span data-stu-id="f6862-116">File Reading Features</span></span>

<span data-ttu-id="f6862-117">讀取 ASF 檔案是 Windows Media Format SDK 的主要功能之一。</span><span class="sxs-lookup"><span data-stu-id="f6862-117">Reading ASF files is one of the primary features of the Windows Media Format SDK.</span></span> <span data-ttu-id="f6862-118">支援兩種類型的讀取：非同步和同步。</span><span class="sxs-lookup"><span data-stu-id="f6862-118">Two types of reading are supported: asynchronous and synchronous.</span></span> <span data-ttu-id="f6862-119">非同步檔案讀取是由 reader 物件處理。</span><span class="sxs-lookup"><span data-stu-id="f6862-119">Asynchronous file reading is handled by the reader object.</span></span> <span data-ttu-id="f6862-120">同步讀取器物件是用來同步讀取檔案。</span><span class="sxs-lookup"><span data-stu-id="f6862-120">The synchronous reader object is used to read files synchronously.</span></span> <span data-ttu-id="f6862-121">如需不同讀取物件的詳細資訊，請參閱 [讀取器物件](reader-object.md) 和 [同步讀取器物件](synchronous-reader-object.md)。</span><span class="sxs-lookup"><span data-stu-id="f6862-121">For more information about the different reading objects, see [Reader Object](reader-object.md) and [Synchronous Reader Object](synchronous-reader-object.md).</span></span>

<span data-ttu-id="f6862-122">在最基本的非同步檔案讀取案例中，您必須在範例準備就緒時，執行讀取器物件將呼叫的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="f6862-122">In the most basic asynchronous file reading scenario, you must implement a callback method that the reader object will call when samples are ready.</span></span> <span data-ttu-id="f6862-123">當您開始讀取檔案之後，您的應用程式會等候範例傳遞給您的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="f6862-123">After you begin reading a file, your application waits for the samples to be delivered to your callback method.</span></span> <span data-ttu-id="f6862-124">非同步讀取適用于播放程式應用程式，並支援同步讀取時無法使用的功能。</span><span class="sxs-lookup"><span data-stu-id="f6862-124">Asynchronous reading is useful for player applications, and supports features not available with synchronous reading.</span></span> <span data-ttu-id="f6862-125">如果您的應用程式需要從網路位置讀取檔案，或與執行 Windows Media Services 的伺服器互動，您必須使用 reader 物件。</span><span class="sxs-lookup"><span data-stu-id="f6862-125">If your application needs to read files from a network location, or interact with a server running Windows Media Services, you must use the reader object.</span></span> <span data-ttu-id="f6862-126">讀取器物件的缺點在於每個傳遞的輸出都會使用個別的執行緒。</span><span class="sxs-lookup"><span data-stu-id="f6862-126">The disadvantage of the reader object is that a separate thread is used for each output delivered.</span></span> <span data-ttu-id="f6862-127">此外，讀取器物件的彈性，與同步讀取器在如何提供範例之間的彈性。</span><span class="sxs-lookup"><span data-stu-id="f6862-127">Additionally, the reader object is not as flexible as the synchronous reader in how it can deliver samples.</span></span>

<span data-ttu-id="f6862-128">使用同步讀取器時，您不需要使用任何回呼方法。</span><span class="sxs-lookup"><span data-stu-id="f6862-128">With the synchronous reader you do not need to use any callback methods.</span></span> <span data-ttu-id="f6862-129">相反地，您會選取部分檔案，以使用方法呼叫一次讀取並取出範例。</span><span class="sxs-lookup"><span data-stu-id="f6862-129">Instead, you select a portion of the file to read and retrieve the samples one at a time with method calls.</span></span> <span data-ttu-id="f6862-130">同步讀取器非常適合內容編輯應用程式的需求，在這種情況下，快速存取特定範例是不可或缺的。</span><span class="sxs-lookup"><span data-stu-id="f6862-130">The synchronous reader is well suited to the needs of content-editing applications, where quick access to specific samples is essential.</span></span> <span data-ttu-id="f6862-131">因為同步讀取器不會使用任何回呼方法，所以您可以建立應用程式來讀取具有最少編碼額外負荷的 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="f6862-131">Because no callback methods are used by the synchronous reader, you can create applications to read ASF files with a minimum of coding overhead.</span></span> <span data-ttu-id="f6862-132">但是，同步讀取器無法從網路位置開啟檔案，或與執行 Windows Media Services 的伺服器互動，或讀取受 [*DRM*](wmformat-glossary.md)保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="f6862-132">However, the synchronous reader cannot open a file from a network location, or interact with a server running Windows Media Services, or read files protected with [*DRM*](wmformat-glossary.md).</span></span>

<span data-ttu-id="f6862-133">下列主題討論讀取器和同步讀取器的功能。</span><span class="sxs-lookup"><span data-stu-id="f6862-133">The following topics discuss the features of the reader and the synchronous reader.</span></span>



| <span data-ttu-id="f6862-134">主題</span><span class="sxs-lookup"><span data-stu-id="f6862-134">Topic</span></span>                                                              | <span data-ttu-id="f6862-135">描述</span><span class="sxs-lookup"><span data-stu-id="f6862-135">Description</span></span>                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6862-136">使用者配置的範例支援</span><span class="sxs-lookup"><span data-stu-id="f6862-136">User Allocated Sample Support</span></span>](user-allocated-sample-support.md) | <span data-ttu-id="f6862-137">討論讀取器和同步讀取器中的緩衝區配置，以及使用者配置可以如何改善效能。</span><span class="sxs-lookup"><span data-stu-id="f6862-137">Discusses buffer allocation in the reader and synchronous reader, and how user allocation can improve performance.</span></span> |
| [<span data-ttu-id="f6862-138">輸出格式列舉</span><span class="sxs-lookup"><span data-stu-id="f6862-138">Output Format Enumeration</span></span>](output-format-enumeration.md)         | <span data-ttu-id="f6862-139">討論輸出格式列舉。</span><span class="sxs-lookup"><span data-stu-id="f6862-139">Discusses output format enumeration.</span></span>                                                                               |



 

<span data-ttu-id="f6862-140">此外，[撰寫功能] 區段中的下列主題也適用于檔案讀取：</span><span class="sxs-lookup"><span data-stu-id="f6862-140">In addition, the following topics from the writing features section also apply to file reading:</span></span>

-   [<span data-ttu-id="f6862-141">影片調整大小</span><span class="sxs-lookup"><span data-stu-id="f6862-141">Video Resizing</span></span>](video-resizing.md)
-   [<span data-ttu-id="f6862-142">色彩空間轉換</span><span class="sxs-lookup"><span data-stu-id="f6862-142">Color Space Conversion</span></span>](color-space-conversion.md)
-   [<span data-ttu-id="f6862-143">音訊重新取樣</span><span class="sxs-lookup"><span data-stu-id="f6862-143">Audio Resampling</span></span>](audio-resampling.md)

## <a name="related-topics"></a><span data-ttu-id="f6862-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="f6862-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6862-145">**功能**</span><span class="sxs-lookup"><span data-stu-id="f6862-145">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="f6862-146">**讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="f6862-146">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




