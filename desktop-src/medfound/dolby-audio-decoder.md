---
description: 杜比音訊解碼器是一種會將杜比數位 (AC-3) 和杜比數位加號解碼的 MFT。
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: 杜比音訊解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f1d8ca21cb3ab86f1fdbeddf03624aaaffb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689308"
---
# <a name="dolby-audio-decoder"></a><span data-ttu-id="a0dd5-103">杜比音訊解碼器</span><span class="sxs-lookup"><span data-stu-id="a0dd5-103">Dolby Audio Decoder</span></span>

<span data-ttu-id="a0dd5-104">杜比音訊解碼器是 [媒體基礎轉換](media-foundation-transforms.md) (MFT) ，可將下列串流類型解碼：</span><span class="sxs-lookup"><span data-stu-id="a0dd5-104">The Dolby audio decoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that decodes the following stream types:</span></span>

-   <span data-ttu-id="a0dd5-105">杜比數位，也稱為杜比 AC-3</span><span class="sxs-lookup"><span data-stu-id="a0dd5-105">Dolby Digital, also called Dolby AC-3</span></span>
-   <span data-ttu-id="a0dd5-106">杜比數位 Plus，也稱為增強的 AC-3 (E-AC-3) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-106">Dolby Digital Plus, also called Enhanced AC-3 (E-AC-3)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0dd5-107">在 Windows 8 之前的 Windows 版本中，Microsoft 應用程式所使用的杜比數位授權方案會限制 Microsoft 的杜比數位技術。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-107">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="a0dd5-108">如需這些格式的詳細資訊，請參閱 Advanced 電視 Systems 委員會 (ATSC) 檔 *數位音訊壓縮標準 (AC-3、E-AC-3) 修訂 B*。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-108">For more information about these formats, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

<span data-ttu-id="a0dd5-109">此解碼器也可以將杜比數位加號串流轉換為 AC-3 S/PIDF 輸出的杜數位格式，或為 HDMI 數位輸出格式化杜比數位的資料流程。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-109">The decoder can also convert a Dolby Digital Plus stream to Dolby Digital format for AC-3 S/PIDF output, or format a Dolby Digital Plus stream for HDMI digital output.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="a0dd5-110">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="a0dd5-110">Class Identifier</span></span>

<span data-ttu-id="a0dd5-111">[杜比音訊解碼器] (CLSID) 的類別識別碼是 **clsid \_ CMSDDPlusDecMFT**，定義于標頭檔 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-111">The class identifier (CLSID) of the Dolby audio decoder is **CLSID\_CMSDDPlusDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="a0dd5-112">輸入類型</span><span class="sxs-lookup"><span data-stu-id="a0dd5-112">Input Types</span></span>

<span data-ttu-id="a0dd5-113">杜比音訊解碼器支援下列輸入子類型。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-113">The Dolby audio decoder supports the following input subtypes.</span></span>



