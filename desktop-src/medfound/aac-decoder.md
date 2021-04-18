---
description: Microsoft 媒體基礎的 AAC 解碼器是媒體基礎轉換，可將下列 Advanced 音訊編碼 (AAC) 和高效率 AAC (AAC) 設定檔：
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: AAC 解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82dde090dee98cddce9658366bde593b5fc779d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971392"
---
# <a name="aac-decoder"></a><span data-ttu-id="a8855-103">AAC 解碼器</span><span class="sxs-lookup"><span data-stu-id="a8855-103">AAC Decoder</span></span>

<span data-ttu-id="a8855-104">Microsoft 媒體基礎的 AAC 解碼器是 [媒體基礎轉換](media-foundation-transforms.md) ，可將下列 Advanced 音訊編碼 (AAC) 和高效率 AAC (AAC) 設定檔：</span><span class="sxs-lookup"><span data-stu-id="a8855-104">The Microsoft Media Foundation AAC decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes the following Advanced Audio Coding (AAC) and High Efficiency AAC (HE-AAC) profiles:</span></span>

-   <span data-ttu-id="a8855-105">MPEG-2 AAC 低複雜度 (LC) 設定檔 (多重通道) 。</span><span class="sxs-lookup"><span data-stu-id="a8855-105">MPEG-2 AAC Low Complexity (LC) profile (multichannel).</span></span>
-   <span data-ttu-id="a8855-106">MPEG-2 AAC v1 (多重通道) 搭配 AAC-LC 核心。</span><span class="sxs-lookup"><span data-stu-id="a8855-106">MPEG-4 HE-AAC v1 (multichannel) with AAC-LC core.</span></span>
-   <span data-ttu-id="a8855-107">使用 AAC-LC 核心的 MPEG-2 AAC v2 (身歷聲) 。</span><span class="sxs-lookup"><span data-stu-id="a8855-107">MPEG-4 HE-AAC v2 (stereo) with AAC-LC core.</span></span>

<span data-ttu-id="a8855-108">AAC 解碼器支援音訊資料傳輸串流中沒有標頭和 AAC 的原始 AAC 串流 (ADTS) 。</span><span class="sxs-lookup"><span data-stu-id="a8855-108">The AAC decoder supports both raw AAC streams with no headers and AAC in an audio data transport stream (ADTS).</span></span>

<span data-ttu-id="a8855-109">從 Windows 8 開始，AAC 解碼器也支援使用多工層來解碼 MPEG-2 音訊廣播串流， (LATM) 和同步處理層 (LOA) 。</span><span class="sxs-lookup"><span data-stu-id="a8855-109">Starting in Windows 8, the AAC decoder also supports decoding MPEG-4 audio transport streams with a multiplex layer (LATM) and synchronization layer (LOAS).</span></span> <span data-ttu-id="a8855-110">它也可以將 LATM/LOA 資料流程轉換為 ADTS。</span><span class="sxs-lookup"><span data-stu-id="a8855-110">It can also convert an LATM/LOAS stream to ADTS.</span></span>

## <a name="media-types"></a><span data-ttu-id="a8855-111">媒體類型</span><span class="sxs-lookup"><span data-stu-id="a8855-111">Media Types</span></span>

<span data-ttu-id="a8855-112">AAC 解碼器支援下列媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a8855-112">The AAC decoder supports the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="a8855-113">輸入類型</span><span class="sxs-lookup"><span data-stu-id="a8855-113">Input Types</span></span>

<span data-ttu-id="a8855-114">AAC 解碼器支援下列音訊子類型：</span><span class="sxs-lookup"><span data-stu-id="a8855-114">The AAC decoder supports the following audio subtypes:</span></span>



