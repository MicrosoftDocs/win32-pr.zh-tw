---
description: MPEG-2 分隔器媒體類型
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: MPEG-2 分隔器媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e878acaea8bc87bee2bf5c46a6f7e66c7aa0a485
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909424"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="52aa2-103">MPEG-2 分隔器媒體類型</span><span class="sxs-lookup"><span data-stu-id="52aa2-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="52aa2-104">[Mpeg-2 分隔](mpeg-2-splitter.md)器篩選器目前支援音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="52aa2-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="52aa2-105">由 DVD 定義的子串流支援杜比 AC-3。</span><span class="sxs-lookup"><span data-stu-id="52aa2-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="52aa2-106">篩選準則也支援 MPEG-2 音訊。</span><span class="sxs-lookup"><span data-stu-id="52aa2-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="52aa2-107">媒體類型取決於 MPEG-2 分隔器是否提供 PE 封包或 PE 承載。</span><span class="sxs-lookup"><span data-stu-id="52aa2-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="52aa2-108">影片</span><span class="sxs-lookup"><span data-stu-id="52aa2-108">Video</span></span>

<span data-ttu-id="52aa2-109">針對 MPEG-2 影片，媒體類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="52aa2-109">For MPEG-2 video, the media types are as follows.</span></span>



| <span data-ttu-id="52aa2-110">標籤</span><span class="sxs-lookup"><span data-stu-id="52aa2-110">Label</span></span> | <span data-ttu-id="52aa2-111">值</span><span class="sxs-lookup"><span data-stu-id="52aa2-111">Value</span></span> |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="52aa2-112">PE 輸出</span><span class="sxs-lookup"><span data-stu-id="52aa2-112">PES output</span></span>                               | <span data-ttu-id="52aa2-113">承載輸出</span><span class="sxs-lookup"><span data-stu-id="52aa2-113">Payload output</span></span>                 |
| <span data-ttu-id="52aa2-114">主要類型</span><span class="sxs-lookup"><span data-stu-id="52aa2-114">Major Type</span></span>       | <span data-ttu-id="52aa2-115">**媒體媒體的 \_ MPEG2 \_ pe**</span><span class="sxs-lookup"><span data-stu-id="52aa2-115">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="52aa2-116">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="52aa2-116">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="52aa2-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="52aa2-117">Subtype</span></span>          | <span data-ttu-id="52aa2-118">**MEDIASUBTYPE \_ MPEG2 \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="52aa2-118">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="52aa2-119">**MEDIASUBTYPE \_ MPEG2 \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="52aa2-119">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="52aa2-120">格式類型</span><span class="sxs-lookup"><span data-stu-id="52aa2-120">Format Type</span></span>      | <span data-ttu-id="52aa2-121">**格式 \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="52aa2-121">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="52aa2-122">**格式 \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="52aa2-122">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="52aa2-123">格式結構</span><span class="sxs-lookup"><span data-stu-id="52aa2-123">Format Structure</span></span> | [<span data-ttu-id="52aa2-124">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="52aa2-124">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="52aa2-125">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="52aa2-125">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="52aa2-126">AC-3 音訊</span><span class="sxs-lookup"><span data-stu-id="52aa2-126">AC-3 Audio</span></span>

<span data-ttu-id="52aa2-127">針對 AC 3 音訊，媒體類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="52aa2-127">For AC-3 audio, the media types are as follows.</span></span>



| <span data-ttu-id="52aa2-128">標籤</span><span class="sxs-lookup"><span data-stu-id="52aa2-128">Label</span></span> | <span data-ttu-id="52aa2-129">值</span><span class="sxs-lookup"><span data-stu-id="52aa2-129">Value</span></span> |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="52aa2-130">PE 輸出</span><span class="sxs-lookup"><span data-stu-id="52aa2-130">PES output</span></span>                           | <span data-ttu-id="52aa2-131">承載輸出</span><span class="sxs-lookup"><span data-stu-id="52aa2-131">Payload output</span></span>               |
| <span data-ttu-id="52aa2-132">主要類型</span><span class="sxs-lookup"><span data-stu-id="52aa2-132">Major Type</span></span>       | <span data-ttu-id="52aa2-133">媒體媒體的 \_ MPEG2 \_ pe</span><span class="sxs-lookup"><span data-stu-id="52aa2-133">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="52aa2-134">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="52aa2-134">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="52aa2-135">Subtype</span><span class="sxs-lookup"><span data-stu-id="52aa2-135">Subtype</span></span>          | <span data-ttu-id="52aa2-136">MEDIASUBTYPE \_ 杜 \_ AC3</span><span class="sxs-lookup"><span data-stu-id="52aa2-136">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="52aa2-137">**MEDIASUBTYPE \_ 杜 \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="52aa2-137">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="52aa2-138">格式類型</span><span class="sxs-lookup"><span data-stu-id="52aa2-138">Format Type</span></span>      | <span data-ttu-id="52aa2-139">格式 \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="52aa2-139">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="52aa2-140">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="52aa2-140">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="52aa2-141">格式結構</span><span class="sxs-lookup"><span data-stu-id="52aa2-141">Format Structure</span></span> | <span data-ttu-id="52aa2-142">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="52aa2-142">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="52aa2-143">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="52aa2-143">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="52aa2-144">適用于 AC-3 的 **WAVEFORMATEX** 結構的 **wFormatTag** 成員目前為 **WAVE \_ 格式 \_ 未知**，但這可能會變更。</span><span class="sxs-lookup"><span data-stu-id="52aa2-144">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="52aa2-145">MPEG-2 音訊</span><span class="sxs-lookup"><span data-stu-id="52aa2-145">MPEG-2 Audio</span></span>

