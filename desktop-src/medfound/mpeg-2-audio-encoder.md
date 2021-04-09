---
description: Microsoft 媒體基礎的 MPEG-2 音訊編碼器是媒體基礎轉換，可將 mono 或身歷聲音訊編碼為 MPEG-2 音訊 (ISO/IEC 11172-3) 或 MPEG-2 音訊 (ISO/IEC 13818-3) 。
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: MPEG-2 音訊編碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848443"
---
# <a name="mpeg-2-audio-encoder"></a><span data-ttu-id="a7eee-103">MPEG-2 音訊編碼器</span><span class="sxs-lookup"><span data-stu-id="a7eee-103">MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="a7eee-104">Microsoft 媒體基礎的 MPEG-2 音訊編碼器是 [媒體基礎轉換](media-foundation-transforms.md) ，可將 mono 或身歷聲音訊編碼為 mpeg-2 音訊 (ISO/iec 11172-3) 或 mpeg-2 音訊 (ISO/iec 13818-3) 。</span><span class="sxs-lookup"><span data-stu-id="a7eee-104">The Microsoft Media Foundation MPEG-2 audio encoder is a [Media Foundation transform](media-foundation-transforms.md) that encodes mono or stereo audio to MPEG-1 audio (ISO/IEC 11172-3) or MPEG-2 audio (ISO/IEC 13818-3).</span></span>

<span data-ttu-id="a7eee-105">編碼器支援第1層和第2層音訊。</span><span class="sxs-lookup"><span data-stu-id="a7eee-105">The encoder supports Layer 1 and Layer 2 audio.</span></span> <span data-ttu-id="a7eee-106">它不支援 MPEG-Layer 3 (MP3) 音訊。</span><span class="sxs-lookup"><span data-stu-id="a7eee-106">It does not support MPEG-Layer 3 (MP3) audio.</span></span> <span data-ttu-id="a7eee-107">針對 MPEG-2，編碼器支援 (LSF) 部分的 MPEG-2 音訊的低取樣頻率。</span><span class="sxs-lookup"><span data-stu-id="a7eee-107">For MPEG-2, the encoder supports the Low Sampling Frequencies (LSF) portion of MPEG-2 audio.</span></span> <span data-ttu-id="a7eee-108">它不支援多重通道擴充。</span><span class="sxs-lookup"><span data-stu-id="a7eee-108">It does not support the multichannel extensions.</span></span> <span data-ttu-id="a7eee-109">MFT 會輸出 MPEG 基本資料流程。</span><span class="sxs-lookup"><span data-stu-id="a7eee-109">The MFT outputs an MPEG elementary stream.</span></span> <span data-ttu-id="a7eee-110">它無法產生 packetized 的基本資料流程、程式資料流程或傳輸串流。</span><span class="sxs-lookup"><span data-stu-id="a7eee-110">It cannot generate packetized elementary streams, program streams, or transport streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="a7eee-111">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="a7eee-111">Class Identifier</span></span>

<span data-ttu-id="a7eee-112">MEPG-2 音訊編碼器 (CLSID) 的類別識別碼為 **clsid \_ CMPEG2AudioEncoderMFT**，定義于標頭檔 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="a7eee-112">The class identifier (CLSID) of the MEPG-2 audio encoder is **CLSID\_CMPEG2AudioEncoderMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="a7eee-113">輸出型別</span><span class="sxs-lookup"><span data-stu-id="a7eee-113">Output Types</span></span>

