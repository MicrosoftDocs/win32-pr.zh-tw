---
description: MPEG-2 視頻解碼器是一種媒體基礎轉換，可將 MPEG-2 和 MPEG-2 影片解碼。
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: MPEG-2 視頻解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca4384154faff777280fd0a03cf4fd289603e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512596"
---
# <a name="mpeg-2-video-decoder"></a><span data-ttu-id="b0bf4-103">MPEG-2 視頻解碼器</span><span class="sxs-lookup"><span data-stu-id="b0bf4-103">MPEG-2 Video Decoder</span></span>

<span data-ttu-id="b0bf4-104">MPEG-2 視頻解碼器是一種 [媒體基礎轉換](media-foundation-transforms.md) ，可將 MPEG-2 和 Mpeg-2 影片解碼。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-104">The MPEG-2 Video Decoder is a [Media Foundation transform](media-foundation-transforms.md) that decodes MPEG-1 and MPEG-2 video.</span></span> <span data-ttu-id="b0bf4-105">此解碼器支援 MPEG-2 的簡單和主要設定檔影片 (262、ISO/IEC 13818-2) 和 MPEG-2 video (ISO/IEC 11172-2) 。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-105">The decoder supports MPEG-2 Simple and Main profile video (H.262, ISO/IEC 13818-2) and MPEG-1 video (ISO/IEC 11172-2).</span></span>

## <a name="input-types"></a><span data-ttu-id="b0bf4-106">輸入類型</span><span class="sxs-lookup"><span data-stu-id="b0bf4-106">Input Types</span></span>

<span data-ttu-id="b0bf4-107">此解碼器支援下列輸入媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-107">The decoder supports the following input media types.</span></span>