| <span data-ttu-id="a0dd5-114">Subtype</span><span class="sxs-lookup"><span data-stu-id="a0dd5-114">Subtype</span></span>                                 | <span data-ttu-id="a0dd5-115">描述</span><span class="sxs-lookup"><span data-stu-id="a0dd5-115">Description</span></span>                                                                                                                                                 | <span data-ttu-id="a0dd5-116">標頭</span><span class="sxs-lookup"><span data-stu-id="a0dd5-116">Header</span></span>       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="a0dd5-117">**MEDIASUBTYPE \_ 杜 \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="a0dd5-117">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>            | <span data-ttu-id="a0dd5-118">杜比數位音訊。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-118">Dolby Digital audio.</span></span>                                                                                                                                        | <span data-ttu-id="a0dd5-119">mfapi。h</span><span class="sxs-lookup"><span data-stu-id="a0dd5-119">mfapi.h</span></span>      |
| <span data-ttu-id="a0dd5-120">**MEDIASUBTYPE \_ DVM**</span><span class="sxs-lookup"><span data-stu-id="a0dd5-120">**MEDIASUBTYPE\_DVM**</span></span>                   | <span data-ttu-id="a0dd5-121">杜比數位音訊;請參閱 [**音訊子類型**](../directshow/audio-subtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-121">Dolby Digital audio; see [**Audio Subtypes**](../directshow/audio-subtypes.md).</span></span> <span data-ttu-id="a0dd5-122">此子類型可與 **MEDIASUBTYPE \_ 杜比 \_ AC3** 互換使用。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-122">This subtype can be used interchangeably with **MEDIASUBTYPE\_DOLBY\_AC3**.</span></span><br/> | <span data-ttu-id="a0dd5-123">wmcodecdsp。h</span><span class="sxs-lookup"><span data-stu-id="a0dd5-123">wmcodecdsp.h</span></span> |
| <span data-ttu-id="a0dd5-124">**MFAudioFormat \_ 杜比 \_ 數位 \_ 加號**</span><span class="sxs-lookup"><span data-stu-id="a0dd5-124">**MFAudioFormat\_Dolby\_Digital\_Plus**</span></span> | <span data-ttu-id="a0dd5-125">杜比數位加號音訊。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-125">Dolby Digital Plus audio.</span></span>                                                                                                                                   | <span data-ttu-id="a0dd5-126">mfapi。h</span><span class="sxs-lookup"><span data-stu-id="a0dd5-126">mfapi.h</span></span>      |



 

<span data-ttu-id="a0dd5-127">下表列出輸入媒體類型的需要和選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-127">The following table lists the requires and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0dd5-128">屬性</span><span class="sxs-lookup"><span data-stu-id="a0dd5-128">Attribute</span></span></th>
<th><span data-ttu-id="a0dd5-129">描述</span><span class="sxs-lookup"><span data-stu-id="a0dd5-129">Description</span></span></th>
<th><span data-ttu-id="a0dd5-130">備註</span><span class="sxs-lookup"><span data-stu-id="a0dd5-130">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0dd5-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="a0dd5-132">主要類型。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-132">Major type.</span></span></td>
<td><span data-ttu-id="a0dd5-133">必要。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-133">Required.</span></span> <span data-ttu-id="a0dd5-134">必須是 <strong>MFMediaType_Audio</strong>。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-134">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dd5-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="a0dd5-136">音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-136">Audio subtype.</span></span></td>
<td><span data-ttu-id="a0dd5-137">必要。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-137">Required.</span></span> <span data-ttu-id="a0dd5-138">請參閱上表以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-138">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dd5-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="a0dd5-140">取樣率（以每秒樣本數為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-140">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="a0dd5-141">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-141">Optional.</span></span> <span data-ttu-id="a0dd5-142">有效的值為：48000、44100、32000、24000、22050和16000。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-142">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="a0dd5-143">如果未設定此屬性，則預設值為48000。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-143">If this attribute is not set, the default value is 48000.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dd5-144">這份清單中的三個最高比率僅限最高的 AC-3 個串流。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-144">Dolby AC-3 streams are limited to the three highest rates in this list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dd5-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="a0dd5-146">通道的數目，包括低頻率 (LFE) 通道（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-146">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="a0dd5-147">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-147">Optional.</span></span> <span data-ttu-id="a0dd5-148">有效值的範圍為 1 (mono) 為 8 (7.1 channel configuration) 。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-148">Valid values are in the range 1 (mono) to 8 (7.1 channel configuration).</span></span> <span data-ttu-id="a0dd5-149">如果未設定此屬性，預設值為 2 (身歷聲) 。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-149">If this attribute is not set, the default value is 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dd5-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="a0dd5-151">指定喇叭位置的音訊通道指派。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-151">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="a0dd5-152">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-152">Optional.</span></span> <span data-ttu-id="a0dd5-153">如果有指定，此值必須與音訊通道的數目一致。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-153">If specified, the value must be consistent with the number of audio channels.</span></span> <span data-ttu-id="a0dd5-154">如果未設定屬性，則會使用預設通道遮罩（以通道數目為基礎）。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-154">If the attribute is not set, the decoder uses a default channel mask, based on the number of channels.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a0dd5-155">下表列出支援的杜比通道設定。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-155">The following table lists the supported Dolby channel configurations.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0dd5-156">通道設定</span><span class="sxs-lookup"><span data-stu-id="a0dd5-156">Channel configuration</span></span></th>
<th><span data-ttu-id="a0dd5-157">通道數目</span><span class="sxs-lookup"><span data-stu-id="a0dd5-157">Number of channels</span></span></th>
<th><span data-ttu-id="a0dd5-158">通道遮罩</span><span class="sxs-lookup"><span data-stu-id="a0dd5-158">Channel masks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0dd5-159">1/0 (mono) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-159">1/0 (mono)</span></span></td>
<td><span data-ttu-id="a0dd5-160">1</span><span class="sxs-lookup"><span data-stu-id="a0dd5-160">1</span></span></td>
<td><span data-ttu-id="a0dd5-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dd5-162">2/0 (身歷聲) 或 1 + 1 (雙 mono) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-162">2/0 (stereo) or 1+1 (dual mono)</span></span></td>
<td><span data-ttu-id="a0dd5-163">2</span><span class="sxs-lookup"><span data-stu-id="a0dd5-163">2</span></span></td>
<td><span data-ttu-id="a0dd5-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dd5-165">3/0</span><span class="sxs-lookup"><span data-stu-id="a0dd5-165">3/0</span></span></td>
<td><span data-ttu-id="a0dd5-166">3</span><span class="sxs-lookup"><span data-stu-id="a0dd5-166">3</span></span></td>
<td><span data-ttu-id="a0dd5-167">0x7 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong> |SPEAKER_FRONT_CENTER) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-167">0x7 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dd5-168">2/1</span><span class="sxs-lookup"><span data-stu-id="a0dd5-168">2/1</span></span></td>
<td><span data-ttu-id="a0dd5-169">3</span><span class="sxs-lookup"><span data-stu-id="a0dd5-169">3</span></span></td>
<td><span data-ttu-id="a0dd5-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dd5-171">3/1</span><span class="sxs-lookup"><span data-stu-id="a0dd5-171">3/1</span></span></td>
<td><span data-ttu-id="a0dd5-172">4</span><span class="sxs-lookup"><span data-stu-id="a0dd5-172">4</span></span></td>
<td><span data-ttu-id="a0dd5-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dd5-174">2/2</span><span class="sxs-lookup"><span data-stu-id="a0dd5-174">2/2</span></span></td>
<td><span data-ttu-id="a0dd5-175">4</span><span class="sxs-lookup"><span data-stu-id="a0dd5-175">4</span></span></td>
<td><span data-ttu-id="a0dd5-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="a0dd5-177">或</span><span class="sxs-lookup"><span data-stu-id="a0dd5-177">or</span></span><br/> <span data-ttu-id="a0dd5-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dd5-179">3/2</span><span class="sxs-lookup"><span data-stu-id="a0dd5-179">3/2</span></span></td>
<td><span data-ttu-id="a0dd5-180">5</span><span class="sxs-lookup"><span data-stu-id="a0dd5-180">5</span></span></td>
<td><span data-ttu-id="a0dd5-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong></strong> SPEAKER_BACK_RIGHT) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="a0dd5-182">或</span><span class="sxs-lookup"><span data-stu-id="a0dd5-182">or</span></span><br/> <span data-ttu-id="a0dd5-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong></strong> SPEAKER_SIDE_RIGHT) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dd5-184">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="a0dd5-184">3/2 + LFE</span></span></td>
<td><span data-ttu-id="a0dd5-185">6</span><span class="sxs-lookup"><span data-stu-id="a0dd5-185">6</span></span></td>
<td><span data-ttu-id="a0dd5-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong></strong>  |  <strong></strong> SPEAKER_BACK_LEFT SPEAKER_BACK_RIGHT) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="a0dd5-187">或</span><span class="sxs-lookup"><span data-stu-id="a0dd5-187">or</span></span><br/> <span data-ttu-id="a0dd5-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong></strong>  |  <strong></strong> SPEAKER_SIDE_LEFT SPEAKER_SIDE_RIGHT) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dd5-189">3/2/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="a0dd5-189">3/2/2 + LFE</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="a0dd5-190">僅限杜比數位加號。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-190">Dolby Digital Plus only.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="a0dd5-191">8</span><span class="sxs-lookup"><span data-stu-id="a0dd5-191">8</span></span></td>
<td><span data-ttu-id="a0dd5-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong> |SPEAKER_SIDE_LEFT |SPEAKER_SIDE_RIGHT) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a0dd5-193">此外，通道設定1/0、2/0、3/0、2/1、3/1 和2/2 也可能出現 LFE 通道。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-193">In addition, channel configurations 1/0, 2/0, 3/0, 2/1, 3/1, and 2/2 may also appear with an LFE channel.</span></span>

