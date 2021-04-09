---
title: 若要逐行掃描影片
description: 若要逐行掃描影片
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows Media Format SDK，deinterlaced 影片
- Windows Media Format SDK，反向電視
- Windows Media Format SDK，電影
- Advanced Systems Format (ASF) 、deinterlaced 影片
- ASF (Advanced Systems Format) 、deinterlaced video
- Advanced Systems Format (ASF) ，反向電視
- ASF (Advanced Systems Format) ，反向電視
- Advanced Systems Format (ASF) ，電影
- ASF (Advanced Systems Format) ，電影
- deinterlaced 影片
- 反向電視電影，關於
- 電影、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580b8425e5807fefdfa889fcd08deedb4143cf39
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023056"
---
# <a name="to-deinterlace-video"></a><span data-ttu-id="80053-115">若要逐行掃描影片</span><span class="sxs-lookup"><span data-stu-id="80053-115">To Deinterlace Video</span></span>

<span data-ttu-id="80053-116">影片的某些來源（例如影片捕獲卡片）會傳遞影片資料以進行交錯顯示。</span><span class="sxs-lookup"><span data-stu-id="80053-116">Some sources of video, such as video capture cards, deliver video data for interlaced display.</span></span> <span data-ttu-id="80053-117">交錯影片的每個畫面格都是由兩個欄位所組成。</span><span class="sxs-lookup"><span data-stu-id="80053-117">Each frame of interlaced video is made up of two fields.</span></span> <span data-ttu-id="80053-118">頂端欄位包含第一行影片和其後的每一行。</span><span class="sxs-lookup"><span data-stu-id="80053-118">The top field contains the first line of video and every other line thereafter.</span></span> <span data-ttu-id="80053-119">底部的欄位包含第二行的影片和其後的每一行。</span><span class="sxs-lookup"><span data-stu-id="80053-119">The bottom field contains the second line of video and every other line thereafter.</span></span> <span data-ttu-id="80053-120">其中一個欄位包含所有偶數行，另一個則包含所有奇數的行。</span><span class="sxs-lookup"><span data-stu-id="80053-120">So one field contains all of the even numbered lines and the other contains all of the odd numbered lines.</span></span> <span data-ttu-id="80053-121">組成框架的欄位代表呈現時間稍微不同，因此在交錯時，它們不會形成靜態影像。</span><span class="sxs-lookup"><span data-stu-id="80053-121">The fields that make up a frame represent slightly different presentation times so that, when interleaved, they do not form a static image.</span></span>

<span data-ttu-id="80053-122">當您想要在電腦監視器上顯示影片時，影片的每個畫面格都應該顯示為一個影像 (此方法會一次顯示一個整個框架的影片，稱為「 *漸進式* 影片」。 ) 如果您以漸進方式顯示交錯的影片，則畫面格可能不會正確，因為這兩個欄位之間的時間差異。</span><span class="sxs-lookup"><span data-stu-id="80053-122">When you want to display video on a computer monitor, each frame of the video should be displayed as one image (this method of displaying video one whole frame at a time is called *progressive* video.) If you display interlaced video progressively, the frames may not look right, because of the time difference between the two fields.</span></span> <span data-ttu-id="80053-123">Windows Media 視訊編解碼器和 Windows Media 視訊 Advanced Profile 編解碼器都支援將交錯式內容轉換成漸進式框架的前置處理功能。</span><span class="sxs-lookup"><span data-stu-id="80053-123">The Windows Media Video codec and the Windows Media Video Advanced Profile codec both support a preprocessing feature that converts interlaced content into progressive frames.</span></span>

