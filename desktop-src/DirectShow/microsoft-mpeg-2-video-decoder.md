---
description: 此篩選器會將 MPEG-2、MPEG-2、h.264 video 解碼。
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: 'Microsoft MPEG-2 影片解碼 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385609"
---
# <a name="microsoft-mpeg-2-video-decoder"></a><span data-ttu-id="0e110-103">Microsoft MPEG-2 影片解碼</span><span class="sxs-lookup"><span data-stu-id="0e110-103">Microsoft MPEG-2 Video Decoder</span></span>

<span data-ttu-id="0e110-104">此篩選器會將 MPEG-2、MPEG-2、h.264 video 解碼。</span><span class="sxs-lookup"><span data-stu-id="0e110-104">This filter decodes MPEG-1, MPEG-2, H.264 video.</span></span>

> [!Note]  
> <span data-ttu-id="0e110-105">對 h.264 video 進行解碼需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="0e110-105">Decoding of H.264 video requires Windows 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0e110-106">以 IA-64 為基礎的平臺不支援此篩選器。</span><span class="sxs-lookup"><span data-stu-id="0e110-106">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="0e110-107">在登錄中，此篩選器的易記名稱是「Microsoft DTV DVD Video 解碼」。</span><span class="sxs-lookup"><span data-stu-id="0e110-107">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Video Decoder".</span></span>



<span data-ttu-id="0e110-108">篩選資訊</span><span class="sxs-lookup"><span data-stu-id="0e110-108">Filter Information</span></span>

<span data-ttu-id="0e110-109">篩選介面</span><span class="sxs-lookup"><span data-stu-id="0e110-109">Filter Interfaces</span></span>

