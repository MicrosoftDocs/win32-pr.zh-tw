---
description: 深入瞭解 DirectShow 中的媒體類型。 媒體類型是用來描述數位媒體格式的通用且可擴充的方式。
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: '關於媒體類型 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b1489543b33f5eeb2c288add48148b37f31915
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010891"
---
# <a name="about-media-types-directshow"></a><span data-ttu-id="3c06d-104">關於媒體類型 (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="3c06d-104">About Media Types (DirectShow)</span></span>

<span data-ttu-id="3c06d-105">由於 DirectShow 是模組化的，因此需要一種方式來描述篩選圖形中每個點的資料格式。</span><span class="sxs-lookup"><span data-stu-id="3c06d-105">Because DirectShow is modular, it requires a way to describe the format of the data at each point in the filter graph.</span></span> <span data-ttu-id="3c06d-106">例如，請考慮採用 AVI 播放。</span><span class="sxs-lookup"><span data-stu-id="3c06d-106">For example, consider AVI playback.</span></span> <span data-ttu-id="3c06d-107">資料會以 RIFF 區塊的資料流程形式進入圖形。</span><span class="sxs-lookup"><span data-stu-id="3c06d-107">Data enters the graph as a stream of RIFF chunks.</span></span> <span data-ttu-id="3c06d-108">這些會剖析成影片和音訊串流。</span><span class="sxs-lookup"><span data-stu-id="3c06d-108">These are parsed into video and audio streams.</span></span> <span data-ttu-id="3c06d-109">影片資料流程是由可能壓縮的影片框架所組成。</span><span class="sxs-lookup"><span data-stu-id="3c06d-109">The video stream consists of video frames, which are probably compressed.</span></span> <span data-ttu-id="3c06d-110">解碼之後，影片串流是一系列未壓縮的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="3c06d-110">After decoding, the video stream is a series of uncompressed bitmaps.</span></span> <span data-ttu-id="3c06d-111">音訊串流會經歷類似的程式。</span><span class="sxs-lookup"><span data-stu-id="3c06d-111">The audio stream goes through a similar process.</span></span>

<span data-ttu-id="3c06d-112">媒體類型： DirectShow 如何表示格式</span><span class="sxs-lookup"><span data-stu-id="3c06d-112">Media Types: How DirectShow Represents Formats</span></span>

<span data-ttu-id="3c06d-113">*媒體類型* 是用來描述數位媒體格式的通用且可擴充的方式。</span><span class="sxs-lookup"><span data-stu-id="3c06d-113">The *media type* is a universal and extensible way to describe digital media formats.</span></span> <span data-ttu-id="3c06d-114">當兩個篩選準則連線時，它們會同意媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3c06d-114">When two filters connect, they agree on a media type.</span></span> <span data-ttu-id="3c06d-115">媒體類型會識別上游篩選器會傳遞至下游篩選器的資料類型，以及資料的實體版面配置。</span><span class="sxs-lookup"><span data-stu-id="3c06d-115">The media type identifies what kind of data the upstream filter will deliver to the downstream filter, and the physical layout of the data.</span></span> <span data-ttu-id="3c06d-116">如果有兩個篩選器無法同意媒體類型，它們將不會連接。</span><span class="sxs-lookup"><span data-stu-id="3c06d-116">If two filters cannot agree on a media type, they will not connect.</span></span>

<span data-ttu-id="3c06d-117">針對某些應用程式，您永遠都不需要擔心媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3c06d-117">For some applications, you will never have to worry about media types.</span></span> <span data-ttu-id="3c06d-118">例如，在檔案播放中，DirectShow 會處理所有詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3c06d-118">In file playback, for example, DirectShow handles all of the details.</span></span> <span data-ttu-id="3c06d-119">其他類型的應用程式可能必須直接使用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3c06d-119">Other kinds of applications may need to work directly with media types.</span></span>

<span data-ttu-id="3c06d-120">媒體類型是使用 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構來定義。</span><span class="sxs-lookup"><span data-stu-id="3c06d-120">Media types are defined using the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="3c06d-121">此結構包含下列資訊：</span><span class="sxs-lookup"><span data-stu-id="3c06d-121">This structure contains the following information:</span></span>