<span data-ttu-id="80053-124">若要讓編解碼器將輸入影片進行逐行掃描，請呼叫 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) 方法。</span><span class="sxs-lookup"><span data-stu-id="80053-124">To have the codec deinterlace input video, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method.</span></span> <span data-ttu-id="80053-125">要使用的設定為 g \_ wszDeinterlaceMode。</span><span class="sxs-lookup"><span data-stu-id="80053-125">The setting to use is g\_wszDeinterlaceMode.</span></span> <span data-ttu-id="80053-126">將去交錯模式設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="80053-126">Set the deinterlacing mode to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80053-127">值</span><span class="sxs-lookup"><span data-stu-id="80053-127">Value</span></span></th>
<th><span data-ttu-id="80053-128">描述</span><span class="sxs-lookup"><span data-stu-id="80053-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="80053-129">WM_DM_NOTINTERLACED</span><span class="sxs-lookup"><span data-stu-id="80053-129">WM_DM_NOTINTERLACED</span></span></td>
<td><span data-ttu-id="80053-130">輸入是漸進式的。</span><span class="sxs-lookup"><span data-stu-id="80053-130">Input is progressive.</span></span> <span data-ttu-id="80053-131">當您先前已將去交錯模式設定為另一個值時，請使用此設定來停止去交錯。</span><span class="sxs-lookup"><span data-stu-id="80053-131">Use this setting to stop deinterlacing when you have previously set the deinterlacing mode to another value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80053-132">WM_DM_DEINTERLACE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="80053-132">WM_DM_DEINTERLACE_NORMAL</span></span></td>
<td><span data-ttu-id="80053-133">選取此模式以混合交錯框架的偶數和奇數位段， (使用運動補償機制) 。好處：</span><span class="sxs-lookup"><span data-stu-id="80053-133">Select this mode to blend the even and odd fields of an interlaced frame (using a motion compensation mechanism).Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="80053-134">漸進顯示的交錯構件大幅減少。</span><span class="sxs-lookup"><span data-stu-id="80053-134">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
<li><span data-ttu-id="80053-135">Windows Media 視訊編解碼器會產生較高品質的壓縮影片。</span><span class="sxs-lookup"><span data-stu-id="80053-135">The Windows Media Video codec produces higher quality compressed video.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80053-136">WM_DM_DEINTERLACE_HALFSIZE</span><span class="sxs-lookup"><span data-stu-id="80053-136">WM_DM_DEINTERLACE_HALFSIZE</span></span></td>
<td><span data-ttu-id="80053-137">當輸出解析度為輸入解析度的一半或更少時，請選取此模式。</span><span class="sxs-lookup"><span data-stu-id="80053-137">Select this mode when the output resolution is half, or less, of the input resolution.</span></span> <span data-ttu-id="80053-138">例如，當輸入影片解析度為 640 x 480 圖元，且輸出視頻解析度為 320 x 240 圖元時，請使用此模式。好處：</span><span class="sxs-lookup"><span data-stu-id="80053-138">For example, use this mode when the input video resolution is 640 x 480 pixels and the output video resolution is 320 x 240 pixels.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="80053-139">漸進顯示的交錯構件大幅減少。</span><span class="sxs-lookup"><span data-stu-id="80053-139">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80053-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="80053-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="80053-141">當輸出解析度為輸入解析度的一半或更少時，請選取此模式，而且輸出 <a href="wmformat-glossary.md"><em>畫面播放速率</em></a> 會是高兩倍。</span><span class="sxs-lookup"><span data-stu-id="80053-141">Select this mode when the output resolution is half, or less, of the input resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="80053-142">例如，當輸入影片解析度是 640 x 480 圖元（每秒30個交錯的框架/秒），且輸出影片解析度為 320 x 240 圖元（每秒的60畫面格）時，請使用此模式。好處：</span><span class="sxs-lookup"><span data-stu-id="80053-142">For example, use this mode when the input video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="80053-143">這會產生高品質的漸進式框架，因為每個欄位都會轉換成框架，因此不需要 blend 任何資訊。</span><span class="sxs-lookup"><span data-stu-id="80053-143">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="80053-144">會捕獲交錯式欄位的完整動作。</span><span class="sxs-lookup"><span data-stu-id="80053-144">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="80053-145">WM_DM_DEINTERLACE_INVERSETELECINE</span><span class="sxs-lookup"><span data-stu-id="80053-145">WM_DM_DEINTERLACE_INVERSETELECINE</span></span></td>
<td><span data-ttu-id="80053-146">選取此模式可將 telecined 30 個畫面/秒的影片轉換成原始電影的每秒24個畫面格。好處：</span><span class="sxs-lookup"><span data-stu-id="80053-146">Select this mode to convert telecined 30 frames/sec video into the 24 frames/sec of the original film.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="80053-147">壓縮品質大幅改善，因為只需要編碼24個框架/秒，而不是每秒30個畫面格。</span><span class="sxs-lookup"><span data-stu-id="80053-147">The compression quality improves significantly because only 24 frames/sec instead of 30 frames/sec need to be encoded.</span></span></li>
<li><span data-ttu-id="80053-148">由於結果是漸進式的，因此會實現去交錯的相同壓縮和顯示優勢。</span><span class="sxs-lookup"><span data-stu-id="80053-148">Because the result is progressive, the same compression and display benefits of deinterlacing are realized.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="80053-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="80053-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="80053-150">當垂直輸出解析度是輸入垂直解析度的一半或更少時，請選取此模式，而且輸出 <a href="wmformat-glossary.md"><em>畫面播放速率</em></a> 會是高兩倍。</span><span class="sxs-lookup"><span data-stu-id="80053-150">Select this mode when the vertical output resolution is half, or less, of the input vertical resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="80053-151">例如，輸入垂直影片解析度是 640 x 480 圖元，每秒30個交錯的畫面格，輸出垂直影片解析度是 320 x 240 圖元，每秒畫面60。好處：</span><span class="sxs-lookup"><span data-stu-id="80053-151">For example, the input vertical video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output vertical video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="80053-152">這會產生高品質的漸進式框架，因為每個欄位都會轉換成框架，因此不需要 blend 任何資訊。</span><span class="sxs-lookup"><span data-stu-id="80053-152">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="80053-153">會捕獲交錯式欄位的完整動作。</span><span class="sxs-lookup"><span data-stu-id="80053-153">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="80053-154">針對混合內容，請在傳遞新類型的範例之前，視需要設定去交錯模式。</span><span class="sxs-lookup"><span data-stu-id="80053-154">For mixed content, set the deinterlacing mode as needed before passing samples of a new type.</span></span> <span data-ttu-id="80053-155">例如，若要以漸進式輸入開始編碼，您不需要設定任何去交錯模式。</span><span class="sxs-lookup"><span data-stu-id="80053-155">For example, to start encoding with progressive input, you don't need to set any deinterlacing mode.</span></span> <span data-ttu-id="80053-156">如果某些範例接著需要一般去交錯，您必須將去交錯模式設定為 WM \_ DM 可進行 \_ 一般的交錯 \_ 。</span><span class="sxs-lookup"><span data-stu-id="80053-156">If some samples then require normal deinterlacing, you must set the deinterlacing mode to WM\_DM\_DEINTERLACE\_NORMAL.</span></span> <span data-ttu-id="80053-157">若要處理其他漸進式範例，您必須將去交錯模式設定為 WM \_ DM \_ NOTINTERLACED。</span><span class="sxs-lookup"><span data-stu-id="80053-157">To then process additional progressive samples you must set the deinterlacing mode to WM\_DM\_NOTINTERLACED.</span></span>

