---
description: Microsoft 媒體基礎的 AAC 解碼器是媒體基礎轉換，可將下列 Advanced 音訊編碼 (AAC) 和高效率 AAC (AAC) 設定檔：
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: AAC 解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7554d6bc4a13fe1e4af4c51e75f1fe8a0bd38286
ms.sourcegitcommit: 3a0a8a8fdce560a81a27789a1c04172ed96147b1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/22/2021
ms.locfileid: "112436582"
---
# <a name="aac-decoder"></a><span data-ttu-id="6157e-103">AAC 解碼器</span><span class="sxs-lookup"><span data-stu-id="6157e-103">AAC Decoder</span></span>

<span data-ttu-id="6157e-104">Microsoft 媒體基礎的 AAC 解碼器是 [媒體基礎轉換](media-foundation-transforms.md) ，可將下列 Advanced 音訊編碼 (AAC) 和高效率 AAC (AAC) 設定檔：</span><span class="sxs-lookup"><span data-stu-id="6157e-104">The Microsoft Media Foundation AAC decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes the following Advanced Audio Coding (AAC) and High Efficiency AAC (HE-AAC) profiles:</span></span>

-   <span data-ttu-id="6157e-105">MPEG-2 AAC 低複雜度 (LC) 設定檔 (多重通道) 。</span><span class="sxs-lookup"><span data-stu-id="6157e-105">MPEG-2 AAC Low Complexity (LC) profile (multichannel).</span></span>
-   <span data-ttu-id="6157e-106">MPEG-2 AAC v1 (多重通道) 搭配 AAC-LC 核心。</span><span class="sxs-lookup"><span data-stu-id="6157e-106">MPEG-4 HE-AAC v1 (multichannel) with AAC-LC core.</span></span>
-   <span data-ttu-id="6157e-107">使用 AAC-LC 核心的 MPEG-2 AAC v2 (身歷聲) 。</span><span class="sxs-lookup"><span data-stu-id="6157e-107">MPEG-4 HE-AAC v2 (stereo) with AAC-LC core.</span></span>

<span data-ttu-id="6157e-108">AAC 解碼器支援音訊資料傳輸串流中沒有標頭和 AAC 的原始 AAC 串流 (ADTS) 。</span><span class="sxs-lookup"><span data-stu-id="6157e-108">The AAC decoder supports both raw AAC streams with no headers and AAC in an audio data transport stream (ADTS).</span></span>

<span data-ttu-id="6157e-109">從 Windows 8 開始，AAC 解碼器也支援使用多工層來解碼 MPEG-2 音訊廣播串流， (LATM) 和同步處理層 (LOA) 。</span><span class="sxs-lookup"><span data-stu-id="6157e-109">Starting in Windows 8, the AAC decoder also supports decoding MPEG-4 audio transport streams with a multiplex layer (LATM) and synchronization layer (LOAS).</span></span> <span data-ttu-id="6157e-110">它也可以將 LATM/LOA 資料流程轉換為 ADTS。</span><span class="sxs-lookup"><span data-stu-id="6157e-110">It can also convert an LATM/LOAS stream to ADTS.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="6157e-111">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="6157e-111">Class Identifier</span></span>

<span data-ttu-id="6157e-112">AAC 編碼器 (CLSID) 的類別識別碼是 **clsid \_ CMSAACDecMFT**，定義于標頭檔 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="6157e-112">The class identifier (CLSID) of the AAC encoder is **CLSID\_CMSAACDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="6157e-113">媒體類型</span><span class="sxs-lookup"><span data-stu-id="6157e-113">Media Types</span></span>

<span data-ttu-id="6157e-114">AAC 解碼器支援下列媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6157e-114">The AAC decoder supports the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="6157e-115">輸入類型</span><span class="sxs-lookup"><span data-stu-id="6157e-115">Input Types</span></span>

<span data-ttu-id="6157e-116">AAC 解碼器支援下列音訊子類型：</span><span class="sxs-lookup"><span data-stu-id="6157e-116">The AAC decoder supports the following audio subtypes:</span></span>



