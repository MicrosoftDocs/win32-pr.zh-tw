---
description: Windows Media 音訊解碼器會將 Windows Media 音訊編碼器編碼的音訊串流解碼。
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: 'Windows Media 音訊 (Wmcodecdsp 的解碼器) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984296"
---
# <a name="windows-media-audio-decoder"></a><span data-ttu-id="e2d69-103">Windows Media 音訊的解碼器</span><span class="sxs-lookup"><span data-stu-id="e2d69-103">Windows Media Audio Decoder</span></span>

<span data-ttu-id="e2d69-104">Windows Media 音訊解碼器會將 [**Windows Media 音訊編碼器**](windowsmediaaudioencoder.md)編碼的音訊串流解碼。</span><span class="sxs-lookup"><span data-stu-id="e2d69-104">The Windows Media Audio decoder decodes audio streams that were encoded by the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span> <span data-ttu-id="e2d69-105">編碼器和解碼器支援三種編碼音訊類別： Windows Media 音訊 Standard、Windows Media 音訊 Professional 和 Windows Media 音訊不失真。</span><span class="sxs-lookup"><span data-stu-id="e2d69-105">The encoder and decoder support three categories of encoded audio: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="e2d69-106">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="e2d69-106">Class Identifier</span></span>

<span data-ttu-id="e2d69-107">Windows Media 音訊解碼器 (CLSID) 的類別識別碼是以常數 **CLSID \_ CWMADecMediaObject** 來表示。</span><span class="sxs-lookup"><span data-stu-id="e2d69-107">The class identifier (CLSID) for the Windows Media Audio decoder is represented by the constant **CLSID\_CWMADecMediaObject**.</span></span> <span data-ttu-id="e2d69-108">您可以藉由呼叫 **CoCreateInstance** 來建立音訊解碼器的實例。</span><span class="sxs-lookup"><span data-stu-id="e2d69-108">You can create an instance of the audio decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="e2d69-109">輸入格式</span><span class="sxs-lookup"><span data-stu-id="e2d69-109">Input Formats</span></span>

<span data-ttu-id="e2d69-110">下表顯示的音訊格式標記代表 Windows Media 音訊的解碼器所支援的輸入分類。</span><span class="sxs-lookup"><span data-stu-id="e2d69-110">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio decoder.</span></span> <span data-ttu-id="e2d69-111">如需有關如何設定此解碼器之輸入和輸出類型的詳細資訊，請參閱設定 [音訊解碼](configuringaudiodecoding.md)。</span><span class="sxs-lookup"><span data-stu-id="e2d69-111">For information about how to set the input and output types for the decoder, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>



| <span data-ttu-id="e2d69-112">格式化標記常數</span><span class="sxs-lookup"><span data-stu-id="e2d69-112">Format tag constant</span></span>             | <span data-ttu-id="e2d69-113">格式化標記值</span><span class="sxs-lookup"><span data-stu-id="e2d69-113">Format tag value</span></span> | <span data-ttu-id="e2d69-114">音訊格式</span><span class="sxs-lookup"><span data-stu-id="e2d69-114">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="e2d69-115">WAVE \_ 格式 \_ WMAUDIO2</span><span class="sxs-lookup"><span data-stu-id="e2d69-115">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="e2d69-116">0x0161</span><span class="sxs-lookup"><span data-stu-id="e2d69-116">0x0161</span></span>           | <span data-ttu-id="e2d69-117">Windows Media 音訊標準</span><span class="sxs-lookup"><span data-stu-id="e2d69-117">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="e2d69-118">WAVE \_ 格式 \_ WMAUDIO3</span><span class="sxs-lookup"><span data-stu-id="e2d69-118">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="e2d69-119">0x0162</span><span class="sxs-lookup"><span data-stu-id="e2d69-119">0x0162</span></span>           | <span data-ttu-id="e2d69-120">Windows Media 音訊專業人員</span><span class="sxs-lookup"><span data-stu-id="e2d69-120">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="e2d69-121">WAVE \_ 格式 \_ WMAUDIO \_ 無損</span><span class="sxs-lookup"><span data-stu-id="e2d69-121">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="e2d69-122">0x0163</span><span class="sxs-lookup"><span data-stu-id="e2d69-122">0x0163</span></span>           | <span data-ttu-id="e2d69-123">Windows Media 音訊無損</span><span class="sxs-lookup"><span data-stu-id="e2d69-123">Windows Media Audio Lossless</span></span>     |



 

