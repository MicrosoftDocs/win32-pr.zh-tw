---
description: Microsoft 媒體基礎 h.264 影片編碼器是支援下列 h.264 設定檔的媒體基礎轉換：
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: H.264 影片編碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5631239e9db0ddf078848bc3c4a04282e7e79990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982288"
---
# <a name="h264-video-encoder"></a><span data-ttu-id="5a043-103">H.264 影片編碼器</span><span class="sxs-lookup"><span data-stu-id="5a043-103">H.264 Video Encoder</span></span>

<span data-ttu-id="5a043-104">Microsoft 媒體基礎 h.264 影片編碼器是支援下列 h.264 設定檔的 [媒體基礎轉換](media-foundation-transforms.md) ：</span><span class="sxs-lookup"><span data-stu-id="5a043-104">The Microsoft Media Foundation H.264 video encoder is a [Media Foundation transform](media-foundation-transforms.md) that supports the following H.264 profiles:</span></span>

-   <span data-ttu-id="5a043-105">基準設定檔</span><span class="sxs-lookup"><span data-stu-id="5a043-105">Baseline Profile</span></span>
-   <span data-ttu-id="5a043-106">主要設定檔</span><span class="sxs-lookup"><span data-stu-id="5a043-106">Main Profile</span></span>
-   <span data-ttu-id="5a043-107">高設定檔 (需要 Windows 8) </span><span class="sxs-lookup"><span data-stu-id="5a043-107">High profile (requires Windows 8)</span></span>

<span data-ttu-id="5a043-108">H.264 video 編碼器會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="5a043-108">The H.264 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="5a043-109">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="5a043-109">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="5a043-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="5a043-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="5a043-111">輸入類型</span><span class="sxs-lookup"><span data-stu-id="5a043-111">Input Types</span></span>

<span data-ttu-id="5a043-112">輸入媒體類型必須有下列其中一個子類型：</span><span class="sxs-lookup"><span data-stu-id="5a043-112">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="5a043-113">**MFVideoFormat_I420**</span><span class="sxs-lookup"><span data-stu-id="5a043-113">**MFVideoFormat_I420**</span></span>
-   <span data-ttu-id="5a043-114">**MFVideoFormat_IYUV**</span><span class="sxs-lookup"><span data-stu-id="5a043-114">**MFVideoFormat_IYUV**</span></span>
-   <span data-ttu-id="5a043-115">**MFVideoFormat_NV12**</span><span class="sxs-lookup"><span data-stu-id="5a043-115">**MFVideoFormat_NV12**</span></span>
-   <span data-ttu-id="5a043-116">**MFVideoFormat_YUY2**</span><span class="sxs-lookup"><span data-stu-id="5a043-116">**MFVideoFormat_YUY2**</span></span>
-   <span data-ttu-id="5a043-117">**MFVideoFormat_YV12**</span><span class="sxs-lookup"><span data-stu-id="5a043-117">**MFVideoFormat_YV12**</span></span>

<span data-ttu-id="5a043-118">如需這些子類型的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="5a043-118">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="5a043-119">輸出類型必須在輸入類型之前設定。</span><span class="sxs-lookup"><span data-stu-id="5a043-119">The output type must be set before the input type.</span></span> <span data-ttu-id="5a043-120">在設定輸出類型之前，編碼器的 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 方法會傳回 **MF_E_TRANSFORM_TYPE_NOT_SET**。</span><span class="sxs-lookup"><span data-stu-id="5a043-120">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF_E_TRANSFORM_TYPE_NOT_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="5a043-121">輸出型別</span><span class="sxs-lookup"><span data-stu-id="5a043-121">Output Types</span></span>

<span data-ttu-id="5a043-122">編碼器支援單一輸出子類型：</span><span class="sxs-lookup"><span data-stu-id="5a043-122">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="5a043-123">**MFVideoFormat_H264**</span><span class="sxs-lookup"><span data-stu-id="5a043-123">**MFVideoFormat_H264**</span></span>

