---
description: 速率變更屬性集可讓 MPEG-2 來源/剖析器篩選器變更播放速率。 MPEG-2 解碼器應該支援此屬性集。 DVD 導覽器和資料流程緩衝區引擎都會使用此屬性集來控制播放速率。
ms.assetid: f88c64ce-af76-49fe-8ebd-029928506243
title: '速率變更屬性集 (Dvdmedia .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e56b679b0ce9b0127b15c69cd02b016a4990b6f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990624"
---
# <a name="rate-change-property-set"></a><span data-ttu-id="514b3-105">速率變更屬性集</span><span class="sxs-lookup"><span data-stu-id="514b3-105">Rate Change Property Set</span></span>

<span data-ttu-id="514b3-106">速率變更屬性集可讓 MPEG-2 來源/剖析器篩選器變更播放速率。</span><span class="sxs-lookup"><span data-stu-id="514b3-106">The Rate Change property set enables MPEG-2 source/parser filters to change the playback rate.</span></span> <span data-ttu-id="514b3-107">MPEG-2 解碼器應該支援此屬性集。</span><span class="sxs-lookup"><span data-stu-id="514b3-107">MPEG-2 decoders should support this property set.</span></span> <span data-ttu-id="514b3-108">DVD 導覽器和資料流程緩衝區引擎都會使用此屬性集來控制播放速率。</span><span class="sxs-lookup"><span data-stu-id="514b3-108">The DVD Navigator and the Stream Buffer Engine both use this property set to control playback rates.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="514b3-109">屬性集 GUID</span><span class="sxs-lookup"><span data-stu-id="514b3-109">Property Set GUID</span></span> | <span data-ttu-id="514b3-110">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="514b3-110">AM\_KSPROPSETID\_TSRateChange</span></span> |



 



| <span data-ttu-id="514b3-111">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="514b3-111">Property ID</span></span>                                                                   | <span data-ttu-id="514b3-112">描述</span><span class="sxs-lookup"><span data-stu-id="514b3-112">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="514b3-113">**AM \_ RATE \_ CorrectTS**</span><span class="sxs-lookup"><span data-stu-id="514b3-113">**AM\_RATE\_CorrectTS**</span></span>](am-rate-correctts-property.md)                     | <span data-ttu-id="514b3-114">通知解碼器導覽器正在設定正確的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="514b3-114">Informs the decoder that the Navigator is setting the correct time stamps.</span></span>             |
| <span data-ttu-id="514b3-115">AM \_ RATE \_ ExactRateChange</span><span class="sxs-lookup"><span data-stu-id="514b3-115">AM\_RATE\_ExactRateChange</span></span>                                                     | <span data-ttu-id="514b3-116">已過時。</span><span class="sxs-lookup"><span data-stu-id="514b3-116">Obsolete.</span></span>                                                                              |
| [<span data-ttu-id="514b3-117">**AM \_ RATE \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="514b3-117">**AM\_RATE\_MaxFullDataRate**</span></span>](am-rate-maxfulldatarate-property.md)         | <span data-ttu-id="514b3-118">查詢解碼器的最大資料速率。</span><span class="sxs-lookup"><span data-stu-id="514b3-118">Queries the decoder for the decoder's maximum data rate.</span></span>                               |
| [<span data-ttu-id="514b3-119">**AM \_ RATE \_ QueryFullFrameRate**</span><span class="sxs-lookup"><span data-stu-id="514b3-119">**AM\_RATE\_QueryFullFrameRate**</span></span>](am-rate-queryfullframerate-property.md)   | <span data-ttu-id="514b3-120">查詢解碼器的最大全畫面播放速率的解碼器。</span><span class="sxs-lookup"><span data-stu-id="514b3-120">Queries the decoder for the decoder's maximum full-frame rate.</span></span>                         |
| [<span data-ttu-id="514b3-121">**AM \_ RATE \_ QueryLastRateSegPTS**</span><span class="sxs-lookup"><span data-stu-id="514b3-121">**AM\_RATE\_QueryLastRateSegPTS**</span></span>](am-rate-querylastratesegpts-property.md) | <span data-ttu-id="514b3-122">查詢解碼器，以取得最近設定之速率區段的開始時間。</span><span class="sxs-lookup"><span data-stu-id="514b3-122">Queries the decoder for the start time of the rate segment that was set most recently.</span></span> |
| [<span data-ttu-id="514b3-123">**AM \_ RATE \_ SimpleRateChange**</span><span class="sxs-lookup"><span data-stu-id="514b3-123">**AM\_RATE\_SimpleRateChange**</span></span>](am-rate-simpleratechange-property.md)       | <span data-ttu-id="514b3-124">將速率變更傳送至解碼器。</span><span class="sxs-lookup"><span data-stu-id="514b3-124">Sends a rate change to the decoder.</span></span>                                                    |
| <span data-ttu-id="514b3-125">AM \_ RATE \_ Step</span><span class="sxs-lookup"><span data-stu-id="514b3-125">AM\_RATE\_Step</span></span>                                                                | <span data-ttu-id="514b3-126">已過時。</span><span class="sxs-lookup"><span data-stu-id="514b3-126">Obsolete.</span></span> <span data-ttu-id="514b3-127">請參閱 [框架逐步執行屬性集](frame-stepping-property-set.md)。</span><span class="sxs-lookup"><span data-stu-id="514b3-127">See [Frame Stepping Property Set](frame-stepping-property-set.md).</span></span>          |
| [<span data-ttu-id="514b3-128">**AM \_ RATE \_ UseRateVersion**</span><span class="sxs-lookup"><span data-stu-id="514b3-128">**AM\_RATE\_UseRateVersion**</span></span>](am-rate-userateversion-property.md)           | <span data-ttu-id="514b3-129">指定要使用的速率變更機制版本。</span><span class="sxs-lookup"><span data-stu-id="514b3-129">Specifies which version of the rate change mechanism to use.</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="514b3-130">備註</span><span class="sxs-lookup"><span data-stu-id="514b3-130">Remarks</span></span>