## <a name="output-types"></a><span data-ttu-id="a0dd5-194">輸出型別</span><span class="sxs-lookup"><span data-stu-id="a0dd5-194">Output Types</span></span>

<span data-ttu-id="a0dd5-195">杜比音訊解碼器支援下列輸出子類型。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-195">The Dolby audio decoder supports the following output subtypes.</span></span>



| <span data-ttu-id="a0dd5-196">Subtype</span><span class="sxs-lookup"><span data-stu-id="a0dd5-196">Subtype</span></span>                                                   | <span data-ttu-id="a0dd5-197">描述</span><span class="sxs-lookup"><span data-stu-id="a0dd5-197">Description</span></span>                                                                                                                               | <span data-ttu-id="a0dd5-198">標頭</span><span class="sxs-lookup"><span data-stu-id="a0dd5-198">Header</span></span>    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="a0dd5-199">**MFAudioFormat \_ 杜 \_ AC3 \_ SPDIF**</span><span class="sxs-lookup"><span data-stu-id="a0dd5-199">**MFAudioFormat\_Dolby\_AC3\_SPDIF**</span></span>                      | <span data-ttu-id="a0dd5-200">針對 S/PDIF 數位輸出格式化的 AC-3 音訊。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-200">Dolby AC-3 audio formatted for S/PDIF digital output.</span></span>                                                                                     | <span data-ttu-id="a0dd5-201">mfapi。h</span><span class="sxs-lookup"><span data-stu-id="a0dd5-201">mfapi.h</span></span>   |
| <span data-ttu-id="a0dd5-202">**KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ 數位 \_ 加號**</span><span class="sxs-lookup"><span data-stu-id="a0dd5-202">**KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**</span></span> | <span data-ttu-id="a0dd5-203">針對 HDMI 數位輸出格式化的杜數位加音訊。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-203">Dolby Digital Plus audio formatted for HDMI digital output.</span></span>                                                                               | <span data-ttu-id="a0dd5-204">ksmedia。h</span><span class="sxs-lookup"><span data-stu-id="a0dd5-204">ksmedia.h</span></span> |
| <span data-ttu-id="a0dd5-205">**MFAudioFormat \_ 浮點數**</span><span class="sxs-lookup"><span data-stu-id="a0dd5-205">**MFAudioFormat\_Float**</span></span>                                  | <span data-ttu-id="a0dd5-206">IEEE 32 位浮點 PCM 音訊</span><span class="sxs-lookup"><span data-stu-id="a0dd5-206">IEEE 32-bit floating-point PCM audio</span></span><br/> <span data-ttu-id="a0dd5-207">**Windows 10**：身歷聲、5.1、7。1</span><span class="sxs-lookup"><span data-stu-id="a0dd5-207">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="a0dd5-208">**先前的版本**：身歷聲、5。1</span><span class="sxs-lookup"><span data-stu-id="a0dd5-208">**Previous versions**: stereo, 5.1</span></span><br/> | <span data-ttu-id="a0dd5-209">mfapi。h</span><span class="sxs-lookup"><span data-stu-id="a0dd5-209">mfapi.h</span></span>   |
| <span data-ttu-id="a0dd5-210">**MFAudioFormat \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="a0dd5-210">**MFAudioFormat\_PCM**</span></span>                                    | <span data-ttu-id="a0dd5-211">16位 PCM 音訊</span><span class="sxs-lookup"><span data-stu-id="a0dd5-211">16-bit PCM audio</span></span><br/> <span data-ttu-id="a0dd5-212">**Windows 10**：身歷聲、5.1、7。1</span><span class="sxs-lookup"><span data-stu-id="a0dd5-212">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="a0dd5-213">**先前的版本**：身歷聲、5。1</span><span class="sxs-lookup"><span data-stu-id="a0dd5-213">**Previous versions**: stereo, 5.1</span></span><br/>                     | <span data-ttu-id="a0dd5-214">mfapi。h</span><span class="sxs-lookup"><span data-stu-id="a0dd5-214">mfapi.h</span></span>   |



 

