---
title: 執行 Video DSP 外掛程式
description: 執行 Video DSP 外掛程式
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Windows Media Player 外掛程式、影片 DSP
- 外掛程式、視頻 DSP
- 數位信號處理外掛程式，執行程式碼
- DSP 外掛程式，執行程式碼
- 數位信號處理外掛程式，修改範例程式碼
- DSP 外掛程式，修改範例程式碼
- 數位信號處理外掛程式、影片執行
- DSP 外掛程式、影片執行
- 影片 DSP 外掛程式，執行程式碼
- 影片 DSP 外掛程式，修改範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f1b819f328fc586d21208c00b6f0d03dca4fe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301096"
---
# <a name="implementing-a-video-dsp-plug-in"></a><span data-ttu-id="67dc2-113">執行 Video DSP 外掛程式</span><span class="sxs-lookup"><span data-stu-id="67dc2-113">Implementing a Video DSP Plug-in</span></span>

<span data-ttu-id="67dc2-114">電腦影片顯示介面卡支援一組影片格式。</span><span class="sxs-lookup"><span data-stu-id="67dc2-114">Computer video display adapters support a set of video formats.</span></span> <span data-ttu-id="67dc2-115">數位視訊編碼器也支援一組影片格式。</span><span class="sxs-lookup"><span data-stu-id="67dc2-115">Digital video codecs also support a set of video formats.</span></span> <span data-ttu-id="67dc2-116">嘗試播放特定的影片檔案時，Windows Media Player 必須選擇要用於轉譯的格式。</span><span class="sxs-lookup"><span data-stu-id="67dc2-116">When attempting to play a particular video file, Windows Media Player must choose a format to use for rendering.</span></span> <span data-ttu-id="67dc2-117">播放程式會嘗試在影片編解碼器支援的格式與視頻顯示器介面卡支援的格式（也就是產生最高品質的格式）之間尋找最相符的結果。</span><span class="sxs-lookup"><span data-stu-id="67dc2-117">The Player attempts to find the best match between the formats supported by the video codec and the formats supported by the video display adapter—that is, the one that yields the highest quality.</span></span>

<span data-ttu-id="67dc2-118">若要建立可處理影片的 Windows Media Player DSP 外掛程式，您必須先決定要讓外掛程式處理的影片格式。</span><span class="sxs-lookup"><span data-stu-id="67dc2-118">To create a Windows Media Player DSP plug-in that processes video, you'll first need to decide which video formats you'd like your plug-in to process.</span></span> <span data-ttu-id="67dc2-119">範例影片 DSP 外掛程式適用于下列影片格式：</span><span class="sxs-lookup"><span data-stu-id="67dc2-119">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="67dc2-120">NV12</span><span class="sxs-lookup"><span data-stu-id="67dc2-120">NV12</span></span>
-   <span data-ttu-id="67dc2-121">YV12</span><span class="sxs-lookup"><span data-stu-id="67dc2-121">YV12</span></span>
-   <span data-ttu-id="67dc2-122">YUY2</span><span class="sxs-lookup"><span data-stu-id="67dc2-122">YUY2</span></span>
-   <span data-ttu-id="67dc2-123">UYVY</span><span class="sxs-lookup"><span data-stu-id="67dc2-123">UYVY</span></span>
-   <span data-ttu-id="67dc2-124">RGB32</span><span class="sxs-lookup"><span data-stu-id="67dc2-124">RGB32</span></span>
-   <span data-ttu-id="67dc2-125">RGB24</span><span class="sxs-lookup"><span data-stu-id="67dc2-125">RGB24</span></span>
-   <span data-ttu-id="67dc2-126">RGB555</span><span class="sxs-lookup"><span data-stu-id="67dc2-126">RGB555</span></span>
-   <span data-ttu-id="67dc2-127">RGB565</span><span class="sxs-lookup"><span data-stu-id="67dc2-127">RGB565</span></span>

<span data-ttu-id="67dc2-128">您選擇要處理的格式是由您決定。</span><span class="sxs-lookup"><span data-stu-id="67dc2-128">Which formats you choose to process is up to you.</span></span> <span data-ttu-id="67dc2-129">您可以移除範例外掛程式的格式，使其不再受到支援，而且您可以加入程式碼來處理其他格式。</span><span class="sxs-lookup"><span data-stu-id="67dc2-129">You can remove formats from the sample plug-in so that they aren't supported any longer and you can add code to process additional formats.</span></span>

<span data-ttu-id="67dc2-130">下列各節提供在為 Windows Media Player 建立自己的影片 DSP 外掛程式之前，您應該知道的其他資訊：</span><span class="sxs-lookup"><span data-stu-id="67dc2-130">The following sections provide additional information you should know before creating your own video DSP plug-in for Windows Media Player:</span></span>

-   [<span data-ttu-id="67dc2-131">範例影片 DSP 外掛程式中的影片格式協調</span><span class="sxs-lookup"><span data-stu-id="67dc2-131">Video Format Negotiation in the Sample Video DSP Plug-in</span></span>](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="67dc2-132">範例影片 DSP 外掛程式中的 DoProcessOutput</span><span class="sxs-lookup"><span data-stu-id="67dc2-132">DoProcessOutput in the Sample Video DSP Plug-in</span></span>](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="67dc2-133">處理影片</span><span class="sxs-lookup"><span data-stu-id="67dc2-133">Processing the Video</span></span>](processing-the-video.md)

## <a name="related-topics"></a><span data-ttu-id="67dc2-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="67dc2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67dc2-135">**執行您的 DSP 程式碼**</span><span class="sxs-lookup"><span data-stu-id="67dc2-135">**Implementing Your DSP Code**</span></span>](implementing-your-dsp-code.md)
</dt> </dl>

 

 




