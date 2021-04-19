---
title: 浮水印支援
description: 浮水印支援
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- Windows Media 格式 SDK，浮水印支援
- Windows Media Format SDK，數位浮水印
- Advanced Systems Format (ASF) 、浮水印支援
- ASF (Advanced Systems Format) 、浮水印支援
- Advanced Systems Format (ASF) 、數位浮水印
- ASF (Advanced Systems Format) 、數位浮水印
- Windows Media Format SDK、SQL-DMO
- Advanced Systems Format (ASF) ，SQL-DMO
- ASF (Advanced Systems Format) ，SQL-DMO
- Windows Media Format SDK，IWMWatermarkInfo 介面
- Advanced Systems Format (ASF) ，IWMWatermarkInfo 介面
- ASF (Advanced Systems Format) ，IWMWatermarkInfo 介面
- 浮水印，關於
- 數位浮水印
- DirectX 媒體物件 (的) ，關於
- SQL-DMO (DirectX 媒體物件) ，關於
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106995147"
---
# <a name="watermarking-support"></a><span data-ttu-id="11219-120">浮水印支援</span><span class="sxs-lookup"><span data-stu-id="11219-120">Watermarking Support</span></span>

<span data-ttu-id="11219-121">數位浮水印是在媒體資料流程的資料中內嵌著作權或其他資訊的一種方式。</span><span class="sxs-lookup"><span data-stu-id="11219-121">Digital watermarking is a way to embed copyright or other information in the data of a media stream.</span></span> <span data-ttu-id="11219-122">浮水印的技巧在不同的解決方案之間有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="11219-122">Techniques for watermarking vary widely from one solution to the next.</span></span> <span data-ttu-id="11219-123">浮水印最簡單的形式就是將識別影像新增至影片串流的每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="11219-123">The simplest form of watermarking is simply adding an identifying image to each frame of a video stream.</span></span> <span data-ttu-id="11219-124">電視電臺通常會使用這項技術，在其廣播的右下角插入半透明的標誌。</span><span class="sxs-lookup"><span data-stu-id="11219-124">Television stations frequently use this technique to insert a semi-transparent logo in a bottom corner of their broadcast.</span></span> <span data-ttu-id="11219-125">更複雜的數位浮水印形式 imperceptible 給使用者觀賞或聆聽內容。</span><span class="sxs-lookup"><span data-stu-id="11219-125">More sophisticated forms of digital watermarking are imperceptible to the user watching or listening to the content.</span></span>

<span data-ttu-id="11219-126">Windows Media Format SDK 支援使用數位浮水印 [*DMOs*](wmformat-glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="11219-126">The Windows Media Format SDK supports the use of digital watermarking [*DMOs*](wmformat-glossary.md).</span></span> <span data-ttu-id="11219-127">在實務上，浮水印系統非常類似于編解碼器：它會取得媒體範例、對資料執行演算法，以及輸出已改變的範例。</span><span class="sxs-lookup"><span data-stu-id="11219-127">In practice, a watermarking system is very similar to a codec: it takes media samples, runs algorithms on the data, and outputs the altered samples.</span></span> <span data-ttu-id="11219-128">當針對資料流程指定浮水印系統時，寫入器物件會在其處理輸入樣本時包含該物件。</span><span class="sxs-lookup"><span data-stu-id="11219-128">When a watermarking system is specified for a stream, the writer object includes the DMO in its processing of input samples.</span></span>

<span data-ttu-id="11219-129">當您設定浮水印的串流時，必須指定浮水印設定資訊。</span><span class="sxs-lookup"><span data-stu-id="11219-129">You must specify watermark configuration information when you configure a stream for watermarking.</span></span> <span data-ttu-id="11219-130">設定值會隨著浮水印的是不同而不同。</span><span class="sxs-lookup"><span data-stu-id="11219-130">The configuration values will be different depending upon the watermarking DMO.</span></span> <span data-ttu-id="11219-131">您所使用的 SQL-DMO 應該會有描述其所支援之設定值的指示。</span><span class="sxs-lookup"><span data-stu-id="11219-131">The DMO you use should come with instructions describing the configuration values it supports.</span></span>

<span data-ttu-id="11219-132">如需用來指定浮水印系統之設定的相關資訊，請參閱 [ **IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span><span class="sxs-lookup"><span data-stu-id="11219-132">For information about the settings used to specify a watermarking system, see [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span></span>

<span data-ttu-id="11219-133">您可以對應用程式進行程式設計，以列舉用戶端電腦上所安裝的浮水印 DMOs。</span><span class="sxs-lookup"><span data-stu-id="11219-133">You can program your application to enumerate the watermarking DMOs installed on the client computer.</span></span> <span data-ttu-id="11219-134">如需詳細資訊，請參閱 [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) 介面。</span><span class="sxs-lookup"><span data-stu-id="11219-134">For more information, see the [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11219-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="11219-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11219-136">**檔案寫入功能**</span><span class="sxs-lookup"><span data-stu-id="11219-136">**File Writing Features**</span></span>](file-writing-features.md)
</dt> </dl>

 

 




