---
description: Microsoft MPEG-2 音訊編碼器篩選器會將 MPEG-2 音訊層編碼為 I 和 II，包括支援 MPEG-2 低取樣頻率 (LSF) 擴充功能。
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: 'Microsoft MPEG-2 音訊編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d055acd379d9e966f43eac284e38a10c05a86c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971283"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a><span data-ttu-id="72f1e-103">Microsoft MPEG-2 音訊編碼器</span><span class="sxs-lookup"><span data-stu-id="72f1e-103">Microsoft MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="72f1e-104">Microsoft MPEG-2 音訊編碼器篩選器會將 MPEG-2 音訊層編碼為 I 和 II，包括支援 MPEG-2 低取樣頻率 (LSF) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="72f1e-104">The Microsoft MPEG-2 Audio Encoder filter encodes MPEG-1 audio layers I and II, including support for the MPEG-2 Low Sampling Frequency (LSF) extensions.</span></span>

<span data-ttu-id="72f1e-105">若要對音訊/影片串流進行編碼和多工處理，請使用 [**MICROSOFT Mpeg-2 編碼器**](microsoft-mpeg-2-encoder.md) 篩選器，它會封裝此篩選器和 [**Microsoft mpeg-2 影片編碼器**](microsoft-mpeg-2-video-encoder.md) 篩選器的功能。</span><span class="sxs-lookup"><span data-stu-id="72f1e-105">To encode and multiplex audio/video streams, use the [**Microsoft MPEG-2 Encoder**](microsoft-mpeg-2-encoder.md) filter, which encapsulates the functions of both this filter and the [**Microsoft MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="72f1e-106">以 IA-64 為基礎的平臺不支援此篩選器。</span><span class="sxs-lookup"><span data-stu-id="72f1e-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="72f1e-107">篩選資訊</span><span class="sxs-lookup"><span data-stu-id="72f1e-107">Filter Information</span></span>

<span data-ttu-id="72f1e-108">篩選介面</span><span class="sxs-lookup"><span data-stu-id="72f1e-108">Filter Interfaces</span></span>

[<span data-ttu-id="72f1e-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="72f1e-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="72f1e-110">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="72f1e-110">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="72f1e-111">**IEncoderAPI**</span><span class="sxs-lookup"><span data-stu-id="72f1e-111">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="72f1e-112">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="72f1e-112">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="72f1e-113">**IVideoEncoder**</span><span class="sxs-lookup"><span data-stu-id="72f1e-113">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="72f1e-114">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="72f1e-114">Input Pin Media Types</span></span>

<span data-ttu-id="72f1e-115">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="72f1e-115">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="72f1e-116">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="72f1e-116">Input Pin Interfaces</span></span>

[<span data-ttu-id="72f1e-117">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="72f1e-117">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="72f1e-118">**IPin**</span><span class="sxs-lookup"><span data-stu-id="72f1e-118">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="72f1e-119">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="72f1e-119">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="72f1e-120">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="72f1e-120">Output Pin Media Types</span></span>

<span data-ttu-id="72f1e-121">**媒體媒體 \_音訊**、 **MEDIASUBTYPE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="72f1e-121">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="72f1e-122">**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ 音訊**</span><span class="sxs-lookup"><span data-stu-id="72f1e-122">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="72f1e-123">**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ 方案**</span><span class="sxs-lookup"><span data-stu-id="72f1e-123">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span><br/> <span data-ttu-id="72f1e-124">**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**</span><span class="sxs-lookup"><span data-stu-id="72f1e-124">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span><br/>

<span data-ttu-id="72f1e-125">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="72f1e-125">Output Pin Interfaces</span></span>

[<span data-ttu-id="72f1e-126">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="72f1e-126">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="72f1e-127">**IPin**</span><span class="sxs-lookup"><span data-stu-id="72f1e-127">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="72f1e-128">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="72f1e-128">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="72f1e-129">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="72f1e-129">Filter CLSID</span></span>

<span data-ttu-id="72f1e-130">**CLSID \_** 在 wmcodecdsp 中宣告的 CMPEG2EncoderAudioDS () </span><span class="sxs-lookup"><span data-stu-id="72f1e-130">**CLSID\_CMPEG2EncoderAudioDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="72f1e-131">可執行檔</span><span class="sxs-lookup"><span data-stu-id="72f1e-131">Executable</span></span>

<span data-ttu-id="72f1e-132">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="72f1e-132">msmpeg2enc.dll</span></span>

[<span data-ttu-id="72f1e-133">優點</span><span class="sxs-lookup"><span data-stu-id="72f1e-133">Merit</span></span>](merit.md)

<span data-ttu-id="72f1e-134">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="72f1e-134">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="72f1e-135">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="72f1e-135">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="72f1e-136">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="72f1e-136">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="72f1e-137">備註</span><span class="sxs-lookup"><span data-stu-id="72f1e-137">Remarks</span></span>

<span data-ttu-id="72f1e-138">MPEG-2 音訊編碼器可以產生下列種類的輸出：</span><span class="sxs-lookup"><span data-stu-id="72f1e-138">The MPEG-2 Audio Encoder can produce the following kinds of output:</span></span>

-   <span data-ttu-id="72f1e-139">音訊基本資料流程</span><span class="sxs-lookup"><span data-stu-id="72f1e-139">Audio elementary stream</span></span>
-   <span data-ttu-id="72f1e-140">MPEG-2 程式串流中的音訊</span><span class="sxs-lookup"><span data-stu-id="72f1e-140">Audio in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="72f1e-141">MPEG-2 傳輸串流中的音訊</span><span class="sxs-lookup"><span data-stu-id="72f1e-141">Audio in an MPEG-2 transport stream</span></span>

<span data-ttu-id="72f1e-142">它支援 (LSF) 擴充功能的 MPEG-2 層級 I 和 II 和 MPEG-2 低取樣頻率</span><span class="sxs-lookup"><span data-stu-id="72f1e-142">It supports MPEG-1 layers I and II and MPEG-2 low sampling frequency (LSF) extensions</span></span>

<span data-ttu-id="72f1e-143">輸入範例必須是每個樣本16位，音訊取樣率為48、44.1、32、22.05 或 16 KHz。</span><span class="sxs-lookup"><span data-stu-id="72f1e-143">Input samples must 16 bits per sample, with an audio sampling rate of 48, 44.1, 32, 22.05, or 16 KHz.</span></span> <span data-ttu-id="72f1e-144">編碼器無法重新取樣音訊串流;編碼的音訊具有與輸入相同的取樣率。</span><span class="sxs-lookup"><span data-stu-id="72f1e-144">The encoder cannot resample the audio stream; the encoded audio has the same sample rate as the input.</span></span>

<span data-ttu-id="72f1e-145">輸入範例必須是 mono 或身歷聲。</span><span class="sxs-lookup"><span data-stu-id="72f1e-145">Input samples must be mono or stereo.</span></span> <span data-ttu-id="72f1e-146">編碼的音訊具有輸入的通道數目。</span><span class="sxs-lookup"><span data-stu-id="72f1e-146">The encoded audio has the number of channels as the input.</span></span>

### <a name="limitations"></a><span data-ttu-id="72f1e-147">限制</span><span class="sxs-lookup"><span data-stu-id="72f1e-147">Limitations</span></span>

<span data-ttu-id="72f1e-148">編碼器不支援下列各項：</span><span class="sxs-lookup"><span data-stu-id="72f1e-148">The encoder does not support the following:</span></span>

-   <span data-ttu-id="72f1e-149">MPEG layer III 音訊 bitstreams。</span><span class="sxs-lookup"><span data-stu-id="72f1e-149">MPEG layer III audio bitstreams.</span></span>
-   <span data-ttu-id="72f1e-150">MPEG-2 多通道擴充 bitstreams。</span><span class="sxs-lookup"><span data-stu-id="72f1e-150">MPEG-2 multi-channel extension bitstreams.</span></span>
-   <span data-ttu-id="72f1e-151">MPEG 4 AAC bitstreams。</span><span class="sxs-lookup"><span data-stu-id="72f1e-151">MPEG-4 AAC bitstreams.</span></span>
-   <span data-ttu-id="72f1e-152">MPEG-2 的非與舊版相容 (NBC) bitstreams。</span><span class="sxs-lookup"><span data-stu-id="72f1e-152">MPEG-2 non-backward compatible (NBC) bitstreams.</span></span>
-   <span data-ttu-id="72f1e-153">產生 packetized 基本資料流程 (PE) 封包。</span><span class="sxs-lookup"><span data-stu-id="72f1e-153">Generation of packetized elementary stream (PES) packets.</span></span>
-   <span data-ttu-id="72f1e-154">杜比數位編碼。</span><span class="sxs-lookup"><span data-stu-id="72f1e-154">Dolby Digital encoding.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="72f1e-155">編解碼器屬性</span><span class="sxs-lookup"><span data-stu-id="72f1e-155">Codec Properties</span></span>

<span data-ttu-id="72f1e-156">篩選準則透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="72f1e-156">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>

-   [<span data-ttu-id="72f1e-157">**AVAudioChannelCount**</span><span class="sxs-lookup"><span data-stu-id="72f1e-157">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)
-   [<span data-ttu-id="72f1e-158">**AVAudioSampleRate**</span><span class="sxs-lookup"><span data-stu-id="72f1e-158">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)
-   [<span data-ttu-id="72f1e-159">**AVEncAudioIntervalToEncode**</span><span class="sxs-lookup"><span data-stu-id="72f1e-159">**AVEncAudioIntervalToEncode**</span></span>](avencaudiointervaltoencode-property.md)
-   [<span data-ttu-id="72f1e-160">**AVEncCommonFormatConstraint**</span><span class="sxs-lookup"><span data-stu-id="72f1e-160">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
-   [<span data-ttu-id="72f1e-161">**AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="72f1e-161">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="72f1e-162">**AVEncMPACodingMode**</span><span class="sxs-lookup"><span data-stu-id="72f1e-162">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)
-   [<span data-ttu-id="72f1e-163">**AVEncMPACopyright**</span><span class="sxs-lookup"><span data-stu-id="72f1e-163">**AVEncMPACopyright**</span></span>](avencmpacopyright-property.md)
-   [<span data-ttu-id="72f1e-164">**AVEncMPAEmphasisType**</span><span class="sxs-lookup"><span data-stu-id="72f1e-164">**AVEncMPAEmphasisType**</span></span>](avencmpaemphasistype-property.md)
-   [<span data-ttu-id="72f1e-165">**AVEncMPAEnableRedundancyProtection**</span><span class="sxs-lookup"><span data-stu-id="72f1e-165">**AVEncMPAEnableRedundancyProtection**</span></span>](avencmpaenableredundancyprotection-property.md)
-   [<span data-ttu-id="72f1e-166">**AVEncMPALayer**</span><span class="sxs-lookup"><span data-stu-id="72f1e-166">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
-   [<span data-ttu-id="72f1e-167">**AVEncMPAOriginalBitstream**</span><span class="sxs-lookup"><span data-stu-id="72f1e-167">**AVEncMPAOriginalBitstream**</span></span>](avencmpaoriginalbitstream-property.md)
-   [<span data-ttu-id="72f1e-168">**AVEncMPAPrivateUserBit**</span><span class="sxs-lookup"><span data-stu-id="72f1e-168">**AVEncMPAPrivateUserBit**</span></span>](avencmpaprivateuserbit-property.md)

> [!Note]  
> <span data-ttu-id="72f1e-169">舊版檔不正確地列出一些不支援的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="72f1e-169">An earlier version of the documentation incorrectly listed some additional properties that are not supported.</span></span>

 

<span data-ttu-id="72f1e-170">為了回溯相容性，此篩選會透過 **IEncoderAPI** 介面支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="72f1e-170">For backward compatibility, the filter supports the following property through the **IEncoderAPI** interface:</span></span>



| <span data-ttu-id="72f1e-171">屬性</span><span class="sxs-lookup"><span data-stu-id="72f1e-171">Property</span></span>                 | <span data-ttu-id="72f1e-172">描述</span><span class="sxs-lookup"><span data-stu-id="72f1e-172">Description</span></span>                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="72f1e-173">**ENCAPIPARAM \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="72f1e-173">**ENCAPIPARAM\_BITRATE**</span></span> | <span data-ttu-id="72f1e-174">相當於 [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)。</span><span class="sxs-lookup"><span data-stu-id="72f1e-174">Equivalent to [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).</span></span> |



 

<span data-ttu-id="72f1e-175">建議您以下列順序設定屬性：</span><span class="sxs-lookup"><span data-stu-id="72f1e-175">It is recommended to set properties in the following order:</span></span>

1.  [<span data-ttu-id="72f1e-176">**AVEncCommonFormatConstraint**</span><span class="sxs-lookup"><span data-stu-id="72f1e-176">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
2.  [<span data-ttu-id="72f1e-177">**AVEncMPALayer**</span><span class="sxs-lookup"><span data-stu-id="72f1e-177">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
3.  [<span data-ttu-id="72f1e-178">**AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="72f1e-178">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
4.  [<span data-ttu-id="72f1e-179">**AVEncMPACodingMode**</span><span class="sxs-lookup"><span data-stu-id="72f1e-179">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)

<span data-ttu-id="72f1e-180">以任何順序設定其餘的屬性。</span><span class="sxs-lookup"><span data-stu-id="72f1e-180">Set the remaining properties in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f1e-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="72f1e-181">Requirements</span></span>



| <span data-ttu-id="72f1e-182">需求</span><span class="sxs-lookup"><span data-stu-id="72f1e-182">Requirement</span></span> | <span data-ttu-id="72f1e-183">值</span><span class="sxs-lookup"><span data-stu-id="72f1e-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72f1e-184">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72f1e-184">Minimum supported client</span></span><br/> | <span data-ttu-id="72f1e-185">Windows Vista Home Premium、Windows Vista 旗艦版、Windows 7 Home Premium、Windows 7 Professional、Windows 7 企業版、僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72f1e-185">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="72f1e-186">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72f1e-186">Minimum supported server</span></span><br/> | <span data-ttu-id="72f1e-187">都不支援</span><span class="sxs-lookup"><span data-stu-id="72f1e-187">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="72f1e-188">標頭</span><span class="sxs-lookup"><span data-stu-id="72f1e-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="72f1e-189"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="72f1e-189"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="72f1e-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72f1e-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f1e-191">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="72f1e-191">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="72f1e-192">**MPEG-2 信號信號媒體類型**</span><span class="sxs-lookup"><span data-stu-id="72f1e-192">**MPEG-2 Demultiplexer Media Types**</span></span>](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
