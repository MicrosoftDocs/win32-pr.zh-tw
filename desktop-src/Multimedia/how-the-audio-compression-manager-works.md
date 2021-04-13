---
title: 音訊壓縮管理員的運作方式
description: 音訊壓縮管理員的運作方式
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- '多媒體音訊、音訊壓縮管理員 (的) '
- '音訊、音訊壓縮管理員 (的) '
- 音訊壓縮管理員 (的) ，關於
- " (音效壓縮管理員) ，關於"
- 音訊壓縮管理員 (的) 、編解碼器驅動程式
- " (的音訊壓縮管理員) 、編解碼器驅動程式"
- 音訊壓縮管理員 (的) 、格式轉換器驅動程式
- " (音效壓縮管理員) 、格式化轉換器驅動程式"
- 音訊壓縮管理員 (的) 、篩選器驅動程式
- " (音效壓縮管理員) 、篩選器驅動程式"
- 音訊壓縮管理員 (的) 、壓縮程式驅動程式
- " (音效壓縮管理員) 、壓縮程式驅動程式"
- 音訊壓縮管理員 (的) 、解壓縮程式驅動程式
- " (音效壓縮管理員) 的解壓縮程式驅動程式"
- 編解碼器驅動程式
- 格式化轉換器驅動程式
- 篩選器驅動程式
- 壓縮程式驅動程式
- 解壓縮程式驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b861d381dfc28307c090dbb71b93db8e58e90a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301179"
---
# <a name="how-the-audio-compression-manager-works"></a><span data-ttu-id="e196f-122">音訊壓縮管理員的運作方式</span><span class="sxs-lookup"><span data-stu-id="e196f-122">How the Audio Compression Manager Works</span></span>

<span data-ttu-id="e196f-123">使用現有的驅動程式介面勾點來覆寫波形音訊裝置的預設對應演算法。</span><span class="sxs-lookup"><span data-stu-id="e196f-123">The ACM uses existing driver interface hooks to override the default mapping algorithm for waveform-audio devices.</span></span> <span data-ttu-id="e196f-124">這可讓進行中的要求攔截裝置開啟的呼叫。</span><span class="sxs-lookup"><span data-stu-id="e196f-124">This allows the ACM to intercept device-open calls.</span></span> <span data-ttu-id="e196f-125">在攔截呼叫之後，執行程式可執行各種不同的工作來處理音訊資料，例如將外部壓縮程式或解壓縮程式插入序列中。</span><span class="sxs-lookup"><span data-stu-id="e196f-125">After a call has been intercepted, the ACM can perform a variety of tasks to process the audio data, such as inserting an external compressor or decompressor into the sequence.</span></span>

<span data-ttu-id="e196f-126">這類的驅動程式會管理下列類型的驅動程式：</span><span class="sxs-lookup"><span data-stu-id="e196f-126">The ACM manages the following types of drivers:</span></span>

-   <span data-ttu-id="e196f-127"> (編解碼器) 驅動程式的壓縮程式和解壓縮程式</span><span class="sxs-lookup"><span data-stu-id="e196f-127">Compressor and decompressor (codec) drivers</span></span>
-   <span data-ttu-id="e196f-128">格式化轉換器驅動程式</span><span class="sxs-lookup"><span data-stu-id="e196f-128">Format converter drivers</span></span>
-   <span data-ttu-id="e196f-129">篩選器驅動程式</span><span class="sxs-lookup"><span data-stu-id="e196f-129">Filter drivers</span></span>

<span data-ttu-id="e196f-130">壓縮機和 decompressors 會將一種格式類型變更為另一種格式。</span><span class="sxs-lookup"><span data-stu-id="e196f-130">Compressors and decompressors change one format type to another.</span></span> <span data-ttu-id="e196f-131">例如，「壓縮程式」或「解壓縮程式」可以將 PCM (脈衝程式碼調製) 檔變更為 ADPCM (彈性差異脈衝程式碼調製) 檔。</span><span class="sxs-lookup"><span data-stu-id="e196f-131">For example, a compressor or decompressor can change a PCM (Pulse Code Modulation) file to an ADPCM (Adaptive Differential Pulse Code Modulation) file.</span></span> <span data-ttu-id="e196f-132">格式轉換器會變更格式，但不會變更資料類型。</span><span class="sxs-lookup"><span data-stu-id="e196f-132">Format converters change the format, but not the data type.</span></span> <span data-ttu-id="e196f-133">例如，轉換器可以將 44-kHz、16位資料變更為 44-kHz、8位的資料。</span><span class="sxs-lookup"><span data-stu-id="e196f-133">For example, a converter can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span> <span data-ttu-id="e196f-134">篩選器完全不會變更資料格式，但會以某種方式變更波形音訊資料。</span><span class="sxs-lookup"><span data-stu-id="e196f-134">Filters do not change the data format at all, but they change the waveform-audio data in some manner.</span></span> <span data-ttu-id="e196f-135">例如，篩選可以結合資料流程和本身的 echo。</span><span class="sxs-lookup"><span data-stu-id="e196f-135">For example, a filter could combine a data stream and an echo of itself.</span></span> <span data-ttu-id="e196f-136">在驅動程式中，單一的 [的] 或 [篩選標記] 或 [格式] 標記，也可能支援上述類型的組合。</span><span class="sxs-lookup"><span data-stu-id="e196f-136">A single ACM driver, or a filter tag or format tag within a driver, might also support combinations of the preceding types.</span></span>

<span data-ttu-id="e196f-137">針對波形音訊輸出，當器抵達時，會將資料的每個緩衝區傳遞給轉換器。</span><span class="sxs-lookup"><span data-stu-id="e196f-137">For waveform-audio output, the ACM passes each buffer of data to the converter as it arrives.</span></span> <span data-ttu-id="e196f-138">轉換器會將資料解壓縮，並將解壓縮的資料傳回至「影子」緩衝區中的 [資料]。</span><span class="sxs-lookup"><span data-stu-id="e196f-138">The converter decompresses the data and returns the decompressed data to the ACM in a "shadow" buffer.</span></span> <span data-ttu-id="e196f-139">然後，會將解壓縮的陰影緩衝區傳遞給波形音訊驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e196f-139">The ACM then passes the decompressed shadow buffer to the waveform-audio driver.</span></span> <span data-ttu-id="e196f-140">當配置每次收到準備訊息時，都會配置陰影緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e196f-140">The ACM allocates the shadow buffers whenever it receives a prepare message.</span></span>

<span data-ttu-id="e196f-141">若為波形音訊輸入，則會將空的陰影緩衝區傳遞給驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e196f-141">For waveform-audio input, the ACM passes empty shadow buffers to the driver.</span></span> <span data-ttu-id="e196f-142">它會使用背景工作在驅動程式填滿陰影緩衝區之後收到通知。</span><span class="sxs-lookup"><span data-stu-id="e196f-142">It uses a background task to receive a notification after the driver has filled the shadow buffer.</span></span> <span data-ttu-id="e196f-143">然後，將緩衝區傳遞至驅動程式進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="e196f-143">The ACM then passes the buffers to the driver for compression.</span></span> <span data-ttu-id="e196f-144">壓縮完成之後，驅動程式會將資料傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="e196f-144">After compression is finished, the driver passes the data to the application.</span></span>

 

 




