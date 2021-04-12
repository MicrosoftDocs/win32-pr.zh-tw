---
title: 讀取 ASF 檔案
description: 讀取 ASF 檔案
ms.assetid: e0aabe05-b317-42ac-85fc-5a75165722d4
keywords:
- Windows Media Format SDK，讀取 ASF 檔案
- 'Windows Media Format SDK、Advanced Systems Format (ASF) '
- Advanced Systems Format (ASF) ，讀取檔案
- ASF (Advanced Systems Format) ，讀取檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f35cbd0e9a7dde800e23f83337ac30cdd66582
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301847"
---
# <a name="reading-asf-files"></a><span data-ttu-id="fa931-107">讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="fa931-107">Reading ASF Files</span></span>

<span data-ttu-id="fa931-108">Windows Media Format SDK 可以用來從 ASF 檔案傳遞媒體範例。</span><span class="sxs-lookup"><span data-stu-id="fa931-108">The Windows Media Format SDK can be used to deliver media samples from an ASF file.</span></span> <span data-ttu-id="fa931-109">使用兩個物件來抓取範例、讀取器物件和同步讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="fa931-109">Two objects are used to retrieve samples, the reader object and the synchronous reader object.</span></span>

<span data-ttu-id="fa931-110">讀取器物件是 Windows Media 格式 SDK 中的原始讀取物件。</span><span class="sxs-lookup"><span data-stu-id="fa931-110">The reader object is the original reading object in the Windows Media Format SDK.</span></span> <span data-ttu-id="fa931-111">讀取器物件使用非同步架構將範例推送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="fa931-111">The reader object uses an asynchronous architecture to push samples to an application.</span></span> <span data-ttu-id="fa931-112">使用 reader 物件建立的應用程式必須執行回呼函式，以回應這個多執行緒模型所產生的各種訊息和事件。</span><span class="sxs-lookup"><span data-stu-id="fa931-112">Applications built using the reader object must implement callback functions that respond to the various messages and events that result from this multi-threaded model.</span></span> <span data-ttu-id="fa931-113">為了清楚起見，本章節將會以非同步讀取器的形式來參考 reader 物件。</span><span class="sxs-lookup"><span data-stu-id="fa931-113">For clarity, this section will refer to the reader object as the asynchronous reader.</span></span>

<span data-ttu-id="fa931-114">同步讀取器物件是此版本 Windows Media Format SDK 的新功能。</span><span class="sxs-lookup"><span data-stu-id="fa931-114">The synchronous reader object is new for this version of the Windows Media Format SDK.</span></span> <span data-ttu-id="fa931-115">同步讀取器不會使用多個執行緒來處理來自 ASF 檔案的範例。</span><span class="sxs-lookup"><span data-stu-id="fa931-115">The synchronous reader does not use multiple threads in processing samples from ASF files.</span></span> <span data-ttu-id="fa931-116">使用同步讀取器所建立的應用程式會視需要抓取範例，而不是等候讀取器傳送。</span><span class="sxs-lookup"><span data-stu-id="fa931-116">An application built using the synchronous reader retrieves samples on demand, rather than waiting for the reader to send them.</span></span>

<span data-ttu-id="fa931-117">建立應用程式以讀取 ASF 檔案時，您必須選擇要使用的讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="fa931-117">When creating an application to read ASF files, you must choose which reader object to use.</span></span> <span data-ttu-id="fa931-118">一般情況下，設計用來提供 Windows Media 內容的應用程式應該使用非同步讀取器來建立，而設計用來編輯 ASF 檔案的應用程式應該使用同步讀取器來建立。</span><span class="sxs-lookup"><span data-stu-id="fa931-118">In general, applications designed to deliver Windows Media-based content should be created using the asynchronous reader, while applications designed to edit ASF files should be created with the synchronous reader.</span></span>