<span data-ttu-id="a7eee-114">在輸入類型之前，必須先設定輸出類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-114">The output type must be set first, before the input type.</span></span> <span data-ttu-id="a7eee-115">下表列出輸出媒體類型的必要和選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="a7eee-115">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7eee-116">屬性</span><span class="sxs-lookup"><span data-stu-id="a7eee-116">Attribute</span></span></th>
<th><span data-ttu-id="a7eee-117">描述</span><span class="sxs-lookup"><span data-stu-id="a7eee-117">Description</span></span></th>
<th><span data-ttu-id="a7eee-118">備註</span><span class="sxs-lookup"><span data-stu-id="a7eee-118">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7eee-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="a7eee-120">主要類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-120">Major type.</span></span></td>
<td><span data-ttu-id="a7eee-121">必要。</span><span class="sxs-lookup"><span data-stu-id="a7eee-121">Required.</span></span> <span data-ttu-id="a7eee-122">必須是 <strong>MFMediaType_Audio</strong>。</span><span class="sxs-lookup"><span data-stu-id="a7eee-122">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7eee-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="a7eee-124">音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-124">Audio subtype.</span></span></td>
<td><span data-ttu-id="a7eee-125">必要。</span><span class="sxs-lookup"><span data-stu-id="a7eee-125">Required.</span></span> <span data-ttu-id="a7eee-126">必須是 <strong>MFAudioFormat_MPEG</strong>。</span><span class="sxs-lookup"><span data-stu-id="a7eee-126">Must be <strong>MFAudioFormat_MPEG</strong>.</span></span> <span data-ttu-id="a7eee-127">這個子類型可用於 MPEG-2 和 MPEG-2 音訊。</span><span class="sxs-lookup"><span data-stu-id="a7eee-127">This subtype is used for both MPEG-1 and MPEG-2 audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7eee-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="a7eee-129">每秒樣本數。</span><span class="sxs-lookup"><span data-stu-id="a7eee-129">Samples per second.</span></span></td>
<td><span data-ttu-id="a7eee-130">必要。</span><span class="sxs-lookup"><span data-stu-id="a7eee-130">Required.</span></span> <span data-ttu-id="a7eee-131">MPEG-2 和 MPEG-2 都支援下列值：</span><span class="sxs-lookup"><span data-stu-id="a7eee-131">The following values are supported for both MPEG-1 and MPEG-2:</span></span>
<ul>
<li><span data-ttu-id="a7eee-132">32000</span><span class="sxs-lookup"><span data-stu-id="a7eee-132">32000</span></span></li>
<li><span data-ttu-id="a7eee-133">44100</span><span class="sxs-lookup"><span data-stu-id="a7eee-133">44100</span></span></li>
<li><span data-ttu-id="a7eee-134">48000</span><span class="sxs-lookup"><span data-stu-id="a7eee-134">48000</span></span></li>
</ul>
<span data-ttu-id="a7eee-135">此外，MPEG-2 LSF 支援下列值：</span><span class="sxs-lookup"><span data-stu-id="a7eee-135">In addition, the following values are supported for MPEG-2 LSF:</span></span> <br/>
<ul>
<li><span data-ttu-id="a7eee-136">16000</span><span class="sxs-lookup"><span data-stu-id="a7eee-136">16000</span></span></li>
<li><span data-ttu-id="a7eee-137">22050</span><span class="sxs-lookup"><span data-stu-id="a7eee-137">22050</span></span></li>
<li><span data-ttu-id="a7eee-138">24000</span><span class="sxs-lookup"><span data-stu-id="a7eee-138">24000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7eee-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="a7eee-140">通道數目。</span><span class="sxs-lookup"><span data-stu-id="a7eee-140">Number of channels.</span></span></td>
<td><span data-ttu-id="a7eee-141">必要。</span><span class="sxs-lookup"><span data-stu-id="a7eee-141">Required.</span></span> <span data-ttu-id="a7eee-142">必須是 1 (mono) 或 2 (身歷聲) 。</span><span class="sxs-lookup"><span data-stu-id="a7eee-142">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7eee-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="a7eee-144">指定喇叭位置的音訊通道指派。</span><span class="sxs-lookup"><span data-stu-id="a7eee-144">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="a7eee-145">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a7eee-145">Optional.</span></span> <span data-ttu-id="a7eee-146">如果設定，則值必須是 0x3 (front 左方和右聲道) 或 0x4 (front center 頻道) 。</span><span class="sxs-lookup"><span data-stu-id="a7eee-146">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7eee-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="a7eee-148">編碼 MPEG 資料流程的位元速率（以每秒位元組數為單位）。</span><span class="sxs-lookup"><span data-stu-id="a7eee-148">Bit rate of the encoded MPEG stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="a7eee-149">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a7eee-149">Optional.</span></span><br/> <span data-ttu-id="a7eee-150">ISO/IEC 11172-3 和 ISO/IEC 13818-3 (LSF) 規格會根據取樣率、通道數目和音訊層 (1 或 2) ，定義數位費率。</span><span class="sxs-lookup"><span data-stu-id="a7eee-150">The ISO/IEC 11172-3 and ISO/IEC 13818-3 (LSF) specifications define several bit rates, depending on the sampling rate, the number of channels, and the audio layer (1 or 2).</span></span> <br/> <span data-ttu-id="a7eee-151">編碼器預設為第2層音訊。</span><span class="sxs-lookup"><span data-stu-id="a7eee-151">The encoder defaults to Layer 2 audio.</span></span> <span data-ttu-id="a7eee-152">如果未設定 <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> 屬性，則編碼器會使用下列預設的位元速率：</span><span class="sxs-lookup"><span data-stu-id="a7eee-152">If the <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> attribute is not set, the encoder uses the following default bit rates:</span></span><br/>
<ul>
<li><span data-ttu-id="a7eee-153">MPEG-1 身歷聲：每秒224000位 (bps) = 每秒28000位元組。</span><span class="sxs-lookup"><span data-stu-id="a7eee-153">MPEG-1 stereo: 224,000 bits per second (bps) = 28,000 bytes per second.</span></span></li>
<li><span data-ttu-id="a7eee-154">MPEG-2 mono： 192000 bps = 每秒24000位元組。</span><span class="sxs-lookup"><span data-stu-id="a7eee-154">MPEG-1 mono: 192,000 bps = 24,000 bytes per second.</span></span></li>
<li><span data-ttu-id="a7eee-155">MPEG-2 LSF、mono 或身歷聲： 160000 bps = 每秒20000位元組。</span><span class="sxs-lookup"><span data-stu-id="a7eee-155">MPEG-2 LSF, mono or stereo: 160,000 bps = 20,000 bytes per second.</span></span></li>
</ul>
<span data-ttu-id="a7eee-156">這個屬性可以設定為其他值。</span><span class="sxs-lookup"><span data-stu-id="a7eee-156">This attribute can be set to other values.</span></span> <span data-ttu-id="a7eee-157">如果根據 MPEG 規格，此值無效，則 MFT 會拒絕媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-157">If the value is not valid according to MPEG specifications, the MFT will reject the media type.</span></span><br/> <span data-ttu-id="a7eee-158">您也可以使用 <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> 介面來設定位元速率。</span><span class="sxs-lookup"><span data-stu-id="a7eee-158">You can also set the bit rate by using the <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> interface.</span></span> <span data-ttu-id="a7eee-159">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="a7eee-159">See Remarks for more information.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a7eee-160">如果未設定選用的屬性，編碼器會在設定類型之後，將它們新增至媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-160">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="a7eee-161">輸入類型</span><span class="sxs-lookup"><span data-stu-id="a7eee-161">Input Types</span></span>

