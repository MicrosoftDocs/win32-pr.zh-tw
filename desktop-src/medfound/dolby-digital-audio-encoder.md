---
description: 杜比音訊編碼器是媒體基礎轉換 (MFT) 將 mono 或身歷聲音訊編碼為杜比數位，也稱為杜比 AC-3。
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: 杜比數位音訊編碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f901587b816bc17d62f4095e093b661ce55f0009
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153561"
---
# <a name="dolby-digital-audio-encoder"></a><span data-ttu-id="d39b0-103">杜比數位音訊編碼器</span><span class="sxs-lookup"><span data-stu-id="d39b0-103">Dolby Digital Audio Encoder</span></span>

<span data-ttu-id="d39b0-104">杜比音訊編碼器是 [媒體基礎轉換](media-foundation-transforms.md) (MFT) 將 mono 或身歷聲音訊編碼為杜比數位，也稱為杜比 AC-3。</span><span class="sxs-lookup"><span data-stu-id="d39b0-104">The Dolby audio encoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that encodes mono or stereo audio to Dolby Digital, also called Dolby AC-3.</span></span> <span data-ttu-id="d39b0-105">編碼器不支援多重通道輸入，例如5.1 通道設定。</span><span class="sxs-lookup"><span data-stu-id="d39b0-105">The encoder does not support multi-channel input, such as the 5.1 channel configuration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d39b0-106">在 Windows 8 之前的 Windows 版本中，Microsoft 應用程式所使用的杜比數位授權方案會限制 Microsoft 的杜比數位技術。</span><span class="sxs-lookup"><span data-stu-id="d39b0-106">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="d39b0-107">如需有關杜比數位音訊的詳細資訊，請參閱 Advanced 電視 Systems 委員會 (ATSC) 檔 *數位音訊壓縮標準 (AC-3、E-AC-3) 修訂 B*。</span><span class="sxs-lookup"><span data-stu-id="d39b0-107">For more information about Dolby Digital audio, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="d39b0-108">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="d39b0-108">Class Identifier</span></span>

<span data-ttu-id="d39b0-109">[杜比音訊編碼器] (CLSID) 的類別識別碼是 **clsid \_ CMSDolbyDigitalEncMFT**，定義于標頭檔 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="d39b0-109">The class identifier (CLSID) of the Dolby audio encoder is **CLSID\_CMSDolbyDigitalEncMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="d39b0-110">輸出型別</span><span class="sxs-lookup"><span data-stu-id="d39b0-110">Output Types</span></span>