| <span data-ttu-id="6157e-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="6157e-117">Subtype</span></span>                     | <span data-ttu-id="6157e-118">描述</span><span class="sxs-lookup"><span data-stu-id="6157e-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="6157e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="6157e-119">Header</span></span>       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="6157e-120">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="6157e-120">**MFAudioFormat_AAC**</span></span>      | <span data-ttu-id="6157e-121">Raw AAC 或 ADTS AAC。</span><span class="sxs-lookup"><span data-stu-id="6157e-121">Raw AAC or ADTS AAC.</span></span><br/> <span data-ttu-id="6157e-122">針對此子類型，媒體類型會在應用光譜頻內複寫 (.SBR) 和參數身歷聲 (PS) 工具（如果有的話）之前，提供取樣率和通道數目。</span><span class="sxs-lookup"><span data-stu-id="6157e-122">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="6157e-123">.SBR 工具的效果是將已解碼的取樣率加倍，相對於 core AAC-LC 取樣率。</span><span class="sxs-lookup"><span data-stu-id="6157e-123">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="6157e-124">PS 工具的效果是從 mono 通道核心 AAC-LC 串流解碼身歷聲。</span><span class="sxs-lookup"><span data-stu-id="6157e-124">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span><br/> <span data-ttu-id="6157e-125">這個子類型相當於 wmcodecdsp 中定義的 **MEDIASUBTYPE_MPEG_HEAAC**。</span><span class="sxs-lookup"><span data-stu-id="6157e-125">This subtype is equivalent to **MEDIASUBTYPE_MPEG_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="6157e-126">請參閱 [音訊子類型 guid](audio-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="6157e-126">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> <br/> <span data-ttu-id="6157e-127">[Mpeg-2 檔案來源](mpeg-4-file-source.md)和 ADTS 剖析器會輸出此子類型。</span><span class="sxs-lookup"><span data-stu-id="6157e-127">The [MPEG-4 File Source](mpeg-4-file-source.md) and the ADTS Parser output this subtype.</span></span> <br/> | <span data-ttu-id="6157e-128">mfapi。h</span><span class="sxs-lookup"><span data-stu-id="6157e-128">mfapi.h</span></span>      |
| <span data-ttu-id="6157e-129">**MEDIASUBTYPE_RAW_AAC1**</span><span class="sxs-lookup"><span data-stu-id="6157e-129">**MEDIASUBTYPE_RAW_AAC1**</span></span> | <span data-ttu-id="6157e-130">原始 AAC。</span><span class="sxs-lookup"><span data-stu-id="6157e-130">Raw AAC.</span></span> <br/> <span data-ttu-id="6157e-131">此子類型是用於包含在 AAC 中，且音訊格式標記等於 WAVE_FORMAT_RAW_AAC1 (0x00FF) 的 AVI 檔案中的。</span><span class="sxs-lookup"><span data-stu-id="6157e-131">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE_FORMAT_RAW_AAC1 (0x00FF).</span></span> <br/> <span data-ttu-id="6157e-132">針對此子類型，媒體類型會提供套用 .SBR 和 PS 工具之後的取樣速率和通道數目（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="6157e-132">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="6157e-133">wmcodecdsp。h</span><span class="sxs-lookup"><span data-stu-id="6157e-133">wmcodecdsp.h</span></span> |



 