<span data-ttu-id="5a043-124">在輸出媒體類型上設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-124">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a043-125">屬性</span><span class="sxs-lookup"><span data-stu-id="5a043-125">Attribute</span></span></th>
<th><span data-ttu-id="5a043-126">描述</span><span class="sxs-lookup"><span data-stu-id="5a043-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5a043-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a043-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="5a043-128">主要類型。</span><span class="sxs-lookup"><span data-stu-id="5a043-128">Major type.</span></span> <span data-ttu-id="5a043-129">必須是 <strong>MFMediaType_Video</strong>。</span><span class="sxs-lookup"><span data-stu-id="5a043-129">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a043-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a043-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="5a043-131">影片子類型。</span><span class="sxs-lookup"><span data-stu-id="5a043-131">Video subtype.</span></span> <span data-ttu-id="5a043-132">必須是 <strong>MFVideoFormat_H264</strong>。</span><span class="sxs-lookup"><span data-stu-id="5a043-132">Must be <strong>MFVideoFormat_H264</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a043-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a043-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="5a043-134">平均編碼的位速度，以位/秒為單位。</span><span class="sxs-lookup"><span data-stu-id="5a043-134">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="5a043-135">必須大於零。</span><span class="sxs-lookup"><span data-stu-id="5a043-135">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a043-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a043-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="5a043-137">畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="5a043-137">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a043-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a043-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="5a043-139">框架大小。</span><span class="sxs-lookup"><span data-stu-id="5a043-139">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a043-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a043-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="5a043-141">交錯模式。</span><span class="sxs-lookup"><span data-stu-id="5a043-141">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a043-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a043-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span></span></td>
<td><span data-ttu-id="5a043-143">H.264 編碼設定檔。</span><span class="sxs-lookup"><span data-stu-id="5a043-143">H.264 encoding profile.</span></span><br/> <span data-ttu-id="5a043-144">支援的值為：</span><span class="sxs-lookup"><span data-stu-id="5a043-144">The supported values are:</span></span><br/>
<ul>
<li><span data-ttu-id="5a043-145"><strong>eAVEncH264VProfile_Base</strong> (預設) </span><span class="sxs-lookup"><span data-stu-id="5a043-145"><strong>eAVEncH264VProfile_Base</strong> (default)</span></span></li>
<li><span data-ttu-id="5a043-146"><strong>eAVEncH264VProfile_Main</strong></span><span class="sxs-lookup"><span data-stu-id="5a043-146"><strong>eAVEncH264VProfile_Main</strong></span></span></li>
<li><span data-ttu-id="5a043-147"><strong>eAVEncH264VProfile_High</strong> (需要 Windows 8) </span><span class="sxs-lookup"><span data-stu-id="5a043-147"><strong>eAVEncH264VProfile_High</strong> (requires Windows 8)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a043-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a043-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="5a043-149">選擇性。</span><span class="sxs-lookup"><span data-stu-id="5a043-149">Optional.</span></span> <span data-ttu-id="5a043-150">指定 h.264 編碼層級。</span><span class="sxs-lookup"><span data-stu-id="5a043-150">Specifies the H.264 encoding level.</span></span><br/> <span data-ttu-id="5a043-151">預設值為–1，表示編碼器將選取編碼層級。</span><span class="sxs-lookup"><span data-stu-id="5a043-151">The default value is –1, indicating that the encoder will select the encoding level.</span></span><br/> <span data-ttu-id="5a043-152">建議不要設定媒體類型中的層級，並允許編碼器選取層級。</span><span class="sxs-lookup"><span data-stu-id="5a043-152">It is recommended not to set the level in the media type, and allow the encoder to select the level.</span></span> <span data-ttu-id="5a043-153">編碼器可以針對指定的影片串流衍生適當的層級，並考慮影片的格式限制和特性。</span><span class="sxs-lookup"><span data-stu-id="5a043-153">The encoder can derive the proper level for a given video stream, taking into account the format constraints and the characteristics of the video.</span></span> <span data-ttu-id="5a043-154">如需有關設定檔和層級條件約束的詳細資訊，請參閱 ITU-T H. h.264 的附錄 A。</span><span class="sxs-lookup"><span data-stu-id="5a043-154">For more information about profile and level constraints, refer to Annex A of ITU-T H.264.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a043-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a043-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="5a043-156">選擇性。</span><span class="sxs-lookup"><span data-stu-id="5a043-156">Optional.</span></span> <span data-ttu-id="5a043-157">指定圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="5a043-157">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="5a043-158">預設值為1:1。</span><span class="sxs-lookup"><span data-stu-id="5a043-158">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5a043-159">設定輸出類型之後，影片編碼器會藉由新增 [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) 屬性來更新類型。</span><span class="sxs-lookup"><span data-stu-id="5a043-159">After the output type is set, the video encoder updates the type by adding the [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="5a043-160">此屬性包含 sequence 標頭。</span><span class="sxs-lookup"><span data-stu-id="5a043-160">This attribute contains the sequence header.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="5a043-161">編解碼器屬性</span><span class="sxs-lookup"><span data-stu-id="5a043-161">Codec Properties</span></span>

<span data-ttu-id="5a043-162">H.264 編碼器會實 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面來設定編碼參數。</span><span class="sxs-lookup"><span data-stu-id="5a043-162">The H.264 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="5a043-163">它支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-163">It supports the following properties.</span></span>

<span data-ttu-id="5a043-164">如需 HCK 編碼器認證的編解碼器需求，請參閱下面的「 **經認證的硬體編碼器** 」一節。</span><span class="sxs-lookup"><span data-stu-id="5a043-164">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>

<span data-ttu-id="5a043-165">以下是 Windows 7 中支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-165">The following properties are supported in Windows 7.</span></span>