<span data-ttu-id="a0dd5-215">下表列出輸出媒體類型的必要和選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-215">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0dd5-216">屬性</span><span class="sxs-lookup"><span data-stu-id="a0dd5-216">Attribute</span></span></th>
<th><span data-ttu-id="a0dd5-217">描述</span><span class="sxs-lookup"><span data-stu-id="a0dd5-217">Description</span></span></th>
<th><span data-ttu-id="a0dd5-218">備註</span><span class="sxs-lookup"><span data-stu-id="a0dd5-218">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0dd5-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="a0dd5-220">主要類型。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-220">Major type.</span></span></td>
<td><span data-ttu-id="a0dd5-221">必要。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-221">Required.</span></span> <span data-ttu-id="a0dd5-222">必須是 <strong>MFMediaType_Audio</strong>。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-222">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dd5-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="a0dd5-224">音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-224">Audio subtype.</span></span></td>
<td><span data-ttu-id="a0dd5-225">必要。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-225">Required.</span></span> <span data-ttu-id="a0dd5-226">請參閱上表以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-226">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dd5-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="a0dd5-228">取樣率（以每秒樣本數為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-228">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="a0dd5-229">必要。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-229">Required.</span></span> <span data-ttu-id="a0dd5-230">有效的值為：48000、44100、32000、24000、22050和16000。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-230">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="a0dd5-231">輸出取樣率必須與輸入取樣率相同。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-231">The output sample rate must be identical to the input sample rate.</span></span> <span data-ttu-id="a0dd5-232">此解碼器無法變更資料流程的取樣率。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-232">The decoder cannot change the sampling rate of the stream.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dd5-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="a0dd5-234">通道的數目，包括低頻率 (LFE) 通道（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-234">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="a0dd5-235">PCM 輸出的必要參數。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-235">Required for PCM output.</span></span> <br/> <span data-ttu-id="a0dd5-236">數位輸出不需要。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-236">Not needed for digital output.</span></span> <br/> <span data-ttu-id="a0dd5-237">如果輸入類型是 mono、身歷聲或雙 mono (全都不會有 LFE 通道) ，唯一有效的值為2，表示身歷聲輸出。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-237">If the input type is mono, stereo, or dual-mono (all without LFE channel), the only valid value is 2, for stereo output.</span></span> <span data-ttu-id="a0dd5-238">否則，此值可以是：</span><span class="sxs-lookup"><span data-stu-id="a0dd5-238">Otherwise, the value can be:</span></span> <br/>
<ul>
<li><span data-ttu-id="a0dd5-239">適用于身歷聲 downmix 的2</span><span class="sxs-lookup"><span data-stu-id="a0dd5-239">2 for stereo downmix</span></span></li>
<li><span data-ttu-id="a0dd5-240">6適用于5.1 通道設定</span><span class="sxs-lookup"><span data-stu-id="a0dd5-240">6 for 5.1 channel configurations</span></span></li>
<li><span data-ttu-id="a0dd5-241">7.1 通道設定為8</span><span class="sxs-lookup"><span data-stu-id="a0dd5-241">8 for 7.1 channel configurations</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dd5-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="a0dd5-243">指定喇叭位置的音訊通道指派。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-243">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="a0dd5-244">如果通道數目大於2，則需要進行 PCM 輸出。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-244">Required for PCM output if the number of channels is greater than 2.</span></span> <span data-ttu-id="a0dd5-245">值必須是：</span><span class="sxs-lookup"><span data-stu-id="a0dd5-245">The value must be:</span></span><br/>
<ul>
<li><span data-ttu-id="a0dd5-246">0x3 的身歷聲輸出</span><span class="sxs-lookup"><span data-stu-id="a0dd5-246">0x3 for stereo output</span></span></li>
<li><span data-ttu-id="a0dd5-247">5.1 通道輸出的0x3F</span><span class="sxs-lookup"><span data-stu-id="a0dd5-247">0x3F for 5.1 channel output</span></span></li>
<li><span data-ttu-id="a0dd5-248">7.1 通道輸出的0x63F</span><span class="sxs-lookup"><span data-stu-id="a0dd5-248">0x63F for 7.1 channel output</span></span></li>
</ul>
<span data-ttu-id="a0dd5-249">數位輸出不需要。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-249">Not needed for digital output.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dd5-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="a0dd5-251">每個音訊樣本的位數數目。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-251">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="a0dd5-252">PCM 輸出的必要參數。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-252">Required for PCM output.</span></span> <span data-ttu-id="a0dd5-253"><strong>MFAudioFormat_Float</strong>的值必須是32，而<strong>MFAudioFormat_PCM</strong>的值必須是16。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-253">The value must be 32 for <strong>MFAudioFormat_Float</strong>, and 16 for <strong>MFAudioFormat_PCM</strong>.</span></span><br/> <span data-ttu-id="a0dd5-254">數位輸出不需要。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-254">Not needed for digital output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dd5-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="a0dd5-256">每個音訊樣本中音訊資料的有效位數。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-256">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="a0dd5-257">PCM 輸出的選擇性。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-257">Optional for PCM output.</span></span> <span data-ttu-id="a0dd5-258">如果設定，此值必須等同于 <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-258">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span><br/> <span data-ttu-id="a0dd5-259">數位輸出子類型不需要。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-259">Not needed for the digital output subtypes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0dd5-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="a0dd5-261">區塊對齊（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-261">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="a0dd5-262">PCM 輸出的選擇性。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-262">Optional for PCM output.</span></span> <span data-ttu-id="a0dd5-263">數位輸出不需要。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-263">Not needed for digital output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0dd5-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="a0dd5-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="a0dd5-265">每秒的平均位元組數。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-265">Average number of bytes per second.</span></span></td>
<td><span data-ttu-id="a0dd5-266">PCM 輸出的選擇性。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-266">Optional for PCM output.</span></span> <span data-ttu-id="a0dd5-267">數位輸出不需要。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-267">Not needed for digital output.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transform-attributes"></a><span data-ttu-id="a0dd5-268">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="a0dd5-268">Transform Attributes</span></span>

