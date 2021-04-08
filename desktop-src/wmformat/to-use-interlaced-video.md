---
title: 使用交錯式影片
description: 使用交錯式影片
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- Windows Media Format SDK，交錯式影片
- Windows Media Format SDK、影片編碼交錯式
- Windows Media Format SDK，編碼交錯式影片
- Windows Media Format SDK，解碼交錯式影片
- Windows Media Format SDK，欄位順序
- Advanced Systems Format (ASF) 、交錯式影片
- ASF (Advanced Systems Format) 、交錯式影片
- Advanced Systems Format (ASF) 、影片編碼交錯式
- ASF (Advanced Systems Format) 、影片編碼交錯式
- Advanced Systems Format (ASF) 、編碼交錯式影片
- ASF (Advanced Systems Format) 、編碼交錯式影片
- Advanced Systems Format (ASF) ，解碼交錯式影片
- ASF (Advanced Systems Format) ，解碼交錯式影片
- Advanced Systems Format (ASF) ，欄位順序
- ASF (Advanced Systems Format) ，欄位順序
- 交錯式影片，關於
- 交錯式影片，編碼
- 交錯式影片，解碼
- 交錯式影片，欄位順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841900"
---
# <a name="to-use-interlaced-video"></a><span data-ttu-id="b7e9d-122">使用交錯式影片</span><span class="sxs-lookup"><span data-stu-id="b7e9d-122">To Use Interlaced Video</span></span>

<span data-ttu-id="b7e9d-123">有兩種基本類型的影片編碼：漸進式和交錯式。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-123">There are two basic types of video encoding: progressive and interlaced.</span></span> <span data-ttu-id="b7e9d-124">在漸進式編碼中，每個畫面格都是一段影片的編碼標記法。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-124">In progressive encoding, each frame is an encoded representation of one frame of video.</span></span> <span data-ttu-id="b7e9d-125">在交錯編碼中，每個畫面格都是一種編碼的標記法，表示影片中的所有資料列或所有奇數資料列。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-125">In interlaced encoding, each frame is an encoded representation of either all of the even rows of pixels in the video, or all of the odd rows.</span></span> <span data-ttu-id="b7e9d-126">每個交錯框架稱為 *欄位*，因此有奇數位段甚至是欄位。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-126">Each interlaced frame is called a *field*, so there are odd fields and even fields.</span></span> <span data-ttu-id="b7e9d-127">交錯顯示 (像是電視) 會一次轉譯一個欄位，也就是替代欄位。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-127">An interlaced display (like a television) renders the fields one at a time, alternating fields.</span></span> <span data-ttu-id="b7e9d-128">漸進式顯示器會一次呈現全部的畫面格。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-128">A progressive display renders frames all at once.</span></span>

<span data-ttu-id="b7e9d-129">Windows Media 視訊 9 Advanced Profile 編解碼器可支援在壓縮的資料流程中維持交錯。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-129">The Windows Media Video 9 Advanced Profile codec provides support for maintaining interlacing in compressed streams.</span></span>

## <a name="when-to-use-interlaced-video"></a><span data-ttu-id="b7e9d-130">使用交錯式影片的時機</span><span class="sxs-lookup"><span data-stu-id="b7e9d-130">When to Use Interlaced Video</span></span>

<span data-ttu-id="b7e9d-131">只有在交錯式裝置上顯示內容時，才會對交錯式影片進行編碼。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-131">Encoding interlaced video is useful only when the content is displayed on an interlaced device.</span></span> <span data-ttu-id="b7e9d-132">想要透過機上盒或其他裝置在電視上觀看 (的內容，) 可能需要進行交錯。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-132">Content that is intended to be viewed on a television (through a set-top box or other device) may need to be interlaced.</span></span> <span data-ttu-id="b7e9d-133">要以獨佔方式在電腦顯示器上查看的內容不應編碼為交錯式。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-133">Content that is intended to be viewed exclusively on a computer display should not be encoded as interlaced.</span></span>

