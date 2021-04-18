---
description: Windows Media 音訊編碼器會編碼音訊串流。 編碼器支援三種編碼輸出類別： Windows Media 音訊 Standard、Windows Media 音訊 Professional 和 Windows Media 音訊不失真。
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: 'Windows Media 音訊編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976207"
---
# <a name="windows-media-audio-encoder"></a><span data-ttu-id="9ee02-104">Windows Media 音訊編碼器</span><span class="sxs-lookup"><span data-stu-id="9ee02-104">Windows Media Audio Encoder</span></span>

<span data-ttu-id="9ee02-105">Windows Media 音訊編碼器會編碼音訊串流。</span><span class="sxs-lookup"><span data-stu-id="9ee02-105">The Windows Media Audio encoder encodes audio streams.</span></span> <span data-ttu-id="9ee02-106">編碼器支援三種編碼輸出類別： Windows Media 音訊 Standard、Windows Media 音訊 Professional 和 Windows Media 音訊不失真。</span><span class="sxs-lookup"><span data-stu-id="9ee02-106">The encoder supports three categories of encoded output: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="9ee02-107">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="9ee02-107">Class Identifier</span></span>

<span data-ttu-id="9ee02-108">Windows Media 音訊編碼器 (CLSID) 的類別識別碼是以常數 **CLSID \_ CWMAEncMediaObject** 來表示。</span><span class="sxs-lookup"><span data-stu-id="9ee02-108">The class identifier (CLSID) for the Windows Media Audio Encoder is represented by the constant **CLSID\_CWMAEncMediaObject**.</span></span> <span data-ttu-id="9ee02-109">您可以藉由呼叫 **CoCreateInstance** 來建立音訊編碼器的實例。</span><span class="sxs-lookup"><span data-stu-id="9ee02-109">You can create an instance of the audio encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="9ee02-110">輸入格式</span><span class="sxs-lookup"><span data-stu-id="9ee02-110">Input Formats</span></span>

<span data-ttu-id="9ee02-111">下表顯示的音訊格式標記代表 Windows Media 音訊編碼器所支援的輸入分類。</span><span class="sxs-lookup"><span data-stu-id="9ee02-111">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio encoder.</span></span> <span data-ttu-id="9ee02-112">如需有關如何設定編碼器之輸入和輸出類型的詳細資訊，請參閱設定 [音訊編碼](configuringaudioencoding.md)。</span><span class="sxs-lookup"><span data-stu-id="9ee02-112">For information about how to set the input and output types for the encoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="9ee02-113">格式化標記常數</span><span class="sxs-lookup"><span data-stu-id="9ee02-113">Format tag constant</span></span>       | <span data-ttu-id="9ee02-114">格式化標記值</span><span class="sxs-lookup"><span data-stu-id="9ee02-114">Format tag value</span></span> | <span data-ttu-id="9ee02-115">音訊格式</span><span class="sxs-lookup"><span data-stu-id="9ee02-115">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="9ee02-116">WAVE \_ 格式 \_ PCM</span><span class="sxs-lookup"><span data-stu-id="9ee02-116">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="9ee02-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="9ee02-117">0x0001</span></span>           | <span data-ttu-id="9ee02-118">PCM 格式</span><span class="sxs-lookup"><span data-stu-id="9ee02-118">PCM format</span></span>                                            |
| <span data-ttu-id="9ee02-119">WAVE \_ 格式 \_ IEEE \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="9ee02-119">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="9ee02-120">0x0003</span><span class="sxs-lookup"><span data-stu-id="9ee02-120">0x0003</span></span>           | <span data-ttu-id="9ee02-121">IEEE 浮點數</span><span class="sxs-lookup"><span data-stu-id="9ee02-121">IEEE floating point</span></span>                                   |
| <span data-ttu-id="9ee02-122">WAVE \_ 格式 \_ 可擴充</span><span class="sxs-lookup"><span data-stu-id="9ee02-122">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="9ee02-123">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="9ee02-123">0xFFFE</span></span>           | <span data-ttu-id="9ee02-124">**WAVEFORMATEXTENSIBLE** 結構中的 PCM/IEEE 格式</span><span class="sxs-lookup"><span data-stu-id="9ee02-124">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="9ee02-125">輸出格式</span><span class="sxs-lookup"><span data-stu-id="9ee02-125">Output Formats</span></span>

