---
title: 使用計時層級
description: 使用計時層級
ms.assetid: 4a253521-3036-488a-98bc-62596b538f68
keywords:
- 視覺效果，計時事件
- 自訂視覺效果，計時事件
- 視覺效果、頻率陣列
- 自訂視覺效果、頻率陣列
- 視覺效果、波形陣列
- 自訂視覺效果、波形陣列
- 視覺效果，狀態變數
- 自訂視覺效果，狀態變數
- 視覺效果、時間戳記變數
- 自訂視覺效果，timeStamp 變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2d9a23818d57305b3b205ea2e17b6dda2884e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021473"
---
# <a name="using-timed-levels"></a><span data-ttu-id="23b8a-113">使用計時層級</span><span class="sxs-lookup"><span data-stu-id="23b8a-113">Using Timed Levels</span></span>

<span data-ttu-id="23b8a-114">**TimedLevel** 結構是由 2 2 維度陣列、狀態值和時間戳記值所組成。</span><span class="sxs-lookup"><span data-stu-id="23b8a-114">The **TimedLevel** structure is composed of two two-dimensional arrays, a state value, and a time stamp value.</span></span>

## <a name="frequency-array"></a><span data-ttu-id="23b8a-115">頻率陣列</span><span class="sxs-lookup"><span data-stu-id="23b8a-115">Frequency Array</span></span>

<span data-ttu-id="23b8a-116">頻率陣列是二維陣列。</span><span class="sxs-lookup"><span data-stu-id="23b8a-116">The frequency array is a two-dimensional array.</span></span> <span data-ttu-id="23b8a-117">每個陣列的第一個維度會對應到身歷聲音訊頻道 (左或右) ，而第二個維度對應到快照集的頻率層級 (（以位元組為單位) ），其中的音訊頻譜會分成1024個區域。</span><span class="sxs-lookup"><span data-stu-id="23b8a-117">The first dimension of each array corresponds to the stereo audio channel (left or right), and the second corresponds to the frequency levels (in bytes) of the snapshot, where the audio spectrum is divided up into 1024 regions.</span></span>

<span data-ttu-id="23b8a-118">您可以透過下列方式取得從 Windows Media Player 提供的頻率陣列資料：</span><span class="sxs-lookup"><span data-stu-id="23b8a-118">You can get the frequency array data supplied from the Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->frequency[0][0];
```



<span data-ttu-id="23b8a-119">Snapshot 的值適用于左邊的通道，且包含 frequency 頻譜的最小部分值。</span><span class="sxs-lookup"><span data-stu-id="23b8a-119">The value of snapshot is for the left channel and contains the value of the lowest part of the frequency spectrum.</span></span> <span data-ttu-id="23b8a-120">例如，如果快照集有很大的值，則會指出頻率頻譜的最低1024th 部分在頻率方面很豐富。</span><span class="sxs-lookup"><span data-stu-id="23b8a-120">For example, if snapshot has a large value, it indicates that the lowest 1024th part of the frequency spectrum is rich in frequency.</span></span> <span data-ttu-id="23b8a-121">值為零表示左方頻道的範圍內沒有低頻率值。</span><span class="sxs-lookup"><span data-stu-id="23b8a-121">A value of zero indicates no low frequency values in that part of the spectrum for the left channel.</span></span> <span data-ttu-id="23b8a-122">如果您有單聲道信號，則只有第一個維度具有有效的值。</span><span class="sxs-lookup"><span data-stu-id="23b8a-122">If you have a monophonic signal, only the first dimension has valid values.</span></span>

<span data-ttu-id="23b8a-123">如果信號為非身歷聲，則第二個數組將包含 mono 信號的複本。</span><span class="sxs-lookup"><span data-stu-id="23b8a-123">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="23b8a-124">也就是說，frequency \[ 0 \] \[ *n* \] 和 frequency \[ 1 \] \[ *n* \] 會包含相同的資料，其中 *n* 是特定資料格的索引。</span><span class="sxs-lookup"><span data-stu-id="23b8a-124">That is, frequency\[0\]\[*n*\] and frequency\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="waveform-array"></a><span data-ttu-id="23b8a-125">波形陣列</span><span class="sxs-lookup"><span data-stu-id="23b8a-125">Waveform Array</span></span>

<span data-ttu-id="23b8a-126">波形陣列也是二維陣列。</span><span class="sxs-lookup"><span data-stu-id="23b8a-126">The waveform array is also a two-dimensional array.</span></span> <span data-ttu-id="23b8a-127">陣列的第一個維度會對應至通道 (左或右) ，而第二個維度對應到快照集的電源等級 (（以位元組為單位）) ，其中音訊電源會分成1024個連續的時間區段。</span><span class="sxs-lookup"><span data-stu-id="23b8a-127">The first dimension of the array corresponds to the channel (left or right), and the second corresponds to the power levels (in bytes) of the snapshot, where the audio power is broken up into 1024 contiguous time segments.</span></span>

<span data-ttu-id="23b8a-128">您可以利用下列方式，從 Windows Media Player 取得波形陣列資料：</span><span class="sxs-lookup"><span data-stu-id="23b8a-128">You can get the waveform array data from Windows Media Player in the following manner:</span></span>


```C++
TimedLevel *pLevels;
int snapshot = pLevels->waveform[0][0];