<span data-ttu-id="514b3-131">在這個屬性集的內容中，rate 會測量相對於參考時鐘的時間戳記前進的速率。</span><span class="sxs-lookup"><span data-stu-id="514b3-131">In the context of this property set, rate measures the rate at which time stamps advance relative to the reference clock.</span></span> <span data-ttu-id="514b3-132">對播放速度的反向進行評分。</span><span class="sxs-lookup"><span data-stu-id="514b3-132">Rate the inverse of playback speed.</span></span> <span data-ttu-id="514b3-133">例如，如果播放速度為2x，則時間戳記必須以標準速率增加到1/2。</span><span class="sxs-lookup"><span data-stu-id="514b3-133">For example, if the playback speed is 2x, the time stamps must increase at 1/2 the normal rate.</span></span> <span data-ttu-id="514b3-134">這會轉譯成更快的播放速度，因為樣本的轉譯速度早于一般。</span><span class="sxs-lookup"><span data-stu-id="514b3-134">This translates to a faster playback speed, because samples are rendered earlier than normal.</span></span>

<span data-ttu-id="514b3-135">範例會傳送至具有時間戳記的時間戳記等於以1x 速率表示的呈現時間的解碼器。</span><span class="sxs-lookup"><span data-stu-id="514b3-135">Samples are sent to the decoder with a time stamp equal to the presentation time at 1x rate.</span></span> <span data-ttu-id="514b3-136">此解碼器必須將輸出範例上的時間戳記調整為目前速率的正確呈現時間。</span><span class="sxs-lookup"><span data-stu-id="514b3-136">The decoder must scale the time stamps on the output samples to the correct presentation time for the current rate.</span></span> <span data-ttu-id="514b3-137">例如，如果速率是 1/2 (表示播放速度為 2x) ，則此解碼器必須將時間戳記調整為1/2。</span><span class="sxs-lookup"><span data-stu-id="514b3-137">For example, if the rate is 1/2 (meaning the playback speed is 2x), the decoder must scale the time stamps by 1/2.</span></span> <span data-ttu-id="514b3-138">一般來說，只有 I 個框架具有時間戳記。</span><span class="sxs-lookup"><span data-stu-id="514b3-138">Generally, only I frames have time stamps.</span></span> <span data-ttu-id="514b3-139">此解碼器必須插入 B 和 P 框架的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="514b3-139">The decoder must interpolate the time stamps for the B and P frames.</span></span> <span data-ttu-id="514b3-140">請注意，在進行反向播放時，時間戳記會持續增加，時間戳記永遠不會再向下。</span><span class="sxs-lookup"><span data-stu-id="514b3-140">Note that during reverse playback, time stamps continue to increase — time stamps never go backward.</span></span>