[<span data-ttu-id="0e110-110">**IAMDecoderCaps**</span><span class="sxs-lookup"><span data-stu-id="0e110-110">**IAMDecoderCaps**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [<span data-ttu-id="0e110-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="0e110-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="0e110-112">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="0e110-112">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="0e110-113">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="0e110-113">Input Pin Media Types</span></span>

<span data-ttu-id="0e110-114">影片輸入釘選：</span><span class="sxs-lookup"><span data-stu-id="0e110-114">Video input pin:</span></span>

-   <span data-ttu-id="0e110-115">媒體 \_ 媒體 \_ 加密 \_ 套件，MEDIASUBTYPE \_ MPEG2 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="0e110-115">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="0e110-116">媒體 \_ \_ 上的 MPEG2，MEDIASUBTYPE \_ MPEG2 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="0e110-116">MEDIATYPE\_MPEG2\_PES, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="0e110-117">媒體媒體 \_ 、MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="0e110-117">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Packet</span></span>
-   <span data-ttu-id="0e110-118">媒體媒體 \_ 、MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="0e110-118">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Payload</span></span>
-   <span data-ttu-id="0e110-119">媒體媒體 \_ MEDIASUBTYPE \_ MPEG2 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="0e110-119">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>

<span data-ttu-id="0e110-120">子圖片輸入 pin：</span><span class="sxs-lookup"><span data-stu-id="0e110-120">Subpicture input pin:</span></span><br/>

-   <span data-ttu-id="0e110-121">媒體 \_ \_ \_ MEDIASUBTYPE \_ DVD 子圖片、媒體加密 \_ 套件</span><span class="sxs-lookup"><span data-stu-id="0e110-121">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_DVD\_SUBPICTURE</span></span>

<span data-ttu-id="0e110-122">從 Windows 7 開始，影片輸入 pin 也支援下列輸入類型：</span><span class="sxs-lookup"><span data-stu-id="0e110-122">Starting in Windows 7, the video input pin also supports the following input types:</span></span><br/>

-   <span data-ttu-id="0e110-123">**媒體媒體 \_影片**、 **MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="0e110-123">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_AVC1**</span></span>
-   <span data-ttu-id="0e110-124">**媒體媒體 \_影片**， **MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="0e110-124">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_H264**</span></span>
-   <span data-ttu-id="0e110-125">**媒體媒體 \_影片**， **MEDIASUBTYPE \_ h264**</span><span class="sxs-lookup"><span data-stu-id="0e110-125">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_h264**</span></span>
-   <span data-ttu-id="0e110-126">**媒體媒體 \_影片**、 **MEDIASUBTYPE \_ X264**</span><span class="sxs-lookup"><span data-stu-id="0e110-126">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_X264**</span></span>
-   <span data-ttu-id="0e110-127">**媒體媒體 \_影片**、 **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="0e110-127">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_x264**</span></span>

<span data-ttu-id="0e110-128">如需詳細資訊，請參閱 h.264 [影片類型](h-264-video-types.md) 。</span><span class="sxs-lookup"><span data-stu-id="0e110-128">See [H.264 Video Types](h-264-video-types.md) for more information.</span></span> <span data-ttu-id="0e110-129">輸入媒體類型可以在 MPEG2 和 h.264 類型之間動態變更。</span><span class="sxs-lookup"><span data-stu-id="0e110-129">The input media type can change dynamically between MPEG2 and H.264 types.</span></span><br/>

<span data-ttu-id="0e110-130">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="0e110-130">Input Pin Interfaces</span></span>

[<span data-ttu-id="0e110-131">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="0e110-131">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="0e110-132">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="0e110-132">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="0e110-133">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="0e110-133">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="0e110-134">**IMFSampleProtection**</span><span class="sxs-lookup"><span data-stu-id="0e110-134">**IMFSampleProtection**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [<span data-ttu-id="0e110-135">**IPin**</span><span class="sxs-lookup"><span data-stu-id="0e110-135">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="0e110-136">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="0e110-136">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="0e110-137">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="0e110-137">Output Pin Media Types</span></span>

<span data-ttu-id="0e110-138">影片輸出圖釘：</span><span class="sxs-lookup"><span data-stu-id="0e110-138">Video output pin:</span></span>

-   <span data-ttu-id="0e110-139">媒體媒體 \_ 、DXVA \_ MODEMPEG2 \_ (DXVA 1.0) </span><span class="sxs-lookup"><span data-stu-id="0e110-139">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_A (DXVA 1.0)</span></span>
-   <span data-ttu-id="0e110-140">媒體媒體 \_ 、DXVA \_ ModeMPEG2 \_ C (DXVA 1.0) </span><span class="sxs-lookup"><span data-stu-id="0e110-140">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_C (DXVA 1.0)</span></span>
-   <span data-ttu-id="0e110-141">媒體媒體 \_ 、MEDIASUBTYPE \_ I420 (軟體解碼或 dxva 2.0) </span><span class="sxs-lookup"><span data-stu-id="0e110-141">MEDIATYPE\_Video, MEDIASUBTYPE\_I420 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="0e110-142">媒體媒體 \_ 、MEDIASUBTYPE \_ NV12 (軟體解碼或 dxva 2.0) </span><span class="sxs-lookup"><span data-stu-id="0e110-142">MEDIATYPE\_Video, MEDIASUBTYPE\_NV12 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="0e110-143">媒體媒體 \_ 、MEDIASUBTYPE \_ YUY2 (軟體解碼或 dxva 2.0) </span><span class="sxs-lookup"><span data-stu-id="0e110-143">MEDIATYPE\_Video, MEDIASUBTYPE\_YUY2 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="0e110-144">媒體媒體 \_ 、MEDIASUBTYPE \_ IMC3 (僅限 dxva 2.0) </span><span class="sxs-lookup"><span data-stu-id="0e110-144">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC3 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="0e110-145">媒體媒體 \_ 、MEDIASUBTYPE \_ IMC4 (僅限 dxva 2.0) </span><span class="sxs-lookup"><span data-stu-id="0e110-145">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC4 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="0e110-146">媒體媒體 \_ 、MEDIASUBTYPE \_ S340 (僅限 dxva 2.0) </span><span class="sxs-lookup"><span data-stu-id="0e110-146">MEDIATYPE\_Video, MEDIASUBTYPE\_S340 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="0e110-147">媒體媒體 \_ 、MEDIASUBTYPE \_ YV12 (僅限 dxva 2.0) </span><span class="sxs-lookup"><span data-stu-id="0e110-147">MEDIATYPE\_Video, MEDIASUBTYPE\_YV12 (DXVA2.0 only)</span></span>

<span data-ttu-id="0e110-148">行21輸出圖釘：</span><span class="sxs-lookup"><span data-stu-id="0e110-148">Line-21 output pin:</span></span><br/>

-   <span data-ttu-id="0e110-149">媒體 \_ AUXLine21Data、MEDIASUBTYPE \_ Line21 \_ GOPPacket</span><span class="sxs-lookup"><span data-stu-id="0e110-149">MEDIATYPE\_AUXLine21Data, MEDIASUBTYPE\_Line21\_GOPPacket</span></span>

<span data-ttu-id="0e110-150">子圖片輸出 pin：</span><span class="sxs-lookup"><span data-stu-id="0e110-150">Subpicture output pin:</span></span><br/>

-   <span data-ttu-id="0e110-151">媒體媒體 \_ 、MEDIASUBTYPE \_ AI44</span><span class="sxs-lookup"><span data-stu-id="0e110-151">MEDIATYPE\_Video, MEDIASUBTYPE\_AI44</span></span>
-   <span data-ttu-id="0e110-152">媒體媒體 \_ 、MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="0e110-152">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="0e110-153">媒體媒體 \_ 、MEDIASUBTYPE \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="0e110-153">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="0e110-154">媒體媒體 \_ 、MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="0e110-154">MEDIATYPE\_Video, MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="0e110-155">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="0e110-155">Output Pin Interfaces</span></span>

<span data-ttu-id="0e110-156">[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (video 輸出釘選) </span><span class="sxs-lookup"><span data-stu-id="0e110-156">[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (video output pin only)</span></span><br/> [<span data-ttu-id="0e110-157">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="0e110-157">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="0e110-158">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="0e110-158">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="0e110-159">**IPin**</span><span class="sxs-lookup"><span data-stu-id="0e110-159">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="0e110-160">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="0e110-160">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [<span data-ttu-id="0e110-161">**IVPConfig**</span><span class="sxs-lookup"><span data-stu-id="0e110-161">**IVPConfig**</span></span>](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

<span data-ttu-id="0e110-162">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="0e110-162">Filter CLSID</span></span>

<span data-ttu-id="0e110-163">**CLSID \_** 在 wmcodecdsp 中定義的 CMPEG2VidDecoderDS () </span><span class="sxs-lookup"><span data-stu-id="0e110-163">**CLSID\_CMPEG2VidDecoderDS** (defined in wmcodecdsp.h)</span></span>

<span data-ttu-id="0e110-164">可執行檔</span><span class="sxs-lookup"><span data-stu-id="0e110-164">Executable</span></span>

<span data-ttu-id="0e110-165">msmpeg2vdec.dll</span><span class="sxs-lookup"><span data-stu-id="0e110-165">msmpeg2vdec.dll</span></span>

[<span data-ttu-id="0e110-166">優點</span><span class="sxs-lookup"><span data-stu-id="0e110-166">Merit</span></span>](merit.md)

<span data-ttu-id="0e110-167">**業績 \_正常** -1</span><span class="sxs-lookup"><span data-stu-id="0e110-167">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="0e110-168">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="0e110-168">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="0e110-169">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="0e110-169">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="0e110-170">備註</span><span class="sxs-lookup"><span data-stu-id="0e110-170">Remarks</span></span>

<span data-ttu-id="0e110-171">此篩選器有兩個輸入圖釘和三個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="0e110-171">This filter has two input pins and three output pins.</span></span>

<span data-ttu-id="0e110-172">輸入釘：</span><span class="sxs-lookup"><span data-stu-id="0e110-172">Input pins:</span></span>

-   <span data-ttu-id="0e110-173">視訊輸入</span><span class="sxs-lookup"><span data-stu-id="0e110-173">Video input</span></span>
-   <span data-ttu-id="0e110-174">子圖片輸入</span><span class="sxs-lookup"><span data-stu-id="0e110-174">Subpicture input</span></span>

<span data-ttu-id="0e110-175">輸出圖釘：</span><span class="sxs-lookup"><span data-stu-id="0e110-175">Output pins:</span></span>

-   <span data-ttu-id="0e110-176">視訊輸出</span><span class="sxs-lookup"><span data-stu-id="0e110-176">Video output</span></span>
-   <span data-ttu-id="0e110-177">行21輸出</span><span class="sxs-lookup"><span data-stu-id="0e110-177">Line-21 output</span></span>
-   <span data-ttu-id="0e110-178">子圖片輸出</span><span class="sxs-lookup"><span data-stu-id="0e110-178">Subpicture output</span></span>

<span data-ttu-id="0e110-179">篩選不會建立子圖片輸出 pin，除非影片輸入 pin 與媒體 **\_ \_ 加密 \_ 套件** 媒體類型連線。</span><span class="sxs-lookup"><span data-stu-id="0e110-179">The filter does not create the subpicture output pin unless the video input pin is connected with a **MEDIATYPE\_DVD\_ENCRYPTED\_PACK** media type.</span></span>

### <a name="mpeg-12-support"></a><span data-ttu-id="0e110-180">MPEG 1/2 支援</span><span class="sxs-lookup"><span data-stu-id="0e110-180">MPEG-1/2 Support</span></span>

<span data-ttu-id="0e110-181">若為 MPEG 1 和 MPEG-2，此解碼器支援下列格式：</span><span class="sxs-lookup"><span data-stu-id="0e110-181">For MPEG-1 and MPEG-2, the decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e110-182">設定檔/層級</span><span class="sxs-lookup"><span data-stu-id="0e110-182">Profiles/Levels</span></span></td>
<td><span data-ttu-id="0e110-183">下列設定檔和層級的任意組合：</span><span class="sxs-lookup"><span data-stu-id="0e110-183">Any combination of the following profiles and levels:</span></span><br/>
<ul>
<li><span data-ttu-id="0e110-184">設定檔：簡單、主要</span><span class="sxs-lookup"><span data-stu-id="0e110-184">Profiles: Simple, Main</span></span></li>
<li><span data-ttu-id="0e110-185">層級：低、主要、高、高1440</span><span class="sxs-lookup"><span data-stu-id="0e110-185">Levels: Low, Main, High, High 1440</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e110-186">色度格式</span><span class="sxs-lookup"><span data-stu-id="0e110-186">Chroma Formats</span></span></td>
<td><span data-ttu-id="0e110-187">4:2:0 色度</span><span class="sxs-lookup"><span data-stu-id="0e110-187">4:2:0 chroma</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e110-188">最大解析度</span><span class="sxs-lookup"><span data-stu-id="0e110-188">Maximum Resolution</span></span></td>
<td><span data-ttu-id="0e110-189">1920×1088圖元</span><span class="sxs-lookup"><span data-stu-id="0e110-189">1920 × 1088 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e110-190">DXVA</span><span class="sxs-lookup"><span data-stu-id="0e110-190">DXVA</span></span></td>
<td><span data-ttu-id="0e110-191">此解碼器支援 DirectX Video 加速 (DXVA) 第1版和第2版。</span><span class="sxs-lookup"><span data-stu-id="0e110-191">The decoder supports DirectX Video Acceleration (DXVA) version 1 and version 2.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0e110-192">此解碼器不支援可調整的 bitstreams。</span><span class="sxs-lookup"><span data-stu-id="0e110-192">The decoder does not support scalable bitstreams.</span></span> <span data-ttu-id="0e110-193">輸入必須是基本影片串流。</span><span class="sxs-lookup"><span data-stu-id="0e110-193">The input must be an elementary video stream.</span></span>

<span data-ttu-id="0e110-194">此解碼器不支援4:2:2 色度格式。</span><span class="sxs-lookup"><span data-stu-id="0e110-194">The decoder does not support 4:2:2 chroma formats.</span></span>

### <a name="h264-support"></a><span data-ttu-id="0e110-195">H.264 支援</span><span class="sxs-lookup"><span data-stu-id="0e110-195">H.264 Support</span></span>

<span data-ttu-id="0e110-196">針對 h.264，此解碼器支援下列格式：</span><span class="sxs-lookup"><span data-stu-id="0e110-196">For H.264, the decoder supports the following formats:</span></span>



| <span data-ttu-id="0e110-197">需求</span><span class="sxs-lookup"><span data-stu-id="0e110-197">Requirement</span></span> | <span data-ttu-id="0e110-198">值</span><span class="sxs-lookup"><span data-stu-id="0e110-198">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e110-199">設定檔/層級</span><span class="sxs-lookup"><span data-stu-id="0e110-199">Profiles/Levels</span></span>    | <span data-ttu-id="0e110-200">基準、主要和高設定檔，最高到層級5.1。</span><span class="sxs-lookup"><span data-stu-id="0e110-200">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="0e110-201"> (如需詳細資料，請參閱 ITU-T h.264 規格。 ) </span><span class="sxs-lookup"><span data-stu-id="0e110-201">(See ITU-T H.264 specification for details.)</span></span>                                                                                                                                                                          |
| <span data-ttu-id="0e110-202">色度格式</span><span class="sxs-lookup"><span data-stu-id="0e110-202">Chroma Formats</span></span>     | <span data-ttu-id="0e110-203">4:2:0 色度或單色</span><span class="sxs-lookup"><span data-stu-id="0e110-203">4:2:0 chroma or monochrome</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="0e110-204">最低解析度</span><span class="sxs-lookup"><span data-stu-id="0e110-204">Minimum Resolution</span></span> | <span data-ttu-id="0e110-205">48×48圖元</span><span class="sxs-lookup"><span data-stu-id="0e110-205">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="0e110-206">最大解析度</span><span class="sxs-lookup"><span data-stu-id="0e110-206">Maximum Resolution</span></span> | <span data-ttu-id="0e110-207">1920×1088圖元</span><span class="sxs-lookup"><span data-stu-id="0e110-207">1920 × 1088 pixels</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="0e110-208">DXVA</span><span class="sxs-lookup"><span data-stu-id="0e110-208">DXVA</span></span>               | <span data-ttu-id="0e110-209">此解碼器支援 DXVA 第2版，但不支援 DXVA 第1版。</span><span class="sxs-lookup"><span data-stu-id="0e110-209">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="0e110-210">只有主要相容的基準、主要和高設定檔 bitstreams 才支援 DXVA 解碼。</span><span class="sxs-lookup"><span data-stu-id="0e110-210">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="0e110-211"> (主要相容的基準 bitstreams 定義為 **設定檔 \_ idc**= 66，且 **限制 \_ set1 \_ 旗** 標 = 1。 ) </span><span class="sxs-lookup"><span data-stu-id="0e110-211">(Main-compatible Baseline bitstreams are defined as **profile\_idc**=66 and **constrained\_set1\_flag**=1.)</span></span> |



 

<span data-ttu-id="0e110-212">此解碼器不支援電影細微性技術。</span><span class="sxs-lookup"><span data-stu-id="0e110-212">The decoder does not support Film Grain Technology.</span></span>

<span data-ttu-id="0e110-213">如需有關 h.264 媒體類型的詳細資訊，請參閱 h.264 [影片類型](h-264-video-types.md)。</span><span class="sxs-lookup"><span data-stu-id="0e110-213">For information about the H.264 media types, see [H.264 Video Types](h-264-video-types.md).</span></span>

### <a name="codec-properties"></a><span data-ttu-id="0e110-214">編解碼器屬性</span><span class="sxs-lookup"><span data-stu-id="0e110-214">Codec Properties</span></span>

<span data-ttu-id="0e110-215">輸入 pin 支援下列透過 [**IKsPropertySet**](ikspropertyset.md)的屬性集：</span><span class="sxs-lookup"><span data-stu-id="0e110-215">The input pins support the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="0e110-216">**DVD 禁止複製屬性集**</span><span class="sxs-lookup"><span data-stu-id="0e110-216">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="0e110-217">[**DVD 子圖片屬性集**](dvd-subpicture-property-set.md) (僅子圖片 pin) </span><span class="sxs-lookup"><span data-stu-id="0e110-217">[**DVD Subpicture Property Set**](dvd-subpicture-property-set.md) (subpicture pin only)</span></span>

<span data-ttu-id="0e110-218">輸入 pin 透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="0e110-218">The input pins support the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="0e110-219">屬性</span><span class="sxs-lookup"><span data-stu-id="0e110-219">Property</span></span>                                                                  | <span data-ttu-id="0e110-220">需要</span><span class="sxs-lookup"><span data-stu-id="0e110-220">Requires</span></span>      |
|---------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="0e110-221">**AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="0e110-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md)         | <span data-ttu-id="0e110-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e110-222">Windows Vista</span></span> |
| [<span data-ttu-id="0e110-223">**AVDecVideoInputScanType**</span><span class="sxs-lookup"><span data-stu-id="0e110-223">**AVDecVideoInputScanType**</span></span>](avdecvideoinputscantype-property.md)       | <span data-ttu-id="0e110-224">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e110-224">Windows Vista</span></span> |
| [<span data-ttu-id="0e110-225">**AVDecVideoPixelAspectRatio**</span><span class="sxs-lookup"><span data-stu-id="0e110-225">**AVDecVideoPixelAspectRatio**</span></span>](avdecvideopixelaspectratio-property.md) | <span data-ttu-id="0e110-226">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e110-226">Windows Vista</span></span> |



 

<span data-ttu-id="0e110-227">篩選準則透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)支援下列屬性：</span><span class="sxs-lookup"><span data-stu-id="0e110-227">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="0e110-228">屬性</span><span class="sxs-lookup"><span data-stu-id="0e110-228">Property</span></span>                                                                                | <span data-ttu-id="0e110-229">需要</span><span class="sxs-lookup"><span data-stu-id="0e110-229">Requires</span></span>      |
|-----------------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="0e110-230">**AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="0e110-230">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                          | <span data-ttu-id="0e110-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e110-231">Windows Vista</span></span> |
| [<span data-ttu-id="0e110-232">**AVDecVideoAcceleration \_ H264**</span><span class="sxs-lookup"><span data-stu-id="0e110-232">**AVDecVideoAcceleration\_H264**</span></span>](avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="0e110-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e110-233">Windows 7</span></span>     |
| [<span data-ttu-id="0e110-234">**AVDecVideoAcceleration \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="0e110-234">**AVDecVideoAcceleration\_MPEG2**</span></span>](avdecvideoacceleration-mpeg2-property.md)          | <span data-ttu-id="0e110-235">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e110-235">Windows 7</span></span>     |
| [<span data-ttu-id="0e110-236">**AVDecVideoDropPicWithMissingRef**</span><span class="sxs-lookup"><span data-stu-id="0e110-236">**AVDecVideoDropPicWithMissingRef**</span></span>](avdecvideodroppicwithmissingref-property.md)     | <span data-ttu-id="0e110-237">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e110-237">Windows 7</span></span>     |
| [<span data-ttu-id="0e110-238">**AVDecVideoFastDecodeMode**</span><span class="sxs-lookup"><span data-stu-id="0e110-238">**AVDecVideoFastDecodeMode**</span></span>](avdecvideofastdecodemode.md)                            | <span data-ttu-id="0e110-239">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e110-239">Windows 7</span></span>     |
| [<span data-ttu-id="0e110-240">**AVDecVideoImageSize**</span><span class="sxs-lookup"><span data-stu-id="0e110-240">**AVDecVideoImageSize**</span></span>](avdecvideoimagesize.md)                                      | <span data-ttu-id="0e110-241">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e110-241">Windows 7</span></span>     |
| [<span data-ttu-id="0e110-242">**AVDecVideoSoftwareDeinterlaceMode**</span><span class="sxs-lookup"><span data-stu-id="0e110-242">**AVDecVideoSoftwareDeinterlaceMode**</span></span>](avdecvideosoftwaredeinterlacemode-property.md) | <span data-ttu-id="0e110-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e110-243">Windows 7</span></span>     |
| [<span data-ttu-id="0e110-244">**AVDecVideoThumbnailGenerationMode**</span><span class="sxs-lookup"><span data-stu-id="0e110-244">**AVDecVideoThumbnailGenerationMode**</span></span>](avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="0e110-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e110-245">Windows 7</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="0e110-246">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e110-246">Requirements</span></span>



| <span data-ttu-id="0e110-247">需求</span><span class="sxs-lookup"><span data-stu-id="0e110-247">Requirement</span></span> | <span data-ttu-id="0e110-248">值</span><span class="sxs-lookup"><span data-stu-id="0e110-248">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e110-249">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e110-249">Minimum supported client</span></span><br/> | <span data-ttu-id="0e110-250">Windows Vista Home Premium、Windows Vista 旗艦版、Windows 7 Home Premium、Windows 7 Professional、Windows 7 企業版、僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e110-250">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0e110-251">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e110-251">Minimum supported server</span></span><br/> | <span data-ttu-id="0e110-252">都不支援</span><span class="sxs-lookup"><span data-stu-id="0e110-252">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="0e110-253">標頭</span><span class="sxs-lookup"><span data-stu-id="0e110-253">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e110-254"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e110-254"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="0e110-255">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e110-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e110-256">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="0e110-256">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="0e110-257">**DVD 媒體類型**</span><span class="sxs-lookup"><span data-stu-id="0e110-257">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> <dt>

[<span data-ttu-id="0e110-258">H.264 影片類型</span><span class="sxs-lookup"><span data-stu-id="0e110-258">H.264 Video Types</span></span>](h-264-video-types.md)
</dt> </dl>

 

 