| <span data-ttu-id="5a043-166">屬性</span><span class="sxs-lookup"><span data-stu-id="5a043-166">Property</span></span>                                                                              | <span data-ttu-id="5a043-167">描述</span><span class="sxs-lookup"><span data-stu-id="5a043-167">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a043-168">**CODECAPI_AVEncCommonRateControlMode**</span><span class="sxs-lookup"><span data-stu-id="5a043-168">**CODECAPI_AVEncCommonRateControlMode**</span></span>](../directshow/avenccommonratecontrolmode-property.md) | <span data-ttu-id="5a043-169">設定速率控制模式。</span><span class="sxs-lookup"><span data-stu-id="5a043-169">Sets the rate control mode.</span></span> <span data-ttu-id="5a043-170">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="5a043-170">See Remarks.</span></span> <span data-ttu-id="5a043-171">預設模式是 (VBR) 的無限制變數位元速率。</span><span class="sxs-lookup"><span data-stu-id="5a043-171">The default mode is unconstrained variable bit rate (VBR).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="5a043-172">**CODECAPI_AVEncCommonQuality**</span><span class="sxs-lookup"><span data-stu-id="5a043-172">**CODECAPI_AVEncCommonQuality**</span></span>](../directshow/avenccommonquality-property.md)                 | <span data-ttu-id="5a043-173">設定品質等級。</span><span class="sxs-lookup"><span data-stu-id="5a043-173">Sets the quality level.</span></span> <span data-ttu-id="5a043-174">當速率控制模式是以品質為基礎的 VBR (**eAVEncCommonRateControlMode_Quality**) 時，就會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-174">This property applies when the rate control mode is quality-based VBR (**eAVEncCommonRateControlMode_Quality**).</span></span> <span data-ttu-id="5a043-175">有效範圍是1–100。</span><span class="sxs-lookup"><span data-stu-id="5a043-175">The valid range is 1–100.</span></span> <span data-ttu-id="5a043-176">預設值為70。</span><span class="sxs-lookup"><span data-stu-id="5a043-176">The default value is 70.</span></span> <br/> <span data-ttu-id="5a043-177">若要設定此參數，請在呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)之前設定屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-177">To set this parameter, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <br/> <span data-ttu-id="5a043-178">若要在 Windows 7 中設定此參數，請在呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)之前設定屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-178">To set this parameter in Windows 7, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="5a043-179">編碼器會在設定輸出類型之後忽略變更。</span><span class="sxs-lookup"><span data-stu-id="5a043-179">The encoder ignores changes after the output type is set.</span></span> <br/> <span data-ttu-id="5a043-180">在 Windows 8 中，您可以在編碼期間隨時設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-180">In Windows 8, this property can be set at any time during encoding.</span></span> <span data-ttu-id="5a043-181">從下一個輸入畫面格開始套用變更。</span><span class="sxs-lookup"><span data-stu-id="5a043-181">Changes are applied starting at the next input frame.</span></span> <br/> <span data-ttu-id="5a043-182">編碼器會在內部將此屬性轉換成 [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) 值。</span><span class="sxs-lookup"><span data-stu-id="5a043-182">Internally, the encoder converts this property to an [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) value.</span></span> <br/> |



 

