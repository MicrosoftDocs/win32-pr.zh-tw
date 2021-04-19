---
description: 影片交錯
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: 影片交錯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec10f49ef21f3701f85467a3f4a1c4b08d69df72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974977"
---
# <a name="video-interlacing"></a><span data-ttu-id="6103d-103">影片交錯</span><span class="sxs-lookup"><span data-stu-id="6103d-103">Video Interlacing</span></span>

<span data-ttu-id="6103d-104">本主題說明媒體來源和解碼器應該如何處理交錯的影片內容。</span><span class="sxs-lookup"><span data-stu-id="6103d-104">This topic describes how media sources and decoders should handle interlaced video content.</span></span>

<span data-ttu-id="6103d-105">若要正確地解碼和轉譯交錯的影片，需要下列資訊：</span><span class="sxs-lookup"><span data-stu-id="6103d-105">To decode and render interlaced video correctly, the following information is needed:</span></span>

-   <span data-ttu-id="6103d-106">漸進式或交錯式。</span><span class="sxs-lookup"><span data-stu-id="6103d-106">Progressive or interlaced.</span></span> <span data-ttu-id="6103d-107">影片串流可以包含漸進式的框架、交錯的框架，或兩者的混合。</span><span class="sxs-lookup"><span data-stu-id="6103d-107">A video stream can contain progressive frames, interlaced frames, or a mix of both.</span></span>

-   <span data-ttu-id="6103d-108">現場支配。</span><span class="sxs-lookup"><span data-stu-id="6103d-108">Field dominance.</span></span> <span data-ttu-id="6103d-109">欄位支配會描述先出現的欄位、上方欄位或下方欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-109">Field dominance describes which field appears first, the upper field or the lower field.</span></span>

-   <span data-ttu-id="6103d-110">重複第一個欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-110">Repeat first field.</span></span> <span data-ttu-id="6103d-111">當框架是漸進式的，但資料流程是交錯式時，會在3:2 的下拉中使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="6103d-111">This flag is used in 3:2 pulldown, when the frame is progressive but the stream is interlaced.</span></span> <span data-ttu-id="6103d-112">在此內容中，第一個欄位可以是欄位的上限或下限。</span><span class="sxs-lookup"><span data-stu-id="6103d-112">In this context, the first field can be the upper or lower field.</span></span>

-   <span data-ttu-id="6103d-113">交錯的欄位或單一欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-113">Interleaved fields or single field.</span></span> <span data-ttu-id="6103d-114">範例可以保留單一欄位或兩個交錯的欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-114">A sample can hold either a single field, or two interleaved fields.</span></span> <span data-ttu-id="6103d-115">如果範例包含單一欄位，範例高度會是框架高度的一半，因為此範例只包含框架的一半掃描行。</span><span class="sxs-lookup"><span data-stu-id="6103d-115">If a sample contains a single field, the sample height is half the frame height, because the sample contains only half of the scan lines for a frame.</span></span> <span data-ttu-id="6103d-116">除非來源內容的特性另外決定，否則建議使用交錯欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-116">Interleaved fields are recommended unless the characteristics of the source content dictate otherwise.</span></span>

<span data-ttu-id="6103d-117">任何這些特性都可以從一個範例變更為下一個範例。</span><span class="sxs-lookup"><span data-stu-id="6103d-117">Any of these characteristics can change from one sample to the next.</span></span> <span data-ttu-id="6103d-118">不過，在串流處理開始之前，影片元件需要知道整體內容的相關事項。</span><span class="sxs-lookup"><span data-stu-id="6103d-118">However, video components need to know something about the overall content before streaming begins.</span></span> <span data-ttu-id="6103d-119">例如，如果影片是交錯的，則增強的影片轉譯器 (EVR) 需要為去交錯保留視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="6103d-119">For example, if the video is interlaced, the enhanced video renderer (EVR) needs to reserve video memory for the deinterlacing.</span></span> <span data-ttu-id="6103d-120">另一方面，如果影片完全是漸進式框架，EVR 可以優化轉譯管線。</span><span class="sxs-lookup"><span data-stu-id="6103d-120">If the video is entirely progressive frames, on the other hand, the EVR can optimize the rendering pipeline.</span></span> <span data-ttu-id="6103d-121">將去交錯步驟新增至管線會增加轉譯延遲。</span><span class="sxs-lookup"><span data-stu-id="6103d-121">Adding a deinterlacing step to the pipeline increases the rendering latency.</span></span>

<span data-ttu-id="6103d-122">交錯的相關資訊會儲存在兩個位置：</span><span class="sxs-lookup"><span data-stu-id="6103d-122">Information about interlacing is stored in two places:</span></span>