<span data-ttu-id="a7eee-162">下表列出輸入媒體類型的必要和選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="a7eee-162">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7eee-163">屬性</span><span class="sxs-lookup"><span data-stu-id="a7eee-163">Attribute</span></span></th>
<th><span data-ttu-id="a7eee-164">描述</span><span class="sxs-lookup"><span data-stu-id="a7eee-164">Description</span></span></th>
<th><span data-ttu-id="a7eee-165">備註</span><span class="sxs-lookup"><span data-stu-id="a7eee-165">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7eee-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="a7eee-167">主要類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-167">Major type.</span></span></td>
<td><span data-ttu-id="a7eee-168">必要。</span><span class="sxs-lookup"><span data-stu-id="a7eee-168">Required.</span></span> <span data-ttu-id="a7eee-169">必須是 <strong>MFMediaType_Audio</strong>。</span><span class="sxs-lookup"><span data-stu-id="a7eee-169">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7eee-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="a7eee-171">音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-171">Audio subtype.</span></span></td>
<td><span data-ttu-id="a7eee-172">必要。</span><span class="sxs-lookup"><span data-stu-id="a7eee-172">Required.</span></span> <span data-ttu-id="a7eee-173">必須是 <strong>MFAudioFormat_PCM</strong> 或 <strong>MFAudioFormat_Float</strong>。</span><span class="sxs-lookup"><span data-stu-id="a7eee-173">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7eee-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="a7eee-175">每個音訊樣本的位數數目。</span><span class="sxs-lookup"><span data-stu-id="a7eee-175">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="a7eee-176">必要。</span><span class="sxs-lookup"><span data-stu-id="a7eee-176">Required.</span></span> <span data-ttu-id="a7eee-177">如果子類型為 <strong>MFAudioFormat_PCM</strong>，則值必須是16，如果是 <strong>MFAudioFormat_Float</strong>子類型，則為32。</span><span class="sxs-lookup"><span data-stu-id="a7eee-177">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7eee-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="a7eee-179">每秒樣本數。</span><span class="sxs-lookup"><span data-stu-id="a7eee-179">Samples per second.</span></span></td>
<td><span data-ttu-id="a7eee-180">必要。</span><span class="sxs-lookup"><span data-stu-id="a7eee-180">Required.</span></span> <span data-ttu-id="a7eee-181">必須符合輸出類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-181">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7eee-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="a7eee-183">通道數目。</span><span class="sxs-lookup"><span data-stu-id="a7eee-183">Number of channels.</span></span></td>
<td><span data-ttu-id="a7eee-184">必要。</span><span class="sxs-lookup"><span data-stu-id="a7eee-184">Required.</span></span> <span data-ttu-id="a7eee-185">必須符合輸出類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-185">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7eee-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="a7eee-187">區塊對齊（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a7eee-187">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="a7eee-188">必要。</span><span class="sxs-lookup"><span data-stu-id="a7eee-188">Required.</span></span> <span data-ttu-id="a7eee-189">計算值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a7eee-189">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="a7eee-190"><strong>MFAudioFormat_PCM</strong>：通道數目×2。</span><span class="sxs-lookup"><span data-stu-id="a7eee-190"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="a7eee-191"><strong>MFAudioFormat_Float</strong>：通道數目×4。</span><span class="sxs-lookup"><span data-stu-id="a7eee-191"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7eee-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="a7eee-193">編碼 AC3 資料流程的位元速率（以每秒位元組數為單位）。</span><span class="sxs-lookup"><span data-stu-id="a7eee-193">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="a7eee-194">必要。</span><span class="sxs-lookup"><span data-stu-id="a7eee-194">Required.</span></span> <span data-ttu-id="a7eee-195">每秒必須等於區塊對齊×樣本。</span><span class="sxs-lookup"><span data-stu-id="a7eee-195">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7eee-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="a7eee-197">指定喇叭位置的音訊通道指派。</span><span class="sxs-lookup"><span data-stu-id="a7eee-197">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="a7eee-198">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a7eee-198">Optional.</span></span> <span data-ttu-id="a7eee-199">如果設定，則值必須符合輸出類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-199">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7eee-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="a7eee-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="a7eee-201">每個音訊樣本中音訊資料的有效位數。</span><span class="sxs-lookup"><span data-stu-id="a7eee-201">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="a7eee-202">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a7eee-202">Optional.</span></span> <span data-ttu-id="a7eee-203">如果設定，此值必須等同于 <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>。</span><span class="sxs-lookup"><span data-stu-id="a7eee-203">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a7eee-204">編碼器不支援取樣率轉換或身歷聲/mono 轉換。</span><span class="sxs-lookup"><span data-stu-id="a7eee-204">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span> <span data-ttu-id="a7eee-205">如果未設定選用的屬性，編碼器會在設定類型之後，將它們新增至媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-205">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="a7eee-206">編解碼器屬性</span><span class="sxs-lookup"><span data-stu-id="a7eee-206">Codec Properties</span></span>

<span data-ttu-id="a7eee-207">編碼器透過 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a7eee-207">The encoder supports the following properties through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>



