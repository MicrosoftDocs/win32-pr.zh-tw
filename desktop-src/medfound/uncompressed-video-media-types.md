---
description: 未壓縮的影片媒體類型
ms.assetid: 50bf2947-27ee-4092-9d3a-a1c13ee80e95
title: 未壓縮的影片媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c90a48aed62f22a492ac22dae93761c1046750a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514320"
---
# <a name="uncompressed-video-media-types"></a><span data-ttu-id="6293a-103">未壓縮的影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="6293a-103">Uncompressed Video Media Types</span></span>

<span data-ttu-id="6293a-104">本主題說明如何建立描述未壓縮影片格式的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6293a-104">This topic describes how to create a media type that describes an uncompressed video format.</span></span> <span data-ttu-id="6293a-105">如需有關媒體類型的詳細資訊，請參閱 [關於媒體類型](about-media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="6293a-105">For more information about media types generally, see [About Media Types](about-media-types.md).</span></span>

<span data-ttu-id="6293a-106">若要建立完整的未壓縮影片類型，請在 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面指標上設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="6293a-106">To create a complete uncompressed video type, set the following attributes on the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span>



| <span data-ttu-id="6293a-107">屬性</span><span class="sxs-lookup"><span data-stu-id="6293a-107">Attribute</span></span>                                                                            | <span data-ttu-id="6293a-108">描述</span><span class="sxs-lookup"><span data-stu-id="6293a-108">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6293a-109">**MF \_ MT \_ 主要 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6293a-109">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="6293a-110">主要類型。</span><span class="sxs-lookup"><span data-stu-id="6293a-110">Major type.</span></span> <span data-ttu-id="6293a-111">設定為 **MFMediaType \_ Video**。</span><span class="sxs-lookup"><span data-stu-id="6293a-111">Set to **MFMediaType\_Video**.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="6293a-112">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="6293a-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                   | <span data-ttu-id="6293a-113">亞。</span><span class="sxs-lookup"><span data-stu-id="6293a-113">Subtype.</span></span> <span data-ttu-id="6293a-114">請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="6293a-114">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="6293a-115">**MF \_ MT \_ 預設 \_ STRIDE**</span><span class="sxs-lookup"><span data-stu-id="6293a-115">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)                    | <span data-ttu-id="6293a-116">介面 stride。</span><span class="sxs-lookup"><span data-stu-id="6293a-116">Surface stride.</span></span> <span data-ttu-id="6293a-117">*Stride* 是從一個圖元到下一個資料列所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="6293a-117">The *stride* is the number of bytes needed to go from one row of pixels to the next.</span></span> <span data-ttu-id="6293a-118">如果位元組跨距與影片寬度不同（以位元組為單位），請設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="6293a-118">Set this attribute if the stride in bytes is not the same as the video width in bytes.</span></span> <span data-ttu-id="6293a-119">否則，您可以省略此屬性。</span><span class="sxs-lookup"><span data-stu-id="6293a-119">Otherwise, you can omit this attribute.</span></span> |
| [<span data-ttu-id="6293a-120">**MF \_ MT \_ 幀 \_ 速率**</span><span class="sxs-lookup"><span data-stu-id="6293a-120">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)                            | <span data-ttu-id="6293a-121">畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="6293a-121">Frame rate.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="6293a-122">**MF \_ MT \_ 框架 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="6293a-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                            | <span data-ttu-id="6293a-123">框架大小。</span><span class="sxs-lookup"><span data-stu-id="6293a-123">Frame size.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="6293a-124">**MF \_ MT \_ 交錯 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="6293a-124">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                    | <span data-ttu-id="6293a-125">交錯模式。</span><span class="sxs-lookup"><span data-stu-id="6293a-125">Interlacing mode.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="6293a-126">**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**</span><span class="sxs-lookup"><span data-stu-id="6293a-126">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="6293a-127">指定每個範例是否獨立。</span><span class="sxs-lookup"><span data-stu-id="6293a-127">Specifies whether each sample is independent.</span></span> <span data-ttu-id="6293a-128">針對未壓縮的格式，請設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="6293a-128">Set to **TRUE** for uncompressed formats.</span></span>                                                                                                                                             |
| [<span data-ttu-id="6293a-129">**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**</span><span class="sxs-lookup"><span data-stu-id="6293a-129">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)           | <span data-ttu-id="6293a-130">圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="6293a-130">Pixel aspect ratio.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="6293a-131">此外，如果您知道正確的值，請設定下列屬性。</span><span class="sxs-lookup"><span data-stu-id="6293a-131">In addition, set the following attributes if you know the correct values.</span></span> <span data-ttu-id="6293a-132"> (否則，請省略這些屬性。 ) </span><span class="sxs-lookup"><span data-stu-id="6293a-132">(Otherwise, omit these attributes.)</span></span>