## <a name="output-formats"></a><span data-ttu-id="e2d69-124">輸出格式</span><span class="sxs-lookup"><span data-stu-id="e2d69-124">Output Formats</span></span>

<span data-ttu-id="e2d69-125">下表顯示的音訊格式標記代表 **Windows Media 音訊的解碼器** 所支援的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="e2d69-125">The following table shows the audio format tags that represent the output types supported by the **Windows Media Audio Decoder**.</span></span> <span data-ttu-id="e2d69-126">如需有關如何設定編碼器之輸入和輸出類型的詳細資訊，請參閱設定 [音訊編碼](configuringaudioencoding.md)。</span><span class="sxs-lookup"><span data-stu-id="e2d69-126">For information about how to set the input and output types for the decoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="e2d69-127">格式化標記常數</span><span class="sxs-lookup"><span data-stu-id="e2d69-127">Format tag constant</span></span>       | <span data-ttu-id="e2d69-128">格式化標記值</span><span class="sxs-lookup"><span data-stu-id="e2d69-128">Format tag value</span></span> | <span data-ttu-id="e2d69-129">音訊格式</span><span class="sxs-lookup"><span data-stu-id="e2d69-129">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="e2d69-130">WAVE \_ 格式 \_ PCM</span><span class="sxs-lookup"><span data-stu-id="e2d69-130">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="e2d69-131">0x0001</span><span class="sxs-lookup"><span data-stu-id="e2d69-131">0x0001</span></span>           | <span data-ttu-id="e2d69-132">PCM 格式</span><span class="sxs-lookup"><span data-stu-id="e2d69-132">PCM format</span></span>                                            |
| <span data-ttu-id="e2d69-133">WAVE \_ 格式 \_ IEEE \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="e2d69-133">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="e2d69-134">0x0003</span><span class="sxs-lookup"><span data-stu-id="e2d69-134">0x0003</span></span>           | <span data-ttu-id="e2d69-135">IEEE 浮點數</span><span class="sxs-lookup"><span data-stu-id="e2d69-135">IEEE floating point</span></span>                                   |
| <span data-ttu-id="e2d69-136">WAVE \_ 格式 \_ 可擴充</span><span class="sxs-lookup"><span data-stu-id="e2d69-136">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="e2d69-137">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="e2d69-137">0xFFFE</span></span>           | <span data-ttu-id="e2d69-138">**WAVEFORMATEXTENSIBLE** 結構中的 PCM/IEEE 格式</span><span class="sxs-lookup"><span data-stu-id="e2d69-138">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="e2d69-139">介面</span><span class="sxs-lookup"><span data-stu-id="e2d69-139">Interfaces</span></span>

<span data-ttu-id="e2d69-140">音訊解碼物件會公開 **IMediaObject** 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 **IMFTransform** 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="e2d69-140">An audio decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="e2d69-141">Windows Media 音訊的解碼器會根據您所取得的介面和執行的 Windows 版本，以一或 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="e2d69-141">A Windows Media Audio decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="e2d69-142">下表顯示音訊解碼器以 SQL-DMO 或 MFT 的行為條件。</span><span class="sxs-lookup"><span data-stu-id="e2d69-142">The following table shows the conditions under which an audio decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="e2d69-143">作業系統</span><span class="sxs-lookup"><span data-stu-id="e2d69-143">Operating system</span></span> | <span data-ttu-id="e2d69-144">解碼器行為</span><span class="sxs-lookup"><span data-stu-id="e2d69-144">Decoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d69-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e2d69-145">Windows XP</span></span>       | <span data-ttu-id="e2d69-146">Windows Media 音訊的解碼器一律會以 SQL-DMO 的方式運作。</span><span class="sxs-lookup"><span data-stu-id="e2d69-146">A Windows Media Audio decoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="e2d69-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2d69-147">Windows Vista</span></span>    | <span data-ttu-id="e2d69-148">Windows Media 音訊的解碼器預設會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="e2d69-148">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="e2d69-149">如果您在音訊解碼器上取得 **IMFTransform** 介面或 **IPropertyStore** 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="e2d69-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="e2d69-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2d69-150">Windows 7</span></span>        | <span data-ttu-id="e2d69-151">Windows Media 音訊的解碼器預設會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="e2d69-151">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="e2d69-152">如果您在音訊解碼器上取得 **IMFTransform** 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="e2d69-152">If you obtain an **IMFTransform** interface on an audio decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="properties"></a><span data-ttu-id="e2d69-153">屬性</span><span class="sxs-lookup"><span data-stu-id="e2d69-153">Properties</span></span>

