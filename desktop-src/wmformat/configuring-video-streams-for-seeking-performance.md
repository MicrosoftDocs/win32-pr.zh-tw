---
title: 設定影片串流以搜尋效能
description: 設定影片串流以搜尋效能
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- 串流，設定影片串流
- 編解碼器，設定影片串流
- 影片串流，設定
- 影片串流，效能
- 效能、影片串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681393"
---
# <a name="configuring-video-streams-for-seeking-performance"></a><span data-ttu-id="6c89e-108">設定影片串流以搜尋效能</span><span class="sxs-lookup"><span data-stu-id="6c89e-108">Configuring Video Streams for Seeking Performance</span></span>

<span data-ttu-id="6c89e-109">有些播放應用程式會對個別資料流程執行許多搜尋。</span><span class="sxs-lookup"><span data-stu-id="6c89e-109">Some playback applications perform a lot of seeking on individual streams.</span></span> <span data-ttu-id="6c89e-110">搜尋是一個區域，根據資料流程的設定而定，效能可能會有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="6c89e-110">Seeking is an area where performance can vary greatly depending upon the settings of the stream.</span></span> <span data-ttu-id="6c89e-111">如果您知道您的內容需要針對快速搜尋進行優化，您可以量身打造您的串流設定以改善效能。</span><span class="sxs-lookup"><span data-stu-id="6c89e-111">If you know your content needs to be optimized for quick seeking, you can tailor your stream configuration to improve performance.</span></span>

<span data-ttu-id="6c89e-112">影響影片中搜尋作業速度的最大因素就是主要畫面格的間距。</span><span class="sxs-lookup"><span data-stu-id="6c89e-112">The biggest factor affecting the speed of seeking operations in video is the spacing of the key frames.</span></span> <span data-ttu-id="6c89e-113">因為主要畫面格之間的每個畫面格都必須根據其前面的畫面格來重建，所以廣泛的主要畫面格結果會比搜尋時間更長。</span><span class="sxs-lookup"><span data-stu-id="6c89e-113">Because every frame between key frames needs to be reconstructed based on the frames that come before it, widely spaced key frames result longer seek times.</span></span> <span data-ttu-id="6c89e-114">例如，如果影片資料流程的每秒30個畫面格的最大索引鍵-畫面格間距為10秒，主要畫面格之間可能會有300的框架。</span><span class="sxs-lookup"><span data-stu-id="6c89e-114">For example, if a video stream with 30 frames per second has a maximum key-frame spacing of 10 seconds, there are potentially 300 frames between key frames.</span></span> <span data-ttu-id="6c89e-115">如果您搜尋到最後一個 [*delta 框架*](wmformat-glossary.md)，則必須重建299的框架，才能解壓縮框架。</span><span class="sxs-lookup"><span data-stu-id="6c89e-115">If you seek to the last [*delta frame*](wmformat-glossary.md), 299 frames have to be reconstructed for the frame to be decompressed.</span></span> <span data-ttu-id="6c89e-116">如果每個畫面格重建花費了 .01 秒，則搜尋需要大約3秒的時間。</span><span class="sxs-lookup"><span data-stu-id="6c89e-116">If each frame reconstruction took .01 second, the seek would take almost 3 seconds.</span></span> <span data-ttu-id="6c89e-117">如果您想要提高搜尋效率，請降低主要畫面格間距的協助。</span><span class="sxs-lookup"><span data-stu-id="6c89e-117">If you want to increase the efficiency of seeking, lowering the key-frame spacing can help.</span></span> <span data-ttu-id="6c89e-118">但是，如果您設定的主要畫面格太緊密，可能會失去品質。</span><span class="sxs-lookup"><span data-stu-id="6c89e-118">However, if you set the key frames too close together, you can lose quality.</span></span>

<span data-ttu-id="6c89e-119">您可以藉由呼叫 [**IWMVideoMediaProps：： SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing)來設定最大的主要畫面格間距。</span><span class="sxs-lookup"><span data-stu-id="6c89e-119">You can set the maximum key-frame spacing by calling [**IWMVideoMediaProps::SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing).</span></span> <span data-ttu-id="6c89e-120">下表列出建議值（根據資料流程的位元速率）。</span><span class="sxs-lookup"><span data-stu-id="6c89e-120">The recommended values, based on the bit rate of the stream, are listed in the following table.</span></span> <span data-ttu-id="6c89e-121">這些值可提供良好的平衡來尋找效能和品質。</span><span class="sxs-lookup"><span data-stu-id="6c89e-121">These values provide a good balance of seeking performance and quality.</span></span> <span data-ttu-id="6c89e-122">SDK 不會在主要畫面格之間的時間強制執行任何限制。</span><span class="sxs-lookup"><span data-stu-id="6c89e-122">The SDK does not enforce any limit on the time between key frames.</span></span> <span data-ttu-id="6c89e-123">一般情況下，超過30秒的時間可能會在內容透過網路進行串流處理，以及在本機播放時，對搜尋時間造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="6c89e-123">In general, times longer than 30 seconds can adversely affect seek times both when the content is streamed over a network, and when it is played back locally.</span></span>



| <span data-ttu-id="6c89e-124">位元速率</span><span class="sxs-lookup"><span data-stu-id="6c89e-124">Bit rate</span></span>             | <span data-ttu-id="6c89e-125">建議的最大索引鍵框架間距</span><span class="sxs-lookup"><span data-stu-id="6c89e-125">Suggested maximum key-frame spacing</span></span> |
|----------------------|-------------------------------------|
| <span data-ttu-id="6c89e-126">22 kbps 至 300 Kbps</span><span class="sxs-lookup"><span data-stu-id="6c89e-126">22 Kbps to 300 Kbps</span></span>  | <span data-ttu-id="6c89e-127">8秒</span><span class="sxs-lookup"><span data-stu-id="6c89e-127">8 seconds</span></span>                           |
| <span data-ttu-id="6c89e-128">300 kbps 到 600 Kbps</span><span class="sxs-lookup"><span data-stu-id="6c89e-128">300 Kbps to 600 Kbps</span></span> | <span data-ttu-id="6c89e-129">6 秒</span><span class="sxs-lookup"><span data-stu-id="6c89e-129">6 seconds</span></span>                           |
| <span data-ttu-id="6c89e-130">600 Kbps 至 2 Mbps</span><span class="sxs-lookup"><span data-stu-id="6c89e-130">600 Kbps to 2 Mbps</span></span>   | <span data-ttu-id="6c89e-131">4 秒</span><span class="sxs-lookup"><span data-stu-id="6c89e-131">4 seconds</span></span>                           |
| <span data-ttu-id="6c89e-132">2 Mbps 和更新版本</span><span class="sxs-lookup"><span data-stu-id="6c89e-132">2 Mbps and higher</span></span>    | <span data-ttu-id="6c89e-133">3 秒</span><span class="sxs-lookup"><span data-stu-id="6c89e-133">3 seconds</span></span>                           |



 

<span data-ttu-id="6c89e-134">如需在搜尋影片檔案時取得最佳效能的詳細資訊，請參閱 [取得最佳的影片尋找效能](getting-the-best-video-seeking-performance.md)。</span><span class="sxs-lookup"><span data-stu-id="6c89e-134">For more information about getting the best performance when seeking video files, see [Getting the Best Video Seeking Performance](getting-the-best-video-seeking-performance.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c89e-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="6c89e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c89e-136">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="6c89e-136">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