| <span data-ttu-id="6293a-133">屬性</span><span class="sxs-lookup"><span data-stu-id="6293a-133">Attribute</span></span>                                                                    | <span data-ttu-id="6293a-134">描述</span><span class="sxs-lookup"><span data-stu-id="6293a-134">Description</span></span>        |
|------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="6293a-135">**MF \_ MT \_ 影片 \_ 主要複本**</span><span class="sxs-lookup"><span data-stu-id="6293a-135">**MF\_MT\_VIDEO\_PRIMARIES**</span></span>](mf-mt-video-primaries-attribute.md)          | <span data-ttu-id="6293a-136">色彩主要複本。</span><span class="sxs-lookup"><span data-stu-id="6293a-136">Color primaries.</span></span>   |
| [<span data-ttu-id="6293a-137">**MF \_ MT \_ 傳送函式 \_**</span><span class="sxs-lookup"><span data-stu-id="6293a-137">**MF\_MT\_TRANSFER\_FUNCTION**</span></span>](mf-mt-transfer-function-attribute.md)      | <span data-ttu-id="6293a-138">Transfer 函數。</span><span class="sxs-lookup"><span data-stu-id="6293a-138">Transfer function.</span></span> |
| [<span data-ttu-id="6293a-139">**MF \_ MT \_ YUV \_ 矩陣**</span><span class="sxs-lookup"><span data-stu-id="6293a-139">**MF\_MT\_YUV\_MATRIX**</span></span>](mf-mt-yuv-matrix-attribute.md)                    | <span data-ttu-id="6293a-140">轉移矩陣。</span><span class="sxs-lookup"><span data-stu-id="6293a-140">Transfer matrix.</span></span>   |
| [<span data-ttu-id="6293a-141">**MF \_ MT \_ 視頻 \_ 色度 \_ 地點**</span><span class="sxs-lookup"><span data-stu-id="6293a-141">**MF\_MT\_VIDEO\_CHROMA\_SITING**</span></span>](mf-mt-video-chroma-siting-attribute.md) | <span data-ttu-id="6293a-142">色度地點。</span><span class="sxs-lookup"><span data-stu-id="6293a-142">Chroma siting.</span></span>     |
| [<span data-ttu-id="6293a-143">**MF \_ MT \_ 影片 \_ 名義 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="6293a-143">**MF\_MT\_VIDEO\_NOMINAL\_RANGE**</span></span>](mf-mt-video-nominal-range-attribute.md) | <span data-ttu-id="6293a-144">名義範圍。</span><span class="sxs-lookup"><span data-stu-id="6293a-144">Nominal range.</span></span>     |



 

<span data-ttu-id="6293a-145">如需詳細資訊，請參閱 [擴充色彩資訊](extended-color-information.md)。</span><span class="sxs-lookup"><span data-stu-id="6293a-145">For more information, see [Extended Color Information](extended-color-information.md).</span></span> <span data-ttu-id="6293a-146">例如，如果您建立一個描述影片標準的媒體類型，而標準定義了色度地點，請將此資訊新增至媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6293a-146">For example, if you create a media type that describes a video standard, and the standard defines the chroma siting, add this information to the media type.</span></span> <span data-ttu-id="6293a-147">這麼做有助於保持整個管線的色彩精確度。</span><span class="sxs-lookup"><span data-stu-id="6293a-147">Doing so helps to preserve color fidelity throughout the pipeline.</span></span>