<span data-ttu-id="514b3-141">已定義兩個版本的速率變更屬性集，版本1.0 和1.1 版。</span><span class="sxs-lookup"><span data-stu-id="514b3-141">Two versions of the Rate Change property set are defined, version 1.0 and version 1.1.</span></span> <span data-ttu-id="514b3-142">預設行為是由1.0 版提供。</span><span class="sxs-lookup"><span data-stu-id="514b3-142">The default behavior is given by version 1.0.</span></span> <span data-ttu-id="514b3-143">建議使用解碼器廠商支援1.1 版，因為它提供更流暢的播放體驗。</span><span class="sxs-lookup"><span data-stu-id="514b3-143">Decoder vendors are encouraged to support version 1.1, because it provides a smoother playback experience.</span></span> <span data-ttu-id="514b3-144">DVD 導覽器目前使用1.0 版。</span><span class="sxs-lookup"><span data-stu-id="514b3-144">The DVD Navigator currently uses version 1.0.</span></span> <span data-ttu-id="514b3-145">資料流程緩衝區引擎使用1.1 版。</span><span class="sxs-lookup"><span data-stu-id="514b3-145">The Stream Buffer Engine uses version 1.1.</span></span>

### <a name="rate-change-version-10"></a><span data-ttu-id="514b3-146">速率變更版本1。0</span><span class="sxs-lookup"><span data-stu-id="514b3-146">Rate Change Version 1.0</span></span>

<span data-ttu-id="514b3-147">1.0 版的速率變更屬性集會定義 MPEG-2 的預設行為。</span><span class="sxs-lookup"><span data-stu-id="514b3-147">Version 1.0 of the Rate Change property set defines the default behavior for MPEG-2 decoders.</span></span>

<span data-ttu-id="514b3-148">來源篩選藉由設定 [**AM \_ rate \_ SimpleRateChange**](am-rate-simpleratechange-property.md) 屬性來發出速率變更的信號。</span><span class="sxs-lookup"><span data-stu-id="514b3-148">The source filter signals a rate change by setting the [**AM\_RATE\_SimpleRateChange**](am-rate-simpleratechange-property.md) property.</span></span> <span data-ttu-id="514b3-149">這個屬性的資料是新的速率，以及當速率生效時輸入範例的開始時間。</span><span class="sxs-lookup"><span data-stu-id="514b3-149">The data for this property is the new rate, plus the start time on the input sample when the rate takes effect.</span></span> <span data-ttu-id="514b3-150">此解碼器會維護暫止速率變更的佇列，並依開始時間排序。</span><span class="sxs-lookup"><span data-stu-id="514b3-150">The decoder maintains a queue of pending rate changes, sorted by start time.</span></span>