<span data-ttu-id="d39b0-111">在輸入類型之前，必須先設定輸出類型。</span><span class="sxs-lookup"><span data-stu-id="d39b0-111">The output type must be set first, before the input type.</span></span> <span data-ttu-id="d39b0-112">下表列出輸出媒體類型的必要和選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="d39b0-112">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d39b0-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d39b0-113">Attribute</span></span></th>
<th><span data-ttu-id="d39b0-114">描述</span><span class="sxs-lookup"><span data-stu-id="d39b0-114">Description</span></span></th>
<th><span data-ttu-id="d39b0-115">備註</span><span class="sxs-lookup"><span data-stu-id="d39b0-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d39b0-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="d39b0-117">主要類型。</span><span class="sxs-lookup"><span data-stu-id="d39b0-117">Major type.</span></span></td>
<td><span data-ttu-id="d39b0-118">必要。</span><span class="sxs-lookup"><span data-stu-id="d39b0-118">Required.</span></span> <span data-ttu-id="d39b0-119">必須是 <strong>MFMediaType_Audio</strong>。</span><span class="sxs-lookup"><span data-stu-id="d39b0-119">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d39b0-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="d39b0-121">音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="d39b0-121">Audio subtype.</span></span></td>
<td><span data-ttu-id="d39b0-122">必要。</span><span class="sxs-lookup"><span data-stu-id="d39b0-122">Required.</span></span> <span data-ttu-id="d39b0-123">必須是 <strong>MFAudioFormat_Dolby_AC3</strong>。</span><span class="sxs-lookup"><span data-stu-id="d39b0-123">Must be <strong>MFAudioFormat_Dolby_AC3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d39b0-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="d39b0-125">每秒樣本數。</span><span class="sxs-lookup"><span data-stu-id="d39b0-125">Samples per second.</span></span></td>
<td><span data-ttu-id="d39b0-126">必要。</span><span class="sxs-lookup"><span data-stu-id="d39b0-126">Required.</span></span> <span data-ttu-id="d39b0-127">支援下列值：</span><span class="sxs-lookup"><span data-stu-id="d39b0-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="d39b0-128">32000</span><span class="sxs-lookup"><span data-stu-id="d39b0-128">32000</span></span></li>
<li><span data-ttu-id="d39b0-129">44100</span><span class="sxs-lookup"><span data-stu-id="d39b0-129">44100</span></span></li>
<li><span data-ttu-id="d39b0-130">48000</span><span class="sxs-lookup"><span data-stu-id="d39b0-130">48000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d39b0-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="d39b0-132">通道數目。</span><span class="sxs-lookup"><span data-stu-id="d39b0-132">Number of channels.</span></span></td>
<td><span data-ttu-id="d39b0-133">必要。</span><span class="sxs-lookup"><span data-stu-id="d39b0-133">Required.</span></span> <span data-ttu-id="d39b0-134">必須是 1 (mono) 或 2 (身歷聲) 。</span><span class="sxs-lookup"><span data-stu-id="d39b0-134">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d39b0-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="d39b0-136">指定喇叭位置的音訊通道指派。</span><span class="sxs-lookup"><span data-stu-id="d39b0-136">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="d39b0-137">選擇性。</span><span class="sxs-lookup"><span data-stu-id="d39b0-137">Optional.</span></span> <span data-ttu-id="d39b0-138">如果設定，則值必須是 0x3 (front 左方和右聲道) 或 0x4 (front center 頻道) 。</span><span class="sxs-lookup"><span data-stu-id="d39b0-138">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d39b0-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="d39b0-140">編碼的 AC-3 串流的位元速率（以每秒位元組數為單位）。</span><span class="sxs-lookup"><span data-stu-id="d39b0-140">Bit rate of the encoded AC-3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="d39b0-141">選擇性。</span><span class="sxs-lookup"><span data-stu-id="d39b0-141">Optional.</span></span> <span data-ttu-id="d39b0-142">請參閱備註中的有效值。</span><span class="sxs-lookup"><span data-stu-id="d39b0-142">See Remarks for valid values.</span></span> <span data-ttu-id="d39b0-143">如果未設定此屬性，則編碼器會使用預設的位元速率，如備註中所述。</span><span class="sxs-lookup"><span data-stu-id="d39b0-143">If this attribute is not set, the encoder uses a default bit rate, as described in Remarks.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d39b0-144">如果未設定選用的屬性，編碼器會在設定類型之後，將它們新增至媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d39b0-144">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="d39b0-145">輸入類型</span><span class="sxs-lookup"><span data-stu-id="d39b0-145">Input Types</span></span>