| <span data-ttu-id="a7eee-208">屬性</span><span class="sxs-lookup"><span data-stu-id="a7eee-208">Property</span></span>                                                                                | <span data-ttu-id="a7eee-209">描述</span><span class="sxs-lookup"><span data-stu-id="a7eee-209">Description</span></span>                                                                                      | <span data-ttu-id="a7eee-210">預設值</span><span class="sxs-lookup"><span data-stu-id="a7eee-210">Default value</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7eee-211">CODECAPI \_ AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="a7eee-211">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)               | <span data-ttu-id="a7eee-212">指定平均編碼的位元速率（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a7eee-212">Specifies the average encoded bit rate, in bits per second.</span></span>                                      | <span data-ttu-id="a7eee-213">如輸出媒體類型中適用于 [MF \_ MT \_ 音訊 \_ \_ \_ 每 \_ 秒平均位元組數](mf-mt-audio-avg-bytes-per-second-attribute.md) 屬性所述。</span><span class="sxs-lookup"><span data-stu-id="a7eee-213">As described for the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output media type.</span></span>                      |
| [<span data-ttu-id="a7eee-214">CODECAPI \_ AVEncMPACodingMode</span><span class="sxs-lookup"><span data-stu-id="a7eee-214">CODECAPI\_AVEncMPACodingMode</span></span>](../directshow/avencmpacodingmode-property.md)                       | <span data-ttu-id="a7eee-215">指定 MPEG 音訊編碼模式。</span><span class="sxs-lookup"><span data-stu-id="a7eee-215">Specifies the MPEG audio encoding mode.</span></span>                                                          | <span data-ttu-id="a7eee-216">雙聲道音訊的身歷聲，或1聲道音訊的單一通道。</span><span class="sxs-lookup"><span data-stu-id="a7eee-216">Stereo for 2-channel audio, or single channel for 1-channel audio.</span></span><br/> <span data-ttu-id="a7eee-217">針對雙聲道音訊，編碼器也支援雙重通道和聯合身歷聲。</span><span class="sxs-lookup"><span data-stu-id="a7eee-217">For 2-channel audio, the encoder also supports dual channel and joint stereo.</span></span><br/> |
| [<span data-ttu-id="a7eee-218">CODECAPI \_ AVEncMPACopyright</span><span class="sxs-lookup"><span data-stu-id="a7eee-218">CODECAPI\_AVEncMPACopyright</span></span>](../directshow/avencmpacopyright-property.md)                         | <span data-ttu-id="a7eee-219">指定是否要在 MPEG 音訊串流中設定著作權位。</span><span class="sxs-lookup"><span data-stu-id="a7eee-219">Specifies whether to set the copyright bit in the MPEG audio stream.</span></span>                             | <span data-ttu-id="a7eee-220">沒有著作權。</span><span class="sxs-lookup"><span data-stu-id="a7eee-220">No copyright.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="a7eee-221">CODECAPI \_ AVEncMPAEmphasisType</span><span class="sxs-lookup"><span data-stu-id="a7eee-221">CODECAPI\_AVEncMPAEmphasisType</span></span>](../directshow/avencmpaemphasistype-property.md)                   | <span data-ttu-id="a7eee-222">指定當編碼的資料流程解碼時，應使用的反強調篩選類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-222">Specifies the type of de-emphasis filter that should be used when the encoded stream is decoded.</span></span> | <span data-ttu-id="a7eee-223">未指定任何強調。</span><span class="sxs-lookup"><span data-stu-id="a7eee-223">No emphasis specified.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="a7eee-224">AVEncMPAEnableRedundancyProtection</span><span class="sxs-lookup"><span data-stu-id="a7eee-224">AVEncMPAEnableRedundancyProtection</span></span>](../directshow/avencmpaenableredundancyprotection-property.md) | <span data-ttu-id="a7eee-225">指定是否要將迴圈冗余檢查 (CRC) 新增至框架頁首。</span><span class="sxs-lookup"><span data-stu-id="a7eee-225">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span>                    | <span data-ttu-id="a7eee-226">CRC 總和檢查碼會寫入位資料流程。</span><span class="sxs-lookup"><span data-stu-id="a7eee-226">A CRC checksum is written to the bit stream.</span></span>                                                                                                                           |
| [<span data-ttu-id="a7eee-227">CODECAPI \_ AVEncMPALayer</span><span class="sxs-lookup"><span data-stu-id="a7eee-227">CODECAPI\_AVEncMPALayer</span></span>](../directshow/avencmpalayer-property.md)                                 | <span data-ttu-id="a7eee-228">指定 MPEG 音訊層。</span><span class="sxs-lookup"><span data-stu-id="a7eee-228">Specifies the MPEG audio layer.</span></span>                                                                  | <span data-ttu-id="a7eee-229">第2層音訊。</span><span class="sxs-lookup"><span data-stu-id="a7eee-229">Layer 2 audio.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="a7eee-230">CODECAPI \_ AVEncMPAOriginalBitstream</span><span class="sxs-lookup"><span data-stu-id="a7eee-230">CODECAPI\_AVEncMPAOriginalBitstream</span></span>](../directshow/avencmpaoriginalbitstream-property.md)         | <span data-ttu-id="a7eee-231">指定是否要針對 MPEG 音訊資料流程中的原始位進行設定。</span><span class="sxs-lookup"><span data-stu-id="a7eee-231">Specifies whether to set for the original bit in the MPEG audio stream.</span></span>                          | <span data-ttu-id="a7eee-232">「原始」位為 off。</span><span class="sxs-lookup"><span data-stu-id="a7eee-232">"Original" bit is off.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="a7eee-233">CODECAPI \_ AVEncMPAPrivateUserBit</span><span class="sxs-lookup"><span data-stu-id="a7eee-233">CODECAPI\_AVEncMPAPrivateUserBit</span></span>](../directshow/avencmpaprivateuserbit-property.md)               | <span data-ttu-id="a7eee-234">指定是否要針對 MPEG 音訊資料流程中的私用使用者位進行設定。</span><span class="sxs-lookup"><span data-stu-id="a7eee-234">Specifies whether to set for the private user bit in the MPEG audio stream.</span></span>                      | <span data-ttu-id="a7eee-235">私用使用者位為 off。</span><span class="sxs-lookup"><span data-stu-id="a7eee-235">Private user bit is off.</span></span>                                                                                                                                               |



 

<span data-ttu-id="a7eee-236">若要取得 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面的指標，請呼叫 MFT 上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="a7eee-236">To get a pointer to the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the MFT.</span></span>

