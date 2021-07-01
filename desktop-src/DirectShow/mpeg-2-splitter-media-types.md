---
description: MPEG-2 分隔器媒體類型
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: MPEG-2 分隔器媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4e025fafabdeb8c437cc1d1cd6fbb843cf63e3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119973"
---
# <a name="mpeg-2-splitter-media-types"></a><span data-ttu-id="723fb-103">MPEG-2 分隔器媒體類型</span><span class="sxs-lookup"><span data-stu-id="723fb-103">MPEG-2 Splitter Media Types</span></span>

<span data-ttu-id="723fb-104">[Mpeg-2 分隔](mpeg-2-splitter.md)器篩選器目前支援音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="723fb-104">The [MPEG-2 Splitter](mpeg-2-splitter.md) filter currently supports audio and video.</span></span> <span data-ttu-id="723fb-105">由 DVD 定義的子串流支援杜比 AC-3。</span><span class="sxs-lookup"><span data-stu-id="723fb-105">Dolby AC-3 is supported as a substream as defined by DVD.</span></span> <span data-ttu-id="723fb-106">篩選準則也支援 MPEG-2 音訊。</span><span class="sxs-lookup"><span data-stu-id="723fb-106">The filter also supports MPEG-2 audio.</span></span> <span data-ttu-id="723fb-107">媒體類型取決於 MPEG-2 分隔器是否提供 PE 封包或 PE 承載。</span><span class="sxs-lookup"><span data-stu-id="723fb-107">The media types depend on whether the MPEG-2 splitter is delivering PES packets or PES payloads.</span></span>

### <a name="video"></a><span data-ttu-id="723fb-108">影片</span><span class="sxs-lookup"><span data-stu-id="723fb-108">Video</span></span>

<span data-ttu-id="723fb-109">針對 MPEG-2 影片，媒體類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="723fb-109">For MPEG-2 video, the media types are as follows.</span></span>