-   <span data-ttu-id="3c06d-122">**主要類型**：主要類型是定義資料整體分類的 GUID。</span><span class="sxs-lookup"><span data-stu-id="3c06d-122">**Major type**: The major type is a GUID that defines the overall category of the data.</span></span> <span data-ttu-id="3c06d-123">主要類型包括影片、音訊、未剖析的位元組資料流程、MIDI 資料等等。</span><span class="sxs-lookup"><span data-stu-id="3c06d-123">Major types include video, audio, unparsed byte stream, MIDI data, and so forth.</span></span>
-   <span data-ttu-id="3c06d-124">**子類型**：子類型是另一個 GUID，可進一步定義格式。</span><span class="sxs-lookup"><span data-stu-id="3c06d-124">**Subtype**: The subtype is another GUID, which further defines the format.</span></span> <span data-ttu-id="3c06d-125">例如，在影片主要類型中，有 RGB-24、RGB-32、UYVY 等等的子類型。</span><span class="sxs-lookup"><span data-stu-id="3c06d-125">For example, within the video major type, there are subtypes for RGB-24, RGB-32, UYVY, and so forth.</span></span> <span data-ttu-id="3c06d-126">在音訊中，有 PCM 音訊、MPEG-2 承載和其他專案。</span><span class="sxs-lookup"><span data-stu-id="3c06d-126">Within audio, there is PCM audio, MPEG-1 payload, and others.</span></span> <span data-ttu-id="3c06d-127">子類型提供的資訊高於主要類型，但不會定義格式的所有內容。</span><span class="sxs-lookup"><span data-stu-id="3c06d-127">The subtype provides more information than the major type, but it does not define everything about the format.</span></span> <span data-ttu-id="3c06d-128">例如，影片子類型不會定義影像大小或畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="3c06d-128">For example, video subtypes do not define the image size or the frame rate.</span></span> <span data-ttu-id="3c06d-129">這些是由格式區塊所定義，如下所述。</span><span class="sxs-lookup"><span data-stu-id="3c06d-129">These are defined by the format block, described below.</span></span>
-   <span data-ttu-id="3c06d-130">**格式區塊**：格式區塊是資料區塊，會詳細描述此格式。</span><span class="sxs-lookup"><span data-stu-id="3c06d-130">**Format block**: The format block is a block of data that describes the format in detail.</span></span> <span data-ttu-id="3c06d-131">格式區塊會與 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構分開配置。</span><span class="sxs-lookup"><span data-stu-id="3c06d-131">The format block is allocated separately from the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="3c06d-132">**AM \_ 媒體 \_ 類型** 結構的 **pbFormat** 成員會指向格式區塊。</span><span class="sxs-lookup"><span data-stu-id="3c06d-132">The **pbFormat** member of the **AM\_MEDIA\_TYPE** structure points to the format block.</span></span>

    <span data-ttu-id="3c06d-133">**PbFormat** 成員是輸入的 \**void \** _，因為 format 區塊的配置會根據媒體類型而變更。</span><span class="sxs-lookup"><span data-stu-id="3c06d-133">The **pbFormat** member is typed \**void\** _ because the layout of the format block changes depending on the media type.</span></span> <span data-ttu-id="3c06d-134">例如，PCM 音訊使用 [_ *WAVEFORMATEX* \*](/previous-versions/dd757713(v=vs.85))結構。</span><span class="sxs-lookup"><span data-stu-id="3c06d-134">For example, PCM audio uses a [_ *WAVEFORMATEX*\*](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="3c06d-135">影片使用各種結構，包括 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 和 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)。</span><span class="sxs-lookup"><span data-stu-id="3c06d-135">Video uses various structures, including [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span> <span data-ttu-id="3c06d-136">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的 **formattype** 成員是 GUID，用來指定要包含在格式區塊中的結構。</span><span class="sxs-lookup"><span data-stu-id="3c06d-136">The **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure is a GUID that specifies which structure is contained in the format block.</span></span> <span data-ttu-id="3c06d-137">每個格式結構都會被指派一個 GUID。</span><span class="sxs-lookup"><span data-stu-id="3c06d-137">Each format structure is assigned a GUID.</span></span> <span data-ttu-id="3c06d-138">**CbFormat** 成員會指定格式區塊的大小。</span><span class="sxs-lookup"><span data-stu-id="3c06d-138">The **cbFormat** member specifies the size of the format block.</span></span> <span data-ttu-id="3c06d-139">在取值 **pbFormat** 指標之前，請務必先檢查這些值。</span><span class="sxs-lookup"><span data-stu-id="3c06d-139">Always check these values before dereferencing the **pbFormat** pointer.</span></span>

<span data-ttu-id="3c06d-140">如果已填入格式區塊，則主要類型和子類型會包含重複的資訊。</span><span class="sxs-lookup"><span data-stu-id="3c06d-140">If the format block is filled in, then the major type and subtype contain redundant information.</span></span> <span data-ttu-id="3c06d-141">不過，主要類型和子類型可提供便利的方式來識別沒有完整格式區塊的格式。</span><span class="sxs-lookup"><span data-stu-id="3c06d-141">The major type and subtype, however, provide a convenient way to identify formats without a complete format block.</span></span> <span data-ttu-id="3c06d-142">例如，您可以指定泛型24位 RGB 格式 (MEDIASUBTYPE \_ RGB24) ，而不需要知道 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構所需的所有資訊，例如影像大小和畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="3c06d-142">For example, you can specify a generic 24-bit RGB format (MEDIASUBTYPE\_RGB24), without knowing all of the information required by the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, such as image size and frame rate.</span></span>

<span data-ttu-id="3c06d-143">例如，篩選器可能會使用下列程式碼來檢查媒體類型：</span><span class="sxs-lookup"><span data-stu-id="3c06d-143">For example, a filter might use the following code to check a media type:</span></span>


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



<span data-ttu-id="3c06d-144">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構也包含一些選擇性欄位。</span><span class="sxs-lookup"><span data-stu-id="3c06d-144">The [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure also contains some optional fields.</span></span> <span data-ttu-id="3c06d-145">這些可用來提供其他資訊，但不需要篩選來使用它們：</span><span class="sxs-lookup"><span data-stu-id="3c06d-145">These can be used to provide additional information, but filters are not required to use them:</span></span>

-   <span data-ttu-id="3c06d-146">**lSampleSize**。</span><span class="sxs-lookup"><span data-stu-id="3c06d-146">**lSampleSize**.</span></span> <span data-ttu-id="3c06d-147">如果此欄位不是零，則會定義每個樣本的大小。</span><span class="sxs-lookup"><span data-stu-id="3c06d-147">If this field is non-zero, it defines the size of each sample.</span></span> <span data-ttu-id="3c06d-148">如果是零，則表示樣本大小可能會從範例變更為範例。</span><span class="sxs-lookup"><span data-stu-id="3c06d-148">If it is zero, it indicates that the sample size may change from sample to sample.</span></span>
-   <span data-ttu-id="3c06d-149">**bFixedSizeSamples**。</span><span class="sxs-lookup"><span data-stu-id="3c06d-149">**bFixedSizeSamples**.</span></span> <span data-ttu-id="3c06d-150">如果這個布林值旗標為 **TRUE**，表示 **lSampleSize** 中的值是有效的。</span><span class="sxs-lookup"><span data-stu-id="3c06d-150">If this Boolean flag is **TRUE**, it means the value in **lSampleSize** is valid.</span></span> <span data-ttu-id="3c06d-151">否則，您應該忽略 **lSampleSize**。</span><span class="sxs-lookup"><span data-stu-id="3c06d-151">Otherwise, you should ignore **lSampleSize**.</span></span>
-   <span data-ttu-id="3c06d-152">**bTemporalCompression**。</span><span class="sxs-lookup"><span data-stu-id="3c06d-152">**bTemporalCompression**.</span></span> <span data-ttu-id="3c06d-153">如果這個布林值旗標為 **FALSE**，則表示所有框架都是主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="3c06d-153">If this Boolean flag is **FALSE**, it means that all frames are key frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c06d-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c06d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c06d-155">篩選圖形及其元件</span><span class="sxs-lookup"><span data-stu-id="3c06d-155">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
