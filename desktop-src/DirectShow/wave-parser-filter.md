---
description: WAVE 剖析器篩選
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: WAVE 剖析器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb30465a25ab3a6eef190b5fbecd4a4878c2744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986405"
---
# <a name="wave-parser-filter"></a><span data-ttu-id="50f1c-103">WAVE 剖析器篩選</span><span class="sxs-lookup"><span data-stu-id="50f1c-103">WAVE Parser Filter</span></span>

<span data-ttu-id="50f1c-104">WAVE 剖析器篩選器會剖析 wav、澳大利亞或. aif 檔案中的 WAV 格式音訊資料。</span><span class="sxs-lookup"><span data-stu-id="50f1c-104">The WAVE Parser filter parses WAV-format audio data from .wav, .au, or .aif files.</span></span> <span data-ttu-id="50f1c-105">上游篩選必須是非同步檔案 [來源](file-source--async--filter.md) 篩選、URL 檔案 [來源](file-source--url--filter.md) 篩選，或包含 WAV 音訊資料的相容協力廠商非同步來源篩選。</span><span class="sxs-lookup"><span data-stu-id="50f1c-105">The upstream filter must be the [Async File Source](file-source--async--filter.md) filter, [URL File Source](file-source--url--filter.md) filter, or a compatible third-party asynchronous source filter that contains WAV audio data.</span></span> <span data-ttu-id="50f1c-106">輸出資料流程是音訊資料，您可以直接連接到音訊轉譯篩選器，也可以連接到中間的音訊轉換篩選。</span><span class="sxs-lookup"><span data-stu-id="50f1c-106">The output stream is audio data, which you can connect directly to an audio rendering filter or to an intervening audio transform filter.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="50f1c-107">篩選介面</span><span class="sxs-lookup"><span data-stu-id="50f1c-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="50f1c-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></span><span class="sxs-lookup"><span data-stu-id="50f1c-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50f1c-109">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="50f1c-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="50f1c-110">主要類型： MEDIATYPE_StreamThe 下列子類型有效：</span><span class="sxs-lookup"><span data-stu-id="50f1c-110">Major type: MEDIATYPE_StreamThe following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="50f1c-111">MEDIASUBTYPE_AIFF</span><span class="sxs-lookup"><span data-stu-id="50f1c-111">MEDIASUBTYPE_AIFF</span></span></li>
<li><span data-ttu-id="50f1c-112">MEDIASUBTYPE_AU</span><span class="sxs-lookup"><span data-stu-id="50f1c-112">MEDIASUBTYPE_AU</span></span></li>
<li><span data-ttu-id="50f1c-113">MEDIASUBTYPE_WAVE</span><span class="sxs-lookup"><span data-stu-id="50f1c-113">MEDIASUBTYPE_WAVE</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50f1c-114">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="50f1c-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="50f1c-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="50f1c-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50f1c-116">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="50f1c-116">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="50f1c-117">主要類型： MEDIATYPE_AudioSubtype： MEDIASUBTYPE_PCM 或其他壓縮類型。</span><span class="sxs-lookup"><span data-stu-id="50f1c-117">Major type: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM or other compression type.</span></span> <span data-ttu-id="50f1c-118"> (查看 <a href="audio-subtypes.md"><strong>音訊子類型</strong></a>。 ) </span><span class="sxs-lookup"><span data-stu-id="50f1c-118">(See <a href="audio-subtypes.md"><strong>Audio Subtypes</strong></a>.)</span></span><br/> <span data-ttu-id="50f1c-119">格式類型： FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="50f1c-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50f1c-120">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="50f1c-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="50f1c-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="50f1c-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50f1c-122">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="50f1c-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="50f1c-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span><span class="sxs-lookup"><span data-stu-id="50f1c-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50f1c-124">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="50f1c-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="50f1c-125">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="50f1c-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50f1c-126">可執行檔</span><span class="sxs-lookup"><span data-stu-id="50f1c-126">Executable</span></span></td>
<td><span data-ttu-id="50f1c-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="50f1c-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50f1c-128"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="50f1c-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="50f1c-129">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="50f1c-129">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50f1c-130"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="50f1c-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="50f1c-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="50f1c-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="50f1c-132">備註</span><span class="sxs-lookup"><span data-stu-id="50f1c-132">Remarks</span></span>

<span data-ttu-id="50f1c-133">此篩選器支援下列檔案類型：</span><span class="sxs-lookup"><span data-stu-id="50f1c-133">This filter supports the following file types:</span></span>

-   <span data-ttu-id="50f1c-134">WAVE ( .wav) </span><span class="sxs-lookup"><span data-stu-id="50f1c-134">WAVE (.wav)</span></span>
-   <span data-ttu-id="50f1c-135">.AIFF 和 .AIFF-C ( 的) </span><span class="sxs-lookup"><span data-stu-id="50f1c-135">AIFF and AIFF-C (.aif)</span></span>
-   <span data-ttu-id="50f1c-136">AU ( 澳大利亞) </span><span class="sxs-lookup"><span data-stu-id="50f1c-136">AU (.au)</span></span>

<span data-ttu-id="50f1c-137">但是，它對音訊格式有下列限制：</span><span class="sxs-lookup"><span data-stu-id="50f1c-137">However, it has the following limitations on the audio format:</span></span>

-   <span data-ttu-id="50f1c-138">音訊必須是8位或16位的線性 PCM。</span><span class="sxs-lookup"><span data-stu-id="50f1c-138">The audio must be 8-bit or 16-bit linear PCM.</span></span>
-   <span data-ttu-id="50f1c-139">若為 .AIFF-C 檔案，必須將音訊解壓縮，以位元組由大到小的位元組順序 (壓縮類型 ' NONE ' ) 。</span><span class="sxs-lookup"><span data-stu-id="50f1c-139">For AIFF-C files, the audio must be uncompressed, in big-endian byte order (compression type 'NONE').</span></span>

## <a name="related-topics"></a><span data-ttu-id="50f1c-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="50f1c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50f1c-141">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="50f1c-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