<span data-ttu-id="52aa2-146">針對 MPEG-2 音訊，媒體類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="52aa2-146">For MPEG-2 audio, the media types are as follows.</span></span>



| <span data-ttu-id="52aa2-147">標籤</span><span class="sxs-lookup"><span data-stu-id="52aa2-147">Label</span></span> | <span data-ttu-id="52aa2-148">值</span><span class="sxs-lookup"><span data-stu-id="52aa2-148">Value</span></span> |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="52aa2-149">PE 輸出</span><span class="sxs-lookup"><span data-stu-id="52aa2-149">PES output</span></span>                    | <span data-ttu-id="52aa2-150">承載輸出</span><span class="sxs-lookup"><span data-stu-id="52aa2-150">Payload output</span></span>                 |
| <span data-ttu-id="52aa2-151">主要類型</span><span class="sxs-lookup"><span data-stu-id="52aa2-151">Major Type</span></span>       | <span data-ttu-id="52aa2-152">**媒體媒體的 \_ MPEG2 \_ pe**</span><span class="sxs-lookup"><span data-stu-id="52aa2-152">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="52aa2-153">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="52aa2-153">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="52aa2-154">Subtype</span><span class="sxs-lookup"><span data-stu-id="52aa2-154">Subtype</span></span>          | <span data-ttu-id="52aa2-155">**MEDIASUBTYE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="52aa2-155">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="52aa2-156">**MEDIASUBTYPE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="52aa2-156">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="52aa2-157">格式類型</span><span class="sxs-lookup"><span data-stu-id="52aa2-157">Format Type</span></span>      | <span data-ttu-id="52aa2-158">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="52aa2-158">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="52aa2-159">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="52aa2-159">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="52aa2-160">格式結構</span><span class="sxs-lookup"><span data-stu-id="52aa2-160">Format Structure</span></span> | <span data-ttu-id="52aa2-161">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="52aa2-161">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="52aa2-162">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="52aa2-162">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="52aa2-163">MPEG-2 音訊的 **WAVEFORMATEX** 結構的 **wFormatTag** 成員目前為 **WAVE \_ 格式 \_ 未知**，但這可能會變更。</span><span class="sxs-lookup"><span data-stu-id="52aa2-163">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="52aa2-164">MPEG-2 分割器會假設串流 D0 至 DF 是用於多重通道擴充資料流程，因為它們適用于 DVD MPEG-2 音訊。</span><span class="sxs-lookup"><span data-stu-id="52aa2-164">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="52aa2-165">因此，每當選取資料流程 C *x* 時，分隔器也會轉送串流 D *x* 的封包。</span><span class="sxs-lookup"><span data-stu-id="52aa2-165">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="52aa2-166">LPCM 音訊</span><span class="sxs-lookup"><span data-stu-id="52aa2-166">LPCM Audio</span></span>

<span data-ttu-id="52aa2-167">針對 LPCM 音訊，媒體類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="52aa2-167">For LPCM audio, the media types are as follows.</span></span>



| <span data-ttu-id="52aa2-168">標籤</span><span class="sxs-lookup"><span data-stu-id="52aa2-168">Label</span></span> | <span data-ttu-id="52aa2-169">值</span><span class="sxs-lookup"><span data-stu-id="52aa2-169">Value</span></span> |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="52aa2-170">PE 輸出</span><span class="sxs-lookup"><span data-stu-id="52aa2-170">PES output</span></span>                         | <span data-ttu-id="52aa2-171">承載輸出</span><span class="sxs-lookup"><span data-stu-id="52aa2-171">Payload output</span></span>                     |
| <span data-ttu-id="52aa2-172">主要類型</span><span class="sxs-lookup"><span data-stu-id="52aa2-172">Major Type</span></span>       | <span data-ttu-id="52aa2-173">**媒體媒體的 \_ MPEG2 \_ pe**</span><span class="sxs-lookup"><span data-stu-id="52aa2-173">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="52aa2-174">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="52aa2-174">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="52aa2-175">Subtype</span><span class="sxs-lookup"><span data-stu-id="52aa2-175">Subtype</span></span>          | <span data-ttu-id="52aa2-176">**MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="52aa2-176">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="52aa2-177">**MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="52aa2-177">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="52aa2-178">格式類型</span><span class="sxs-lookup"><span data-stu-id="52aa2-178">Format Type</span></span>      | <span data-ttu-id="52aa2-179">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="52aa2-179">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="52aa2-180">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="52aa2-180">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="52aa2-181">格式結構</span><span class="sxs-lookup"><span data-stu-id="52aa2-181">Format Structure</span></span> | <span data-ttu-id="52aa2-182">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="52aa2-182">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="52aa2-183">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="52aa2-183">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="52aa2-184">**WAVEFORMATEX** 結構的 LPCM 音訊 **wFormatTag** 成員目前為 **WAVE \_ 格式 \_ 未知**，但這可能會變更。</span><span class="sxs-lookup"><span data-stu-id="52aa2-184">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52aa2-185">相關主題</span><span class="sxs-lookup"><span data-stu-id="52aa2-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52aa2-186">MPEG-2 媒體類型</span><span class="sxs-lookup"><span data-stu-id="52aa2-186">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