| <span data-ttu-id="b0bf4-108">屬性</span><span class="sxs-lookup"><span data-stu-id="b0bf4-108">Attribute</span></span>                                                 | <span data-ttu-id="b0bf4-109">描述</span><span class="sxs-lookup"><span data-stu-id="b0bf4-109">Description</span></span>                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="b0bf4-110">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-110">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="b0bf4-111">**MFMediaType \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-111">**MFMediaType\_Video**</span></span>                                                  |
| [<span data-ttu-id="b0bf4-112">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="b0bf4-113">**MFVideoFormat \_ MPEG1**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-113">**MFVideoFormat\_MPEG1**</span></span><br/> <span data-ttu-id="b0bf4-114">**MFVideoFormat \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-114">**MFVideoFormat\_MPEG2**</span></span><br/> |



 

## <a name="output-types"></a><span data-ttu-id="b0bf4-115">輸出型別</span><span class="sxs-lookup"><span data-stu-id="b0bf4-115">Output Types</span></span>

<span data-ttu-id="b0bf4-116">此解碼器支援下列輸出類型。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-116">The decoder supports the following output types.</span></span>

| <span data-ttu-id="b0bf4-117">屬性</span><span class="sxs-lookup"><span data-stu-id="b0bf4-117">Attribute</span></span>                                                 | <span data-ttu-id="b0bf4-118">描述</span><span class="sxs-lookup"><span data-stu-id="b0bf4-118">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0bf4-119">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-119">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="b0bf4-120">**MFMediaType \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-120">**MFMediaType\_Video**</span></span>                                                                                                                                                         |
| [<span data-ttu-id="b0bf4-121">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-121">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="b0bf4-122">**MFVideoFormat \_ I420**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-122">**MFVideoFormat\_I420**</span></span><br/> <span data-ttu-id="b0bf4-123">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-123">**MFVideoFormat\_IYUV**</span></span><br/> <span data-ttu-id="b0bf4-124">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-124">**MFVideoFormat\_NV12**</span></span><br/> <span data-ttu-id="b0bf4-125">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-125">**MFVideoFormat\_YUY2**</span></span><br/> <span data-ttu-id="b0bf4-126">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-126">**MFVideoFormat\_YV12**</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0bf4-127">備註</span><span class="sxs-lookup"><span data-stu-id="b0bf4-127">Remarks</span></span>

<span data-ttu-id="b0bf4-128">MPEG-2 影片解碼會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="b0bf4-128">The MPEG-2 video decoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="b0bf4-129">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-129">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="b0bf4-130">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-130">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="b0bf4-131">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-131">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="b0bf4-132">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-132">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="b0bf4-133">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-133">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="b0bf4-134">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-134">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="b0bf4-135">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-135">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="b0bf4-136">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-136">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="b0bf4-137">對解碼器的輸入必須是基本資料流程。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-137">The input to the decoder must be an elementary stream.</span></span> <span data-ttu-id="b0bf4-138">支援的最大解析度為1920×1088圖元。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-138">The maximum supported resolution is 1920 × 1088 pixels.</span></span>

<span data-ttu-id="b0bf4-139">此解碼器支援使用 Microsoft Direct3D 9 或 Microsoft Direct3D 11 (DXVA) 的 DirectX Video 加速。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-139">The decoder supports DirectX Video Acceleration (DXVA) using either Microsoft Direct3D 9 or Microsoft Direct3D 11.</span></span>

### <a name="special-decoding-modes"></a><span data-ttu-id="b0bf4-140">特殊解碼模式</span><span class="sxs-lookup"><span data-stu-id="b0bf4-140">Special Decoding Modes</span></span>

-   <span data-ttu-id="b0bf4-141">**低延遲模式。**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-141">**Low latency mode.**</span></span> <span data-ttu-id="b0bf4-142">這種模式適用于即時通訊等案例。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-142">This mode is appropriate for scenarios such as real-time communications.</span></span> <span data-ttu-id="b0bf4-143">它可減少啟動延遲，讓解碼器更快產生第一個輸出範例。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-143">It reduces start-up latency, so the decoder produces the first output sample sooner.</span></span> <span data-ttu-id="b0bf4-144">不過，在此模式中，解碼器會緩衝較少的樣本，這可能會導致問題，因為此解碼器不會預先解碼為許多框架。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-144">However, the decoder buffers fewer samples in this mode, which can potentially lead to glitches, because the decoder does not decode as many frames in advance.</span></span> <span data-ttu-id="b0bf4-145">若要啟用低延遲模式，請設定 [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-145">To enable low latency mode, set the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) attribute.</span></span>
-   <span data-ttu-id="b0bf4-146">**尋求。**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-146">**Seeking.**</span></span> <span data-ttu-id="b0bf4-147">如需精確的搜尋，請呼叫 [**IMFTransform：： SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) 方法。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-147">For precise seeking, call the [**IMFTransform::SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) method.</span></span> <span data-ttu-id="b0bf4-148">當呼叫這個方法時，此解碼器只會輸出落在呼叫端所指定時間戳記範圍內的框架。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-148">When this method is called, the decoder outputs only frames that fall within the range of time stamps specified by the caller.</span></span>
-   <span data-ttu-id="b0bf4-149">**縮圖產生模式**。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-149">**Thumbnail generation mode**.</span></span> <span data-ttu-id="b0bf4-150">此模式適用于快速產生縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-150">This mode is intended for quick generation of thumbnail images.</span></span> <span data-ttu-id="b0bf4-151">在此模式中，解碼器一開始只會解碼 I 個框架。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-151">In this mode, the decoder initially decodes only I frames.</span></span> <span data-ttu-id="b0bf4-152">如果在特定的畫面格數目內找不到 I 框架，則會以固定的間隔開始解碼 P 框架並輸出非 I 框架 (每 *N* 個圖片) 一次，直到達到 I 個框架為止。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-152">If no I frame is found within a certain number of frames, the decoder starts decoding P frames and outputs non–I frames at a fixed interval (one per *N* pictures) until an I frame is reached.</span></span> <span data-ttu-id="b0bf4-153">若要啟用縮圖產生模式，請設定 [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-153">To enable thumbnail generation mode, set the [CODECAPI\_AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) property.</span></span>
-   <span data-ttu-id="b0bf4-154">**訣竅。**</span><span class="sxs-lookup"><span data-stu-id="b0bf4-154">**Trick play.**</span></span> <span data-ttu-id="b0bf4-155">此解碼器可以更快地以速率解碼，而非即時。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-155">The decoder can decode at rates faster than real time.</span></span> <span data-ttu-id="b0bf4-156">在較高的播放速率中，解碼器會切換為僅解碼 I 個畫面格。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-156">At higher playback rates, the decoder will switch to decoding only I frames.</span></span> <span data-ttu-id="b0bf4-157">若要進行反向播放，只會解碼 I 個框架。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-157">For reverse playback, only I frames are decoded.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="b0bf4-158">編解碼器屬性</span><span class="sxs-lookup"><span data-stu-id="b0bf4-158">Codec Properties</span></span>

<span data-ttu-id="b0bf4-159">此解碼器透過 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-159">The decoder supports the following properties through the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span>



| <span data-ttu-id="b0bf4-160">屬性</span><span class="sxs-lookup"><span data-stu-id="b0bf4-160">Property</span></span>                                                                                                      | <span data-ttu-id="b0bf4-161">描述</span><span class="sxs-lookup"><span data-stu-id="b0bf4-161">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0bf4-162">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="b0bf4-162">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)               | <span data-ttu-id="b0bf4-163">啟用或停用縮圖產生模式。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-163">Enables or disables thumbnail generation mode.</span></span>                                                             |
| [<span data-ttu-id="b0bf4-164">CODECAPI \_ AVDecVideoAcceleration \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="b0bf4-164">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | <span data-ttu-id="b0bf4-165">啟用或停用硬體加速解碼。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-165">Enables or disables hardware accelerated decoding.</span></span>                                                         |
| [<span data-ttu-id="b0bf4-166">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="b0bf4-166">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="b0bf4-167">啟用或停用低延遲模式。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-167">Enables or disables low-latency mode.</span></span>                                                                      |
| [<span data-ttu-id="b0bf4-168">MFT \_ 解碼 \_ 會 \_ \_ \_ 以 \_ 原生 \_ 順序公開輸出類型</span><span class="sxs-lookup"><span data-stu-id="b0bf4-168">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="b0bf4-169">指定此解碼器是否會在其他格式之前公開適用于轉碼的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-169">Specifies whether the decoder exposes output types that are suitable for transcoding before other formats.</span></span> |



 

<span data-ttu-id="b0bf4-170">在這些屬性中，也可以透過 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面設定下列內容：</span><span class="sxs-lookup"><span data-stu-id="b0bf4-170">Of these properties, the following can also be set through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface:</span></span>

-   [<span data-ttu-id="b0bf4-171">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="b0bf4-171">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="b0bf4-172">CODECAPI \_ AVDecVideoAcceleration \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="b0bf4-172">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [<span data-ttu-id="b0bf4-173">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="b0bf4-173">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

### <a name="limitations"></a><span data-ttu-id="b0bf4-174">限制</span><span class="sxs-lookup"><span data-stu-id="b0bf4-174">Limitations</span></span>

-   <span data-ttu-id="b0bf4-175">以 IA-64 為基礎的平臺不支援此解碼器。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-175">The decoder is not supported on IA-64–based platforms.</span></span>
-   <span data-ttu-id="b0bf4-176">此解碼器不支援 CSS 解密或播放加密的 Dvd。</span><span class="sxs-lookup"><span data-stu-id="b0bf4-176">The decoder does not support CSS decryption or playback of encrypted DVDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0bf4-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0bf4-177">Requirements</span></span>



| <span data-ttu-id="b0bf4-178">需求</span><span class="sxs-lookup"><span data-stu-id="b0bf4-178">Requirement</span></span> | <span data-ttu-id="b0bf4-179">值</span><span class="sxs-lookup"><span data-stu-id="b0bf4-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0bf4-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0bf4-180">Minimum supported client</span></span><br/> | <span data-ttu-id="b0bf4-181">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0bf4-181">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b0bf4-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0bf4-182">Minimum supported server</span></span><br/> | <span data-ttu-id="b0bf4-183">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0bf4-183">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b0bf4-184">DLL</span><span class="sxs-lookup"><span data-stu-id="b0bf4-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0bf4-185"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0bf4-185"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0bf4-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0bf4-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0bf4-187">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="b0bf4-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