<span data-ttu-id="d39b0-146">下表列出輸入媒體類型的必要和選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="d39b0-146">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d39b0-147">屬性</span><span class="sxs-lookup"><span data-stu-id="d39b0-147">Attribute</span></span></th>
<th><span data-ttu-id="d39b0-148">描述</span><span class="sxs-lookup"><span data-stu-id="d39b0-148">Description</span></span></th>
<th><span data-ttu-id="d39b0-149">備註</span><span class="sxs-lookup"><span data-stu-id="d39b0-149">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d39b0-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="d39b0-151">主要類型。</span><span class="sxs-lookup"><span data-stu-id="d39b0-151">Major type.</span></span></td>
<td><span data-ttu-id="d39b0-152">必要。</span><span class="sxs-lookup"><span data-stu-id="d39b0-152">Required.</span></span> <span data-ttu-id="d39b0-153">必須是 <strong>MFMediaType_Audio</strong>。</span><span class="sxs-lookup"><span data-stu-id="d39b0-153">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d39b0-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="d39b0-155">音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="d39b0-155">Audio subtype.</span></span></td>
<td><span data-ttu-id="d39b0-156">必要。</span><span class="sxs-lookup"><span data-stu-id="d39b0-156">Required.</span></span> <span data-ttu-id="d39b0-157">必須是 <strong>MFAudioFormat_PCM</strong> 或 <strong>MFAudioFormat_Float</strong>。</span><span class="sxs-lookup"><span data-stu-id="d39b0-157">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d39b0-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="d39b0-159">每個音訊樣本的位數數目。</span><span class="sxs-lookup"><span data-stu-id="d39b0-159">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="d39b0-160">必要。</span><span class="sxs-lookup"><span data-stu-id="d39b0-160">Required.</span></span> <span data-ttu-id="d39b0-161">如果子類型為 <strong>MFAudioFormat_PCM</strong>，則值必須是16，如果是 <strong>MFAudioFormat_Float</strong>子類型，則為32。</span><span class="sxs-lookup"><span data-stu-id="d39b0-161">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d39b0-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="d39b0-163">每秒樣本數。</span><span class="sxs-lookup"><span data-stu-id="d39b0-163">Samples per second.</span></span></td>
<td><span data-ttu-id="d39b0-164">必要。</span><span class="sxs-lookup"><span data-stu-id="d39b0-164">Required.</span></span> <span data-ttu-id="d39b0-165">必須符合輸出類型。</span><span class="sxs-lookup"><span data-stu-id="d39b0-165">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d39b0-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="d39b0-167">通道數目。</span><span class="sxs-lookup"><span data-stu-id="d39b0-167">Number of channels.</span></span></td>
<td><span data-ttu-id="d39b0-168">必要。</span><span class="sxs-lookup"><span data-stu-id="d39b0-168">Required.</span></span> <span data-ttu-id="d39b0-169">必須符合輸出類型。</span><span class="sxs-lookup"><span data-stu-id="d39b0-169">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d39b0-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="d39b0-171">區塊對齊（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d39b0-171">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="d39b0-172">必要。</span><span class="sxs-lookup"><span data-stu-id="d39b0-172">Required.</span></span> <span data-ttu-id="d39b0-173">計算值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d39b0-173">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="d39b0-174"><strong>MFAudioFormat_PCM</strong>：通道數目×2。</span><span class="sxs-lookup"><span data-stu-id="d39b0-174"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="d39b0-175"><strong>MFAudioFormat_Float</strong>：通道數目×4。</span><span class="sxs-lookup"><span data-stu-id="d39b0-175"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d39b0-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="d39b0-177">編碼 AC3 資料流程的位元速率（以每秒位元組數為單位）。</span><span class="sxs-lookup"><span data-stu-id="d39b0-177">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="d39b0-178">必要。</span><span class="sxs-lookup"><span data-stu-id="d39b0-178">Required.</span></span> <span data-ttu-id="d39b0-179">每秒必須等於區塊對齊×樣本。</span><span class="sxs-lookup"><span data-stu-id="d39b0-179">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d39b0-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="d39b0-181">指定喇叭位置的音訊通道指派。</span><span class="sxs-lookup"><span data-stu-id="d39b0-181">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="d39b0-182">選擇性。</span><span class="sxs-lookup"><span data-stu-id="d39b0-182">Optional.</span></span> <span data-ttu-id="d39b0-183">如果設定，則值必須符合輸出類型。</span><span class="sxs-lookup"><span data-stu-id="d39b0-183">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d39b0-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="d39b0-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="d39b0-185">每個音訊樣本中音訊資料的有效位數。</span><span class="sxs-lookup"><span data-stu-id="d39b0-185">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="d39b0-186">選擇性。</span><span class="sxs-lookup"><span data-stu-id="d39b0-186">Optional.</span></span> <span data-ttu-id="d39b0-187">如果設定，此值必須等同于 <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>。</span><span class="sxs-lookup"><span data-stu-id="d39b0-187">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d39b0-188">編碼器不支援取樣率轉換或身歷聲/mono 轉換。</span><span class="sxs-lookup"><span data-stu-id="d39b0-188">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span>

