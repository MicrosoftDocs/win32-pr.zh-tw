---
description: 媒體基礎 .H 的視頻編碼程式是一種媒體基礎轉換，支援在附錄 B 格式中解碼 H. 265/HEVC 內容，並可用於播放數量和 .m2ts 檔案。
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: H. 265/HEVC 影片解碼器
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c20a83f82e106bd749deb8bf2350cc9e5a347a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512460"
---
# <a name="h265--hevc-video-decoder"></a><span data-ttu-id="e7632-103">H. 265/HEVC 影片解碼器</span><span class="sxs-lookup"><span data-stu-id="e7632-103">H.265 / HEVC Video Decoder</span></span>

<span data-ttu-id="e7632-104">媒體基礎 .H 的視頻編碼程式是一種 [媒體基礎轉換](media-foundation-transforms.md) ，支援在附錄 B 格式中解碼 H. 265/HEVC 內容，並可用於播放數量和 .m2ts 檔案。</span><span class="sxs-lookup"><span data-stu-id="e7632-104">The Media Foundation H.265 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding H.265/HEVC content in Annex B format and can be used in playback of mp4 and m2ts files.</span></span>

<span data-ttu-id="e7632-105">H. 視頻解碼會公開下列介面。</span><span class="sxs-lookup"><span data-stu-id="e7632-105">The H.265 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="e7632-106">Windows 8) 支援的 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (</span><span class="sxs-lookup"><span data-stu-id="e7632-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="e7632-107">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="e7632-107">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="e7632-108">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="e7632-108">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="e7632-109">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="e7632-109">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="e7632-110">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="e7632-110">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="e7632-111">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="e7632-111">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="e7632-112">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="e7632-112">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="e7632-113">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="e7632-113">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="e7632-114">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="e7632-114">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="e7632-115">若要建立 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 或 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數的解碼器實例。</span><span class="sxs-lookup"><span data-stu-id="e7632-115">To create an instance of the decoder call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="input-types"></a><span data-ttu-id="e7632-116">輸入類型</span><span class="sxs-lookup"><span data-stu-id="e7632-116">Input Types</span></span>

<span data-ttu-id="e7632-117">輸入類型必須至少包含下列兩個屬性：</span><span class="sxs-lookup"><span data-stu-id="e7632-117">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="e7632-118">屬性</span><span class="sxs-lookup"><span data-stu-id="e7632-118">Attribute</span></span>                                                 | <span data-ttu-id="e7632-119">描述</span><span class="sxs-lookup"><span data-stu-id="e7632-119">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7632-120">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="e7632-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="e7632-121">**MFMediaType \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="e7632-121">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="e7632-122">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="e7632-122">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="e7632-123">[MFVideoFormat \_HEVC](video-subtype-guids.md) 或 MFVideoFormat \_ HEVC \_ ES</span><span class="sxs-lookup"><span data-stu-id="e7632-123">[MFVideoFormat\_HEVC](video-subtype-guids.md) or MFVideoFormat\_HEVC\_ES</span></span> |



 

<span data-ttu-id="e7632-124">第一個媒體子類型（MFVideoFormat \_ HEVC）指出媒體範例包含具有開始代碼的 h. 位流，且資料流程具有交錯的 SPS/PPS。</span><span class="sxs-lookup"><span data-stu-id="e7632-124">The first media subtype, MFVideoFormat\_HEVC, indicates that the media samples carry H.265 bitstream with start codes, and the stream has interleaved SPS/PPS.</span></span> <span data-ttu-id="e7632-125">它會假設每個樣本都有一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="e7632-125">It assumes one frame per sample.</span></span>

<span data-ttu-id="e7632-126">媒體子類型 MFVideoFormat \_ HEVC \_ ES 指出媒體範例包含基本的 h. 位流，其中每個範例可能包含部分圖片、多張圖片、某些圖片，以及部分圖片。</span><span class="sxs-lookup"><span data-stu-id="e7632-126">The media subtype MFVideoFormat\_ HEVC\_ES is to indicate the media samples carry elementary H.265 bitstream, where each sample may contain a partial picture, multiple pictures, some pictures plus a partial picture.</span></span>

<span data-ttu-id="e7632-127">輸入媒體類型無法在兩種類型之間動態變更。</span><span class="sxs-lookup"><span data-stu-id="e7632-127">The input media types cannot change dynamically between two types.</span></span> <span data-ttu-id="e7632-128">此解碼器可以根據基礎資料流程語法來偵測進行中的輸出格式變更 (外觀比例、維度、交錯旗標、colorimetry 資訊) 和觸發程式對應的輸出媒體類型變更。</span><span class="sxs-lookup"><span data-stu-id="e7632-128">The decoder can detect in-flight output format changes based on the elementary stream syntax (aspect ratio, dimension, interlace flags, colorimetry information) and trigger corresponding output media type changes.</span></span>

<span data-ttu-id="e7632-129">針對輸入媒體類型，解碼器預期來源必須設定正確的設定檔。</span><span class="sxs-lookup"><span data-stu-id="e7632-129">For input media type, the decoder expects the source to set the correct Profile.</span></span> <span data-ttu-id="e7632-130">例如，如果內容即將10位，則輸入媒體類型應將設定檔指定為 Main10。</span><span class="sxs-lookup"><span data-stu-id="e7632-130">For example if the content is going to be 10bit, input media type should specify the profile as Main10.</span></span>

## <a name="output-types"></a><span data-ttu-id="e7632-131">輸出型別</span><span class="sxs-lookup"><span data-stu-id="e7632-131">Output Types</span></span>

<span data-ttu-id="e7632-132">此解碼器支援下列輸出子類型：</span><span class="sxs-lookup"><span data-stu-id="e7632-132">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="e7632-133">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="e7632-133">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="e7632-134">**MFVideoFormat \_ P010**</span><span class="sxs-lookup"><span data-stu-id="e7632-134">**MFVideoFormat\_P010**</span></span>

<span data-ttu-id="e7632-135">如需這些子類型的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="e7632-135">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="e7632-136">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="e7632-136">Transform Attributes</span></span>

<span data-ttu-id="e7632-137">H. 解碼會實 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。</span><span class="sxs-lookup"><span data-stu-id="e7632-137">The H.265 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="e7632-138">應用程式可以使用這個方法來取得或設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="e7632-138">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="e7632-139">屬性</span><span class="sxs-lookup"><span data-stu-id="e7632-139">Attribute</span></span>                                                                                       | <span data-ttu-id="e7632-140">描述</span><span class="sxs-lookup"><span data-stu-id="e7632-140">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7632-141">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="e7632-141">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                     | <span data-ttu-id="e7632-142">啟用或停用低延遲解碼模式。</span><span class="sxs-lookup"><span data-stu-id="e7632-142">Enables or disables low-latency decoding mode.</span></span>                                                                                |
| [<span data-ttu-id="e7632-143">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="e7632-143">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                           | <span data-ttu-id="e7632-144">設定用於此解碼器的背景工作執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="e7632-144">Sets the number of worker threads used by the decoder.</span></span>                                                                        |
| [<span data-ttu-id="e7632-145">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="e7632-145">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="e7632-146">啟用或停用縮圖產生模式。</span><span class="sxs-lookup"><span data-stu-id="e7632-146">Enables or disables thumbnail generation mode.</span></span>                                                                                |
| [<span data-ttu-id="e7632-147">已 \_ 設定 MF NALU \_ 長度 \_</span><span class="sxs-lookup"><span data-stu-id="e7632-147">MF\_NALU\_LENGTH\_SET</span></span>](mf-nalu-length-set.md)                                                 | <span data-ttu-id="e7632-148">指出 NALU 長度資訊會以 BLOB 的形式傳送，每個壓縮的 h. 範例。</span><span class="sxs-lookup"><span data-stu-id="e7632-148">Indicates that NALU length information will be sent as a BLOB with each compressed H.265 sample.</span></span>                              |
| [<span data-ttu-id="e7632-149">MF \_ NALU \_ 長度 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="e7632-149">MF\_NALU\_LENGTH\_INFORMATION</span></span>](mf-nalu-length-information.md)                                 | <span data-ttu-id="e7632-150">指出範例中的 NALUs 長度。</span><span class="sxs-lookup"><span data-stu-id="e7632-150">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="e7632-151">這是在壓縮的輸入範例上設定為 .H 解碼的 MF BLOB。</span><span class="sxs-lookup"><span data-stu-id="e7632-151">This is a MF BLOB that is set on compressed input samples to the H.265 decoder.</span></span> |
| [<span data-ttu-id="e7632-152">MF \_ SA \_ 最小 \_ 輸出 \_ 範例 \_ 計數</span><span class="sxs-lookup"><span data-stu-id="e7632-152">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                 | <span data-ttu-id="e7632-153">指定輸出樣本的最大數目。</span><span class="sxs-lookup"><span data-stu-id="e7632-153">Specifies the maximum number of output samples.</span></span>                                                                               |



 

<span data-ttu-id="e7632-154">H. 265 解碼支援 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面。</span><span class="sxs-lookup"><span data-stu-id="e7632-154">The H.265 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="e7632-155">此介面提供 alternativate API 來設定下列編解碼器屬性。</span><span class="sxs-lookup"><span data-stu-id="e7632-155">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="e7632-156">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="e7632-156">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)
-   [<span data-ttu-id="e7632-157">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="e7632-157">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="e7632-158">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="e7632-158">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a><span data-ttu-id="e7632-159">格式條件約束</span><span class="sxs-lookup"><span data-stu-id="e7632-159">Format Constraints</span></span>

<span data-ttu-id="e7632-160">此解碼器支援下列格式：</span><span class="sxs-lookup"><span data-stu-id="e7632-160">The decoder supports the following formats:</span></span>



| <span data-ttu-id="e7632-161">需求</span><span class="sxs-lookup"><span data-stu-id="e7632-161">Requirement</span></span> | <span data-ttu-id="e7632-162">值</span><span class="sxs-lookup"><span data-stu-id="e7632-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7632-163">設定檔/層級</span><span class="sxs-lookup"><span data-stu-id="e7632-163">Profiles/Levels</span></span>    | <span data-ttu-id="e7632-164">主要、主要的圖片和 Main10 設定檔</span><span class="sxs-lookup"><span data-stu-id="e7632-164">Main, Main Still Picture, and Main10 profiles</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="e7632-165">色度格式</span><span class="sxs-lookup"><span data-stu-id="e7632-165">Chroma Formats</span></span>     | <span data-ttu-id="e7632-166">4:2:0 色度</span><span class="sxs-lookup"><span data-stu-id="e7632-166">4:2:0 chroma</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="e7632-167">最低解析度</span><span class="sxs-lookup"><span data-stu-id="e7632-167">Minimum Resolution</span></span> | <span data-ttu-id="e7632-168">48×48圖元</span><span class="sxs-lookup"><span data-stu-id="e7632-168">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e7632-169">最大解析度</span><span class="sxs-lookup"><span data-stu-id="e7632-169">Maximum Resolution</span></span> | <span data-ttu-id="e7632-170">4096×2304圖元</span><span class="sxs-lookup"><span data-stu-id="e7632-170">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="e7632-171">DXVA 加速的保證解析度上限為1920×1088圖元;在較高的解析度中，解碼是使用 DXVA 來完成（如果基礎硬體支援的話），否則會使用軟體進行解碼。</span><span class="sxs-lookup"><span data-stu-id="e7632-171">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/> |
| <span data-ttu-id="e7632-172">DXVA</span><span class="sxs-lookup"><span data-stu-id="e7632-172">DXVA</span></span>               | <span data-ttu-id="e7632-173">此解碼器支援 DX11 相互作用和 DX12 DXVA，但不支援 DXVA 第2版或 DXVA 第1版。</span><span class="sxs-lookup"><span data-stu-id="e7632-173">The decoder supports DX11 and DX12 DXVA, but not DXVA version 2 or DXVA version 1.</span></span>                                                                                                                                                                                                         |



 

<span data-ttu-id="e7632-174">輸入資料必須符合 ITU-T H 的附錄 B。 265 \| ISO/IEC 23008-2。</span><span class="sxs-lookup"><span data-stu-id="e7632-174">Input data must conform to Annex B of ITU-T H.265 \| ISO/IEC 23008-2.</span></span> <span data-ttu-id="e7632-175">資料必須包含起始碼。</span><span class="sxs-lookup"><span data-stu-id="e7632-175">The data must include the start codes.</span></span> <span data-ttu-id="e7632-176">除非在位元組資料流程中找到有效的 sequence 參數集 (SPS) 和圖片參數集 (PPS) ，否則此解碼器會略過位元組。</span><span class="sxs-lookup"><span data-stu-id="e7632-176">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7632-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7632-177">Requirements</span></span>



| <span data-ttu-id="e7632-178">需求</span><span class="sxs-lookup"><span data-stu-id="e7632-178">Requirement</span></span> | <span data-ttu-id="e7632-179">值</span><span class="sxs-lookup"><span data-stu-id="e7632-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7632-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7632-180">Minimum supported client</span></span><br/> | <span data-ttu-id="e7632-181">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7632-181">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e7632-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7632-182">Minimum supported server</span></span><br/> | <span data-ttu-id="e7632-183">都不支援</span><span class="sxs-lookup"><span data-stu-id="e7632-183">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e7632-184">DLL</span><span class="sxs-lookup"><span data-stu-id="e7632-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7632-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7632-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7632-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7632-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7632-187">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="e7632-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