<span data-ttu-id="9ee02-126">下表顯示的音訊格式標記，代表 Windows Media 音訊編碼器支援的輸出分類。</span><span class="sxs-lookup"><span data-stu-id="9ee02-126">The following table shows the audio format tags that represent the output categories supported by the Windows Media Audio encoder.</span></span>



| <span data-ttu-id="9ee02-127">格式化標記常數</span><span class="sxs-lookup"><span data-stu-id="9ee02-127">Format tag constant</span></span>             | <span data-ttu-id="9ee02-128">格式化標記值</span><span class="sxs-lookup"><span data-stu-id="9ee02-128">Format tag value</span></span> | <span data-ttu-id="9ee02-129">音訊格式</span><span class="sxs-lookup"><span data-stu-id="9ee02-129">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="9ee02-130">WAVE \_ 格式 \_ WMAUDIO2</span><span class="sxs-lookup"><span data-stu-id="9ee02-130">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="9ee02-131">0x0161</span><span class="sxs-lookup"><span data-stu-id="9ee02-131">0x0161</span></span>           | <span data-ttu-id="9ee02-132">Windows Media 音訊標準</span><span class="sxs-lookup"><span data-stu-id="9ee02-132">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="9ee02-133">WAVE \_ 格式 \_ WMAUDIO3</span><span class="sxs-lookup"><span data-stu-id="9ee02-133">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="9ee02-134">0x0162</span><span class="sxs-lookup"><span data-stu-id="9ee02-134">0x0162</span></span>           | <span data-ttu-id="9ee02-135">Windows Media 音訊專業人員</span><span class="sxs-lookup"><span data-stu-id="9ee02-135">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="9ee02-136">WAVE \_ 格式 \_ WMAUDIO \_ 無損</span><span class="sxs-lookup"><span data-stu-id="9ee02-136">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="9ee02-137">0x0163</span><span class="sxs-lookup"><span data-stu-id="9ee02-137">0x0163</span></span>           | <span data-ttu-id="9ee02-138">Windows Media 音訊無損</span><span class="sxs-lookup"><span data-stu-id="9ee02-138">Windows Media Audio Lossless</span></span>     |



 

## <a name="interfaces"></a><span data-ttu-id="9ee02-139">介面</span><span class="sxs-lookup"><span data-stu-id="9ee02-139">Interfaces</span></span>

<span data-ttu-id="9ee02-140">音訊 endoder 物件會公開 **IMediaObject** 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 **IMFTransform** 介面，讓物件可以做為 (MFT) 媒體基礎轉換。</span><span class="sxs-lookup"><span data-stu-id="9ee02-140">An audio endoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="9ee02-141">Windows Media 音訊編碼器的運作方式，視您取得的介面和執行的 Windows 版本而定。</span><span class="sxs-lookup"><span data-stu-id="9ee02-141">A Windows Media Audio encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="9ee02-142">下表顯示音訊編碼器以 SQL-DMO 或 MFT 行為的條件。</span><span class="sxs-lookup"><span data-stu-id="9ee02-142">The following table shows the conditions under which an audio encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="9ee02-143">作業系統</span><span class="sxs-lookup"><span data-stu-id="9ee02-143">Operating system</span></span> | <span data-ttu-id="9ee02-144">編碼器行為</span><span class="sxs-lookup"><span data-stu-id="9ee02-144">Encoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee02-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9ee02-145">Windows XP</span></span>       | <span data-ttu-id="9ee02-146">Windows Media 音訊編碼器一律會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="9ee02-146">A Windows Media Audio encoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="9ee02-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ee02-147">Windows Vista</span></span>    | <span data-ttu-id="9ee02-148">Windows Media 音訊編碼器預設會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="9ee02-148">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="9ee02-149">如果您在音訊編碼器上取得 **IMFTransform** 介面或 **IPropertyStore** 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="9ee02-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio encoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="9ee02-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ee02-150">Windows 7</span></span>        | <span data-ttu-id="9ee02-151">Windows Media 音訊編碼器預設會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="9ee02-151">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="9ee02-152">如果您在音訊編碼器上取得 **IMFTransform** 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="9ee02-152">If you obtain an **IMFTransform** interface on an audio encoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="encoder-properties"></a><span data-ttu-id="9ee02-153">編碼器屬性</span><span class="sxs-lookup"><span data-stu-id="9ee02-153">Encoder Properties</span></span>

