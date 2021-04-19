---
description: MPEG-2 分隔器媒體類型
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: MPEG-2 分隔器媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb10310bd126346c8e1558801200682792836d92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106975596"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="df51d-103">MPEG-2 分隔器媒體類型</span><span class="sxs-lookup"><span data-stu-id="df51d-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="df51d-104">[Mpeg-2 分隔](mpeg-2-splitter.md)器篩選器目前支援音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="df51d-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="df51d-105">由 DVD 定義的子串流支援杜比 AC-3。</span><span class="sxs-lookup"><span data-stu-id="df51d-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="df51d-106">篩選準則也支援 MPEG-2 音訊。</span><span class="sxs-lookup"><span data-stu-id="df51d-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="df51d-107">媒體類型取決於 MPEG-2 分隔器是否提供 PE 封包或 PE 承載。</span><span class="sxs-lookup"><span data-stu-id="df51d-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="df51d-108">影片</span><span class="sxs-lookup"><span data-stu-id="df51d-108">Video</span></span>

<span data-ttu-id="df51d-109">針對 MPEG-2 影片，媒體類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="df51d-109">For MPEG-2 video, the media types are as follows.</span></span>



|                  |                                          |                                |
|------------------|------------------------------------------|--------------------------------|
|                  | <span data-ttu-id="df51d-110">PE 輸出</span><span class="sxs-lookup"><span data-stu-id="df51d-110">PES output</span></span>                               | <span data-ttu-id="df51d-111">承載輸出</span><span class="sxs-lookup"><span data-stu-id="df51d-111">Payload output</span></span>                 |
| <span data-ttu-id="df51d-112">主要類型</span><span class="sxs-lookup"><span data-stu-id="df51d-112">Major Type</span></span>       | <span data-ttu-id="df51d-113">**媒體媒體的 \_ MPEG2 \_ pe**</span><span class="sxs-lookup"><span data-stu-id="df51d-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="df51d-114">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="df51d-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="df51d-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="df51d-115">Subtype</span></span>          | <span data-ttu-id="df51d-116">**MEDIASUBTYPE \_ MPEG2 \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="df51d-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="df51d-117">**MEDIASUBTYPE \_ MPEG2 \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="df51d-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="df51d-118">格式類型</span><span class="sxs-lookup"><span data-stu-id="df51d-118">Format Type</span></span>      | <span data-ttu-id="df51d-119">**格式 \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="df51d-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="df51d-120">**格式 \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="df51d-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="df51d-121">格式結構</span><span class="sxs-lookup"><span data-stu-id="df51d-121">Format Structure</span></span> | [<span data-ttu-id="df51d-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="df51d-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="df51d-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="df51d-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="df51d-124">AC-3 音訊</span><span class="sxs-lookup"><span data-stu-id="df51d-124">AC-3 Audio</span></span>

<span data-ttu-id="df51d-125">針對 AC 3 音訊，媒體類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="df51d-125">For AC-3 audio, the media types are as follows.</span></span>



|                  |                                      |                              |
|------------------|--------------------------------------|------------------------------|
|                  | <span data-ttu-id="df51d-126">PE 輸出</span><span class="sxs-lookup"><span data-stu-id="df51d-126">PES output</span></span>                           | <span data-ttu-id="df51d-127">承載輸出</span><span class="sxs-lookup"><span data-stu-id="df51d-127">Payload output</span></span>               |
| <span data-ttu-id="df51d-128">主要類型</span><span class="sxs-lookup"><span data-stu-id="df51d-128">Major Type</span></span>       | <span data-ttu-id="df51d-129">媒體媒體的 \_ MPEG2 \_ pe</span><span class="sxs-lookup"><span data-stu-id="df51d-129">MEDIATYPE\_MPEG2\_PES</span></span>                | <span data-ttu-id="df51d-130">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="df51d-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="df51d-131">Subtype</span><span class="sxs-lookup"><span data-stu-id="df51d-131">Subtype</span></span>          | <span data-ttu-id="df51d-132">MEDIASUBTYPE \_ 杜 \_ AC3</span><span class="sxs-lookup"><span data-stu-id="df51d-132">MEDIASUBTYPE\_DOLBY\_AC3</span></span>             | <span data-ttu-id="df51d-133">**MEDIASUBTYPE \_ 杜 \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="df51d-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="df51d-134">格式類型</span><span class="sxs-lookup"><span data-stu-id="df51d-134">Format Type</span></span>      | <span data-ttu-id="df51d-135">格式 \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="df51d-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="df51d-136">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="df51d-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="df51d-137">格式結構</span><span class="sxs-lookup"><span data-stu-id="df51d-137">Format Structure</span></span> | <span data-ttu-id="df51d-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="df51d-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="df51d-139">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="df51d-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="df51d-140">適用于 AC-3 的 **WAVEFORMATEX** 結構的 **wFormatTag** 成員目前為 **WAVE \_ 格式 \_ 未知**，但這可能會變更。</span><span class="sxs-lookup"><span data-stu-id="df51d-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="df51d-141">MPEG-2 音訊</span><span class="sxs-lookup"><span data-stu-id="df51d-141">MPEG-2 Audio</span></span>