<span data-ttu-id="fa931-119">下表列出兩個讀取器物件的主要功能。</span><span class="sxs-lookup"><span data-stu-id="fa931-119">The following table lists the major features of both reader objects.</span></span> <span data-ttu-id="fa931-120">您可以使用此表格來協助判斷要用於應用程式的物件。</span><span class="sxs-lookup"><span data-stu-id="fa931-120">Use this table to help determine which object to use for your application.</span></span>



| <span data-ttu-id="fa931-121">功能</span><span class="sxs-lookup"><span data-stu-id="fa931-121">Feature</span></span>                                                                    | <span data-ttu-id="fa931-122">非同步讀取器</span><span class="sxs-lookup"><span data-stu-id="fa931-122">Async reader</span></span> | <span data-ttu-id="fa931-123">同步讀者</span><span class="sxs-lookup"><span data-stu-id="fa931-123">Sync reader</span></span> |
|----------------------------------------------------------------------------|--------------|-------------|
| <span data-ttu-id="fa931-124">依輸出編號讀取未壓縮的範例</span><span class="sxs-lookup"><span data-stu-id="fa931-124">Read uncompressed samples by output number</span></span>                                 | <span data-ttu-id="fa931-125">是</span><span class="sxs-lookup"><span data-stu-id="fa931-125">Yes</span></span>          | <span data-ttu-id="fa931-126">是</span><span class="sxs-lookup"><span data-stu-id="fa931-126">Yes</span></span>         |
| <span data-ttu-id="fa931-127">依串流號碼讀取壓縮的範例</span><span class="sxs-lookup"><span data-stu-id="fa931-127">Read compressed samples by stream number</span></span>                                   | <span data-ttu-id="fa931-128">是</span><span class="sxs-lookup"><span data-stu-id="fa931-128">Yes</span></span>          | <span data-ttu-id="fa931-129">是</span><span class="sxs-lookup"><span data-stu-id="fa931-129">Yes</span></span>         |
| <span data-ttu-id="fa931-130">依串流號碼讀取未壓縮的範例</span><span class="sxs-lookup"><span data-stu-id="fa931-130">Read uncompressed samples by stream number</span></span>                                 | <span data-ttu-id="fa931-131">否</span><span class="sxs-lookup"><span data-stu-id="fa931-131">No</span></span>           | <span data-ttu-id="fa931-132">是</span><span class="sxs-lookup"><span data-stu-id="fa931-132">Yes</span></span>         |
| <span data-ttu-id="fa931-133">從網際網路網站讀取</span><span class="sxs-lookup"><span data-stu-id="fa931-133">Read from Internet site</span></span>                                                    | <span data-ttu-id="fa931-134">是</span><span class="sxs-lookup"><span data-stu-id="fa931-134">Yes</span></span>          | <span data-ttu-id="fa931-135">否</span><span class="sxs-lookup"><span data-stu-id="fa931-135">No</span></span>          |
| <span data-ttu-id="fa931-136">讀取中繼資料</span><span class="sxs-lookup"><span data-stu-id="fa931-136">Read metadata</span></span>                                                              | <span data-ttu-id="fa931-137">是</span><span class="sxs-lookup"><span data-stu-id="fa931-137">Yes</span></span>          | <span data-ttu-id="fa931-138">是</span><span class="sxs-lookup"><span data-stu-id="fa931-138">Yes</span></span>         |
| <span data-ttu-id="fa931-139">搜尋展示時間</span><span class="sxs-lookup"><span data-stu-id="fa931-139">Seek to presentation time</span></span>                                                  | <span data-ttu-id="fa931-140">是</span><span class="sxs-lookup"><span data-stu-id="fa931-140">Yes</span></span>          | <span data-ttu-id="fa931-141">是</span><span class="sxs-lookup"><span data-stu-id="fa931-141">Yes</span></span>         |
| <span data-ttu-id="fa931-142">搜尋至框架</span><span class="sxs-lookup"><span data-stu-id="fa931-142">Seek to frame</span></span>                                                              | <span data-ttu-id="fa931-143">是</span><span class="sxs-lookup"><span data-stu-id="fa931-143">Yes</span></span>          | <span data-ttu-id="fa931-144">是</span><span class="sxs-lookup"><span data-stu-id="fa931-144">Yes</span></span>         |
| <span data-ttu-id="fa931-145">搜尋至標記</span><span class="sxs-lookup"><span data-stu-id="fa931-145">Seek to marker</span></span>                                                             | <span data-ttu-id="fa931-146">是</span><span class="sxs-lookup"><span data-stu-id="fa931-146">Yes</span></span>          | <span data-ttu-id="fa931-147">否</span><span class="sxs-lookup"><span data-stu-id="fa931-147">No</span></span>          |
| <span data-ttu-id="fa931-148">在播放期間于壓縮和未壓縮的範例傳遞之間切換</span><span class="sxs-lookup"><span data-stu-id="fa931-148">Switch between compressed and uncompressed sample delivery during playback</span></span> | <span data-ttu-id="fa931-149">否</span><span class="sxs-lookup"><span data-stu-id="fa931-149">No</span></span>           | <span data-ttu-id="fa931-150">是</span><span class="sxs-lookup"><span data-stu-id="fa931-150">Yes</span></span>         |
| <span data-ttu-id="fa931-151">使用 **IStream** 介面開啟檔案</span><span class="sxs-lookup"><span data-stu-id="fa931-151">Open files using **IStream** interface</span></span>                                     | <span data-ttu-id="fa931-152">是</span><span class="sxs-lookup"><span data-stu-id="fa931-152">Yes</span></span>          | <span data-ttu-id="fa931-153">是</span><span class="sxs-lookup"><span data-stu-id="fa931-153">Yes</span></span>         |



 