<span data-ttu-id="b7e9d-134">若要將交錯式影片編碼為漸進式影片，您必須設定輸入設定。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-134">To encode interlaced video as progressive video, you must configure input settings.</span></span> <span data-ttu-id="b7e9d-135">如需詳細資訊，請參閱 [將影片進行逐行掃描](to-deinterlace-video.md)。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-135">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>

## <a name="field-order"></a><span data-ttu-id="b7e9d-136">欄位順序</span><span class="sxs-lookup"><span data-stu-id="b7e9d-136">Field Order</span></span>

<span data-ttu-id="b7e9d-137">交錯影片的大部分來源（例如影片捕獲卡）都會提供影片範例，其中包含兩個欄位交錯。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-137">Most sources of interlaced video, such as video capture cards, deliver video samples that include both fields interleaved with each other.</span></span> <span data-ttu-id="b7e9d-138">結果就像是完整的影片框架，不同的是，奇數甚至線條會稍微移動一段時間。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-138">The result is like a complete frame of video, except that the odd and even lines are shifted slightly in time.</span></span> <span data-ttu-id="b7e9d-139">在交錯的影片範例中，第一次發生的欄位並沒有通用標準。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-139">There is no universal standard as to which field in the interleaved video sample occurs first in time.</span></span>

<span data-ttu-id="b7e9d-140">您應該讓使用者在傳遞交錯式範例至您的應用程式時指定欄位順序。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-140">You should enable users to specify field order when passing interlaced samples to your application.</span></span>

## <a name="encoding-interlaced-video"></a><span data-ttu-id="b7e9d-141">編碼交錯式影片</span><span class="sxs-lookup"><span data-stu-id="b7e9d-141">Encoding Interlaced Video</span></span>

<span data-ttu-id="b7e9d-142">若要使用交錯編碼，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b7e9d-142">To use interlaced encoding, perform the following steps:</span></span>

1.  <span data-ttu-id="b7e9d-143">藉由呼叫 [**IWMStreamConfig2：： AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) 方法，在設定檔中設定影片串流以使用內容類型的資料單位延伸。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-143">Configure the video stream in the profile to use the content type data unit extension by calling the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method.</span></span> <span data-ttu-id="b7e9d-144">內容類型延伸模組的範例延伸模組 GUID 是 WM \_ SampleExtensionsGUID \_ ContentType。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-144">The sample extension GUID for the content type extension is WM\_SampleExtensionsGUID\_ContentType.</span></span>
2.  <span data-ttu-id="b7e9d-145">設定設定檔中的資料流程，並將寫入器設定為一般設定檔。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-145">Set the stream in the profile and configure the writer with the profile as normal.</span></span>
3.  <span data-ttu-id="b7e9d-146">將交錯式範例傳遞給寫入器之前，請先呼叫 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) 方法，將 g \_ wszInterlacedCoding 輸入設定設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-146">Before passing interlaced samples to the writer, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method to set the g\_wszInterlacedCoding input setting to **TRUE**.</span></span>
4.  <span data-ttu-id="b7e9d-147">針對您傳遞至寫入器的每個交錯樣本，呼叫 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 方法以設定內容類型。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-147">For every interlaced sample that you pass to the writer, call the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the content type.</span></span> <span data-ttu-id="b7e9d-148">內容類型值是下表中的旗標組合。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-148">Content type values are combinations of the flags in the following table.</span></span>