<span data-ttu-id="6157e-134">若要設定 AAC 解碼器，請在輸入媒體類型上設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="6157e-134">To configure the AAC decoder, set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6157e-135">屬性</span><span class="sxs-lookup"><span data-stu-id="6157e-135">Attribute</span></span></th>
<th><span data-ttu-id="6157e-136">描述</span><span class="sxs-lookup"><span data-stu-id="6157e-136">Description</span></span></th>
<th><span data-ttu-id="6157e-137">備註</span><span class="sxs-lookup"><span data-stu-id="6157e-137">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6157e-138"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6157e-138"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="6157e-139">主要類型。</span><span class="sxs-lookup"><span data-stu-id="6157e-139">Major type.</span></span></td>
<td><span data-ttu-id="6157e-140">必須是 <strong>MFMediaType_Audio</strong>。</span><span class="sxs-lookup"><span data-stu-id="6157e-140">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6157e-141"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6157e-141"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="6157e-142">音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="6157e-142">Audio subtype.</span></span></td>
<td><span data-ttu-id="6157e-143">如需詳細資料，請參閱先前的描述。</span><span class="sxs-lookup"><span data-stu-id="6157e-143">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6157e-144"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="6157e-144"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="6157e-145">音訊設定檔和層級。</span><span class="sxs-lookup"><span data-stu-id="6157e-145">Audio profile and level.</span></span> <br/></td>
<td><span data-ttu-id="6157e-146">選擇性。</span><span class="sxs-lookup"><span data-stu-id="6157e-146">Optional.</span></span> <span data-ttu-id="6157e-147">只適用于 <strong>MFAudioFormat_AAC</strong>。</span><span class="sxs-lookup"><span data-stu-id="6157e-147">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <br/> <span data-ttu-id="6157e-148">這個屬性的值是 <strong>audioProfileLevelIndication</strong> 欄位，如 ISO/IEC 14496-3 所定義。</span><span class="sxs-lookup"><span data-stu-id="6157e-148">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span> <br/> <span data-ttu-id="6157e-149">如果不明，請將設定為零或 0xFE (&quot; 未指定任何音訊設定檔 &quot;) 。</span><span class="sxs-lookup"><span data-stu-id="6157e-149">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6157e-150"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="6157e-150"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="6157e-151">裝載類型。</span><span class="sxs-lookup"><span data-stu-id="6157e-151">Payload type.</span></span><br/></td>
<td><span data-ttu-id="6157e-152">只適用于 <strong>MFAudioFormat_AAC</strong>。</span><span class="sxs-lookup"><span data-stu-id="6157e-152">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <span data-ttu-id="6157e-153">此解碼器支援下列承載類型：</span><span class="sxs-lookup"><span data-stu-id="6157e-153">The decoder supports the following payload types:</span></span> <br/>
<ul>
<li><span data-ttu-id="6157e-154">0：原始 AAC。</span><span class="sxs-lookup"><span data-stu-id="6157e-154">0: Raw AAC.</span></span> <span data-ttu-id="6157e-155">資料流程只包含 raw_data_block 的 () 元素，如 MPEG-2 所定義。</span><span class="sxs-lookup"><span data-stu-id="6157e-155">The stream contains raw_data_block() elements only, as defined by MPEG-2.</span></span></li>
<li><span data-ttu-id="6157e-156">1： ADTS。</span><span class="sxs-lookup"><span data-stu-id="6157e-156">1: ADTS.</span></span> <span data-ttu-id="6157e-157">資料流程包含 adts_sequence 的 () ，如 MPEG-2 所定義。</span><span class="sxs-lookup"><span data-stu-id="6157e-157">The stream contains an adts_sequence(), as defined by MPEG-2.</span></span> <span data-ttu-id="6157e-158">每個 adts_frame () 只允許一個 raw_data_block () 。</span><span class="sxs-lookup"><span data-stu-id="6157e-158">Only one raw_data_block() per adts_frame() is allowed.</span></span></li>
<li><span data-ttu-id="6157e-159">3：具有同步處理層的音訊廣播串流 (LOA) 和多工層 (LATM) 。</span><span class="sxs-lookup"><span data-stu-id="6157e-159">3: Audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span> <span data-ttu-id="6157e-160">在這三種類型的 LOA 中，只支援 <strong>AudioSyncStream</strong> 。</span><span class="sxs-lookup"><span data-stu-id="6157e-160">Of the three types of LOAS, only <strong>AudioSyncStream</strong> is supported.</span></span> <span data-ttu-id="6157e-161">多工層是 <strong>AudioMuxElement</strong>，限制為一個音訊程式和一層。</span><span class="sxs-lookup"><span data-stu-id="6157e-161">The multiplex layer is <strong>AudioMuxElement</strong>, restricted to one audio program and one layer.</span></span></li>
</ul><span data-ttu-id="6157e-162">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6157e-162">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="6157e-163">如果未指定此屬性，則會使用預設值0，此值會指定資料流程只包含 raw_data_block 元素。</span><span class="sxs-lookup"><span data-stu-id="6157e-163">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6157e-164"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6157e-164"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="6157e-165">已解碼 PCM 音訊所需的位深度。</span><span class="sxs-lookup"><span data-stu-id="6157e-165">Desired bit depth of the decoded PCM audio.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6157e-166"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="6157e-166"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="6157e-167">指定喇叭位置的音訊通道指派。</span><span class="sxs-lookup"><span data-stu-id="6157e-167">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="6157e-168">選擇性。</span><span class="sxs-lookup"><span data-stu-id="6157e-168">Optional.</span></span> <span data-ttu-id="6157e-169">如需詳細資訊，請參閱 <a href="#format-constraints">格式條件約束</a>。</span><span class="sxs-lookup"><span data-stu-id="6157e-169">For more information, see <a href="#format-constraints">Format Constraints</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6157e-170"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="6157e-170"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="6157e-171">通道的數目，包括低頻率 (LFE) 通道（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="6157e-171">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/></td>
<td><span data-ttu-id="6157e-172">此值的解讀取決於媒體子類型，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="6157e-172">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6157e-173"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="6157e-173"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="6157e-174">取樣率（以每秒樣本數為單位）。</span><span class="sxs-lookup"><span data-stu-id="6157e-174">Sample rate, in samples per second.</span></span><br/></td>
<td><span data-ttu-id="6157e-175">此值的解讀取決於媒體子類型，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="6157e-175">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6157e-176"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="6157e-176"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="6157e-177">其他格式資訊。</span><span class="sxs-lookup"><span data-stu-id="6157e-177">Additional format information.</span></span></td>
<td><span data-ttu-id="6157e-178">這個屬性的值取決於子類型。</span><span class="sxs-lookup"><span data-stu-id="6157e-178">The value of this attribute depends on the subtype.</span></span><br/>
<ul>
<li><span data-ttu-id="6157e-179"><strong>MFAudioFormat_AAC</strong>：包含在<strong>WAVEFORMATEX</strong>結構後面出現的部分<a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a>結構， (也就是<strong>wfx</strong>成員) 之後。</span><span class="sxs-lookup"><span data-stu-id="6157e-179"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="6157e-180">後面接著 AudioSpecificConfig () 資料，如 ISO/IEC 14496-3 所定義。</span><span class="sxs-lookup"><span data-stu-id="6157e-180">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="6157e-181"><strong>MEDIASUBTYPE_RAW_AAC1</strong>：包含 AudioSpecificConfig () 資料。</span><span class="sxs-lookup"><span data-stu-id="6157e-181"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span> <span data-ttu-id="6157e-182">此資料必須出現;否則，此解碼器將會拒絕媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6157e-182">This data must appear; otherwise, the decoder will reject the media type.</span></span></li>
</ul>
<span data-ttu-id="6157e-183">AudioSpecificConfig () 資料的長度為2個位元組，適用于 AAC-LC 或 AAC，且具有 .SBR/PS 的隱含信號。</span><span class="sxs-lookup"><span data-stu-id="6157e-183">The length of the AudioSpecificConfig() data is 2 bytes for AAC-LC or HE-AAC with implicit signaling of SBR/PS.</span></span> <span data-ttu-id="6157e-184">使用 .SBR/PS 的明確信號，AAC 超過2個位元組。</span><span class="sxs-lookup"><span data-stu-id="6157e-184">It is more than 2 bytes for HE-AAC with explicit signaling of SBR/PS.</span></span><br/> <span data-ttu-id="6157e-185">在 AudioSpecificConfig () 中定義的 <strong>audioObjectType</strong> 值必須是2，表示 AAC-LC。</span><span class="sxs-lookup"><span data-stu-id="6157e-185">The value of <strong>audioObjectType</strong> as defined in AudioSpecificConfig() must be 2, indicating AAC-LC.</span></span> <span data-ttu-id="6157e-186"><strong>ExtensionAudioObjectType</strong>的值必須是5，適用于 .sbr 或29（適用于 PS）。</span><span class="sxs-lookup"><span data-stu-id="6157e-186">The value of <strong>extensionAudioObjectType</strong> must be 5 for SBR or 29 for PS.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a><span data-ttu-id="6157e-187">輸出型別</span><span class="sxs-lookup"><span data-stu-id="6157e-187">Output Types</span></span>