<span data-ttu-id="514b3-151">在 DVD 導覽器變更為非1x 的速度之前，它會提供所有暫止的範例、暫時將速率設定為1.0，以及排清圖形。</span><span class="sxs-lookup"><span data-stu-id="514b3-151">Before the DVD Navigator changes to a non-1x speed, it delivers all pending samples, temporarily sets the rate to 1.0, and flushes the graph.</span></span> <span data-ttu-id="514b3-152">然後，它會設定新的費率。</span><span class="sxs-lookup"><span data-stu-id="514b3-152">Then it sets the new rate.</span></span> <span data-ttu-id="514b3-153">所有速率變更都會排定在目前 VOBU 的結尾， (video 物件單位) 。</span><span class="sxs-lookup"><span data-stu-id="514b3-153">All rate changes are scheduled for the end of the current VOBU (video object unit).</span></span> <span data-ttu-id="514b3-154">請注意，清除圖形會將呈現時間重設為零。</span><span class="sxs-lookup"><span data-stu-id="514b3-154">Note that flushing the graph resets the presentation time to zero.</span></span>

<span data-ttu-id="514b3-155">DVD 導覽器以 *平滑模式* 或 *掃描模式* 操作。</span><span class="sxs-lookup"><span data-stu-id="514b3-155">The DVD Navigator operates either in *smooth mode* or in *scan mode*.</span></span> <span data-ttu-id="514b3-156">在平滑模式中，它會將每個畫面格傳送給解碼器，包括 B 框架和 P 框架。</span><span class="sxs-lookup"><span data-stu-id="514b3-156">In smooth mode, it sends every frame to the decoder, including B frames and P frames.</span></span> <span data-ttu-id="514b3-157">當播放速度大於零但小於解碼器的 maxmimum 資料速率時，DVD 導覽器會使用平滑模式。</span><span class="sxs-lookup"><span data-stu-id="514b3-157">The DVD Navigator uses smooth mode whenever playback speed is greater than zero but less than the decoder's maxmimum data rate.</span></span> <span data-ttu-id="514b3-158">如果播放速度小於零 (反轉播放) ，或超過解碼器的最大資料速率，則 DVD 瀏覽器會使用掃描模式，在此模式中，它只會將 I 框架傳送至解碼器。</span><span class="sxs-lookup"><span data-stu-id="514b3-158">If playback speed is less than zero (reverse playback), or exceeds the decoder's maximum data rate, the DVD Navigator uses scan mode, where it sends just the I frames to the decoder.</span></span> <span data-ttu-id="514b3-159">在非常高的速度下，它可能會略過一些框架;例如，它可能會傳送其他每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="514b3-159">At very high speeds, it may skip some I frames; for example, it may send every other I frame.</span></span>

<span data-ttu-id="514b3-160">根據預設，DVD 導覽器會靜音非1.0 的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="514b3-160">By default, the DVD Navigator mutes the audio stream for rates other than 1.0.</span></span> <span data-ttu-id="514b3-161">您可以藉由呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) 與 DVD AudioDuringFFwdRew 旗標來變更此項 \_ 。</span><span class="sxs-lookup"><span data-stu-id="514b3-161">You can change this by calling [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) with the DVD\_AudioDuringFFwdRew flag.</span></span>

### <a name="rate-change-version-11"></a><span data-ttu-id="514b3-162">速率變更版本1。1</span><span class="sxs-lookup"><span data-stu-id="514b3-162">Rate Change Version 1.1</span></span>

<span data-ttu-id="514b3-163">速率變更屬性集的1.1 版遵循與1.0 版相同的基本原則，但有下列差異：</span><span class="sxs-lookup"><span data-stu-id="514b3-163">Version 1.1 of the Rate Change property set follows the same basic principles as version 1.0, with the following differences:</span></span>

