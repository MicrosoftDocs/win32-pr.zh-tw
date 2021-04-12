---
title: 影像串流
description: 影像串流
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows Media Format SDK，映射資料流程
- 先進的系統格式 (ASF) 、影像串流
- ASF (Advanced 系統格式) 、影像串流
- Windows Media Format SDK，資料流程
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- 影像串流，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d029715a3c722d05ee335a3a88ae4632cabbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301683"
---
# <a name="image-streams"></a><span data-ttu-id="97de7-110">影像串流</span><span class="sxs-lookup"><span data-stu-id="97de7-110">Image Streams</span></span>

<span data-ttu-id="97de7-111">影像串流是一種特殊類型的資料流程，其中包含指派給簡報時間的靜止影像。</span><span class="sxs-lookup"><span data-stu-id="97de7-111">An image stream is a special type of stream that contains still images assigned to presentation times.</span></span> <span data-ttu-id="97de7-112">應用程式可以視需要在影像資料流程中顯示圖片，但一般的執行是在下一張圖片（例如投影片放映）之前顯示每張圖片。</span><span class="sxs-lookup"><span data-stu-id="97de7-112">An application can display the pictures in an image stream as desired, but the typical implementation is to display each picture until the next picture is delivered, like a slide show.</span></span> <span data-ttu-id="97de7-113">影像資料流程通常會在具有音訊串流的檔案中進行編碼，以產生與音樂或語音同步處理的簡單影像呈現。</span><span class="sxs-lookup"><span data-stu-id="97de7-113">Usually, an image stream is encoded in a file with an audio stream to produce a simple presentation of images synchronized with music or speech.</span></span>

<span data-ttu-id="97de7-114">影像串流就像是影片串流，因為它們是從未壓縮的範例所建立，而這些樣本會壓縮為檔案撰寫程式的一部分，但它們也與任意資料流程相同，因為您必須為內容指派適當的位元速率和緩衝區視窗，而不需要依賴編解碼器指派的屬性。</span><span class="sxs-lookup"><span data-stu-id="97de7-114">Image streams are like video streams in that they are created from uncompressed samples that are compressed as part of the file writing process, but they are also like arbitrary streams because you must assign a bit rate and buffer window appropriate to the content without relying on codec-assigned properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97de7-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="97de7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97de7-116">**任意資料流程**</span><span class="sxs-lookup"><span data-stu-id="97de7-116">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="97de7-117">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="97de7-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="97de7-118">**音訊和影片串流**</span><span class="sxs-lookup"><span data-stu-id="97de7-118">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="97de7-119">**寫入影像資料流程**</span><span class="sxs-lookup"><span data-stu-id="97de7-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