<span data-ttu-id="6157e-188">此解碼器支援下列輸出類型：</span><span class="sxs-lookup"><span data-stu-id="6157e-188">The decoder supports the following output types:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6157e-189">Subtype</span><span class="sxs-lookup"><span data-stu-id="6157e-189">Subtype</span></span></th>
<th><span data-ttu-id="6157e-190">描述</span><span class="sxs-lookup"><span data-stu-id="6157e-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6157e-191"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="6157e-191"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="6157e-192">IEEE 浮點音訊。</span><span class="sxs-lookup"><span data-stu-id="6157e-192">IEEE floating-point audio.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6157e-193"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="6157e-193"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="6157e-194">16位 PCM 音訊。</span><span class="sxs-lookup"><span data-stu-id="6157e-194">16-bit PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6157e-195"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="6157e-195"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="6157e-196">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="6157e-196">Requires Windows 8.</span></span> <br/> <span data-ttu-id="6157e-197">此輸出類型可以用來將 LOA/LATM 格式的 AAC 資料流程轉換成 ADTS 格式。</span><span class="sxs-lookup"><span data-stu-id="6157e-197">This output type can be used to convert an AAC stream in the LOAS/LATM format to ADTS format.</span></span> <br/> <span data-ttu-id="6157e-198">若要將 LOA/LATM 資料流程轉換成 ADTS 資料流程，請將輸入類型設定為具有裝載類型 3 (LOA) 的 <strong>MFAudioFormat_AAC</strong> 。</span><span class="sxs-lookup"><span data-stu-id="6157e-198">To convert an LOAS/LATM stream to an ADTS stream, set the input type to <strong>MFAudioFormat_AAC</strong> with payload type 3 (LOAS).</span></span> <span data-ttu-id="6157e-199">然後，將輸出類型設定為承載類型 1 (ADTS) 的 <strong>MFAudioFormat_AAC</strong> 。</span><span class="sxs-lookup"><span data-stu-id="6157e-199">Then set the output type to <strong>MFAudioFormat_AAC</strong> with payload type 1 (ADTS).</span></span> <span data-ttu-id="6157e-200">此解碼器將會重新格式化 conainter，而不會解碼位流。</span><span class="sxs-lookup"><span data-stu-id="6157e-200">The decoder will reformat the conainter without decoding the bitstream.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6157e-201">此解碼器不會將 <strong>MFAudioFormat_AAC</strong> 註冊為輸出類型。</span><span class="sxs-lookup"><span data-stu-id="6157e-201">The decoder does not register <strong>MFAudioFormat_AAC</strong> as an output type.</span></span> <span data-ttu-id="6157e-202">但是，如果應用程式設定所述的輸入類型， <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform：： GetOutputAvailableType</strong></a> 方法會傳回可用輸出類型清單中 <strong>MFAudioFormat_AAC</strong> 。</span><span class="sxs-lookup"><span data-stu-id="6157e-202">However, if the application sets the input type as described, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> method returns <strong>MFAudioFormat_AAC</strong> in the list of available output types.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6157e-203">如果輸入資料流程包含兩個以上的通道，AAC 解碼器會提供輸出格式的兩個選項：</span><span class="sxs-lookup"><span data-stu-id="6157e-203">If the input stream contains more than two channels, the AAC decoder provides two options for the output format:</span></span>

-   <span data-ttu-id="6157e-204">與輸入類型相同的通道設定。</span><span class="sxs-lookup"><span data-stu-id="6157e-204">The same channel configuration as the input type.</span></span>
-   <span data-ttu-id="6157e-205">身歷聲折迭。</span><span class="sxs-lookup"><span data-stu-id="6157e-205">Stereo fold-down.</span></span>

## <a name="format-constraints"></a><span data-ttu-id="6157e-206">格式條件約束</span><span class="sxs-lookup"><span data-stu-id="6157e-206">Format Constraints</span></span>

<span data-ttu-id="6157e-207">已解碼的音訊取樣率必須是下列其中一項，套用 .SBR 之後 (如果存在) ：</span><span class="sxs-lookup"><span data-stu-id="6157e-207">The decoded audio sampling rate must be one of the following, after SBR is applied (if present):</span></span>

-   <span data-ttu-id="6157e-208">8 kHz</span><span class="sxs-lookup"><span data-stu-id="6157e-208">8 kHz</span></span>
-   <span data-ttu-id="6157e-209">11.025 kHz</span><span class="sxs-lookup"><span data-stu-id="6157e-209">11.025 kHz</span></span>
-   <span data-ttu-id="6157e-210">12 kHz</span><span class="sxs-lookup"><span data-stu-id="6157e-210">12 kHz</span></span>
-   <span data-ttu-id="6157e-211">16 kHz</span><span class="sxs-lookup"><span data-stu-id="6157e-211">16 kHz</span></span>
-   <span data-ttu-id="6157e-212">22.05 kHz</span><span class="sxs-lookup"><span data-stu-id="6157e-212">22.05 kHz</span></span>
-   <span data-ttu-id="6157e-213">24 kHz</span><span class="sxs-lookup"><span data-stu-id="6157e-213">24 kHz</span></span>
-   <span data-ttu-id="6157e-214">32 kHz</span><span class="sxs-lookup"><span data-stu-id="6157e-214">32 kHz</span></span>
-   <span data-ttu-id="6157e-215">44.1 kHz</span><span class="sxs-lookup"><span data-stu-id="6157e-215">44.1 kHz</span></span>
-   <span data-ttu-id="6157e-216">48 kHz</span><span class="sxs-lookup"><span data-stu-id="6157e-216">48 kHz</span></span>