<span data-ttu-id="df51d-142">針對 MPEG-2 音訊，媒體類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="df51d-142">For MPEG-2 audio, the media types are as follows.</span></span>



|                  |                               |                                |
|------------------|-------------------------------|--------------------------------|
|                  | <span data-ttu-id="df51d-143">PE 輸出</span><span class="sxs-lookup"><span data-stu-id="df51d-143">PES output</span></span>                    | <span data-ttu-id="df51d-144">承載輸出</span><span class="sxs-lookup"><span data-stu-id="df51d-144">Payload output</span></span>                 |
| <span data-ttu-id="df51d-145">主要類型</span><span class="sxs-lookup"><span data-stu-id="df51d-145">Major Type</span></span>       | <span data-ttu-id="df51d-146">**媒體媒體的 \_ MPEG2 \_ pe**</span><span class="sxs-lookup"><span data-stu-id="df51d-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="df51d-147">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="df51d-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="df51d-148">Subtype</span><span class="sxs-lookup"><span data-stu-id="df51d-148">Subtype</span></span>          | <span data-ttu-id="df51d-149">**MEDIASUBTYE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="df51d-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="df51d-150">**MEDIASUBTYPE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="df51d-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="df51d-151">格式類型</span><span class="sxs-lookup"><span data-stu-id="df51d-151">Format Type</span></span>      | <span data-ttu-id="df51d-152">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="df51d-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="df51d-153">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="df51d-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="df51d-154">格式結構</span><span class="sxs-lookup"><span data-stu-id="df51d-154">Format Structure</span></span> | <span data-ttu-id="df51d-155">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="df51d-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="df51d-156">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="df51d-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="df51d-157">MPEG-2 音訊的 **WAVEFORMATEX** 結構的 **wFormatTag** 成員目前為 **WAVE \_ 格式 \_ 未知**，但這可能會變更。</span><span class="sxs-lookup"><span data-stu-id="df51d-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="df51d-158">MPEG-2 分割器會假設串流 D0 至 DF 是用於多重通道擴充資料流程，因為它們適用于 DVD MPEG-2 音訊。</span><span class="sxs-lookup"><span data-stu-id="df51d-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="df51d-159">因此，每當選取資料流程 C *x* 時，分隔器也會轉送串流 D *x* 的封包。</span><span class="sxs-lookup"><span data-stu-id="df51d-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="df51d-160">LPCM 音訊</span><span class="sxs-lookup"><span data-stu-id="df51d-160">LPCM Audio</span></span>

<span data-ttu-id="df51d-161">針對 LPCM 音訊，媒體類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="df51d-161">For LPCM audio, the media types are as follows.</span></span>



|                  |                                    |                                    |
|------------------|------------------------------------|------------------------------------|
|                  | <span data-ttu-id="df51d-162">PE 輸出</span><span class="sxs-lookup"><span data-stu-id="df51d-162">PES output</span></span>                         | <span data-ttu-id="df51d-163">承載輸出</span><span class="sxs-lookup"><span data-stu-id="df51d-163">Payload output</span></span>                     |
| <span data-ttu-id="df51d-164">主要類型</span><span class="sxs-lookup"><span data-stu-id="df51d-164">Major Type</span></span>       | <span data-ttu-id="df51d-165">**媒體媒體的 \_ MPEG2 \_ pe**</span><span class="sxs-lookup"><span data-stu-id="df51d-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="df51d-166">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="df51d-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="df51d-167">Subtype</span><span class="sxs-lookup"><span data-stu-id="df51d-167">Subtype</span></span>          | <span data-ttu-id="df51d-168">**MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="df51d-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="df51d-169">**MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="df51d-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="df51d-170">格式類型</span><span class="sxs-lookup"><span data-stu-id="df51d-170">Format Type</span></span>      | <span data-ttu-id="df51d-171">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="df51d-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="df51d-172">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="df51d-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="df51d-173">格式結構</span><span class="sxs-lookup"><span data-stu-id="df51d-173">Format Structure</span></span> | <span data-ttu-id="df51d-174">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="df51d-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="df51d-175">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="df51d-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="df51d-176">**WAVEFORMATEX** 結構的 LPCM 音訊 **wFormatTag** 成員目前為 **WAVE \_ 格式 \_ 未知**，但這可能會變更。</span><span class="sxs-lookup"><span data-stu-id="df51d-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df51d-177">相關主題</span><span class="sxs-lookup"><span data-stu-id="df51d-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df51d-178">MPEG-2 媒體類型</span><span class="sxs-lookup"><span data-stu-id="df51d-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