<span data-ttu-id="6293a-148">建立影片媒體類型時，下列功能可能很有用。</span><span class="sxs-lookup"><span data-stu-id="6293a-148">The following functions might be useful when creating a video media type.</span></span>



| <span data-ttu-id="6293a-149">函式</span><span class="sxs-lookup"><span data-stu-id="6293a-149">Function</span></span>                                                                     | <span data-ttu-id="6293a-150">描述</span><span class="sxs-lookup"><span data-stu-id="6293a-150">Description</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6293a-151">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="6293a-151">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="6293a-152">計算畫面播放速率（指定平均幀持續時間）。</span><span class="sxs-lookup"><span data-stu-id="6293a-152">Calculates the frame rate, given the average frame duration.</span></span>                                                                                                                         |
| [<span data-ttu-id="6293a-153">**MFCalculateImageSize**</span><span class="sxs-lookup"><span data-stu-id="6293a-153">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="6293a-154">計算未壓縮影片格式的影像大小。</span><span class="sxs-lookup"><span data-stu-id="6293a-154">Calculates the image size for an uncompressed video format.</span></span>                                                                                                                          |
| [<span data-ttu-id="6293a-155">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="6293a-155">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="6293a-156">根據畫面播放速率計算影片框架的平均持續時間。</span><span class="sxs-lookup"><span data-stu-id="6293a-156">Calculates the average duration of a video frame, given the frame rate.</span></span>                                                                                                              |
| [<span data-ttu-id="6293a-157">**MFGetStrideForBitmapInfoHeader**</span><span class="sxs-lookup"><span data-stu-id="6293a-157">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="6293a-158">傳回影片格式的最小表面 stride。</span><span class="sxs-lookup"><span data-stu-id="6293a-158">Returns the minimum surface stride for a video format.</span></span> <span data-ttu-id="6293a-159">如需詳細資訊，請參閱 [影像 Stride](image-stride.md)。</span><span class="sxs-lookup"><span data-stu-id="6293a-159">For more information, see [Image Stride](image-stride.md).</span></span>                                                                   |
| [<span data-ttu-id="6293a-160">**MFInitVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="6293a-160">**MFInitVideoFormat**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | <span data-ttu-id="6293a-161">針對一些標準的影片格式（例如 NTSC 電視），初始化 [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) 結構。</span><span class="sxs-lookup"><span data-stu-id="6293a-161">Initializes an [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) structure for some standard video formats, such as NTSC television.</span></span> <span data-ttu-id="6293a-162">然後，您可以使用此結構來初始化媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6293a-162">You can then use the structure to initialize a media type.</span></span> |
| [<span data-ttu-id="6293a-163">**MFIsFormatYUV**</span><span class="sxs-lookup"><span data-stu-id="6293a-163">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="6293a-164">查詢影片格式是否為 YUV 格式。</span><span class="sxs-lookup"><span data-stu-id="6293a-164">Queries whether a video format is a YUV format.</span></span>                                                                                                                                      |



 

## <a name="examples"></a><span data-ttu-id="6293a-165">範例</span><span class="sxs-lookup"><span data-stu-id="6293a-165">Examples</span></span>

<span data-ttu-id="6293a-166">此範例顯示的函式會針對未壓縮的影片格式填滿最常見的資訊。</span><span class="sxs-lookup"><span data-stu-id="6293a-166">This example shows a function that fills in the most common information for an uncompressed video format.</span></span> <span data-ttu-id="6293a-167">函數會傳回 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="6293a-167">The function returns an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface pointer.</span></span> <span data-ttu-id="6293a-168">然後，您可以視需要將其他屬性新增至媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6293a-168">You can then add additional attributes to the media type as needed.</span></span>


```C++
HRESULT CreateUncompressedVideoType(
    DWORD                fccFormat,  // FOURCC or D3DFORMAT value.     
    UINT32               width, 
    UINT32               height,
    MFVideoInterlaceMode interlaceMode,
    const MFRatio&       frameRate,
    const MFRatio&       par,
    IMFMediaType         **ppType
    )
{
    if (ppType == NULL)
    {
        return E_POINTER;
    }

    GUID    subtype = MFVideoFormat_Base;
    LONG    lStride = 0;
    UINT    cbImage = 0;

    IMFMediaType *pType = NULL;

    // Set the subtype GUID from the FOURCC or D3DFORMAT value.
    subtype.Data1 = fccFormat;

    HRESULT hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_INTERLACE_MODE, interlaceMode);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the default stride value.
    hr = pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    if (FAILED(hr))
    {
        goto done;
    }

    // Calculate the image size in bytes.
    hr = MFCalculateImageSize(subtype, width, height, &cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_SAMPLE_SIZE, cbImage);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_FIXED_SIZE_SAMPLES, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Frame rate
    hr = MFSetAttributeRatio(pType, MF_MT_FRAME_RATE, frameRate.Numerator, 
        frameRate.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Pixel aspect ratio
    hr = MFSetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, par.Numerator, 
        par.Denominator);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppType = pType;
    (*ppType)->AddRef();

done:
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="6293a-169">下一個範例會採用編碼的影片格式作為輸入，並建立相符的未壓縮影片類型。</span><span class="sxs-lookup"><span data-stu-id="6293a-169">The next example takes an encoded video format as input, and creates a matching uncompressed video type.</span></span> <span data-ttu-id="6293a-170">例如，此類型適合在編碼器或解碼器上設定。</span><span class="sxs-lookup"><span data-stu-id="6293a-170">This type would be suitable to set on an encoder or decoder, for example.</span></span>


```C++
HRESULT ConvertVideoTypeToUncompressedType(
    IMFMediaType *pType,    // Pointer to an encoded video type.
    const GUID& subtype,    // Uncompressed subtype (eg, RGB-32, AYUV)
    IMFMediaType **ppType   // Receives a matching uncompressed video type.
    )
{
    IMFMediaType *pTypeUncomp = NULL;

    HRESULT hr = S_OK;
    GUID majortype = { 0 };
    MFRatio par = { 0 };

    hr = pType->GetMajorType(&majortype);

    if (majortype != MFMediaType_Video)
    {
        return MF_E_INVALIDMEDIATYPE;
    }

    // Create a new media type and copy over all of the items.
    // This ensures that extended color information is retained.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pTypeUncomp);
    }

    if (SUCCEEDED(hr))
    {
        hr = pType->CopyAllItems(pTypeUncomp);
    }

    // Set the subtype.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetGUID(MF_MT_SUBTYPE, subtype);
    }

    // Uncompressed means all samples are independent.
    if (SUCCEEDED(hr))
    {
        hr = pTypeUncomp->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
    }

    // Fix up PAR if not set on the original type.
    if (SUCCEEDED(hr))
    {
        hr = MFGetAttributeRatio(
            pTypeUncomp, 
            MF_MT_PIXEL_ASPECT_RATIO, 
            (UINT32*)&par.Numerator, 
            (UINT32*)&par.Denominator
            );

        // Default to square pixels.
        if (FAILED(hr))
        {
            hr = MFSetAttributeRatio(
                pTypeUncomp, 
                MF_MT_PIXEL_ASPECT_RATIO, 
                1, 1
                );
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppType = pTypeUncomp;
        (*ppType)->AddRef();
    }

    SafeRelease(&pTypeUncomp);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="6293a-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="6293a-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6293a-172">擴充的色彩資訊</span><span class="sxs-lookup"><span data-stu-id="6293a-172">Extended Color Information</span></span>](extended-color-information.md)
</dt> <dt>

[<span data-ttu-id="6293a-173">影像 Stride</span><span class="sxs-lookup"><span data-stu-id="6293a-173">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="6293a-174">媒體類型</span><span class="sxs-lookup"><span data-stu-id="6293a-174">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="6293a-175">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="6293a-175">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="6293a-176">影片子類型 Guid</span><span class="sxs-lookup"><span data-stu-id="6293a-176">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 