<span data-ttu-id="6157e-217">不支援超過 48 kHz 的取樣率。</span><span class="sxs-lookup"><span data-stu-id="6157e-217">Sampling rates above 48 kHz are not supported.</span></span>

<span data-ttu-id="6157e-218">此解碼器支援最多6個音訊通道。</span><span class="sxs-lookup"><span data-stu-id="6157e-218">The decoder supports up to 6 audio channels.</span></span> <span data-ttu-id="6157e-219">針對每個說話者設定，解碼器預期 AAC 的語法元素會以特定的順序出現。</span><span class="sxs-lookup"><span data-stu-id="6157e-219">For each speaker configuration, the decoder expects the AAC syntactic elements to appear in a certain order.</span></span> <span data-ttu-id="6157e-220">下表列出支援的說話者設定。</span><span class="sxs-lookup"><span data-stu-id="6157e-220">The following table lists the supported speaker configurations.</span></span> <span data-ttu-id="6157e-221">資料表的第三個數據行使用下列標記法來列出預期的語法元素及其順序：</span><span class="sxs-lookup"><span data-stu-id="6157e-221">The third column of the table lists the expected syntactic elements and their order, using the following notation:</span></span>

-   <span data-ttu-id="6157e-222"><SCE1>：與 front center 喇叭相關聯的 single_channel_element (SCE) 。</span><span class="sxs-lookup"><span data-stu-id="6157e-222"><SCE1>: The single_channel_element (SCE) associated with the front center speaker.</span></span>
-   <span data-ttu-id="6157e-223"><SCE2>：與後置的喇叭相關的 SCE。</span><span class="sxs-lookup"><span data-stu-id="6157e-223"><SCE2>: The SCE associated with the back center speaker.</span></span>
-   <span data-ttu-id="6157e-224"><CPE1>：與 front 喇叭相關聯的 channel_pair_element (CPE) 。</span><span class="sxs-lookup"><span data-stu-id="6157e-224"><CPE1>: The channel_pair_element (CPE) associated with the front speakers.</span></span>
-   <span data-ttu-id="6157e-225"><CPE2>：與後 (或側邊) 喇叭相關聯的 CPE</span><span class="sxs-lookup"><span data-stu-id="6157e-225"><CPE2>: The CPE associated with the back (or side) speakers</span></span>
-   <span data-ttu-id="6157e-226"><LFE>： Lfe_channel_element (LFE) 。</span><span class="sxs-lookup"><span data-stu-id="6157e-226"><LFE>: The lfe_channel_element (LFE).</span></span>

<span data-ttu-id="6157e-227">如需這些語法元素的詳細資訊，請參閱 ISO/IEC 13818-7。</span><span class="sxs-lookup"><span data-stu-id="6157e-227">For more information about these syntactic elements, refer to ISO/IEC 13818-7.</span></span>



| <span data-ttu-id="6157e-228">組態</span><span class="sxs-lookup"><span data-stu-id="6157e-228">Configuration</span></span>       | <span data-ttu-id="6157e-229">通道遮罩</span><span class="sxs-lookup"><span data-stu-id="6157e-229">Channel Mask</span></span>                                                                                                                                                              | <span data-ttu-id="6157e-230">AAC 語法元素</span><span class="sxs-lookup"><span data-stu-id="6157e-230">AAC Syntactic Elements</span></span>                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="6157e-231">Mono</span><span class="sxs-lookup"><span data-stu-id="6157e-231">Mono</span></span>                | <span data-ttu-id="6157e-232">**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="6157e-232">**SPEAKER_FRONT_CENTER**</span></span>                                                                                                                                                | <SCE1>                                    |
| <span data-ttu-id="6157e-233">身歷聲或雙 mono</span><span class="sxs-lookup"><span data-stu-id="6157e-233">Stereo or dual mono</span></span> | <span data-ttu-id="6157e-234">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="6157e-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span></span>                                                                                                                     | <CPE1>                                    |
| <span data-ttu-id="6157e-235">2/1</span><span class="sxs-lookup"><span data-stu-id="6157e-235">2/1</span></span>                 | <span data-ttu-id="6157e-236">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="6157e-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span></span>                                                                                        | <CPE1><SCE1>                        |
| <span data-ttu-id="6157e-237">2/2</span><span class="sxs-lookup"><span data-stu-id="6157e-237">2/2</span></span>                 | <span data-ttu-id="6157e-238">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_BACK_LEFT** \|**SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="6157e-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                                              | <CPE1><CPE2>                        |
| <span data-ttu-id="6157e-239">3/0</span><span class="sxs-lookup"><span data-stu-id="6157e-239">3/0</span></span>                 | <span data-ttu-id="6157e-240">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="6157e-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span></span>                                                                                       | <SCE1><CPE1>                        |
| <span data-ttu-id="6157e-241">3/1</span><span class="sxs-lookup"><span data-stu-id="6157e-241">3/1</span></span>                 | <span data-ttu-id="6157e-242">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_FRONT_CENTER** \|**SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="6157e-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span></span>                                                          | <SCE1><CPE1><SCE2>            |
| <span data-ttu-id="6157e-243">3/2</span><span class="sxs-lookup"><span data-stu-id="6157e-243">3/2</span></span>                 | <span data-ttu-id="6157e-244">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_FRONT_CENTER** \|**SPEAKER_BACK_LEFT** \|**SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="6157e-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                | <SCE1><CPE1><CPE2>            |
| <span data-ttu-id="6157e-245">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="6157e-245">3/2 + LFE</span></span>           | <span data-ttu-id="6157e-246">**SPEAKER_FRONT_LEFT** \|**SPEAKER_FRONT_RIGHT** \|**SPEAKER_FRONT_CENTER** \|**SPEAKER_LOW_FREQUENCY** \|**SPEAKER_BACK_LEFT** \|**SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="6157e-246">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span> | <SCE1><CPE1><CPE2><LFE> |



 

