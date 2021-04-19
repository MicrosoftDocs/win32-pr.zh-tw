---
description: 此篩選器會解碼下列音訊格式：
ms.assetid: 2fd14296-9eed-4e25-b140-6281c707fdb7
title: 'Microsoft MPEG-1/DD/AAC 音訊解碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a685fa2be32dd963cdc7de08ec716117e6a7016e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106967008"
---
# <a name="microsoft-mpeg-1ddaac-audio-decoder"></a><span data-ttu-id="e1a9c-103">Microsoft MPEG-1/DD/AAC 音訊解碼器</span><span class="sxs-lookup"><span data-stu-id="e1a9c-103">Microsoft MPEG-1/DD/AAC Audio Decoder</span></span>

<span data-ttu-id="e1a9c-104">此篩選器會解碼下列音訊格式：</span><span class="sxs-lookup"><span data-stu-id="e1a9c-104">This filter decodes the following audio formats:</span></span>

-   <span data-ttu-id="e1a9c-105">MPEG-2 音訊層 I 和 II。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-105">MPEG-1 audio layers I and II.</span></span>
-   <span data-ttu-id="e1a9c-106">與舊版相容的 MPEG-2 音訊、圖層 I 和 II (ISO/IEC 13818-3) 、mono 和身歷聲。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-106">Backward-compatible MPEG-2 audio, layers I and II (ISO/IEC 13818-3), mono and stereo only.</span></span>
-   <span data-ttu-id="e1a9c-107">Advanced Audio 編碼 (AAC) 低複雜度 (LC) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-107">Advanced Audio Coding (AAC) Low Complexity (LC) profile.</span></span>
-   <span data-ttu-id="e1a9c-108">High-Efficiency AAC (AAC) 第1版和第2版。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-108">High-Efficiency AAC (HE-AAC) version 1 and version 2.</span></span>
-   <span data-ttu-id="e1a9c-109">傳遞數位劇院系統 (DTS) 的數位輸出。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-109">Pass-through Digital Theater Systems (DTS) for digital output.</span></span>
-   <span data-ttu-id="e1a9c-110">LPCM、mono 和身歷聲（含或不含 PE 標頭）。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-110">LPCM, mono and stereo only, with or without PES headers.</span></span>
-   <span data-ttu-id="e1a9c-111">杜比數位。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-111">Dolby Digital.</span></span>
-   <span data-ttu-id="e1a9c-112">杜比數位 Plus，包括從杜比數位的轉換到數位輸出的杜數位。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-112">Dolby Digital Plus, including conversion from Dolby Digital Plus to Dolby Digital for digital output.</span></span>

> [!Note]  
> <span data-ttu-id="e1a9c-113">Microsoft 應用程式使用的杜比數位授權方案，會限制 Microsoft 的杜比數位技術。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-113">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

> [!Note]  
> <span data-ttu-id="e1a9c-114">以 IA-64 為基礎的平臺不支援此篩選器。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-114">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="e1a9c-115">將杜比數位加號、AAC 和 AAC 格式解碼需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-115">Decoding of Dolby Digital Plus, AAC, and HE-AAC formats requires Windows 7.</span></span> <span data-ttu-id="e1a9c-116">Windows 7 Home Basic 或 Windows 7 Starter 版不支援對杜比數位或杜比數位加號進行解碼。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-116">Decoding of Dolby Digital or Dolby Digital Plus is not supported on Windows 7 Home Basic or Windows 7 Starter.</span></span>

<span data-ttu-id="e1a9c-117">在登錄中，此篩選器的易記名稱是「Microsoft DTV DVD-音訊解碼」。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-117">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Audio Decoder".</span></span>



<span data-ttu-id="e1a9c-118">篩選資訊</span><span class="sxs-lookup"><span data-stu-id="e1a9c-118">Filter Information</span></span>

<span data-ttu-id="e1a9c-119">篩選介面</span><span class="sxs-lookup"><span data-stu-id="e1a9c-119">Filter Interfaces</span></span>