-   <span data-ttu-id="6103d-123">資料流程中交錯的一般資訊會放在媒體類型中。</span><span class="sxs-lookup"><span data-stu-id="6103d-123">General information about the interlacing in a stream is placed in the media type.</span></span> <span data-ttu-id="6103d-124">如需媒體類型的詳細資訊，請參閱 [媒體類型](media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="6103d-124">For more information about media types, see [Media Types](media-types.md).</span></span>

-   <span data-ttu-id="6103d-125">可隨著每個範例變更的資訊會放在範例上做為屬性。</span><span class="sxs-lookup"><span data-stu-id="6103d-125">Information that can change with each sample is placed on the sample as an attribute.</span></span> <span data-ttu-id="6103d-126">如需範例的詳細資訊，請參閱 [媒體範例](media-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="6103d-126">For more information about samples, see [Media Samples](media-samples.md).</span></span>

## <a name="interlace-information-in-the-media-type"></a><span data-ttu-id="6103d-127">媒體類型中的隔行資訊</span><span class="sxs-lookup"><span data-stu-id="6103d-127">Interlace Information in the Media Type</span></span>

<span data-ttu-id="6103d-128">媒體類型上的 [**MF \_ MT \_ 交錯 \_ 模式**](mf-mt-interlace-mode-attribute.md) 屬性描述整個資料流程如何交錯。</span><span class="sxs-lookup"><span data-stu-id="6103d-128">The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute on the media type describes how the stream as a whole is interlaced.</span></span> <span data-ttu-id="6103d-129">這個屬性的值是 [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="6103d-129">The value of this attribute is a member of the [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) enumeration.</span></span> <span data-ttu-id="6103d-130">影片媒體類型應該一律有此屬性。</span><span class="sxs-lookup"><span data-stu-id="6103d-130">A video media type should always have this attribute.</span></span>

-   <span data-ttu-id="6103d-131">如果資料流程只包含漸進式框架（沒有交錯框架），請使用 MFVideoInterlace \_ 累進。</span><span class="sxs-lookup"><span data-stu-id="6103d-131">If the stream contains only progressive frames, with no interlaced frames, use MFVideoInterlace\_Progressive.</span></span>
-   <span data-ttu-id="6103d-132">如果資料流程只包含交錯的框架，而且每個範例都包含兩個交錯的欄位，請使用 MFVideoInterlace \_ FieldInterleavedUpperFirst 或 MFVideoInterlace \_ FieldInterleavedLowerFirst。</span><span class="sxs-lookup"><span data-stu-id="6103d-132">If the stream contains only interlaced frames, and every sample contains two interleaved fields, use MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>
-   <span data-ttu-id="6103d-133">如果資料流程只包含交錯的框架，而且每個範例都包含單一欄位，請使用 MFVideoInterlace \_ FieldSingleUpper 或 MFVideoInterlace \_ FieldSingleLower。</span><span class="sxs-lookup"><span data-stu-id="6103d-133">If the stream contains only interlaced frames, and every sample contains a single field, use MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span> <span data-ttu-id="6103d-134">如果欄位在上方和下方都是替代欄位，則這兩個值的使用方式並不重要。</span><span class="sxs-lookup"><span data-stu-id="6103d-134">If the fields alternate between upper and lower, then it does not matter which of these two values is used.</span></span> <span data-ttu-id="6103d-135">如果格式只包含上方欄位，或只包含較低的欄位，請設定對應至內容的值。</span><span class="sxs-lookup"><span data-stu-id="6103d-135">If the format contains just upper fields, or just lower fields, then set the value that corresponds to the content.</span></span>
-   <span data-ttu-id="6103d-136">如果資料流程包含混合式和漸進式框架，或如果欄位支配參數，請將媒體類型設定為 MFVideoInterlace \_ MixedInterlaceOrProgressive。</span><span class="sxs-lookup"><span data-stu-id="6103d-136">If the stream contains a mix of interlaced and progressive frames, or if the field dominance switches, set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span> <span data-ttu-id="6103d-137">使用範例屬性來描述每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="6103d-137">Use sample attributes to describe each frame.</span></span>

<span data-ttu-id="6103d-138">下表摘要說明此屬性。</span><span class="sxs-lookup"><span data-stu-id="6103d-138">The following table summarizes this attribute.</span></span>



| <span data-ttu-id="6103d-139">MF \_ MT \_ 交錯 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="6103d-139">MF\_MT\_INTERLACE\_MODE</span></span>                       | <span data-ttu-id="6103d-140">交錯？</span><span class="sxs-lookup"><span data-stu-id="6103d-140">Interlaced?</span></span> | <span data-ttu-id="6103d-141">範例</span><span class="sxs-lookup"><span data-stu-id="6103d-141">Samples</span></span>                                  | <span data-ttu-id="6103d-142">第一個欄位</span><span class="sxs-lookup"><span data-stu-id="6103d-142">First field</span></span>    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| <span data-ttu-id="6103d-143">MFVideoInterlace \_ 漸進式</span><span class="sxs-lookup"><span data-stu-id="6103d-143">MFVideoInterlace\_Progressive</span></span>                 | <span data-ttu-id="6103d-144">No</span><span class="sxs-lookup"><span data-stu-id="6103d-144">No</span></span>          | <span data-ttu-id="6103d-145">漸進式框架</span><span class="sxs-lookup"><span data-stu-id="6103d-145">Progressive frame</span></span>                        | <span data-ttu-id="6103d-146">不適用</span><span class="sxs-lookup"><span data-stu-id="6103d-146">Not applicable</span></span> |
| <span data-ttu-id="6103d-147">MFVideoInterlace \_ FieldInterleavedUpperFirst</span><span class="sxs-lookup"><span data-stu-id="6103d-147">MFVideoInterlace\_FieldInterleavedUpperFirst</span></span>  | <span data-ttu-id="6103d-148">Yes</span><span class="sxs-lookup"><span data-stu-id="6103d-148">Yes</span></span>         | <span data-ttu-id="6103d-149">交錯欄位</span><span class="sxs-lookup"><span data-stu-id="6103d-149">Interleaved fields</span></span>                       | <span data-ttu-id="6103d-150">上一個</span><span class="sxs-lookup"><span data-stu-id="6103d-150">Upper first</span></span>    |
| <span data-ttu-id="6103d-151">MFVideoInterlace \_ FieldInterleavedLowerFirst</span><span class="sxs-lookup"><span data-stu-id="6103d-151">MFVideoInterlace\_FieldInterleavedLowerFirst</span></span>  | <span data-ttu-id="6103d-152">Yes</span><span class="sxs-lookup"><span data-stu-id="6103d-152">Yes</span></span>         | <span data-ttu-id="6103d-153">交錯欄位</span><span class="sxs-lookup"><span data-stu-id="6103d-153">Interleaved fields</span></span>                       | <span data-ttu-id="6103d-154">先較低</span><span class="sxs-lookup"><span data-stu-id="6103d-154">Lower first</span></span>    |
| <span data-ttu-id="6103d-155">MFVideoInterlace \_ FieldSingleUpper</span><span class="sxs-lookup"><span data-stu-id="6103d-155">MFVideoInterlace\_FieldSingleUpper</span></span>            | <span data-ttu-id="6103d-156">Yes</span><span class="sxs-lookup"><span data-stu-id="6103d-156">Yes</span></span>         | <span data-ttu-id="6103d-157">單一欄位</span><span class="sxs-lookup"><span data-stu-id="6103d-157">Single field</span></span>                             | <span data-ttu-id="6103d-158">上一個</span><span class="sxs-lookup"><span data-stu-id="6103d-158">Upper first</span></span>    |
| <span data-ttu-id="6103d-159">MFVideoInterlace \_ FieldSingleLower</span><span class="sxs-lookup"><span data-stu-id="6103d-159">MFVideoInterlace\_FieldSingleLower</span></span>            | <span data-ttu-id="6103d-160">Yes</span><span class="sxs-lookup"><span data-stu-id="6103d-160">Yes</span></span>         | <span data-ttu-id="6103d-161">單一欄位</span><span class="sxs-lookup"><span data-stu-id="6103d-161">Single field</span></span>                             | <span data-ttu-id="6103d-162">先較低</span><span class="sxs-lookup"><span data-stu-id="6103d-162">Lower first</span></span>    |
| <span data-ttu-id="6103d-163">MFVideoInterlace \_ MixedInterlaceOrProgressive</span><span class="sxs-lookup"><span data-stu-id="6103d-163">MFVideoInterlace\_MixedInterlaceOrProgressive</span></span> | <span data-ttu-id="6103d-164">可能不同</span><span class="sxs-lookup"><span data-stu-id="6103d-164">Can vary</span></span>    | <span data-ttu-id="6103d-165">交錯的欄位或漸進式框架</span><span class="sxs-lookup"><span data-stu-id="6103d-165">Interleaved fields or progressive frames</span></span> | <span data-ttu-id="6103d-166">可能不同</span><span class="sxs-lookup"><span data-stu-id="6103d-166">Can vary</span></span>       |



 

<span data-ttu-id="6103d-167">交錯的欄位和單一欄位不能混用。</span><span class="sxs-lookup"><span data-stu-id="6103d-167">Interleaved fields and single fields cannot be mixed.</span></span> <span data-ttu-id="6103d-168">從一個切換到另一個需要變更媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6103d-168">Switching from one to another requires a media type change.</span></span>

## <a name="interlace-flags-on-samples"></a><span data-ttu-id="6103d-169">範例上的交錯旗標</span><span class="sxs-lookup"><span data-stu-id="6103d-169">Interlace Flags on Samples</span></span>

<span data-ttu-id="6103d-170">可從某個範例變更為下一個樣本的資訊會使用範例屬性來表示。</span><span class="sxs-lookup"><span data-stu-id="6103d-170">Information that can change from one sample to the next is indicated using sample attributes.</span></span> <span data-ttu-id="6103d-171">您可以使用 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面來取得或設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6103d-171">Use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to get or set these attributes.</span></span>

<span data-ttu-id="6103d-172">本節所列的所有交錯屬性都有布林值。</span><span class="sxs-lookup"><span data-stu-id="6103d-172">All of the interlacing attributes listed in this section have Boolean values.</span></span> <span data-ttu-id="6103d-173">實際上，每個屬性都可以有三個值： **TRUE**、 **FALSE** 或未設定。</span><span class="sxs-lookup"><span data-stu-id="6103d-173">Effectively, each of these attributes can have three values: either **TRUE**, **FALSE**, or not set.</span></span> <span data-ttu-id="6103d-174">如果未設定屬性，則會從媒體類型取得值。</span><span class="sxs-lookup"><span data-stu-id="6103d-174">If an attribute is not set, the value is taken from the media type.</span></span> <span data-ttu-id="6103d-175">如果已設定屬性，此值會覆寫媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6103d-175">If an attribute is set, the value overrides the media type.</span></span> <span data-ttu-id="6103d-176">某些旗標和媒體類型的組合無效。</span><span class="sxs-lookup"><span data-stu-id="6103d-176">Some combinations of flags and media types are not valid.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6103d-177">屬性</span><span class="sxs-lookup"><span data-stu-id="6103d-177">Attribute</span></span></th>
<th><span data-ttu-id="6103d-178">描述</span><span class="sxs-lookup"><span data-stu-id="6103d-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6103d-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span><span class="sxs-lookup"><span data-stu-id="6103d-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span></span></td>
<td><span data-ttu-id="6103d-180">若 <strong>為 TRUE</strong>，則框架為交錯式。</span><span class="sxs-lookup"><span data-stu-id="6103d-180">If <strong>TRUE</strong>, the frame is interlaced.</span></span> <span data-ttu-id="6103d-181">如果 <strong>為 FALSE</strong>，則表示框架為漸進式。</span><span class="sxs-lookup"><span data-stu-id="6103d-181">If <strong>FALSE</strong>, the frame is progressive.</span></span><br/> <span data-ttu-id="6103d-182">如果媒體類型為 MFVideoInterlace_MixedInterlaceOrProgressive，請在每個範例上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="6103d-182">Set this attribute on every sample if the media type is MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6103d-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span><span class="sxs-lookup"><span data-stu-id="6103d-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span></span></td>
<td><span data-ttu-id="6103d-184">此旗標的意義取決於範例是否包含交錯欄位或單一欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-184">The meaning of this flag depends on whether the samples contain interleaved fields or single fields.</span></span><br/>
<ul>
<li><span data-ttu-id="6103d-185">交錯欄位：如果 <strong>為 TRUE</strong>，則較低的欄位為第一個。</span><span class="sxs-lookup"><span data-stu-id="6103d-185">Interleaved fields: If <strong>TRUE</strong>, the lower field is first.</span></span> <span data-ttu-id="6103d-186">如果 <strong>為 FALSE</strong>，則表示上方欄位為第一個。</span><span class="sxs-lookup"><span data-stu-id="6103d-186">If <strong>FALSE</strong>, the upper field is first.</span></span><br/></li>
<li><span data-ttu-id="6103d-187">單一欄位：如果 <strong>為 TRUE</strong>，則範例包含較低的欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-187">Single fields: If <strong>TRUE</strong>, the sample contains a lower field.</span></span> <span data-ttu-id="6103d-188">如果 <strong>為 FALSE</strong>，則表示範例包含上方欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-188">If <strong>FALSE</strong>, the sample contains an upper field.</span></span><br/></li>
</ul>
<span data-ttu-id="6103d-189">如果媒體類型為 MFVideoInterlace_FieldSingleUpper、MFVideoInterlace_FieldSingleLower 或 MFVideoInterlace_MixedInterlaceOrProgressive，請在每個交錯範例上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="6103d-189">Set this attribute on every interlace sample if the media type is MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower, or MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6103d-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span><span class="sxs-lookup"><span data-stu-id="6103d-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span></span></td>
<td><span data-ttu-id="6103d-191">若 <strong>為 TRUE</strong>，則會重複第一個欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-191">If <strong>TRUE</strong>, the first field is repeated.</span></span> <span data-ttu-id="6103d-192">如果 <strong>為 FALSE</strong> 或未設定，則不會重複第一個欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-192">If <strong>FALSE</strong> or not set, the first field is not repeated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6103d-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span><span class="sxs-lookup"><span data-stu-id="6103d-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span></span></td>
<td><span data-ttu-id="6103d-194">若 <strong>為 TRUE</strong>，則範例包含單一欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-194">If <strong>TRUE</strong>, the sample contains a single field.</span></span> <span data-ttu-id="6103d-195">如果 <strong>為 FALSE</strong>，則範例包含交錯的欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-195">If <strong>FALSE</strong>, the sample contains interleaved fields.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6103d-196">下表根據媒體類型顯示必要、選擇性或禁止的旗標。</span><span class="sxs-lookup"><span data-stu-id="6103d-196">The following table shows which flags are required, optional, or prohibited, based on the media type.</span></span>



| <span data-ttu-id="6103d-197">媒體類型</span><span class="sxs-lookup"><span data-stu-id="6103d-197">Media Type</span></span>         | <span data-ttu-id="6103d-198">交錯旗標</span><span class="sxs-lookup"><span data-stu-id="6103d-198">Interlaced Flag</span></span>                      | <span data-ttu-id="6103d-199">BottomFieldFirst 旗標</span><span class="sxs-lookup"><span data-stu-id="6103d-199">BottomFieldFirst Flag</span></span>                    | <span data-ttu-id="6103d-200">RepeatFirstField 旗標</span><span class="sxs-lookup"><span data-stu-id="6103d-200">RepeatFirstField Flag</span></span> | <span data-ttu-id="6103d-201">SingleField 旗標</span><span class="sxs-lookup"><span data-stu-id="6103d-201">SingleField Flag</span></span>                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| <span data-ttu-id="6103d-202">漸進式</span><span class="sxs-lookup"><span data-stu-id="6103d-202">Progressive</span></span>        | <span data-ttu-id="6103d-203">參數如果設定，則必須為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-203">Optional; if set, must be **FALSE**.</span></span> | <span data-ttu-id="6103d-204">不要設定。</span><span class="sxs-lookup"><span data-stu-id="6103d-204">Do not set.</span></span>                              | <span data-ttu-id="6103d-205">不要設定。</span><span class="sxs-lookup"><span data-stu-id="6103d-205">Do not set.</span></span>           | <span data-ttu-id="6103d-206">不要設定。</span><span class="sxs-lookup"><span data-stu-id="6103d-206">Do not set.</span></span>                          |
| <span data-ttu-id="6103d-207">交錯欄位</span><span class="sxs-lookup"><span data-stu-id="6103d-207">Interleaved fields</span></span> | <span data-ttu-id="6103d-208">參數如果設定，則必須為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-208">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="6103d-209">參數如果設定，必須符合媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6103d-209">Optional; if set, must match media type.</span></span> | <span data-ttu-id="6103d-210">不要設定。</span><span class="sxs-lookup"><span data-stu-id="6103d-210">Do not set.</span></span>           | <span data-ttu-id="6103d-211">參數如果設定，則必須為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-211">Optional; if set, must be **FALSE**.</span></span> |
| <span data-ttu-id="6103d-212">單一欄位</span><span class="sxs-lookup"><span data-stu-id="6103d-212">Single fields</span></span>      | <span data-ttu-id="6103d-213">參數如果設定，則必須為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-213">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="6103d-214">必要。</span><span class="sxs-lookup"><span data-stu-id="6103d-214">Required.</span></span>                                | <span data-ttu-id="6103d-215">不要設定。</span><span class="sxs-lookup"><span data-stu-id="6103d-215">Do not set.</span></span>           | <span data-ttu-id="6103d-216">設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-216">Set to **TRUE**.</span></span>                     |
| <span data-ttu-id="6103d-217">Mixed</span><span class="sxs-lookup"><span data-stu-id="6103d-217">Mixed</span></span>              | <span data-ttu-id="6103d-218">必要。</span><span class="sxs-lookup"><span data-stu-id="6103d-218">Required.</span></span>                            | <span data-ttu-id="6103d-219">必要。</span><span class="sxs-lookup"><span data-stu-id="6103d-219">Required.</span></span>                                | <span data-ttu-id="6103d-220">必要。</span><span class="sxs-lookup"><span data-stu-id="6103d-220">Required.</span></span>             | <span data-ttu-id="6103d-221">參數如果設定，則必須為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-221">Optional; if set, must be **FALSE**.</span></span> |



 

<span data-ttu-id="6103d-222">在屬性為選擇性的情況下，媒體類型已定義資訊。</span><span class="sxs-lookup"><span data-stu-id="6103d-222">In the cases where the attribute is optional, the media type already defines the information.</span></span> <span data-ttu-id="6103d-223">將屬性設定為相符（但不是必要）是有效的。</span><span class="sxs-lookup"><span data-stu-id="6103d-223">It is valid to set the attribute to match, but not required.</span></span>

<span data-ttu-id="6103d-224">例如，如果媒體類型是 MFVideoInterlace \_ 累進，則表示資料流程中的所有框架都是漸進式的。</span><span class="sxs-lookup"><span data-stu-id="6103d-224">For example, if the media type is MFVideoInterlace\_Progressive, it implies that all frames in the stream are progressive.</span></span> <span data-ttu-id="6103d-225">因此，您可以將 [ **MFSampleExtension \_ 交錯** ] 屬性設定為 [ **FALSE**]，或將屬性保留為 [未設定]。</span><span class="sxs-lookup"><span data-stu-id="6103d-225">Therefore, you can either set the **MFSampleExtension\_Interlaced** attribute to **FALSE**, or leave the attribute unset.</span></span>

## <a name="recommendations"></a><span data-ttu-id="6103d-226">建議</span><span class="sxs-lookup"><span data-stu-id="6103d-226">Recommendations</span></span>

<span data-ttu-id="6103d-227">本節包含各種內容類型的建議。</span><span class="sxs-lookup"><span data-stu-id="6103d-227">This section contains recommendations for various types of content.</span></span>

1. <span data-ttu-id="6103d-228">影片是所有漸進式的畫面格。</span><span class="sxs-lookup"><span data-stu-id="6103d-228">The video is all progressive frames.</span></span>

-   <span data-ttu-id="6103d-229">將 [媒體類型] 設定為 [ \_ 漸進式 MFVideoInterlace]。</span><span class="sxs-lookup"><span data-stu-id="6103d-229">Set the media type to MFVideoInterlace\_Progressive.</span></span>

-   <span data-ttu-id="6103d-230">請勿設定 **MFSampleExtension \_ 交錯** 屬性，或在每個畫面格上將其設定為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6103d-230">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="6103d-231">請勿設定 **MFSampleExtension \_ BottomFieldFirst**、 **MFSampleExtension \_ RepeatFirstField** 或 **MFSampleExtension \_ SingleField** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6103d-231">Do not set the **MFSampleExtension\_BottomFieldFirst**, **MFSampleExtension\_RepeatFirstField**, or **MFSampleExtension\_SingleField** attributes.</span></span>

2. <span data-ttu-id="6103d-232">影片是具有相同現場支配的所有交錯欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-232">The video is all interlaced fields with the same field dominance.</span></span> <span data-ttu-id="6103d-233">範例包含交錯的欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-233">Samples contain interleaved fields.</span></span>

-   <span data-ttu-id="6103d-234">將 [媒體類型] 設定為 [MFVideoInterlace \_ FieldInterleavedUpperFirst] 或 [MFVideoInterlace \_ FieldInterleavedLowerFirst]。</span><span class="sxs-lookup"><span data-stu-id="6103d-234">Set the media type to MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>

-   <span data-ttu-id="6103d-235">請勿設定 **MFSampleExtension \_ 交錯** 屬性，或在每個畫面格上將其設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="6103d-235">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="6103d-236">請勿設定 **MFSampleExtension \_ BottomFieldFirst** 屬性，或設定每個畫面格的值以符合媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6103d-236">Do not set the **MFSampleExtension\_BottomFieldFirst** attribute, or set the value on every frame to match the media type.</span></span>

-   <span data-ttu-id="6103d-237">請勿設定 **MFSampleExtension \_ RepeatFirstField** 屬性，或在每個畫面格上將其設定為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6103d-237">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="6103d-238">請勿設定 **MFSampleExtension \_ SingleField** 屬性，或在每個畫面格上將其設定為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6103d-238">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

3. <span data-ttu-id="6103d-239">影片包含混合式和漸進式的框架，其中包含重複的欄位和不同的現場支配 (例如 DVD 影片) 。</span><span class="sxs-lookup"><span data-stu-id="6103d-239">The video contains a mix of interlaced and progressive frames, with repeated fields and varying field dominance (for example, DVD video).</span></span>

-   <span data-ttu-id="6103d-240">將 [媒體類型] 設定為 [MFVideoInterlace \_ MixedInterlaceOrProgressive]。</span><span class="sxs-lookup"><span data-stu-id="6103d-240">Set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span>

-   <span data-ttu-id="6103d-241">在每個畫面上，設定 **MFSampleExtension \_ 交錯** 式、 **MFSampleExtension \_ BottomFieldFirst** 和 **MFSampleExtension \_ RepeatFirstField** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6103d-241">On every frame, set the **MFSampleExtension\_Interlaced**, **MFSampleExtension\_BottomFieldFirst**, and **MFSampleExtension\_RepeatFirstField** attributes.</span></span>

-   <span data-ttu-id="6103d-242">請勿設定 **MFSampleExtension \_ SingleField** 屬性，或在每個畫面格上將其設定為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6103d-242">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

4. <span data-ttu-id="6103d-243">影片是交錯的，範例包含單一欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-243">The video is interlaced and samples contain single fields.</span></span>

-   <span data-ttu-id="6103d-244">將 [媒體類型] 設定為 [MFVideoInterlace \_ FieldSingleUpper] 或 [MFVideoInterlace \_ FieldSingleLower]。</span><span class="sxs-lookup"><span data-stu-id="6103d-244">Set the media type to MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span>

-   <span data-ttu-id="6103d-245">在每個畫面上，設定 **MFSampleExtension \_ BottomFieldFirst** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6103d-245">On every frame, set the **MFSampleExtension\_BottomFieldFirst** attribute.</span></span>

-   <span data-ttu-id="6103d-246">請勿設定 **MFSampleExtension \_ 交錯** 屬性，或在每個畫面格上將其設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="6103d-246">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="6103d-247">請勿設定 **MFSampleExtension \_ RepeatFirstField** 屬性，或在每個畫面格上將其設定為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6103d-247">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="6103d-248">請勿設定 **MFSampleExtension \_ SingleField** 屬性，或在每個畫面格上將其設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="6103d-248">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **TRUE** on every frame.</span></span>

<span data-ttu-id="6103d-249">大部分的影片內容都屬於上述其中一種類別。</span><span class="sxs-lookup"><span data-stu-id="6103d-249">Most video content falls into one of these categories.</span></span>

## <a name="mpeg-2-mappings"></a><span data-ttu-id="6103d-250">MPEG-2 對應</span><span class="sxs-lookup"><span data-stu-id="6103d-250">MPEG-2 Mappings</span></span>

<span data-ttu-id="6103d-251">針對 MPEG-2 內容，請使用下列對應將 MPEG-2 旗標轉換成媒體基礎範例屬性。</span><span class="sxs-lookup"><span data-stu-id="6103d-251">For MPEG-2 content, use the following mappings to convert the MPEG-2 flags to Media Foundation sample attributes.</span></span>

<span data-ttu-id="6103d-252">**圖片 \_ 結構**</span><span class="sxs-lookup"><span data-stu-id="6103d-252">**picture\_structure**</span></span>



| <span data-ttu-id="6103d-253">值</span><span class="sxs-lookup"><span data-stu-id="6103d-253">Value</span></span>         | <span data-ttu-id="6103d-254">Sample 屬性</span><span class="sxs-lookup"><span data-stu-id="6103d-254">Sample Attribute</span></span>                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6103d-255">框架</span><span class="sxs-lookup"><span data-stu-id="6103d-255">frame</span></span>         | <span data-ttu-id="6103d-256">**MFSampleExtension \_SingleField**  =  **FALSE**</span><span class="sxs-lookup"><span data-stu-id="6103d-256">**MFSampleExtension\_SingleField** = **FALSE**</span></span>                                                                          |
| <span data-ttu-id="6103d-257">頂端 \_ 欄位</span><span class="sxs-lookup"><span data-stu-id="6103d-257">top\_field</span></span>    | <span data-ttu-id="6103d-258">**MFSampleExtension \_SingleField**  =  **TRUE**</span><span class="sxs-lookup"><span data-stu-id="6103d-258">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="6103d-259">**MFSampleExtension \_BottomFieldFirst**  =  **FALSE**</span><span class="sxs-lookup"><span data-stu-id="6103d-259">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span><br/> |
| <span data-ttu-id="6103d-260">底部 \_ 欄位</span><span class="sxs-lookup"><span data-stu-id="6103d-260">bottom\_field</span></span> | <span data-ttu-id="6103d-261">**MFSampleExtension \_SingleField**  =  **TRUE**</span><span class="sxs-lookup"><span data-stu-id="6103d-261">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="6103d-262">**MFSampleExtension \_BottomFieldFirst**  =  **TRUE**</span><span class="sxs-lookup"><span data-stu-id="6103d-262">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span><br/>  |



 

<span data-ttu-id="6103d-263">**漸進式 \_ 框架**</span><span class="sxs-lookup"><span data-stu-id="6103d-263">**progressive\_frame**</span></span>



| <span data-ttu-id="6103d-264">值</span><span class="sxs-lookup"><span data-stu-id="6103d-264">Value</span></span> | <span data-ttu-id="6103d-265">Sample 屬性</span><span class="sxs-lookup"><span data-stu-id="6103d-265">Sample Attribute</span></span>                              |
|-------|-----------------------------------------------|
| <span data-ttu-id="6103d-266">0</span><span class="sxs-lookup"><span data-stu-id="6103d-266">0</span></span>     | <span data-ttu-id="6103d-267">**MFSampleExtension \_交錯** 式  =  **TRUE**</span><span class="sxs-lookup"><span data-stu-id="6103d-267">**MFSampleExtension\_Interlaced** = **TRUE**</span></span>  |
| <span data-ttu-id="6103d-268">1</span><span class="sxs-lookup"><span data-stu-id="6103d-268">1</span></span>     | <span data-ttu-id="6103d-269">**MFSampleExtension \_交錯** 式  =  **FALSE**</span><span class="sxs-lookup"><span data-stu-id="6103d-269">**MFSampleExtension\_Interlaced** = **FALSE**</span></span> |



 

<span data-ttu-id="6103d-270">**top \_ 欄位 \_ first**</span><span class="sxs-lookup"><span data-stu-id="6103d-270">**top\_field\_first**</span></span>



| <span data-ttu-id="6103d-271">值</span><span class="sxs-lookup"><span data-stu-id="6103d-271">Value</span></span> | <span data-ttu-id="6103d-272">Sample 屬性</span><span class="sxs-lookup"><span data-stu-id="6103d-272">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="6103d-273">0</span><span class="sxs-lookup"><span data-stu-id="6103d-273">0</span></span>     | <span data-ttu-id="6103d-274">**MFSampleExtension \_BottomFieldFirst**  =  **TRUE**</span><span class="sxs-lookup"><span data-stu-id="6103d-274">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span>  |
| <span data-ttu-id="6103d-275">1</span><span class="sxs-lookup"><span data-stu-id="6103d-275">1</span></span>     | <span data-ttu-id="6103d-276">**MFSampleExtension \_BottomFieldFirst**  =  **FALSE**</span><span class="sxs-lookup"><span data-stu-id="6103d-276">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span> |



 

<span data-ttu-id="6103d-277">**重複 \_ 第一個 \_ 欄位**</span><span class="sxs-lookup"><span data-stu-id="6103d-277">**repeat\_first\_field**</span></span>



| <span data-ttu-id="6103d-278">值</span><span class="sxs-lookup"><span data-stu-id="6103d-278">Value</span></span> | <span data-ttu-id="6103d-279">Sample 屬性</span><span class="sxs-lookup"><span data-stu-id="6103d-279">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="6103d-280">0</span><span class="sxs-lookup"><span data-stu-id="6103d-280">0</span></span>     | <span data-ttu-id="6103d-281">**MFSampleExtension \_RepeatFirstField**  =  **FALSE**</span><span class="sxs-lookup"><span data-stu-id="6103d-281">**MFSampleExtension\_RepeatFirstField** = **FALSE**</span></span> |
| <span data-ttu-id="6103d-282">1</span><span class="sxs-lookup"><span data-stu-id="6103d-282">1</span></span>     | <span data-ttu-id="6103d-283">**MFSampleExtension \_RepeatFirstField**  =  **TRUE**</span><span class="sxs-lookup"><span data-stu-id="6103d-283">**MFSampleExtension\_RepeatFirstField** = **TRUE**</span></span>  |



 

## <a name="single-field-samples"></a><span data-ttu-id="6103d-284">Single-Field 範例</span><span class="sxs-lookup"><span data-stu-id="6103d-284">Single-Field Samples</span></span>

<span data-ttu-id="6103d-285">如果媒體類型為 [MFVideoInterlace \_ FieldSingleUpper] 或 [MFVideoInterlace \_ FieldSingleLower]，表示每個範例都包含單一欄位。</span><span class="sxs-lookup"><span data-stu-id="6103d-285">If the media type is MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower, it means that each sample contains a single field.</span></span> <span data-ttu-id="6103d-286">不過，媒體類型會描述整個框架。</span><span class="sxs-lookup"><span data-stu-id="6103d-286">However, the media type describes the entire frame.</span></span> <span data-ttu-id="6103d-287">因此，每個緩衝區只包含媒體類型中所指定的欄位行數一半。</span><span class="sxs-lookup"><span data-stu-id="6103d-287">Therefore, each buffer contains only half the number of field lines given in the media type.</span></span> <span data-ttu-id="6103d-288">例如，如果媒體類型將影片描述為720×480，則每個欄位都包含240掃描行，因此每個緩衝區只會包含240的圖元列。</span><span class="sxs-lookup"><span data-stu-id="6103d-288">For example, if the media type describes the video as 720 × 480, each field contains 240 scan lines, and therefore each buffer contains only 240 rows of pixels.</span></span> <span data-ttu-id="6103d-289">如果您撰寫的元件會接受具有單一欄位範例的媒體類型，則當您存取緩衝區中的資料時，必須將這項事實納入考慮。</span><span class="sxs-lookup"><span data-stu-id="6103d-289">If you write a component that accepts media types with single-field samples, you must take this fact into account when you access the data in the buffer.</span></span>

<span data-ttu-id="6103d-290">相同規則適用于幾何光圈 ([MF \_ mt \_ 幾何 \_ 光圈](mf-mt-geometric-aperture-attribute.md) 屬性) 和最小顯示光圈 ([MF \_ mt \_ 最小 \_ 顯示 \_ 光圈](mf-mt-minimum-display-aperture-attribute.md) 屬性) 。</span><span class="sxs-lookup"><span data-stu-id="6103d-290">The same rule applies to the geometric aperture ([MF\_MT\_GEOMETRIC\_APERTURE](mf-mt-geometric-aperture-attribute.md) attribute) and minimum display aperture ([MF\_MT\_MINIMUM\_DISPLAY\_APERTURE](mf-mt-minimum-display-aperture-attribute.md) attribute).</span></span> <span data-ttu-id="6103d-291">這些區域是以整個框架（而非個別欄位）來指定。</span><span class="sxs-lookup"><span data-stu-id="6103d-291">These regions are specified in terms of the entire frame, not the individual fields.</span></span>

## <a name="directshow-mappings"></a><span data-ttu-id="6103d-292">DirectShow 對應</span><span class="sxs-lookup"><span data-stu-id="6103d-292">DirectShow Mappings</span></span>

<span data-ttu-id="6103d-293">在 DirectShow 中，每個範例交錯的資訊都包含在 **AM \_ sample2.xml \_ 屬性** 結構的 **dwTypeSpecificFlags** 成員中。</span><span class="sxs-lookup"><span data-stu-id="6103d-293">In DirectShow, per-sample interlacing information is contained in the **dwTypeSpecificFlags** member of the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="6103d-294">下表顯示媒體基礎的對等屬性。</span><span class="sxs-lookup"><span data-stu-id="6103d-294">The following table shows the equivalent attributes for Media Foundation.</span></span>



| <span data-ttu-id="6103d-295">DirectShow 範例旗標</span><span class="sxs-lookup"><span data-stu-id="6103d-295">DirectShow sample flag</span></span>              | <span data-ttu-id="6103d-296">媒體基礎範例屬性</span><span class="sxs-lookup"><span data-stu-id="6103d-296">Media Foundation sample attribute</span></span>                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6103d-297">AM \_ 影片 \_ 旗標 \_ 交錯 \_ 框</span><span class="sxs-lookup"><span data-stu-id="6103d-297">AM\_VIDEO\_FLAG\_INTERLEAVED\_FRAME</span></span> | <span data-ttu-id="6103d-298">**MFSampleExtension \_SingleField**  =  **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-298">**MFSampleExtension\_SingleField** = **FALSE**.</span></span>                                                                                                                                    |
| <span data-ttu-id="6103d-299">AM \_ 影片 \_ 旗標 \_ FIELD1</span><span class="sxs-lookup"><span data-stu-id="6103d-299">AM\_VIDEO\_FLAG\_FIELD1</span></span>             | <span data-ttu-id="6103d-300">**MFSampleExtension \_交錯** 式  =  **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-300">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="6103d-301">**MFSampleExtension \_SingleField**  =  **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-301">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="6103d-302">**MFSampleExtension \_BottomFieldFirst**  =  **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-302">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span><br/> |
| <span data-ttu-id="6103d-303">AM \_ 影片 \_ 旗標 \_ FIELD2</span><span class="sxs-lookup"><span data-stu-id="6103d-303">AM\_VIDEO\_FLAG\_FIELD2</span></span>             | <span data-ttu-id="6103d-304">**MFSampleExtension \_交錯** 式  =  **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-304">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="6103d-305">**MFSampleExtension \_SingleField**  =  **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-305">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="6103d-306">**MFSampleExtension \_BottomFieldFirst**  =  **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-306">**MFSampleExtension\_BottomFieldFirst** = **TRUE**.</span></span><br/>  |
| <span data-ttu-id="6103d-307">AM \_ 影片 \_ 旗標 \_ 編織</span><span class="sxs-lookup"><span data-stu-id="6103d-307">AM\_VIDEO\_FLAG\_WEAVE</span></span>              | <span data-ttu-id="6103d-308">**MFSampleExtension \_交錯** 式  =  **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-308">**MFSampleExtension\_Interlaced** = **FALSE**.</span></span> <span data-ttu-id="6103d-309"> (此旗標指出驅動程式不應將這兩個欄位進行逐行掃描。 ) </span><span class="sxs-lookup"><span data-stu-id="6103d-309">(This flag indicates that the driver should not deinterlace the two fields.)</span></span>                                                        |
| <span data-ttu-id="6103d-310">AM \_ 影片 \_ 旗標 \_ FIELD1FIRST</span><span class="sxs-lookup"><span data-stu-id="6103d-310">AM\_VIDEO\_FLAG\_FIELD1FIRST</span></span>        | <span data-ttu-id="6103d-311">**MFSampleExtension \_BottomFieldFirst**  =  **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-311">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> <span data-ttu-id="6103d-312">如果內容是交錯式的，而 AM \_ 影片 \_ 旗標 \_ FIELD1FIRST 旗標不存在，請將此屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-312">If the content is interlaced and the AM\_VIDEO\_FLAG\_FIELD1FIRST flag is not present, set this attribute to **TRUE**.</span></span>        |
| <span data-ttu-id="6103d-313">AM \_ 影片 \_ 旗標 \_ 重複 \_ 欄位</span><span class="sxs-lookup"><span data-stu-id="6103d-313">AM\_VIDEO\_FLAG\_REPEAT\_FIELD</span></span>      | <span data-ttu-id="6103d-314">**MFSampleExtension \_RepeatFirstField**  =  **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-314">**MFSampleExtension\_RepeatFirstField** = **TRUE**.</span></span> <span data-ttu-id="6103d-315">如果 \_ 不存在「AM 影片 \_ 旗標 \_ 重複欄位」旗標 \_ ，請將此屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-315">If the AM\_VIDEO\_FLAG\_REPEAT\_FIELD flag is not present, set this attribute to **FALSE**.</span></span>                                    |



 

<span data-ttu-id="6103d-316">如果 DirectShow 範例不包含範例旗標，請使用 **VIDEOINFOHEADER2** 結構的 **dwInterlaceFlags** 值：</span><span class="sxs-lookup"><span data-stu-id="6103d-316">If the DirectShow sample does not contain sample flags, use the value of **dwInterlaceFlags** from the **VIDEOINFOHEADER2** structure:</span></span>



| <span data-ttu-id="6103d-317">DirectShow 交錯旗標</span><span class="sxs-lookup"><span data-stu-id="6103d-317">DirectShow interlace flag</span></span>    | <span data-ttu-id="6103d-318">媒體基礎範例屬性</span><span class="sxs-lookup"><span data-stu-id="6103d-318">Media Foundation sample attribute</span></span>                    |
|------------------------------|------------------------------------------------------|
| <span data-ttu-id="6103d-319">AMINTERLACE \_ IsInterlaced</span><span class="sxs-lookup"><span data-stu-id="6103d-319">AMINTERLACE\_IsInterlaced</span></span>    | <span data-ttu-id="6103d-320">**MFSampleExtension \_交錯** 式  =  **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-320">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span>        |
| <span data-ttu-id="6103d-321">AMINTERLACE \_ 1FieldPerSample</span><span class="sxs-lookup"><span data-stu-id="6103d-321">AMINTERLACE\_1FieldPerSample</span></span> | <span data-ttu-id="6103d-322">**MFSampleExtension \_SingleField**  =  **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-322">**MFSampleExtension\_SingleField** = **TRUE**.</span></span>       |
| <span data-ttu-id="6103d-323">AMINTERLACE \_ Field1First</span><span class="sxs-lookup"><span data-stu-id="6103d-323">AMINTERLACE\_Field1First</span></span>     | <span data-ttu-id="6103d-324">**MFSampleExtension \_BottomFieldFirst**  =  **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6103d-324">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6103d-325">相關主題</span><span class="sxs-lookup"><span data-stu-id="6103d-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6103d-326">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="6103d-326">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="6103d-327">媒體類型</span><span class="sxs-lookup"><span data-stu-id="6103d-327">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