## <a name="remarks"></a><span data-ttu-id="d39b0-189">備註</span><span class="sxs-lookup"><span data-stu-id="d39b0-189">Remarks</span></span>

<span data-ttu-id="d39b0-190">每一頻道的每一台 AC 3 音訊框架包含1536個音訊範例。</span><span class="sxs-lookup"><span data-stu-id="d39b0-190">Each Dolby AC-3 audio frame contains 1536 audio samples per channel.</span></span> <span data-ttu-id="d39b0-191">不過，編碼器的每個輸入緩衝區可能包含任意數目的 PCM 樣本。</span><span class="sxs-lookup"><span data-stu-id="d39b0-191">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="d39b0-192">每個輸入緩衝區的大小必須是區塊對齊的倍數。</span><span class="sxs-lookup"><span data-stu-id="d39b0-192">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="d39b0-193">編碼器會快取輸入範例，直到每個頻道有足夠的1536音訊樣本為止;此時編碼器會輸出一個 AC 3 框架。</span><span class="sxs-lookup"><span data-stu-id="d39b0-193">The encoder caches input samples until it has enough for 1536 audio samples per channel; at which point the encoder outputs one AC-3 frame.</span></span>

<span data-ttu-id="d39b0-194">每個輸出緩衝區都包含一個原始的 AC 3 框架。</span><span class="sxs-lookup"><span data-stu-id="d39b0-194">Each output buffer contains one raw AC-3 frame.</span></span> <span data-ttu-id="d39b0-195">持續時間相當於 1536 PCM 樣本的持續時間，以目前的取樣率為 (32 毫秒) 以 48 kHz 取樣速率、34.83 毫秒（44.1 kHz）和 48 msec （32 kHz) ）。</span><span class="sxs-lookup"><span data-stu-id="d39b0-195">The duration is equivalent to the duration of 1536 PCM samples at the current sampling rate (32 msec) at 48 kHz sample rate, 34.83 msec at 44.1 kHz, and 48 msec at 32 kHz).</span></span> <span data-ttu-id="d39b0-196">每個輸出緩衝區的大小取決於位元速率和取樣率。</span><span class="sxs-lookup"><span data-stu-id="d39b0-196">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