-   <span data-ttu-id="514b3-164">來源篩選器會藉由設定 [**AM \_ 速率 \_ UseRateVersion**](am-rate-userateversion-property.md) 屬性，來指示要使用版本1.1 的解碼器。</span><span class="sxs-lookup"><span data-stu-id="514b3-164">The source filter signals the decoder to use version 1.1 by setting the [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md) property.</span></span> <span data-ttu-id="514b3-165">否則，此解碼器應使用1.0 版的行為。</span><span class="sxs-lookup"><span data-stu-id="514b3-165">Otherwise, the decoder should use the version 1.0 behavior.</span></span>
-   <span data-ttu-id="514b3-166">來源篩選不會在速率變更之間清除圖形。</span><span class="sxs-lookup"><span data-stu-id="514b3-166">The source filter does not flush the graph between rate changes.</span></span> <span data-ttu-id="514b3-167">因此，時間戳記會在速率變更界限之間進行單純的增加，而不是重設為零。</span><span class="sxs-lookup"><span data-stu-id="514b3-167">Time stamps therefore increase monotonically across rate change boundaries, rather than resetting to zero.</span></span>
-   <span data-ttu-id="514b3-168">來源篩選器不會針對特定參考時間將速率變更排入佇列，而是會指定將速率變更套用至解碼器的 *最轉寄範例*，並在解碼器傳出佇列的開頭定義為範例。</span><span class="sxs-lookup"><span data-stu-id="514b3-168">Instead of queuing a rate change for a particular reference time, the source filter can specify that a rate change applies to the decoder's *most forward sample*, defined as the sample at the head of the decoder's outgoing queue.</span></span> <span data-ttu-id="514b3-169">若要這樣做，來源篩選器會使用 [**AM \_ RATE \_ SimpleRateChange**](am-rate-simpleratechange-property.md) 屬性，但會將開始時間設定為-1。</span><span class="sxs-lookup"><span data-stu-id="514b3-169">To do so, the source filter uses the [**AM\_RATE\_SimpleRateChange**](am-rate-simpleratechange-property.md) property but sets the start time equal to -1.</span></span>
-   <span data-ttu-id="514b3-170">來源篩選器可以查詢解碼器，以取得最近排入佇列之速率變更的開始時間。</span><span class="sxs-lookup"><span data-stu-id="514b3-170">The source filter can query the decoder for the start time of the rate change that was queued most recently.</span></span> <span data-ttu-id="514b3-171">基於此目的，它會使用 [**AM \_ RATE \_ QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="514b3-171">It uses the [**AM\_RATE\_QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) property for this purpose.</span></span>
-   <span data-ttu-id="514b3-172">來源篩選不會捨棄範例。</span><span class="sxs-lookup"><span data-stu-id="514b3-172">The source filter does not drop samples.</span></span> <span data-ttu-id="514b3-173">如果速率超過解碼器的最大資料速率，則應該視需要卸載框架。</span><span class="sxs-lookup"><span data-stu-id="514b3-173">If the rate exceeds the decoder's maximum data rate, the decoder should drop frames as necessary.</span></span>
-   <span data-ttu-id="514b3-174">無論音訊解碼器的最大資料速率為何，來源篩選都不會將音訊串流靜音。</span><span class="sxs-lookup"><span data-stu-id="514b3-174">The source filter does not mute the audio stream, regardless of the audio decoder's maximum data rate.</span></span> <span data-ttu-id="514b3-175">如果播放速度超過解碼器的最大速率，音訊解碼器可以卸載範例。</span><span class="sxs-lookup"><span data-stu-id="514b3-175">The audio decoder can drop samples if the playback speed exceeds the decoder's maximum rate.</span></span> <span data-ttu-id="514b3-176">不過，它仍應維持排程費率變更的佇列。</span><span class="sxs-lookup"><span data-stu-id="514b3-176">However, it should still maintain the queue of scheduled rate changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="514b3-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="514b3-177">Requirements</span></span>



| <span data-ttu-id="514b3-178">需求</span><span class="sxs-lookup"><span data-stu-id="514b3-178">Requirement</span></span> | <span data-ttu-id="514b3-179">值</span><span class="sxs-lookup"><span data-stu-id="514b3-179">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="514b3-180">標頭</span><span class="sxs-lookup"><span data-stu-id="514b3-180">Header</span></span><br/> | <dl> <span data-ttu-id="514b3-181"><dt>Dvdmedia。h</dt></span><span class="sxs-lookup"><span data-stu-id="514b3-181"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="514b3-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="514b3-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="514b3-183">屬性集</span><span class="sxs-lookup"><span data-stu-id="514b3-183">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




