---
description: 本主題說明如何在媒體基礎中指定 Advanced Audio 編碼 (AAC) 資料流程的格式。
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: AAC 媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95423b26a0e2a327b599011e88a05ab2ab58c5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945593"
---
# <a name="aac-media-types"></a><span data-ttu-id="2bef8-103">AAC 媒體類型</span><span class="sxs-lookup"><span data-stu-id="2bef8-103">AAC Media Types</span></span>

<span data-ttu-id="2bef8-104">本主題說明如何在媒體基礎中指定 Advanced Audio 編碼 (AAC) 資料流程的格式。</span><span class="sxs-lookup"><span data-stu-id="2bef8-104">This topic describes how to specify the format of an Advanced Audio Coding (AAC) stream in Media Foundation.</span></span>

<span data-ttu-id="2bef8-105">針對 AAC 音訊定義了兩個子類型：</span><span class="sxs-lookup"><span data-stu-id="2bef8-105">Two subtypes are defined for AAC audio:</span></span>



| <span data-ttu-id="2bef8-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="2bef8-106">Subtype</span></span>                     | <span data-ttu-id="2bef8-107">描述</span><span class="sxs-lookup"><span data-stu-id="2bef8-107">Description</span></span>          | <span data-ttu-id="2bef8-108">標頭</span><span class="sxs-lookup"><span data-stu-id="2bef8-108">Header</span></span>       |
|-----------------------------|----------------------|--------------|
| <span data-ttu-id="2bef8-109">**MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="2bef8-109">**MFAudioFormat\_AAC**</span></span>      | <span data-ttu-id="2bef8-110">Raw AAC 或 ADTS AAC。</span><span class="sxs-lookup"><span data-stu-id="2bef8-110">Raw AAC or ADTS AAC.</span></span> | <span data-ttu-id="2bef8-111">mfapi。h</span><span class="sxs-lookup"><span data-stu-id="2bef8-111">mfapi.h</span></span>      |
| <span data-ttu-id="2bef8-112">**MEDIASUBTYPE \_ 原始 \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="2bef8-112">**MEDIASUBTYPE\_RAW\_AAC1**</span></span> | <span data-ttu-id="2bef8-113">原始 AAC。</span><span class="sxs-lookup"><span data-stu-id="2bef8-113">Raw AAC.</span></span>             | <span data-ttu-id="2bef8-114">wmcodecdsp。h</span><span class="sxs-lookup"><span data-stu-id="2bef8-114">wmcodecdsp.h</span></span> |



 

<dl> <dt>

<span data-ttu-id="2bef8-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat \_ AAC</span><span class="sxs-lookup"><span data-stu-id="2bef8-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat\_AAC</span></span>
</dt> <dd>

<span data-ttu-id="2bef8-116">針對此子類型，媒體類型會在應用光譜頻內複寫 (.SBR) 和參數身歷聲 (PS) 工具（如果有的話）之前，提供取樣率和通道數目。</span><span class="sxs-lookup"><span data-stu-id="2bef8-116">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="2bef8-117">.SBR 工具的效果是將已解碼的取樣率加倍，相對於 core AAC-LC 取樣率。</span><span class="sxs-lookup"><span data-stu-id="2bef8-117">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="2bef8-118">PS 工具的效果是從 mono 通道核心 AAC-LC 串流解碼身歷聲。</span><span class="sxs-lookup"><span data-stu-id="2bef8-118">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span>

