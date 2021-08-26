---
description: 媒體類型轉換
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: 媒體類型轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5d91844a062d5d4a1aa98af1a2e77c9cabfadb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474344"
---
# <a name="media-type-conversions"></a>媒體類型轉換

有時候，您必須從 DirectShow 或 Windows 媒體格式 SDK，在媒體基礎媒體類型與較舊的媒體類型結構之間進行轉換。

### <a name="from-a-format-structure-to-a-media-foundation-type"></a>從格式結構到媒體基礎類型

下列函式會從格式結構初始化媒體基礎的媒體類型。 如果資料流程或檔案標頭包含格式結構，這些函數也很有用。 例如，WAVE 音訊檔案的 file 標頭包含 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構。




| 要轉換的結構 | 函數 | 
|----------------------|----------|
| <a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow) <br /><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (DirectX 媒體物件)  <br /><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows 媒體格式 SDK)  <br /><blockquote>[!Note]<br />這些結構是相等的。</blockquote><br /><br /> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a> | 
| <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a> | 
| <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a> | 
| <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a> | 
| <a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a>或<a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>WAVEFORMATEXTENSIBLE</strong></a> | <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a> | 




 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a>從媒體基礎類型到格式結構

下列函式會建立或初始化媒體基礎媒體類型的格式結構。



| 函數                                                                             | 目標結構                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | [**AM \_媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)、 [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)、 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)或 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) |
| [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [**\_媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [**MFCreateMFVideoFormatFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))或 [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))                                                                                    |
| [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [**\_媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a>格式對應

下表列出對應至各種格式結構的媒體基礎屬性。 並非所有這些屬性都可以直接轉譯。 若要執行轉換，您應該使用上一節所列的函式;這些資料表主要是供參考之用。

### <a name="am_media_type"></a>\_媒體 \_ 類型



| 成員                   | 屬性                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| **bTemporalCompression** | [**MF \_ MT \_ 所有 \_ 範例 \_ 獨立**](mf-mt-all-samples-independent-attribute.md) |
| **bFixedSizeSamples**    | [**MF \_ MT \_ 固定 \_ 大小 \_ 範例**](mf-mt-fixed-size-samples-attribute.md)           |
| **lSampleSize**          | [**MF \_ MT \_ 樣本 \_ 大小**](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a>WAVEFORMATEX, WAVEFORMATEXTENSIBLE



| 成員                  | 屬性                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wFormatTag**          | [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)<br/> 如果 **wFormatTag** 是 WAVE 格式可延伸的 \_ \_ ，子類型會在 **SubFormat** 成員中找到。<br/> |
| **nChannels**           | [**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| **nSamplesPerSec**      | [**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| **nAvgBytesPerSec**     | [**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| **nBlockAlign**         | [**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| **wBitsPerSample**      | [**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| **wValidBitsPerSample** | [**\_ \_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊有效位數**](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| **wSamplesPerBlock**    | [**\_ \_ \_ \_ 每個 \_ 區塊的 MF MT 音訊範例**](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| **dwChannelMask**       | [**MF \_ MT \_ 音訊 \_ 通道 \_ 遮罩**](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| **SubFormat**           | [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)                                                                                                                        |
| 額外的資料              | [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a>VIDEOINFOHEADER, VIDEOINFOHEADER2



| 成員                                         | 屬性                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwBitRate**                                  | [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| **dwBitErrorRate**                             | [**MF \_ MT \_ 平均 \_ 位 \_ 誤差 \_ 率**](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| **AvgTimePerFrame**                            | [**MF \_MT \_ 幀 \_ 速率**](mf-mt-frame-rate-attribute.md); 使用 [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) 來計算這個值。                                                                             |
| **dwInterlaceFlags**                           | [**MF \_ MT \_ 交錯 \_ 模式**](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| **dwCopyProtectFlags**                         | 沒有任何定義的對等專案                                                                                                                                                                                                                            |
| **dwPictAspectRatioX**、 **dwPictAspectRatioY** | [**MF \_MT \_ 圖元 \_ 外觀 \_ 比例**](mf-mt-pixel-aspect-ratio-attribute.md); 必須從圖片外觀比例轉換成圖片外觀比例。                                                                                                      |
| **dwControlFlags**                             | [**MF \_MT \_ 板 \_ 控制項 \_ 旗標**](mf-mt-pad-control-flags-attribute.md)。 如果出現 **AMCONTROL \_ COLORINFO \_** 的旗標，請設定 [擴充色彩資訊](extended-color-information.md)中所述的擴充色彩屬性。 |
| **bmiHeader. biWidth**、 **bmiHeader. biHeight**  | [**MF \_ MT \_ 框架 \_ 大小**](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| **bmiHeader.biBitCount**                       | 子類型中的隱含 ([**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)) 。                                                                                                                                                                    |
| **bmiHeader.biCompression**                    | 子類型中的隱含。                                                                                                                                                                                                                         |
| **bmiHeader.biSizeImage**                      | [**MF \_ MT \_ 樣本 \_ 大小**](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| 調色板資訊                            | [**MF \_ MT \_ 調色板**](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

下列屬性可以從 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 或 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 結構推斷，但也需要一些格式詳細資料的知識。 例如，不同的 YUV 格式具有不同的 stride 需求。

-   [**MF \_ MT \_ 預設 \_ STRIDE**](mf-mt-default-stride-attribute.md)
-   [**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**](mf-mt-minimum-display-aperture-attribute.md)
-   [**MF \_ MT \_ 平移 \_ 掃描 \_ 光圈**](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a>MPEG1VIDEOINFO



| 成員                                   | 屬性                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**                      | [**MF \_ MT \_ MPEG \_ 開始 \_ 時間 \_ 代碼**](mf-mt-mpeg-start-time-code-attribute.md) |
| **bSequenceHeader**                      | [**MF \_ MT \_ MPEG \_ 序列 \_ 標頭**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **biXPelsPerMeter**、 **biYPelsPerMeter** | [**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a>MPEG2VIDEOINFO



| 成員               | 屬性                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**  | [**MF \_ MT \_ MPEG \_ 開始 \_ 時間 \_ 代碼**](mf-mt-mpeg-start-time-code-attribute.md) |
| **dwSequenceHeader** | [**MF \_ MT \_ MPEG \_ 序列 \_ 標頭**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **dwProfile**        | [**MF \_ MT \_ MPEG2 \_ 設定檔**](mf-mt-mpeg2-profile-attribute.md)                 |
| **dwLevel**          | [**MF \_ MT \_ MPEG2 \_ 層級**](mf-mt-mpeg2-level-attribute.md)                     |
| **dwFlags**          | [**MF \_ MT \_ MPEG2 \_ 旗標**](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a>範例

下列程式碼會從影片媒體類型填入 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。 請注意，這項轉換會遺失部分格式資訊 (交錯、畫面播放速率、擴充色彩資料) 。 不過，這在從影片框架儲存點陣圖時可能很有用。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體類型](media-types.md)
</dt> </dl>

 

 