## <a name="inverse-telecine-settings"></a><span data-ttu-id="80053-158">反向電影設定</span><span class="sxs-lookup"><span data-stu-id="80053-158">Inverse Telecine Settings</span></span>

<span data-ttu-id="80053-159">如需反向電視電影的說明，請參閱 [使用反向電視電影](to-use-inverse-telecine.md)。</span><span class="sxs-lookup"><span data-stu-id="80053-159">For a description of inverse telecine, see [To Use Inverse Telecine](to-use-inverse-telecine.md).</span></span>

<span data-ttu-id="80053-160">如果您將去交錯模式設定為 WM \_ DM \_ 交錯 \_ INVERSETELECINE，您可以藉由呼叫 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)，指定第一個輸入框架的電影模式。</span><span class="sxs-lookup"><span data-stu-id="80053-160">If you set the deinterlacing mode to WM\_DM\_DEINTERLACE\_INVERSETELECINE, you can specify the telecine pattern of the first input frame by calling the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="80053-161">要使用的設定為 g \_ wszInitialPatternForInverseTelecine。</span><span class="sxs-lookup"><span data-stu-id="80053-161">The setting to use is g\_wszInitialPatternForInverseTelecine.</span></span> <span data-ttu-id="80053-162">將初始模式設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="80053-162">Set the initial pattern to one of the following values.</span></span>



