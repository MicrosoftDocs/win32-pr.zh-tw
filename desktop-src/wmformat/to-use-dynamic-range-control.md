---
title: 若要使用動態範圍控制項
description: 若要使用動態範圍控制項
ms.assetid: 719658c1-952f-4e8f-a3ea-bdf89a0a7268
keywords:
- Windows Media Format SDK，動態範圍控制項
- Windows Media Format SDK，Windows Media 音訊 9 Professional 編解碼器
- Windows Media 格式 SDK，Windows Media 音訊9無失真編解碼器
- Advanced Systems Format (ASF) 、Windows Media 音訊 9 Professional 編解碼器
- ASF (Advanced Systems Format) 、Windows Media 音訊 9 Professional 編解碼器
- Advanced Systems Format (ASF) 、Windows Media 音訊9無失真編解碼器
- ASF (Advanced Systems Format) ，Windows Media 音訊9無失真編解碼器
- Advanced Systems Format (ASF) 、動態範圍控制
- ASF (Advanced 系統格式) 、動態範圍控制
- 動態範圍控制項
- 編解碼器，Windows Media 音訊9無失真編解碼器
- 編解碼器，Windows Media 音訊 9 Professional 編解碼器
- Windows Media 音訊9無失真編解碼器，動態範圍控制
- Windows Media 音訊 9 Professional 編解碼器，動態範圍控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077ebc0052d0154aec395f371a5c2dc3ffd46c67
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965414"
---
# <a name="to-use-dynamic-range-control"></a><span data-ttu-id="bdc61-117">若要使用動態範圍控制項</span><span class="sxs-lookup"><span data-stu-id="bdc61-117">To Use Dynamic Range Control</span></span>

<span data-ttu-id="bdc61-118">一段音訊內容的動態範圍基本上是最低磁片區與最大磁片區之間的差異。</span><span class="sxs-lookup"><span data-stu-id="bdc61-118">The dynamic range of a piece of audio content is basically the difference between the lowest volume and the maximum volume.</span></span> <span data-ttu-id="bdc61-119">如果內容的動態範圍太高，使用者可能會在播放期間重複調整音量。</span><span class="sxs-lookup"><span data-stu-id="bdc61-119">If the dynamic range of the content is too high, users may find themselves adjusting the volume repeatedly during playback.</span></span> <span data-ttu-id="bdc61-120">例如，電影通常會有很高的動態範圍。</span><span class="sxs-lookup"><span data-stu-id="bdc61-120">For example, movies frequently have a high dynamic range.</span></span> <span data-ttu-id="bdc61-121">通常，當調整磁片區，以便在無訊息的場景期間瞭解對話時，電影的其他部分會有音樂或音效效果，而不是所需的部分。</span><span class="sxs-lookup"><span data-stu-id="bdc61-121">Often, when the volume is adjusted so that dialog can be understood during quiet scenes, other parts of the movie with music or sound effects are louder than desired.</span></span>

<span data-ttu-id="bdc61-122">Windows Media 音訊 9 Professional 和 Windows Media 音訊9無失真編解碼器支援稱為動態範圍控制的功能。</span><span class="sxs-lookup"><span data-stu-id="bdc61-122">The Windows Media Audio 9 Professional and Windows Media Audio 9 Lossless codecs support a feature called dynamic range control.</span></span> <span data-ttu-id="bdc61-123">編碼時，編解碼器會計算內容中的尖峰和平均波幅值，而寫入器物件會在編碼完成時，將這些值儲存在資料流程的中繼資料中。</span><span class="sxs-lookup"><span data-stu-id="bdc61-123">At encode time, the codec calculates the peak and average amplitude values in the content, and the writer object stores these values in the metadata for the stream when encoding is finished.</span></span> <span data-ttu-id="bdc61-124">或者，應用程式也可以撰寫「目標」值做為中繼資料，讓播放機應用程式和解碼器在播放檔案時可以用來做為提示。</span><span class="sxs-lookup"><span data-stu-id="bdc61-124">Optionally, an application can also write "target" values as metadata that player applications and the decoder can use as hints when playing back the file.</span></span> <span data-ttu-id="bdc61-125">在播放期間，應用程式可以指定要套用到音訊資料流程的動態範圍控制層級。</span><span class="sxs-lookup"><span data-stu-id="bdc61-125">At playback time, an application can specify the level of dynamic range control to apply to the audio stream.</span></span>

