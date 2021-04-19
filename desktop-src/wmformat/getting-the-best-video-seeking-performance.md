---
title: 取得最佳的影片搜尋效能
description: 取得最佳的影片搜尋效能
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- Windows Media Format SDK，最佳的影片搜尋效能
- 先進的系統格式 (ASF) ，最佳的影片搜尋效能
- ASF (Advanced Systems Format) ，最佳的影片搜尋效能
- 先進的系統格式 (ASF) 、影片搜尋效能
- ASF (Advanced Systems Format) ，影片搜尋效能
- Advanced Systems Format (ASF) ，效能
- ASF (Advanced Systems Format) ，效能
- 影片搜尋
- 效能、影片搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969052"
---
# <a name="getting-the-best-video-seeking-performance"></a><span data-ttu-id="19d87-112">取得最佳的影片搜尋效能</span><span class="sxs-lookup"><span data-stu-id="19d87-112">Getting the Best Video Seeking Performance</span></span>

<span data-ttu-id="19d87-113">搜尋檔案中的內容是很常見的作業，可能會發生效能問題。</span><span class="sxs-lookup"><span data-stu-id="19d87-113">Seeking to content in a file is a very common operation that is potentially a performance issue.</span></span> <span data-ttu-id="19d87-114">以 Windows Media 視訊9編解碼器編碼的影片主要是由差異框架組成，其只會記錄與先前畫面格相關的變更。</span><span class="sxs-lookup"><span data-stu-id="19d87-114">Video encoded with the Windows Media Video 9 codec is made up primarily of delta frames, which only record the changes in relation to the previous frame.</span></span> <span data-ttu-id="19d87-115">重建差異框架需要一些時間，特別是在主要畫面格太遠的時候。</span><span class="sxs-lookup"><span data-stu-id="19d87-115">Reconstructing delta frames takes time, particularly if the key frames are far apart.</span></span> <span data-ttu-id="19d87-116">如需設定主要畫面格以進行有效率搜尋的詳細資訊，請參閱設定 [影片串流以搜尋效能](configuring-video-streams-for-seeking-performance.md)。</span><span class="sxs-lookup"><span data-stu-id="19d87-116">For more information about configuring key frames for efficient seeking, see [Configuring Video Streams for Seeking Performance](configuring-video-streams-for-seeking-performance.md).</span></span>

<span data-ttu-id="19d87-117">除了適當的設定之外，您還可以使用影片串流的框架索引來改善搜尋效能。</span><span class="sxs-lookup"><span data-stu-id="19d87-117">In addition to proper configuration, you can improve seeking performance by using frame indexing for the video stream.</span></span> <span data-ttu-id="19d87-118">搜尋框架號碼通常比搜尋展示時間更快。</span><span class="sxs-lookup"><span data-stu-id="19d87-118">Seeking to a frame number is typically faster than seeking to a presentation time.</span></span>

<span data-ttu-id="19d87-119">如果搜尋具有多個資料流程的檔案，您應該只選取所需的資料流程。</span><span class="sxs-lookup"><span data-stu-id="19d87-119">If seeking in a file with multiple streams, you should select only the streams that are needed.</span></span> <span data-ttu-id="19d87-120">針對讀取設定的每個資料流程都會影響搜尋的效能，因為當您搜尋至檔案中的某個點時，會同步處理所有選取的資料流程。</span><span class="sxs-lookup"><span data-stu-id="19d87-120">Each stream configured for reading will affect the performance of seeking, because all selected streams are synchronized when you seek to a point in a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19d87-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="19d87-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19d87-122">**讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="19d87-122">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="19d87-123">**使用非同步讀取器依框架編號搜尋**</span><span class="sxs-lookup"><span data-stu-id="19d87-123">**To Seek By Frame Number Using the Asynchronous Reader**</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="19d87-124">**使用同步讀取器依框架編號搜尋**</span><span class="sxs-lookup"><span data-stu-id="19d87-124">**To Seek By Frame Number Using the Synchronous Reader**</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="19d87-125">**使用非同步讀取器依時間進行搜尋**</span><span class="sxs-lookup"><span data-stu-id="19d87-125">**To Seek By Time Using the Asynchronous Reader**</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="19d87-126">**使用同步讀取器依時間進行搜尋**</span><span class="sxs-lookup"><span data-stu-id="19d87-126">**To Seek By Time Using the Synchronous Reader**</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