<span data-ttu-id="fa931-154">下列各節提供有關使用兩個讀取器物件的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fa931-154">The following sections provide more information about working with the two reader objects.</span></span>



| <span data-ttu-id="fa931-155">區段</span><span class="sxs-lookup"><span data-stu-id="fa931-155">Section</span></span>                                                                                      | <span data-ttu-id="fa931-156">描述</span><span class="sxs-lookup"><span data-stu-id="fa931-156">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa931-157">使用輸出</span><span class="sxs-lookup"><span data-stu-id="fa931-157">Working with Outputs</span></span>](working-with-outputs.md)                                             | <span data-ttu-id="fa931-158">說明如何使用和操作輸出。</span><span class="sxs-lookup"><span data-stu-id="fa931-158">Describes how to use and manipulate outputs.</span></span> <span data-ttu-id="fa931-159">適用于這兩個讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="fa931-159">Applies to both reader objects.</span></span>                                                            |
| [<span data-ttu-id="fa931-160">設定檔案讀取的緩衝區</span><span class="sxs-lookup"><span data-stu-id="fa931-160">Allocating Buffers for File Reading</span></span>](allocating-buffers-for-file-reading.md)               | <span data-ttu-id="fa931-161">說明如何使用您自己的緩衝區集區來保存讀取器或同步讀取器所提供的範例。</span><span class="sxs-lookup"><span data-stu-id="fa931-161">Describes how to use your own pool of buffers to hold samples delivered by the reader or synchronous reader.</span></span>                            |
| [<span data-ttu-id="fa931-162">在播放時讀取中繼資料</span><span class="sxs-lookup"><span data-stu-id="fa931-162">Reading Metadata at Playback</span></span>](reading-metadata-at-playback.md)                             | <span data-ttu-id="fa931-163">描述如何在播放時利用中繼資料支援。</span><span class="sxs-lookup"><span data-stu-id="fa931-163">Describes how to take advantage of metadata support at playback.</span></span> <span data-ttu-id="fa931-164">適用于這兩個讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="fa931-164">Applies to both reader objects.</span></span>                                        |
| [<span data-ttu-id="fa931-165">在播放時取得設定檔資訊</span><span class="sxs-lookup"><span data-stu-id="fa931-165">Getting Profile Information at Playback</span></span>](getting-profile-information-at-playback.md)       | <span data-ttu-id="fa931-166">說明如何存取已開啟檔案的設定檔資訊。</span><span class="sxs-lookup"><span data-stu-id="fa931-166">Describes how to access profile information for opened files.</span></span> <span data-ttu-id="fa931-167">適用于這兩個讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="fa931-167">Applies to both reader objects.</span></span>                                           |
| [<span data-ttu-id="fa931-168">讀取多頻道音訊</span><span class="sxs-lookup"><span data-stu-id="fa931-168">Reading Multichannel Audio</span></span>](reading-multichannel-audio.md)                                 | <span data-ttu-id="fa931-169">描述如何設定寫入器以正確地將多頻道音訊解碼。</span><span class="sxs-lookup"><span data-stu-id="fa931-169">Describes how to configure the writer to properly decode multichannel audio.</span></span>                                                            |
| [<span data-ttu-id="fa931-170">轉譯內容</span><span class="sxs-lookup"><span data-stu-id="fa931-170">Rendering Content</span></span>](rendering-content.md)                                                   | <span data-ttu-id="fa931-171">討論轉譯未壓縮範例的相關問題。</span><span class="sxs-lookup"><span data-stu-id="fa931-171">Discusses the issues related to rendering uncompressed samples.</span></span> <span data-ttu-id="fa931-172">適用于這兩個讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="fa931-172">Applies to both reader objects.</span></span>                                         |
| [<span data-ttu-id="fa931-173">取得最佳的影片搜尋效能</span><span class="sxs-lookup"><span data-stu-id="fa931-173">Getting the Best Video Seeking Performance</span></span>](getting-the-best-video-seeking-performance.md) | <span data-ttu-id="fa931-174">描述改善影片搜尋效能的方法。</span><span class="sxs-lookup"><span data-stu-id="fa931-174">Describes ways to improve video seeking performance.</span></span>                                                                                    |
| [<span data-ttu-id="fa931-175">使用非同步讀取器讀取檔案</span><span class="sxs-lookup"><span data-stu-id="fa931-175">Reading Files with the Asynchronous Reader</span></span>](reading-files-with-the-asynchronous-reader.md) | <span data-ttu-id="fa931-176">說明如何使用非同步讀取器物件讀取 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="fa931-176">Describes how to read ASF files using the asynchronous reader object.</span></span>                                                                   |
| [<span data-ttu-id="fa931-177">使用同步讀取器讀取檔案</span><span class="sxs-lookup"><span data-stu-id="fa931-177">Reading Files with the Synchronous Reader</span></span>](reading-files-with-the-synchronous-reader.md)   | <span data-ttu-id="fa931-178">說明如何使用同步讀取器物件讀取 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="fa931-178">Describes how to read ASF files using the synchronous reader object.</span></span>                                                                    |
| [<span data-ttu-id="fa931-179">啟用 DirectX Video 加速</span><span class="sxs-lookup"><span data-stu-id="fa931-179">Enabling DirectX Video Acceleration</span></span>](enabling-directx-video-acceleration.md)               | <span data-ttu-id="fa931-180">說明如何執行 DirectX Video 加速，以使用部分視訊卡的硬體加速功能來解碼影片。</span><span class="sxs-lookup"><span data-stu-id="fa931-180">Describes how to implement DirectX Video Acceleration to use the hardware acceleration features of some video cards for decoding video.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fa931-181">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa931-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa931-182">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="fa931-182">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="fa931-183">**讀取器物件**</span><span class="sxs-lookup"><span data-stu-id="fa931-183">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="fa931-184">**同步讀取器物件**</span><span class="sxs-lookup"><span data-stu-id="fa931-184">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> </dl>

 

 




