---
description: 媒體基礎 h.264 視頻編碼程式是一種媒體基礎轉換，支援基準、主要和高設定檔的解碼，最多可達層級5.1。
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: H.264 Video 解碼
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468613"
---
# <a name="h264-video-decoder"></a><span data-ttu-id="6b529-103">H.264 Video 解碼</span><span class="sxs-lookup"><span data-stu-id="6b529-103">H.264 Video Decoder</span></span>

<span data-ttu-id="6b529-104">媒體基礎 h.264 視頻編碼程式是一種 [媒體基礎轉換](media-foundation-transforms.md) ，支援基準、主要和高設定檔的解碼，最多可達層級5.1。</span><span class="sxs-lookup"><span data-stu-id="6b529-104">The Media Foundation H.264 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding of Baseline, Main, and High profiles, up to level 5.1.</span></span>

<span data-ttu-id="6b529-105">H.264 video 解碼會公開下列介面。</span><span class="sxs-lookup"><span data-stu-id="6b529-105">The H.264 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="6b529-106">Windows 8) 支援的 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (</span><span class="sxs-lookup"><span data-stu-id="6b529-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="6b529-107">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="6b529-107">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="6b529-108">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="6b529-108">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="6b529-109">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="6b529-109">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="6b529-110">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="6b529-110">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="6b529-111">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="6b529-111">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="6b529-112">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="6b529-112">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="6b529-113">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="6b529-113">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="6b529-114">若要建立此解碼器的實例，請執行下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="6b529-114">To create an instance of the decoder, do one of the following:</span></span>

-   <span data-ttu-id="6b529-115">呼叫 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 或 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數。</span><span class="sxs-lookup"><span data-stu-id="6b529-115">Call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>
-   <span data-ttu-id="6b529-116">呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)。</span><span class="sxs-lookup"><span data-stu-id="6b529-116">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="6b529-117">此解碼器的 CLSID 是 **clsid \_ CMSH264DecoderMFT**，宣告于 wmcodecdsp 中。</span><span class="sxs-lookup"><span data-stu-id="6b529-117">The CLSID for the decoder is **CLSID\_CMSH264DecoderMFT**, declared in wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="6b529-118">輸入類型</span><span class="sxs-lookup"><span data-stu-id="6b529-118">Input Types</span></span>

<span data-ttu-id="6b529-119">輸入類型必須至少包含下列兩個屬性：</span><span class="sxs-lookup"><span data-stu-id="6b529-119">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="6b529-120">屬性</span><span class="sxs-lookup"><span data-stu-id="6b529-120">Attribute</span></span>                                                 | <span data-ttu-id="6b529-121">描述</span><span class="sxs-lookup"><span data-stu-id="6b529-121">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b529-122">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6b529-122">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="6b529-123">**MFMediaType \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="6b529-123">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="6b529-124">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="6b529-124">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="6b529-125">[MFVideoFormat \_H264](video-subtype-guids.md) 或 MFVideoFormat \_ h264 \_ ES</span><span class="sxs-lookup"><span data-stu-id="6b529-125">[MFVideoFormat\_H264](video-subtype-guids.md) or MFVideoFormat\_H264\_ES</span></span> |



 

