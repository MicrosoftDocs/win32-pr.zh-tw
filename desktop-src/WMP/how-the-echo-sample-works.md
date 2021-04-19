---
title: Echo 範例的運作方式
description: Echo 範例的運作方式
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Windows Media Player 外掛程式，Echo 範例總覽
- 外掛程式，Echo 範例總覽
- 數位信號處理外掛程式，Echo 範例總覽
- DSP 外掛程式，Echo 範例總覽
- Echo DSP 外掛程式範例，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08814a6f0d604c7d566a0fc8d9f07b05446fca64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106999782"
---
# <a name="how-the-echo-sample-works"></a><span data-ttu-id="7b2b7-108">Echo 範例的運作方式</span><span class="sxs-lookup"><span data-stu-id="7b2b7-108">How the Echo Sample Works</span></span>

<span data-ttu-id="7b2b7-109">程式碼會建立回應效果，方法是配置夠大的緩衝區，以包含可在延遲時間值指定的時間範圍內轉譯的音訊資料量。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-109">The code creates the echo effect by allocating a buffer large enough to contain exactly the amount of audio data that can be rendered in the time frame specified by the delay time value.</span></span> <span data-ttu-id="7b2b7-110">緩衝區的大小是以位元組為單位計算，並以下列公式計算：</span><span class="sxs-lookup"><span data-stu-id="7b2b7-110">The size of the buffer is calculated, in bytes, by the following formula:</span></span>

<span data-ttu-id="7b2b7-111">緩衝區大小 = 延遲時間 \* 採樣速率/1000 \* 區塊對齊</span><span class="sxs-lookup"><span data-stu-id="7b2b7-111">buffer size = delay time \* sample rate / 1000 \* block alignment</span></span>

<span data-ttu-id="7b2b7-112">延遲時間是以毫秒為單位。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-112">The delay time is in milliseconds.</span></span> <span data-ttu-id="7b2b7-113">取樣率和區塊對齊值會以 WAVEFORMATEX 結構提供。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-113">The sample rate and block alignment values are given in a WAVEFORMATEX structure.</span></span> <span data-ttu-id="7b2b7-114">取樣率為每秒樣本數;除以1000會每毫秒產生樣本。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-114">The sample rate is in samples per second; dividing by 1000 yields samples per millisecond.</span></span> <span data-ttu-id="7b2b7-115">區塊對齊等同于 mono 的 (1、身歷聲) 的乘積、每個樣本的位數 (8 或 16) 除以每個位元組的 8 (位) 。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-115">The block alignment is equal to the product of the number of channels (1 for mono, 2 for stereo) and the number of bits per sample (8 or 16) divided by 8 (bits per byte).</span></span>

<span data-ttu-id="7b2b7-116">除了指向延遲緩衝區開頭的指標變數之外，此程式碼會建立一個可移動指標，以逐步執行緩衝區中的資料與 **DoProcessOutput** 函數中的處理迴圈進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-116">In addition to the pointer variable that points to the head of the delay buffer, the code creates a movable pointer that steps through the data in the buffer in synchronization with the processing loop in the **DoProcessOutput** function.</span></span> <span data-ttu-id="7b2b7-117">當可移動指標到達延遲緩衝區的結尾時，會移回緩衝區的標頭。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-117">When the movable pointer reaches the end of the delay buffer, it moves back to the head of the buffer.</span></span> <span data-ttu-id="7b2b7-118">以這種方式使用的緩衝區稱為圓形緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-118">A buffer used in this manner is called a circular buffer.</span></span>

<span data-ttu-id="7b2b7-119">一旦延遲緩衝區存在，而且 Windows Media Player 配置了輸入緩衝區來提供音訊資料和輸出緩衝區來接收處理的音訊資料，回應處理會如下所示：</span><span class="sxs-lookup"><span data-stu-id="7b2b7-119">Once the delay buffer exists, and Windows Media Player has allocated an input buffer to supply audio data and an output buffer to receive processed audio data, the echo processing proceeds like this:</span></span>