<span data-ttu-id="d39b0-197">若要指定編碼位元速率，請在輸出類型中設定 [MF \_ MT \_ 音訊的 \_ \_ \_ 每 \_ 秒平均位元組數](mf-mt-audio-avg-bytes-per-second-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="d39b0-197">To specify the encoding bit rate, set the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output type.</span></span> <span data-ttu-id="d39b0-198">下表顯示編碼位元速率和 MF \_ MT \_ 音訊 \_ \_ \_ 每秒位元組數 \_ 之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="d39b0-198">The following table shows the relation between encoding bit rate and MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND.</span></span>



| <span data-ttu-id="d39b0-199">位元速率 (kbps) </span><span class="sxs-lookup"><span data-stu-id="d39b0-199">Bit rate (kbps)</span></span> | [<span data-ttu-id="d39b0-200">\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_</span><span class="sxs-lookup"><span data-stu-id="d39b0-200">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="d39b0-201">備註</span><span class="sxs-lookup"><span data-stu-id="d39b0-201">Remarks</span></span>                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d39b0-202">64</span><span class="sxs-lookup"><span data-stu-id="d39b0-202">64</span></span>              | <span data-ttu-id="d39b0-203">8000</span><span class="sxs-lookup"><span data-stu-id="d39b0-203">8000</span></span>                                                                                     | <span data-ttu-id="d39b0-204">僅限 Mono。</span><span class="sxs-lookup"><span data-stu-id="d39b0-204">Mono only.</span></span>                                              |
| <span data-ttu-id="d39b0-205">80</span><span class="sxs-lookup"><span data-stu-id="d39b0-205">80</span></span>              | <span data-ttu-id="d39b0-206">10000</span><span class="sxs-lookup"><span data-stu-id="d39b0-206">10000</span></span>                                                                                    | <span data-ttu-id="d39b0-207">僅限 Mono。</span><span class="sxs-lookup"><span data-stu-id="d39b0-207">Mono only.</span></span>                                              |
| <span data-ttu-id="d39b0-208">96</span><span class="sxs-lookup"><span data-stu-id="d39b0-208">96</span></span>              | <span data-ttu-id="d39b0-209">12000</span><span class="sxs-lookup"><span data-stu-id="d39b0-209">12000</span></span>                                                                                    | <span data-ttu-id="d39b0-210">僅限 Mono。</span><span class="sxs-lookup"><span data-stu-id="d39b0-210">Mono only.</span></span>                                              |
| <span data-ttu-id="d39b0-211">112</span><span class="sxs-lookup"><span data-stu-id="d39b0-211">112</span></span>             | <span data-ttu-id="d39b0-212">14000</span><span class="sxs-lookup"><span data-stu-id="d39b0-212">14000</span></span>                                                                                    | <span data-ttu-id="d39b0-213">僅限 Mono。</span><span class="sxs-lookup"><span data-stu-id="d39b0-213">Mono only.</span></span>                                              |
| <span data-ttu-id="d39b0-214">128</span><span class="sxs-lookup"><span data-stu-id="d39b0-214">128</span></span>             | <span data-ttu-id="d39b0-215">16000</span><span class="sxs-lookup"><span data-stu-id="d39b0-215">16000</span></span>                                                                                    | <span data-ttu-id="d39b0-216">Mono 或身歷聲。</span><span class="sxs-lookup"><span data-stu-id="d39b0-216">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="d39b0-217">160</span><span class="sxs-lookup"><span data-stu-id="d39b0-217">160</span></span>             | <span data-ttu-id="d39b0-218">20000</span><span class="sxs-lookup"><span data-stu-id="d39b0-218">20000</span></span>                                                                                    | <span data-ttu-id="d39b0-219">Mono 或身歷聲。</span><span class="sxs-lookup"><span data-stu-id="d39b0-219">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="d39b0-220">192</span><span class="sxs-lookup"><span data-stu-id="d39b0-220">192</span></span>             | <span data-ttu-id="d39b0-221">24000</span><span class="sxs-lookup"><span data-stu-id="d39b0-221">24000</span></span>                                                                                    | <span data-ttu-id="d39b0-222">Mono 或身歷聲。</span><span class="sxs-lookup"><span data-stu-id="d39b0-222">Mono or stereo.</span></span> <span data-ttu-id="d39b0-223">這是 mono 的預設設定。</span><span class="sxs-lookup"><span data-stu-id="d39b0-223">This is the default setting for mono.</span></span>   |
| <span data-ttu-id="d39b0-224">224</span><span class="sxs-lookup"><span data-stu-id="d39b0-224">224</span></span>             | <span data-ttu-id="d39b0-225">28000</span><span class="sxs-lookup"><span data-stu-id="d39b0-225">28000</span></span>                                                                                    | <span data-ttu-id="d39b0-226">Mono 或身歷聲。</span><span class="sxs-lookup"><span data-stu-id="d39b0-226">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="d39b0-227">256</span><span class="sxs-lookup"><span data-stu-id="d39b0-227">256</span></span>             | <span data-ttu-id="d39b0-228">32000</span><span class="sxs-lookup"><span data-stu-id="d39b0-228">32000</span></span>                                                                                    | <span data-ttu-id="d39b0-229">Mono 或身歷聲。</span><span class="sxs-lookup"><span data-stu-id="d39b0-229">Mono or stereo.</span></span> <span data-ttu-id="d39b0-230">這是身歷聲的預設設定。</span><span class="sxs-lookup"><span data-stu-id="d39b0-230">This is the default setting for stereo.</span></span> |
| <span data-ttu-id="d39b0-231">320</span><span class="sxs-lookup"><span data-stu-id="d39b0-231">320</span></span>             | <span data-ttu-id="d39b0-232">40000</span><span class="sxs-lookup"><span data-stu-id="d39b0-232">40000</span></span>                                                                                    | <span data-ttu-id="d39b0-233">僅限身歷聲。</span><span class="sxs-lookup"><span data-stu-id="d39b0-233">Stereo only.</span></span>                                            |
| <span data-ttu-id="d39b0-234">384</span><span class="sxs-lookup"><span data-stu-id="d39b0-234">384</span></span>             | <span data-ttu-id="d39b0-235">48000</span><span class="sxs-lookup"><span data-stu-id="d39b0-235">48000</span></span>                                                                                    | <span data-ttu-id="d39b0-236">僅限身歷聲。</span><span class="sxs-lookup"><span data-stu-id="d39b0-236">Stereo only.</span></span>                                            |
| <span data-ttu-id="d39b0-237">448</span><span class="sxs-lookup"><span data-stu-id="d39b0-237">448</span></span>             | <span data-ttu-id="d39b0-238">56000</span><span class="sxs-lookup"><span data-stu-id="d39b0-238">56000</span></span>                                                                                    | <span data-ttu-id="d39b0-239">僅限身歷聲。</span><span class="sxs-lookup"><span data-stu-id="d39b0-239">Stereo only.</span></span>                                            |



 

<span data-ttu-id="d39b0-240">預設的編碼位元速率會設定為 256 kbps （適用于身歷聲）和 192 kbps （mono）。</span><span class="sxs-lookup"><span data-stu-id="d39b0-240">The default encoding bit rate is set at 256 kbps for stereo and 192 kbps for mono.</span></span> <span data-ttu-id="d39b0-241">預設設定會反映在編碼器的 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 方法所傳回的媒體類型中。</span><span class="sxs-lookup"><span data-stu-id="d39b0-241">The default settings are reflected in the media types returned by the encoder's [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

### <a name="example-media-types"></a><span data-ttu-id="d39b0-242">範例媒體類型</span><span class="sxs-lookup"><span data-stu-id="d39b0-242">Example Media Types</span></span>

<span data-ttu-id="d39b0-243">以下是將16位整數 PCM 編碼的媒體類型範例，以 256 kbps 的預設位元速率為 48-kHz 身歷聲音訊。</span><span class="sxs-lookup"><span data-stu-id="d39b0-243">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate of 256 kbps.</span></span>

<span data-ttu-id="d39b0-244">輸出媒體類型：</span><span class="sxs-lookup"><span data-stu-id="d39b0-244">Output media type:</span></span>

| <span data-ttu-id="d39b0-245">屬性</span><span class="sxs-lookup"><span data-stu-id="d39b0-245">Attribute</span></span>                                                                           | <span data-ttu-id="d39b0-246">值</span><span class="sxs-lookup"><span data-stu-id="d39b0-246">Value</span></span>                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="d39b0-247">MF \_ MT \_ 主要 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="d39b0-247">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="d39b0-248">**MFMediaType \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="d39b0-248">**MFMediaType\_Audio**</span></span>        |
| [<span data-ttu-id="d39b0-249">MF \_ MT \_ 子類型</span><span class="sxs-lookup"><span data-stu-id="d39b0-249">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="d39b0-250">**MFAudioFormat \_ 杜 \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="d39b0-250">**MFAudioFormat\_Dolby\_AC3**</span></span> |
| [<span data-ttu-id="d39b0-251">\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_</span><span class="sxs-lookup"><span data-stu-id="d39b0-251">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="d39b0-252">48000</span><span class="sxs-lookup"><span data-stu-id="d39b0-252">48000</span></span>                         |
| [<span data-ttu-id="d39b0-253">MF \_ MT \_ 音訊 \_ 數目 \_ 通道</span><span class="sxs-lookup"><span data-stu-id="d39b0-253">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="d39b0-254">2</span><span class="sxs-lookup"><span data-stu-id="d39b0-254">2</span></span>                             |



 

<span data-ttu-id="d39b0-255">輸入媒體類型：</span><span class="sxs-lookup"><span data-stu-id="d39b0-255">Input media type:</span></span>

| <span data-ttu-id="d39b0-256">屬性</span><span class="sxs-lookup"><span data-stu-id="d39b0-256">Attribute</span></span>                                                                                | <span data-ttu-id="d39b0-257">值</span><span class="sxs-lookup"><span data-stu-id="d39b0-257">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="d39b0-258">MF \_ MT \_ 主要 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="d39b0-258">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="d39b0-259">**MFMediaType \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="d39b0-259">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="d39b0-260">MF \_ MT \_ 子類型</span><span class="sxs-lookup"><span data-stu-id="d39b0-260">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="d39b0-261">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="d39b0-261">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="d39b0-262">\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數</span><span class="sxs-lookup"><span data-stu-id="d39b0-262">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="d39b0-263">16</span><span class="sxs-lookup"><span data-stu-id="d39b0-263">16</span></span>                     |
| [<span data-ttu-id="d39b0-264">\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_</span><span class="sxs-lookup"><span data-stu-id="d39b0-264">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="d39b0-265">48000</span><span class="sxs-lookup"><span data-stu-id="d39b0-265">48000</span></span>                  |
| [<span data-ttu-id="d39b0-266">MF \_ MT \_ 音訊 \_ 數目 \_ 通道</span><span class="sxs-lookup"><span data-stu-id="d39b0-266">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="d39b0-267">2</span><span class="sxs-lookup"><span data-stu-id="d39b0-267">2</span></span>                      |
| [<span data-ttu-id="d39b0-268">MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊</span><span class="sxs-lookup"><span data-stu-id="d39b0-268">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="d39b0-269">4</span><span class="sxs-lookup"><span data-stu-id="d39b0-269">4</span></span>                      |
| [<span data-ttu-id="d39b0-270">\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_</span><span class="sxs-lookup"><span data-stu-id="d39b0-270">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="d39b0-271">192000</span><span class="sxs-lookup"><span data-stu-id="d39b0-271">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="d39b0-272">規格需求</span><span class="sxs-lookup"><span data-stu-id="d39b0-272">Requirements</span></span>



| <span data-ttu-id="d39b0-273">需求</span><span class="sxs-lookup"><span data-stu-id="d39b0-273">Requirement</span></span> | <span data-ttu-id="d39b0-274">值</span><span class="sxs-lookup"><span data-stu-id="d39b0-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d39b0-275">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d39b0-275">Minimum supported client</span></span><br/> | <span data-ttu-id="d39b0-276">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d39b0-276">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                       |
| <span data-ttu-id="d39b0-277">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d39b0-277">Minimum supported server</span></span><br/> | <span data-ttu-id="d39b0-278">都不支援</span><span class="sxs-lookup"><span data-stu-id="d39b0-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d39b0-279">DLL</span><span class="sxs-lookup"><span data-stu-id="d39b0-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d39b0-280"><dt>Msac3enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d39b0-280"><dt>Msac3enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d39b0-281">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d39b0-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d39b0-282">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="d39b0-282">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 




