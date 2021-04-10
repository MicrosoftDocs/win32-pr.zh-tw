---
title: 輸入設定
description: 輸入設定
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows Media Format SDK，全域常數
- Advanced Systems Format (ASF) 、global 常數
- ASF (Advanced Systems Format) ，global 常數
- 全域常數，清單
- Windows Media Format SDK，常數
- Advanced Systems Format (ASF) ，常數
- ASF (Advanced Systems Format) ，常數
- 常數，清單
- Windows Media Format SDK，輸入設定
- Advanced Systems Format (ASF) ，輸入設定
- ASF (Advanced Systems Format) ，輸入設定
- 輸入設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023009"
---
# <a name="input-settings"></a><span data-ttu-id="34c6a-115">輸入設定</span><span class="sxs-lookup"><span data-stu-id="34c6a-115">Input Settings</span></span>

<span data-ttu-id="34c6a-116">下列全域常數用來識別寫入器的輸入設定。</span><span class="sxs-lookup"><span data-stu-id="34c6a-116">The following global constants are used to identify input settings for the writer.</span></span>



| <span data-ttu-id="34c6a-117">全域常數</span><span class="sxs-lookup"><span data-stu-id="34c6a-117">Global constant</span></span>                        | <span data-ttu-id="34c6a-118">WMT \_ ATTR \_ 資料類型</span><span class="sxs-lookup"><span data-stu-id="34c6a-118">WMT\_ATTR\_DATATYPE</span></span>                                                                                                                       | <span data-ttu-id="34c6a-119">*PValue* 的描述</span><span class="sxs-lookup"><span data-stu-id="34c6a-119">Description of *pValue*</span></span>                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34c6a-120">g \_ wszDeinterlaceMode</span><span class="sxs-lookup"><span data-stu-id="34c6a-120">g\_wszDeinterlaceMode</span></span>                  | <span data-ttu-id="34c6a-121">**WMT \_在 \_** 主題中，將 [DWORD] 類型設定為 [模式] 資料表中的其中一個值 [，以將影片進行逐行掃描](to-deinterlace-video.md)。</span><span class="sxs-lookup"><span data-stu-id="34c6a-121">**WMT\_TYPE\_DWORD** set to one of the values in the mode table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span>            | <span data-ttu-id="34c6a-122">設定時，指定輸入的交錯內容類型。</span><span class="sxs-lookup"><span data-stu-id="34c6a-122">When set, specifies the type of interlaced content of the input.</span></span> <span data-ttu-id="34c6a-123">如需詳細資訊，請參閱 [將影片進行逐行掃描](to-deinterlace-video.md)。</span><span class="sxs-lookup"><span data-stu-id="34c6a-123">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>                                                                                                                            |
| <span data-ttu-id="34c6a-124">g \_ wszFixedFrameRate</span><span class="sxs-lookup"><span data-stu-id="34c6a-124">g\_wszFixedFrameRate</span></span>                   | <span data-ttu-id="34c6a-125">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="34c6a-125">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="34c6a-126">當設為 True 時，會指示編解碼器不要在編碼期間卸載任何框架。</span><span class="sxs-lookup"><span data-stu-id="34c6a-126">When set to True, instructs the codec not to drop any frames during encoding.</span></span> <span data-ttu-id="34c6a-127">這會導致輸出影片資料流程的 [*畫面播放速率*](wmformat-glossary.md) 是常數。</span><span class="sxs-lookup"><span data-stu-id="34c6a-127">This will cause the [*frame rate*](wmformat-glossary.md) of the output video stream to be constant.</span></span> <span data-ttu-id="34c6a-128">輸入資料流程的畫面播放速率不需要是常數。</span><span class="sxs-lookup"><span data-stu-id="34c6a-128">The frame rate of the input stream does not need to be constant.</span></span> |
| <span data-ttu-id="34c6a-129">g \_ wszInitialPatternForInverseTelecine</span><span class="sxs-lookup"><span data-stu-id="34c6a-129">g\_wszInitialPatternForInverseTelecine</span></span> | <span data-ttu-id="34c6a-130">**WMT \_在 \_** 主題中，將 [DWORD] 類型設定為 [初始模式] 資料表中的其中一個值 [，以將影片進行逐行掃描](to-deinterlace-video.md)。</span><span class="sxs-lookup"><span data-stu-id="34c6a-130">**WMT\_TYPE\_DWORD** set to one of the values in the initial pattern table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span> | <span data-ttu-id="34c6a-131">當 [交錯模式] 設定為 [WM \_ DM \_ 交錯] INVERSETELECINE 時，您 \_ 可以將此設定為指定 [*電影*](wmformat-glossary.md) 輸入的模式。</span><span class="sxs-lookup"><span data-stu-id="34c6a-131">When the deinterlace mode is set to WM\_DM\_DEINTERLACE\_INVERSETELECINE, this can be set to specify the pattern of the [*telecine*](wmformat-glossary.md) input.</span></span> <span data-ttu-id="34c6a-132">如需詳細資訊，請參閱 [將影片進行逐行掃描](to-deinterlace-video.md)。</span><span class="sxs-lookup"><span data-stu-id="34c6a-132">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>        |
| <span data-ttu-id="34c6a-133">g \_ wszInterlacedCoding</span><span class="sxs-lookup"><span data-stu-id="34c6a-133">g\_wszInterlacedCoding</span></span>                 | <span data-ttu-id="34c6a-134">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="34c6a-134">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="34c6a-135">設定為 True 時，會指定編解碼器應該將資料流程編碼為交錯式內容。</span><span class="sxs-lookup"><span data-stu-id="34c6a-135">When set to True, specifies that that the codec should encode the stream as interlaced content.</span></span> <span data-ttu-id="34c6a-136">如需詳細資訊，請參閱 [使用交錯式影片](to-use-interlaced-video.md)。</span><span class="sxs-lookup"><span data-stu-id="34c6a-136">For more information, see [To Use Interlaced Video](to-use-interlaced-video.md).</span></span>                                                                                       |
| <span data-ttu-id="34c6a-137">g \_ wszJPEGCompressionQuality</span><span class="sxs-lookup"><span data-stu-id="34c6a-137">g\_wszJPEGCompressionQuality</span></span>           | <span data-ttu-id="34c6a-138">**WMT \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="34c6a-138">**WMT\_TYPE\_DWORD**</span></span>                                                                                                                      | <span data-ttu-id="34c6a-139">指定要用於輸入的 JPEG 品質層級 (從1到 100) 。</span><span class="sxs-lookup"><span data-stu-id="34c6a-139">Specifies the JPEG quality level (from 1 to 100) to be used on the input.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="34c6a-140">g \_ wszWatermarkCLSID</span><span class="sxs-lookup"><span data-stu-id="34c6a-140">g\_wszWatermarkCLSID</span></span>                   | <span data-ttu-id="34c6a-141">**WMT \_ 類型 \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="34c6a-141">**WMT\_TYPE\_GUID**</span></span>                                                                                                                       | <span data-ttu-id="34c6a-142">值設定為浮水印 GUID。</span><span class="sxs-lookup"><span data-stu-id="34c6a-142">The value is set to the watermark GUID.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="34c6a-143">g \_ wszWatermarkConfig</span><span class="sxs-lookup"><span data-stu-id="34c6a-143">g\_wszWatermarkConfig</span></span>                  | <span data-ttu-id="34c6a-144">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="34c6a-144">**WMT\_TYPE\_STRING**</span></span>                                                                                                                     | <span data-ttu-id="34c6a-145">值設定為水位線設定。</span><span class="sxs-lookup"><span data-stu-id="34c6a-145">The value is set to the watermark configuration.</span></span> <span data-ttu-id="34c6a-146">此值會視浮水印的值而異。</span><span class="sxs-lookup"><span data-stu-id="34c6a-146">This value will vary depending upon the watermarking DMO.</span></span> <span data-ttu-id="34c6a-147">如需詳細資訊，請參閱浮水印系統的檔。</span><span class="sxs-lookup"><span data-stu-id="34c6a-147">Consult the documentation of the watermarking system for more information.</span></span>                                                                                   |



 

> [!Note]  
> <span data-ttu-id="34c6a-148">針對資料流程設定的輸入設定不會保存在寫入的檔案中。</span><span class="sxs-lookup"><span data-stu-id="34c6a-148">The input settings configured for a stream are not persisted in the written file.</span></span> <span data-ttu-id="34c6a-149">如果您想要讓自訂讀取器擁有這些編碼參數的存取權，您必須建立自訂屬性，以將它們儲存在檔案標頭中。</span><span class="sxs-lookup"><span data-stu-id="34c6a-149">If you want your custom reader to have access to these encoding parameters, you must create custom attributes to store them in the file header.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="34c6a-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="34c6a-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34c6a-151">**IWMWriterAdvanced2::GetInputSetting**</span><span class="sxs-lookup"><span data-stu-id="34c6a-151">**IWMWriterAdvanced2::GetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[<span data-ttu-id="34c6a-152">**IWMWriterAdvanced2::SetInputSetting**</span><span class="sxs-lookup"><span data-stu-id="34c6a-152">**IWMWriterAdvanced2::SetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