| <span data-ttu-id="80053-163">值</span><span class="sxs-lookup"><span data-stu-id="80053-163">Value</span></span>                                              | <span data-ttu-id="80053-164">描述</span><span class="sxs-lookup"><span data-stu-id="80053-164">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80053-165">WM \_ DM \_ IT \_ 停用 \_ 一致 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="80053-165">WM\_DM\_IT\_DISABLE\_COHERENT\_MODE</span></span>                | <span data-ttu-id="80053-166">指定輸入媒體已通過電視程式，但框架已不再處於可預測的模式。</span><span class="sxs-lookup"><span data-stu-id="80053-166">Specifies that the input media has gone through the telecine process but that the frames are no longer in a predictable pattern.</span></span> <span data-ttu-id="80053-167">這通常表示媒體是在電影處理之後編輯。</span><span class="sxs-lookup"><span data-stu-id="80053-167">This usually indicates that the media was edited after the telecine processing.</span></span> <span data-ttu-id="80053-168">當您使用此設定時，編解碼器會嘗試自行重建原始框架。</span><span class="sxs-lookup"><span data-stu-id="80053-168">When you use this setting, the codec attempts to reconstruct the original frames on its own.</span></span> |
| <span data-ttu-id="80053-169">\_以 WM \_ 的 \_ 方式將第一個剪輯中的第一個 \_ 框架顯示 \_ \_ \_ 為 \_ AA \_ TOP</span><span class="sxs-lookup"><span data-stu-id="80053-169">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_TOP</span></span>    | <span data-ttu-id="80053-170">指定 AA 框架的頂端欄位是第一個範例。</span><span class="sxs-lookup"><span data-stu-id="80053-170">Specifies that the top field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="80053-171">\_ \_ \_ 在剪輯中的第一幀第一個 \_ 框架 \_ \_ \_ 是 \_ BB \_ TOP</span><span class="sxs-lookup"><span data-stu-id="80053-171">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_TOP</span></span>    | <span data-ttu-id="80053-172">指定 BB 框架的頂端欄位是第一個範例。</span><span class="sxs-lookup"><span data-stu-id="80053-172">Specifies that the top field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="80053-173">\_ \_ \_ 在剪輯中的第一幀 IT 第一個 \_ 框架 \_ \_ \_ 是 \_ BC \_ TOP</span><span class="sxs-lookup"><span data-stu-id="80053-173">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_TOP</span></span>    | <span data-ttu-id="80053-174">指定 BC 框架的頂端欄位是第一個範例。</span><span class="sxs-lookup"><span data-stu-id="80053-174">Specifies that the top field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="80053-175">\_以 WM \_ 的 \_ 方式將第一個剪輯中的第一個 \_ 框架 \_ \_ 放在 \_ \_ \_ 最上層</span><span class="sxs-lookup"><span data-stu-id="80053-175">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_TOP</span></span>    | <span data-ttu-id="80053-176">指定 CD 框架的頂端欄位是第一個範例。</span><span class="sxs-lookup"><span data-stu-id="80053-176">Specifies that the top field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="80053-177">\_以 WM \_ 的 \_ \_ 方式將剪輯第一個框架中的第一個框架 \_ \_ \_ 作為 \_ DD \_ TOP</span><span class="sxs-lookup"><span data-stu-id="80053-177">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_TOP</span></span>    | <span data-ttu-id="80053-178">指定 DD 框架的頂端欄位是第一個範例。</span><span class="sxs-lookup"><span data-stu-id="80053-178">Specifies that the top field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="80053-179">WM \_ DM \_ IT \_ 第一個 \_ 框架 \_ 在 \_ 剪輯中 \_ 是 \_ AA \_ 底部</span><span class="sxs-lookup"><span data-stu-id="80053-179">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_BOTTOM</span></span> | <span data-ttu-id="80053-180">指定 AA 框架的底部欄位是第一個範例。</span><span class="sxs-lookup"><span data-stu-id="80053-180">Specifies that the bottom field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="80053-181">\_ \_ \_ \_ 在剪輯中，WM 的第一個框架 \_ \_ \_ 是 \_ BB \_ 底端</span><span class="sxs-lookup"><span data-stu-id="80053-181">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_BOTTOM</span></span> | <span data-ttu-id="80053-182">指定 BB 框架的底端欄位是第一個範例。</span><span class="sxs-lookup"><span data-stu-id="80053-182">Specifies that the bottom field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="80053-183">\_以 WM \_ \_ \_ 為範圍的第一個剪輯第一個框架 \_ \_ \_ 是 \_ BC \_ 底部</span><span class="sxs-lookup"><span data-stu-id="80053-183">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_BOTTOM</span></span> | <span data-ttu-id="80053-184">指定 BC 框架的底部欄位是第一個範例。</span><span class="sxs-lookup"><span data-stu-id="80053-184">Specifies that the bottom field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="80053-185">\_以 WM \_ 的 \_ \_ 方式將剪輯第一個框架的第一個框架 \_ \_ 放在 \_ \_ 光碟上 \_</span><span class="sxs-lookup"><span data-stu-id="80053-185">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_BOTTOM</span></span> | <span data-ttu-id="80053-186">指定 CD 框架的底部欄位是第一個範例。</span><span class="sxs-lookup"><span data-stu-id="80053-186">Specifies that the bottom field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="80053-187">\_以 WM \_ 的 \_ \_ 方式將剪輯第一個框架中的第一個框架 \_ \_ \_ 作為 \_ DD \_ 底部</span><span class="sxs-lookup"><span data-stu-id="80053-187">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_BOTTOM</span></span> | <span data-ttu-id="80053-188">指定 DD 框架的下半部欄位是第一個範例。</span><span class="sxs-lookup"><span data-stu-id="80053-188">Specifies that the bottom field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="80053-189">相關主題</span><span class="sxs-lookup"><span data-stu-id="80053-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80053-190">**Advanced 主題**</span><span class="sxs-lookup"><span data-stu-id="80053-190">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