| <span data-ttu-id="a8855-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="a8855-115">Subtype</span></span>                     | <span data-ttu-id="a8855-116">描述</span><span class="sxs-lookup"><span data-stu-id="a8855-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="a8855-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a8855-117">Header</span></span>       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="a8855-118">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="a8855-118">**MFAudioFormat_AAC**</span></span>      | <span data-ttu-id="a8855-119">Raw AAC 或 ADTS AAC。</span><span class="sxs-lookup"><span data-stu-id="a8855-119">Raw AAC or ADTS AAC.</span></span><br/> <span data-ttu-id="a8855-120">針對此子類型，媒體類型會在應用光譜頻內複寫 (.SBR) 和參數身歷聲 (PS) 工具（如果有的話）之前，提供取樣率和通道數目。</span><span class="sxs-lookup"><span data-stu-id="a8855-120">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="a8855-121">.SBR 工具的效果是將已解碼的取樣率加倍，相對於 core AAC-LC 取樣率。</span><span class="sxs-lookup"><span data-stu-id="a8855-121">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="a8855-122">PS 工具的效果是從 mono 通道核心 AAC-LC 串流解碼身歷聲。</span><span class="sxs-lookup"><span data-stu-id="a8855-122">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span><br/> <span data-ttu-id="a8855-123">這個子類型相當於 wmcodecdsp 中定義的 **MEDIASUBTYPE_MPEG_HEAAC**。</span><span class="sxs-lookup"><span data-stu-id="a8855-123">This subtype is equivalent to **MEDIASUBTYPE_MPEG_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="a8855-124">請參閱 [音訊子類型 guid](audio-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="a8855-124">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> <br/> <span data-ttu-id="a8855-125">[Mpeg-2 檔案來源](mpeg-4-file-source.md)和 ADTS 剖析器會輸出此子類型。</span><span class="sxs-lookup"><span data-stu-id="a8855-125">The [MPEG-4 File Source](mpeg-4-file-source.md) and the ADTS Parser output this subtype.</span></span> <br/> | <span data-ttu-id="a8855-126">mfapi。h</span><span class="sxs-lookup"><span data-stu-id="a8855-126">mfapi.h</span></span>      |
| <span data-ttu-id="a8855-127">**MEDIASUBTYPE_RAW_AAC1**</span><span class="sxs-lookup"><span data-stu-id="a8855-127">**MEDIASUBTYPE_RAW_AAC1**</span></span> | <span data-ttu-id="a8855-128">原始 AAC。</span><span class="sxs-lookup"><span data-stu-id="a8855-128">Raw AAC.</span></span> <br/> <span data-ttu-id="a8855-129">此子類型是用於包含在 AAC 中，且音訊格式標記等於 WAVE_FORMAT_RAW_AAC1 (0x00FF) 的 AVI 檔案中的。</span><span class="sxs-lookup"><span data-stu-id="a8855-129">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE_FORMAT_RAW_AAC1 (0x00FF).</span></span> <br/> <span data-ttu-id="a8855-130">針對此子類型，媒體類型會提供套用 .SBR 和 PS 工具之後的取樣速率和通道數目（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a8855-130">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="a8855-131">wmcodecdsp。h</span><span class="sxs-lookup"><span data-stu-id="a8855-131">wmcodecdsp.h</span></span> |



 

<span data-ttu-id="a8855-132">若要設定 AAC 解碼器，請在輸入媒體類型上設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a8855-132">To configure the AAC decoder, set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a8855-133">屬性</span><span class="sxs-lookup"><span data-stu-id="a8855-133">Attribute</span></span></th>
<th><span data-ttu-id="a8855-134">描述</span><span class="sxs-lookup"><span data-stu-id="a8855-134">Description</span></span></th>
<th><span data-ttu-id="a8855-135">備註</span><span class="sxs-lookup"><span data-stu-id="a8855-135">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a8855-136"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8855-136"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="a8855-137">主要類型。</span><span class="sxs-lookup"><span data-stu-id="a8855-137">Major type.</span></span></td>
<td><span data-ttu-id="a8855-138">必須是 <strong>MFMediaType_Audio</strong>。</span><span class="sxs-lookup"><span data-stu-id="a8855-138">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8855-139"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8855-139"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="a8855-140">音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="a8855-140">Audio subtype.</span></span></td>
<td><span data-ttu-id="a8855-141">如需詳細資料，請參閱先前的描述。</span><span class="sxs-lookup"><span data-stu-id="a8855-141">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8855-142"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="a8855-142"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="a8855-143">音訊設定檔和層級。</span><span class="sxs-lookup"><span data-stu-id="a8855-143">Audio profile and level.</span></span> <br/></td>
<td><span data-ttu-id="a8855-144">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a8855-144">Optional.</span></span> <span data-ttu-id="a8855-145">只適用于 <strong>MFAudioFormat_AAC</strong>。</span><span class="sxs-lookup"><span data-stu-id="a8855-145">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <br/> <span data-ttu-id="a8855-146">這個屬性的值是 <strong>audioProfileLevelIndication</strong> 欄位，如 ISO/IEC 14496-3 所定義。</span><span class="sxs-lookup"><span data-stu-id="a8855-146">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span> <br/> <span data-ttu-id="a8855-147">如果不明，請將設定為零或 0xFE (&quot; 未指定任何音訊設定檔 &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="a8855-147">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8855-148"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="a8855-148"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="a8855-149">裝載類型。</span><span class="sxs-lookup"><span data-stu-id="a8855-149">Payload type.</span></span><br/></td>
<td><span data-ttu-id="a8855-150">只適用于 <strong>MFAudioFormat_AAC</strong>。</span><span class="sxs-lookup"><span data-stu-id="a8855-150">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <span data-ttu-id="a8855-151">此解碼器支援下列承載類型：</span><span class="sxs-lookup"><span data-stu-id="a8855-151">The decoder supports the following payload types:</span></span> <br/>
<ul>
<li><span data-ttu-id="a8855-152">0：原始 AAC。</span><span class="sxs-lookup"><span data-stu-id="a8855-152">0: Raw AAC.</span></span> <span data-ttu-id="a8855-153">資料流程只包含 raw_data_block 的 () 元素，如 MPEG-2 所定義。</span><span class="sxs-lookup"><span data-stu-id="a8855-153">The stream contains raw_data_block() elements only, as defined by MPEG-2.</span></span></li>
<li><span data-ttu-id="a8855-154">1： ADTS。</span><span class="sxs-lookup"><span data-stu-id="a8855-154">1: ADTS.</span></span> <span data-ttu-id="a8855-155">資料流程包含 adts_sequence 的 () ，如 MPEG-2 所定義。</span><span class="sxs-lookup"><span data-stu-id="a8855-155">The stream contains an adts_sequence(), as defined by MPEG-2.</span></span> <span data-ttu-id="a8855-156">每個 adts_frame () 只允許一個 raw_data_block () 。</span><span class="sxs-lookup"><span data-stu-id="a8855-156">Only one raw_data_block() per adts_frame() is allowed.</span></span></li>
<li><span data-ttu-id="a8855-157">3：具有同步處理層的音訊廣播串流 (LOA) 和多工層 (LATM) 。</span><span class="sxs-lookup"><span data-stu-id="a8855-157">3: Audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span> <span data-ttu-id="a8855-158">在這三種類型的 LOA 中，只支援 <strong>AudioSyncStream</strong> 。</span><span class="sxs-lookup"><span data-stu-id="a8855-158">Of the three types of LOAS, only <strong>AudioSyncStream</strong> is supported.</span></span> <span data-ttu-id="a8855-159">多工層是 <strong>AudioMuxElement</strong>，限制為一個音訊程式和一層。</span><span class="sxs-lookup"><span data-stu-id="a8855-159">The multiplex layer is <strong>AudioMuxElement</strong>, restricted to one audio program and one layer.</span></span></li>
</ul><span data-ttu-id="a8855-160">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a8855-160">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="a8855-161">如果未指定此屬性，則會使用預設值0，此值會指定資料流程只包含 raw_data_block 元素。</span><span class="sxs-lookup"><span data-stu-id="a8855-161">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8855-162"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8855-162"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="a8855-163">已解碼 PCM 音訊所需的位深度。</span><span class="sxs-lookup"><span data-stu-id="a8855-163">Desired bit depth of the decoded PCM audio.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="a8855-164"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8855-164"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="a8855-165">指定喇叭位置的音訊通道指派。</span><span class="sxs-lookup"><span data-stu-id="a8855-165">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="a8855-166">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a8855-166">Optional.</span></span> <span data-ttu-id="a8855-167">如需詳細資訊，請參閱 <a href="#format-constraints">格式條件約束</a>。</span><span class="sxs-lookup"><span data-stu-id="a8855-167">For more information, see <a href="#format-constraints">Format Constraints</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8855-168"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8855-168"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="a8855-169">通道的數目，包括低頻率 (LFE) 通道（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a8855-169">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/></td>
<td><span data-ttu-id="a8855-170">此值的解讀取決於媒體子類型，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="a8855-170">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8855-171"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8855-171"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="a8855-172">取樣率（以每秒樣本數為單位）。</span><span class="sxs-lookup"><span data-stu-id="a8855-172">Sample rate, in samples per second.</span></span><br/></td>
<td><span data-ttu-id="a8855-173">此值的解讀取決於媒體子類型，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="a8855-173">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8855-174"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8855-174"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="a8855-175">其他格式資訊。</span><span class="sxs-lookup"><span data-stu-id="a8855-175">Additional format information.</span></span></td>
<td><span data-ttu-id="a8855-176">這個屬性的值取決於子類型。</span><span class="sxs-lookup"><span data-stu-id="a8855-176">The value of this attribute depends on the subtype.</span></span><br/>
<ul>
<li><span data-ttu-id="a8855-177"><strong>MFAudioFormat_AAC</strong>：包含在<strong>WAVEFORMATEX</strong>結構後面出現的部分<a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a>結構， (也就是<strong>wfx</strong>成員) 之後。</span><span class="sxs-lookup"><span data-stu-id="a8855-177"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="a8855-178">後面接著 AudioSpecificConfig () 資料，如 ISO/IEC 14496-3 所定義。</span><span class="sxs-lookup"><span data-stu-id="a8855-178">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="a8855-179"><strong>MEDIASUBTYPE_RAW_AAC1</strong>：包含 AudioSpecificConfig () 資料。</span><span class="sxs-lookup"><span data-stu-id="a8855-179"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span> <span data-ttu-id="a8855-180">此資料必須出現;否則，此解碼器將會拒絕媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a8855-180">This data must appear; otherwise, the decoder will reject the media type.</span></span></li>
</ul>
<span data-ttu-id="a8855-181">AudioSpecificConfig () 資料的長度為2個位元組，適用于 AAC-LC 或 AAC，且具有 .SBR/PS 的隱含信號。</span><span class="sxs-lookup"><span data-stu-id="a8855-181">The length of the AudioSpecificConfig() data is 2 bytes for AAC-LC or HE-AAC with implicit signaling of SBR/PS.</span></span> <span data-ttu-id="a8855-182">使用 .SBR/PS 的明確信號，AAC 超過2個位元組。</span><span class="sxs-lookup"><span data-stu-id="a8855-182">It is more than 2 bytes for HE-AAC with explicit signaling of SBR/PS.</span></span><br/> <span data-ttu-id="a8855-183">在 AudioSpecificConfig () 中定義的 <strong>audioObjectType</strong> 值必須是2，表示 AAC-LC。</span><span class="sxs-lookup"><span data-stu-id="a8855-183">The value of <strong>audioObjectType</strong> as defined in AudioSpecificConfig() must be 2, indicating AAC-LC.</span></span> <span data-ttu-id="a8855-184"><strong>ExtensionAudioObjectType</strong>的值必須是5，適用于 .sbr 或29（適用于 PS）。</span><span class="sxs-lookup"><span data-stu-id="a8855-184">The value of <strong>extensionAudioObjectType</strong> must be 5 for SBR or 29 for PS.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a><span data-ttu-id="a8855-185">輸出型別</span><span class="sxs-lookup"><span data-stu-id="a8855-185">Output Types</span></span>

<span data-ttu-id="a8855-186">此解碼器支援下列輸出類型：</span><span class="sxs-lookup"><span data-stu-id="a8855-186">The decoder supports the following output types:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a8855-187">Subtype</span><span class="sxs-lookup"><span data-stu-id="a8855-187">Subtype</span></span></th>
<th><span data-ttu-id="a8855-188">Description</span><span class="sxs-lookup"><span data-stu-id="a8855-188">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a8855-189"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="a8855-189"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="a8855-190">IEEE 浮點音訊。</span><span class="sxs-lookup"><span data-stu-id="a8855-190">IEEE floating-point audio.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8855-191"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="a8855-191"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="a8855-192">16位 PCM 音訊。</span><span class="sxs-lookup"><span data-stu-id="a8855-192">16-bit PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8855-193"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="a8855-193"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="a8855-194">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="a8855-194">Requires Windows 8.</span></span> <br/> <span data-ttu-id="a8855-195">此輸出類型可以用來將 LOA/LATM 格式的 AAC 資料流程轉換成 ADTS 格式。</span><span class="sxs-lookup"><span data-stu-id="a8855-195">This output type can be used to convert an AAC stream in the LOAS/LATM format to ADTS format.</span></span> <br/> <span data-ttu-id="a8855-196">若要將 LOA/LATM 資料流程轉換成 ADTS 資料流程，請將輸入類型設定為具有裝載類型 3 (LOA) 的 <strong>MFAudioFormat_AAC</strong> 。</span><span class="sxs-lookup"><span data-stu-id="a8855-196">To convert an LOAS/LATM stream to an ADTS stream, set the input type to <strong>MFAudioFormat_AAC</strong> with payload type 3 (LOAS).</span></span> <span data-ttu-id="a8855-197">然後，將輸出類型設定為承載類型 1 (ADTS) 的 <strong>MFAudioFormat_AAC</strong> 。</span><span class="sxs-lookup"><span data-stu-id="a8855-197">Then set the output type to <strong>MFAudioFormat_AAC</strong> with payload type 1 (ADTS).</span></span> <span data-ttu-id="a8855-198">此解碼器將會重新格式化 conainter，而不會解碼位流。</span><span class="sxs-lookup"><span data-stu-id="a8855-198">The decoder will reformat the conainter without decoding the bitstream.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a8855-199">此解碼器不會將 <strong>MFAudioFormat_AAC</strong> 註冊為輸出類型。</span><span class="sxs-lookup"><span data-stu-id="a8855-199">The decoder does not register <strong>MFAudioFormat_AAC</strong> as an output type.</span></span> <span data-ttu-id="a8855-200">但是，如果應用程式設定所述的輸入類型， <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform：： GetOutputAvailableType</strong></a> 方法會傳回可用輸出類型清單中 <strong>MFAudioFormat_AAC</strong> 。</span><span class="sxs-lookup"><span data-stu-id="a8855-200">However, if the application sets the input type as described, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> method returns <strong>MFAudioFormat_AAC</strong> in the list of available output types.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a8855-201">如果輸入資料流程包含兩個以上的通道，AAC 解碼器會提供輸出格式的兩個選項：</span><span class="sxs-lookup"><span data-stu-id="a8855-201">If the input stream contains more than two channels, the AAC decoder provides two options for the output format:</span></span>

-   <span data-ttu-id="a8855-202">與輸入類型相同的通道設定。</span><span class="sxs-lookup"><span data-stu-id="a8855-202">The same channel configuration as the input type.</span></span>
-   <span data-ttu-id="a8855-203">身歷聲折迭。</span><span class="sxs-lookup"><span data-stu-id="a8855-203">Stereo fold-down.</span></span>

## <a name="format-constraints"></a><span data-ttu-id="a8855-204">格式條件約束</span><span class="sxs-lookup"><span data-stu-id="a8855-204">Format Constraints</span></span>

<span data-ttu-id="a8855-205">已解碼的音訊取樣率必須是下列其中一項，套用 .SBR 之後 (如果存在) ：</span><span class="sxs-lookup"><span data-stu-id="a8855-205">The decoded audio sampling rate must be one of the following, after SBR is applied (if present):</span></span>

-   <span data-ttu-id="a8855-206">8 kHz</span><span class="sxs-lookup"><span data-stu-id="a8855-206">8 kHz</span></span>
-   <span data-ttu-id="a8855-207">11.025 kHz</span><span class="sxs-lookup"><span data-stu-id="a8855-207">11.025 kHz</span></span>
-   <span data-ttu-id="a8855-208">12 kHz</span><span class="sxs-lookup"><span data-stu-id="a8855-208">12 kHz</span></span>
-   <span data-ttu-id="a8855-209">16 kHz</span><span class="sxs-lookup"><span data-stu-id="a8855-209">16 kHz</span></span>
-   <span data-ttu-id="a8855-210">22.05 kHz</span><span class="sxs-lookup"><span data-stu-id="a8855-210">22.05 kHz</span></span>
-   <span data-ttu-id="a8855-211">24 kHz</span><span class="sxs-lookup"><span data-stu-id="a8855-211">24 kHz</span></span>
-   <span data-ttu-id="a8855-212">32 kHz</span><span class="sxs-lookup"><span data-stu-id="a8855-212">32 kHz</span></span>
-   <span data-ttu-id="a8855-213">44.1 kHz</span><span class="sxs-lookup"><span data-stu-id="a8855-213">44.1 kHz</span></span>
-   <span data-ttu-id="a8855-214">48 kHz</span><span class="sxs-lookup"><span data-stu-id="a8855-214">48 kHz</span></span>

<span data-ttu-id="a8855-215">不支援超過 48 kHz 的取樣率。</span><span class="sxs-lookup"><span data-stu-id="a8855-215">Sampling rates above 48 kHz are not supported.</span></span>

<span data-ttu-id="a8855-216">此解碼器支援最多6個音訊通道。</span><span class="sxs-lookup"><span data-stu-id="a8855-216">The decoder supports up to 6 audio channels.</span></span> <span data-ttu-id="a8855-217">針對每個說話者設定，解碼器預期 AAC 的語法元素會以特定的順序出現。</span><span class="sxs-lookup"><span data-stu-id="a8855-217">For each speaker configuration, the decoder expects the AAC syntactic elements to appear in a certain order.</span></span> <span data-ttu-id="a8855-218">下表列出支援的說話者設定。</span><span class="sxs-lookup"><span data-stu-id="a8855-218">The following table lists the supported speaker configurations.</span></span> <span data-ttu-id="a8855-219">資料表的第三個數據行使用下列標記法來列出預期的語法元素及其順序：</span><span class="sxs-lookup"><span data-stu-id="a8855-219">The third column of the table lists the expected syntactic elements and their order, using the following notation:</span></span>

-   <span data-ttu-id="a8855-220"><SCE1>：與 front center 喇叭相關聯的 single_channel_element (SCE) 。</span><span class="sxs-lookup"><span data-stu-id="a8855-220"><SCE1>: The single_channel_element (SCE) associated with the front center speaker.</span></span>
-   <span data-ttu-id="a8855-221"><SCE2>：與後置的喇叭相關的 SCE。</span><span class="sxs-lookup"><span data-stu-id="a8855-221"><SCE2>: The SCE associated with the back center speaker.</span></span>
-   <span data-ttu-id="a8855-222"><CPE1>：與 front 喇叭相關聯的 channel_pair_element (CPE) 。</span><span class="sxs-lookup"><span data-stu-id="a8855-222"><CPE1>: The channel_pair_element (CPE) associated with the front speakers.</span></span>
-   <span data-ttu-id="a8855-223"><CPE2>：與後 (或側邊) 喇叭相關聯的 CPE</span><span class="sxs-lookup"><span data-stu-id="a8855-223"><CPE2>: The CPE associated with the back (or side) speakers</span></span>
-   <span data-ttu-id="a8855-224"><LFE>： Lfe_channel_element (LFE) 。</span><span class="sxs-lookup"><span data-stu-id="a8855-224"><LFE>: The lfe_channel_element (LFE).</span></span>

<span data-ttu-id="a8855-225">如需這些語法元素的詳細資訊，請參閱 ISO/IEC 13818-7。</span><span class="sxs-lookup"><span data-stu-id="a8855-225">For more information about these syntactic elements, refer to ISO/IEC 13818-7.</span></span>



| <span data-ttu-id="a8855-226">組態</span><span class="sxs-lookup"><span data-stu-id="a8855-226">Configuration</span></span>       | <span data-ttu-id="a8855-227">通道遮罩</span><span class="sxs-lookup"><span data-stu-id="a8855-227">Channel Mask</span></span>                                                                                                                                                              | <span data-ttu-id="a8855-228">AAC 語法元素</span><span class="sxs-lookup"><span data-stu-id="a8855-228">AAC Syntactic Elements</span></span>                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="a8855-229">Mono</span><span class="sxs-lookup"><span data-stu-id="a8855-229">Mono</span></span>                | <span data-ttu-id="a8855-230">**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="a8855-230">**SPEAKER_FRONT_CENTER**</span></span>                                                                                                                                                | <SCE1>                                    |
| <span data-ttu-id="a8855-231">身歷聲或雙 mono</span><span class="sxs-lookup"><span data-stu-id="a8855-231">Stereo or dual mono</span></span> | <span data-ttu-id="a8855-232">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="a8855-232">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span></span>                                                                                                                     | <CPE1>                                    |
| <span data-ttu-id="a8855-233">2/1</span><span class="sxs-lookup"><span data-stu-id="a8855-233">2/1</span></span>                 | <span data-ttu-id="a8855-234">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="a8855-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span></span>                                                                                        | <CPE1><SCE1>                        |
| <span data-ttu-id="a8855-235">2/2</span><span class="sxs-lookup"><span data-stu-id="a8855-235">2/2</span></span>                 | <span data-ttu-id="a8855-236">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_BACK_LEFT** \|**SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="a8855-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                                              | <CPE1><CPE2>                        |
| <span data-ttu-id="a8855-237">3/0</span><span class="sxs-lookup"><span data-stu-id="a8855-237">3/0</span></span>                 | <span data-ttu-id="a8855-238">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="a8855-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span></span>                                                                                       | <SCE1><CPE1>                        |
| <span data-ttu-id="a8855-239">3/1</span><span class="sxs-lookup"><span data-stu-id="a8855-239">3/1</span></span>                 | <span data-ttu-id="a8855-240">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_FRONT_CENTER** \|**SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="a8855-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span></span>                                                          | <SCE1><CPE1><SCE2>            |
| <span data-ttu-id="a8855-241">3/2</span><span class="sxs-lookup"><span data-stu-id="a8855-241">3/2</span></span>                 | <span data-ttu-id="a8855-242">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_FRONT_CENTER** \|**SPEAKER_BACK_LEFT** \|**SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="a8855-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                | <SCE1><CPE1><CPE2>            |
| <span data-ttu-id="a8855-243">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="a8855-243">3/2 + LFE</span></span>           | <span data-ttu-id="a8855-244">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_FRONT_CENTER** \|**SPEAKER_LOW_FREQUENCY** \|**SPEAKER_BACK_LEFT** \|**SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="a8855-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span> | <SCE1><CPE1><CPE2><LFE> |



 

<span data-ttu-id="a8855-245">針對原始 AAC，每個輸入範例必須只包含一個完整的 AAC 壓縮框架。</span><span class="sxs-lookup"><span data-stu-id="a8855-245">For raw AAC, each input sample must contain exactly one full AAC compressed frame.</span></span>

<span data-ttu-id="a8855-246">針對 ADTS，每個輸入範例可以包含多個音訊畫面格，也可以包含部分框架，也就是框架可以橫跨範例界限。</span><span class="sxs-lookup"><span data-stu-id="a8855-246">For ADTS, each input sample can contain multiple audio frames, as well as partial frames   that is, frames can span sample boundaries.</span></span> <span data-ttu-id="a8855-247">每個 ADTS 標頭後面都必須有一個 AAC 框架。</span><span class="sxs-lookup"><span data-stu-id="a8855-247">Each ADTS header must be followed by one AAC frame.</span></span>

<span data-ttu-id="a8855-248">AAC 解碼器不支援下列任何一項：</span><span class="sxs-lookup"><span data-stu-id="a8855-248">The AAC decoder does not support any of the following:</span></span>

-   <span data-ttu-id="a8855-249">主要設定檔、Sample-Rate 可調整 (SRS) 設定檔或長期預測 (LTP) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a8855-249">Main profile, Sample-Rate Scalable (SRS) profile, or Long Term Prediction (LTP) profile.</span></span>
-   <span data-ttu-id="a8855-250">音訊資料交換格式 (ADIF) 。</span><span class="sxs-lookup"><span data-stu-id="a8855-250">Audio data interchange format (ADIF).</span></span>
-   <span data-ttu-id="a8855-251">LATM/老撾傳輸串流。</span><span class="sxs-lookup"><span data-stu-id="a8855-251">LATM/LAOS transport streams.</span></span>
-   <span data-ttu-id="a8855-252">結合通道元素 (CCEs) 。</span><span class="sxs-lookup"><span data-stu-id="a8855-252">Coupling channel elements (CCEs).</span></span> <span data-ttu-id="a8855-253">此解碼器會使用 CCEs 略過音訊框架。</span><span class="sxs-lookup"><span data-stu-id="a8855-253">The decoder will skip audio frames with CCEs.</span></span>
-   <span data-ttu-id="a8855-254">AAC-具有960範例框架大小的 LC。</span><span class="sxs-lookup"><span data-stu-id="a8855-254">AAC-LC with a 960-sample frame size.</span></span> <span data-ttu-id="a8855-255">僅支援 1024-範例框架。</span><span class="sxs-lookup"><span data-stu-id="a8855-255">Only 1024-sample frames are supported.</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="a8855-256">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="a8855-256">Transform Attributes</span></span>

<span data-ttu-id="a8855-257">AAC 解碼器會 [**執行 IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。</span><span class="sxs-lookup"><span data-stu-id="a8855-257">The AAC decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="a8855-258">應用程式可以使用這個方法來取得或設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a8855-258">Applications can use this method to get or set the following attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a8855-259">屬性</span><span class="sxs-lookup"><span data-stu-id="a8855-259">Attribute</span></span></th>
<th><span data-ttu-id="a8855-260">描述</span><span class="sxs-lookup"><span data-stu-id="a8855-260">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a8855-261"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8855-261"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span></span></td>
<td><span data-ttu-id="a8855-262">指定雙聲道音訊是否編碼為身歷聲或雙 mono。</span><span class="sxs-lookup"><span data-stu-id="a8855-262">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span> <span data-ttu-id="a8855-263">視為唯讀。</span><span class="sxs-lookup"><span data-stu-id="a8855-263">Treat as read-only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8855-264"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8855-264"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span></span></td>
<td><span data-ttu-id="a8855-265">指定解碼器如何重現雙重 mono 音訊。</span><span class="sxs-lookup"><span data-stu-id="a8855-265">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="a8855-266">預設值為 [ <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>：輸出 Ch1 至左方和右邊的喇叭。</span><span class="sxs-lookup"><span data-stu-id="a8855-266">The default value is <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output Ch1 to the left and right speakers.</span></span> <br/> <span data-ttu-id="a8855-267">應用程式可以設定此屬性來變更預設行為。</span><span class="sxs-lookup"><span data-stu-id="a8855-267">Applications can set this property to change the default behavior.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8855-268"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a8855-268"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="a8855-269">AAC 解碼器不會處理動態格式變更，而且必須在設定新的輸入媒體類型之前排清或清空。</span><span class="sxs-lookup"><span data-stu-id="a8855-269">The AAC decoder does not handle dynamic format changes, and must be flushed or drained before a new input media type is set.</span></span> <span data-ttu-id="a8855-270">將此屬性視為唯讀。</span><span class="sxs-lookup"><span data-stu-id="a8855-270">Treat this attribute as read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a8855-271">AAC 解碼器錯誤地將此屬性的值報告為 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="a8855-271">The AAC decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="a8855-272">在 Windows 7 中，解碼器錯誤地將這個屬性的值報告為 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="a8855-272">In Windows 7, the decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span> <span data-ttu-id="a8855-273">在 Windows 8 中，此解碼器會報告 <strong>FALSE</strong>，也就是正確的值</span><span class="sxs-lookup"><span data-stu-id="a8855-273">In Windows 8, the decoder reports <strong>FALSE</strong>, which is the correct value</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a><span data-ttu-id="a8855-274">範例媒體類型</span><span class="sxs-lookup"><span data-stu-id="a8855-274">Example Media Types</span></span>

<span data-ttu-id="a8855-275">以下是使用原始 AAC 承載之6通道 48-kHz AAC-LC 串流所需的輸入媒體類型範例：</span><span class="sxs-lookup"><span data-stu-id="a8855-275">Here is an example of the input media type needed for a 6-channel, 48-kHz AAC-LC stream, using a raw AAC payload:</span></span>



| <span data-ttu-id="a8855-276">屬性</span><span class="sxs-lookup"><span data-stu-id="a8855-276">Attribute</span></span>                                                                                      | <span data-ttu-id="a8855-277">值</span><span class="sxs-lookup"><span data-stu-id="a8855-277">Value</span></span>                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8855-278">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="a8855-278">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="a8855-279">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="a8855-279">**MFMediaType_Audio**</span></span>                                                               |
| [<span data-ttu-id="a8855-280">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="a8855-280">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="a8855-281">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="a8855-281">**MFAudioFormat_AAC**</span></span>                                                               |
| [<span data-ttu-id="a8855-282">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="a8855-282">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="a8855-283">48000</span><span class="sxs-lookup"><span data-stu-id="a8855-283">48000</span></span>                                                                                |
| [<span data-ttu-id="a8855-284">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="a8855-284">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="a8855-285">6</span><span class="sxs-lookup"><span data-stu-id="a8855-285">6</span></span>                                                                                    |
| [<span data-ttu-id="a8855-286">MF_MT_AAC_PAYLOAD_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8855-286">MF_MT_AAC_PAYLOAD_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="a8855-287">0</span><span class="sxs-lookup"><span data-stu-id="a8855-287">0</span></span>                                                                                    |
| [<span data-ttu-id="a8855-288">**MF_MT_USER_DATA**</span><span class="sxs-lookup"><span data-stu-id="a8855-288">**MF_MT_USER_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="a8855-289">{0x00，0x00，0x2a，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x11，0xb0}</span><span class="sxs-lookup"><span data-stu-id="a8855-289">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span></span> |
| [<span data-ttu-id="a8855-290">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="a8855-290">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="a8855-291">0x2a (選用) </span><span class="sxs-lookup"><span data-stu-id="a8855-291">0x2a (optional)</span></span>                                                                      |



 

<span data-ttu-id="a8855-292">[**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)的前12個位元組會對應到下列 [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo)結構成員：</span><span class="sxs-lookup"><span data-stu-id="a8855-292">The first 12 bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspond to the following [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure members:</span></span>

-   <span data-ttu-id="a8855-293">**wPayloadType** = 0 (原始 AAC) </span><span class="sxs-lookup"><span data-stu-id="a8855-293">**wPayloadType** = 0 (raw AAC)</span></span>
-   <span data-ttu-id="a8855-294">**wAudioProfileLevelIndication** = 0X2A (AAC 設定檔，層級 4) </span><span class="sxs-lookup"><span data-stu-id="a8855-294">**wAudioProfileLevelIndication** = 0x2a (AAC Profile, Level 4)</span></span>
-   <span data-ttu-id="a8855-295">**wStructType** = 0</span><span class="sxs-lookup"><span data-stu-id="a8855-295">**wStructType** = 0</span></span>

<span data-ttu-id="a8855-296">[**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)的最後兩個位元組包含 AudioSpecificConfig () 的值，如 mpeg-2 所定義。</span><span class="sxs-lookup"><span data-stu-id="a8855-296">The last two bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contain the value of AudioSpecificConfig(), as defined by MPEG-4.</span></span>

-   <span data-ttu-id="a8855-297">AudioSpecificConfig. audioObjectType = 2 (AAC LC)  (5 個位) </span><span class="sxs-lookup"><span data-stu-id="a8855-297">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)</span></span>
-   <span data-ttu-id="a8855-298">AudioSpecificConfig. samplingFrequencyIndex = 3 (4 位) </span><span class="sxs-lookup"><span data-stu-id="a8855-298">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)</span></span>
-   <span data-ttu-id="a8855-299">AudioSpecificConfig. channelConfiguration = 6 (4 位) </span><span class="sxs-lookup"><span data-stu-id="a8855-299">AudioSpecificConfig.channelConfiguration = 6 (4 bits)</span></span>
-   <span data-ttu-id="a8855-300">GASpecificConfig. frameLengthFlag = 0 (1 位) </span><span class="sxs-lookup"><span data-stu-id="a8855-300">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span></span>
-   <span data-ttu-id="a8855-301">GASpecificConfig. dependsOnCoreCoder = 0 (1 位) </span><span class="sxs-lookup"><span data-stu-id="a8855-301">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span></span>
-   <span data-ttu-id="a8855-302">GASpecificConfig. extensionFlag = 0 (1 位) </span><span class="sxs-lookup"><span data-stu-id="a8855-302">GASpecificConfig.extensionFlag = 0 (1 bit)</span></span>

<span data-ttu-id="a8855-303">指定此輸入類型時，請使用下列輸出媒體類型，從解碼器取得6通道的32位浮點 PCM 音訊：</span><span class="sxs-lookup"><span data-stu-id="a8855-303">Given this input type, use the following output media type to get 6-channel, 32-bit floating point PCM audio from the decoder:</span></span>



| <span data-ttu-id="a8855-304">屬性</span><span class="sxs-lookup"><span data-stu-id="a8855-304">Attribute</span></span>                                                                                    | <span data-ttu-id="a8855-305">值</span><span class="sxs-lookup"><span data-stu-id="a8855-305">Value</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [<span data-ttu-id="a8855-306">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="a8855-306">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="a8855-307">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="a8855-307">**MFMediaType_Audio**</span></span>   |
| [<span data-ttu-id="a8855-308">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="a8855-308">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="a8855-309">**MFAudioFormat_Float**</span><span class="sxs-lookup"><span data-stu-id="a8855-309">**MFAudioFormat_Float**</span></span> |
| [<span data-ttu-id="a8855-310">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span><span class="sxs-lookup"><span data-stu-id="a8855-310">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="a8855-311">32</span><span class="sxs-lookup"><span data-stu-id="a8855-311">32</span></span>                       |
| [<span data-ttu-id="a8855-312">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="a8855-312">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="a8855-313">48000</span><span class="sxs-lookup"><span data-stu-id="a8855-313">48000</span></span>                    |
| [<span data-ttu-id="a8855-314">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="a8855-314">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="a8855-315">6</span><span class="sxs-lookup"><span data-stu-id="a8855-315">6</span></span>                        |
| [<span data-ttu-id="a8855-316">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="a8855-316">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="a8855-317">1152000 (選用) </span><span class="sxs-lookup"><span data-stu-id="a8855-317">1152000 (optional)</span></span>       |
| [<span data-ttu-id="a8855-318">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span><span class="sxs-lookup"><span data-stu-id="a8855-318">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="a8855-319">24 (選用) </span><span class="sxs-lookup"><span data-stu-id="a8855-319">24 (optional)</span></span>            |
| [<span data-ttu-id="a8855-320">**MF_MT_AUDIO_CHANNEL_MASK**</span><span class="sxs-lookup"><span data-stu-id="a8855-320">**MF_MT_AUDIO_CHANNEL_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                   | <span data-ttu-id="a8855-321">0x3f (選用) </span><span class="sxs-lookup"><span data-stu-id="a8855-321">0x3f (optional)</span></span>          |



 

<span data-ttu-id="a8855-322">如果已安裝 Windows Vista 的平臺更新補充，AAC 音訊解碼器可在 Windows Vista 上取得，但只能在 Windows Vista 上使用 [來源讀取器](source-reader.md)來存取。</span><span class="sxs-lookup"><span data-stu-id="a8855-322">If Platform Update Supplement for Windows Vista is installed, the AAC audio decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8855-323">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8855-323">Requirements</span></span>



| <span data-ttu-id="a8855-324">需求</span><span class="sxs-lookup"><span data-stu-id="a8855-324">Requirement</span></span> | <span data-ttu-id="a8855-325">值</span><span class="sxs-lookup"><span data-stu-id="a8855-325">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8855-326">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8855-326">Minimum supported client</span></span><br/> | <span data-ttu-id="a8855-327">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8855-327">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="a8855-328">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8855-328">Minimum supported server</span></span><br/> | <span data-ttu-id="a8855-329">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8855-329">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="a8855-330">DLL</span><span class="sxs-lookup"><span data-stu-id="a8855-330">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8855-331"><dt>Windows 7 上的Msmpeg2adec.dll;</dt><dt>Windows 8 上的MSAudDecMFT.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8855-331"><dt>Msmpeg2adec.dll on Windows 7; </dt> <dt>MSAudDecMFT.dll on Windows 8</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8855-332">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8855-332">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8855-333">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="a8855-333">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="a8855-334">AAC 媒體類型</span><span class="sxs-lookup"><span data-stu-id="a8855-334">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="a8855-335">音訊媒體類型</span><span class="sxs-lookup"><span data-stu-id="a8855-335">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="a8855-336">**Microsoft MPEG-1/DD/AAC 音訊解碼器**</span><span class="sxs-lookup"><span data-stu-id="a8855-336">**Microsoft MPEG-1/DD/AAC Audio Decoder**</span></span>](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[<span data-ttu-id="a8855-337">媒體基礎中的 MPEG 4 支援</span><span class="sxs-lookup"><span data-stu-id="a8855-337">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a8855-338">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="a8855-338">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>