<span data-ttu-id="6157e-247">針對原始 AAC，每個輸入範例必須只包含一個完整的 AAC 壓縮框架。</span><span class="sxs-lookup"><span data-stu-id="6157e-247">For raw AAC, each input sample must contain exactly one full AAC compressed frame.</span></span>

<span data-ttu-id="6157e-248">針對 ADTS，每個輸入範例可以包含多個音訊畫面格，也可以包含部分框架，也就是框架可以橫跨範例界限。</span><span class="sxs-lookup"><span data-stu-id="6157e-248">For ADTS, each input sample can contain multiple audio frames, as well as partial frames   that is, frames can span sample boundaries.</span></span> <span data-ttu-id="6157e-249">每個 ADTS 標頭後面都必須有一個 AAC 框架。</span><span class="sxs-lookup"><span data-stu-id="6157e-249">Each ADTS header must be followed by one AAC frame.</span></span>

<span data-ttu-id="6157e-250">AAC 解碼器不支援下列任何一項：</span><span class="sxs-lookup"><span data-stu-id="6157e-250">The AAC decoder does not support any of the following:</span></span>

-   <span data-ttu-id="6157e-251">主要設定檔、Sample-Rate 可調整 (SRS) 設定檔或長期預測 (LTP) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6157e-251">Main profile, Sample-Rate Scalable (SRS) profile, or Long Term Prediction (LTP) profile.</span></span>
-   <span data-ttu-id="6157e-252">音訊資料交換格式 (ADIF) 。</span><span class="sxs-lookup"><span data-stu-id="6157e-252">Audio data interchange format (ADIF).</span></span>
-   <span data-ttu-id="6157e-253">LATM/老撾傳輸串流。</span><span class="sxs-lookup"><span data-stu-id="6157e-253">LATM/LAOS transport streams.</span></span>
-   <span data-ttu-id="6157e-254">結合通道元素 (CCEs) 。</span><span class="sxs-lookup"><span data-stu-id="6157e-254">Coupling channel elements (CCEs).</span></span> <span data-ttu-id="6157e-255">此解碼器會使用 CCEs 略過音訊框架。</span><span class="sxs-lookup"><span data-stu-id="6157e-255">The decoder will skip audio frames with CCEs.</span></span>
-   <span data-ttu-id="6157e-256">AAC-具有960範例框架大小的 LC。</span><span class="sxs-lookup"><span data-stu-id="6157e-256">AAC-LC with a 960-sample frame size.</span></span> <span data-ttu-id="6157e-257">僅支援 1024-範例框架。</span><span class="sxs-lookup"><span data-stu-id="6157e-257">Only 1024-sample frames are supported.</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="6157e-258">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="6157e-258">Transform Attributes</span></span>