<span data-ttu-id="5a043-183">下列屬性需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="5a043-183">The following properties require Windows 8.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a043-184">屬性</span><span class="sxs-lookup"><span data-stu-id="5a043-184">Property</span></span></th>
<th><span data-ttu-id="5a043-185">描述</span><span class="sxs-lookup"><span data-stu-id="5a043-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5a043-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span><span class="sxs-lookup"><span data-stu-id="5a043-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span></span></td>
<td><span data-ttu-id="5a043-187">設定適應性編碼模式。</span><span class="sxs-lookup"><span data-stu-id="5a043-187">Sets the adaptive encoding mode.</span></span> <span data-ttu-id="5a043-188">在 Windows 8 中，h.264 編碼器支援下列模式：</span><span class="sxs-lookup"><span data-stu-id="5a043-188">The H.264 encoder supports the following modes in Windows 8:</span></span>
<ul>
<li><span data-ttu-id="5a043-189"><strong>eAVEncAdaptiveMode_None</strong>。</span><span class="sxs-lookup"><span data-stu-id="5a043-189"><strong>eAVEncAdaptiveMode_None</strong>.</span></span> <span data-ttu-id="5a043-190">無適應性編碼。</span><span class="sxs-lookup"><span data-stu-id="5a043-190">No adaptive encoding.</span></span> <span data-ttu-id="5a043-191">(預設值。)</span><span class="sxs-lookup"><span data-stu-id="5a043-191">(Default.)</span></span></li>
<li><span data-ttu-id="5a043-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>。</span><span class="sxs-lookup"><span data-stu-id="5a043-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span></span> <span data-ttu-id="5a043-193">自我調整變更畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="5a043-193">Adaptively change the frame rate.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a043-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="5a043-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="5a043-195">以位元組為單位，設定常數速率的緩衝區大小（以位元組為單位） (CBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="5a043-195">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="5a043-196">有效範圍為 [1 .。。2³²-1]。</span><span class="sxs-lookup"><span data-stu-id="5a043-196">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="5a043-197">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="5a043-197">Requires Windows 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a043-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="5a043-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="5a043-199">針對 [受條件約束的 VBR 編碼]，指定 &quot; 有漏洞 bucket 的清空速率 &quot; （以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="5a043-199">For constrained VBR encoding, specifies the rate at which the &quot;leaky bucket&quot; is drained, in bits per second.</span></span> <span data-ttu-id="5a043-200">當速率控制模式 <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>時，就會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-200">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>.</span></span> <br/> <span data-ttu-id="5a043-201">有效範圍為 [1 .。。2³²-1]。</span><span class="sxs-lookup"><span data-stu-id="5a043-201">The valid range is [1 ... 2³²–1].</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a043-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="5a043-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="5a043-203">設定編碼位資料流程的平均位元速率，以每秒位數為單位。</span><span class="sxs-lookup"><span data-stu-id="5a043-203">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <span data-ttu-id="5a043-204">如果 <strong>eAVEncCommonRateControlMode_Quality</strong>的速率控制模式，則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-204">This property is ignored if the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="5a043-205">有效範圍為 [1 .。。2³²-1]。</span><span class="sxs-lookup"><span data-stu-id="5a043-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="5a043-206">在 CBR 和未受限制的 VBR 模式中，平均位元速率會決定檔案的最終大小。</span><span class="sxs-lookup"><span data-stu-id="5a043-206">In CBR and unconstrained VBR modes, the average bit rate determines the final size of the file.</span></span> <span data-ttu-id="5a043-207">在 CBR 模式中，平均位元速率也是壓縮的位從有漏洞值區中排出的速率 &quot; 。 &quot; (如需詳細資訊，請參閱 <a href="the-leaky-bucket-buffer-model.md">有漏洞 bucket 緩衝區模型</a>。 ) </span><span class="sxs-lookup"><span data-stu-id="5a043-207">In CBR mode, the average bit rate is also the rate at which compressed bits are drained from the &quot;leaky bucket.&quot; (For more information, see <a href="the-leaky-bucket-buffer-model.md">The Leaky Bucket Buffer Model</a>.)</span></span> <br/> <span data-ttu-id="5a043-208">在 Windows 7 中，平均位元速率是由媒體類型上的 <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="5a043-208">In Windows 7, the average bit rate is specified by the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute on the media type.</span></span> <br/> <span data-ttu-id="5a043-209">在 Windows 8 中，您可以使用 <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> 屬性或 <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> 屬性來設定平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="5a043-209">In Windows 8, you can set the average bit rate using either the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute or the <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> property.</span></span> <span data-ttu-id="5a043-210">如果兩者都已設定，CODECAPI_AVEncCommonMeanBitRate 覆寫。</span><span class="sxs-lookup"><span data-stu-id="5a043-210">If both are set, CODECAPI_AVEncCommonMeanBitRate overrides.</span></span> <span data-ttu-id="5a043-211">在 Windows 8 中，您可以設定編碼期間的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="5a043-211">In Windows 8, you can set the average bit rate during encoding.</span></span> <span data-ttu-id="5a043-212">如果位元速率有所變更，則編碼器會使用適應性編碼。</span><span class="sxs-lookup"><span data-stu-id="5a043-212">If the bit rate changes, the encoder uses adaptive encoding.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a043-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="5a043-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="5a043-214">設定品質/速度的取捨。</span><span class="sxs-lookup"><span data-stu-id="5a043-214">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="5a043-215">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="5a043-215">Valid range:</span></span>
<ul>
<li><span data-ttu-id="5a043-216">0-33：低複雜度</span><span class="sxs-lookup"><span data-stu-id="5a043-216">0–33: Low complexity</span></span></li>
<li><span data-ttu-id="5a043-217">34–66：中等複雜度 (預設) </span><span class="sxs-lookup"><span data-stu-id="5a043-217">34–66: Medium complexity (default)</span></span></li>
<li><span data-ttu-id="5a043-218">67–100：高複雜度</span><span class="sxs-lookup"><span data-stu-id="5a043-218">67–100: High complexity</span></span></li>
</ul>
<br/> <span data-ttu-id="5a043-219">此值會影響編碼器執行各種編碼作業（例如動作補償）的方式。</span><span class="sxs-lookup"><span data-stu-id="5a043-219">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="5a043-220">在較高的複雜性層級中，編碼器的執行速度會更慢，但以相同的位元速率產生更高的品質。</span><span class="sxs-lookup"><span data-stu-id="5a043-220">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a043-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span><span class="sxs-lookup"><span data-stu-id="5a043-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span></span></td>
<td><span data-ttu-id="5a043-222">啟用或停用 CABAC (內容自我調整二進位算術編碼) 適用于 h.264 熵編碼。</span><span class="sxs-lookup"><span data-stu-id="5a043-222">Enables or disables CABAC (context-adaptive binary arithmetic coding) for H.264 entropy coding.</span></span> <span data-ttu-id="5a043-223">預設值為 <strong>VARIANT_FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="5a043-223">The default value is <strong>VARIANT_FALSE</strong>.</span></span> <br/> <span data-ttu-id="5a043-224">CABAC 不會用於基準設定檔。</span><span class="sxs-lookup"><span data-stu-id="5a043-224">CABAC is not used for Baseline profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a043-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span><span class="sxs-lookup"><span data-stu-id="5a043-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span></span></td>
<td><span data-ttu-id="5a043-226">將 NAL 的 <strong>seq_parameter_set_id</strong> 值設定在 h.264 位流的 SPS 單位中。</span><span class="sxs-lookup"><span data-stu-id="5a043-226">Sets the value of <strong>seq_parameter_set_id</strong> in the SPS NAL unit of the H.264 bitstream.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a043-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span><span class="sxs-lookup"><span data-stu-id="5a043-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span></span></td>
<td><span data-ttu-id="5a043-228">設定輸出位流中連續 B 框架的最大數目。</span><span class="sxs-lookup"><span data-stu-id="5a043-228">Sets the maximum number of consecutive B frames in the output bitstream.</span></span> <span data-ttu-id="5a043-229">有效值為：</span><span class="sxs-lookup"><span data-stu-id="5a043-229">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="5a043-230">0：請勿使用 B 框架 (預設) 。</span><span class="sxs-lookup"><span data-stu-id="5a043-230">0: Do not use B frames (default).</span></span></li>
<li><span data-ttu-id="5a043-231">1：使用一個 B 框架。</span><span class="sxs-lookup"><span data-stu-id="5a043-231">1: Use one B frame.</span></span></li>
<li><span data-ttu-id="5a043-232">2：使用兩個 B 框架。</span><span class="sxs-lookup"><span data-stu-id="5a043-232">2: Use two B frames.</span></span></li>
</ul>
<span data-ttu-id="5a043-233">若要設定此參數，請在呼叫 <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform：： SetOutputType</strong></a>之前設定屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-233">To set this parameter, set the property before calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform::SetOutputType</strong></a>.</span></span> <br/> <span data-ttu-id="5a043-234">針對基準設定檔，B 框架的數目一律為零。</span><span class="sxs-lookup"><span data-stu-id="5a043-234">For Baseline profile, the number of B frames is always zero.</span></span> <span data-ttu-id="5a043-235">編碼器將覆寫非零值。</span><span class="sxs-lookup"><span data-stu-id="5a043-235">The encoder will override nonzero values.</span></span><br/> <span data-ttu-id="5a043-236">針對其他 h.264 設定檔，如果此屬性為非零，則會 IBBPBBP 編碼模式，其中連續 B 框架的最大數目等於 <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>。</span><span class="sxs-lookup"><span data-stu-id="5a043-236">For other H.264 profiles, if this property is nonzero, the encoding pattern is IBBPBBP, where the maximum number of consecutive B frames is equal to <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a043-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="5a043-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="5a043-238">將每個 GOP 標頭的圖片數目設定為下一個，包括前置錨點，但不包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="5a043-238">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="5a043-239">有效範圍是 [0 .。。2³²-1]。</span><span class="sxs-lookup"><span data-stu-id="5a043-239">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="5a043-240">如果為零，則編碼器會選取 GOP 大小。</span><span class="sxs-lookup"><span data-stu-id="5a043-240">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="5a043-241">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="5a043-241">The default value is zero.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a043-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="5a043-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="5a043-243">設定編碼器所使用的背景工作執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="5a043-243">Sets the number of worker threads used by a encoder.</span></span><br/> <span data-ttu-id="5a043-244">有效範圍為0到16。</span><span class="sxs-lookup"><span data-stu-id="5a043-244">The valid range is 0–16.</span></span> <span data-ttu-id="5a043-245">如果為零，則編碼器會選取執行緒的數目。</span><span class="sxs-lookup"><span data-stu-id="5a043-245">If zero, the encoder selects the number of threads.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a043-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span><span class="sxs-lookup"><span data-stu-id="5a043-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span></span></td>
<td><span data-ttu-id="5a043-247">表示影片內容的類型。</span><span class="sxs-lookup"><span data-stu-id="5a043-247">Indicates the type of video content.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a043-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="5a043-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="5a043-249">有效範圍：16–51。</span><span class="sxs-lookup"><span data-stu-id="5a043-249">Valid range: 16–51.</span></span> <span data-ttu-id="5a043-250">預設值為24。</span><span class="sxs-lookup"><span data-stu-id="5a043-250">The default value is 24.</span></span> <br/> <span data-ttu-id="5a043-251">當速率控制模式 <strong>eAVEncCommonRateControlMode_Quality</strong>時，就會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-251">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="5a043-252">這個屬性會設定與 <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>相同的編碼設定。</span><span class="sxs-lookup"><span data-stu-id="5a043-252">This property configures the same encoding setting as <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>.</span></span> <span data-ttu-id="5a043-253">但是， <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> 可讓應用程式直接指定 QP 的值。</span><span class="sxs-lookup"><span data-stu-id="5a043-253">However, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> enables the application to specify the value of QP directly.</span></span> <span data-ttu-id="5a043-254">如果同時設定這兩個屬性，則 AVEncVideoEncodeQP 覆寫。</span><span class="sxs-lookup"><span data-stu-id="5a043-254">If both properties are set, AVEncVideoEncodeQP overrides.</span></span> <br/> <span data-ttu-id="5a043-255">預設值24對應于 <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> 設定的預設值70。</span><span class="sxs-lookup"><span data-stu-id="5a043-255">The default value of 24 corresponds to the default value of 70 for the <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a043-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="5a043-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="5a043-257">強制編碼器將下一個畫面格編碼為主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="5a043-257">Forces the encoder to code the next frame as a key frame.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a043-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="5a043-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="5a043-259">有效範圍：0到51。</span><span class="sxs-lookup"><span data-stu-id="5a043-259">Valid range: 0–51.</span></span> <span data-ttu-id="5a043-260">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="5a043-260">The default value is 0.</span></span> <br/> <span data-ttu-id="5a043-261">這個屬性會套用至所有速率控制模式。</span><span class="sxs-lookup"><span data-stu-id="5a043-261">This property applies to all rate control modes.</span></span> <span data-ttu-id="5a043-262">編碼器不應產生小於 <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> 屬性指定的值。</span><span class="sxs-lookup"><span data-stu-id="5a043-262">The encoder should not produce a QP value lower than what is specified by the <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a043-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="5a043-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="5a043-264">啟用或停用低延遲模式。</span><span class="sxs-lookup"><span data-stu-id="5a043-264">Enables or disables low-latency mode.</span></span> <span data-ttu-id="5a043-265">請參閱「 &quot; &quot; 備註」一節中的多執行緒。</span><span class="sxs-lookup"><span data-stu-id="5a043-265">See &quot;Multithreading&quot; in the Remarks section.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="5a043-266">備註</span><span class="sxs-lookup"><span data-stu-id="5a043-266">Remarks</span></span>

