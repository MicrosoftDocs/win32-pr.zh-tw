---
description: 音訊子類型 Guid
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: 音訊子類型 Guid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04192f19f530c288b9aef7b5718b8329ea108bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468652"
---
# <a name="audio-subtype-guids"></a><span data-ttu-id="d2891-103">音訊子類型 Guid</span><span class="sxs-lookup"><span data-stu-id="d2891-103">Audio Subtype GUIDs</span></span>

<span data-ttu-id="d2891-104">已定義下列音訊子類型 Guid。</span><span class="sxs-lookup"><span data-stu-id="d2891-104">The following audio subtype GUIDs are defined.</span></span> <span data-ttu-id="d2891-105">若要指定子類型，請在媒體類型上設定 [ [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="d2891-105">To specify the subtype, set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="d2891-106">除非有注明，否則這些常數會定義在標頭檔 mfapi 中。</span><span class="sxs-lookup"><span data-stu-id="d2891-106">Except where noted, these constants are defined in the header file mfapi.h.</span></span>

<span data-ttu-id="d2891-107">使用這些子類型時，請將 [ [MF \_ MT \_ 主要 \_ 類型](mf-mt-major-type-attribute.md) ] 屬性設定為 [ **MFMediaType \_ 音訊**]。</span><span class="sxs-lookup"><span data-stu-id="d2891-107">When these subtypes are used, set the [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2891-108">GUID</span><span class="sxs-lookup"><span data-stu-id="d2891-108">GUID</span></span></th>
<th><span data-ttu-id="d2891-109">Description</span><span class="sxs-lookup"><span data-stu-id="d2891-109">Description</span></span></th>
<th><span data-ttu-id="d2891-110">格式化標記 (FOURCC) </span><span class="sxs-lookup"><span data-stu-id="d2891-110">Format Tag (FOURCC)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2891-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span></span></td>
<td><span data-ttu-id="d2891-112">Advanced Audio 編碼 (AAC) 。</span><span class="sxs-lookup"><span data-stu-id="d2891-112">Advanced Audio Coding (AAC).</span></span><br/> <span data-ttu-id="d2891-113">此子類型是用於包含在音訊格式標記等於0x00FF 之 AVI 檔案中的 AAC。</span><span class="sxs-lookup"><span data-stu-id="d2891-113">This subtype is used for AAC contained in an AVI file with an audio format tag equal to 0x00FF.</span></span> <br/> <span data-ttu-id="d2891-114">如需詳細資訊，請參閱 <a href="aac-decoder.md"><strong>AAC 解碼器</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="d2891-114">For more information, see <a href="aac-decoder.md"><strong>AAC Decoder</strong></a>.</span></span><br/> <span data-ttu-id="d2891-115">定義于 wmcodecdsp .h 中</span><span class="sxs-lookup"><span data-stu-id="d2891-115">Defined in wmcodecdsp.h</span></span><br/></td>
<td><span data-ttu-id="d2891-116">WAVE_FORMAT_RAW_AAC1 (0x00FF) </span><span class="sxs-lookup"><span data-stu-id="d2891-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2891-117"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-117"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="d2891-118">Advanced Audio 編碼 (AAC) 。</span><span class="sxs-lookup"><span data-stu-id="d2891-118">Advanced Audio Coding (AAC).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2891-119">相當於 MEDIASUBTYPE_MPEG_HEAAC，定義于 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="d2891-119">Equivalent to MEDIASUBTYPE_MPEG_HEAAC, defined in wmcodecdsp.h.</span></span>
</blockquote>
<br/> <span data-ttu-id="d2891-120">資料流程可以在音訊資料傳輸資料流程中包含原始的 AAC 資料或 AAC 資料 (ADTS) 串流。</span><span class="sxs-lookup"><span data-stu-id="d2891-120">The stream can contain raw AAC data or AAC data in an Audio Data Transport Stream (ADTS) stream.</span></span><br/> <span data-ttu-id="d2891-121">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d2891-121">For more information, see:</span></span><br/>
<ul>
<li><span data-ttu-id="d2891-122"><a href="aac-decoder.md"><strong>AAC 解碼器</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2891-122"><a href="aac-decoder.md"><strong>AAC Decoder</strong></a></span></span></li>
<li><span data-ttu-id="d2891-123"><a href="mpeg-4-file-source.md">MPEG-2 檔案來源</a></span><span class="sxs-lookup"><span data-stu-id="d2891-123"><a href="mpeg-4-file-source.md">MPEG-4 File Source</a></span></span></li>
</ul></td>
<td><span data-ttu-id="d2891-124">WAVE_FORMAT_MPEG_HEAAC (0x1610) </span><span class="sxs-lookup"><span data-stu-id="d2891-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2891-125"><strong>MFAudioFormat_ADTS</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-125"><strong>MFAudioFormat_ADTS</strong></span></span></td>
<td><span data-ttu-id="d2891-126">未使用。</span><span class="sxs-lookup"><span data-stu-id="d2891-126">Not used.</span></span></td>
<td><span data-ttu-id="d2891-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600) </span><span class="sxs-lookup"><span data-stu-id="d2891-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2891-128"><strong>MFAudioFormat_ALAC</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-128"><strong>MFAudioFormat_ALAC</strong></span></span></td>
<td><span data-ttu-id="d2891-129">Apple 無失真音訊編解碼器</span><span class="sxs-lookup"><span data-stu-id="d2891-129">Apple Lossless Audio Codec</span></span><br/> <span data-ttu-id="d2891-130">在 Windows 10 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="d2891-130">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="d2891-131">WAVE_FORMAT_ALAC (0x6C61) </span><span class="sxs-lookup"><span data-stu-id="d2891-131">WAVE_FORMAT_ALAC (0x6C61)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2891-132"><strong>MFAudioFormat_AMR_NB</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-132"><strong>MFAudioFormat_AMR_NB</strong></span></span></td>
<td><span data-ttu-id="d2891-133">Adaptative 多速率音訊</span><span class="sxs-lookup"><span data-stu-id="d2891-133">Adaptative Multi-Rate audio</span></span><br/> <span data-ttu-id="d2891-134">在 Windows 8.1 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="d2891-134">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="d2891-135">WAVE_FORMAT_AMR_NB</span><span class="sxs-lookup"><span data-stu-id="d2891-135">WAVE_FORMAT_AMR_NB</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2891-136"><strong>MFAudioFormat_AMR_WB</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-136"><strong>MFAudioFormat_AMR_WB</strong></span></span></td>
<td><span data-ttu-id="d2891-137">Adaptative 多比率寬頻音訊</span><span class="sxs-lookup"><span data-stu-id="d2891-137">Adaptative Multi-Rate Wideband audio</span></span><br/> <span data-ttu-id="d2891-138">在 Windows 8.1 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="d2891-138">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="d2891-139">WAVE_FORMAT_AMR_WB</span><span class="sxs-lookup"><span data-stu-id="d2891-139">WAVE_FORMAT_AMR_WB</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2891-140"><strong>MFAudioFormat_AMR_WP</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-140"><strong>MFAudioFormat_AMR_WP</strong></span></span></td>
<td><span data-ttu-id="d2891-141">在 Windows 8.1 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="d2891-141">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="d2891-142">WAVE_FORMAT_AMR_WP</span><span class="sxs-lookup"><span data-stu-id="d2891-142">WAVE_FORMAT_AMR_WP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2891-143"><strong>MFAudioFormat_Dolby_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-143"><strong>MFAudioFormat_Dolby_AC3</strong></span></span></td>
<td><span data-ttu-id="d2891-144">杜比數位 (AC-3) 。</span><span class="sxs-lookup"><span data-stu-id="d2891-144">Dolby Digital (AC-3).</span></span><br/> <span data-ttu-id="d2891-145">與 <strong>MEDIASUBTYPE_DOLBY_AC3</strong>相同的 GUID 值，其定義于 ksuuids 中。</span><span class="sxs-lookup"><span data-stu-id="d2891-145">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, which is defined in ksuuids.h</span></span><br/></td>
<td><span data-ttu-id="d2891-146">無。</span><span class="sxs-lookup"><span data-stu-id="d2891-146">None.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2891-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span></span></td>
<td><span data-ttu-id="d2891-148">透過索尼/Philips 數位介面 (S/PDIF) 的杜比 AC-3 音訊。</span><span class="sxs-lookup"><span data-stu-id="d2891-148">Dolby AC-3 audio over Sony/Philips Digital Interface (S/PDIF).</span></span><br/> <span data-ttu-id="d2891-149">這個 GUID 值與下列子類型相同：</span><span class="sxs-lookup"><span data-stu-id="d2891-149">This GUID value is identical to the following subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="d2891-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>，定義于 ksmedia 中。</span><span class="sxs-lookup"><span data-stu-id="d2891-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, defined in ksmedia.h.</span></span></li>
<li><span data-ttu-id="d2891-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>，定義于 uuid. h 中。</span><span class="sxs-lookup"><span data-stu-id="d2891-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, defined in uuids.h.</span></span></li>
</ul></td>
<td><span data-ttu-id="d2891-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092) </span><span class="sxs-lookup"><span data-stu-id="d2891-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2891-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span></span></td>
<td><span data-ttu-id="d2891-154">杜比數位 Plus。</span><span class="sxs-lookup"><span data-stu-id="d2891-154">Dolby Digital Plus.</span></span><br/> <span data-ttu-id="d2891-155">與 <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>相同的 GUID 值，其定義于 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="d2891-155">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, which is defined in wmcodecdsp.h.</span></span><br/></td>
<td><span data-ttu-id="d2891-156">無</span><span class="sxs-lookup"><span data-stu-id="d2891-156">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2891-157"><strong>MFAudioFormat_DRM</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-157"><strong>MFAudioFormat_DRM</strong></span></span></td>
<td><span data-ttu-id="d2891-158">搭配安全音訊路徑使用的加密音訊資料。</span><span class="sxs-lookup"><span data-stu-id="d2891-158">Encrypted audio data used with secure audio path.</span></span></td>
<td><span data-ttu-id="d2891-159">WAVE_FORMAT_DRM (0x0009) </span><span class="sxs-lookup"><span data-stu-id="d2891-159">WAVE_FORMAT_DRM (0x0009)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2891-160"><strong>MFAudioFormat_DTS</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-160"><strong>MFAudioFormat_DTS</strong></span></span></td>
<td><span data-ttu-id="d2891-161">數位劇院系統 (DTS) 音訊。</span><span class="sxs-lookup"><span data-stu-id="d2891-161">Digital Theater Systems (DTS) audio.</span></span></td>
<td><span data-ttu-id="d2891-162">WAVE_FORMAT_DTS (0x0008) </span><span class="sxs-lookup"><span data-stu-id="d2891-162">WAVE_FORMAT_DTS (0x0008)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2891-163"><strong>MFAudioFormat_FLAC</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-163"><strong>MFAudioFormat_FLAC</strong></span></span></td>
<td><span data-ttu-id="d2891-164">免費的無失真音訊編解碼器</span><span class="sxs-lookup"><span data-stu-id="d2891-164">Free Lossless Audio Codec</span></span><br/> <span data-ttu-id="d2891-165">在 Windows 10 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="d2891-165">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="d2891-166">WAVE_FORMAT_FLAC (0xF1AC) </span><span class="sxs-lookup"><span data-stu-id="d2891-166">WAVE_FORMAT_FLAC (0xF1AC)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2891-167"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-167"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="d2891-168">未壓縮的 IEEE 浮點音訊。</span><span class="sxs-lookup"><span data-stu-id="d2891-168">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="d2891-169">WAVE_FORMAT_IEEE_FLOAT (0x0003) </span><span class="sxs-lookup"><span data-stu-id="d2891-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2891-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span></span></td>
<td><span data-ttu-id="d2891-171">未壓縮的 IEEE 浮點音訊。</span><span class="sxs-lookup"><span data-stu-id="d2891-171">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="d2891-172">無</span><span class="sxs-lookup"><span data-stu-id="d2891-172">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2891-173"><strong>MFAudioFormat_MP3</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-173"><strong>MFAudioFormat_MP3</strong></span></span></td>
<td><span data-ttu-id="d2891-174">MPEG 音訊第3層 (MP3) 。</span><span class="sxs-lookup"><span data-stu-id="d2891-174">MPEG Audio Layer-3 (MP3).</span></span></td>
<td><span data-ttu-id="d2891-175">WAVE_FORMAT_MPEGLAYER3 (0x0055) </span><span class="sxs-lookup"><span data-stu-id="d2891-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2891-176"><strong>MFAudioFormat_MPEG</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-176"><strong>MFAudioFormat_MPEG</strong></span></span></td>
<td><span data-ttu-id="d2891-177">MPEG-2 音訊承載。</span><span class="sxs-lookup"><span data-stu-id="d2891-177">MPEG-1 audio payload.</span></span></td>
<td><span data-ttu-id="d2891-178">WAVE_FORMAT_MPEG (0x0050) </span><span class="sxs-lookup"><span data-stu-id="d2891-178">WAVE_FORMAT_MPEG (0x0050)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2891-179"><strong>MFAudioFormat_MSP1</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-179"><strong>MFAudioFormat_MSP1</strong></span></span></td>
<td><span data-ttu-id="d2891-180">Windows Media 音訊9語音編解碼器。</span><span class="sxs-lookup"><span data-stu-id="d2891-180">Windows Media Audio 9 Voice codec.</span></span></td>
<td><span data-ttu-id="d2891-181">WAVE_FORMAT_WMAVOICE9 (0x000A) </span><span class="sxs-lookup"><span data-stu-id="d2891-181">WAVE_FORMAT_WMAVOICE9 (0x000A)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2891-182"><strong>MFAudioFormat_Opus</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-182"><strong>MFAudioFormat_Opus</strong></span></span></td>
<td><span data-ttu-id="d2891-183">Opus</span><span class="sxs-lookup"><span data-stu-id="d2891-183">Opus</span></span><br/> <span data-ttu-id="d2891-184">在 Windows 10 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="d2891-184">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="d2891-185">WAVE_FORMAT_OPUS (0x704F) </span><span class="sxs-lookup"><span data-stu-id="d2891-185">WAVE_FORMAT_OPUS (0x704F)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2891-186"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-186"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="d2891-187">未壓縮的 PCM 音訊。</span><span class="sxs-lookup"><span data-stu-id="d2891-187">Uncompressed PCM audio.</span></span></td>
<td><span data-ttu-id="d2891-188">WAVE_FORMAT_PCM (1) </span><span class="sxs-lookup"><span data-stu-id="d2891-188">WAVE_FORMAT_PCM (1)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2891-189"><strong>MFAudioFormat_QCELP</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-189"><strong>MFAudioFormat_QCELP</strong></span></span></td>
<td><span data-ttu-id="d2891-190">QCELP (的 Qualcomm 程式碼興奮線性預測) 音訊。</span><span class="sxs-lookup"><span data-stu-id="d2891-190">QCELP (Qualcomm Code Excited Linear Prediction) audio.</span></span></td>
<td><span data-ttu-id="d2891-191">無</span><span class="sxs-lookup"><span data-stu-id="d2891-191">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2891-192"><strong>MFAudioFormat_WMASPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-192"><strong>MFAudioFormat_WMASPDIF</strong></span></span></td>
<td><span data-ttu-id="d2891-193">S/PDIF Windows Media 音訊 9 Professional 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="d2891-193">Windows Media Audio 9 Professional codec over S/PDIF.</span></span></td>
<td><span data-ttu-id="d2891-194">WAVE_FORMAT_WMASPDIF (0x0164) </span><span class="sxs-lookup"><span data-stu-id="d2891-194">WAVE_FORMAT_WMASPDIF (0x0164)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2891-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span></span></td>
<td><span data-ttu-id="d2891-196">Windows Media 音訊9無失真編解碼器或 Windows Media 音訊9.1 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="d2891-196">Windows Media Audio 9 Lossless codec or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="d2891-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163) </span><span class="sxs-lookup"><span data-stu-id="d2891-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2891-198"><strong>MFAudioFormat_WMAudioV8</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-198"><strong>MFAudioFormat_WMAudioV8</strong></span></span></td>
<td><span data-ttu-id="d2891-199">Windows Media 音訊8編解碼器、Windows Media 音訊9編解碼器或 Windows Media 音訊9.1 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="d2891-199">Windows Media Audio 8 codec, Windows Media Audio 9 codec, or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="d2891-200">WAVE_FORMAT_WMAUDIO2 (0x0161) </span><span class="sxs-lookup"><span data-stu-id="d2891-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2891-201"><strong>MFAudioFormat_WMAudioV9</strong></span><span class="sxs-lookup"><span data-stu-id="d2891-201"><strong>MFAudioFormat_WMAudioV9</strong></span></span></td>
<td><span data-ttu-id="d2891-202">Windows Media 音訊 9 Professional 編解碼器或 Windows Media 音訊 9.1 Professional 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="d2891-202">Windows Media Audio 9 Professional codec or Windows Media Audio 9.1 Professional codec.</span></span></td>
<td><span data-ttu-id="d2891-203">WAVE_FORMAT_WMAUDIO3 (0x0162) </span><span class="sxs-lookup"><span data-stu-id="d2891-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d2891-204">此資料表的第三個數據行中所列的格式標記會在 **WAVEFORMATEX** 結構中使用，並定義于標頭檔 mmreg 中。</span><span class="sxs-lookup"><span data-stu-id="d2891-204">The format tags listed in the third column of this table are used in the **WAVEFORMATEX** structure, and are defined in the header file mmreg.h.</span></span>

<span data-ttu-id="d2891-205">指定音訊格式標記時，您可以建立音訊子類型 GUID，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d2891-205">Given an audio format tag, you can create an audio subtype GUID as follows:</span></span>

1.  <span data-ttu-id="d2891-206">從值 **MFAudioFormat \_ Base** 開始，此值定義于 mfaph 中。</span><span class="sxs-lookup"><span data-stu-id="d2891-206">Start with the value **MFAudioFormat\_Base**, which is defined in mfaph.i.</span></span>
2.  <span data-ttu-id="d2891-207">以格式標記取代這個 GUID 的第一個 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="d2891-207">Replace the first **DWORD** of this GUID with the format tag.</span></span>

<span data-ttu-id="d2891-208">您可以使用 [**定義 \_ 媒體 \_ guid**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) 宏來定義遵循此模式的新 GUID 常數。</span><span class="sxs-lookup"><span data-stu-id="d2891-208">You can use the [**DEFINE\_MEDIATYPE\_GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) macro to define a new GUID constant that follows this pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2891-209">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2891-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2891-210">音訊媒體類型</span><span class="sxs-lookup"><span data-stu-id="d2891-210">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="d2891-211">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d2891-211">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="d2891-212">媒體類型 Guid</span><span class="sxs-lookup"><span data-stu-id="d2891-212">Media Type GUIDs</span></span>](media-type-guids.md)
</dt> <dt>

[<span data-ttu-id="d2891-213">媒體類型</span><span class="sxs-lookup"><span data-stu-id="d2891-213">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




