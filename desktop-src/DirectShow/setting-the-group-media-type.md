---
description: 設定群組媒體類型
ms.assetid: 05f0fdcb-74a4-441e-ac3c-d3d2c1dfee80
title: 設定群組媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c758e089a4f1240debb14c8159d039380b3473991860fef54470c12c1c00b1e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928178"
---
# <a name="setting-the-group-media-type"></a>設定群組媒體類型

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

所有群組都必須定義未壓縮的媒體類型，也就是音訊或影片。 未壓縮的媒體類型是檢視器在播放期間看到或聽到的格式。 通常，最後的輸出會是壓縮格式。 如需詳細資訊，請參閱轉譯[Project](rendering-a-project.md)。

若要設定未壓縮的格式，請建立 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構，並以適當的主要類型、子類型和格式標頭填入該結構。 針對影片，配置格式區塊的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構，並設定寬度、高度和位深度。 針對音訊，配置格式區塊的 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構，並設定取樣率、位深度和通道數目。 如果您只設定主要類型，DES 會為其他值提供合理的預設值。 在實務上，您應該明確地設定值以控制輸出。

在您初始化媒體類型結構之後，請呼叫 [**IAMTimelineGroup：： SetMediaType**](iamtimelinegroup-setmediatype.md) 方法來設定群組的媒體類型。

下列範例會指定16位 RGB 影片，320圖元寬乘以240圖元高：


```C++
AM_MEDIA_TYPE mtGroup;  
mtGroup.majortype = MEDIATYPE_Video;
mtGroup.subtype = MEDIASUBTYPE_RGB555;

// Set format headers.
mtGroup.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(VIDEOINFOHEADER));
if (mtGroup.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}

VIDEOINFOHEADER *pVideoHeader = (VIDEOINFOHEADER*)mtGroup.pbFormat;
ZeroMemory(pVideoHeader, sizeof(VIDEOINFOHEADER));
pVideoHeader->bmiHeader.biBitCount = 16;
pVideoHeader->bmiHeader.biWidth = 320;
pVideoHeader->bmiHeader.biHeight = 240;
pVideoHeader->bmiHeader.biPlanes = 1;
pVideoHeader->bmiHeader.biSize = sizeof(BITMAPINFOHEADER);
pVideoHeader->bmiHeader.biSizeImage = DIBSIZE(pVideoHeader->bmiHeader);

// Set the format type and size.
mtGroup.formattype = FORMAT_VideoInfo;
mtGroup.cbFormat = sizeof(VIDEOINFOHEADER);

// Set the sample size.
mtGroup.bFixedSizeSamples = TRUE;
mtGroup.lSampleSize = DIBSIZE(pVideoHeader->bmiHeader);

// Now use this media type for the group.
pGroup->SetMediaType(&mtGroup);

// Clean up.
CoTaskMemFree(mtGroup.pbFormat);
```



下一個範例會將群組媒體類型設定為16位身歷聲、每秒44100個樣本，以指定音訊群組：


```C++
AM_MEDIA_TYPE mt;  
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));

mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.formattype = FORMAT_WaveFormatEx;

// Set format block.
mt.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(WAVEFORMATEX));
if (mt.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}
mt.cbFormat = sizeof(WAVEFORMATEX);

// Fill in the WAVEFORMATEX structure.
WAVEFORMATEX *wave = (WAVEFORMATEX*) mt.pbFormat;
wave->wFormatTag = WAVE_FORMAT_PCM;
wave->nChannels = 2;  // Stereo
wave->nSamplesPerSec = 44100;
wave->wBitsPerSample = 16;
wave->nBlockAlign = wave->nChannels * wave->wBitsPerSample/8;
wave->nAvgBytesPerSec = wave->nSamplesPerSec * wave->nBlockAlign; 
wave->cbSize = 0;

hr = pGroup->SetMediaType(&mt);
CoTaskMemFree(mt.pbFormat);
```



您也可以使用 [DirectShow 基類](directshow-base-classes.md)中的 [**CMediaType**](cmediatype.md)類別來管理媒體類型。 它包含一些實用的 helper 方法，並且會自動釋放格式區塊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於媒體類型](about-media-types.md)
</dt> <dt>

[建立時間軸](constructing-a-timeline.md)
</dt> </dl>

 

 