<span data-ttu-id="a0dd5-269">杜比音訊解碼器會實 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-269">The Dolby audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="a0dd5-270">應用程式可以使用這個方法來取得或設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-270">The application can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="a0dd5-271">屬性</span><span class="sxs-lookup"><span data-stu-id="a0dd5-271">Attribute</span></span>                                                                                | <span data-ttu-id="a0dd5-272">描述</span><span class="sxs-lookup"><span data-stu-id="a0dd5-272">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0dd5-273">CODECAPI \_ AVDecAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="a0dd5-273">CODECAPI\_AVDecAudioDualMono</span></span>](../directshow/avdecaudiodualmono-property.md)                        | <span data-ttu-id="a0dd5-274">指定2通道杜比音訊資料流程是否編碼為身歷聲或雙 mono。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-274">Specifies whether a 2-channel Dolby audio stream is encoded as stereo or dual-mono.</span></span> <span data-ttu-id="a0dd5-275">在解碼第一個杜比框架之前，此值為 **eAVDecAudioDualMono \_ 未指定**。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-275">Before the first Dolby frame is decoded, the value is **eAVDecAudioDualMono\_UnSpecified**.</span></span> <span data-ttu-id="a0dd5-276">解碼開始之後，此值會反映最近的杜比框架。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-276">After decoding begins, the value reflects the most recent Dolby frame.</span></span><br/> <span data-ttu-id="a0dd5-277">唯讀。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-277">Read-only.</span></span> <br/> |
| [<span data-ttu-id="a0dd5-278">CODECAPI \_ AVDecAudioDualMonoReproMode</span><span class="sxs-lookup"><span data-stu-id="a0dd5-278">CODECAPI\_AVDecAudioDualMonoReproMode</span></span>](../directshow/avdecaudiodualmonorepromode-property.md)      | <span data-ttu-id="a0dd5-279">指定解碼器如何重現雙重 mono 音訊。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-279">Specifies how the decoder reproduces dual-mono audio.</span></span> <span data-ttu-id="a0dd5-280">預設值為 **eAVDecAudioDualMonoReproMode \_ LEFT \_ MONO**。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-280">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span> <span data-ttu-id="a0dd5-281">應用程式可以隨時設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-281">The application can set this property at any time.</span></span><br/> <span data-ttu-id="a0dd5-282">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a0dd5-282">Read/write.</span></span><br/>                                                                            |
| [<span data-ttu-id="a0dd5-283">CODECAPI \_ AVDecCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="a0dd5-283">CODECAPI\_AVDecCommonMeanBitRate</span></span>](../directshow/avdeccommonmeanbitrate.md)                         | <span data-ttu-id="a0dd5-284">針對杜比數位 (AC-3) 串流，指定輸入資料流程的位元速率（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-284">For Dolby Digital (AC-3) streams, specifies the bit rate of the input stream in bits per second.</span></span> <span data-ttu-id="a0dd5-285">針對杜比數位 Plus (E-AC3) ，此值一律為零。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-285">For Dolby Digital Plus (E-AC3), the value is always zero.</span></span><br/> <span data-ttu-id="a0dd5-286">唯讀。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-286">Read only.</span></span><br/>                                                                                              |
| [<span data-ttu-id="a0dd5-287">CODECAPI \_ AVDecDDDynamicRangeScaleHigh</span><span class="sxs-lookup"><span data-stu-id="a0dd5-287">CODECAPI\_AVDecDDDynamicRangeScaleHigh</span></span>](../directshow/avdecdddynamicrangescalehigh-property.md)    | <span data-ttu-id="a0dd5-288">當解碼器執行動態範圍控制時的高階剪下。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-288">The high-level cut when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="a0dd5-289">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a0dd5-289">Read/write.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="a0dd5-290">CODECAPI \_ AVDecDDDynamicRangeScaleLow</span><span class="sxs-lookup"><span data-stu-id="a0dd5-290">CODECAPI\_AVDecDDDynamicRangeScaleLow</span></span>](../directshow/avdecdddynamicrangescalelow-property.md)      | <span data-ttu-id="a0dd5-291">當解碼器執行動態範圍控制時，低層級的提升。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-291">The low-level boost when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="a0dd5-292">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a0dd5-292">Read/write.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="a0dd5-293">CODECAPI \_ AVDecDDOperationalMode</span><span class="sxs-lookup"><span data-stu-id="a0dd5-293">CODECAPI\_AVDecDDOperationalMode</span></span>](../directshow/avdecddoperationalmode-property.md)                | <span data-ttu-id="a0dd5-294">壓縮控制模式。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-294">The compression control mode.</span></span><br/> <span data-ttu-id="a0dd5-295">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a0dd5-295">Read/write.</span></span><br/>                                                                                                                                                                                                                          |
| [<span data-ttu-id="a0dd5-296">CODECAPI \_ AVDecDDStereoDownMixMode</span><span class="sxs-lookup"><span data-stu-id="a0dd5-296">CODECAPI\_AVDecDDStereoDownMixMode</span></span>](codecapi-avdecddstereodownmixmode.md)              | <span data-ttu-id="a0dd5-297">身歷聲 downmix 的類型。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-297">The type of stereo downmix.</span></span> <span data-ttu-id="a0dd5-298">當輸入是多聲道資料流程且輸出為身歷聲資料流程時，就會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-298">This property applies when the input is a multichannel stream and the output is a stereo stream.</span></span><br/> <span data-ttu-id="a0dd5-299">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a0dd5-299">Read/write.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="a0dd5-300">MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="a0dd5-300">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE</span></span>](mft-support-dynamic-format-change-attribute.md) | <span data-ttu-id="a0dd5-301">這個屬性會傳回 **FALSE**，表示在設定新的輸入類型之前，必須先清空解碼器。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-301">This attribute returns **FALSE**, indicating that the decoder must be drained before a new input type is set.</span></span><br/> <span data-ttu-id="a0dd5-302">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a0dd5-302">Read/write.</span></span><br/>                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="a0dd5-303">備註</span><span class="sxs-lookup"><span data-stu-id="a0dd5-303">Remarks</span></span>