<span data-ttu-id="e2d69-154">Windows Media 音訊的解碼器支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="e2d69-154">The Windows Media Audio decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e2d69-155">屬性</span><span class="sxs-lookup"><span data-stu-id="e2d69-155">Property</span></span></th>
<th><span data-ttu-id="e2d69-156">描述</span><span class="sxs-lookup"><span data-stu-id="e2d69-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e2d69-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2d69-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span></span></td>
<td><span data-ttu-id="e2d69-158">指定在解碼檔案結尾可能會傳回的額外 PCM 樣本數上限。</span><span class="sxs-lookup"><span data-stu-id="e2d69-158">Specifies the maximum number of additional PCM samples that might be returned at the end of decoding a file.</span></span><br/> <dl> <span data-ttu-id="e2d69-159">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="e2d69-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="e2d69-160">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="e2d69-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="e2d69-161">唯讀。</span><span class="sxs-lookup"><span data-stu-id="e2d69-161">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2d69-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2d69-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span></span></td>
<td><span data-ttu-id="e2d69-163">指定音訊解碼器將使用的動態範圍控制模式。</span><span class="sxs-lookup"><span data-stu-id="e2d69-163">Specifies the dynamic-range control mode that the audio decoder will use.</span></span><br/> <dl> <span data-ttu-id="e2d69-164">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="e2d69-164">Windows XP and later.</span></span><br />
<span data-ttu-id="e2d69-165">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="e2d69-165">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="e2d69-166">唯寫。</span><span class="sxs-lookup"><span data-stu-id="e2d69-166">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2d69-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2d69-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span></span></td>
<td><span data-ttu-id="e2d69-168">指定作者提供的折迭係數，可針對比編碼的資料流程所包含的通道更少的通道來解碼多頻道音訊。</span><span class="sxs-lookup"><span data-stu-id="e2d69-168">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span> <br/> <dl> <span data-ttu-id="e2d69-169">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="e2d69-169">Windows XP and later.</span></span><br />
<span data-ttu-id="e2d69-170">Professional</span><span class="sxs-lookup"><span data-stu-id="e2d69-170">Professional</span></span><br />
<span data-ttu-id="e2d69-171">唯寫。</span><span class="sxs-lookup"><span data-stu-id="e2d69-171">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2d69-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2d69-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="e2d69-173">指定音訊解碼器是否應提供高解析度的輸出。</span><span class="sxs-lookup"><span data-stu-id="e2d69-173">Specifies whether the audio decoder should deliver high-resolution output.</span></span><br/> <dl> <span data-ttu-id="e2d69-174">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="e2d69-174">Windows XP and later.</span></span><br />
<span data-ttu-id="e2d69-175">Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="e2d69-175">Professional, Lossless.</span></span><br />
<span data-ttu-id="e2d69-176">唯寫。</span><span class="sxs-lookup"><span data-stu-id="e2d69-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2d69-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2d69-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="e2d69-178">指定音訊解碼器是否應該執行 Lt-Rt 折迭。</span><span class="sxs-lookup"><span data-stu-id="e2d69-178">Specifies whether the audio decoder should perform Lt-Rt fold down.</span></span><br/> <dl> <span data-ttu-id="e2d69-179">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="e2d69-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="e2d69-180">Professional。</span><span class="sxs-lookup"><span data-stu-id="e2d69-180">Professional.</span></span><br />
<span data-ttu-id="e2d69-181">唯寫。</span><span class="sxs-lookup"><span data-stu-id="e2d69-181">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2d69-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2d69-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span></span></td>
<td><span data-ttu-id="e2d69-183">指定用戶端電腦上的說話者設定。</span><span class="sxs-lookup"><span data-stu-id="e2d69-183">Specifies the speaker configuration on the client computer.</span></span><br/> <dl> <span data-ttu-id="e2d69-184">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="e2d69-184">Windows XP and later.</span></span><br />
<span data-ttu-id="e2d69-185">Professional。</span><span class="sxs-lookup"><span data-stu-id="e2d69-185">Professional.</span></span><br />
<span data-ttu-id="e2d69-186">唯寫。</span><span class="sxs-lookup"><span data-stu-id="e2d69-186">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2d69-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2d69-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="e2d69-188">指定音訊內容的平均音量層級。</span><span class="sxs-lookup"><span data-stu-id="e2d69-188">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="e2d69-189">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="e2d69-189">Windows XP and later.</span></span><br />
<span data-ttu-id="e2d69-190">Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="e2d69-190">Professional, Lossless.</span></span><br />
<span data-ttu-id="e2d69-191">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e2d69-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2d69-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2d69-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span></span></td>
<td><span data-ttu-id="e2d69-193">指定輸出音訊內容所需的平均音量層級。</span><span class="sxs-lookup"><span data-stu-id="e2d69-193">Specifies the desired average volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="e2d69-194">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="e2d69-194">Windows XP and later.</span></span><br />
<span data-ttu-id="e2d69-195">Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="e2d69-195">Professional, Lossless.</span></span><br />
<span data-ttu-id="e2d69-196">唯寫。</span><span class="sxs-lookup"><span data-stu-id="e2d69-196">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2d69-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2d69-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="e2d69-198">指定音訊內容中發生的最高音量層級。</span><span class="sxs-lookup"><span data-stu-id="e2d69-198">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="e2d69-199">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="e2d69-199">Windows XP and later.</span></span><br />
<span data-ttu-id="e2d69-200">Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="e2d69-200">Professional, Lossless.</span></span><br />
<span data-ttu-id="e2d69-201">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e2d69-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2d69-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2d69-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span></span></td>
<td><span data-ttu-id="e2d69-203">指定輸出音訊內容所需的最大音量層級。</span><span class="sxs-lookup"><span data-stu-id="e2d69-203">Specifies the desired maximum volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="e2d69-204">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="e2d69-204">Windows XP and later.</span></span><br />
<span data-ttu-id="e2d69-205">Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="e2d69-205">Professional, Lossless.</span></span><br />
<span data-ttu-id="e2d69-206">唯寫。</span><span class="sxs-lookup"><span data-stu-id="e2d69-206">Write-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="e2d69-207">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2d69-207">Requirements</span></span>



| <span data-ttu-id="e2d69-208">需求</span><span class="sxs-lookup"><span data-stu-id="e2d69-208">Requirement</span></span> | <span data-ttu-id="e2d69-209">值</span><span class="sxs-lookup"><span data-stu-id="e2d69-209">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d69-210">用戶端</span><span class="sxs-lookup"><span data-stu-id="e2d69-210">Client</span></span><br/> | <span data-ttu-id="e2d69-211">Windows XP、Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2d69-211">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="e2d69-212">標頭</span><span class="sxs-lookup"><span data-stu-id="e2d69-212">Header</span></span><br/> | <dl> <span data-ttu-id="e2d69-213"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2d69-213"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="e2d69-214">DLL</span><span class="sxs-lookup"><span data-stu-id="e2d69-214">DLL</span></span><br/>    | <dl> <span data-ttu-id="e2d69-215"><dt>Wmadmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2d69-215"><dt>Wmadmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e2d69-216">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2d69-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d69-217">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="e2d69-217">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="e2d69-218">編解碼器實行</span><span class="sxs-lookup"><span data-stu-id="e2d69-218">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




