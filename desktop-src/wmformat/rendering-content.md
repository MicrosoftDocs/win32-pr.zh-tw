---
title: 轉譯內容
description: 轉譯內容
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- Windows Media Format SDK，轉譯內容
- Advanced Systems Format (ASF) 、轉譯內容
- ASF (Advanced Systems Format) ，轉譯內容
- Advanced Systems Format (ASF) 、內容轉譯
- ASF (Advanced 系統格式) 、內容轉譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a171ce9b404c4cc16862ffd64b53ada5821b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840732"
---
# <a name="rendering-content"></a><span data-ttu-id="bf205-108">轉譯內容</span><span class="sxs-lookup"><span data-stu-id="bf205-108">Rendering Content</span></span>

<span data-ttu-id="bf205-109">Windows Media 格式 SDK 不提供任何常式來轉譯讀取器物件所傳遞的內容。</span><span class="sxs-lookup"><span data-stu-id="bf205-109">The Windows Media Format SDK does not provide any routines for rendering content delivered by the reader object.</span></span> <span data-ttu-id="bf205-110">如果您撰寫應用程式來播放 ASF 檔案中的內容，則必須執行您自己的轉譯常式。</span><span class="sxs-lookup"><span data-stu-id="bf205-110">If you write applications to play back the content in ASF files, you must implement your own rendering routines.</span></span>

<span data-ttu-id="bf205-111">轉譯內容時，您必須小心，以確保會以呈現時間的順序轉譯樣本，並且在轉譯時同步處理來自不同資料流程的樣本。</span><span class="sxs-lookup"><span data-stu-id="bf205-111">You must be careful when rendering content to ensure that samples are rendered in order of presentation time and that samples from different streams are synchronized when rendering.</span></span> <span data-ttu-id="bf205-112">您用來確保資料流程同步處理的方法，將取決於您針對應用程式所使用的轉譯技術。</span><span class="sxs-lookup"><span data-stu-id="bf205-112">The method you employ to ensure stream synchronization will depend upon the rendering technique you use for your application.</span></span> <span data-ttu-id="bf205-113">一般而言，如果您有音訊和影片串流，則應該同步處理至音訊串流，因為音訊串流中的不一致會比影片串流中的幾個已捨棄的框架更明顯。</span><span class="sxs-lookup"><span data-stu-id="bf205-113">In general, if you have audio and video streams, you should synchronize to the audio stream, because inconsistency in the audio stream is more noticeable than a few dropped frames in a video stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf205-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf205-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf205-115">**讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="bf205-115">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="bf205-116">**使用非同步讀取器取出媒體範例**</span><span class="sxs-lookup"><span data-stu-id="bf205-116">**To Retrieve Media Samples with the Asynchronous Reader**</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="bf205-117">**使用同步讀取器取出媒體範例**</span><span class="sxs-lookup"><span data-stu-id="bf205-117">**To Retrieve Media Samples with the Synchronous Reader**</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




