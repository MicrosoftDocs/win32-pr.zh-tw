---
description: 媒體類型轉換
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: 媒體類型轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3a72e74439251f9661e0ff27166c504e47c238
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103696266"
---
# <a name="media-type-conversions"></a><span data-ttu-id="4f3c0-103">媒體類型轉換</span><span class="sxs-lookup"><span data-stu-id="4f3c0-103">Media Type Conversions</span></span>

<span data-ttu-id="4f3c0-104">有時候，您必須在媒體基礎媒體類型與 DirectShow 或 Windows Media Format SDK 的較舊媒體類型結構之間進行轉換。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-104">Occasionally it is necessary to convert between Media Foundation media types and the older media type structures from DirectShow or the Windows Media Format SDK.</span></span>

### <a name="from-a-format-structure-to-a-media-foundation-type"></a><span data-ttu-id="4f3c0-105">從格式結構到媒體基礎類型</span><span class="sxs-lookup"><span data-stu-id="4f3c0-105">From a Format Structure to a Media Foundation Type</span></span>

<span data-ttu-id="4f3c0-106">下列函式會從格式結構初始化媒體基礎的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-106">The following functions initialize a Media Foundation media type from a format structure.</span></span> <span data-ttu-id="4f3c0-107">如果資料流程或檔案標頭包含格式結構，這些函數也很有用。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-107">These functions are also useful if a data stream or a file header contains a format structure.</span></span> <span data-ttu-id="4f3c0-108">例如，WAVE 音訊檔案的 file 標頭包含 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-108">For example, the file header for WAVE audio files contains a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f3c0-109">要轉換的結構</span><span class="sxs-lookup"><span data-stu-id="4f3c0-109">Structure to Convert</span></span></th>
<th><span data-ttu-id="4f3c0-110">函式</span><span class="sxs-lookup"><span data-stu-id="4f3c0-110">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4f3c0-111"><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="4f3c0-111"><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)</span></span><br/> <span data-ttu-id="4f3c0-112"><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (DirectX 媒體物件) </span><span class="sxs-lookup"><span data-stu-id="4f3c0-112"><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (DirectX Media Objects)</span></span> <br/> <span data-ttu-id="4f3c0-113"><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows MEDIA Format SDK) </span><span class="sxs-lookup"><span data-stu-id="4f3c0-113"><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows Media Format SDK)</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4f3c0-114">這些結構是相等的。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-114">These structures are equivalent.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="4f3c0-115"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-115"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f3c0-116"><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-116"><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></span></span></td>
<td><span data-ttu-id="4f3c0-117"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-117"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f3c0-118"><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-118"><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="4f3c0-119"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-119"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f3c0-120"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-120"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></span></span></td>
<td><span data-ttu-id="4f3c0-121"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-121"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f3c0-122"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-122"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></span></span></td>
<td><span data-ttu-id="4f3c0-123"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-123"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f3c0-124"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-124"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></span></span></td>
<td><span data-ttu-id="4f3c0-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f3c0-126"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-126"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></span></span></td>
<td><span data-ttu-id="4f3c0-127"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-127"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f3c0-128"><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a>或<a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>WAVEFORMATEXTENSIBLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-128"><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> or <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"><strong>WAVEFORMATEXTENSIBLE</strong></a></span></span></td>
<td><span data-ttu-id="4f3c0-129"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f3c0-129"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a><span data-ttu-id="4f3c0-130">從媒體基礎類型到格式結構</span><span class="sxs-lookup"><span data-stu-id="4f3c0-130">From a Media Foundation Type to a Format Structure</span></span>

<span data-ttu-id="4f3c0-131">下列函式會建立或初始化媒體基礎媒體類型的格式結構。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-131">The following functions create or initialize a format structure from a Media Foundation media type.</span></span>