<span data-ttu-id="5a043-267">編碼器支援下列速率控制模式。</span><span class="sxs-lookup"><span data-stu-id="5a043-267">The encoder supports the following rate control modes.</span></span>



| <span data-ttu-id="5a043-268">模式</span><span class="sxs-lookup"><span data-stu-id="5a043-268">Mode</span></span>                                  | <span data-ttu-id="5a043-269">常數</span><span class="sxs-lookup"><span data-stu-id="5a043-269">Constant</span></span>                                            | <span data-ttu-id="5a043-270">描述</span><span class="sxs-lookup"><span data-stu-id="5a043-270">Description</span></span>                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a043-271">固定位元速率 (CBR) </span><span class="sxs-lookup"><span data-stu-id="5a043-271">Constant bit rate (CBR)</span></span>               | <span data-ttu-id="5a043-272">**eAVEncCommonRateControlMode_CBR**</span><span class="sxs-lookup"><span data-stu-id="5a043-272">**eAVEncCommonRateControlMode_CBR**</span></span>                | <span data-ttu-id="5a043-273">編碼器會使用 "有漏洞 bucket" 模型，嘗試達到常數的位元速率。</span><span class="sxs-lookup"><span data-stu-id="5a043-273">The encoder tries to achieve a constant bit rate, using a "leaky bucket" model.</span></span> <span data-ttu-id="5a043-274">目標位速率是由 [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) 屬性提供。</span><span class="sxs-lookup"><span data-stu-id="5a043-274">The target bit rate is given by the [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="5a043-275">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="5a043-275">Requires Windows 8.</span></span> <br/> |
| <span data-ttu-id="5a043-276"> (VBR) 的限制變數位速率</span><span class="sxs-lookup"><span data-stu-id="5a043-276">Constrained variable bit rate (VBR)</span></span>   | <span data-ttu-id="5a043-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="5a043-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span></span> | <span data-ttu-id="5a043-278">編碼器會使用具有尖峰位速率的「有漏洞 bucket」模型。</span><span class="sxs-lookup"><span data-stu-id="5a043-278">The encoder uses a "leaky bucket" model with a peak bit rate.</span></span> <span data-ttu-id="5a043-279">有漏洞 bucket 的清空率是由 [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) 屬性提供。</span><span class="sxs-lookup"><span data-stu-id="5a043-279">The drain rate for the leaky bucket is given by the [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="5a043-280">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="5a043-280">Requires Windows 8.</span></span> <br/>     |
| <span data-ttu-id="5a043-281">以品質為基礎的變數位元速率 (VBR) </span><span class="sxs-lookup"><span data-stu-id="5a043-281">Quality-based variable bit rate (VBR)</span></span> | <span data-ttu-id="5a043-282">**eAVEncCommonRateControlMode_Quality**</span><span class="sxs-lookup"><span data-stu-id="5a043-282">**eAVEncCommonRateControlMode_Quality**</span></span>            | <span data-ttu-id="5a043-283">編碼器會嘗試達成 [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) 屬性所提供的常數品質層級。</span><span class="sxs-lookup"><span data-stu-id="5a043-283">The encoder tries to achieve a constant quality level, given by the [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) property.</span></span>                                                                                                           |
| <span data-ttu-id="5a043-284">未受限制的 VBR</span><span class="sxs-lookup"><span data-stu-id="5a043-284">Unconstrained VBR</span></span>                     | <span data-ttu-id="5a043-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="5a043-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span></span>   | <span data-ttu-id="5a043-286">編碼器嘗試達到輸出媒體類型中 [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) 屬性指定的目標位元速率。</span><span class="sxs-lookup"><span data-stu-id="5a043-286">The encoder tries to achieve the target bitrate given by the [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute in the output media type.</span></span> <span data-ttu-id="5a043-287">這是預設模式。</span><span class="sxs-lookup"><span data-stu-id="5a043-287">This is the default mode.</span></span>                                                              |



 

<span data-ttu-id="5a043-288">CBR 和受限的 VBR 模式需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="5a043-288">CBR and constrained VBR modes require Windows 8.</span></span>

<span data-ttu-id="5a043-289">在 Windows 8 中，編碼器會在輸出範例中設定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="5a043-289">In Windows 8, the encoder sets the following attributes on the output samples:</span></span>

-   [<span data-ttu-id="5a043-290">MFSampleExtension_DecodeTimestamp</span><span class="sxs-lookup"><span data-stu-id="5a043-290">MFSampleExtension_DecodeTimestamp</span></span>](mfsampleextension-decodetimestamp.md)
-   [<span data-ttu-id="5a043-291">MFSampleExtension_VideoEncodePictureType</span><span class="sxs-lookup"><span data-stu-id="5a043-291">MFSampleExtension_VideoEncodePictureType</span></span>](mfsampleextension-videoencodepicturetype.md)
-   [<span data-ttu-id="5a043-292">MFSampleExtension_VideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="5a043-292">MFSampleExtension_VideoEncodeQP</span></span>](mfsampleextension-videoencodeqp.md)

> [!Note]  
> <span data-ttu-id="5a043-293">先前版本的檔不正確地指出 Windows Server 2008 R2 支援編碼器。</span><span class="sxs-lookup"><span data-stu-id="5a043-293">A previous version of the documentation incorrectly stated that the encoder is supported on Windows Server 2008 R2.</span></span>

 

### <a name="multithreading"></a><span data-ttu-id="5a043-294">多執行緒</span><span class="sxs-lookup"><span data-stu-id="5a043-294">Multithreading</span></span>

<span data-ttu-id="5a043-295">在 Windows 8 中，編碼器支援兩種編碼模式：</span><span class="sxs-lookup"><span data-stu-id="5a043-295">In Windows 8, the encoder supports two encoding modes:</span></span>

-   <span data-ttu-id="5a043-296">**配量編碼。**</span><span class="sxs-lookup"><span data-stu-id="5a043-296">**Slice encoding.**</span></span> <span data-ttu-id="5a043-297">在此模式中，配量會以平行方式編碼。</span><span class="sxs-lookup"><span data-stu-id="5a043-297">In this mode, slices are encoded in parallel.</span></span> <span data-ttu-id="5a043-298">每個配量都會在不同的執行緒上進行編碼。</span><span class="sxs-lookup"><span data-stu-id="5a043-298">Each slice is encoded on a different thread.</span></span> <span data-ttu-id="5a043-299">這個模式的延遲很低，因為單一圖片會以平行方式編碼。</span><span class="sxs-lookup"><span data-stu-id="5a043-299">This mode has low latency, because a single picture is encoded in parallel.</span></span> <span data-ttu-id="5a043-300">不過，此方法不會隨著核心數目的增加而調整，因為配量的數目是由輸入圖片中的巨大區塊資料列數目所限制。</span><span class="sxs-lookup"><span data-stu-id="5a043-300">However, this approach does not scale as the number of cores increases, because the number of slices is bounded by the number of macroblock rows in the input picture.</span></span>
-   <span data-ttu-id="5a043-301">**多畫面編碼。**</span><span class="sxs-lookup"><span data-stu-id="5a043-301">**Multi-frame encoding.**</span></span> <span data-ttu-id="5a043-302">在此模式中，編碼器會接受多個輸入畫面格，並以平行方式進行編碼。</span><span class="sxs-lookup"><span data-stu-id="5a043-302">In this mode, the encoder accepts multiple frames of input and encodes them in parallel.</span></span> <span data-ttu-id="5a043-303">這個模式在多核心環境中會調整得更好，但會引進更多延遲。</span><span class="sxs-lookup"><span data-stu-id="5a043-303">This mode scales better in a multicore environment, but introduces more latency.</span></span>

<span data-ttu-id="5a043-304">編碼器預設為配量編碼，以將延遲降至最低。</span><span class="sxs-lookup"><span data-stu-id="5a043-304">The encoder defaults to slice encoding, to minimize latency.</span></span> <span data-ttu-id="5a043-305">若要啟用多畫面編碼，請將 [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) 屬性設定為 **VARIANT_FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5a043-305">To enable multi-frame encoding, set the [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) property to **VARIANT_FALSE**.</span></span>

<span data-ttu-id="5a043-306">若要設定編碼器所使用的背景工作執行緒數目，請設定 [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-306">To set the number of worker threads used by the encoder, set the [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) property.</span></span>

<span data-ttu-id="5a043-307">在 Windows 7 中，編碼器一律會使用配量編碼。</span><span class="sxs-lookup"><span data-stu-id="5a043-307">In Windows 7, the encoder always uses slice encoding.</span></span>

### <a name="certified-hardware-encoder"></a><span data-ttu-id="5a043-308">經認證的硬體編碼器</span><span class="sxs-lookup"><span data-stu-id="5a043-308">Certified Hardware Encoder</span></span>

<span data-ttu-id="5a043-309">如果有認證硬體編碼器，通常會使用它來取代媒體基礎相關案例的收件匣系統編碼器。</span><span class="sxs-lookup"><span data-stu-id="5a043-309">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="5a043-310">需要經過認證的編碼器，才能支援特定的 **ICodecAPI** 屬性集，並可選擇性地支援另一組屬性。</span><span class="sxs-lookup"><span data-stu-id="5a043-310">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="5a043-311">認證程式應保證所需的屬性受到適當支援，而且如果支援選擇性屬性，也會受到適當的支援。</span><span class="sxs-lookup"><span data-stu-id="5a043-311">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="5a043-312">以下是用來傳遞 HCK 編碼器認證之編碼器的必要和選擇性 **ICodecAPI** 屬性集。</span><span class="sxs-lookup"><span data-stu-id="5a043-312">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

<span data-ttu-id="5a043-313">需要下列 Windows 8 和 Windows 8.1 **ICodecAPI** 屬性：</span><span class="sxs-lookup"><span data-stu-id="5a043-313">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are required:</span></span>

-   [<span data-ttu-id="5a043-314">CODECAPI_AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="5a043-314">CODECAPI_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="5a043-315">CODECAPI_AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="5a043-315">CODECAPI_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="5a043-316">CODECAPI_AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="5a043-316">CODECAPI_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="5a043-317">CODECAPI_AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="5a043-317">CODECAPI_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="5a043-318">CODECAPI_AVEncCommonMaxBitRate</span><span class="sxs-lookup"><span data-stu-id="5a043-318">CODECAPI_AVEncCommonMaxBitRate</span></span>](../directshow/avenccommonmaxbitrate-property.md)
-   [<span data-ttu-id="5a043-319">CODECAPI_AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="5a043-319">CODECAPI_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="5a043-320">CODECAPI_AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="5a043-320">CODECAPI_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="5a043-321">CODECAPI_AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="5a043-321">CODECAPI_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="5a043-322">CODECAPI_AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="5a043-322">CODECAPI_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

<span data-ttu-id="5a043-323">下列 Windows 8.1 **ICodecAPI** 屬性是選擇性的，但如果支援，則會在 HCK 中進行測試。</span><span class="sxs-lookup"><span data-stu-id="5a043-323">The following Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   [<span data-ttu-id="5a043-324">CODECAPI_AVEncVideoMinQP</span><span class="sxs-lookup"><span data-stu-id="5a043-324">CODECAPI_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
-   [<span data-ttu-id="5a043-325">CODECAPI_AVEncVideoLTRBufferControl</span><span class="sxs-lookup"><span data-stu-id="5a043-325">CODECAPI_AVEncVideoLTRBufferControl</span></span>](codecapi-avencvideoltrbuffercontrol.md)
-   [<span data-ttu-id="5a043-326">CODECAPI_AVEncVideoMarkLTRFrame</span><span class="sxs-lookup"><span data-stu-id="5a043-326">CODECAPI_AVEncVideoMarkLTRFrame</span></span>](codecapi-avencvideomarkltrframe.md)
-   [<span data-ttu-id="5a043-327">CODECAPI_AVEncVideoUseLTRFrame</span><span class="sxs-lookup"><span data-stu-id="5a043-327">CODECAPI_AVEncVideoUseLTRFrame</span></span>](codecapi-avencvideouseltrframe.md)
-   [<span data-ttu-id="5a043-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span><span class="sxs-lookup"><span data-stu-id="5a043-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span></span>](codecapi-avencvideoencodeframetypeqp.md)
-   [<span data-ttu-id="5a043-329">CODECAPI_AVEncSliceControlMode</span><span class="sxs-lookup"><span data-stu-id="5a043-329">CODECAPI_AVEncSliceControlMode</span></span>](codecapi-avencslicecontrolmode.md)
-   [<span data-ttu-id="5a043-330">CODECAPI_AVEncSliceControlSize</span><span class="sxs-lookup"><span data-stu-id="5a043-330">CODECAPI_AVEncSliceControlSize</span></span>](codecapi-avencslicecontrolsize.md)
-   [<span data-ttu-id="5a043-331">CODECAPI_AVEncVideoMaxNumRefFrame</span><span class="sxs-lookup"><span data-stu-id="5a043-331">CODECAPI_AVEncVideoMaxNumRefFrame</span></span>](codecapi-avencvideomaxnumrefframe.md)
-   [<span data-ttu-id="5a043-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span><span class="sxs-lookup"><span data-stu-id="5a043-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span></span>](codecapi-avencvideomeanabsolutedifference.md)
-   [<span data-ttu-id="5a043-333">CODECAPI_AVEncVideoMaxQP</span><span class="sxs-lookup"><span data-stu-id="5a043-333">CODECAPI_AVEncVideoMaxQP</span></span>](codecapi-avencvideomaxqp.md)
-   [<span data-ttu-id="5a043-334">CODECAPI_AVEncVideoROIEnabled</span><span class="sxs-lookup"><span data-stu-id="5a043-334">CODECAPI_AVEncVideoROIEnabled</span></span>](codecapi-avencvideoroienabled.md)
-   <span data-ttu-id="5a043-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (動態) </span><span class="sxs-lookup"><span data-stu-id="5a043-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Dynamic)</span></span>
-   [<span data-ttu-id="5a043-336">CODECAPI_AVEncH264CABACEnable</span><span class="sxs-lookup"><span data-stu-id="5a043-336">CODECAPI_AVEncH264CABACEnable</span></span>](codecapi-avench264cabacenable.md)

<span data-ttu-id="5a043-337">下列 Windows 8 和 Windows 8.1 **ICodecAPI** 屬性是選擇性的，但如果支援，則會在 HCK 中進行測試。</span><span class="sxs-lookup"><span data-stu-id="5a043-337">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   <span data-ttu-id="5a043-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (靜態) </span><span class="sxs-lookup"><span data-stu-id="5a043-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Static)</span></span>
-   [<span data-ttu-id="5a043-339">CODECAPI_AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="5a043-339">CODECAPI_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

<span data-ttu-id="5a043-340">下列 **ICodecAPI** 屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="5a043-340">The following **ICodecAPI** properties are optional.</span></span> <span data-ttu-id="5a043-341">它們不會在 HCK 中進行測試。</span><span class="sxs-lookup"><span data-stu-id="5a043-341">They are not tested in HCK.</span></span>

-   [<span data-ttu-id="5a043-342">CODECAPI_AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="5a043-342">CODECAPI_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a><span data-ttu-id="5a043-343">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a043-343">Requirements</span></span>



| <span data-ttu-id="5a043-344">需求</span><span class="sxs-lookup"><span data-stu-id="5a043-344">Requirement</span></span> | <span data-ttu-id="5a043-345">值</span><span class="sxs-lookup"><span data-stu-id="5a043-345">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a043-346">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a043-346">Minimum supported client</span></span><br/> | <span data-ttu-id="5a043-347">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a043-347">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5a043-348">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a043-348">Minimum supported server</span></span><br/> | <span data-ttu-id="5a043-349">都不支援</span><span class="sxs-lookup"><span data-stu-id="5a043-349">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5a043-350">DLL</span><span class="sxs-lookup"><span data-stu-id="5a043-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a043-351"><dt>Mfh264enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a043-351"><dt>Mfh264enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a043-352">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a043-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a043-353">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="5a043-353">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="5a043-354">媒體基礎中的 MPEG 4 支援</span><span class="sxs-lookup"><span data-stu-id="5a043-354">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="5a043-355">媒體基礎中支援的媒體格式</span><span class="sxs-lookup"><span data-stu-id="5a043-355">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="5a043-356">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="5a043-356">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
