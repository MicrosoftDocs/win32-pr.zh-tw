---
title: 使用非正方形圖元讀取和寫入影片串流
description: 使用非正方形圖元讀取和寫入影片串流
ms.assetid: fe66d13e-61cf-4bb6-9ca2-aafeabe320ec
keywords:
- Windows Media Format SDK，讀取影片串流
- Windows Media Format SDK，撰寫影片串流
- Windows Media Format SDK、影片串流
- Windows Media Format SDK、非正方形圖元
- 'Windows Media 格式 SDK，圖元 (非正方形) '
- Advanced Systems Format (ASF) ，讀取影片串流
- ASF (Advanced 系統格式) ，讀取影片串流
- Advanced Systems Format (ASF) 、撰寫影片串流
- ASF (Advanced 系統格式) 、撰寫影片串流
- Advanced Systems Format (ASF) 、影片串流
- ASF (Advanced 系統格式) 、影片串流
- Advanced Systems Format (ASF) 、非平方圖元
- ASF (Advanced Systems Format) 、非正方形圖元
- 'Advanced Systems Format (ASF) 、圖元 (非正方形) '
- 'ASF (Advanced Systems Format) ，圖元 (非正方形) '
- 讀取影片串流
- 撰寫影片串流
- 影片串流，讀取
- 影片串流，書寫
- 影片串流，非正方形圖元
- 非正方形圖元
- '圖元 (非正方形) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6b3e3ba67ba42dfc144e7f95ddd042dea0f84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300764"
---
# <a name="to-read-and-write-video-streams-with-non-square-pixels"></a><span data-ttu-id="84dcc-125">使用非正方形圖元讀取和寫入影片串流</span><span class="sxs-lookup"><span data-stu-id="84dcc-125">To Read and Write Video Streams with Non-Square Pixels</span></span>

<span data-ttu-id="84dcc-126">電腦監視器具有正方形圖元，但其他類型的影片畫面（包括 NTSC 電視）則具有矩形或非正方形圖元。</span><span class="sxs-lookup"><span data-stu-id="84dcc-126">Computer monitors have square pixels, but other types of video screens, including NTSC televisions, have rectangular or non-square pixels.</span></span> <span data-ttu-id="84dcc-127">此外，某些輸入裝置（例如數位視訊 (DV) 攝影機）會以非正方形的圖元來收取一些裝置。</span><span class="sxs-lookup"><span data-stu-id="84dcc-127">Also, some input devices, such as Digital Video (DV) cameras, have charged couple devices with non-square pixels.</span></span> <span data-ttu-id="84dcc-128">當您要撰寫以非正方形圖元來源資料為基礎的檔案，或是以非正方形圖元為基礎的裝置上顯示的檔案時，必須在 ASF 檔案中包含圖元外觀比例資訊。</span><span class="sxs-lookup"><span data-stu-id="84dcc-128">When you are writing files that are either based on non-square pixel source data or else intended for display on devices with non-square pixels, the pixel aspect ratio information must be included in the ASF file.</span></span> <span data-ttu-id="84dcc-129">讀者應用程式必須檢查該資訊，並視需要使用它來調整影片矩形的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="84dcc-129">Reader applications must examine that information and use it to adjust the aspect ratio of the video rectangle as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84dcc-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="84dcc-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84dcc-131">**Advanced 主題**</span><span class="sxs-lookup"><span data-stu-id="84dcc-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="84dcc-132">**使用非正方形圖元讀取資料流程**</span><span class="sxs-lookup"><span data-stu-id="84dcc-132">**Reading Streams with Non-Square Pixels**</span></span>](reading-streams-with-non-square-pixels.md)
</dt> <dt>

[<span data-ttu-id="84dcc-133">**以非正方形圖元撰寫資料流程**</span><span class="sxs-lookup"><span data-stu-id="84dcc-133">**Writing Streams with Non-Square Pixels**</span></span>](writing-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