<span data-ttu-id="a0dd5-304">此解碼器只接受原始的杜比串流，如/52B 所定義。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-304">The decoder accepts only raw Dolby streams, as defined by A/52B.</span></span> <span data-ttu-id="a0dd5-305">不支援承載（例如 Packetized 基本資料流程） (PE) 。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-305">Payloads such as Packetized Elementary Streams (PES) are not supported.</span></span> <span data-ttu-id="a0dd5-306">針對杜比數位 Plus，解碼器會解碼為5.1 個通道。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-306">For Dolby Digital Plus, the decoder decodes up to 5.1 channels.</span></span> <span data-ttu-id="a0dd5-307">在 Windows 10 上，會在不 downmix 的情況下解碼7.1 通道資料流程。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-307">On Windows 10, 7.1 channel streams are decoded without downmix.</span></span> <span data-ttu-id="a0dd5-308">在舊版作業系統上，如果資料流程是7.1 通道，則只會解碼5.1 通道 downmix。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-308">On previous OS versions, if the stream is 7.1 channels, only the 5.1 channel downmix will be decoded.</span></span> <span data-ttu-id="a0dd5-309">如果資料流程是具有多個獨立子資料流程的杜比數位加號，則只會解碼獨立的子資料流程0。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-309">If the stream is Dolby Digital Plus with more than one independent substream, only independent substream 0 is decoded.</span></span> <span data-ttu-id="a0dd5-310">此解碼器會略過其他獨立子串流。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-310">The decoder skips other independent substreams.</span></span> <span data-ttu-id="a0dd5-311">此外，此解碼器會略過所有相依的子串流。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-311">In addition, the decoder skips all dependent substreams.</span></span> <span data-ttu-id="a0dd5-312">此解碼器支援以數位 Rights Management (DRM) 技術保護的資料流程解密和解碼。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-312">The decoder supports decryption and decoding of streams that are protected by Digital Rights Management (DRM) technology.</span></span>