| <span data-ttu-id="4f3c0-132">函式</span><span class="sxs-lookup"><span data-stu-id="4f3c0-132">Function</span></span>                                                                             | <span data-ttu-id="4f3c0-133">目標結構</span><span class="sxs-lookup"><span data-stu-id="4f3c0-133">Target Structure</span></span>                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f3c0-134">**IMFMediaType::GetRepresentation**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-134">**IMFMediaType::GetRepresentation**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | <span data-ttu-id="4f3c0-135">[**AM \_媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)、 [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)、 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)或 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span><span class="sxs-lookup"><span data-stu-id="4f3c0-135">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader), or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span></span> |
| [<span data-ttu-id="4f3c0-136">**MFCreateAMMediaTypeFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-136">**MFCreateAMMediaTypeFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [<span data-ttu-id="4f3c0-137">**\_媒體 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-137">**AM\_MEDIA\_TYPE**</span></span>](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [<span data-ttu-id="4f3c0-138">**MFCreateMFVideoFormatFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-138">**MFCreateMFVideoFormatFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [<span data-ttu-id="4f3c0-139">**MFVIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-139">**MFVIDEOFORMAT**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [<span data-ttu-id="4f3c0-140">**MFCreateWaveFormatExFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-140">**MFCreateWaveFormatExFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | <span data-ttu-id="4f3c0-141">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))或 [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4f3c0-141">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))</span></span>                                                                                    |
| [<span data-ttu-id="4f3c0-142">**MFInitAMMediaTypeFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-142">**MFInitAMMediaTypeFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [<span data-ttu-id="4f3c0-143">**\_媒體 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-143">**AM\_MEDIA\_TYPE**</span></span>](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a><span data-ttu-id="4f3c0-144">格式對應</span><span class="sxs-lookup"><span data-stu-id="4f3c0-144">Format Mappings</span></span>

<span data-ttu-id="4f3c0-145">下表列出對應至各種格式結構的媒體基礎屬性。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-145">The following tables list the Media Foundation attributes that correspond to various format structures.</span></span> <span data-ttu-id="4f3c0-146">並非所有這些屬性都可以直接轉譯。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-146">Not all of these attributes can be translated directly.</span></span> <span data-ttu-id="4f3c0-147">若要執行轉換，您應該使用上一節所列的函式;這些資料表主要是供參考之用。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-147">To perform conversions, you should use the functions listed in the previous section; these tables are provided mainly for reference.</span></span>

### <a name="am_media_type"></a><span data-ttu-id="4f3c0-148">\_媒體 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="4f3c0-148">AM\_MEDIA\_TYPE</span></span>



| <span data-ttu-id="4f3c0-149">成員</span><span class="sxs-lookup"><span data-stu-id="4f3c0-149">Member</span></span>                   | <span data-ttu-id="4f3c0-150">屬性</span><span class="sxs-lookup"><span data-stu-id="4f3c0-150">Attribute</span></span>                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4f3c0-151">**bTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-151">**bTemporalCompression**</span></span> | [<span data-ttu-id="4f3c0-152">**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-152">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) |
| <span data-ttu-id="4f3c0-153">**bFixedSizeSamples**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-153">**bFixedSizeSamples**</span></span>    | [<span data-ttu-id="4f3c0-154">**MF \_ MT \_ 固定 \_ 大小 \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-154">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)           |
| <span data-ttu-id="4f3c0-155">**lSampleSize**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-155">**lSampleSize**</span></span>          | [<span data-ttu-id="4f3c0-156">**MF \_ MT \_ 樣本 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-156">**MF\_MT\_SAMPLE\_SIZE**</span></span>](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a><span data-ttu-id="4f3c0-157">WAVEFORMATEX, WAVEFORMATEXTENSIBLE</span><span class="sxs-lookup"><span data-stu-id="4f3c0-157">WAVEFORMATEX, WAVEFORMATEXTENSIBLE</span></span>



| <span data-ttu-id="4f3c0-158">成員</span><span class="sxs-lookup"><span data-stu-id="4f3c0-158">Member</span></span>                  | <span data-ttu-id="4f3c0-159">屬性</span><span class="sxs-lookup"><span data-stu-id="4f3c0-159">Attribute</span></span>                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f3c0-160">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-160">**wFormatTag**</span></span>          | [<span data-ttu-id="4f3c0-161">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-161">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)<br/> <span data-ttu-id="4f3c0-162">如果 **wFormatTag** 是 WAVE 格式可延伸的 \_ \_ ，子類型會在 **SubFormat** 成員中找到。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-162">If **wFormatTag** is WAVE\_FORMAT\_EXTENSIBLE, the subtype is found in the **SubFormat** member.</span></span><br/> |
| <span data-ttu-id="4f3c0-163">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-163">**nChannels**</span></span>           | [<span data-ttu-id="4f3c0-164">**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-164">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| <span data-ttu-id="4f3c0-165">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-165">**nSamplesPerSec**</span></span>      | [<span data-ttu-id="4f3c0-166">**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-166">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| <span data-ttu-id="4f3c0-167">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-167">**nAvgBytesPerSec**</span></span>     | [<span data-ttu-id="4f3c0-168">**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-168">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| <span data-ttu-id="4f3c0-169">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-169">**nBlockAlign**</span></span>         | [<span data-ttu-id="4f3c0-170">**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-170">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| <span data-ttu-id="4f3c0-171">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-171">**wBitsPerSample**</span></span>      | [<span data-ttu-id="4f3c0-172">**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-172">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| <span data-ttu-id="4f3c0-173">**wValidBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-173">**wValidBitsPerSample**</span></span> | [<span data-ttu-id="4f3c0-174">**\_ \_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊有效位數**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-174">**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| <span data-ttu-id="4f3c0-175">**wSamplesPerBlock**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-175">**wSamplesPerBlock**</span></span>    | [<span data-ttu-id="4f3c0-176">**\_ \_ \_ \_ 每個 \_ 區塊的 MF MT 音訊範例**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-176">**MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK**</span></span>](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| <span data-ttu-id="4f3c0-177">**dwChannelMask**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-177">**dwChannelMask**</span></span>       | [<span data-ttu-id="4f3c0-178">**MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-178">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| <span data-ttu-id="4f3c0-179">**SubFormat**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-179">**SubFormat**</span></span>           | [<span data-ttu-id="4f3c0-180">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-180">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                                                                                                        |
| <span data-ttu-id="4f3c0-181">額外的資料</span><span class="sxs-lookup"><span data-stu-id="4f3c0-181">Extra data</span></span>              | [<span data-ttu-id="4f3c0-182">**MF \_ MT \_ 使用者 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-182">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a><span data-ttu-id="4f3c0-183">VIDEOINFOHEADER, VIDEOINFOHEADER2</span><span class="sxs-lookup"><span data-stu-id="4f3c0-183">VIDEOINFOHEADER, VIDEOINFOHEADER2</span></span>



| <span data-ttu-id="4f3c0-184">成員</span><span class="sxs-lookup"><span data-stu-id="4f3c0-184">Member</span></span>                                         | <span data-ttu-id="4f3c0-185">屬性</span><span class="sxs-lookup"><span data-stu-id="4f3c0-185">Attribute</span></span>                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f3c0-186">**dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-186">**dwBitRate**</span></span>                                  | [<span data-ttu-id="4f3c0-187">**MF \_ MT \_ 平均 \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-187">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| <span data-ttu-id="4f3c0-188">**dwBitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-188">**dwBitErrorRate**</span></span>                             | [<span data-ttu-id="4f3c0-189">**MF \_ MT \_ 平均 \_ 位 \_ 誤差 \_ 率**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-189">**MF\_MT\_AVG\_BIT\_ERROR\_RATE**</span></span>](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| <span data-ttu-id="4f3c0-190">**AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-190">**AvgTimePerFrame**</span></span>                            | <span data-ttu-id="4f3c0-191">[**MF \_MT \_ 幀 \_ 速率**](mf-mt-frame-rate-attribute.md); 使用 [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) 來計算這個值。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-191">[**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md); use [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) to calculate this value.</span></span>                                                                             |
| <span data-ttu-id="4f3c0-192">**dwInterlaceFlags**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-192">**dwInterlaceFlags**</span></span>                           | [<span data-ttu-id="4f3c0-193">**MF \_ MT \_ 交錯 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-193">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| <span data-ttu-id="4f3c0-194">**dwCopyProtectFlags**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-194">**dwCopyProtectFlags**</span></span>                         | <span data-ttu-id="4f3c0-195">沒有任何定義的對等專案</span><span class="sxs-lookup"><span data-stu-id="4f3c0-195">No defined equivalent</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="4f3c0-196">**dwPictAspectRatioX**、 **dwPictAspectRatioY**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-196">**dwPictAspectRatioX**, **dwPictAspectRatioY**</span></span> | <span data-ttu-id="4f3c0-197">[**MF \_MT \_ 圖元 \_ 外觀 \_ 比例**](mf-mt-pixel-aspect-ratio-attribute.md); 必須從圖片外觀比例轉換成圖片外觀比例。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-197">[**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md); must convert from picture aspect ratio to picture aspect ratio.</span></span>                                                                                                      |
| <span data-ttu-id="4f3c0-198">**dwControlFlags**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-198">**dwControlFlags**</span></span>                             | <span data-ttu-id="4f3c0-199">[**MF \_MT \_ 板 \_ 控制項 \_ 旗標**](mf-mt-pad-control-flags-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-199">[**MF\_MT\_PAD\_CONTROL\_FLAGS**](mf-mt-pad-control-flags-attribute.md).</span></span> <span data-ttu-id="4f3c0-200">如果出現 **AMCONTROL \_ COLORINFO \_** 的旗標，請設定 [擴充色彩資訊](extended-color-information.md)中所述的擴充色彩屬性。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-200">If the **AMCONTROL\_COLORINFO\_PRESENT** flag is present, set the extended color attributes described in [Extended Color Information](extended-color-information.md).</span></span> |
| <span data-ttu-id="4f3c0-201">**bmiHeader. biWidth**、 **bmiHeader. biHeight**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-201">**bmiHeader.biWidth**, **bmiHeader.biHeight**</span></span>  | [<span data-ttu-id="4f3c0-202">**MF \_ MT \_ 框架 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-202">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| <span data-ttu-id="4f3c0-203">**bmiHeader.biBitCount**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-203">**bmiHeader.biBitCount**</span></span>                       | <span data-ttu-id="4f3c0-204">子類型中的隱含 ([**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)) 。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-204">Implicit in the subtype ([**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md)).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="4f3c0-205">**bmiHeader.biCompression**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-205">**bmiHeader.biCompression**</span></span>                    | <span data-ttu-id="4f3c0-206">子類型中的隱含。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-206">Implicit in the subtype.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="4f3c0-207">**bmiHeader.biSizeImage**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-207">**bmiHeader.biSizeImage**</span></span>                      | [<span data-ttu-id="4f3c0-208">**MF \_ MT \_ 樣本 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-208">**MF\_MT\_SAMPLE\_SIZE**</span></span>](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| <span data-ttu-id="4f3c0-209">調色板資訊</span><span class="sxs-lookup"><span data-stu-id="4f3c0-209">Palette information</span></span>                            | [<span data-ttu-id="4f3c0-210">**MF \_ MT \_ 調色板**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-210">**MF\_MT\_PALETTE**</span></span>](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

<span data-ttu-id="4f3c0-211">下列屬性可以從 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 或 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 結構推斷，但也需要一些格式詳細資料的知識。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-211">The following attributes can be inferred from the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure but also require some knowledge of the format details.</span></span> <span data-ttu-id="4f3c0-212">例如，不同的 YUV 格式具有不同的 stride 需求。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-212">For example, different YUV formats have different stride requirements.</span></span>

-   [<span data-ttu-id="4f3c0-213">**MF \_ MT \_ 預設 \_ STRIDE**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-213">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)
-   [<span data-ttu-id="4f3c0-214">**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-214">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="4f3c0-215">**MF \_ MT \_ 平移 \_ 掃描 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-215">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a><span data-ttu-id="4f3c0-216">MPEG1VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="4f3c0-216">MPEG1VIDEOINFO</span></span>



| <span data-ttu-id="4f3c0-217">成員</span><span class="sxs-lookup"><span data-stu-id="4f3c0-217">Member</span></span>                                   | <span data-ttu-id="4f3c0-218">屬性</span><span class="sxs-lookup"><span data-stu-id="4f3c0-218">Attribute</span></span>                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4f3c0-219">**dwStartTimeCode**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-219">**dwStartTimeCode**</span></span>                      | [<span data-ttu-id="4f3c0-220">**MF \_ MT \_ MPEG \_ 開始 \_ 時間 \_ 代碼**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-220">**MF\_MT\_MPEG\_START\_TIME\_CODE**</span></span>](mf-mt-mpeg-start-time-code-attribute.md) |
| <span data-ttu-id="4f3c0-221">**bSequenceHeader**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-221">**bSequenceHeader**</span></span>                      | [<span data-ttu-id="4f3c0-222">**MF \_ MT \_ MPEG \_ 序列 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-222">**MF\_MT\_MPEG\_SEQUENCE\_HEADER**</span></span>](mf-mt-mpeg-sequence-header-attribute.md)  |
| <span data-ttu-id="4f3c0-223">**biXPelsPerMeter**、 **biYPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-223">**biXPelsPerMeter**, **biYPelsPerMeter**</span></span> | [<span data-ttu-id="4f3c0-224">**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-224">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a><span data-ttu-id="4f3c0-225">MPEG2VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="4f3c0-225">MPEG2VIDEOINFO</span></span>



| <span data-ttu-id="4f3c0-226">成員</span><span class="sxs-lookup"><span data-stu-id="4f3c0-226">Member</span></span>               | <span data-ttu-id="4f3c0-227">屬性</span><span class="sxs-lookup"><span data-stu-id="4f3c0-227">Attribute</span></span>                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4f3c0-228">**dwStartTimeCode**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-228">**dwStartTimeCode**</span></span>  | [<span data-ttu-id="4f3c0-229">**MF \_ MT \_ MPEG \_ 開始 \_ 時間 \_ 代碼**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-229">**MF\_MT\_MPEG\_START\_TIME\_CODE**</span></span>](mf-mt-mpeg-start-time-code-attribute.md) |
| <span data-ttu-id="4f3c0-230">**dwSequenceHeader**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-230">**dwSequenceHeader**</span></span> | [<span data-ttu-id="4f3c0-231">**MF \_ MT \_ MPEG \_ 序列 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-231">**MF\_MT\_MPEG\_SEQUENCE\_HEADER**</span></span>](mf-mt-mpeg-sequence-header-attribute.md)  |
| <span data-ttu-id="4f3c0-232">**dwProfile**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-232">**dwProfile**</span></span>        | [<span data-ttu-id="4f3c0-233">**MF \_ MT \_ MPEG2 \_ 設定檔**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-233">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md)                 |
| <span data-ttu-id="4f3c0-234">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-234">**dwLevel**</span></span>          | [<span data-ttu-id="4f3c0-235">**MF \_ MT \_ MPEG2 \_ 層級**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-235">**MF\_MT\_MPEG2\_LEVEL**</span></span>](mf-mt-mpeg2-level-attribute.md)                     |
| <span data-ttu-id="4f3c0-236">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-236">**dwFlags**</span></span>          | [<span data-ttu-id="4f3c0-237">**MF \_ MT \_ MPEG2 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="4f3c0-237">**MF\_MT\_MPEG2\_FLAGS**</span></span>](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a><span data-ttu-id="4f3c0-238">範例</span><span class="sxs-lookup"><span data-stu-id="4f3c0-238">Examples</span></span>

<span data-ttu-id="4f3c0-239">下列程式碼會從影片媒體類型填入 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-239">The following code fills in a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure from a video media type.</span></span> <span data-ttu-id="4f3c0-240">請注意，這項轉換會遺失部分格式資訊 (交錯、畫面播放速率、擴充色彩資料) 。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-240">Note that this conversions loses some of the format information (interlacing, frame rate, extended color data).</span></span> <span data-ttu-id="4f3c0-241">不過，這在從影片框架儲存點陣圖時可能很有用。</span><span class="sxs-lookup"><span data-stu-id="4f3c0-241">However, it might be useful when saving a bitmap from a video frame, for example.</span></span>


```C++
#include <dshow.h>
#include <dvdmedia.h>

// Converts a video type to a BITMAPINFO structure.
// The caller must free the structure by calling CoTaskMemFree.

// Note that this conversion loses some format information, including 
// interlacing, and frame rate.

HRESULT GetBitmapInfoHeaderFromMFMediaType(
    IMFMediaType *pType,            // Pointer to the media type.
    BITMAPINFOHEADER **ppBmih,      // Receives a pointer to the structure. 
    DWORD *pcbSize)                 // Receives the size of the structure.
{
    *ppBmih = NULL;
    *pcbSize = 0;

    GUID majorType = GUID_NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    DWORD cbSize = 0;
    DWORD cbOffset = 0;
    BITMAPINFOHEADER *pBMIH = NULL;

    // Verify that this is a video type.
    HRESULT hr = pType->GetMajorType(&majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (majorType != MFMediaType_Video)
    {
        hr = MF_E_INVALIDMEDIATYPE;
        goto done;
    }

    hr = pType->GetRepresentation(AM_MEDIA_TYPE_REPRESENTATION, (void**)&pmt);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pmt->formattype == FORMAT_VideoInfo)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER,bmiHeader));
    }
    else if (pmt->formattype == FORMAT_VideoInfo2)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER2,bmiHeader));
    }
    else
    {
        hr = MF_E_INVALIDMEDIATYPE; // Unsupported format type.
        goto done;
    }

    if (pmt->cbFormat - cbOffset < sizeof(BITMAPINFOHEADER))
    {
        hr = E_UNEXPECTED; // Bad format size. 
        goto done;
    }

    cbSize = pmt->cbFormat - cbOffset;

    pBMIH = (BITMAPINFOHEADER*)CoTaskMemAlloc(cbSize);
    if (pBMIH == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }
    
    CopyMemory(pBMIH, pmt->pbFormat + cbOffset, cbSize);
    
    *ppBmih = pBMIH;
    *pcbSize = cbSize;

done:
    if (pmt)
    {
        pType->FreeRepresentation(AM_MEDIA_TYPE_REPRESENTATION, pmt);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4f3c0-242">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f3c0-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f3c0-243">媒體類型</span><span class="sxs-lookup"><span data-stu-id="4f3c0-243">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