| <span data-ttu-id="b7e9d-149">旗標</span><span class="sxs-lookup"><span data-stu-id="b7e9d-149">Flag</span></span>                         | <span data-ttu-id="b7e9d-150">描述</span><span class="sxs-lookup"><span data-stu-id="b7e9d-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e9d-151">WM \_ CT \_ 交錯式</span><span class="sxs-lookup"><span data-stu-id="b7e9d-151">WM\_CT\_INTERLACED</span></span>           | <span data-ttu-id="b7e9d-152">編碼交錯的內容時，一律設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-152">Always set this flag when encoding interlaced content.</span></span> <span data-ttu-id="b7e9d-153">如果您在沒有設定欄位順序旗標的情況下使用此旗標 (WM \_ ct \_ \_ \_ 第一個欄位或 WM \_ ct \_ 頂端 \_ 欄位 \_) 編解碼器將會假設頂端欄位是第一個。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-153">If you use this flag without setting a field-order flag (WM\_CT\_BOTTOM\_FIELD\_FIRST or WM\_CT\_TOP\_FIELD\_FIRST) the codec will assume that the top field is first.</span></span> <span data-ttu-id="b7e9d-154">如果編解碼器使用錯誤的欄位順序，就不會對影像品質產生任何影響，但編碼效率將會受到影響。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-154">If the codec uses the wrong field order, there should be no impact on image quality, but the encoding efficiency will be affected.</span></span> |
| <span data-ttu-id="b7e9d-155">WM \_ CT \_ 下 \_ \_ 一個欄位</span><span class="sxs-lookup"><span data-stu-id="b7e9d-155">WM\_CT\_BOTTOM\_FIELD\_FIRST</span></span> | <span data-ttu-id="b7e9d-156">當結合了 WM \_ CT \_ 交錯旗標時，此旗標會指出底部欄位 (第二行開始的欄位，) 會先發生。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-156">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the bottom field (the field starting with the second line in the sample) occurs first in time.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="b7e9d-157">WM \_ CT \_ 頂端 \_ 欄位 \_ 優先</span><span class="sxs-lookup"><span data-stu-id="b7e9d-157">WM\_CT\_TOP\_FIELD\_FIRST</span></span>    | <span data-ttu-id="b7e9d-158">當結合了 WM \_ CT \_ 交錯旗標時，此旗標會指出第一個欄位 (開頭為範例中第一行的欄位，) 第一次發生。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-158">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the top field (the field starting with the first line in the sample) occurs first in time.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="b7e9d-159">WM \_ CT \_ 重複 \_ 第一個 \_ 欄位</span><span class="sxs-lookup"><span data-stu-id="b7e9d-159">WM\_CT\_REPEAT\_FIRST\_FIELD</span></span> | <span data-ttu-id="b7e9d-160">指出範例中的第一個欄位應該在播放時重複。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-160">Indicates that the first field in the sample should be repeated on playback.</span></span> <span data-ttu-id="b7e9d-161">此旗標用於影片，該影片是由電影程式從電影建立的。如果未將任何欄位順序旗標與此旗標一起設定，則會假設頂端欄位是在第一次發生。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-161">This flag is used for video that has created from film by the telecine process.If no field-order flag is set in conjunction with this flag, the top field is assumed to occur first in time.</span></span><br/>                                                                             |



 

> [!Note]  
> <span data-ttu-id="b7e9d-162">如果 \_ \_ 未設定 WM CT 交錯旗標，則會假設範例包含漸進式的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-162">If the WM\_CT\_INTERLACED flag is not set, the sample is assumed to contain a progressive video frame.</span></span>

 

## <a name="decoding-interlaced-video"></a><span data-ttu-id="b7e9d-163">解碼交錯式影片</span><span class="sxs-lookup"><span data-stu-id="b7e9d-163">Decoding Interlaced Video</span></span>

<span data-ttu-id="b7e9d-164">解碼交錯式影片時，您必須 \_ 使用 [**IWMReaderAdvanced2：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)方法，將 g wszAllowInterlacedOutput 設定設為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-164">When decoding interlaced video, you must set the g\_wszAllowInterlacedOutput setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="b7e9d-165">否則編解碼器將會提供漸進式的框架。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-165">Otherwise the codec will deliver progressive frames.</span></span>

<span data-ttu-id="b7e9d-166">內容類型資料單位延伸是在輸出範例上進行維護。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-166">The content type data unit extension is maintained on the output samples.</span></span> <span data-ttu-id="b7e9d-167">您應該將欄位方向傳遞到轉譯裝置，以確保能正常播放。</span><span class="sxs-lookup"><span data-stu-id="b7e9d-167">You should pass the field orientation to the rendering device to ensure proper playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7e9d-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7e9d-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7e9d-169">**Advanced 主題**</span><span class="sxs-lookup"><span data-stu-id="b7e9d-169">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





