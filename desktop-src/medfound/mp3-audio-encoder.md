---
description: Microsoft 媒體基礎。
ms.assetid: 4C397139-6553-4707-B737-7C31C5D423BA
title: MP3 音訊編碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea2b22d2fe8cd51f9a2990970493e0415f34d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026395"
---
# <a name="mp3-audio-encoder"></a><span data-ttu-id="3ddec-103">MP3 音訊編碼器</span><span class="sxs-lookup"><span data-stu-id="3ddec-103">MP3 Audio Encoder</span></span>

<span data-ttu-id="3ddec-104">Microsoft 媒體基礎 MP3 音訊編碼器是 [媒體基礎轉換](media-foundation-transforms.md) (MFT) ，可將 mpeg-2 的第3層 (MP3) 音訊編碼。</span><span class="sxs-lookup"><span data-stu-id="3ddec-104">The Microsoft Media Foundation MP3 audio encoder is a [Media Foundation Transform](media-foundation-transforms.md) (MFT) that encodes MPEG-1 layer 3 (MP3) audio.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="3ddec-105">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="3ddec-105">Class Identifier</span></span>

<span data-ttu-id="3ddec-106">MP3 編碼器 (CLSID) 的類別識別碼是 **clsid \_ MP3ACMCodecWrapper**，定義于標頭檔 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="3ddec-106">The class identifier (CLSID) of the MP3 encoder is **CLSID\_MP3ACMCodecWrapper**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="3ddec-107">媒體類型</span><span class="sxs-lookup"><span data-stu-id="3ddec-107">Media Types</span></span>

<span data-ttu-id="3ddec-108">MP3 編碼器支援下列媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3ddec-108">The MP3 encoder supports the following media types.</span></span> <span data-ttu-id="3ddec-109">輸出類型必須在輸入類型之前設定。</span><span class="sxs-lookup"><span data-stu-id="3ddec-109">The output type must be set before the input type.</span></span>

### <a name="output-types"></a><span data-ttu-id="3ddec-110">輸出型別</span><span class="sxs-lookup"><span data-stu-id="3ddec-110">Output Types</span></span>