1.  <span data-ttu-id="7b2b7-120">輸入可在輸入緩衝區中處理每個音訊樣本的迴圈。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-120">Enter a loop that allows processing of each audio sample in the input buffer.</span></span>
2.  <span data-ttu-id="7b2b7-121">從輸入緩衝區取出範例。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-121">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="7b2b7-122">然後，將輸入緩衝區指標向前移至下一個範例，以準備下一個迴圈反覆運算。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-122">Then, move the input buffer pointer forward to the next sample to prepare for the next loop iteration.</span></span>
3.  <span data-ttu-id="7b2b7-123">從延遲緩衝區取出範例。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-123">Retrieve a sample from the delay buffer.</span></span>
4.  <span data-ttu-id="7b2b7-124">從輸入緩衝區將範例複製到延遲緩衝區中的相同位置，以從中抓取最後一個延遲樣本。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-124">Copy the sample from the input buffer to the same location in the delay buffer from which the last delay sample was retrieved.</span></span>
5.  <span data-ttu-id="7b2b7-125">將延遲緩衝區指標向前移至下一個範例。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-125">Move the delay buffer pointer forward to the next sample.</span></span> <span data-ttu-id="7b2b7-126">如果指標移動超過緩衝區的結尾，請將它移至緩衝區的標頭。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-126">If the pointer moves past the end of the buffer, move it to the head of the buffer.</span></span>
6.  <span data-ttu-id="7b2b7-127">結合輸入緩衝區中的範例與延遲緩衝區中的範例。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-127">Combine the sample from the input buffer with the sample from the delay buffer.</span></span>
7.  <span data-ttu-id="7b2b7-128">將結果複製到輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-128">Copy the result to the output buffer.</span></span> <span data-ttu-id="7b2b7-129">然後，將輸出緩衝區指標向下移動至下一個單元，以準備下一個迴圈反復專案。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-129">Then, move the output buffer pointer forward to the next unit to prepare for the next loop iteration.</span></span>
8.  <span data-ttu-id="7b2b7-130">重複直到所有範例都已處理。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-130">Repeat until all the samples are processed.</span></span>

<span data-ttu-id="7b2b7-131">當步驟2中取出的輸入範例複製到步驟4中的延遲緩衝區時，它會一直留在那裡，直到可移動指標逐步執行延遲緩衝區中的每個樣本，最後返回相同位置為止。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-131">When an input sample retrieved in step 2 is copied to the delay buffer in step 4, it remains there until the movable pointer steps through each sample in the delay buffer and finally returns to the same position.</span></span> <span data-ttu-id="7b2b7-132">由於延遲緩衝區的大小是設計來與延遲時間相對應，因此複製到延遲緩衝區的樣本與要再次抓取的樣本之間的經過時間，等於指定的延遲 (加上實際處理) 所引進的任何延遲。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-132">Because the size of the delay buffer is designed to correspond to the delay time, the elapsed time between the sample being copied to the delay buffer and the sample being retrieved once again equals the specified delay (plus any latency introduced by the actual processing).</span></span>

<span data-ttu-id="7b2b7-133">當資料流程開始時，將不會產生延遲資料，直到延遲時間經過為止。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-133">When a stream starts, no delay data is generated until the delay time has elapsed.</span></span> <span data-ttu-id="7b2b7-134">因此，延遲緩衝區一開始必須包含無回應。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-134">Therefore, it is important that the delay buffer initially contains silence.</span></span> <span data-ttu-id="7b2b7-135">如果延遲緩衝區包含亂數據，使用者會聽到白色雜訊，直到外掛程式產生足夠的延遲資料來覆寫整個延遲緩衝區為止。</span><span class="sxs-lookup"><span data-stu-id="7b2b7-135">If the delay buffer contains random data, the user will hear white noise until the plug-in generates enough delay data to overwrite the entire delay buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b2b7-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b2b7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b2b7-137">**Echo 範例總覽**</span><span class="sxs-lookup"><span data-stu-id="7b2b7-137">**Echo Sample Overview**</span></span>](echo-sample-overview.md)
</dt> </dl>

 

 