<span data-ttu-id="6b529-126">如果輸入類型只包含這兩個屬性，則此解碼器將提供預設輸出類型，作為預留位置。</span><span class="sxs-lookup"><span data-stu-id="6b529-126">If the input type contains only these two attributes, the decoder will offer a default output type, which acts as a placeholder.</span></span> <span data-ttu-id="6b529-127">當解碼器收到足夠的輸入樣本來產生輸出框架時，它會從 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)傳回 **MF \_ E \_ 轉換 \_ 串流 \_ 變更**，以發出格式變更的信號。</span><span class="sxs-lookup"><span data-stu-id="6b529-127">When the decoder receives enough input samples to produce an output frame, it signals a format change by returning **MF\_E\_TRANSFORM\_STREAM\_CHANGE** from [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="6b529-128">如需處理格式變更的詳細資訊，請參閱 **ProcessOutput** 檔。</span><span class="sxs-lookup"><span data-stu-id="6b529-128">See the **ProcessOutput** documentation for details about handling format changes.</span></span>

<span data-ttu-id="6b529-129">若要避免初始格式變更，請盡可能在輸入類型中提供最多資訊，包括：</span><span class="sxs-lookup"><span data-stu-id="6b529-129">To avoid an initial format change, provide as much information in the input type as possible, including:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b529-130">屬性</span><span class="sxs-lookup"><span data-stu-id="6b529-130">Attribute</span></span></th>
<th><span data-ttu-id="6b529-131">描述</span><span class="sxs-lookup"><span data-stu-id="6b529-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b529-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b529-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="6b529-133">畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="6b529-133">Frame rate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b529-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b529-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="6b529-135">框架維度。</span><span class="sxs-lookup"><span data-stu-id="6b529-135">Frame dimensions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b529-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b529-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="6b529-137">交錯模式。</span><span class="sxs-lookup"><span data-stu-id="6b529-137">Interlace mode.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="6b529-138">在 h.264 video 中，交錯結構可以動態變更，因此會 <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>這個屬性的建議值。</span><span class="sxs-lookup"><span data-stu-id="6b529-138">In H.264 video, the interlace structure can change dynamically, so the recommended value of this attribute is <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>.</span></span> <span data-ttu-id="6b529-139">影片基本資料流程中的交錯資訊優先于媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6b529-139">Interlace information in the video elementary stream takes precedence over the media type.</span></span> <span data-ttu-id="6b529-140">如需詳細資訊，請參閱 <a href="video-interlacing.md">影片交錯</a>。</span><span class="sxs-lookup"><span data-stu-id="6b529-140">For more information, see <a href="video-interlacing.md">Video Interlacing</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b529-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b529-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="6b529-142">圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="6b529-142">Pixel aspect ratio.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6b529-143">輸入類型必須在輸出類型之前設定。</span><span class="sxs-lookup"><span data-stu-id="6b529-143">The input type must be set before the output type.</span></span> <span data-ttu-id="6b529-144">在設定輸入類型之前，編碼器的 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 方法會傳回 **\_ \_ \_ \_ 未 \_ 設定的 MF E 轉換類型**。</span><span class="sxs-lookup"><span data-stu-id="6b529-144">Until the input type is set, the encoder's [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="6b529-145">輸出型別</span><span class="sxs-lookup"><span data-stu-id="6b529-145">Output Types</span></span>

<span data-ttu-id="6b529-146">此解碼器支援下列輸出子類型：</span><span class="sxs-lookup"><span data-stu-id="6b529-146">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="6b529-147">**MFVideoFormat \_ I420**</span><span class="sxs-lookup"><span data-stu-id="6b529-147">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="6b529-148">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="6b529-148">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="6b529-149">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="6b529-149">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="6b529-150">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="6b529-150">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="6b529-151">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="6b529-151">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="6b529-152">如需這些子類型的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="6b529-152">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="6b529-153">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="6b529-153">Transform Attributes</span></span>

<span data-ttu-id="6b529-154">H.264 解碼會實行 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。</span><span class="sxs-lookup"><span data-stu-id="6b529-154">The H.264 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="6b529-155">應用程式可以使用這個方法來取得或設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="6b529-155">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="6b529-156">屬性</span><span class="sxs-lookup"><span data-stu-id="6b529-156">Attribute</span></span>                                                                                       | <span data-ttu-id="6b529-157">描述</span><span class="sxs-lookup"><span data-stu-id="6b529-157">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b529-158">CODECAPI \_ AVDecVideoAcceleration \_ H264</span><span class="sxs-lookup"><span data-stu-id="6b529-158">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="6b529-159">啟用或停用硬體加速。</span><span class="sxs-lookup"><span data-stu-id="6b529-159">Enables or disables hardware acceleration.</span></span>                                                 |
| [<span data-ttu-id="6b529-160">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="6b529-160">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="6b529-161">啟用或停用縮圖產生模式。</span><span class="sxs-lookup"><span data-stu-id="6b529-161">Enables or disables thumbnail generation mode.</span></span>                                             |
| [<span data-ttu-id="6b529-162">MF \_ SA \_ D3D \_ 感知</span><span class="sxs-lookup"><span data-stu-id="6b529-162">MF\_SA\_D3D\_AWARE</span></span>](mf-sa-d3d-aware-attribute.md)                                             | <span data-ttu-id="6b529-163">指出此解碼器支援 (DXVA) 的 DirectX Video 加速。</span><span class="sxs-lookup"><span data-stu-id="6b529-163">Indicates that the decoder supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="6b529-164">視為唯讀。</span><span class="sxs-lookup"><span data-stu-id="6b529-164">Treat as read-only.</span></span> |



 

<span data-ttu-id="6b529-165">在 Windows 8 中，h.264 解碼器也支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="6b529-165">In Windows 8, the H.264 decoder also supports the following attributes.</span></span>



| <span data-ttu-id="6b529-166">屬性</span><span class="sxs-lookup"><span data-stu-id="6b529-166">Attribute</span></span>                                                                                                     | <span data-ttu-id="6b529-167">描述</span><span class="sxs-lookup"><span data-stu-id="6b529-167">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b529-168">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="6b529-168">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="6b529-169">啟用或停用低延遲解碼模式。</span><span class="sxs-lookup"><span data-stu-id="6b529-169">Enables or disables low-latency decoding mode.</span></span>                                                              |
| [<span data-ttu-id="6b529-170">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="6b529-170">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                                         | <span data-ttu-id="6b529-171">設定用於此解碼器的背景工作執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="6b529-171">Sets the number of worker threads used by the decoder.</span></span>                                                      |
| [<span data-ttu-id="6b529-172">CODECAPI \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="6b529-172">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)                                     | <span data-ttu-id="6b529-173">設定解碼器將接受做為輸入類型的最大圖片寬度。</span><span class="sxs-lookup"><span data-stu-id="6b529-173">Sets the maximum picture width that the decoder will accept as an input type.</span></span>                               |
| [<span data-ttu-id="6b529-174">CODECAPI \_ AVDecVideoMaxCodedHeight</span><span class="sxs-lookup"><span data-stu-id="6b529-174">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)                                   | <span data-ttu-id="6b529-175">設定解碼器將接受做為輸入類型的最大圖片高度。</span><span class="sxs-lookup"><span data-stu-id="6b529-175">Sets the maximum picture height that the decoder will accept as an input type.</span></span>                              |
| [<span data-ttu-id="6b529-176">MF \_ SA \_ 最小 \_ 輸出 \_ 範例 \_ 計數</span><span class="sxs-lookup"><span data-stu-id="6b529-176">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                               | <span data-ttu-id="6b529-177">指定輸出樣本的最大數目。</span><span class="sxs-lookup"><span data-stu-id="6b529-177">Specifies the maximum number of output samples.</span></span>                                                             |
| [<span data-ttu-id="6b529-178">MFT \_ 解碼 \_ 會 \_ \_ \_ 以 \_ 原生 \_ 順序公開輸出類型</span><span class="sxs-lookup"><span data-stu-id="6b529-178">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="6b529-179">指定解碼器是否公開 IYUV/I420 輸出類型 (適用于其他格式之前的轉碼) 。</span><span class="sxs-lookup"><span data-stu-id="6b529-179">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span> |



 

<span data-ttu-id="6b529-180">在 Windows 8 中，h.264 解碼支援 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面。</span><span class="sxs-lookup"><span data-stu-id="6b529-180">In Windows 8, the H.264 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="6b529-181">此介面提供 alternativate API 來設定下列編解碼器屬性。</span><span class="sxs-lookup"><span data-stu-id="6b529-181">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="6b529-182">CODECAPI \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="6b529-182">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="6b529-183">CODECAPI \_ AVDecVideoAcceleration \_ H264</span><span class="sxs-lookup"><span data-stu-id="6b529-183">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)
-   [<span data-ttu-id="6b529-184">CODECAPI \_ AVDecVideoMaxCodedHeight</span><span class="sxs-lookup"><span data-stu-id="6b529-184">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)
-   [<span data-ttu-id="6b529-185">CODECAPI \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="6b529-185">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="6b529-186">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="6b529-186">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a><span data-ttu-id="6b529-187">格式條件約束</span><span class="sxs-lookup"><span data-stu-id="6b529-187">Format Constraints</span></span>

<span data-ttu-id="6b529-188">此解碼器支援下列格式：</span><span class="sxs-lookup"><span data-stu-id="6b529-188">The decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b529-189">設定檔/層級</span><span class="sxs-lookup"><span data-stu-id="6b529-189">Profiles/Levels</span></span></td>
<td><span data-ttu-id="6b529-190">基準、主要和高設定檔，最高到層級5.1。</span><span class="sxs-lookup"><span data-stu-id="6b529-190">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="6b529-191"> (如需詳細資料，請參閱 ITU-T h.264 規格。 ) </span><span class="sxs-lookup"><span data-stu-id="6b529-191">(See ITU-T H.264 specification for details.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b529-192">色度格式</span><span class="sxs-lookup"><span data-stu-id="6b529-192">Chroma Formats</span></span></td>
<td><span data-ttu-id="6b529-193">4:2:0 色度或單色</span><span class="sxs-lookup"><span data-stu-id="6b529-193">4:2:0 chroma or monochrome</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b529-194">最低解析度</span><span class="sxs-lookup"><span data-stu-id="6b529-194">Minimum Resolution</span></span></td>
<td><span data-ttu-id="6b529-195">48×48圖元</span><span class="sxs-lookup"><span data-stu-id="6b529-195">48 × 48 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b529-196">最大解析度</span><span class="sxs-lookup"><span data-stu-id="6b529-196">Maximum Resolution</span></span></td>
<td><span data-ttu-id="6b529-197">4096×2304圖元</span><span class="sxs-lookup"><span data-stu-id="6b529-197">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="6b529-198">DXVA 加速的保證解析度上限為1920×1088圖元;在較高的解析度中，解碼是使用 DXVA 來完成（如果基礎硬體支援的話），否則會使用軟體進行解碼。</span><span class="sxs-lookup"><span data-stu-id="6b529-198">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6b529-199">在 Windows 7 中，軟體和 DXVA 解碼的最大支援解析度為1920×1088圖元。</span><span class="sxs-lookup"><span data-stu-id="6b529-199">In Windows 7, the maximum supported resolution is 1920 × 1088 pixels for both software and DXVA decoding.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b529-200">DXVA</span><span class="sxs-lookup"><span data-stu-id="6b529-200">DXVA</span></span></td>
<td><span data-ttu-id="6b529-201">此解碼器支援 DXVA 第2版，但不支援 DXVA 第1版。</span><span class="sxs-lookup"><span data-stu-id="6b529-201">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="6b529-202">只有主要相容的基準、主要和高設定檔 bitstreams 才支援 DXVA 解碼。</span><span class="sxs-lookup"><span data-stu-id="6b529-202">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="6b529-203"> (主要相容的基準 bitstreams 定義為 <strong>profile_idc</strong>= 66， <strong>constrained_set1_flag</strong>= 1。 ) </span><span class="sxs-lookup"><span data-stu-id="6b529-203">(Main-compatible Baseline bitstreams are defined as <strong>profile_idc</strong>=66 and <strong>constrained_set1_flag</strong>=1.)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6b529-204">輸入資料必須符合 ISO/IEC 14496-10 的附錄 B。</span><span class="sxs-lookup"><span data-stu-id="6b529-204">Input data must conform to Annex B of ISO/IEC 14496-10.</span></span> <span data-ttu-id="6b529-205">資料必須包含起始碼。</span><span class="sxs-lookup"><span data-stu-id="6b529-205">The data must include the start codes.</span></span> <span data-ttu-id="6b529-206">除非在位元組資料流程中找到有效的 sequence 參數集 (SPS) 和圖片參數集 (PPS) ，否則此解碼器會略過位元組。</span><span class="sxs-lookup"><span data-stu-id="6b529-206">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

<span data-ttu-id="6b529-207">此解碼器不支援電影細微性技術。</span><span class="sxs-lookup"><span data-stu-id="6b529-207">The decoder does not support Film Grain Technology.</span></span>

> [!Note]  
> <span data-ttu-id="6b529-208">先前版本的檔不正確地指出 Windows Server 2008 R2 支援此解碼器。</span><span class="sxs-lookup"><span data-stu-id="6b529-208">A previous version of the documentation incorrectly stated that the decoder is supported on Windows Server 2008 R2.</span></span>

 

<span data-ttu-id="6b529-209">如果已安裝 Windows Vista 的平臺更新補充，則可以在 Windows Vista 上使用 h.264 video 解碼器，但只能使用 [來源讀取器](source-reader.md)在 windows vista 上進行存取。</span><span class="sxs-lookup"><span data-stu-id="6b529-209">If Platform Update Supplement for Windows Vista is installed, the H.264 video decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b529-210">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b529-210">Requirements</span></span>



| <span data-ttu-id="6b529-211">需求</span><span class="sxs-lookup"><span data-stu-id="6b529-211">Requirement</span></span> | <span data-ttu-id="6b529-212">值</span><span class="sxs-lookup"><span data-stu-id="6b529-212">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b529-213">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b529-213">Minimum supported client</span></span><br/> | <span data-ttu-id="6b529-214">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b529-214">Windows 7 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6b529-215">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b529-215">Minimum supported server</span></span><br/> | <span data-ttu-id="6b529-216">都不支援</span><span class="sxs-lookup"><span data-stu-id="6b529-216">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="6b529-217">DLL</span><span class="sxs-lookup"><span data-stu-id="6b529-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b529-218"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b529-218"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b529-219">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b529-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b529-220">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="6b529-220">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="6b529-221">媒體基礎中的 MPEG 4 支援</span><span class="sxs-lookup"><span data-stu-id="6b529-221">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6b529-222">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="6b529-222">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6b529-223">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="6b529-223">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
