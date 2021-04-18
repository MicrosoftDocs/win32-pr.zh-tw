---
title: 使用非正方形圖元讀取資料流程
description: 使用非正方形圖元讀取資料流程
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Windows Media Format SDK，讀取影片串流
- Windows Media Format SDK、影片串流
- Windows Media Format SDK、非正方形圖元
- 'Windows Media 格式 SDK，圖元 (非正方形) '
- Advanced Systems Format (ASF) ，讀取影片串流
- ASF (Advanced 系統格式) ，讀取影片串流
- Advanced Systems Format (ASF) 、影片串流
- ASF (Advanced 系統格式) 、影片串流
- Advanced Systems Format (ASF) 、非平方圖元
- ASF (Advanced Systems Format) 、非正方形圖元
- 'Advanced Systems Format (ASF) 、圖元 (非正方形) '
- 'ASF (Advanced Systems Format) ，圖元 (非正方形) '
- 讀取影片串流
- 影片串流，讀取
- 影片串流，非正方形圖元
- 非正方形圖元
- '圖元 (非正方形) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfc14019e9822aefedb7600adc4209317293b2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965399"
---
# <a name="reading-streams-with-non-square-pixels"></a><span data-ttu-id="115a4-120">使用非正方形圖元讀取資料流程</span><span class="sxs-lookup"><span data-stu-id="115a4-120">Reading Streams with Non-Square Pixels</span></span>

<span data-ttu-id="115a4-121">需要正確處理非正方形圖元的讀取器應用程式，應該在每個範例的 ASF 標頭和資料單位延伸中檢查資料流程層級的屬性。</span><span class="sxs-lookup"><span data-stu-id="115a4-121">Reader applications that need to correctly handle non-square pixels should examine both the stream-level attributes in the ASF header and the data unit extensions on each sample.</span></span> <span data-ttu-id="115a4-122">在兩種情況下，必須調整輸出矩形以補償非正方形圖元。</span><span class="sxs-lookup"><span data-stu-id="115a4-122">There are two cases when the output rectangle must be adjusted to compensate for non-square pixels.</span></span>

<span data-ttu-id="115a4-123">從裝置（例如 DV (數位視訊）捕獲來源內容時，若其 CCD 中有非正方形圖元的數位視訊) 攝影機，讀取器應用程式必須調整其影片輸出矩形，以便在具有正方形圖元的電腦監視器上正確顯示影像。</span><span class="sxs-lookup"><span data-stu-id="115a4-123">When the source content has been captured from a device such as a DV (digital video) camera with non-square pixels in its CCD, a reader application must adjust its video output rectangle so that the image displays correctly on a computer monitor with square pixels.</span></span>

<span data-ttu-id="115a4-124">當您的讀者應用程式輸出將在 NTSC 電視上播放的影片時（例如透過視訊卡上的 S-video 輸出連線），您必須調整影片矩形，讓影像在電視的非正方形圖元上正確顯示。</span><span class="sxs-lookup"><span data-stu-id="115a4-124">When your reader application outputs video that will be played back on an NTSC television, for example through an S-Video out connection on the video card, you must adjust the video rectangle so that the image displays correctly on the television's non-square pixels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="115a4-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="115a4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="115a4-126">**使用非正方形圖元讀取和寫入影片串流**</span><span class="sxs-lookup"><span data-stu-id="115a4-126">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




