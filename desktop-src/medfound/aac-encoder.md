---
description: Microsoft 媒體基礎的 AAC 編碼器是媒體基礎的轉換，它會編碼 Advanced 音訊編碼 (AAC) 低複雜性 (LC) 設定檔，如 ISO/IEC 13818-7 (MPEG-2 音訊第7部分) 所定義。
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: AAC 編碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9730ffc17d7ac3d5e16d86ef5aa20a46b329cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848110"
---
# <a name="aac-encoder"></a><span data-ttu-id="30afe-103">AAC 編碼器</span><span class="sxs-lookup"><span data-stu-id="30afe-103">AAC Encoder</span></span>

<span data-ttu-id="30afe-104">Microsoft 媒體基礎的 AAC 編碼器是 [媒體基礎的轉換](media-foundation-transforms.md) ，它會編碼 Advanced 音訊編碼 (AAC) 低複雜性 (LC) 設定檔，如 ISO/IEC 13818-7 (Mpeg-2 音訊第7部分) 所定義。</span><span class="sxs-lookup"><span data-stu-id="30afe-104">The Microsoft Media Foundation AAC encoder is a [Media Foundation Transform](media-foundation-transforms.md) that encodes Advanced Audio Coding (AAC) Low Complexity (LC) profile, as defined by ISO/IEC 13818-7 (MPEG-2 Audio Part 7) .</span></span>

<span data-ttu-id="30afe-105">AAC 編碼器不支援對任何其他 AAC 設定檔（例如 Main、SSR 或 LTP）進行編碼。</span><span class="sxs-lookup"><span data-stu-id="30afe-105">The AAC encoder does not support encoding to any other AAC profiles, such as Main, SSR, or LTP.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="30afe-106">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="30afe-106">Class Identifier</span></span>

<span data-ttu-id="30afe-107">AAC 編碼器 (CLSID) 的類別識別碼是 **clsid \_ AACMFTEncoder**，定義于標頭檔 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="30afe-107">The class identifier (CLSID) of the AAC encoder is **CLSID\_AACMFTEncoder**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="30afe-108">媒體類型</span><span class="sxs-lookup"><span data-stu-id="30afe-108">Media Types</span></span>

<span data-ttu-id="30afe-109">AAC 編碼器支援下列媒體類型。</span><span class="sxs-lookup"><span data-stu-id="30afe-109">The AAC encoder supports the following media types.</span></span> <span data-ttu-id="30afe-110">您可以將類型設定為 [第一個]、[第一個] 或 [輸出類型]。</span><span class="sxs-lookup"><span data-stu-id="30afe-110">You can set the types in either order input type first, or output type first.</span></span>

### <a name="input-types"></a><span data-ttu-id="30afe-111">輸入類型</span><span class="sxs-lookup"><span data-stu-id="30afe-111">Input Types</span></span>

