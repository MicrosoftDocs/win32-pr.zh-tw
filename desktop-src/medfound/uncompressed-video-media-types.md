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
# <a name="uncompressed-video-media-types"></a>未壓縮的影片媒體類型

本主題說明如何建立描述未壓縮影片格式的媒體類型。 如需有關媒體類型的詳細資訊，請參閱 [關於媒體類型](about-media-types.md)。

若要建立完整的未壓縮影片類型，請在 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面指標上設定下列屬性。



| 屬性                                                                            | 描述                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md)                            | 主要類型。 設定為 **MFMediaType \_ Video**。                                                                                                                                                                                          |
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)                                   | 亞。 請參閱 [影片子類型 guid](video-subtype-guids.md)。                                                                                                                                                                        |
| [**MF \_ MT \_ 預設 \_ STRIDE**](mf-mt-default-stride-attribute.md)                    | 介面 stride。 *Stride* 是從一個圖元到下一個資料列所需的位元組數目。 如果位元組跨距與影片寬度不同（以位元組為單位），請設定此屬性。 否則，您可以省略此屬性。 |
| [**MF \_ MT \_ 幀 \_ 速率**](mf-mt-frame-rate-attribute.md)                            | 畫面播放速率。                                                                                                                                                                                                                         |
| [**MF \_ MT \_ 框架 \_ 大小**](mf-mt-frame-size-attribute.md)                            | 框架大小。                                                                                                                                                                                                                         |
| [**MF \_ MT \_ 交錯 \_ 模式**](mf-mt-interlace-mode-attribute.md)                    | 交錯模式。                                                                                                                                                                                                                   |
| [**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**](mf-mt-all-samples-independent-attribute.md) | 指定每個範例是否獨立。 針對未壓縮的格式，請設定為 **TRUE** 。                                                                                                                                             |
| [**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**](mf-mt-pixel-aspect-ratio-attribute.md)           | 圖元外觀比例。                                                                                                                                                                                                                 |



 

此外，如果您知道正確的值，請設定下列屬性。  (否則，請省略這些屬性。 ) 



| 屬性                                                                    | 描述        |
|------------------------------------------------------------------------------|--------------------|
| [**MF \_ MT \_ 影片 \_ 主要複本**](mf-mt-video-primaries-attribute.md)          | 色彩主要複本。   |
| [**MF \_ MT \_ 傳送函式 \_**](mf-mt-transfer-function-attribute.md)      | Transfer 函數。 |
| [**MF \_ MT \_ YUV \_ 矩陣**](mf-mt-yuv-matrix-attribute.md)                    | 轉移矩陣。   |
| [**MF \_ MT \_ 視頻 \_ 色度 \_ 地點**](mf-mt-video-chroma-siting-attribute.md) | 色度地點。     |
| [**MF \_ MT \_ 影片 \_ 名義 \_ 範圍**](mf-mt-video-nominal-range-attribute.md) | 名義範圍。     |



 

如需詳細資訊，請參閱 [擴充色彩資訊](extended-color-information.md)。 例如，如果您建立一個描述影片標準的媒體類型，而標準定義了色度地點，請將此資訊新增至媒體類型。 這麼做有助於保持整個管線的色彩精確度。

建立影片媒體類型時，下列功能可能很有用。



| 函式                                                                     | 描述                                                                                                                                                                          |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | 計算畫面播放速率（指定平均幀持續時間）。                                                                                                                         |
| [**MFCalculateImageSize**](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | 計算未壓縮影片格式的影像大小。                                                                                                                          |
| [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | 根據畫面播放速率計算影片框架的平均持續時間。                                                                                                              |
| [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | 傳回影片格式的最小表面 stride。 如需詳細資訊，請參閱 [影像 Stride](image-stride.md)。                                                                   |
| [**MFInitVideoFormat**](/windows/desktop/api/mfapi/nf-mfapi-mfinitvideoformat)                               | 針對一些標準的影片格式（例如 NTSC 電視），初始化 [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) 結構。 然後，您可以使用此結構來初始化媒體類型。 |
| [**MFIsFormatYUV**](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | 查詢影片格式是否為 YUV 格式。                                                                                                                                      |



 

## <a name="examples"></a>範例

此範例顯示的函式會針對未壓縮的影片格式填滿最常見的資訊。 函數會傳回 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面指標。 然後，您可以視需要將其他屬性新增至媒體類型。


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



下一個範例會採用編碼的影片格式作為輸入，並建立相符的未壓縮影片類型。 例如，此類型適合在編碼器或解碼器上設定。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[擴充的色彩資訊](extended-color-information.md)
</dt> <dt>

[影像 Stride](image-stride.md)
</dt> <dt>

[媒體類型](media-types.md)
</dt> <dt>

[影片媒體類型](video-media-types.md)
</dt> <dt>

[影片子類型 Guid](video-subtype-guids.md)
</dt> </dl>

 

 



