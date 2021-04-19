---
description: 設定群組媒體類型
ms.assetid: 05f0fdcb-74a4-441e-ac3c-d3d2c1dfee80
title: 設定群組媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365bd2171100a9d4bcfc48d70dbeb94d8a6639dd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106997315"
---
# <a name="setting-the-group-media-type"></a><span data-ttu-id="db441-103">設定群組媒體類型</span><span class="sxs-lookup"><span data-stu-id="db441-103">Setting the Group Media Type</span></span>

<span data-ttu-id="db441-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="db441-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="db441-105">所有群組都必須定義未壓縮的媒體類型，也就是音訊或影片。</span><span class="sxs-lookup"><span data-stu-id="db441-105">All groups must define an uncompressed media type, either audio or video.</span></span> <span data-ttu-id="db441-106">未壓縮的媒體類型是檢視器在播放期間看到或聽到的格式。</span><span class="sxs-lookup"><span data-stu-id="db441-106">The uncompressed media type is the format that viewers see or hear during playback.</span></span> <span data-ttu-id="db441-107">通常，最後的輸出會是壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="db441-107">Typically, the final output will be in a compressed format.</span></span> <span data-ttu-id="db441-108">如需詳細資訊，請參閱 [呈現專案](rendering-a-project.md)。</span><span class="sxs-lookup"><span data-stu-id="db441-108">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="db441-109">若要設定未壓縮的格式，請建立 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構，並以適當的主要類型、子類型和格式標頭填入該結構。</span><span class="sxs-lookup"><span data-stu-id="db441-109">To set the uncompressed format, create an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and fill it with the appropriate major type, subtype, and format header.</span></span> <span data-ttu-id="db441-110">針對影片，配置格式區塊的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構，並設定寬度、高度和位深度。</span><span class="sxs-lookup"><span data-stu-id="db441-110">For video, allocate a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure for the format block, and set the width, height, and bit depth.</span></span> <span data-ttu-id="db441-111">針對音訊，配置格式區塊的 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構，並設定取樣率、位深度和通道數目。</span><span class="sxs-lookup"><span data-stu-id="db441-111">For audio, allocate a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure for the format block, and set the sample rate, bit depth, and number of channels.</span></span> <span data-ttu-id="db441-112">如果您只設定主要類型，DES 會為其他值提供合理的預設值。</span><span class="sxs-lookup"><span data-stu-id="db441-112">If you set just the major type, DES provides reasonable defaults for the other values.</span></span> <span data-ttu-id="db441-113">在實務上，您應該明確地設定值以控制輸出。</span><span class="sxs-lookup"><span data-stu-id="db441-113">In practice, you should set the values explicitly to control the output.</span></span>

<span data-ttu-id="db441-114">在您初始化媒體類型結構之後，請呼叫 [**IAMTimelineGroup：： SetMediaType**](iamtimelinegroup-setmediatype.md) 方法來設定群組的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="db441-114">After you initialize the media type structure, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method to set the media type for the group.</span></span>

<span data-ttu-id="db441-115">下列範例會指定16位 RGB 影片，320圖元寬乘以240圖元高：</span><span class="sxs-lookup"><span data-stu-id="db441-115">The following example specifies 16-bit RGB video, 320 pixels wide by 240 pixels high:</span></span>


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



<span data-ttu-id="db441-116">下一個範例會將群組媒體類型設定為16位身歷聲、每秒44100個樣本，以指定音訊群組：</span><span class="sxs-lookup"><span data-stu-id="db441-116">The next example specifies an audio group, by setting the group media type to 16-bit stereo, 44100 samples per second:</span></span>


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



<span data-ttu-id="db441-117">您也可以使用 [DirectShow 基類](directshow-base-classes.md)中的 [**CMediaType**](cmediatype.md)類別來管理媒體類型。</span><span class="sxs-lookup"><span data-stu-id="db441-117">You can also use the [**CMediaType**](cmediatype.md) class in the [DirectShow Base Classes](directshow-base-classes.md) to manage media types.</span></span> <span data-ttu-id="db441-118">它包含一些實用的 helper 方法，並且會自動釋放格式區塊。</span><span class="sxs-lookup"><span data-stu-id="db441-118">It contains some useful helper methods, and automatically releases the format block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db441-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="db441-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db441-120">關於媒體類型</span><span class="sxs-lookup"><span data-stu-id="db441-120">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="db441-121">建立時間軸</span><span class="sxs-lookup"><span data-stu-id="db441-121">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
