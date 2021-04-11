---
description: 媒體基礎 .H 的視頻編碼器是媒體基礎轉換，支援將內容編碼為 HEVC 格式。
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: H. 265/HEVC 影片編碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943689"
---
# <a name="h265--hevc-video-encoder"></a><span data-ttu-id="f311e-103">H. 265/HEVC 影片編碼器</span><span class="sxs-lookup"><span data-stu-id="f311e-103">H.265 / HEVC Video Encoder</span></span>

<span data-ttu-id="f311e-104">媒體基礎 .H 的視頻編碼器是 [媒體基礎轉換](media-foundation-transforms.md) ，支援將內容編碼為 HEVC 格式。</span><span class="sxs-lookup"><span data-stu-id="f311e-104">The Media Foundation H.265 video encoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports encoding content into the H.265/HEVC format.</span></span> <span data-ttu-id="f311e-105">編碼器支援下列設定檔：</span><span class="sxs-lookup"><span data-stu-id="f311e-105">The encoder supports the following profiles:</span></span>

-   <span data-ttu-id="f311e-106">主要設定檔</span><span class="sxs-lookup"><span data-stu-id="f311e-106">Main Profile</span></span>

<span data-ttu-id="f311e-107">H. 視頻編碼器會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="f311e-107">The H.265 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="f311e-108">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="f311e-108">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="f311e-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="f311e-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="f311e-110">輸入類型</span><span class="sxs-lookup"><span data-stu-id="f311e-110">Input Types</span></span>

<span data-ttu-id="f311e-111">輸入媒體類型必須有下列其中一個子類型：</span><span class="sxs-lookup"><span data-stu-id="f311e-111">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="f311e-112">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="f311e-112">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="f311e-113">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="f311e-113">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="f311e-114">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="f311e-114">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="f311e-115">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="f311e-115">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="f311e-116">如需這些子類型的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="f311e-116">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="f311e-117">輸出類型必須在輸入類型之前設定。</span><span class="sxs-lookup"><span data-stu-id="f311e-117">The output type must be set before the input type.</span></span> <span data-ttu-id="f311e-118">在設定輸出類型之前，編碼器的 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 方法會傳回 **\_ \_ \_ \_ 未 \_ 設定的 MF E 轉換類型**。</span><span class="sxs-lookup"><span data-stu-id="f311e-118">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="f311e-119">輸出型別</span><span class="sxs-lookup"><span data-stu-id="f311e-119">Output Types</span></span>

<span data-ttu-id="f311e-120">編碼器支援單一輸出子類型：</span><span class="sxs-lookup"><span data-stu-id="f311e-120">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="f311e-121">**MFVideoFormat \_ H265**</span><span class="sxs-lookup"><span data-stu-id="f311e-121">**MFVideoFormat\_H265**</span></span>