<span data-ttu-id="30afe-112">在輸入媒體類型上設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="30afe-112">Set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30afe-113">屬性</span><span class="sxs-lookup"><span data-stu-id="30afe-113">Attribute</span></span></th>
<th><span data-ttu-id="30afe-114">描述</span><span class="sxs-lookup"><span data-stu-id="30afe-114">Description</span></span></th>
<th><span data-ttu-id="30afe-115">備註</span><span class="sxs-lookup"><span data-stu-id="30afe-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30afe-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="30afe-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="30afe-117">主要類型。</span><span class="sxs-lookup"><span data-stu-id="30afe-117">Major type.</span></span></td>
<td><span data-ttu-id="30afe-118">必須是 <strong>MFMediaType_Audio</strong>。</span><span class="sxs-lookup"><span data-stu-id="30afe-118">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30afe-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="30afe-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="30afe-120">亞。</span><span class="sxs-lookup"><span data-stu-id="30afe-120">Subtype.</span></span></td>
<td><span data-ttu-id="30afe-121">必須是 <strong>MFAudioFormat_PCM</strong>。</span><span class="sxs-lookup"><span data-stu-id="30afe-121">Must be <strong>MFAudioFormat_PCM</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30afe-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="30afe-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="30afe-123">每個樣本的位數。</span><span class="sxs-lookup"><span data-stu-id="30afe-123">Bits per sample.</span></span></td>
<td><span data-ttu-id="30afe-124">必須是16。</span><span class="sxs-lookup"><span data-stu-id="30afe-124">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30afe-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="30afe-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="30afe-126">每秒樣本數。</span><span class="sxs-lookup"><span data-stu-id="30afe-126">Samples per second.</span></span></td>
<td><span data-ttu-id="30afe-127">支援下列值：</span><span class="sxs-lookup"><span data-stu-id="30afe-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="30afe-128">44100 (44.1 KHz) </span><span class="sxs-lookup"><span data-stu-id="30afe-128">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="30afe-129">48000 (48 KHz) </span><span class="sxs-lookup"><span data-stu-id="30afe-129">48000 (48 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30afe-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="30afe-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="30afe-131">通道數目。</span><span class="sxs-lookup"><span data-stu-id="30afe-131">Number of channels.</span></span></td>
<td><span data-ttu-id="30afe-132">必須是 1 (mono) 或 2 (身歷聲) 或 6 (5.1) 。</span><span class="sxs-lookup"><span data-stu-id="30afe-132">Must be 1 (mono) or 2 (stereo), or 6 (5.1).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="30afe-133">Windows 10 引進了6個音訊通道的支援，且不適用於舊版的 Windows。</span><span class="sxs-lookup"><span data-stu-id="30afe-133">Support for 6 audio channels was introduced with Windows 10 and is not available for earlier versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="30afe-134">設定輸入類型之後，編碼器會衍生下列值，並將其新增至媒體類型：</span><span class="sxs-lookup"><span data-stu-id="30afe-134">After the input type is set, the encoder derives the following values and adds them to the media type:</span></span>