<span data-ttu-id="a0dd5-313">如果輸入媒體類型具有 mono、身歷聲或雙 (mono 以外的通道設定，則在沒有 LFE 通道) 的情況下，此解碼器會提供兩個選項供輸出通道設定使用：</span><span class="sxs-lookup"><span data-stu-id="a0dd5-313">If the input media type has a channel configuration other than mono, stereo, or dual-mono (all without LFE channel), the decoder provides two options for the output channel configurations:</span></span>

-   <span data-ttu-id="a0dd5-314">8聲道輸出 (7.1 通道設定) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-314">8-channel output (7.1 channel configuration)</span></span>
-   <span data-ttu-id="a0dd5-315">6聲道輸出 (5.1 通道設定) </span><span class="sxs-lookup"><span data-stu-id="a0dd5-315">6-channel output (5.1 channel configuration)</span></span>
-   <span data-ttu-id="a0dd5-316">身歷聲 downmix</span><span class="sxs-lookup"><span data-stu-id="a0dd5-316">Stereo downmix</span></span>

<span data-ttu-id="a0dd5-317">如果選取了身歷聲 downmix，您可以使用 [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) 屬性，在 MFT 上設定 downmix 的類型。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-317">If stereo downmix is selected, the type of downmix can be set on the MFT by using the [CODECAPI\_AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) property.</span></span>

