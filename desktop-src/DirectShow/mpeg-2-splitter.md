---
description: MPEG-2 分隔器
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: MPEG-2 分隔器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187528"
---
# <a name="mpeg-2-splitter"></a><span data-ttu-id="abe96-103">MPEG-2 分隔器</span><span class="sxs-lookup"><span data-stu-id="abe96-103">MPEG-2 Splitter</span></span>

<span data-ttu-id="abe96-104">從 Microsoft® Windows® XP 開始，MPEG 2 分隔器篩選器已被取代。</span><span class="sxs-lookup"><span data-stu-id="abe96-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="abe96-105">請改用 [Mpeg-2 信號](mpeg-2-demultiplexer.md) 。</span><span class="sxs-lookup"><span data-stu-id="abe96-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

<span data-ttu-id="abe96-106">在舊版平臺上，使用 MPEG-2 分隔器，以提取模式提供的 MPEG-2 程式資料流程，其中至少包含下列其中一個資料流程類型： MPEG-2 影片;MPEG-2 音訊;以 DVD video 定義的 AC3 音訊編碼;或 PCM 音訊編碼為 DVD 影片的定義。</span><span class="sxs-lookup"><span data-stu-id="abe96-106">On earlier platforms, use the MPEG-2 Splitter for MPEG-2 program streams delivered in pull mode that contain at least one of the following stream types: MPEG-2 video; MPEG-2 audio; AC3 audio encoded as defined for DVD video; or PCM audio encoded as defined for DVD video.</span></span> <span data-ttu-id="abe96-107">此篩選器會剖析串流、建立每個資料流程的輸出針腳，然後將壓縮的 MPEG 音訊或影片封包輸出到 MPEG-2 的解碼器篩選器。</span><span class="sxs-lookup"><span data-stu-id="abe96-107">This filter parses the streams, creates an output pin for each stream, and outputs the compressed MPEG audio or video packets to an MPEG-2 decoder filter.</span></span>

<span data-ttu-id="abe96-108">針對以推送模式傳遞的程式和傳輸資料流程，請在所有平臺上使用 [Mpeg-2 信號](mpeg-2-demultiplexer.md)。</span><span class="sxs-lookup"><span data-stu-id="abe96-108">For program and transport streams delivered in push-mode, use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md), on all platforms.</span></span>

> [!Note]  
> <span data-ttu-id="abe96-109">MPEG-2 分隔器不支援框架精確的搜尋。</span><span class="sxs-lookup"><span data-stu-id="abe96-109">The MPEG-2 Splitter does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="abe96-110">篩選介面</span><span class="sxs-lookup"><span data-stu-id="abe96-110">Filter Interfaces</span></span></td>
<td><span data-ttu-id="abe96-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <strong>ISpecifyPropertyPages</strong>、 <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></span><span class="sxs-lookup"><span data-stu-id="abe96-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abe96-112">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="abe96-112">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="abe96-113">MEDIATYPE_Stream，MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="abe96-113">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="abe96-114">MEDIATYPE_Stream，MEDIASUBTYPE_MPEG1_Video</span><span class="sxs-lookup"><span data-stu-id="abe96-114">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</span></span></li>
<li><span data-ttu-id="abe96-115">MEDIATYPE_Stream，MEDIASUBTYPE_Null</span><span class="sxs-lookup"><span data-stu-id="abe96-115">MEDIATYPE_Stream, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abe96-116">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="abe96-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="abe96-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="abe96-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abe96-118">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="abe96-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="abe96-119">相依于資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="abe96-119">Depends on the stream type.</span></span> <span data-ttu-id="abe96-120">請參閱 <a href="mpeg-2-splitter-media-types.md">Mpeg-2 分隔器媒體類型</a></span><span class="sxs-lookup"><span data-stu-id="abe96-120">See <a href="mpeg-2-splitter-media-types.md">MPEG-2 Splitter Media Types</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abe96-121">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="abe96-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="abe96-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="abe96-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abe96-123">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="abe96-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="abe96-124">CLSID_MMSPLITTER</span><span class="sxs-lookup"><span data-stu-id="abe96-124">CLSID_MMSPLITTER</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abe96-125">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="abe96-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="abe96-126">不適用</span><span class="sxs-lookup"><span data-stu-id="abe96-126">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abe96-127">可執行檔</span><span class="sxs-lookup"><span data-stu-id="abe96-127">Executable</span></span></td>
<td><span data-ttu-id="abe96-128">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="abe96-128">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="abe96-129"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="abe96-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="abe96-130">MERIT_NORMAL + 1</span><span class="sxs-lookup"><span data-stu-id="abe96-130">MERIT_NORMAL + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="abe96-131"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="abe96-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="abe96-132">CLSID_AudioInputDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="abe96-132">CLSID_AudioInputDeviceCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="abe96-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="abe96-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abe96-134">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="abe96-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="abe96-135">使用 MPEG-2 分隔器</span><span class="sxs-lookup"><span data-stu-id="abe96-135">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