|                | <span data-ttu-id="723fb-110">PE 輸出</span><span class="sxs-lookup"><span data-stu-id="723fb-110">PES output</span></span> | <span data-ttu-id="723fb-111">承載輸出</span><span class="sxs-lookup"><span data-stu-id="723fb-111">Payload output</span></span>
|------------------|------------------------------------------|--------------------------------|
| <span data-ttu-id="723fb-112">**主要類型**</span><span class="sxs-lookup"><span data-stu-id="723fb-112">**Major type**</span></span>       | <span data-ttu-id="723fb-113">**媒體媒體的 \_ MPEG2 \_ pe**</span><span class="sxs-lookup"><span data-stu-id="723fb-113">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="723fb-114">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="723fb-114">**MEDIATYPE\_Video**</span></span>           |
| <span data-ttu-id="723fb-115">**亞**</span><span class="sxs-lookup"><span data-stu-id="723fb-115">**Subtype**</span></span>          | <span data-ttu-id="723fb-116">**MEDIASUBTYPE \_ MPEG2 \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="723fb-116">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           | <span data-ttu-id="723fb-117">**MEDIASUBTYPE \_ MPEG2 \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="723fb-117">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span> |
| <span data-ttu-id="723fb-118">**格式類型**</span><span class="sxs-lookup"><span data-stu-id="723fb-118">**Format type**</span></span>      | <span data-ttu-id="723fb-119">**格式 \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="723fb-119">**FORMAT\_MPEG2Video**</span></span>                   | <span data-ttu-id="723fb-120">**格式 \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="723fb-120">**FORMAT\_MPEG2Video**</span></span>         |
| <span data-ttu-id="723fb-121">**格式結構**</span><span class="sxs-lookup"><span data-stu-id="723fb-121">**Format structure**</span></span> | [<span data-ttu-id="723fb-122">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="723fb-122">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | <span data-ttu-id="723fb-123">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="723fb-123">**MPEG2VIDEOINFO**</span></span>             |



 

### <a name="ac-3-audio"></a><span data-ttu-id="723fb-124">AC-3 音訊</span><span class="sxs-lookup"><span data-stu-id="723fb-124">AC-3 Audio</span></span>

<span data-ttu-id="723fb-125">針對 AC 3 音訊，媒體類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="723fb-125">For AC-3 audio, the media types are as follows.</span></span>

| | <span data-ttu-id="723fb-126">PE 輸出</span><span class="sxs-lookup"><span data-stu-id="723fb-126">PES output</span></span> | <span data-ttu-id="723fb-127">承載輸出</span><span class="sxs-lookup"><span data-stu-id="723fb-127">Payload output</span></span> |
|------------------|--------------------------------------|------------------------------|
| <span data-ttu-id="723fb-128">**主要類型**</span><span class="sxs-lookup"><span data-stu-id="723fb-128">**Major type**</span></span>       | <span data-ttu-id="723fb-129">**媒體媒體的 \_ MPEG2 \_ pe**</span><span class="sxs-lookup"><span data-stu-id="723fb-129">**MEDIATYPE\_MPEG2\_PES**</span></span>                | <span data-ttu-id="723fb-130">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="723fb-130">**MEDIATYPE\_Audio**</span></span>         |
| <span data-ttu-id="723fb-131">**亞**</span><span class="sxs-lookup"><span data-stu-id="723fb-131">**Subtype**</span></span>          | <span data-ttu-id="723fb-132">**MEDIASUBTYPE \_ 杜 \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="723fb-132">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>             | <span data-ttu-id="723fb-133">**MEDIASUBTYPE \_ 杜 \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="723fb-133">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span> |
| <span data-ttu-id="723fb-134">**格式類型**</span><span class="sxs-lookup"><span data-stu-id="723fb-134">**Format type**</span></span>      | <span data-ttu-id="723fb-135">格式 \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="723fb-135">FORMAT\_WaveFormatEx</span></span>                 | <span data-ttu-id="723fb-136">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="723fb-136">**FORMAT\_WaveFormatEx**</span></span>     |
| <span data-ttu-id="723fb-137">**格式結構**</span><span class="sxs-lookup"><span data-stu-id="723fb-137">**Format structure**</span></span> | <span data-ttu-id="723fb-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="723fb-138">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="723fb-139">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="723fb-139">**WAVEFORMATEX**</span></span>             |



 

<span data-ttu-id="723fb-140">適用于 AC-3 的 **WAVEFORMATEX** 結構的 **wFormatTag** 成員目前為 **WAVE \_ 格式 \_ 未知**，但這可能會變更。</span><span class="sxs-lookup"><span data-stu-id="723fb-140">The **WAVEFORMATEX** structure's **wFormatTag** member for AC-3 is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

### <a name="mpeg-2-audio"></a><span data-ttu-id="723fb-141">MPEG-2 音訊</span><span class="sxs-lookup"><span data-stu-id="723fb-141">MPEG-2 Audio</span></span>

<span data-ttu-id="723fb-142">針對 MPEG-2 音訊，媒體類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="723fb-142">For MPEG-2 audio, the media types are as follows.</span></span>



|  | <span data-ttu-id="723fb-143">PE 輸出</span><span class="sxs-lookup"><span data-stu-id="723fb-143">PES output</span></span> | <span data-ttu-id="723fb-144">承載輸出</span><span class="sxs-lookup"><span data-stu-id="723fb-144">Payload output</span></span> |
|------------------|-------------------------------|--------------------------------|
| <span data-ttu-id="723fb-145">**主要類型**</span><span class="sxs-lookup"><span data-stu-id="723fb-145">**Major type**</span></span>       | <span data-ttu-id="723fb-146">**媒體媒體的 \_ MPEG2 \_ pe**</span><span class="sxs-lookup"><span data-stu-id="723fb-146">**MEDIATYPE\_MPEG2\_PES**</span></span>     | <span data-ttu-id="723fb-147">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="723fb-147">**MEDIATYPE\_Audio**</span></span>           |
| <span data-ttu-id="723fb-148">**亞**</span><span class="sxs-lookup"><span data-stu-id="723fb-148">**Subtype**</span></span>          | <span data-ttu-id="723fb-149">**MEDIASUBTYE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="723fb-149">**MEDIASUBTYE\_MPEG2\_AUDIO**</span></span> | <span data-ttu-id="723fb-150">**MEDIASUBTYPE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="723fb-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span> |
| <span data-ttu-id="723fb-151">**格式類型**</span><span class="sxs-lookup"><span data-stu-id="723fb-151">**Format type**</span></span>      | <span data-ttu-id="723fb-152">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="723fb-152">**FORMAT\_WaveFormatEx**</span></span>      | <span data-ttu-id="723fb-153">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="723fb-153">**FORMAT\_WaveFormatEx**</span></span>       |
| <span data-ttu-id="723fb-154">**格式結構**</span><span class="sxs-lookup"><span data-stu-id="723fb-154">**Format structure**</span></span> | <span data-ttu-id="723fb-155">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="723fb-155">**WAVEFORMATEX**</span></span>              | <span data-ttu-id="723fb-156">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="723fb-156">**WAVEFORMATEX**</span></span>               |



 

<span data-ttu-id="723fb-157">MPEG-2 音訊的 **WAVEFORMATEX** 結構的 **wFormatTag** 成員目前為 **WAVE \_ 格式 \_ 未知**，但這可能會變更。</span><span class="sxs-lookup"><span data-stu-id="723fb-157">The **WAVEFORMATEX** structure's **wFormatTag** member for MPEG-2 Audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

<span data-ttu-id="723fb-158">MPEG-2 分割器會假設串流 D0 至 DF 是用於多重通道擴充資料流程，因為它們適用于 DVD MPEG-2 音訊。</span><span class="sxs-lookup"><span data-stu-id="723fb-158">The MPEG-2 Splitter assumes that streams D0 through DF are used for the multichannel extension stream, as they are for DVD MPEG-2 audio.</span></span> <span data-ttu-id="723fb-159">因此，每當選取資料流程 C *x* 時，分隔器也會轉送串流 D *x* 的封包。</span><span class="sxs-lookup"><span data-stu-id="723fb-159">Therefore, whenever stream C *x* is selected, the splitter forwards the packets for stream D *x* as well.</span></span>

### <a name="lpcm-audio"></a><span data-ttu-id="723fb-160">LPCM 音訊</span><span class="sxs-lookup"><span data-stu-id="723fb-160">LPCM Audio</span></span>

<span data-ttu-id="723fb-161">針對 LPCM 音訊，媒體類型如下所示。</span><span class="sxs-lookup"><span data-stu-id="723fb-161">For LPCM audio, the media types are as follows.</span></span>



|  | <span data-ttu-id="723fb-162">PE 輸出</span><span class="sxs-lookup"><span data-stu-id="723fb-162">PES output</span></span> | <span data-ttu-id="723fb-163">承載輸出</span><span class="sxs-lookup"><span data-stu-id="723fb-163">Payload output</span></span> |
|------------------|------------------------------------|------------------------------------|
| <span data-ttu-id="723fb-164">**主要類型**</span><span class="sxs-lookup"><span data-stu-id="723fb-164">**Major type**</span></span>       | <span data-ttu-id="723fb-165">**媒體媒體的 \_ MPEG2 \_ pe**</span><span class="sxs-lookup"><span data-stu-id="723fb-165">**MEDIATYPE\_MPEG2\_PES**</span></span>          | <span data-ttu-id="723fb-166">**媒體 \_ 媒體**</span><span class="sxs-lookup"><span data-stu-id="723fb-166">**MEDIATYPE\_Audio**</span></span>               |
| <span data-ttu-id="723fb-167">**亞**</span><span class="sxs-lookup"><span data-stu-id="723fb-167">**Subtype**</span></span>          | <span data-ttu-id="723fb-168">**MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="723fb-168">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> | <span data-ttu-id="723fb-169">**MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="723fb-169">**MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span> |
| <span data-ttu-id="723fb-170">**格式類型**</span><span class="sxs-lookup"><span data-stu-id="723fb-170">**Format type**</span></span>      | <span data-ttu-id="723fb-171">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="723fb-171">**FORMAT\_WaveFormatEx**</span></span>           | <span data-ttu-id="723fb-172">**格式 \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="723fb-172">**FORMAT\_WaveFormatEx**</span></span>           |
| <span data-ttu-id="723fb-173">**格式結構**</span><span class="sxs-lookup"><span data-stu-id="723fb-173">**Format structure**</span></span> | <span data-ttu-id="723fb-174">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="723fb-174">**WAVEFORMATEX**</span></span>                   | <span data-ttu-id="723fb-175">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="723fb-175">**WAVEFORMATEX**</span></span>                   |



 

<span data-ttu-id="723fb-176">**WAVEFORMATEX** 結構的 LPCM 音訊 **wFormatTag** 成員目前為 **WAVE \_ 格式 \_ 未知**，但這可能會變更。</span><span class="sxs-lookup"><span data-stu-id="723fb-176">The **WAVEFORMATEX** structure's **wFormatTag** member for LPCM audio is currently **WAVE\_FORMAT\_UNKNOWN**, but this might change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="723fb-177">相關主題</span><span class="sxs-lookup"><span data-stu-id="723fb-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="723fb-178">MPEG-2 媒體類型</span><span class="sxs-lookup"><span data-stu-id="723fb-178">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