<span data-ttu-id="2bef8-119">此子類型相當於 **MEDIASUBTYPE \_ MPEG \_ HEAAC**，定義于 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="2bef8-119">This subtype is equivalent to **MEDIASUBTYPE\_MPEG\_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="2bef8-120">請參閱 [音訊子類型 guid](audio-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="2bef8-120">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bef8-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE \_ 原始 \_ AAC1</span><span class="sxs-lookup"><span data-stu-id="2bef8-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE\_RAW\_AAC1</span></span>
</dt> <dd>

<span data-ttu-id="2bef8-122">這個子類型是用於包含在 AVI 檔案中的 AAC，且其音訊格式標記等於 WAVE \_ 格式的 \_ RAW \_ AAC1 (0x00FF) 。</span><span class="sxs-lookup"><span data-stu-id="2bef8-122">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE\_FORMAT\_RAW\_AAC1 (0x00FF).</span></span>

<span data-ttu-id="2bef8-123">針對此子類型，媒體類型會提供套用 .SBR 和 PS 工具之後的取樣速率和通道數目（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2bef8-123">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span>

</dd> </dl>

<span data-ttu-id="2bef8-124">下列媒體類型屬性適用于 AAC 音訊。</span><span class="sxs-lookup"><span data-stu-id="2bef8-124">The following media type attributes apply to AAC audio.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bef8-125">屬性</span><span class="sxs-lookup"><span data-stu-id="2bef8-125">Attribute</span></span></th>
<th><span data-ttu-id="2bef8-126">描述</span><span class="sxs-lookup"><span data-stu-id="2bef8-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bef8-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bef8-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="2bef8-128">主要類型。</span><span class="sxs-lookup"><span data-stu-id="2bef8-128">Major type.</span></span> <span data-ttu-id="2bef8-129">必須是 <strong>MFMediaType_Audio</strong>。</span><span class="sxs-lookup"><span data-stu-id="2bef8-129">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bef8-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bef8-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="2bef8-131">音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="2bef8-131">Audio subtype.</span></span> <span data-ttu-id="2bef8-132">如需詳細資料，請參閱先前的描述。</span><span class="sxs-lookup"><span data-stu-id="2bef8-132">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bef8-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="2bef8-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="2bef8-134">音訊設定檔和層級。</span><span class="sxs-lookup"><span data-stu-id="2bef8-134">Audio profile and level.</span></span> <br/> <span data-ttu-id="2bef8-135">這個屬性的值是 <strong>audioProfileLevelIndication</strong> 欄位，如 ISO/IEC 14496-3 所定義。</span><span class="sxs-lookup"><span data-stu-id="2bef8-135">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span><br/> <span data-ttu-id="2bef8-136">如果不明，請將設定為零或 0xFE (&quot; 未指定任何音訊設定檔 &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="2bef8-136">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bef8-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bef8-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="2bef8-138">編碼 AAC 資料流程的位元速率（以每秒位元組數為單位）。</span><span class="sxs-lookup"><span data-stu-id="2bef8-138">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bef8-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="2bef8-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="2bef8-140">裝載類型。</span><span class="sxs-lookup"><span data-stu-id="2bef8-140">Payload type.</span></span><br/> <span data-ttu-id="2bef8-141">只適用于 <strong>MFAudioFormat_AAC</strong>。</span><span class="sxs-lookup"><span data-stu-id="2bef8-141">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span><br/> <span data-ttu-id="2bef8-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="2bef8-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="2bef8-143">如果未指定此屬性，則會使用預設值0，此值會指定資料流程只包含 raw_data_block 元素。</span><span class="sxs-lookup"><span data-stu-id="2bef8-143">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bef8-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bef8-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="2bef8-145">已解碼 PCM 音訊的位深度。</span><span class="sxs-lookup"><span data-stu-id="2bef8-145">Bit depth of the decoded PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bef8-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bef8-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="2bef8-147">將音訊頻道指派給喇叭位置。</span><span class="sxs-lookup"><span data-stu-id="2bef8-147">Assignment of audio channels to speaker positions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bef8-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bef8-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="2bef8-149">通道的數目，包括低頻率 (LFE) 通道（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2bef8-149">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/> <span data-ttu-id="2bef8-150">此值的解讀取決於媒體子類型，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="2bef8-150">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bef8-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bef8-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="2bef8-152">取樣率（以每秒樣本數為單位）。</span><span class="sxs-lookup"><span data-stu-id="2bef8-152">Sample rate, in samples per second.</span></span><br/> <span data-ttu-id="2bef8-153">此值的解讀取決於媒體子類型，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="2bef8-153">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bef8-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="2bef8-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="2bef8-155">這個屬性的值取決於子類型：</span><span class="sxs-lookup"><span data-stu-id="2bef8-155">The value of this attribute depends on the subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="2bef8-156"><strong>MFAudioFormat_AAC</strong>：包含在<strong>WAVEFORMATEX</strong>結構後面出現的部分<a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a>結構， (也就是<strong>wfx</strong>成員) 之後。</span><span class="sxs-lookup"><span data-stu-id="2bef8-156"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="2bef8-157">後面接著 AudioSpecificConfig () 資料，如 ISO/IEC 14496-3 所定義。</span><span class="sxs-lookup"><span data-stu-id="2bef8-157">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="2bef8-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>：包含 AudioSpecificConfig () 資料。</span><span class="sxs-lookup"><span data-stu-id="2bef8-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2bef8-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="2bef8-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bef8-160">音訊媒體類型</span><span class="sxs-lookup"><span data-stu-id="2bef8-160">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="2bef8-161">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="2bef8-161">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="2bef8-162">媒體基礎中的 MPEG 4 支援</span><span class="sxs-lookup"><span data-stu-id="2bef8-162">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="2bef8-163">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2bef8-163">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