<span data-ttu-id="9ee02-154">Windows Media 音訊編碼器支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="9ee02-154">The Windows Media Audio encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9ee02-155">屬性</span><span class="sxs-lookup"><span data-stu-id="9ee02-155">Property</span></span></th>
<th><span data-ttu-id="9ee02-156">描述</span><span class="sxs-lookup"><span data-stu-id="9ee02-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ee02-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-158">指定編碼器是否使用平均可控的 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="9ee02-158">Specifies whether the encoder uses average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="9ee02-159">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-160">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-161">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-161">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-163">以毫秒為單位，指定限制可變位速率的緩衝區視窗（以毫秒為單位）， (VBR) 資料流程的尖峰位元速率。</span><span class="sxs-lookup"><span data-stu-id="9ee02-163">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate.</span></span><br/> <dl> <span data-ttu-id="9ee02-164">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-164">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-165">Standard、Professional。</span><span class="sxs-lookup"><span data-stu-id="9ee02-165">Standard, Professional.</span></span><br />
<span data-ttu-id="9ee02-166">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-166">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-168">指定在執行雙向 VBR 編碼時，編碼器是否應該檢查跨行程的資料一致性。</span><span class="sxs-lookup"><span data-stu-id="9ee02-168">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <br/> <dl> <span data-ttu-id="9ee02-169">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-169">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-170">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-170">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-171">唯讀。</span><span class="sxs-lookup"><span data-stu-id="9ee02-171">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-173">指定編碼器是否受限於最大的解碼器延遲需求。</span><span class="sxs-lookup"><span data-stu-id="9ee02-173">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span><br/> <dl> <span data-ttu-id="9ee02-174">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-174">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-175">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-175">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-176">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-176">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-178">指定是否限制編碼演算法的複雜度。</span><span class="sxs-lookup"><span data-stu-id="9ee02-178">Specifies whether the complexity of the encoding algorithm is constrained.</span></span><br/> <dl> <span data-ttu-id="9ee02-179">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-180">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-180">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-181">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-181">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-183">指定編碼器是否受限於最大延遲需求。</span><span class="sxs-lookup"><span data-stu-id="9ee02-183">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span><br/> <dl> <span data-ttu-id="9ee02-184">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-184">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-185">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-185">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-186">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-188">指定由編碼器列舉的模式是否限制為符合品質需求的模式。</span><span class="sxs-lookup"><span data-stu-id="9ee02-188">Specifies whether modes enumerated by the encoder are limited to those that meet a quality requirement.</span></span><br/> <dl> <span data-ttu-id="9ee02-189">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-189">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-190">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-190">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-191">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-193">指定編碼內容的複雜性設定檔。</span><span class="sxs-lookup"><span data-stu-id="9ee02-193">Specifies the complexity profile of the encoded content.</span></span><br/> <dl> <span data-ttu-id="9ee02-194">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-194">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-195">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-195">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-196">唯讀。</span><span class="sxs-lookup"><span data-stu-id="9ee02-196">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-198">指定 VBR 編碼所需的品質等級。</span><span class="sxs-lookup"><span data-stu-id="9ee02-198">Specifies the desired quality level for VBR encoding.</span></span><br/> <dl> <span data-ttu-id="9ee02-199">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-199">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-200">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-200">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-201">唯寫。</span><span class="sxs-lookup"><span data-stu-id="9ee02-201">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-203">指定編碼器是否使用雜訊替代。</span><span class="sxs-lookup"><span data-stu-id="9ee02-203">Specifies whether the encoder uses noise substitution.</span></span><br/> <dl> <span data-ttu-id="9ee02-204">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-205">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-205">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-206">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-206">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-208">指定編碼器是否使用 PCM 範圍限制。</span><span class="sxs-lookup"><span data-stu-id="9ee02-208">Specifies whether the encoder uses PCM range limiting.</span></span><br/> <dl> <span data-ttu-id="9ee02-209">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-209">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-210">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-210">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-211">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-211">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-213">指定編碼器中的帶狀截斷所允許的最大編碼頻寬。</span><span class="sxs-lookup"><span data-stu-id="9ee02-213">Specifies the maximum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="9ee02-214">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-214">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-215">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-215">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-216">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-216">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-218">指定編碼器中的頻外截斷所允許的最低編碼頻寬。</span><span class="sxs-lookup"><span data-stu-id="9ee02-218">Specifies the minimum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="9ee02-219">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-219">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-220">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-220">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-221">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-221">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-223">指定允許最小編碼頻寬的品質。</span><span class="sxs-lookup"><span data-stu-id="9ee02-223">Specifies the quality at which minimum coded bandwidth is allowed.</span></span> <br/> <dl> <span data-ttu-id="9ee02-224">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-224">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-225">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-225">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-226">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-226">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-228">指定允許最大編碼頻寬的品質。</span><span class="sxs-lookup"><span data-stu-id="9ee02-228">Specifies the quality at which maximum coded bandwidth is allowed.</span></span><br/> <dl> <span data-ttu-id="9ee02-229">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-229">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-230">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-230">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-231">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-231">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-233">指定編碼器是否執行帶狀截斷。</span><span class="sxs-lookup"><span data-stu-id="9ee02-233">Specifies whether the encoder performs band truncation.</span></span><br/> <dl> <span data-ttu-id="9ee02-234">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-234">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-235">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-235">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-236">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-236">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-238">指定編碼器是否使用 Windows Media 音訊編碼器第7版所執行之遮罩計算的樣式。</span><span class="sxs-lookup"><span data-stu-id="9ee02-238">Specifies whether the encoder uses the style of mask computation performed by version 7 of the Windows Media Audio encoder.</span></span><br/> <dl> <span data-ttu-id="9ee02-239">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-239">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-240">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-240">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-241">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-241">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-243">指定編碼器是否執行身歷聲影像處理。</span><span class="sxs-lookup"><span data-stu-id="9ee02-243">Specifies whether the encoder performs stereo image processing.</span></span> <br/> <dl> <span data-ttu-id="9ee02-244">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-244">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-245">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-245">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-246">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-246">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-248">以毫秒為單位，為設定為使用可進行平均控制之 VBR 編碼的編碼器指定緩衝區視窗（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ee02-248">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="9ee02-249">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-249">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-250">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-250">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-251">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-253">針對設定為使用可進行平均控制的 VBR 編碼的編碼器，指定平均位元速率（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ee02-253">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="9ee02-254">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-254">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-255">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-255">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-256">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-256">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-258">指定編碼演算法的複雜度。</span><span class="sxs-lookup"><span data-stu-id="9ee02-258">Specifies the complexity of the encoding algorithm.</span></span><br/> <dl> <span data-ttu-id="9ee02-259">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-260">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-260">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-261">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-261">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-263">指定編碼傳遞的結尾。</span><span class="sxs-lookup"><span data-stu-id="9ee02-263">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="9ee02-264">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-264">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-265">Standard、Professional。</span><span class="sxs-lookup"><span data-stu-id="9ee02-265">Standard, Professional.</span></span><br />
<span data-ttu-id="9ee02-266">唯寫。</span><span class="sxs-lookup"><span data-stu-id="9ee02-266">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-268">指定核心編碼器是否使用 &quot; Plus &quot; 功能。</span><span class="sxs-lookup"><span data-stu-id="9ee02-268">Specifies whether the core encoder uses the &quot;Plus&quot; feature.</span></span><br/> <dl> <span data-ttu-id="9ee02-269">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-269">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-270">Professional。</span><span class="sxs-lookup"><span data-stu-id="9ee02-270">Professional.</span></span><br />
<span data-ttu-id="9ee02-271">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-271">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-273">指定最大的解碼器延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ee02-273">Specifies the maximum latency for the decoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="9ee02-274">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-274">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-275">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-275">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-276">唯寫。</span><span class="sxs-lookup"><span data-stu-id="9ee02-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-278">指定編碼器的最大延遲（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ee02-278">Specifies the maximum latency for the encoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="9ee02-279">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-279">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-280">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-280">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-281">唯寫。</span><span class="sxs-lookup"><span data-stu-id="9ee02-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-283">指定最新列舉輸出類型的 VBR 品質層級。</span><span class="sxs-lookup"><span data-stu-id="9ee02-283">Specifies the VBR quality level of the most recently enumerated output type.</span></span><br/> <dl> <span data-ttu-id="9ee02-284">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-284">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-285">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-285">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-286">唯讀。</span><span class="sxs-lookup"><span data-stu-id="9ee02-286">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-288">指定編碼器所支援的最大傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="9ee02-288">Specifies the maximum number of passes supported by the encoder.</span></span><br/> <dl> <span data-ttu-id="9ee02-289">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-289">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-290">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-290">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-291">唯讀。</span><span class="sxs-lookup"><span data-stu-id="9ee02-291">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-293">指定編碼器將用來編碼內容的傳遞數。</span><span class="sxs-lookup"><span data-stu-id="9ee02-293">Specifies the number of passes that the encoder will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="9ee02-294">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-294">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-295">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-295">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-296">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-296">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-298">指定編碼器是否受尖峰位速率的限制。</span><span class="sxs-lookup"><span data-stu-id="9ee02-298">Specifies whether the encoder is constrained by a peak bit rate.</span></span><br/> <dl> <span data-ttu-id="9ee02-299">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-299">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-300">Standard、Professional。</span><span class="sxs-lookup"><span data-stu-id="9ee02-300">Standard, Professional.</span></span><br />
<span data-ttu-id="9ee02-301">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-301">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-303">指定每個框架慣用的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="9ee02-303">Specifies the preferred number of samples per frame.</span></span><br/> <dl> <span data-ttu-id="9ee02-304">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-304">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-305">Professional。</span><span class="sxs-lookup"><span data-stu-id="9ee02-305">Professional.</span></span><br />
<span data-ttu-id="9ee02-306">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-306">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-308">指定編碼器是否應使用慣用的框架大小。</span><span class="sxs-lookup"><span data-stu-id="9ee02-308">Specifies whether the encoder should use a preferred frame size.</span></span><br/> <dl> <span data-ttu-id="9ee02-309">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-309">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-310">Professional。</span><span class="sxs-lookup"><span data-stu-id="9ee02-310">Professional.</span></span><br />
<span data-ttu-id="9ee02-311">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-311">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-313">指定尖峰位速率（以每秒位數為單位），用於受條件約束的2傳遞變數位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="9ee02-313">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span> <br/> <dl> <span data-ttu-id="9ee02-314">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-314">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-315">Standard、Professional。</span><span class="sxs-lookup"><span data-stu-id="9ee02-315">Standard, Professional.</span></span><br />
<span data-ttu-id="9ee02-316">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-316">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-318">指定編碼資料流程的平均緩衝區視窗（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ee02-318">Specifies the average buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="9ee02-319">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-319">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-320">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-320">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-321">唯讀。</span><span class="sxs-lookup"><span data-stu-id="9ee02-321">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-323">指定編碼資料流程的最大緩衝區視窗（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ee02-323">Specifies the maximum buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="9ee02-324">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-324">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-325">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-325">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-326">唯讀。</span><span class="sxs-lookup"><span data-stu-id="9ee02-326">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-328">指定編碼資料流程的平均位元速率（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ee02-328">Specifies the average bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="9ee02-329">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-329">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-330">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-330">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-331">唯讀。</span><span class="sxs-lookup"><span data-stu-id="9ee02-331">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-333">指定編碼資料流程的最大位元速率（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ee02-333">Specifies the maximum bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="9ee02-334">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-334">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-335">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-335">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-336">唯讀。</span><span class="sxs-lookup"><span data-stu-id="9ee02-336">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-338">指定編碼器是否使用 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="9ee02-338">Specifies whether the encoder uses VBR encoding.</span></span><br/> <dl> <span data-ttu-id="9ee02-339">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-339">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-340">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-340">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-341">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-341">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-343">Windows Media 音訊編解碼器目前未使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="9ee02-343">This property is currently not used by the Windows Media Audio codec.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-345">指定音訊內容的平均音量層級。</span><span class="sxs-lookup"><span data-stu-id="9ee02-345">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="9ee02-346">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-346">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-347">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-347">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-348">唯讀。</span><span class="sxs-lookup"><span data-stu-id="9ee02-348">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-350">指定音訊內容中發生的最高音量層級。</span><span class="sxs-lookup"><span data-stu-id="9ee02-350">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="9ee02-351">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-351">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-352">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-352">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-353">唯讀。</span><span class="sxs-lookup"><span data-stu-id="9ee02-353">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-355">指定 VBR 編碼音訊的每秒平均位元組數。</span><span class="sxs-lookup"><span data-stu-id="9ee02-355">Specifies the average bytes per second for VBR encoded audio.</span></span><br/> <dl> <span data-ttu-id="9ee02-356">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-356">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-357">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-357">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-358">唯讀。</span><span class="sxs-lookup"><span data-stu-id="9ee02-358">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-360">指定編碼器是否應該為每個畫面產生1個 WMA 封包。</span><span class="sxs-lookup"><span data-stu-id="9ee02-360">Specifies whether the encoder should produce 1 WMA packet per frame.</span></span><br/> <dl> <span data-ttu-id="9ee02-361">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-361">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-362">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-362">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-363">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-363">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-365">指定編碼器是否應產生動態範圍控制參數。</span><span class="sxs-lookup"><span data-stu-id="9ee02-365">Specifies whether the encoder should generate dynamic range control parameters.</span></span><br/> <dl> <span data-ttu-id="9ee02-366">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-366">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-367">Standard、Professional、無損。</span><span class="sxs-lookup"><span data-stu-id="9ee02-367">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="9ee02-368">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-368">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ee02-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-370">指定描述輸入音訊內容的 <strong>WAVEFORMATEX</strong> 結構。</span><span class="sxs-lookup"><span data-stu-id="9ee02-370">Specifies the <strong>WAVEFORMATEX</strong> structure describing the input audio content.</span></span><br/> <dl> <span data-ttu-id="9ee02-371">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-371">Windows XP and later.</span></span><br />
<span data-ttu-id="9ee02-372">Standard、Professional。</span><span class="sxs-lookup"><span data-stu-id="9ee02-372">Standard, Professional.</span></span><br />
<span data-ttu-id="9ee02-373">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-373">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ee02-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span><span class="sxs-lookup"><span data-stu-id="9ee02-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span></span></td>
<td><span data-ttu-id="9ee02-375">指定編碼器是否應啟用即時 S/PDIF 編碼。</span><span class="sxs-lookup"><span data-stu-id="9ee02-375">Specifies whether the encoder should enable real-time S/PDIF encoding .</span></span><br/> <dl> <span data-ttu-id="9ee02-376">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="9ee02-376">Windows Vista and later.</span></span><br />
<span data-ttu-id="9ee02-377">Professional。</span><span class="sxs-lookup"><span data-stu-id="9ee02-377">Professional.</span></span><br />
<span data-ttu-id="9ee02-378">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9ee02-378">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="9ee02-379">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ee02-379">Requirements</span></span>



| <span data-ttu-id="9ee02-380">需求</span><span class="sxs-lookup"><span data-stu-id="9ee02-380">Requirement</span></span> | <span data-ttu-id="9ee02-381">值</span><span class="sxs-lookup"><span data-stu-id="9ee02-381">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee02-382">用戶端</span><span class="sxs-lookup"><span data-stu-id="9ee02-382">Client</span></span><br/> | <span data-ttu-id="9ee02-383">Windows XP、Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="9ee02-383">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="9ee02-384">標頭</span><span class="sxs-lookup"><span data-stu-id="9ee02-384">Header</span></span><br/> | <dl> <span data-ttu-id="9ee02-385"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9ee02-385"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="9ee02-386">DLL</span><span class="sxs-lookup"><span data-stu-id="9ee02-386">DLL</span></span><br/>    | <dl> <span data-ttu-id="9ee02-387"><dt>Wmadmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ee02-387"><dt>Wmadmoe.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9ee02-388">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ee02-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ee02-389">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="9ee02-389">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="9ee02-390">編解碼器實行</span><span class="sxs-lookup"><span data-stu-id="9ee02-390">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