<span data-ttu-id="bdc61-126">Windows Media Player 將動態範圍控制項實作為無訊息模式功能。</span><span class="sxs-lookup"><span data-stu-id="bdc61-126">Windows Media Player implements dynamic range control as the Quiet Mode feature.</span></span>

## <a name="when-to-use-dynamic-range-control"></a><span data-ttu-id="bdc61-127">使用動態範圍控制的時機</span><span class="sxs-lookup"><span data-stu-id="bdc61-127">When to Use Dynamic Range Control</span></span>

<span data-ttu-id="bdc61-128">動態範圍控制項可以改變內容的音效。</span><span class="sxs-lookup"><span data-stu-id="bdc61-128">Dynamic range control can alter the sound of the content.</span></span> <span data-ttu-id="bdc61-129">基於這個理由，您不應該將應用程式設定為自動使用動態範圍控制。</span><span class="sxs-lookup"><span data-stu-id="bdc61-129">For that reason, you should not configure your application to use dynamic range control automatically.</span></span> <span data-ttu-id="bdc61-130">相反地，請提供使用者視需要開啟或關閉動態範圍控制的能力。</span><span class="sxs-lookup"><span data-stu-id="bdc61-130">Instead, provide users with the ability to turn dynamic range control on or off as needed.</span></span>

## <a name="using-dynamic-range-control"></a><span data-ttu-id="bdc61-131">使用動態範圍控制項</span><span class="sxs-lookup"><span data-stu-id="bdc61-131">Using Dynamic Range Control</span></span>

<span data-ttu-id="bdc61-132">在播放時，會使用輸出設定 g wszDynamicRangeControl 來啟用動態範圍控制項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bdc61-132">At playback time, dynamic range control is activated using the output setting g\_wszDynamicRangeControl.</span></span> <span data-ttu-id="bdc61-133">使用 [**IWMReaderAdvanced2：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) 來設定設定。</span><span class="sxs-lookup"><span data-stu-id="bdc61-133">Use [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) to configure the setting.</span></span> <span data-ttu-id="bdc61-134">值為零 (預設) 表示不應更改動態範圍。</span><span class="sxs-lookup"><span data-stu-id="bdc61-134">A value of zero (the default) indicates that the dynamic range should not be altered.</span></span> <span data-ttu-id="bdc61-135">1或2的值表示要執行動態範圍控制的編解碼器，其中1是動態範圍壓縮的中等層級，而2則是高層級的動態範圍壓縮。</span><span class="sxs-lookup"><span data-stu-id="bdc61-135">A value of 1 or 2 signals the codec to perform dynamic range control, where 1 is a moderate level of dynamic range compression, and 2 is a high level of dynamic range compression.</span></span>

<span data-ttu-id="bdc61-136">在編碼時間或播放時間，您可以分別設定 [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md) 和 [**wm/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md) 屬性，為尖峰和平均層級提供編解碼器目標 PCM 值。</span><span class="sxs-lookup"><span data-stu-id="bdc61-136">At encoding time or playback time, you can give the codec target PCM values for the peak and average levels by setting the [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md) and [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md) attributes, respectively.</span></span> <span data-ttu-id="bdc61-137">這些值會儲存為中繼資料屬性，而且應該使用 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) 介面的方法來存取。</span><span class="sxs-lookup"><span data-stu-id="bdc61-137">These values are stored as metadata attributes and should be accessed using the methods of the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface.</span></span> <span data-ttu-id="bdc61-138">當您使用 professional 或無失真編解碼器編碼音訊串流時，會自動將 [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md) 和 [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md) 屬性設定為原始內容的尖峰和平均層級。</span><span class="sxs-lookup"><span data-stu-id="bdc61-138">When you encode an audio stream using the professional or lossless codec, the [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md) and [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md) attributes are set automatically to the peak and average levels of the original content.</span></span> <span data-ttu-id="bdc61-139">根據預設，目標值會設定為與參考相同的值。</span><span class="sxs-lookup"><span data-stu-id="bdc61-139">The target values are set to the same values as the references by default.</span></span>

<span data-ttu-id="bdc61-140">在播放時，解碼器會根據選取的動態範圍控制項層級以及目標值 (（如果有指定) ）來計算動態範圍。</span><span class="sxs-lookup"><span data-stu-id="bdc61-140">The decoder at playback time calculates the dynamic range based on the selected level of dynamic range control and the target values (if any are specified).</span></span> <span data-ttu-id="bdc61-141">下表顯示可能的範圍。</span><span class="sxs-lookup"><span data-stu-id="bdc61-141">The possible ranges are shown in the following table.</span></span>