[<span data-ttu-id="e1a9c-120">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-120">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="e1a9c-121">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-121">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="e1a9c-122">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="e1a9c-122">Input Pin Media Types</span></span>

<span data-ttu-id="e1a9c-123">在 Windows Vista 和更新版本中，篩選準則支援下列輸入類型：</span><span class="sxs-lookup"><span data-stu-id="e1a9c-123">In Windows Vista and later, the filter supports the following input types:</span></span><br/>

-   <span data-ttu-id="e1a9c-124">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ 杜比 \_ AC3** (請參閱附注1。 ) </span><span class="sxs-lookup"><span data-stu-id="e1a9c-124">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="e1a9c-125">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-125">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="e1a9c-126">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG1Payload**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-126">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1Payload**</span></span>
-   <span data-ttu-id="e1a9c-127">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-127">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="e1a9c-128">**媒體媒體 \_DVD \_ 加密 \_ 套件**， **MEDIASUBTYPE \_ 杜比 \_ AC3** (參閱附注1。 ) </span><span class="sxs-lookup"><span data-stu-id="e1a9c-128">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="e1a9c-129">**媒體媒體 \_DVD \_ 加密 \_ 套件**， **MEDIASUBTYPE \_ DTS** (請參閱附注 2. ) </span><span class="sxs-lookup"><span data-stu-id="e1a9c-129">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="e1a9c-130">**媒體媒體 \_DVD \_ 加密 \_ 套件**、 **MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-130">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="e1a9c-131">**媒體媒體 \_DVD \_ 加密 \_ 套件**， **MEDIASUBTYPE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-131">**MEDIATYPE\_DVD\_ENCRYPTED\_PACK**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="e1a9c-132">**媒體媒體 \_MPEG2 \_ pe**、 **MEDIASUBTYPE \_ 杜比 \_ AC3** (請參閱附注1。 ) </span><span class="sxs-lookup"><span data-stu-id="e1a9c-132">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="e1a9c-133">**媒體媒體 \_MPEG2 \_ pe**、 **MEDIASUBTYPE \_ DTS** (請參閱附注 2. ) </span><span class="sxs-lookup"><span data-stu-id="e1a9c-133">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DTS** (See Note 2.)</span></span>
-   <span data-ttu-id="e1a9c-134">**媒體媒體 \_MPEG2 \_ pe**、 **MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-134">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="e1a9c-135">**媒體媒體 \_MPEG2 \_ pe**、 **MEDIASUBTYPE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-135">**MEDIATYPE\_MPEG2\_PES**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>
-   <span data-ttu-id="e1a9c-136">**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ 杜比 \_ AC3** (請參閱附注1。 ) </span><span class="sxs-lookup"><span data-stu-id="e1a9c-136">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_AC3** (See Note 1.)</span></span>
-   <span data-ttu-id="e1a9c-137">**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG1Audio**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-137">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG1Audio**</span></span>
-   <span data-ttu-id="e1a9c-138">**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-138">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>

<span data-ttu-id="e1a9c-139">從 Windows 7 開始，篩選準則也支援下列輸入類型：</span><span class="sxs-lookup"><span data-stu-id="e1a9c-139">Starting in Windows 7, the filter also supports the following input types:</span></span><br/>

-   <span data-ttu-id="e1a9c-140">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ 杜比 \_ DDPLUS** (請參閱附注1。 ) </span><span class="sxs-lookup"><span data-stu-id="e1a9c-140">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="e1a9c-141">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ DTS2** (請參閱附注 2. ) </span><span class="sxs-lookup"><span data-stu-id="e1a9c-141">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DTS2** (See Note 2.)</span></span>
-   <span data-ttu-id="e1a9c-142">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ DVD \_ LPCM \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-142">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVD\_LPCM\_AUDIO**</span></span>
-   <span data-ttu-id="e1a9c-143">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ DVM** (請參閱附注1。 ) </span><span class="sxs-lookup"><span data-stu-id="e1a9c-143">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DVM** (See Note 1.)</span></span>
-   <span data-ttu-id="e1a9c-144">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-144">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="e1a9c-145">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG \_ loa**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-145">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>
-   <span data-ttu-id="e1a9c-146">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG1AudioPayload**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-146">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG1AudioPayload**</span></span>
-   <span data-ttu-id="e1a9c-147">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ 原始 \_ AAC1**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-147">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_RAW\_AAC1**</span></span>
-   <span data-ttu-id="e1a9c-148">**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ 杜比 \_ DDPLUS** (請參閱附注1。 ) </span><span class="sxs-lookup"><span data-stu-id="e1a9c-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_DOLBY\_DDPLUS** (See Note 1.)</span></span>
-   <span data-ttu-id="e1a9c-149">**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-149">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_ADTS\_AAC**</span></span>
-   <span data-ttu-id="e1a9c-150">**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG \_ loa**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-150">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG\_LOAS**</span></span>

<span data-ttu-id="e1a9c-151">輸入類型在串流處理期間可能會動態變更。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-151">The input type can change dynamically during streaming.</span></span><br/> <span data-ttu-id="e1a9c-152">如需這些媒體類型的詳細資訊，請參閱 [**音訊子類型**](audio-subtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-152">For more information about these media types, see [**Audio Subtypes**](audio-subtypes.md).</span></span><br/>

> [!Note]  
> 1. <span data-ttu-id="e1a9c-153">Microsoft 應用程式使用的杜比數位授權方案，會限制 Microsoft 的杜比數位技術。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-153">The Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

<br/>

> [!Note]  
> 2. <span data-ttu-id="e1a9c-154">針對數位劇院系統 (DTS) 輸入， (DTS over S/PDIF) 只支援 S/PDIF 輸出。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-154">For Digital Theater Systems (DTS) input, only S/PDIF output is supported (DTS over S/PDIF).</span></span> <span data-ttu-id="e1a9c-155">不支援音訊解碼。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-155">Audio decoding is not supported.</span></span>

<br/>

<span data-ttu-id="e1a9c-156">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="e1a9c-156">Input Pin Interfaces</span></span>

[<span data-ttu-id="e1a9c-157">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-157">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="e1a9c-158">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-158">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="e1a9c-159">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-159">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="e1a9c-160">**IPin**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-160">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="e1a9c-161">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-161">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="e1a9c-162">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="e1a9c-162">Output Pin Media Types</span></span>

<span data-ttu-id="e1a9c-163">在 Windows Vista 和更新版本中，篩選準則支援下列輸出類型：</span><span class="sxs-lookup"><span data-stu-id="e1a9c-163">In Windows Vista and later, the filter supports the following output types:</span></span><br/>

-   <span data-ttu-id="e1a9c-164">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ 杜比 \_ AC3 \_ SPDIF** (與 **KSDATAFORMAT \_ 子類型相同 \_ IEC61937 \_ 杜比 \_ 數位**) </span><span class="sxs-lookup"><span data-stu-id="e1a9c-164">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_DOLBY\_AC3\_SPDIF** (same as **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL**)</span></span>
-   <span data-ttu-id="e1a9c-165">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-165">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="e1a9c-166">從 Windows 7 開始，篩選準則也支援下列輸出類型：</span><span class="sxs-lookup"><span data-stu-id="e1a9c-166">Starting in Windows 7, the filter also supports the following output types:</span></span><br/>

-   <span data-ttu-id="e1a9c-167">**媒體媒體 \_音訊**、 **KSDATAFORMAT \_ 子類型 \_ IEC61937 \_ DTS**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-167">**MEDIATYPE\_Audio**, **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS**</span></span>
-   <span data-ttu-id="e1a9c-168">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ IEEE \_ FLOAT**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-168">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_IEEE\_FLOAT**</span></span>

<span data-ttu-id="e1a9c-169">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="e1a9c-169">Output Pin Interfaces</span></span>

[<span data-ttu-id="e1a9c-170">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-170">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="e1a9c-171">**IPin**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-171">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="e1a9c-172">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-172">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="e1a9c-173">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="e1a9c-173">Filter CLSID</span></span>

<span data-ttu-id="e1a9c-174">**CLSID \_** 在 wmcodecdsp 中宣告的 CMPEG2AudDecoderDS () </span><span class="sxs-lookup"><span data-stu-id="e1a9c-174">**CLSID\_CMPEG2AudDecoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="e1a9c-175">可執行檔</span><span class="sxs-lookup"><span data-stu-id="e1a9c-175">Executable</span></span>

<span data-ttu-id="e1a9c-176">msmpeg2adec.dll</span><span class="sxs-lookup"><span data-stu-id="e1a9c-176">msmpeg2adec.dll</span></span>

[<span data-ttu-id="e1a9c-177">優點</span><span class="sxs-lookup"><span data-stu-id="e1a9c-177">Merit</span></span>](merit.md)

<span data-ttu-id="e1a9c-178">**業績 \_正常** -1</span><span class="sxs-lookup"><span data-stu-id="e1a9c-178">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="e1a9c-179">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="e1a9c-179">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="e1a9c-180">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-180">**CLSID\_LegacyAmFilterCategory**</span></span>



 

> [!Note]  
> <span data-ttu-id="e1a9c-181">舊版的檔規定此篩選器可以解碼「MPEG-2 音訊」。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-181">An earlier version of the documentation stated that this filter can decode "MPEG-2 audio."</span></span> <span data-ttu-id="e1a9c-182">篩選只會將後端相容的 MPEG-2 音訊解碼。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-182">The filter decodes only backward-compatible MPEG-2 audio.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="e1a9c-183">備註</span><span class="sxs-lookup"><span data-stu-id="e1a9c-183">Remarks</span></span>

<span data-ttu-id="e1a9c-184">Mono 資料流程一律會解碼為身歷聲。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-184">Mono streams are always decoded to stereo.</span></span>

<span data-ttu-id="e1a9c-185">針對通道設定為兩個以上的喇叭的串流，此解碼器會執行下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="e1a9c-185">For streams with a channel configuration of two or more speakers, the decoder does one of the following:</span></span>

-   <span data-ttu-id="e1a9c-186">使用常見的5.1 喇叭設定，向上混合到六個通道。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-186">Up-mixes to six channels, using the common 5.1 speaker configuration.</span></span>
-   <span data-ttu-id="e1a9c-187">Downmixes 至身歷聲。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-187">Downmixes to stereo.</span></span>

<span data-ttu-id="e1a9c-188">若要在這兩個選項之間做選擇，請先使用 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) 介面設定 [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) 屬性，再連接釘選。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-188">To select between these two options, use the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to set the [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property, before connecting the pins.</span></span> <span data-ttu-id="e1a9c-189">或者，當應用程式建立篩選圖形時，它可以在輸出釘選上設定所需的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-189">Alternatively, when the application builds the filter graph, it can set the desired media type on the output pin.</span></span>

### <a name="aac-decoding"></a><span data-ttu-id="e1a9c-190">AAC 解碼</span><span class="sxs-lookup"><span data-stu-id="e1a9c-190">AAC Decoding</span></span>

<span data-ttu-id="e1a9c-191">針對 AAC，此解碼器在壓縮的 AAC 輸入上有特定的格式條件約束。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-191">For AAC, the decoder has certain format constraints on the compressed AAC input.</span></span> <span data-ttu-id="e1a9c-192">這些格式條件約束與媒體基礎 [**AAC 解碼器**](../medfound/aac-decoder.md)相同，並記載于 "[**format 條件約束**](../medfound/aac-decoder.md)" 一節中。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-192">These format constraints are the same as the Media Foundation [**AAC Decoder**](../medfound/aac-decoder.md), and are documented in the section "[**Format Constraints**](../medfound/aac-decoder.md)".</span></span>

<span data-ttu-id="e1a9c-193">DirectShow 解碼器也可接受與媒體基礎解碼器不同的輸入類型。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-193">The DirectShow decoder also accepts different input types than the Media Foundation decoder.</span></span> <span data-ttu-id="e1a9c-194">DirectShow 解碼器支援下列 AAC 輸入類型：</span><span class="sxs-lookup"><span data-stu-id="e1a9c-194">The DirectShow decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="e1a9c-195">**MEDIASUBTYPE \_RAW \_ AAC1**：原始 AAC，通常會在 AVI 或 Matroska ( 中找到。.MKV) 檔。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-195">**MEDIASUBTYPE\_RAW\_AAC1**: Raw AAC, typically found in AVI or Matroska (.MKV) files.</span></span>
-   <span data-ttu-id="e1a9c-196">**MEDIASUBTYPE \_MPEG \_ ADTS \_ AAC**：音訊資料傳輸串流中的 AAC (ADTS) 進行串流處理。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-196">**MEDIASUBTYPE\_MPEG\_ADTS\_AAC**: AAC in an Audio Data Transport Stream (ADTS) for streaming.</span></span>
-   <span data-ttu-id="e1a9c-197">**MEDIASUBTYPE \_MPEG \_ loa**：具有同步處理層 (loa) 和多工層 (LATM) 的傳輸資料流程。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-197">**MEDIASUBTYPE\_MPEG\_LOAS**: Transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span>

<span data-ttu-id="e1a9c-198">媒體基礎的解碼器支援下列 AAC 輸入類型：</span><span class="sxs-lookup"><span data-stu-id="e1a9c-198">The Media Foundation decoder supports the following AAC input types:</span></span>

-   <span data-ttu-id="e1a9c-199">MFAudioFormat \_ AAC (與 **MEDIASUBTYPE \_ MPEG \_ HEAAC**) 相同，可進行檔播放。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-199">MFAudioFormat\_AAC (same as **MEDIASUBTYPE\_MPEG\_HEAAC**) for MP4 file playback.</span></span>
-   <span data-ttu-id="e1a9c-200">**MEDIASUBTYPE \_原始 \_ AAC1**。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-200">**MEDIASUBTYPE\_RAW\_AAC1**.</span></span>

### <a name="property-sets"></a><span data-ttu-id="e1a9c-201">屬性集</span><span class="sxs-lookup"><span data-stu-id="e1a9c-201">Property Sets</span></span>

<span data-ttu-id="e1a9c-202">此解碼器的輸入 pin 支援下列透過 [**IKsPropertySet**](ikspropertyset.md)的屬性集：</span><span class="sxs-lookup"><span data-stu-id="e1a9c-202">The decoder's input pin supports the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="e1a9c-203">**DVD 禁止複製屬性集**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-203">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="e1a9c-204">[**速率-變更屬性集**](rate-change-property-set.md)。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-204">[**Rate-Change Property Set**](rate-change-property-set.md).</span></span>

> [!Note]  
> <span data-ttu-id="e1a9c-205">從 Windows 7 開始，解碼器會透過速率變更屬性集支援訣竅模式。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-205">Starting in Windows 7, the decoder supports trick mode through the rate-change property set.</span></span> <span data-ttu-id="e1a9c-206">它支援範圍 \[ 0.501 –2.0 的播放率 \] ，其中1.0 是正常播放速率，而2.0 是一般速率的兩倍。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-206">It supports playback rates in the range \[0.501 – 2.0\], where 1.0 is normal playback rate, and 2.0 is twice the normal rate.</span></span>

 

### <a name="codec-properties"></a><span data-ttu-id="e1a9c-207">編解碼器屬性</span><span class="sxs-lookup"><span data-stu-id="e1a9c-207">Codec Properties</span></span>

<span data-ttu-id="e1a9c-208">此解碼器的輸入 pin 透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="e1a9c-208">The decoder's input pin supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="e1a9c-209">屬性</span><span class="sxs-lookup"><span data-stu-id="e1a9c-209">Property</span></span>                                                          | <span data-ttu-id="e1a9c-210">需要</span><span class="sxs-lookup"><span data-stu-id="e1a9c-210">Requires</span></span>                                                 |
|-------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="e1a9c-211">**AVAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-211">**AVAudioChannelConfig**</span></span>](avaudiochannelconfig-property.md)     | <span data-ttu-id="e1a9c-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1a9c-212">Windows Vista</span></span>                                            |
| [<span data-ttu-id="e1a9c-213">**AVAudioChannelCount**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-213">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)       | <span data-ttu-id="e1a9c-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1a9c-214">Windows Vista</span></span>                                            |
| [<span data-ttu-id="e1a9c-215">**AVAudioSampleRate**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-215">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)           | <span data-ttu-id="e1a9c-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1a9c-216">Windows Vista</span></span>                                            |
| [<span data-ttu-id="e1a9c-217">**AVDDSurroundMode**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-217">**AVDDSurroundMode**</span></span>](avddsurroundmode-property.md)             | <span data-ttu-id="e1a9c-218">僅限 Windows Vista;在 Windows 7 或更新版本中不支援。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-218">Windows Vista only; not supported in Windows 7 or later.</span></span> |
| [<span data-ttu-id="e1a9c-219">**AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-219">**AVDecAudioDualMono**</span></span>](avdecaudiodualmono-property.md)         | <span data-ttu-id="e1a9c-220">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1a9c-220">Windows Vista</span></span>                                            |
| [<span data-ttu-id="e1a9c-221">**AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md) | <span data-ttu-id="e1a9c-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1a9c-222">Windows Vista</span></span>                                            |
| [<span data-ttu-id="e1a9c-223">**AVDecCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-223">**AVDecCommonMeanBitRate**</span></span>](avdeccommonmeanbitrate.md)          | <span data-ttu-id="e1a9c-224">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1a9c-224">Windows 7</span></span>                                                |



 

<span data-ttu-id="e1a9c-225">篩選準則透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="e1a9c-225">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="e1a9c-226">屬性</span><span class="sxs-lookup"><span data-stu-id="e1a9c-226">Property</span></span>                                                                          | <span data-ttu-id="e1a9c-227">需要</span><span class="sxs-lookup"><span data-stu-id="e1a9c-227">Requires</span></span>      |
|-----------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="e1a9c-228">**AVDecAACDownmixMode**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-228">**AVDecAACDownmixMode**</span></span>](avdecaacdownmixmode-property.md)                       | <span data-ttu-id="e1a9c-229">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1a9c-229">Windows 7</span></span>     |
| [<span data-ttu-id="e1a9c-230">**AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-230">**AVDecAudioDualMonoReproMode**</span></span>](avdecaudiodualmonorepromode-property.md)       | <span data-ttu-id="e1a9c-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1a9c-231">Windows Vista</span></span> |
| <span data-ttu-id="e1a9c-232">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (參閱附注 3. ) </span><span class="sxs-lookup"><span data-stu-id="e1a9c-232">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) (See Note 3.)</span></span> | <span data-ttu-id="e1a9c-233">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1a9c-233">Windows Vista</span></span> |
| [<span data-ttu-id="e1a9c-234">**AVDecDDDynamicRangeScaleHigh**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-234">**AVDecDDDynamicRangeScaleHigh**</span></span>](avdecdddynamicrangescalehigh-property.md)     | <span data-ttu-id="e1a9c-235">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1a9c-235">Windows Vista</span></span> |
| [<span data-ttu-id="e1a9c-236">**AVDecDDDynamicRangeScaleLow**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-236">**AVDecDDDynamicRangeScaleLow**</span></span>](avdecdddynamicrangescalelow-property.md)       | <span data-ttu-id="e1a9c-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1a9c-237">Windows Vista</span></span> |
| [<span data-ttu-id="e1a9c-238">**AVDecDDOperationalMode**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-238">**AVDecDDOperationalMode**</span></span>](avdecddoperationalmode-property.md)                 | <span data-ttu-id="e1a9c-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1a9c-239">Windows Vista</span></span> |
| [<span data-ttu-id="e1a9c-240">**AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-240">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                    | <span data-ttu-id="e1a9c-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1a9c-241">Windows Vista</span></span> |
| [<span data-ttu-id="e1a9c-242">**AVDSPLoudnessEqualization**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-242">**AVDSPLoudnessEqualization**</span></span>](avdsploudnessequalization-property.md)           | <span data-ttu-id="e1a9c-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1a9c-243">Windows 7</span></span>     |
| [<span data-ttu-id="e1a9c-244">**AVDSPSpeakerFill**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-244">**AVDSPSpeakerFill**</span></span>](avdspspeakerfill-property.md)                             | <span data-ttu-id="e1a9c-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1a9c-245">Windows 7</span></span>     |



 

> [!Note]  
> 3. <span data-ttu-id="e1a9c-246">[**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md)屬性必須在已連接解碼器的輸出圖釘之前設定。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-246">The [**AVDecCommonOutputFormat**](avdeccommonoutputformat-property.md) property must be set before the decoder's output pin is connected.</span></span> <span data-ttu-id="e1a9c-247">否則，變更不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="e1a9c-247">Otherwise, the change has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e1a9c-248">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1a9c-248">Requirements</span></span>



| <span data-ttu-id="e1a9c-249">需求</span><span class="sxs-lookup"><span data-stu-id="e1a9c-249">Requirement</span></span> | <span data-ttu-id="e1a9c-250">值</span><span class="sxs-lookup"><span data-stu-id="e1a9c-250">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1a9c-251">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1a9c-251">Minimum supported client</span></span><br/> | <span data-ttu-id="e1a9c-252">Windows Vista Home Premium、Windows Vista 旗艦版、Windows 7 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1a9c-252">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e1a9c-253">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1a9c-253">Minimum supported server</span></span><br/> | <span data-ttu-id="e1a9c-254">都不支援</span><span class="sxs-lookup"><span data-stu-id="e1a9c-254">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e1a9c-255">標頭</span><span class="sxs-lookup"><span data-stu-id="e1a9c-255">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1a9c-256"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1a9c-256"><dt>Wmcodecdsp.h</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="e1a9c-257">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1a9c-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1a9c-258">**音訊子類型**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-258">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="e1a9c-259">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="e1a9c-259">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="e1a9c-260">**DVD 媒體類型**</span><span class="sxs-lookup"><span data-stu-id="e1a9c-260">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> </dl>

 

 