<span data-ttu-id="a7eee-237">MFT 會執行下列 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 方法：</span><span class="sxs-lookup"><span data-stu-id="a7eee-237">The MFT implements the following [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods:</span></span>

-   [<span data-ttu-id="a7eee-238">**GetParameterRange**</span><span class="sxs-lookup"><span data-stu-id="a7eee-238">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="a7eee-239">**GetParameterValues**</span><span class="sxs-lookup"><span data-stu-id="a7eee-239">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [<span data-ttu-id="a7eee-240">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="a7eee-240">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="a7eee-241">**IsModifiable**</span><span class="sxs-lookup"><span data-stu-id="a7eee-241">**IsModifiable**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [<span data-ttu-id="a7eee-242">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="a7eee-242">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="a7eee-243">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="a7eee-243">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

<span data-ttu-id="a7eee-244">所有其他 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 方法都會傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="a7eee-244">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods return **E\_NOTIMPL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7eee-245">備註</span><span class="sxs-lookup"><span data-stu-id="a7eee-245">Remarks</span></span>

<span data-ttu-id="a7eee-246">每個 MPEG 音訊框架都包含 384 (第1層) 或 1152 (第2層) 每個頻道的音訊範例。</span><span class="sxs-lookup"><span data-stu-id="a7eee-246">Each MPEG audio frame contains either 384 (Layer 1) or 1152 (Layer 2) audio samples per channel.</span></span> <span data-ttu-id="a7eee-247">不過，編碼器的每個輸入緩衝區可能包含任意數目的 PCM 樣本。</span><span class="sxs-lookup"><span data-stu-id="a7eee-247">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="a7eee-248">每個輸入緩衝區的大小必須是區塊對齊的倍數。</span><span class="sxs-lookup"><span data-stu-id="a7eee-248">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="a7eee-249">編碼器會快取輸入範例，直到它對 MPEG 音訊框架足夠。</span><span class="sxs-lookup"><span data-stu-id="a7eee-249">The encoder caches input samples until it has enough for an MPEG audio frame.</span></span>

<span data-ttu-id="a7eee-250">每個輸出緩衝區都包含一個原始 MPEG 框架。</span><span class="sxs-lookup"><span data-stu-id="a7eee-250">Each output buffer contains one raw MPEG frame.</span></span> <span data-ttu-id="a7eee-251">每個輸出緩衝區的大小取決於位元速率和取樣率。</span><span class="sxs-lookup"><span data-stu-id="a7eee-251">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

### <a name="configuring-the-encoder"></a><span data-ttu-id="a7eee-252">設定編碼器</span><span class="sxs-lookup"><span data-stu-id="a7eee-252">Configuring the Encoder</span></span>

<span data-ttu-id="a7eee-253">若要變更編碼器上的任何預設設定，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="a7eee-253">To change any of the default settings on the encoder, perform the following steps:</span></span>

1.  <span data-ttu-id="a7eee-254">建立編碼器 MFT 的實例。</span><span class="sxs-lookup"><span data-stu-id="a7eee-254">Create an instance of the encoder MFT.</span></span>
2.  <span data-ttu-id="a7eee-255">呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) ，以取得慣用的輸出類型清單。</span><span class="sxs-lookup"><span data-stu-id="a7eee-255">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of the preferred output types.</span></span> <span data-ttu-id="a7eee-256">編碼器會列舉 mono 和身歷聲的所有採樣速率。</span><span class="sxs-lookup"><span data-stu-id="a7eee-256">The encoder enumerates all sample rates for both mono and stereo.</span></span> <span data-ttu-id="a7eee-257">根據取樣率和通道數目，選取其中一種媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-257">Select one of these media types, based on the sample rate and number of channels.</span></span> <span data-ttu-id="a7eee-258">[ [MF \_ MT \_ 音訊 \_ \_ \_ 每 \_ 秒平均位元組數](mf-mt-audio-avg-bytes-per-second-attribute.md) ] 屬性工作表示預設的位元速率（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a7eee-258">The [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute indicates the default bit rate, in bytes per second.</span></span>
3.  <span data-ttu-id="a7eee-259">選擇性：您可以針對輸出媒體類型上的 [MF \_ MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_ ](mf-mt-audio-avg-bytes-per-second-attribute.md) 設定新的值，以覆寫預設的位元速率。</span><span class="sxs-lookup"><span data-stu-id="a7eee-259">Optional: You can override the default bit rate by setting a new value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) on the output media type.</span></span> <span data-ttu-id="a7eee-260">有效的位元速率取決於取樣率、通道數目和音訊層。</span><span class="sxs-lookup"><span data-stu-id="a7eee-260">Valid bit rates depend on the sample rate, number of channels, and audio layer.</span></span>
    > [!Note]  
    > <span data-ttu-id="a7eee-261">在設定程式的這個階段中，編碼器會預設為第2層音訊，而且只會接受第2層的位元速率。</span><span class="sxs-lookup"><span data-stu-id="a7eee-261">At this point in the configuration process, the encoder defaults to Layer 2 audio and will only accept Layer 2 bit rates.</span></span> <span data-ttu-id="a7eee-262">您將能夠在稍後的步驟中，將編碼器切換至第1層 (請參閱步驟 7) 。</span><span class="sxs-lookup"><span data-stu-id="a7eee-262">You will be able to switch the encoder to Layer 1 in a later step (see step 7).</span></span> <span data-ttu-id="a7eee-263">在這種情況下，請立即保留預設的位元速率;您可以在步驟8中再次加以變更。</span><span class="sxs-lookup"><span data-stu-id="a7eee-263">In that case, leave the default bit rate for now; you can change it again in step 8.</span></span>

     

4.  <span data-ttu-id="a7eee-264">呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-264">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the output media type.</span></span> <span data-ttu-id="a7eee-265">如果您為 [ \_ \_ \_ \_ \_ 每 \_ 秒的 MF MT 音訊平均位元組](mf-mt-audio-avg-bytes-per-second-attribute.md) 設定您自己的值，而 MFT 拒絕輸出媒體類型，可能是因為您指定了不正確位元速率。</span><span class="sxs-lookup"><span data-stu-id="a7eee-265">If you set your own value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) and the MFT rejects the output media type, it is likely because you specified an invalid bit rate.</span></span>
5.  <span data-ttu-id="a7eee-266">呼叫 [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) 來列舉輸入媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-266">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to enumerate the input media type.</span></span> <span data-ttu-id="a7eee-267">由於取樣率和通道數目必須與輸出類型相同，因此只會列舉兩個選項：32位浮點 PCM 輸入和16位整數 PCM 輸入。</span><span class="sxs-lookup"><span data-stu-id="a7eee-267">Because the sample rate and number of channels must be identical to the output type, only two options are enumerated: 32-bit floating-point PCM input and 16-bit integer PCM input.</span></span> <span data-ttu-id="a7eee-268">選取其中一個。</span><span class="sxs-lookup"><span data-stu-id="a7eee-268">Select one of these.</span></span>
6.  <span data-ttu-id="a7eee-269">呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 來設定輸入媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-269">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the input media type.</span></span>
7.  <span data-ttu-id="a7eee-270">選擇性：若要編碼第1層音訊，請將 [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md) 屬性設定為 **eAVEncMPALayer \_ 1**。</span><span class="sxs-lookup"><span data-stu-id="a7eee-270">Optional: To encode Layer 1 audio, set the [CODECAPI\_AVEncMPALayer](../directshow/avencmpalayer-property.md) property to **eAVEncMPALayer\_1**.</span></span>
8.  <span data-ttu-id="a7eee-271">選擇性：若要變更位元速率，請設定 [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7eee-271">Optional: To change the bit rate, set the [CODECAPI\_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <span data-ttu-id="a7eee-272">位元速率必須是 MPEG-2 或 MPEG-2 LSF 規格中所列的其中一個有效位速度。</span><span class="sxs-lookup"><span data-stu-id="a7eee-272">The bit rate must be one of the valid bit rates listed in the MPEG-1 or MPEG-2 LSF specifications.</span></span> <span data-ttu-id="a7eee-273">或者，您也可以呼叫 [**ICodecAPI：： GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) ，以根據目前的設定取得有效位速率的清單。</span><span class="sxs-lookup"><span data-stu-id="a7eee-273">Alternatively, you can call [**ICodecAPI::GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) to get a list of valid bit rates, based on the current settings.</span></span>
9.  <span data-ttu-id="a7eee-274">選擇性：使用2聲道音訊，您可以設定 [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) 屬性，將編碼模式變更為雙聲道或結合身歷聲。</span><span class="sxs-lookup"><span data-stu-id="a7eee-274">Optional: With 2-channel audio, you can set the [CODECAPI\_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) property to change the coding mode to dual channel or joint stereo.</span></span> <span data-ttu-id="a7eee-275">您可以呼叫 [**ICodecAPI：： GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) 來取得有效的選項。</span><span class="sxs-lookup"><span data-stu-id="a7eee-275">You can call [**ICodecAPI::GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) to get the valid options.</span></span> <span data-ttu-id="a7eee-276"> (1 聲道音訊，唯一的選項是 mono。 ) </span><span class="sxs-lookup"><span data-stu-id="a7eee-276">(For 1-channel audio, the only option is mono.)</span></span>
10. <span data-ttu-id="a7eee-277">選擇性：設定先前所列的其他任何 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 屬性。</span><span class="sxs-lookup"><span data-stu-id="a7eee-277">Optional: Set any of the other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties listed previously.</span></span>

<span data-ttu-id="a7eee-278">請務必遵循這些步驟的順序。</span><span class="sxs-lookup"><span data-stu-id="a7eee-278">It is important to follow the order of these steps.</span></span> <span data-ttu-id="a7eee-279">尤其是在變更任何 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 屬性之前，請先設定輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a7eee-279">In particular, set the output media type before changing any [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties.</span></span> <span data-ttu-id="a7eee-280">此外，您必須先設定 **ICodecAPI** 屬性，然後再接收第一個輸入範例。</span><span class="sxs-lookup"><span data-stu-id="a7eee-280">Also, you must set **ICodecAPI** properties before the MFT receives the first input sample.</span></span> <span data-ttu-id="a7eee-281">在 MFT 收到輸入之後，編解碼器屬性會是唯讀的，而 [**ICodecAPI：： SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) 會傳回值 **\_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a7eee-281">After the MFT receives input, the codec properties are read-only, and [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) returns the value **S\_FALSE**.</span></span>

### <a name="supported-bit-rates"></a><span data-ttu-id="a7eee-282">支援的位元速率</span><span class="sxs-lookup"><span data-stu-id="a7eee-282">Supported Bit Rates</span></span>

<span data-ttu-id="a7eee-283">編碼器支援下列位元速率。</span><span class="sxs-lookup"><span data-stu-id="a7eee-283">The encoder supports the following bit rates.</span></span>



<span data-ttu-id="a7eee-284">MPEG-1</span><span class="sxs-lookup"><span data-stu-id="a7eee-284">MPEG-1</span></span>

<span data-ttu-id="a7eee-285">MPEG-2</span><span class="sxs-lookup"><span data-stu-id="a7eee-285">MPEG-2</span></span>

<span data-ttu-id="a7eee-286">第1層</span><span class="sxs-lookup"><span data-stu-id="a7eee-286">Layer 1</span></span>

<span data-ttu-id="a7eee-287">第2層</span><span class="sxs-lookup"><span data-stu-id="a7eee-287">Layer 2</span></span>

<span data-ttu-id="a7eee-288">第1層</span><span class="sxs-lookup"><span data-stu-id="a7eee-288">Layer 1</span></span>

<span data-ttu-id="a7eee-289">第2層</span><span class="sxs-lookup"><span data-stu-id="a7eee-289">Layer 2</span></span>

<span data-ttu-id="a7eee-290">32</span><span class="sxs-lookup"><span data-stu-id="a7eee-290">32</span></span>

<span data-ttu-id="a7eee-291">32\*</span><span class="sxs-lookup"><span data-stu-id="a7eee-291">32\*</span></span>

<span data-ttu-id="a7eee-292">32</span><span class="sxs-lookup"><span data-stu-id="a7eee-292">32</span></span>

<span data-ttu-id="a7eee-293">8</span><span class="sxs-lookup"><span data-stu-id="a7eee-293">8</span></span>

<span data-ttu-id="a7eee-294">64</span><span class="sxs-lookup"><span data-stu-id="a7eee-294">64</span></span>

<span data-ttu-id="a7eee-295">48\*</span><span class="sxs-lookup"><span data-stu-id="a7eee-295">48\*</span></span>

<span data-ttu-id="a7eee-296">38</span><span class="sxs-lookup"><span data-stu-id="a7eee-296">38</span></span>

<span data-ttu-id="a7eee-297">16</span><span class="sxs-lookup"><span data-stu-id="a7eee-297">16</span></span>

<span data-ttu-id="a7eee-298">96</span><span class="sxs-lookup"><span data-stu-id="a7eee-298">96</span></span>

<span data-ttu-id="a7eee-299">56\*</span><span class="sxs-lookup"><span data-stu-id="a7eee-299">56\*</span></span>

<span data-ttu-id="a7eee-300">56</span><span class="sxs-lookup"><span data-stu-id="a7eee-300">56</span></span>

<span data-ttu-id="a7eee-301">24</span><span class="sxs-lookup"><span data-stu-id="a7eee-301">24</span></span>

<span data-ttu-id="a7eee-302">128</span><span class="sxs-lookup"><span data-stu-id="a7eee-302">128</span></span>

<span data-ttu-id="a7eee-303">64</span><span class="sxs-lookup"><span data-stu-id="a7eee-303">64</span></span>

<span data-ttu-id="a7eee-304">64</span><span class="sxs-lookup"><span data-stu-id="a7eee-304">64</span></span>

<span data-ttu-id="a7eee-305">32</span><span class="sxs-lookup"><span data-stu-id="a7eee-305">32</span></span>

<span data-ttu-id="a7eee-306">160</span><span class="sxs-lookup"><span data-stu-id="a7eee-306">160</span></span>

<span data-ttu-id="a7eee-307">80\*</span><span class="sxs-lookup"><span data-stu-id="a7eee-307">80\*</span></span>

<span data-ttu-id="a7eee-308">80</span><span class="sxs-lookup"><span data-stu-id="a7eee-308">80</span></span>

<span data-ttu-id="a7eee-309">40</span><span class="sxs-lookup"><span data-stu-id="a7eee-309">40</span></span>

<span data-ttu-id="a7eee-310">192</span><span class="sxs-lookup"><span data-stu-id="a7eee-310">192</span></span>

<span data-ttu-id="a7eee-311">96</span><span class="sxs-lookup"><span data-stu-id="a7eee-311">96</span></span>

<span data-ttu-id="a7eee-312">96</span><span class="sxs-lookup"><span data-stu-id="a7eee-312">96</span></span>

<span data-ttu-id="a7eee-313">48</span><span class="sxs-lookup"><span data-stu-id="a7eee-313">48</span></span>

<span data-ttu-id="a7eee-314">224</span><span class="sxs-lookup"><span data-stu-id="a7eee-314">224</span></span>

<span data-ttu-id="a7eee-315">112</span><span class="sxs-lookup"><span data-stu-id="a7eee-315">112</span></span>

<span data-ttu-id="a7eee-316">112</span><span class="sxs-lookup"><span data-stu-id="a7eee-316">112</span></span>

<span data-ttu-id="a7eee-317">56</span><span class="sxs-lookup"><span data-stu-id="a7eee-317">56</span></span>

<span data-ttu-id="a7eee-318">256</span><span class="sxs-lookup"><span data-stu-id="a7eee-318">256</span></span>

<span data-ttu-id="a7eee-319">128</span><span class="sxs-lookup"><span data-stu-id="a7eee-319">128</span></span>

<span data-ttu-id="a7eee-320">128</span><span class="sxs-lookup"><span data-stu-id="a7eee-320">128</span></span>

<span data-ttu-id="a7eee-321">64</span><span class="sxs-lookup"><span data-stu-id="a7eee-321">64</span></span>

<span data-ttu-id="a7eee-322">288</span><span class="sxs-lookup"><span data-stu-id="a7eee-322">288</span></span>

<span data-ttu-id="a7eee-323">160</span><span class="sxs-lookup"><span data-stu-id="a7eee-323">160</span></span>

<span data-ttu-id="a7eee-324">144</span><span class="sxs-lookup"><span data-stu-id="a7eee-324">144</span></span>

<span data-ttu-id="a7eee-325">80</span><span class="sxs-lookup"><span data-stu-id="a7eee-325">80</span></span>

<span data-ttu-id="a7eee-326">320</span><span class="sxs-lookup"><span data-stu-id="a7eee-326">320</span></span>

<span data-ttu-id="a7eee-327">192</span><span class="sxs-lookup"><span data-stu-id="a7eee-327">192</span></span>

<span data-ttu-id="a7eee-328">160</span><span class="sxs-lookup"><span data-stu-id="a7eee-328">160</span></span>

<span data-ttu-id="a7eee-329">96</span><span class="sxs-lookup"><span data-stu-id="a7eee-329">96</span></span>

<span data-ttu-id="a7eee-330">352</span><span class="sxs-lookup"><span data-stu-id="a7eee-330">352</span></span>

<span data-ttu-id="a7eee-331">224\*\*</span><span class="sxs-lookup"><span data-stu-id="a7eee-331">224\*\*</span></span>

<span data-ttu-id="a7eee-332">176</span><span class="sxs-lookup"><span data-stu-id="a7eee-332">176</span></span>

<span data-ttu-id="a7eee-333">112</span><span class="sxs-lookup"><span data-stu-id="a7eee-333">112</span></span>

<span data-ttu-id="a7eee-334">384</span><span class="sxs-lookup"><span data-stu-id="a7eee-334">384</span></span>

<span data-ttu-id="a7eee-335">256\*\*</span><span class="sxs-lookup"><span data-stu-id="a7eee-335">256\*\*</span></span>

<span data-ttu-id="a7eee-336">192</span><span class="sxs-lookup"><span data-stu-id="a7eee-336">192</span></span>

<span data-ttu-id="a7eee-337">128</span><span class="sxs-lookup"><span data-stu-id="a7eee-337">128</span></span>

<span data-ttu-id="a7eee-338">416</span><span class="sxs-lookup"><span data-stu-id="a7eee-338">416</span></span>

<span data-ttu-id="a7eee-339">230\*\*</span><span class="sxs-lookup"><span data-stu-id="a7eee-339">230\*\*</span></span>

<span data-ttu-id="a7eee-340">224</span><span class="sxs-lookup"><span data-stu-id="a7eee-340">224</span></span>

<span data-ttu-id="a7eee-341">144</span><span class="sxs-lookup"><span data-stu-id="a7eee-341">144</span></span>

<span data-ttu-id="a7eee-342">448</span><span class="sxs-lookup"><span data-stu-id="a7eee-342">448</span></span>

<span data-ttu-id="a7eee-343">384\*\*</span><span class="sxs-lookup"><span data-stu-id="a7eee-343">384\*\*</span></span>

<span data-ttu-id="a7eee-344">256</span><span class="sxs-lookup"><span data-stu-id="a7eee-344">256</span></span>

<span data-ttu-id="a7eee-345">160</span><span class="sxs-lookup"><span data-stu-id="a7eee-345">160</span></span>



 

<dl> <span data-ttu-id="a7eee-346">\* 僅限 Mono</span><span class="sxs-lookup"><span data-stu-id="a7eee-346">\* Mono only</span></span>  
<span data-ttu-id="a7eee-347">\*\* 僅限身歷聲</span><span class="sxs-lookup"><span data-stu-id="a7eee-347">\*\* Stereo only</span></span>  
</dl>

### <a name="example-media-types"></a><span data-ttu-id="a7eee-348">範例媒體類型</span><span class="sxs-lookup"><span data-stu-id="a7eee-348">Example Media Types</span></span>

<span data-ttu-id="a7eee-349">以下是將16位整數 PCM 編碼的媒體類型範例，以預設位元速率編碼的 48-kHz 身歷聲音訊。</span><span class="sxs-lookup"><span data-stu-id="a7eee-349">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate.</span></span>

<span data-ttu-id="a7eee-350">輸出媒體類型：</span><span class="sxs-lookup"><span data-stu-id="a7eee-350">Output media type:</span></span>

| <span data-ttu-id="a7eee-351">屬性</span><span class="sxs-lookup"><span data-stu-id="a7eee-351">Attribute</span></span>                                                                           | <span data-ttu-id="a7eee-352">值</span><span class="sxs-lookup"><span data-stu-id="a7eee-352">Value</span></span>                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [<span data-ttu-id="a7eee-353">MF \_ MT \_ 主要 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="a7eee-353">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="a7eee-354">**MFMediaType \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="a7eee-354">**MFMediaType\_Audio**</span></span>  |
| [<span data-ttu-id="a7eee-355">MF \_ MT \_ 子類型</span><span class="sxs-lookup"><span data-stu-id="a7eee-355">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="a7eee-356">**MFAudioFormat \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="a7eee-356">**MFAudioFormat\_MPEG**</span></span> |
| [<span data-ttu-id="a7eee-357">\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_</span><span class="sxs-lookup"><span data-stu-id="a7eee-357">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="a7eee-358">48000</span><span class="sxs-lookup"><span data-stu-id="a7eee-358">48000</span></span>                   |
| [<span data-ttu-id="a7eee-359">MF \_ MT \_ 音訊 \_ 數目 \_ 通道</span><span class="sxs-lookup"><span data-stu-id="a7eee-359">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="a7eee-360">2</span><span class="sxs-lookup"><span data-stu-id="a7eee-360">2</span></span>                       |



 

<span data-ttu-id="a7eee-361">輸入媒體類型：</span><span class="sxs-lookup"><span data-stu-id="a7eee-361">Input media type:</span></span>

| <span data-ttu-id="a7eee-362">屬性</span><span class="sxs-lookup"><span data-stu-id="a7eee-362">Attribute</span></span>                                                                                | <span data-ttu-id="a7eee-363">值</span><span class="sxs-lookup"><span data-stu-id="a7eee-363">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="a7eee-364">MF \_ MT \_ 主要 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="a7eee-364">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="a7eee-365">**MFMediaType \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="a7eee-365">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="a7eee-366">MF \_ MT \_ 子類型</span><span class="sxs-lookup"><span data-stu-id="a7eee-366">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="a7eee-367">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="a7eee-367">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="a7eee-368">\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數</span><span class="sxs-lookup"><span data-stu-id="a7eee-368">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="a7eee-369">16</span><span class="sxs-lookup"><span data-stu-id="a7eee-369">16</span></span>                     |
| [<span data-ttu-id="a7eee-370">\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_</span><span class="sxs-lookup"><span data-stu-id="a7eee-370">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="a7eee-371">48000</span><span class="sxs-lookup"><span data-stu-id="a7eee-371">48000</span></span>                  |
| [<span data-ttu-id="a7eee-372">MF \_ MT \_ 音訊 \_ 數目 \_ 通道</span><span class="sxs-lookup"><span data-stu-id="a7eee-372">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="a7eee-373">2</span><span class="sxs-lookup"><span data-stu-id="a7eee-373">2</span></span>                      |
| [<span data-ttu-id="a7eee-374">MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊</span><span class="sxs-lookup"><span data-stu-id="a7eee-374">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="a7eee-375">4</span><span class="sxs-lookup"><span data-stu-id="a7eee-375">4</span></span>                      |
| [<span data-ttu-id="a7eee-376">\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_</span><span class="sxs-lookup"><span data-stu-id="a7eee-376">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="a7eee-377">192000</span><span class="sxs-lookup"><span data-stu-id="a7eee-377">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="a7eee-378">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7eee-378">Requirements</span></span>



| <span data-ttu-id="a7eee-379">需求</span><span class="sxs-lookup"><span data-stu-id="a7eee-379">Requirement</span></span> | <span data-ttu-id="a7eee-380">值</span><span class="sxs-lookup"><span data-stu-id="a7eee-380">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7eee-381">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7eee-381">Minimum supported client</span></span><br/> | <span data-ttu-id="a7eee-382">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7eee-382">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a7eee-383">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7eee-383">Minimum supported server</span></span><br/> | <span data-ttu-id="a7eee-384">都不支援</span><span class="sxs-lookup"><span data-stu-id="a7eee-384">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="a7eee-385">DLL</span><span class="sxs-lookup"><span data-stu-id="a7eee-385">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7eee-386"><dt>Msmpeg2enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7eee-386"><dt>Msmpeg2enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7eee-387">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7eee-387">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7eee-388">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="a7eee-388">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