| <span data-ttu-id="bdc61-142">設定</span><span class="sxs-lookup"><span data-stu-id="bdc61-142">Settings</span></span>                                                                | <span data-ttu-id="bdc61-143">傳遞的音訊範圍</span><span class="sxs-lookup"><span data-stu-id="bdc61-143">Range of delivered audio</span></span>                                                                                                     |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc61-144">g \_ wszDynamicRangeControl = 0 (任何目標值) </span><span class="sxs-lookup"><span data-stu-id="bdc61-144">g\_wszDynamicRangeControl = 0 (Any target values)</span></span>                       | <span data-ttu-id="bdc61-145">與原始內容相同的範圍。</span><span class="sxs-lookup"><span data-stu-id="bdc61-145">Same range as the original content.</span></span>                                                                                          |
| <span data-ttu-id="bdc61-146">g \_ wszDynamicRangeControl = 1 (目標值等於參考值) </span><span class="sxs-lookup"><span data-stu-id="bdc61-146">g\_wszDynamicRangeControl = 1 (Target values equal to reference values)</span></span> | <span data-ttu-id="bdc61-147">平均層級會維持不變，且尖峰限制為平均 + 12 資料庫。</span><span class="sxs-lookup"><span data-stu-id="bdc61-147">Average level is maintained and peaks are confined to the average +12 dB.</span></span>                                                    |
| <span data-ttu-id="bdc61-148">g \_ wszDynamicRangeControl = 2 (目標值等於參考值) </span><span class="sxs-lookup"><span data-stu-id="bdc61-148">g\_wszDynamicRangeControl = 2 (Target values equal to reference values)</span></span> | <span data-ttu-id="bdc61-149">平均層級會維持不變，且尖峰限制為平均 + 6 資料庫。</span><span class="sxs-lookup"><span data-stu-id="bdc61-149">Average level is maintained and peaks are confined to the average +6 dB.</span></span>                                                     |
| <span data-ttu-id="bdc61-150">g \_ wszDynamicRangeControl = 1 (指定的目標值) </span><span class="sxs-lookup"><span data-stu-id="bdc61-150">g\_wszDynamicRangeControl = 1 (Target values specified)</span></span>                 | <span data-ttu-id="bdc61-151">平均層級設定為目標平均值，且尖峰限制為目標尖峰值。</span><span class="sxs-lookup"><span data-stu-id="bdc61-151">Average level set to the target average value and peaks confined to the target peak value.</span></span>                                   |
| <span data-ttu-id="bdc61-152">g \_ wszDynamicRangeControl = 2 (指定的目標值) </span><span class="sxs-lookup"><span data-stu-id="bdc61-152">g\_wszDynamicRangeControl = 2 (Target values specified)</span></span>                 | <span data-ttu-id="bdc61-153">平均層級設定為目標平均值，尖峰限制為目標平均和目標尖峰值的中位數。</span><span class="sxs-lookup"><span data-stu-id="bdc61-153">Average level set to the target average value and peaks confined to the median of the target average and target peak values.</span></span> |



 

<span data-ttu-id="bdc61-154">請注意，動態範圍控制項是僅解碼的功能，而且只存在於檔案本身的中繼資料中。</span><span class="sxs-lookup"><span data-stu-id="bdc61-154">Note that dynamic range control is a feature of decoding only and exists only as metadata in the file itself.</span></span> <span data-ttu-id="bdc61-155">這些設定不會影響儲存在檔案中的內容，除非您特別指示解碼器使用它們。</span><span class="sxs-lookup"><span data-stu-id="bdc61-155">These settings have no effect on the content stored in the file unless you specifically instruct the decoder to use them.</span></span> <span data-ttu-id="bdc61-156">Windows Media Format SDK 不提供任何方法，可在編碼時間修改音訊資料的動態範圍。</span><span class="sxs-lookup"><span data-stu-id="bdc61-156">The Windows Media Format SDK provides no methods for modifying the dynamic range of the audio data at encoding time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdc61-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="bdc61-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc61-158">**Advanced 主題**</span><span class="sxs-lookup"><span data-stu-id="bdc61-158">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 