<span data-ttu-id="a0dd5-318">如果輸出類型為 **MFAudioFormat \_ 杜比 \_ AC3 \_ SPDIF**，則每個輸出緩衝區都包含6144個位元組。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-318">If the output type is **MFAudioFormat\_Dolby\_AC3\_SPDIF**, each output buffer contains 6,144 bytes.</span></span> <span data-ttu-id="a0dd5-319">緩衝區以8位元組 S/PDIF 標頭開頭，後面接著壓縮的 AC 3 框架，後面接著零填補至6144個位元組。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-319">The buffer starts with an 8-byte S/PDIF header, followed by a compressed AC-3 frame, followed by zero padding to 6,144 bytes.</span></span>

<span data-ttu-id="a0dd5-320">如果輸出類型為 **KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ 杜比 \_ 數位 \_ 加號**，則每個輸出緩衝區都包含24576個位元組。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-320">If the output type is **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**, each output buffer contains 24,576 bytes.</span></span> <span data-ttu-id="a0dd5-321">緩衝區是以8位元組 S/PDIF 標頭為開頭，後面接著1–6個壓縮的杜比數位加框架，對應至 1536 PCM 範例，後面接著零填補至24576個位元組。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-321">The buffer starts with an 8-byte S/PDIF header, followed by 1–6 compressed Dolby Digital Plus frames corresponding to 1,536 PCM samples, followed by zero padding to 24,576 bytes.</span></span> <span data-ttu-id="a0dd5-322">針對 HDMI 輸出，只會封裝獨立的子串流0。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-322">For HDMI output, only independent substream 0 is packed.</span></span>

<span data-ttu-id="a0dd5-323">已向旗標 **mft \_ 列舉 \_ 旗標 \_ FIELDOFUSE** 註冊解碼器 mft，這表示必須由應用程式解除鎖定才能使用的 mft。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-323">The decoder MFT is registered with the flag **MFT\_ENUM\_FLAG\_FIELDOFUSE**, which indicates that the MFT that must be unlocked by the application before use.</span></span> <span data-ttu-id="a0dd5-324">如需詳細資訊，請參閱 [使用限制欄位](field-of-use-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="a0dd5-324">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0dd5-325">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0dd5-325">Requirements</span></span>



| <span data-ttu-id="a0dd5-326">需求</span><span class="sxs-lookup"><span data-stu-id="a0dd5-326">Requirement</span></span> | <span data-ttu-id="a0dd5-327">值</span><span class="sxs-lookup"><span data-stu-id="a0dd5-327">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0dd5-328">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0dd5-328">Minimum supported client</span></span><br/> | <span data-ttu-id="a0dd5-329">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0dd5-329">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="a0dd5-330">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0dd5-330">Minimum supported server</span></span><br/> | <span data-ttu-id="a0dd5-331">都不支援</span><span class="sxs-lookup"><span data-stu-id="a0dd5-331">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="a0dd5-332">DLL</span><span class="sxs-lookup"><span data-stu-id="a0dd5-332">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0dd5-333"><dt>Msauddecmft.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0dd5-333"><dt>Msauddecmft.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0dd5-334">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0dd5-334">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0dd5-335">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="a0dd5-335">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