-   [<span data-ttu-id="30afe-135">**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30afe-135">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="30afe-136">**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**</span><span class="sxs-lookup"><span data-stu-id="30afe-136">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="30afe-137">**MF \_ MT \_ 平均 \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="30afe-137">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a><span data-ttu-id="30afe-138">輸出型別</span><span class="sxs-lookup"><span data-stu-id="30afe-138">Output Types</span></span>

<span data-ttu-id="30afe-139">在輸出媒體類型上設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="30afe-139">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30afe-140">屬性</span><span class="sxs-lookup"><span data-stu-id="30afe-140">Attribute</span></span></th>
<th><span data-ttu-id="30afe-141">描述</span><span class="sxs-lookup"><span data-stu-id="30afe-141">Description</span></span></th>
<th><span data-ttu-id="30afe-142">備註</span><span class="sxs-lookup"><span data-stu-id="30afe-142">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30afe-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="30afe-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="30afe-144">主要類型。</span><span class="sxs-lookup"><span data-stu-id="30afe-144">Major type.</span></span></td>
<td><span data-ttu-id="30afe-145">必須是 <strong>MFMediaType_Audio</strong>。</span><span class="sxs-lookup"><span data-stu-id="30afe-145">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30afe-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="30afe-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="30afe-147">音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="30afe-147">Audio subtype.</span></span></td>
<td><span data-ttu-id="30afe-148">必須是 <strong>MFAudioFormat_AAC</strong>。</span><span class="sxs-lookup"><span data-stu-id="30afe-148">Must be <strong>MFAudioFormat_AAC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30afe-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="30afe-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="30afe-150">每個樣本的位數。</span><span class="sxs-lookup"><span data-stu-id="30afe-150">Bits per sample.</span></span></td>
<td><span data-ttu-id="30afe-151">必須是16。</span><span class="sxs-lookup"><span data-stu-id="30afe-151">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30afe-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="30afe-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="30afe-153">每秒樣本數。</span><span class="sxs-lookup"><span data-stu-id="30afe-153">Samples per second.</span></span></td>
<td><span data-ttu-id="30afe-154">必須符合輸入類型。</span><span class="sxs-lookup"><span data-stu-id="30afe-154">Must match the input type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30afe-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="30afe-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="30afe-156">通道數目。</span><span class="sxs-lookup"><span data-stu-id="30afe-156">Number of channels.</span></span></td>
<td><span data-ttu-id="30afe-157">必須符合輸入類型。</span><span class="sxs-lookup"><span data-stu-id="30afe-157">Must match the input type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30afe-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="30afe-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="30afe-159">編碼 AAC 資料流程的位元速率（以每秒位元組數為單位）。</span><span class="sxs-lookup"><span data-stu-id="30afe-159">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="30afe-160">支援下列值：</span><span class="sxs-lookup"><span data-stu-id="30afe-160">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="30afe-161">12000</span><span class="sxs-lookup"><span data-stu-id="30afe-161">12000</span></span></li>
<li><span data-ttu-id="30afe-162">16000</span><span class="sxs-lookup"><span data-stu-id="30afe-162">16000</span></span></li>
<li><span data-ttu-id="30afe-163">20000</span><span class="sxs-lookup"><span data-stu-id="30afe-163">20000</span></span></li>
<li><span data-ttu-id="30afe-164">24000</span><span class="sxs-lookup"><span data-stu-id="30afe-164">24000</span></span></li>
</ul>
<span data-ttu-id="30afe-165">Mono 和身歷聲的預設值為 12000 (96 Kbps) 。</span><span class="sxs-lookup"><span data-stu-id="30afe-165">The default value for both mono and stereo is 12000 (96 Kbps).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="30afe-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="30afe-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="30afe-167">AAC 裝載類型。</span><span class="sxs-lookup"><span data-stu-id="30afe-167">The AAC payload type.</span></span></td>
<td><span data-ttu-id="30afe-168">選擇性。</span><span class="sxs-lookup"><span data-stu-id="30afe-168">Optional.</span></span> <span data-ttu-id="30afe-169">如果設定，此值必須為零，表示資料流程只包含 raw_data_block 元素。</span><span class="sxs-lookup"><span data-stu-id="30afe-169">If set, the value must be zero, indicating that the stream contains raw_data_block elements only.</span></span><br/> <span data-ttu-id="30afe-170">選擇性。</span><span class="sxs-lookup"><span data-stu-id="30afe-170">Optional.</span></span> <span data-ttu-id="30afe-171">如果未設定屬性，則預設值為零，表示資料流程只包含 (原始 AAC) 的 raw_data_block 元素。</span><span class="sxs-lookup"><span data-stu-id="30afe-171">If the attribute is not set, the default value is zero, indicating that the stream contains raw_data_block elements only (raw AAC).</span></span> <br/> <span data-ttu-id="30afe-172">在 Windows 7 中，如果已設定此屬性，則值必須為零。</span><span class="sxs-lookup"><span data-stu-id="30afe-172">In Windows 7, if this attribute is set, the value must be zero.</span></span><br/> <span data-ttu-id="30afe-173">從 Windows 8 開始，值可以是 0 (原始 AAC) 或 1 (ADTS AAC) 。</span><span class="sxs-lookup"><span data-stu-id="30afe-173">Starting in Windows 8, the value can be 0 (raw AAC) or 1 (ADTS AAC).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30afe-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="30afe-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="30afe-175">AAC 音訊設定檔和層級。</span><span class="sxs-lookup"><span data-stu-id="30afe-175">The AAC audio profile and level.</span></span></td>
<td><span data-ttu-id="30afe-176">選擇性。</span><span class="sxs-lookup"><span data-stu-id="30afe-176">Optional.</span></span> <span data-ttu-id="30afe-177">支援下列值：</span><span class="sxs-lookup"><span data-stu-id="30afe-177">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="30afe-178">0x29 (預設) </span><span class="sxs-lookup"><span data-stu-id="30afe-178">0x29 (default)</span></span></li>
<li><span data-ttu-id="30afe-179">0x2A</span><span class="sxs-lookup"><span data-stu-id="30afe-179">0x2A</span></span></li>
<li><span data-ttu-id="30afe-180">0x2B</span><span class="sxs-lookup"><span data-stu-id="30afe-180">0x2B</span></span></li>
<li><span data-ttu-id="30afe-181">0x2C</span><span class="sxs-lookup"><span data-stu-id="30afe-181">0x2C</span></span></li>
<li><span data-ttu-id="30afe-182">0x2E</span><span class="sxs-lookup"><span data-stu-id="30afe-182">0x2E</span></span></li>
<li><span data-ttu-id="30afe-183">0x2F</span><span class="sxs-lookup"><span data-stu-id="30afe-183">0x2F</span></span></li>
<li><span data-ttu-id="30afe-184">0x30</span><span class="sxs-lookup"><span data-stu-id="30afe-184">0x30</span></span></li>
<li><span data-ttu-id="30afe-185">0x31</span><span class="sxs-lookup"><span data-stu-id="30afe-185">0x31</span></span></li>
<li><span data-ttu-id="30afe-186">0x32</span><span class="sxs-lookup"><span data-stu-id="30afe-186">0x32</span></span></li>
<li><span data-ttu-id="30afe-187">0x33</span><span class="sxs-lookup"><span data-stu-id="30afe-187">0x33</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="30afe-188">下表列出可用於 MF_MT_AAC_PROFILE_LEVEL_INDICATION 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="30afe-188">The following table lists the values that can be used for the MF_MT_AAC_PROFILE_LEVEL_INDICATION attribute.</span></span>

| <span data-ttu-id="30afe-189">MF_MT_AAC_PROFILE_LEVEL_INDICATION 值</span><span class="sxs-lookup"><span data-stu-id="30afe-189">MF_MT_AAC_PROFILE_LEVEL_INDICATION value</span></span> | <span data-ttu-id="30afe-190">設定檔</span><span class="sxs-lookup"><span data-stu-id="30afe-190">Profile</span></span>                           |
|------------------------------------------|-----------------------------------|
| <span data-ttu-id="30afe-191">0x29</span><span class="sxs-lookup"><span data-stu-id="30afe-191">0x29</span></span>                                     | <span data-ttu-id="30afe-192">AAC Profile L2</span><span class="sxs-lookup"><span data-stu-id="30afe-192">AAC Profile L2</span></span>                    | 
| <span data-ttu-id="30afe-193">0x2A</span><span class="sxs-lookup"><span data-stu-id="30afe-193">0x2A</span></span>                                     | <span data-ttu-id="30afe-194">AAC 設定檔 L4</span><span class="sxs-lookup"><span data-stu-id="30afe-194">AAC Profile L4</span></span>                    | 
| <span data-ttu-id="30afe-195">0x2B</span><span class="sxs-lookup"><span data-stu-id="30afe-195">0x2B</span></span>                                     | <span data-ttu-id="30afe-196">AAC 設定檔 L5</span><span class="sxs-lookup"><span data-stu-id="30afe-196">AAC Profile L5</span></span>                    | 
| <span data-ttu-id="30afe-197">0x2C</span><span class="sxs-lookup"><span data-stu-id="30afe-197">0x2C</span></span>                                     | <span data-ttu-id="30afe-198">高效率 v1 AAC 設定檔 L2</span><span class="sxs-lookup"><span data-stu-id="30afe-198">High Efficiency v1 AAC Profile L2</span></span> | 
| <span data-ttu-id="30afe-199">0x2E</span><span class="sxs-lookup"><span data-stu-id="30afe-199">0x2E</span></span>                                     | <span data-ttu-id="30afe-200">高效率 v1 AAC 設定檔 L4</span><span class="sxs-lookup"><span data-stu-id="30afe-200">High Efficiency v1 AAC Profile L4</span></span> | 
| <span data-ttu-id="30afe-201">0x2F</span><span class="sxs-lookup"><span data-stu-id="30afe-201">0x2F</span></span>                                     | <span data-ttu-id="30afe-202">高效率 v1 AAC 設定檔 L5</span><span class="sxs-lookup"><span data-stu-id="30afe-202">High Efficiency v1 AAC Profile L5</span></span> | 
| <span data-ttu-id="30afe-203">0x30</span><span class="sxs-lookup"><span data-stu-id="30afe-203">0x30</span></span>                                     | <span data-ttu-id="30afe-204">高效率 v2 AAC 設定檔 L2</span><span class="sxs-lookup"><span data-stu-id="30afe-204">High Efficiency v2 AAC Profile L2</span></span> | 
| <span data-ttu-id="30afe-205">0x31</span><span class="sxs-lookup"><span data-stu-id="30afe-205">0x31</span></span>                                     | <span data-ttu-id="30afe-206">高效率 v2 AAC 設定檔 L3</span><span class="sxs-lookup"><span data-stu-id="30afe-206">High Efficiency v2 AAC Profile L3</span></span> | 
| <span data-ttu-id="30afe-207">0x32</span><span class="sxs-lookup"><span data-stu-id="30afe-207">0x32</span></span>                                     | <span data-ttu-id="30afe-208">高效率 v2 AAC 設定檔 L4</span><span class="sxs-lookup"><span data-stu-id="30afe-208">High Efficiency v2 AAC Profile L4</span></span> | 
| <span data-ttu-id="30afe-209">0x33</span><span class="sxs-lookup"><span data-stu-id="30afe-209">0x33</span></span>                                     | <span data-ttu-id="30afe-210">高效率 v2 AAC 設定檔 L5</span><span class="sxs-lookup"><span data-stu-id="30afe-210">High Efficiency v2 AAC Profile L5</span></span> | 

 

<span data-ttu-id="30afe-211">設定輸出類型之後，AAC 編碼器會藉由新增 [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md) 屬性來更新類型。</span><span class="sxs-lookup"><span data-stu-id="30afe-211">After the output type is set, the AAC encoder updates the type by adding the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="30afe-212">這個屬性（attribute）包含在 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))結構後面出現的 [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo)結構部分 (也就是 **wfx** 成員) 之後。</span><span class="sxs-lookup"><span data-stu-id="30afe-212">This attribute contains the portion of the [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure that appears after the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure (that is, after the **wfx** member).</span></span> <span data-ttu-id="30afe-213">後面接著 AudioSpecificConfig () 資料，如 ISO/IEC 14496-3 所定義。</span><span class="sxs-lookup"><span data-stu-id="30afe-213">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="30afe-214">每個輸出範例都包含一個不含標頭的壓縮 AAC 框架。</span><span class="sxs-lookup"><span data-stu-id="30afe-214">Each output sample contains one compressed AAC frame with no header.</span></span> <span data-ttu-id="30afe-215">此格式相當於 MPEG-2 所定義的原始 \_ 資料 \_ 區塊 () 元素。</span><span class="sxs-lookup"><span data-stu-id="30afe-215">This format is equivalent to the raw\_data\_block() element defined by MPEG-2.</span></span> <span data-ttu-id="30afe-216">如果輸出類型中有 [ [MF \_ MT \_ AAC 裝載 \_ \_ 類型](mf-mt-aac-payload-type.md) ] 屬性，則必須設定為 [零]，以指出此裝載類型。</span><span class="sxs-lookup"><span data-stu-id="30afe-216">The [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) attribute, if present in the output type, must be set to zero to indicate this payload type.</span></span>

<span data-ttu-id="30afe-217">每個輸出範例都包含一個對應到 1024 PCM 範例的壓縮 AAC 框架。</span><span class="sxs-lookup"><span data-stu-id="30afe-217">Each output sample contains one compressed AAC frame corresponding to 1024 PCM samples.</span></span> <span data-ttu-id="30afe-218">例如，在 48 Khz 取樣率，一個壓縮框架的持續時間是21.33 毫秒。</span><span class="sxs-lookup"><span data-stu-id="30afe-218">For example, at 48 Khz sampling rate, the duration of one compressed frame is 21.33 msec.</span></span>

<span data-ttu-id="30afe-219">如果 [MF \_ MT \_ AAC \_ 裝載 \_ 類型](mf-mt-aac-payload-type.md) 為零 (預設值) ，則每個輸出範例都會包含一個原始 \_ 資料 \_ 區塊 () 元素，如 ISO/IEC 13818-7 所定義。</span><span class="sxs-lookup"><span data-stu-id="30afe-219">If [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) is zero (the default value), each output sample contains one raw\_data\_block() element as defined by ISO/IEC 13818-7.</span></span>

## <a name="example-media-types"></a><span data-ttu-id="30afe-220">範例媒體類型</span><span class="sxs-lookup"><span data-stu-id="30afe-220">Example Media Types</span></span>

<span data-ttu-id="30afe-221">以下是從 44.1-kHz、160 Kbps 身歷聲音訊編碼至原始 AAC 時所需的媒體類型範例</span><span class="sxs-lookup"><span data-stu-id="30afe-221">Here is an example of the media types needed to encode from 44.1-kHz, 160-Kbps stereo audio to raw AAC</span></span>

<span data-ttu-id="30afe-222">輸入媒體類型：</span><span class="sxs-lookup"><span data-stu-id="30afe-222">Input media type:</span></span>



| <span data-ttu-id="30afe-223">屬性</span><span class="sxs-lookup"><span data-stu-id="30afe-223">Attribute</span></span>                                                                                    | <span data-ttu-id="30afe-224">值</span><span class="sxs-lookup"><span data-stu-id="30afe-224">Value</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="30afe-225">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="30afe-225">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="30afe-226">**MFMediaType \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="30afe-226">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="30afe-227">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="30afe-227">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="30afe-228">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="30afe-228">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="30afe-229">**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**</span><span class="sxs-lookup"><span data-stu-id="30afe-229">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="30afe-230">16</span><span class="sxs-lookup"><span data-stu-id="30afe-230">16</span></span>                     |
| [<span data-ttu-id="30afe-231">**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30afe-231">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="30afe-232">44100</span><span class="sxs-lookup"><span data-stu-id="30afe-232">44100</span></span>                  |
| [<span data-ttu-id="30afe-233">**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**</span><span class="sxs-lookup"><span data-stu-id="30afe-233">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="30afe-234">2</span><span class="sxs-lookup"><span data-stu-id="30afe-234">2</span></span>                      |
| [<span data-ttu-id="30afe-235">**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30afe-235">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="30afe-236">176400 (選用) </span><span class="sxs-lookup"><span data-stu-id="30afe-236">176400 (optional)</span></span>      |
| [<span data-ttu-id="30afe-237">**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**</span><span class="sxs-lookup"><span data-stu-id="30afe-237">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="30afe-238">4 (選用) </span><span class="sxs-lookup"><span data-stu-id="30afe-238">4 (optional)</span></span>           |
| [<span data-ttu-id="30afe-239">**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**</span><span class="sxs-lookup"><span data-stu-id="30afe-239">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="30afe-240">1 (選用) </span><span class="sxs-lookup"><span data-stu-id="30afe-240">1 (optional)</span></span>           |
| [<span data-ttu-id="30afe-241">**MF \_ MT \_ 平均 \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="30afe-241">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                  | <span data-ttu-id="30afe-242">1411200 (選用) </span><span class="sxs-lookup"><span data-stu-id="30afe-242">1411200 (optional)</span></span>     |
| [<span data-ttu-id="30afe-243">**MF \_ MT \_ 固定 \_ 大小 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="30afe-243">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)                   | <span data-ttu-id="30afe-244">1 (選用) </span><span class="sxs-lookup"><span data-stu-id="30afe-244">1 (optional)</span></span>           |



 

<span data-ttu-id="30afe-245">輸出媒體類型：</span><span class="sxs-lookup"><span data-stu-id="30afe-245">Output media type:</span></span>



| <span data-ttu-id="30afe-246">屬性</span><span class="sxs-lookup"><span data-stu-id="30afe-246">Attribute</span></span>                                                                                      | <span data-ttu-id="30afe-247">值</span><span class="sxs-lookup"><span data-stu-id="30afe-247">Value</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30afe-248">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="30afe-248">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="30afe-249">**MFMediaType \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="30afe-249">**MFMediaType\_Audio**</span></span>                                                                          |
| [<span data-ttu-id="30afe-250">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="30afe-250">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="30afe-251">**MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="30afe-251">**MFAudioFormat\_AAC**</span></span>                                                                          |
| [<span data-ttu-id="30afe-252">**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**</span><span class="sxs-lookup"><span data-stu-id="30afe-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="30afe-253">16</span><span class="sxs-lookup"><span data-stu-id="30afe-253">16</span></span>                                                                                              |
| [<span data-ttu-id="30afe-254">**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30afe-254">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="30afe-255">44100</span><span class="sxs-lookup"><span data-stu-id="30afe-255">44100</span></span>                                                                                           |
| [<span data-ttu-id="30afe-256">**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**</span><span class="sxs-lookup"><span data-stu-id="30afe-256">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="30afe-257">2</span><span class="sxs-lookup"><span data-stu-id="30afe-257">2</span></span>                                                                                               |
| [<span data-ttu-id="30afe-258">**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="30afe-258">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="30afe-259">20000</span><span class="sxs-lookup"><span data-stu-id="30afe-259">20000</span></span>                                                                                           |
| [<span data-ttu-id="30afe-260">MF \_ MT \_ AAC \_ 裝載 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="30afe-260">MF\_MT\_AAC\_PAYLOAD\_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="30afe-261">0 (選用) </span><span class="sxs-lookup"><span data-stu-id="30afe-261">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="30afe-262">MF \_ MT \_ AAC \_ 音訊 \_ 設定檔 \_ 層級 \_ 指示</span><span class="sxs-lookup"><span data-stu-id="30afe-262">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="30afe-263">0x29 (選用) </span><span class="sxs-lookup"><span data-stu-id="30afe-263">0x29 (optional)</span></span>                                                                                 |
| [<span data-ttu-id="30afe-264">**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**</span><span class="sxs-lookup"><span data-stu-id="30afe-264">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="30afe-265">1 (選用) </span><span class="sxs-lookup"><span data-stu-id="30afe-265">1 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="30afe-266">**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**</span><span class="sxs-lookup"><span data-stu-id="30afe-266">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)           | <span data-ttu-id="30afe-267">0 (選用) </span><span class="sxs-lookup"><span data-stu-id="30afe-267">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="30afe-268">**MF \_ MT \_ 平均 \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="30afe-268">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                    | <span data-ttu-id="30afe-269">160000 (選用) </span><span class="sxs-lookup"><span data-stu-id="30afe-269">160000 (optional)</span></span>                                                                               |
| [<span data-ttu-id="30afe-270">**MF \_ MT \_ 使用者 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="30afe-270">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="30afe-271">{0x00，0x00，0x29，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x00，0x12，0x10} (選用) </span><span class="sxs-lookup"><span data-stu-id="30afe-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} (optional)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="30afe-272">備註</span><span class="sxs-lookup"><span data-stu-id="30afe-272">Remarks</span></span>

<span data-ttu-id="30afe-273">在目前的執行中，每個輸入範例都必須有有效的時間和持續時間。</span><span class="sxs-lookup"><span data-stu-id="30afe-273">In the current implementation, every input sample must have a valid time and duration.</span></span> <span data-ttu-id="30afe-274">若要設定取樣時間，請呼叫 [**IMFSample：： SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime)。</span><span class="sxs-lookup"><span data-stu-id="30afe-274">To set the sample time, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="30afe-275">若要設定範例持續時間，請呼叫 [**IMFSample：： SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration)。</span><span class="sxs-lookup"><span data-stu-id="30afe-275">To set the sample duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="30afe-276">如果未設定範例時間，編碼器的 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 方法會傳回 **MF \_ E \_ NO \_ 範例 \_ 時間戳記**。</span><span class="sxs-lookup"><span data-stu-id="30afe-276">If the sample time is not set, the encoder's [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method returns **MF\_E\_NO\_SAMPLE\_TIMESTAMP**.</span></span> <span data-ttu-id="30afe-277">如果未設定範例持續時間， **ProcessInput** 方法會傳回 **MF \_ E \_ 無 \_ 範例 \_ 持續時間**。</span><span class="sxs-lookup"><span data-stu-id="30afe-277">If the sample duration is not set, the **ProcessInput** method returns **MF\_E\_NO\_SAMPLE\_DURATION**.</span></span>

<span data-ttu-id="30afe-278">範例持續時間可以計算如下：</span><span class="sxs-lookup"><span data-stu-id="30afe-278">Sample duration can be calculated as follows:</span></span>


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



<span data-ttu-id="30afe-279">其中 *nAudioSamplesPerChannel* 是輸入緩衝區中每個通道的 PCM 音訊樣本數目，而 *nSamplesPerSec* 則是取樣率（以樣本/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="30afe-279">where *nAudioSamplesPerChannel* is the number of PCM audio samples per channel in the input buffer, and *nSamplesPerSec* is the sampling rate, in samples per second.</span></span>

> [!Note]  
> <span data-ttu-id="30afe-280">由於目前的執行中有錯誤，如果範例持續時間設定為零，則 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 呼叫會成功，但後續呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 將會擲回零除的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="30afe-280">Due to a bug in the current implementation, if the sample duration is set to zero, the [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) call succeeds, but a subsequent call to [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) will throw a divide-by-zero exception.</span></span> <span data-ttu-id="30afe-281">若要避免這個錯誤，請在每個輸入範例上設定有效的非零持續時間。</span><span class="sxs-lookup"><span data-stu-id="30afe-281">To avoid this error, set a valid nonzero duration on each input sample.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30afe-282">規格需求</span><span class="sxs-lookup"><span data-stu-id="30afe-282">Requirements</span></span>



| <span data-ttu-id="30afe-283">需求</span><span class="sxs-lookup"><span data-stu-id="30afe-283">Requirement</span></span> | <span data-ttu-id="30afe-284">值</span><span class="sxs-lookup"><span data-stu-id="30afe-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30afe-285">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30afe-285">Minimum supported client</span></span><br/> | <span data-ttu-id="30afe-286">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30afe-286">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="30afe-287">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30afe-287">Minimum supported server</span></span><br/> | <span data-ttu-id="30afe-288">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30afe-288">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="30afe-289">DLL</span><span class="sxs-lookup"><span data-stu-id="30afe-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30afe-290"><dt>Mfaacenc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30afe-290"><dt>Mfaacenc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30afe-291">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30afe-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30afe-292">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="30afe-292">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="30afe-293">**AAC 解碼器**</span><span class="sxs-lookup"><span data-stu-id="30afe-293">**AAC Decoder**</span></span>](aac-decoder.md)
</dt> <dt>

[<span data-ttu-id="30afe-294">AAC 媒體類型</span><span class="sxs-lookup"><span data-stu-id="30afe-294">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="30afe-295">音訊媒體類型</span><span class="sxs-lookup"><span data-stu-id="30afe-295">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="30afe-296">媒體基礎中的 MPEG 4 支援</span><span class="sxs-lookup"><span data-stu-id="30afe-296">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="30afe-297">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="30afe-297">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