<span data-ttu-id="f311e-122">在輸出媒體類型上設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="f311e-122">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f311e-123">屬性</span><span class="sxs-lookup"><span data-stu-id="f311e-123">Attribute</span></span></th>
<th><span data-ttu-id="f311e-124">描述</span><span class="sxs-lookup"><span data-stu-id="f311e-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f311e-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f311e-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="f311e-126">主要類型。</span><span class="sxs-lookup"><span data-stu-id="f311e-126">Major type.</span></span> <span data-ttu-id="f311e-127">必須是 <strong>MFMediaType_Video</strong>。</span><span class="sxs-lookup"><span data-stu-id="f311e-127">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f311e-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f311e-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="f311e-129">影片子類型。</span><span class="sxs-lookup"><span data-stu-id="f311e-129">Video subtype.</span></span> <span data-ttu-id="f311e-130">必須是 <strong>MFVideoFormat_HEVC</strong>。</span><span class="sxs-lookup"><span data-stu-id="f311e-130">Must be <strong>MFVideoFormat_HEVC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f311e-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f311e-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="f311e-132">平均編碼的位速度，以位/秒為單位。</span><span class="sxs-lookup"><span data-stu-id="f311e-132">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="f311e-133">必須大於零。</span><span class="sxs-lookup"><span data-stu-id="f311e-133">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f311e-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f311e-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="f311e-135">畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="f311e-135">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f311e-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f311e-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="f311e-137">框架大小。</span><span class="sxs-lookup"><span data-stu-id="f311e-137">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f311e-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="f311e-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="f311e-139">交錯模式。</span><span class="sxs-lookup"><span data-stu-id="f311e-139">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f311e-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span><span class="sxs-lookup"><span data-stu-id="f311e-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span></span></td>
<td><span data-ttu-id="f311e-141">H. 265 編碼設定檔。</span><span class="sxs-lookup"><span data-stu-id="f311e-141">H.265 encoding profile.</span></span><br/> <span data-ttu-id="f311e-142">支援的值為：</span><span class="sxs-lookup"><span data-stu-id="f311e-142">The supported values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="f311e-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span><span class="sxs-lookup"><span data-stu-id="f311e-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f311e-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="f311e-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="f311e-145">指定編碼影片的層級。</span><span class="sxs-lookup"><span data-stu-id="f311e-145">Specifies the level of the coded video.</span></span> <span data-ttu-id="f311e-146">如需有關設定檔和層級條件約束的詳細資訊，請參閱 ITU-T H. 265 的附錄 A。</span><span class="sxs-lookup"><span data-stu-id="f311e-146">For more information about profile and level constraints, refer to Annex A of ITU-T H.265.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f311e-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="f311e-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="f311e-148">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f311e-148">Optional.</span></span> <span data-ttu-id="f311e-149">指定圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="f311e-149">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="f311e-150">預設值為1:1。</span><span class="sxs-lookup"><span data-stu-id="f311e-150">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f311e-151">設定輸出型別之後，影片編碼器會藉由新增 [**MF \_ MT \_ MPEG \_ SEQUENCE \_ 標頭**](mf-mt-mpeg-sequence-header-attribute.md) 屬性來更新型別。</span><span class="sxs-lookup"><span data-stu-id="f311e-151">After the output type is set, the video encoder updates the type by adding the [**MF\_MT\_MPEG\_SEQUENCE\_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="f311e-152">此屬性包含 sequence 標頭。</span><span class="sxs-lookup"><span data-stu-id="f311e-152">This attribute contains the sequence header.</span></span>

## <a name="supported-imftransform-methods"></a><span data-ttu-id="f311e-153">支援的 IMFTransform 方法</span><span class="sxs-lookup"><span data-stu-id="f311e-153">Supported IMFTransform methods</span></span>

<span data-ttu-id="f311e-154">[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)介面的下列方法支援適用于 .H/HEVC 編碼器：</span><span class="sxs-lookup"><span data-stu-id="f311e-154">The following methods of the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="f311e-155">**GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="f311e-155">**GetAttributes**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [<span data-ttu-id="f311e-156">**GetInputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="f311e-156">**GetInputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [<span data-ttu-id="f311e-157">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="f311e-157">**GetInputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [<span data-ttu-id="f311e-158">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="f311e-158">**GetInputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [<span data-ttu-id="f311e-159">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="f311e-159">**GetInputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [<span data-ttu-id="f311e-160">**GetOutputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="f311e-160">**GetOutputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [<span data-ttu-id="f311e-161">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="f311e-161">**GetOutputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [<span data-ttu-id="f311e-162">**GetOutputStatus**</span><span class="sxs-lookup"><span data-stu-id="f311e-162">**GetOutputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [<span data-ttu-id="f311e-163">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="f311e-163">**GetOutputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [<span data-ttu-id="f311e-164">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="f311e-164">**GetStreamCount**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [<span data-ttu-id="f311e-165">**GetStreamLimits**</span><span class="sxs-lookup"><span data-stu-id="f311e-165">**GetStreamLimits**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [<span data-ttu-id="f311e-166">**In processevent.<**</span><span class="sxs-lookup"><span data-stu-id="f311e-166">**ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [<span data-ttu-id="f311e-167">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="f311e-167">**ProcessMessage**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [<span data-ttu-id="f311e-168">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="f311e-168">**ProcessInput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [<span data-ttu-id="f311e-169">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="f311e-169">**ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [<span data-ttu-id="f311e-170">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="f311e-170">**SetInputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [<span data-ttu-id="f311e-171">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="f311e-171">**SetOutputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [<span data-ttu-id="f311e-172">**SetOutputBounds**</span><span class="sxs-lookup"><span data-stu-id="f311e-172">**SetOutputBounds**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

<span data-ttu-id="f311e-173">所有其他 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 方法都會傳回錯誤 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="f311e-173">All other [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods will return the error E\_NOTIMPL.</span></span>

## <a name="supported-icodecapi-methods"></a><span data-ttu-id="f311e-174">支援的 ICodecAPI 方法</span><span class="sxs-lookup"><span data-stu-id="f311e-174">Supported ICodecAPI methods</span></span>

<span data-ttu-id="f311e-175">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)介面的下列方法支援適用于 .H/HEVC 編碼器：</span><span class="sxs-lookup"><span data-stu-id="f311e-175">The following methods of the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="f311e-176">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="f311e-176">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="f311e-177">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="f311e-177">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [<span data-ttu-id="f311e-178">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="f311e-178">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="f311e-179">**GetParameterRange**</span><span class="sxs-lookup"><span data-stu-id="f311e-179">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="f311e-180">**GetParameterValues**</span><span class="sxs-lookup"><span data-stu-id="f311e-180">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

<span data-ttu-id="f311e-181">所有其他 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 方法都會傳回錯誤 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="f311e-181">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods will return the error E\_NOTIMPL.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="f311e-182">編解碼器屬性</span><span class="sxs-lookup"><span data-stu-id="f311e-182">Codec Properties</span></span>

<span data-ttu-id="f311e-183">H. 編碼程式會實 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面來設定編碼參數。</span><span class="sxs-lookup"><span data-stu-id="f311e-183">The H.265 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="f311e-184">它支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="f311e-184">It supports the following properties.</span></span>

<span data-ttu-id="f311e-185">如需 HCK 編碼器認證的編解碼器需求，請參閱下面的「 **經認證的硬體編碼器** 」一節。</span><span class="sxs-lookup"><span data-stu-id="f311e-185">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f311e-186">屬性</span><span class="sxs-lookup"><span data-stu-id="f311e-186">Property</span></span></th>
<th><span data-ttu-id="f311e-187">描述</span><span class="sxs-lookup"><span data-stu-id="f311e-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f311e-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="f311e-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span></span></td>
<td><span data-ttu-id="f311e-189">設定速率控制模式。</span><span class="sxs-lookup"><span data-stu-id="f311e-189">Sets the rate control mode.</span></span> <span data-ttu-id="f311e-190">支援的模式如下：</span><span class="sxs-lookup"><span data-stu-id="f311e-190">The supported modes are:</span></span><br/>
<ul>
<li><span data-ttu-id="f311e-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span><span class="sxs-lookup"><span data-stu-id="f311e-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span></span></li>
<li><span data-ttu-id="f311e-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span><span class="sxs-lookup"><span data-stu-id="f311e-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span></span></li>
</ul>
<span data-ttu-id="f311e-193">如果指定了其他模式，則會使用 <strong>eAVEncCommonRateControlMode_CBR</strong> 速率控制。</span><span class="sxs-lookup"><span data-stu-id="f311e-193">If other modes are specified, the <strong>eAVEncCommonRateControlMode_CBR</strong> rate control will be used.</span></span><br/> <span data-ttu-id="f311e-194">這是 VT_UI4 的值。</span><span class="sxs-lookup"><span data-stu-id="f311e-194">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f311e-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="f311e-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="f311e-196">設定編碼位資料流程的平均位元速率，以每秒位數為單位。</span><span class="sxs-lookup"><span data-stu-id="f311e-196">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <br/> <span data-ttu-id="f311e-197">有效範圍為 [1 .。。2³²-1]。</span><span class="sxs-lookup"><span data-stu-id="f311e-197">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="f311e-198">這是 VT_UI4 的值。</span><span class="sxs-lookup"><span data-stu-id="f311e-198">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f311e-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="f311e-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="f311e-200">以位元組為單位，設定常數速率的緩衝區大小（以位元組為單位） (CBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="f311e-200">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="f311e-201">有效範圍為 [1 .。。2³²-1]。</span><span class="sxs-lookup"><span data-stu-id="f311e-201">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="f311e-202">這是 VT_UI4 的值。</span><span class="sxs-lookup"><span data-stu-id="f311e-202">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f311e-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="f311e-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="f311e-204">針對速率控制模式設定允許尖峰位元速率的最大位元速率。</span><span class="sxs-lookup"><span data-stu-id="f311e-204">Sets the maximum bitrate for rate control modes that allow a peak bitrate.</span></span> <br/> <span data-ttu-id="f311e-205">有效範圍為 [1 .。。2³²-1]。</span><span class="sxs-lookup"><span data-stu-id="f311e-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="f311e-206">這是 VT_UI4 的值。</span><span class="sxs-lookup"><span data-stu-id="f311e-206">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f311e-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="f311e-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="f311e-208">將每個 GOP 標頭的圖片數目設定為下一個，包括前置錨點，但不包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="f311e-208">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="f311e-209">有效範圍是 [0 .。。2³²-1]。</span><span class="sxs-lookup"><span data-stu-id="f311e-209">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="f311e-210">如果為零，則編碼器會選取 GOP 大小。</span><span class="sxs-lookup"><span data-stu-id="f311e-210">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="f311e-211">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="f311e-211">The default value is zero.</span></span> <br/> <span data-ttu-id="f311e-212">這是 VT_UI4 的值。</span><span class="sxs-lookup"><span data-stu-id="f311e-212">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f311e-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="f311e-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="f311e-214">啟用或停用低延遲模式。</span><span class="sxs-lookup"><span data-stu-id="f311e-214">Enables or disables low-latency mode.</span></span> <br/> <span data-ttu-id="f311e-215">這是 VT_BOOL 的值。</span><span class="sxs-lookup"><span data-stu-id="f311e-215">This is a VT_BOOL value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f311e-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="f311e-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="f311e-217">設定品質/速度的取捨。</span><span class="sxs-lookup"><span data-stu-id="f311e-217">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="f311e-218">此值會影響編碼器執行各種編碼作業（例如動作補償）的方式。</span><span class="sxs-lookup"><span data-stu-id="f311e-218">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="f311e-219">在較高的複雜性層級中，編碼器的執行速度會更慢，但以相同的位元速率產生更高的品質。</span><span class="sxs-lookup"><span data-stu-id="f311e-219">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span> <br/> <span data-ttu-id="f311e-220">有效範圍為 0-100。</span><span class="sxs-lookup"><span data-stu-id="f311e-220">The valid range is 0 – 100.</span></span> <span data-ttu-id="f311e-221">就內部而言，此值會對應至編碼器所支援的一組較小品質/速度層級。</span><span class="sxs-lookup"><span data-stu-id="f311e-221">Internally, this value is mapped to a smaller set of quality/speed levels supported by the encoder.</span></span><br/> <span data-ttu-id="f311e-222">這是 VT_UI4 的值。</span><span class="sxs-lookup"><span data-stu-id="f311e-222">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f311e-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="f311e-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="f311e-224">強制編碼器將下一個畫面格編碼為主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="f311e-224">Forces the encoder to code the next frame as a key frame.</span></span><br/> <span data-ttu-id="f311e-225">這是 VT_UI4 的值。</span><span class="sxs-lookup"><span data-stu-id="f311e-225">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f311e-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="f311e-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="f311e-227">設定此屬性時，會導致編碼器使用指定的 QP 來編碼下一個框架和所有後續的框架，直到指定新的 QP 為止。</span><span class="sxs-lookup"><span data-stu-id="f311e-227">When this property is set it will cause the encoder to use the specified QP to encode the next frame and all subsequent frames until a new QP is specified.</span></span> <br/> <span data-ttu-id="f311e-228">有效範圍：0–51（含）</span><span class="sxs-lookup"><span data-stu-id="f311e-228">Valid range: 0–51, inclusive</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f311e-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="f311e-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="f311e-230">這個屬性會設定編碼器在 CBR ratecontrol 期間可以使用的最小 QP 的限制。</span><span class="sxs-lookup"><span data-stu-id="f311e-230">This property will set a limit on the minimum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="f311e-231">這是 VT_UI4 的值。</span><span class="sxs-lookup"><span data-stu-id="f311e-231">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f311e-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span><span class="sxs-lookup"><span data-stu-id="f311e-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span></span></td>
<td><span data-ttu-id="f311e-233">這個屬性會設定在 CBR ratecontrol 期間，編碼器可使用的最大 QP 值的限制。</span><span class="sxs-lookup"><span data-stu-id="f311e-233">This property will set a limit on the maximum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="f311e-234">這是 VT_UI4 的值。</span><span class="sxs-lookup"><span data-stu-id="f311e-234">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f311e-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span><span class="sxs-lookup"><span data-stu-id="f311e-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span></span></td>
<td><span data-ttu-id="f311e-236">設定內容是否為全螢幕的影片，而不是可能有較小影片視窗或完全沒有影片的螢幕內容。</span><span class="sxs-lookup"><span data-stu-id="f311e-236">Sets whether the content is full-screen video, as opposed to screen content that might have a smaller window of video or have no video at all.</span></span><br/> <span data-ttu-id="f311e-237">這是 VT_UI4 的值。</span><span class="sxs-lookup"><span data-stu-id="f311e-237">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f311e-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="f311e-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="f311e-239">設定用來執行壓縮作業的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="f311e-239">Sets the number of threads used to perform the compression operation.</span></span> <span data-ttu-id="f311e-240">編碼器會將框架分成磚，使執行緒數目等於磚數目。</span><span class="sxs-lookup"><span data-stu-id="f311e-240">The encoder will divide the frame into tiles such that the number of threads equals the number of tiles.</span></span><br/>
<ul>
<li><span data-ttu-id="f311e-241">邏輯處理器的數目。</span><span class="sxs-lookup"><span data-stu-id="f311e-241">The number of logical processors.</span></span> <span data-ttu-id="f311e-242">執行緒的數目必須小於或等於邏輯處理器的數目。</span><span class="sxs-lookup"><span data-stu-id="f311e-242">The number of threads must be less than or equal to the number of logical processors.</span></span></li>
<li><span data-ttu-id="f311e-243">框架的大小。</span><span class="sxs-lookup"><span data-stu-id="f311e-243">The size of the frame.</span></span> <span data-ttu-id="f311e-244">磚的大小必須大於或等於265x64 圖元。</span><span class="sxs-lookup"><span data-stu-id="f311e-244">The size of a tile must bigger than or equal to 265x64 pixels.</span></span></li>
<li><span data-ttu-id="f311e-245">同位。</span><span class="sxs-lookup"><span data-stu-id="f311e-245">Parity.</span></span> <span data-ttu-id="f311e-246">執行緒的數目必須是偶數值。</span><span class="sxs-lookup"><span data-stu-id="f311e-246">The number of threads must be an even value.</span></span> <span data-ttu-id="f311e-247">如果指定的值為奇數，則會使用下一個較低的偶數值。</span><span class="sxs-lookup"><span data-stu-id="f311e-247">If the specified value is odd then the next lower even value will be used.</span></span></li>
</ul>
<span data-ttu-id="f311e-248">這是 VT_UI4 的值。</span><span class="sxs-lookup"><span data-stu-id="f311e-248">This is a VT_UI4 value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a><span data-ttu-id="f311e-249">經認證的硬體編碼器</span><span class="sxs-lookup"><span data-stu-id="f311e-249">Certified Hardware Encoder</span></span>

<span data-ttu-id="f311e-250">如果有認證硬體編碼器，通常會使用它來取代媒體基礎相關案例的收件匣系統編碼器。</span><span class="sxs-lookup"><span data-stu-id="f311e-250">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="f311e-251">需要經過認證的編碼器，才能支援特定的 **ICodecAPI** 屬性集，並可選擇性地支援另一組屬性。</span><span class="sxs-lookup"><span data-stu-id="f311e-251">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="f311e-252">認證程式應保證所需的屬性受到適當支援，而且如果支援選擇性屬性，也會受到適當的支援。</span><span class="sxs-lookup"><span data-stu-id="f311e-252">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="f311e-253">以下是用來傳遞 HCK 編碼器認證之編碼器的必要和選擇性 **ICodecAPI** 屬性集。</span><span class="sxs-lookup"><span data-stu-id="f311e-253">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

-   [<span data-ttu-id="f311e-254">CODECAPI \_ AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="f311e-254">CODECAPI\_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="f311e-255">CODECAPI \_ AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="f311e-255">CODECAPI\_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="f311e-256">CODECAPI \_ AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="f311e-256">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="f311e-257">CODECAPI \_ AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="f311e-257">CODECAPI\_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="f311e-258">CODECAPI \_ AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="f311e-258">CODECAPI\_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="f311e-259">CODECAPI \_ AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="f311e-259">CODECAPI\_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="f311e-260">CODECAPI \_ AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="f311e-260">CODECAPI\_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a><span data-ttu-id="f311e-261">規格需求</span><span class="sxs-lookup"><span data-stu-id="f311e-261">Requirements</span></span>



| <span data-ttu-id="f311e-262">需求</span><span class="sxs-lookup"><span data-stu-id="f311e-262">Requirement</span></span> | <span data-ttu-id="f311e-263">值</span><span class="sxs-lookup"><span data-stu-id="f311e-263">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f311e-264">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f311e-264">Minimum supported client</span></span><br/> | <span data-ttu-id="f311e-265">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f311e-265">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f311e-266">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f311e-266">Minimum supported server</span></span><br/> | <span data-ttu-id="f311e-267">都不支援</span><span class="sxs-lookup"><span data-stu-id="f311e-267">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f311e-268">DLL</span><span class="sxs-lookup"><span data-stu-id="f311e-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f311e-269"><dt>Mfh265enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f311e-269"><dt>Mfh265enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f311e-270">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f311e-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f311e-271">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="f311e-271">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