<span data-ttu-id="6157e-259">AAC 解碼器會 [**執行 IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。</span><span class="sxs-lookup"><span data-stu-id="6157e-259">The AAC decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="6157e-260">應用程式可以使用這個方法來取得或設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="6157e-260">Applications can use this method to get or set the following attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6157e-261">屬性</span><span class="sxs-lookup"><span data-stu-id="6157e-261">Attribute</span></span></th>
<th><span data-ttu-id="6157e-262">描述</span><span class="sxs-lookup"><span data-stu-id="6157e-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6157e-263"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span><span class="sxs-lookup"><span data-stu-id="6157e-263"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span></span></td>
<td><span data-ttu-id="6157e-264">指定雙聲道音訊是否編碼為身歷聲或雙 mono。</span><span class="sxs-lookup"><span data-stu-id="6157e-264">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span> <span data-ttu-id="6157e-265">視為唯讀。</span><span class="sxs-lookup"><span data-stu-id="6157e-265">Treat as read-only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6157e-266"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="6157e-266"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span></span></td>
<td><span data-ttu-id="6157e-267">指定解碼器如何重現雙重 mono 音訊。</span><span class="sxs-lookup"><span data-stu-id="6157e-267">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="6157e-268">預設值為 [ <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>：輸出 Ch1 至左方和右邊的喇叭。</span><span class="sxs-lookup"><span data-stu-id="6157e-268">The default value is <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output Ch1 to the left and right speakers.</span></span> <br/> <span data-ttu-id="6157e-269">應用程式可以設定此屬性來變更預設行為。</span><span class="sxs-lookup"><span data-stu-id="6157e-269">Applications can set this property to change the default behavior.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6157e-270"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6157e-270"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="6157e-271">AAC 解碼器不會處理動態格式變更，而且必須在設定新的輸入媒體類型之前排清或清空。</span><span class="sxs-lookup"><span data-stu-id="6157e-271">The AAC decoder does not handle dynamic format changes, and must be flushed or drained before a new input media type is set.</span></span> <span data-ttu-id="6157e-272">將此屬性視為唯讀。</span><span class="sxs-lookup"><span data-stu-id="6157e-272">Treat this attribute as read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6157e-273">AAC 解碼器錯誤地將此屬性的值報告為 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="6157e-273">The AAC decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="6157e-274">在 Windows 7 中，解碼器錯誤地將這個屬性的值報告為 <strong>TRUE</strong> 。</span><span class="sxs-lookup"><span data-stu-id="6157e-274">In Windows 7, the decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span> <span data-ttu-id="6157e-275">在 Windows 8 中，此解碼器會報告 <strong>FALSE</strong>，也就是正確的值</span><span class="sxs-lookup"><span data-stu-id="6157e-275">In Windows 8, the decoder reports <strong>FALSE</strong>, which is the correct value</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a><span data-ttu-id="6157e-276">範例媒體類型</span><span class="sxs-lookup"><span data-stu-id="6157e-276">Example Media Types</span></span>

<span data-ttu-id="6157e-277">以下是使用原始 AAC 承載之6通道 48-kHz AAC-LC 串流所需的輸入媒體類型範例：</span><span class="sxs-lookup"><span data-stu-id="6157e-277">Here is an example of the input media type needed for a 6-channel, 48-kHz AAC-LC stream, using a raw AAC payload:</span></span>



| <span data-ttu-id="6157e-278">屬性</span><span class="sxs-lookup"><span data-stu-id="6157e-278">Attribute</span></span>                                                                                      | <span data-ttu-id="6157e-279">值</span><span class="sxs-lookup"><span data-stu-id="6157e-279">Value</span></span>                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="6157e-280">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="6157e-280">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="6157e-281">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="6157e-281">**MFMediaType_Audio**</span></span>                                                               |
| [<span data-ttu-id="6157e-282">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="6157e-282">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="6157e-283">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="6157e-283">**MFAudioFormat_AAC**</span></span>                                                               |
| [<span data-ttu-id="6157e-284">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="6157e-284">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="6157e-285">48000</span><span class="sxs-lookup"><span data-stu-id="6157e-285">48000</span></span>                                                                                |
| [<span data-ttu-id="6157e-286">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="6157e-286">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="6157e-287">6</span><span class="sxs-lookup"><span data-stu-id="6157e-287">6</span></span>                                                                                    |
| [<span data-ttu-id="6157e-288">MF_MT_AAC_PAYLOAD_TYPE</span><span class="sxs-lookup"><span data-stu-id="6157e-288">MF_MT_AAC_PAYLOAD_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="6157e-289">0</span><span class="sxs-lookup"><span data-stu-id="6157e-289">0</span></span>                                                                                    |
| [<span data-ttu-id="6157e-290">**MF_MT_USER_DATA**</span><span class="sxs-lookup"><span data-stu-id="6157e-290">**MF_MT_USER_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="6157e-291">{0x00，0x00，0x2a，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x11，0xb0}</span><span class="sxs-lookup"><span data-stu-id="6157e-291">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span></span> |
| [<span data-ttu-id="6157e-292">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="6157e-292">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="6157e-293">0x2a (選用) </span><span class="sxs-lookup"><span data-stu-id="6157e-293">0x2a (optional)</span></span>                                                                      |



 

<span data-ttu-id="6157e-294">[**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)的前12個位元組會對應到下列 [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo)結構成員：</span><span class="sxs-lookup"><span data-stu-id="6157e-294">The first 12 bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspond to the following [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure members:</span></span>

-   <span data-ttu-id="6157e-295">**wPayloadType** = 0 (原始 AAC) </span><span class="sxs-lookup"><span data-stu-id="6157e-295">**wPayloadType** = 0 (raw AAC)</span></span>
-   <span data-ttu-id="6157e-296">**wAudioProfileLevelIndication** = 0X2A (AAC 設定檔，層級 4) </span><span class="sxs-lookup"><span data-stu-id="6157e-296">**wAudioProfileLevelIndication** = 0x2a (AAC Profile, Level 4)</span></span>
-   <span data-ttu-id="6157e-297">**wStructType** = 0</span><span class="sxs-lookup"><span data-stu-id="6157e-297">**wStructType** = 0</span></span>

<span data-ttu-id="6157e-298">[**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)的最後兩個位元組包含 AudioSpecificConfig () 的值，如 mpeg-2 所定義。</span><span class="sxs-lookup"><span data-stu-id="6157e-298">The last two bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contain the value of AudioSpecificConfig(), as defined by MPEG-4.</span></span>

-   <span data-ttu-id="6157e-299">AudioSpecificConfig. audioObjectType = 2 (AAC LC)  (5 個位) </span><span class="sxs-lookup"><span data-stu-id="6157e-299">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)</span></span>
-   <span data-ttu-id="6157e-300">AudioSpecificConfig. samplingFrequencyIndex = 3 (4 位) </span><span class="sxs-lookup"><span data-stu-id="6157e-300">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)</span></span>
-   <span data-ttu-id="6157e-301">AudioSpecificConfig. channelConfiguration = 6 (4 位) </span><span class="sxs-lookup"><span data-stu-id="6157e-301">AudioSpecificConfig.channelConfiguration = 6 (4 bits)</span></span>
-   <span data-ttu-id="6157e-302">GASpecificConfig. frameLengthFlag = 0 (1 位) </span><span class="sxs-lookup"><span data-stu-id="6157e-302">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span></span>
-   <span data-ttu-id="6157e-303">GASpecificConfig. dependsOnCoreCoder = 0 (1 位) </span><span class="sxs-lookup"><span data-stu-id="6157e-303">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span></span>
-   <span data-ttu-id="6157e-304">GASpecificConfig. extensionFlag = 0 (1 位) </span><span class="sxs-lookup"><span data-stu-id="6157e-304">GASpecificConfig.extensionFlag = 0 (1 bit)</span></span>

<span data-ttu-id="6157e-305">指定此輸入類型時，請使用下列輸出媒體類型，從解碼器取得6通道的32位浮點 PCM 音訊：</span><span class="sxs-lookup"><span data-stu-id="6157e-305">Given this input type, use the following output media type to get 6-channel, 32-bit floating point PCM audio from the decoder:</span></span>



| <span data-ttu-id="6157e-306">屬性</span><span class="sxs-lookup"><span data-stu-id="6157e-306">Attribute</span></span>                                                                                    | <span data-ttu-id="6157e-307">值</span><span class="sxs-lookup"><span data-stu-id="6157e-307">Value</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [<span data-ttu-id="6157e-308">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="6157e-308">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="6157e-309">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="6157e-309">**MFMediaType_Audio**</span></span>   |
| [<span data-ttu-id="6157e-310">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="6157e-310">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="6157e-311">**MFAudioFormat_Float**</span><span class="sxs-lookup"><span data-stu-id="6157e-311">**MFAudioFormat_Float**</span></span> |
| [<span data-ttu-id="6157e-312">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span><span class="sxs-lookup"><span data-stu-id="6157e-312">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="6157e-313">32</span><span class="sxs-lookup"><span data-stu-id="6157e-313">32</span></span>                       |
| [<span data-ttu-id="6157e-314">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="6157e-314">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="6157e-315">48000</span><span class="sxs-lookup"><span data-stu-id="6157e-315">48000</span></span>                    |
| [<span data-ttu-id="6157e-316">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="6157e-316">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="6157e-317">6</span><span class="sxs-lookup"><span data-stu-id="6157e-317">6</span></span>                        |
| [<span data-ttu-id="6157e-318">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="6157e-318">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="6157e-319">1152000 (選用) </span><span class="sxs-lookup"><span data-stu-id="6157e-319">1152000 (optional)</span></span>       |
| [<span data-ttu-id="6157e-320">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span><span class="sxs-lookup"><span data-stu-id="6157e-320">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="6157e-321">24 (選用) </span><span class="sxs-lookup"><span data-stu-id="6157e-321">24 (optional)</span></span>            |
| [<span data-ttu-id="6157e-322">**MF_MT_AUDIO_CHANNEL_MASK**</span><span class="sxs-lookup"><span data-stu-id="6157e-322">**MF_MT_AUDIO_CHANNEL_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                   | <span data-ttu-id="6157e-323">0x3f (選用) </span><span class="sxs-lookup"><span data-stu-id="6157e-323">0x3f (optional)</span></span>          |



 

<span data-ttu-id="6157e-324">如果已安裝 Windows Vista 的平臺更新補充，AAC 音訊解碼器可在 Windows Vista 上取得，但只能在 Windows Vista 上使用 [來源讀取器](source-reader.md)來存取。</span><span class="sxs-lookup"><span data-stu-id="6157e-324">If Platform Update Supplement for Windows Vista is installed, the AAC audio decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6157e-325">規格需求</span><span class="sxs-lookup"><span data-stu-id="6157e-325">Requirements</span></span>



| <span data-ttu-id="6157e-326">需求</span><span class="sxs-lookup"><span data-stu-id="6157e-326">Requirement</span></span> | <span data-ttu-id="6157e-327">值</span><span class="sxs-lookup"><span data-stu-id="6157e-327">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6157e-328">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6157e-328">Minimum supported client</span></span><br/> | <span data-ttu-id="6157e-329">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6157e-329">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="6157e-330">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6157e-330">Minimum supported server</span></span><br/> | <span data-ttu-id="6157e-331">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6157e-331">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="6157e-332">DLL</span><span class="sxs-lookup"><span data-stu-id="6157e-332">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6157e-333"><dt>Windows 7 上的Msmpeg2adec.dll;</dt><dt>Windows 8 上的MSAudDecMFT.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6157e-333"><dt>Msmpeg2adec.dll on Windows 7; </dt> <dt>MSAudDecMFT.dll on Windows 8</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6157e-334">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6157e-334">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6157e-335">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="6157e-335">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="6157e-336">AAC 媒體類型</span><span class="sxs-lookup"><span data-stu-id="6157e-336">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="6157e-337">音訊媒體類型</span><span class="sxs-lookup"><span data-stu-id="6157e-337">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="6157e-338">**Microsoft MPEG-1/DD/AAC 音訊解碼器**</span><span class="sxs-lookup"><span data-stu-id="6157e-338">**Microsoft MPEG-1/DD/AAC Audio Decoder**</span></span>](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[<span data-ttu-id="6157e-339">媒體基礎中的 MPEG 4 支援</span><span class="sxs-lookup"><span data-stu-id="6157e-339">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6157e-340">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="6157e-340">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>