```



<span data-ttu-id="23b8a-129">Snapshot 的值適用于左邊通道，並且包含電源值的量化快照的第一個值。</span><span class="sxs-lookup"><span data-stu-id="23b8a-129">The value of snapshot is for the left channel and contains the first value of the quantized snapshot of the power values.</span></span> <span data-ttu-id="23b8a-130">建立快照集時，它是由1024的微小遞增量值所組成。</span><span class="sxs-lookup"><span data-stu-id="23b8a-130">When a snapshot is taken, it consists of 1024 tiny incremental measurements of the audio power.</span></span> <span data-ttu-id="23b8a-131">陣列的最小值是由音訊電源的第一次遞增量值所產生。</span><span class="sxs-lookup"><span data-stu-id="23b8a-131">The lowest value of the array is generated by the first incremental measurement of audio power.</span></span> <span data-ttu-id="23b8a-132">請注意，乘冪的值是從-128 到 + 127，但陣列中的值範圍從0到255。</span><span class="sxs-lookup"><span data-stu-id="23b8a-132">Note that the values of the power are measured from -128 to +127 but the values in the array range from 0 to 255.</span></span> <span data-ttu-id="23b8a-133">如果您有單聲道 wave，則只有第一個維度會有有效的值。</span><span class="sxs-lookup"><span data-stu-id="23b8a-133">If you have a monophonic wave, only the first dimension will have valid values.</span></span>

<span data-ttu-id="23b8a-134">如果信號為非身歷聲，則第二個數組將包含 mono 信號的複本。</span><span class="sxs-lookup"><span data-stu-id="23b8a-134">If the signal is non-stereo, then the second array will contain a copy of the mono signal.</span></span> <span data-ttu-id="23b8a-135">也就是說，波形 \[ 0 \] \[ *n* \] 和波形 \[ 1 \] \[ *n* \] 將包含相同的資料，其中 *n* 是特定資料格的索引。</span><span class="sxs-lookup"><span data-stu-id="23b8a-135">That is, waveform\[0\]\[*n*\] and waveform\[1\]\[*n*\] will contain the same data, where *n* is the index into a particular cell.</span></span>

## <a name="state"></a><span data-ttu-id="23b8a-136">狀態</span><span class="sxs-lookup"><span data-stu-id="23b8a-136">State</span></span>

<span data-ttu-id="23b8a-137">狀態變數會反映 Windows Media Player 的音訊播放狀態。</span><span class="sxs-lookup"><span data-stu-id="23b8a-137">The state variable reflects the audio playback state of Windows Media Player.</span></span> <span data-ttu-id="23b8a-138">PlayerState 列舉值為</span><span class="sxs-lookup"><span data-stu-id="23b8a-138">The PlayerState enumeration values are</span></span>


```C++
    stop_state              = 0,    // audio is currently stopped
    pause_state             = 1,    // audio is currently paused
    play_state              = 2     // audio is currently playing

```



<span data-ttu-id="23b8a-139">您可以使用此變數來採取不同的動作，視音訊播放狀態而定。</span><span class="sxs-lookup"><span data-stu-id="23b8a-139">You can use this variable to take different actions depending on the audio playback state.</span></span> <span data-ttu-id="23b8a-140">例如，您可以在播放音訊時播放一種視覺效果，並在停止時播放另一種視覺效果。</span><span class="sxs-lookup"><span data-stu-id="23b8a-140">For example, you can play one kind of visualization when the audio is playing and another when it is stopped.</span></span>

## <a name="time-stamp"></a><span data-ttu-id="23b8a-141">時間戳記</span><span class="sxs-lookup"><span data-stu-id="23b8a-141">Time Stamp</span></span>

<span data-ttu-id="23b8a-142">時間戳記變數會反映拍攝快照集的目前時間。</span><span class="sxs-lookup"><span data-stu-id="23b8a-142">The timeStamp variable reflects the current time when the snapshot is taken.</span></span> <span data-ttu-id="23b8a-143">這可以用來測量拍攝快照集的頻率。</span><span class="sxs-lookup"><span data-stu-id="23b8a-143">This can be used to measure how frequently the snapshots are taken.</span></span>

<span data-ttu-id="23b8a-144">您可以使用此變數來時間動畫。</span><span class="sxs-lookup"><span data-stu-id="23b8a-144">You can use this variable to time your animations.</span></span> <span data-ttu-id="23b8a-145">如果快照集太頻繁，您可以正常地降低影像，使其以您選擇的方式顯示。</span><span class="sxs-lookup"><span data-stu-id="23b8a-145">If the snapshots are too frequent, you can gracefully degrade your image to display in the manner you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23b8a-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="23b8a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23b8a-147">**執行轉譯**</span><span class="sxs-lookup"><span data-stu-id="23b8a-147">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