<span data-ttu-id="3ddec-111">在輸出媒體類型上設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="3ddec-111">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ddec-112">屬性</span><span class="sxs-lookup"><span data-stu-id="3ddec-112">Attribute</span></span></th>
<th><span data-ttu-id="3ddec-113">描述</span><span class="sxs-lookup"><span data-stu-id="3ddec-113">Description</span></span></th>
<th><span data-ttu-id="3ddec-114">備註</span><span class="sxs-lookup"><span data-stu-id="3ddec-114">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ddec-115"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ddec-115"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="3ddec-116">主要類型。</span><span class="sxs-lookup"><span data-stu-id="3ddec-116">Major type.</span></span></td>
<td><span data-ttu-id="3ddec-117">必須是 <strong>MFMediaType_Audio</strong>。</span><span class="sxs-lookup"><span data-stu-id="3ddec-117">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ddec-118"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ddec-118"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="3ddec-119">音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="3ddec-119">Audio subtype.</span></span></td>
<td><span data-ttu-id="3ddec-120">必須是 <strong>MFAudioFormat_MP3</strong>。</span><span class="sxs-lookup"><span data-stu-id="3ddec-120">Must be <strong>MFAudioFormat_MP3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ddec-121"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ddec-121"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="3ddec-122">編碼的 MP3 資料流程的位元速率（以每秒位元組數為單位）。</span><span class="sxs-lookup"><span data-stu-id="3ddec-122">Bit rate of the encoded MP3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="3ddec-123">編碼器支援標準 (32、40、48、56、64、80、96、112、128、160、192、224、256或 320 Kbps) 所定義的所有位元速率。</span><span class="sxs-lookup"><span data-stu-id="3ddec-123">The encoder supports all bit rates defined by the standard (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, or 320 Kbps).</span></span><br/> <span data-ttu-id="3ddec-124">適用于 mono 的預設位元速率為 128 Kbps，身歷聲為 320 Kbps。</span><span class="sxs-lookup"><span data-stu-id="3ddec-124">The default bit rates are 128 Kbps for mono and 320 Kbps for stereo.</span></span><br/> <span data-ttu-id="3ddec-125">您可以使用這個屬性來指定編碼的位元速率。</span><span class="sxs-lookup"><span data-stu-id="3ddec-125">Use this attribute to specify the encoded bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ddec-126"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ddec-126"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="3ddec-127">通道數目。</span><span class="sxs-lookup"><span data-stu-id="3ddec-127">Number of channels.</span></span></td>
<td><span data-ttu-id="3ddec-128">支援下列值：</span><span class="sxs-lookup"><span data-stu-id="3ddec-128">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="3ddec-129">1 (mono)</span><span class="sxs-lookup"><span data-stu-id="3ddec-129">1 (mono)</span></span></li>
<li><span data-ttu-id="3ddec-130">2 (身歷聲) </span><span class="sxs-lookup"><span data-stu-id="3ddec-130">2 (stereo)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ddec-131"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ddec-131"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="3ddec-132">每秒樣本數。</span><span class="sxs-lookup"><span data-stu-id="3ddec-132">Samples per second.</span></span></td>
<td><span data-ttu-id="3ddec-133">支援下列值：</span><span class="sxs-lookup"><span data-stu-id="3ddec-133">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="3ddec-134">48000 (48 KHz) </span><span class="sxs-lookup"><span data-stu-id="3ddec-134">48000 (48 KHz)</span></span></li>
<li><span data-ttu-id="3ddec-135">44100 (44.1 KHz) </span><span class="sxs-lookup"><span data-stu-id="3ddec-135">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="3ddec-136">32000 (32 KHz) </span><span class="sxs-lookup"><span data-stu-id="3ddec-136">32000 (32 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ddec-137"><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></span><span class="sxs-lookup"><span data-stu-id="3ddec-137"><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></span></span></td>
<td><span data-ttu-id="3ddec-138">其他編解碼器資料。</span><span class="sxs-lookup"><span data-stu-id="3ddec-138">Additional codec data.</span></span></td>
<td><span data-ttu-id="3ddec-139">這個屬性包含 <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> 結構的12個位元組，該結構會遵循該結構的 <strong>wfx</strong> 成員。</span><span class="sxs-lookup"><span data-stu-id="3ddec-139">This attribute contains the 12 bytes of the <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> structure that follow the <strong>wfx</strong> member of that structure.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3ddec-140">或者，您可以填入 [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) 結構，然後呼叫 [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) 將結構轉換成媒體基礎的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3ddec-140">Alternatively, you can fill in an [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure and call [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) to convert the structure to a Media Foundation media type.</span></span>

### <a name="input-types"></a><span data-ttu-id="3ddec-141">輸入類型</span><span class="sxs-lookup"><span data-stu-id="3ddec-141">Input Types</span></span>

<span data-ttu-id="3ddec-142">在輸入媒體類型上設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="3ddec-142">Set the following attributes on the input media type.</span></span>



| <span data-ttu-id="3ddec-143">屬性</span><span class="sxs-lookup"><span data-stu-id="3ddec-143">Attribute</span></span>                                                                               | <span data-ttu-id="3ddec-144">描述</span><span class="sxs-lookup"><span data-stu-id="3ddec-144">Description</span></span>         | <span data-ttu-id="3ddec-145">備註</span><span class="sxs-lookup"><span data-stu-id="3ddec-145">Remarks</span></span>                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [<span data-ttu-id="3ddec-146">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="3ddec-146">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="3ddec-147">主要類型。</span><span class="sxs-lookup"><span data-stu-id="3ddec-147">Major type.</span></span>         | <span data-ttu-id="3ddec-148">必須是 **MFMediaType \_ 音訊**。</span><span class="sxs-lookup"><span data-stu-id="3ddec-148">Must be **MFMediaType\_Audio**.</span></span> |
| [<span data-ttu-id="3ddec-149">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="3ddec-149">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="3ddec-150">亞。</span><span class="sxs-lookup"><span data-stu-id="3ddec-150">Subtype.</span></span>            | <span data-ttu-id="3ddec-151">必須是 **MFAudioFormat \_ PCM**。</span><span class="sxs-lookup"><span data-stu-id="3ddec-151">Must be **MFAudioFormat\_PCM**.</span></span> |
| [<span data-ttu-id="3ddec-152">**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**</span><span class="sxs-lookup"><span data-stu-id="3ddec-152">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="3ddec-153">每個樣本的位數。</span><span class="sxs-lookup"><span data-stu-id="3ddec-153">Bits per sample.</span></span>    | <span data-ttu-id="3ddec-154">必須是16。</span><span class="sxs-lookup"><span data-stu-id="3ddec-154">Must be 16.</span></span>                     |
| [<span data-ttu-id="3ddec-155">**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3ddec-155">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="3ddec-156">每秒樣本數。</span><span class="sxs-lookup"><span data-stu-id="3ddec-156">Samples per second.</span></span> | <span data-ttu-id="3ddec-157">必須符合輸出類型。</span><span class="sxs-lookup"><span data-stu-id="3ddec-157">Must match the output type.</span></span>     |
| [<span data-ttu-id="3ddec-158">**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**</span><span class="sxs-lookup"><span data-stu-id="3ddec-158">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="3ddec-159">通道數目。</span><span class="sxs-lookup"><span data-stu-id="3ddec-159">Number of channels.</span></span> | <span data-ttu-id="3ddec-160">必須符合輸出類型。</span><span class="sxs-lookup"><span data-stu-id="3ddec-160">Must match the output type.</span></span>     |



 

<span data-ttu-id="3ddec-161">編碼器僅支援16位的整數 PCM 輸入。</span><span class="sxs-lookup"><span data-stu-id="3ddec-161">The encoder supports only 16-bit integer PCM input.</span></span> <span data-ttu-id="3ddec-162">它不支援32位浮點數輸入。</span><span class="sxs-lookup"><span data-stu-id="3ddec-162">It does not support 32-bit floating point input.</span></span>

### <a name="media-formats"></a><span data-ttu-id="3ddec-163">媒體格式</span><span class="sxs-lookup"><span data-stu-id="3ddec-163">Media Formats</span></span>

<span data-ttu-id="3ddec-164">MPEG 1 和 MPEG-2 標準定義252第3層音訊格式。</span><span class="sxs-lookup"><span data-stu-id="3ddec-164">The MPEG-1 and MPEG-2 standard defines 252 layer 3 audio formats.</span></span> <span data-ttu-id="3ddec-165">MP3 編碼器支援具有一些例外狀況的標準，以及一些其他格式，如下所述。</span><span class="sxs-lookup"><span data-stu-id="3ddec-165">The MP3 encoder supports the standard with some exceptions, as well as some additional formats, as described below.</span></span> <span data-ttu-id="3ddec-166">第3層定義如下：</span><span class="sxs-lookup"><span data-stu-id="3ddec-166">Layer 3 is defined as:</span></span>



| <span data-ttu-id="3ddec-167">需求</span><span class="sxs-lookup"><span data-stu-id="3ddec-167">Requirement</span></span> | <span data-ttu-id="3ddec-168">值</span><span class="sxs-lookup"><span data-stu-id="3ddec-168">Value</span></span> |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3ddec-169">通道</span><span class="sxs-lookup"><span data-stu-id="3ddec-169">Channels</span></span>                         | <span data-ttu-id="3ddec-170">mono 或身歷聲</span><span class="sxs-lookup"><span data-stu-id="3ddec-170">mono or stereo</span></span>                                                |
| <span data-ttu-id="3ddec-171">以 kHz 為例的 MPEG-2 取樣率</span><span class="sxs-lookup"><span data-stu-id="3ddec-171">MPEG-1 sample rates in kHz</span></span>       | <span data-ttu-id="3ddec-172">44.1、48、32</span><span class="sxs-lookup"><span data-stu-id="3ddec-172">44.1, 48, 32</span></span>                                                  |
| <span data-ttu-id="3ddec-173">MPEG-2 編碼的位元速率（kbps）</span><span class="sxs-lookup"><span data-stu-id="3ddec-173">MPEG-1 encoded bit rates in kbps</span></span> | <span data-ttu-id="3ddec-174">32、40、48、56、64、80、96、112、128、160、192、224、256、320</span><span class="sxs-lookup"><span data-stu-id="3ddec-174">32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320</span></span> |
| <span data-ttu-id="3ddec-175">MPEG-2 範例速率（kHz）</span><span class="sxs-lookup"><span data-stu-id="3ddec-175">MPEG-2 sample rates in kHz</span></span>       | <span data-ttu-id="3ddec-176">8、11.025、12、16、22.05、24</span><span class="sxs-lookup"><span data-stu-id="3ddec-176">8, 11.025, 12, 16, 22.05, 24</span></span>                                  |
| <span data-ttu-id="3ddec-177">MPEG-2 編碼的位元速率（kbps）</span><span class="sxs-lookup"><span data-stu-id="3ddec-177">MPEG-2 encoded bit rates in kbps</span></span> | <span data-ttu-id="3ddec-178">8、16、24、32、40、48、56、64、80、96、112、144、160</span><span class="sxs-lookup"><span data-stu-id="3ddec-178">8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160</span></span>          |



 

<span data-ttu-id="3ddec-179">MP3 編碼器也支援下列格式。</span><span class="sxs-lookup"><span data-stu-id="3ddec-179">The MP3 encoder also supports the following formats.</span></span>



| <span data-ttu-id="3ddec-180">採樣速率</span><span class="sxs-lookup"><span data-stu-id="3ddec-180">Sample Rate</span></span> | <span data-ttu-id="3ddec-181">位元速度</span><span class="sxs-lookup"><span data-stu-id="3ddec-181">Bit Rate</span></span>     | <span data-ttu-id="3ddec-182">頻道號碼</span><span class="sxs-lookup"><span data-stu-id="3ddec-182">Channel Number</span></span> |
|-------------|--------------|----------------|
| <span data-ttu-id="3ddec-183">8000</span><span class="sxs-lookup"><span data-stu-id="3ddec-183">8000</span></span>        | <span data-ttu-id="3ddec-184">18000、20000</span><span class="sxs-lookup"><span data-stu-id="3ddec-184">18000, 20000</span></span> | <span data-ttu-id="3ddec-185">2</span><span class="sxs-lookup"><span data-stu-id="3ddec-185">2</span></span>              |
| <span data-ttu-id="3ddec-186">11025</span><span class="sxs-lookup"><span data-stu-id="3ddec-186">11025</span></span>       | <span data-ttu-id="3ddec-187">18000、20000</span><span class="sxs-lookup"><span data-stu-id="3ddec-187">18000, 20000</span></span> | <span data-ttu-id="3ddec-188">1 或 2</span><span class="sxs-lookup"><span data-stu-id="3ddec-188">1 or 2</span></span>         |
| <span data-ttu-id="3ddec-189">12000</span><span class="sxs-lookup"><span data-stu-id="3ddec-189">12000</span></span>       | <span data-ttu-id="3ddec-190">18000、20000</span><span class="sxs-lookup"><span data-stu-id="3ddec-190">18000, 20000</span></span> | <span data-ttu-id="3ddec-191">1 或 2</span><span class="sxs-lookup"><span data-stu-id="3ddec-191">1 or 2</span></span>         |
| <span data-ttu-id="3ddec-192">16000</span><span class="sxs-lookup"><span data-stu-id="3ddec-192">16000</span></span>       | <span data-ttu-id="3ddec-193">18000、20000</span><span class="sxs-lookup"><span data-stu-id="3ddec-193">18000, 20000</span></span> | <span data-ttu-id="3ddec-194">1</span><span class="sxs-lookup"><span data-stu-id="3ddec-194">1</span></span>              |
| <span data-ttu-id="3ddec-195">32000</span><span class="sxs-lookup"><span data-stu-id="3ddec-195">32000</span></span>       | <span data-ttu-id="3ddec-196">144000</span><span class="sxs-lookup"><span data-stu-id="3ddec-196">144000</span></span>       | <span data-ttu-id="3ddec-197">1 或 2</span><span class="sxs-lookup"><span data-stu-id="3ddec-197">1 or 2</span></span>         |
| <span data-ttu-id="3ddec-198">44100</span><span class="sxs-lookup"><span data-stu-id="3ddec-198">44100</span></span>       | <span data-ttu-id="3ddec-199">144000</span><span class="sxs-lookup"><span data-stu-id="3ddec-199">144000</span></span>       | <span data-ttu-id="3ddec-200">1 或 2</span><span class="sxs-lookup"><span data-stu-id="3ddec-200">1 or 2</span></span>         |
| <span data-ttu-id="3ddec-201">48000</span><span class="sxs-lookup"><span data-stu-id="3ddec-201">48000</span></span>       | <span data-ttu-id="3ddec-202">144000</span><span class="sxs-lookup"><span data-stu-id="3ddec-202">144000</span></span>       | <span data-ttu-id="3ddec-203">1 或 2</span><span class="sxs-lookup"><span data-stu-id="3ddec-203">1 or 2</span></span>         |



 

<span data-ttu-id="3ddec-204">MP3 編碼器不支援標準所定義的下列格式。</span><span class="sxs-lookup"><span data-stu-id="3ddec-204">The MP3 encoder does not support the following formats defined by the standard.</span></span>



| <span data-ttu-id="3ddec-205">採樣速率</span><span class="sxs-lookup"><span data-stu-id="3ddec-205">Sample Rate</span></span> | <span data-ttu-id="3ddec-206">位元速率</span><span class="sxs-lookup"><span data-stu-id="3ddec-206">Bit Rates</span></span>                                    | <span data-ttu-id="3ddec-207">頻道號碼</span><span class="sxs-lookup"><span data-stu-id="3ddec-207">Channel Number</span></span> |
|-------------|----------------------------------------------|----------------|
| <span data-ttu-id="3ddec-208">12000</span><span class="sxs-lookup"><span data-stu-id="3ddec-208">12000</span></span>       | <span data-ttu-id="3ddec-209">80000、96000、112000、128000、144000、160000</span><span class="sxs-lookup"><span data-stu-id="3ddec-209">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="3ddec-210">1 或 2</span><span class="sxs-lookup"><span data-stu-id="3ddec-210">1 or 2</span></span>         |
| <span data-ttu-id="3ddec-211">11025</span><span class="sxs-lookup"><span data-stu-id="3ddec-211">11025</span></span>       | <span data-ttu-id="3ddec-212">80000、96000、112000、128000、144000、160000</span><span class="sxs-lookup"><span data-stu-id="3ddec-212">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="3ddec-213">1 或 2</span><span class="sxs-lookup"><span data-stu-id="3ddec-213">1 or 2</span></span>         |
| <span data-ttu-id="3ddec-214">8000</span><span class="sxs-lookup"><span data-stu-id="3ddec-214">8000</span></span>        | <span data-ttu-id="3ddec-215">80000、96000、112000、128000、144000、160000</span><span class="sxs-lookup"><span data-stu-id="3ddec-215">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="3ddec-216">1 或 2</span><span class="sxs-lookup"><span data-stu-id="3ddec-216">1 or 2</span></span>         |
| <span data-ttu-id="3ddec-217">8000</span><span class="sxs-lookup"><span data-stu-id="3ddec-217">8000</span></span>        | <span data-ttu-id="3ddec-218">8000、11025、12000、16000、22050、24000</span><span class="sxs-lookup"><span data-stu-id="3ddec-218">8000, 11025, 12000, 16000, 22050, 24000</span></span>      | <span data-ttu-id="3ddec-219">2</span><span class="sxs-lookup"><span data-stu-id="3ddec-219">2</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="3ddec-220">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ddec-220">Requirements</span></span>



| <span data-ttu-id="3ddec-221">需求</span><span class="sxs-lookup"><span data-stu-id="3ddec-221">Requirement</span></span> | <span data-ttu-id="3ddec-222">值</span><span class="sxs-lookup"><span data-stu-id="3ddec-222">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ddec-223">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ddec-223">Minimum supported client</span></span><br/> | <span data-ttu-id="3ddec-224">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ddec-224">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="3ddec-225">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ddec-225">Minimum supported server</span></span><br/> | <span data-ttu-id="3ddec-226">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ddec-226">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ddec-227">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ddec-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ddec-228">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="3ddec-228">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
