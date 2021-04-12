---
description: DV 影片解碼篩選
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: DV 影片解碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6baab43d4a369cb16d92974a0e6e469c914961bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509777"
---
# <a name="dv-video-decoder-filter"></a><span data-ttu-id="ace32-103">DV 影片解碼篩選</span><span class="sxs-lookup"><span data-stu-id="ace32-103">DV Video Decoder Filter</span></span>

<span data-ttu-id="ace32-104">此篩選器會將數位視訊解碼 (DV) 串流轉換成未壓縮的影片。</span><span class="sxs-lookup"><span data-stu-id="ace32-104">This filter decodes a digital video (DV) stream into uncompressed video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ace32-105">篩選介面</span><span class="sxs-lookup"><span data-stu-id="ace32-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="ace32-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>、 <strong>IPersistStream</strong>、 <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="ace32-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ace32-107">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="ace32-107">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="ace32-108">MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="ace32-108">MEDIATYPE_Video</span></span></li>
<li><span data-ttu-id="ace32-109">MEDIASUBTYPE_dvsd</span><span class="sxs-lookup"><span data-stu-id="ace32-109">MEDIASUBTYPE_dvsd</span></span></li>
<li><span data-ttu-id="ace32-110">FORMAT_VideoInfo，FORMAT_DvInfo</span><span class="sxs-lookup"><span data-stu-id="ace32-110">FORMAT_VideoInfo, FORMAT_DvInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ace32-111">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="ace32-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="ace32-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="ace32-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ace32-113">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="ace32-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="ace32-114"><strong>主要類型</strong>： MEDIATYPE_Video<strong>子</strong>類型：</span><span class="sxs-lookup"><span data-stu-id="ace32-114"><strong>Major type</strong>: MEDIATYPE_Video<strong>Subtypes</strong>:</span></span><br/>
<ul>
<li><span data-ttu-id="ace32-115">MEDIASUBTYPE_YUY2</span><span class="sxs-lookup"><span data-stu-id="ace32-115">MEDIASUBTYPE_YUY2</span></span></li>
<li><span data-ttu-id="ace32-116">MEDIASUBTYPE_UYVY</span><span class="sxs-lookup"><span data-stu-id="ace32-116">MEDIASUBTYPE_UYVY</span></span></li>
<li><span data-ttu-id="ace32-117">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="ace32-117">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="ace32-118">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="ace32-118">MEDIASUBTYPE_RGB32</span></span></li>
<li><span data-ttu-id="ace32-119">MEDIASUBTYPE_ARGB32</span><span class="sxs-lookup"><span data-stu-id="ace32-119">MEDIASUBTYPE_ARGB32</span></span></li>
<li><span data-ttu-id="ace32-120">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="ace32-120">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="ace32-121">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="ace32-121">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="ace32-122">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="ace32-122">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="ace32-123">MEDIASUBTYPE_Y41P</span><span class="sxs-lookup"><span data-stu-id="ace32-123">MEDIASUBTYPE_Y41P</span></span></li>
</ul><span data-ttu-id="ace32-124">
<strong>格式類型</strong>：</span><span class="sxs-lookup"><span data-stu-id="ace32-124">
<strong>Format types</strong>:</span></span><br/> <span data-ttu-id="ace32-125">Format_VideoInfo，Format_VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="ace32-125">Format_VideoInfo, Format_VideoInfo2</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ace32-126">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="ace32-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="ace32-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="ace32-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ace32-128">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="ace32-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="ace32-129">CLSID_DVVideoCodec</span><span class="sxs-lookup"><span data-stu-id="ace32-129">CLSID_DVVideoCodec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ace32-130">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="ace32-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="ace32-131">CLSID_DVDecPropertiesPage</span><span class="sxs-lookup"><span data-stu-id="ace32-131">CLSID_DVDecPropertiesPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ace32-132">可執行檔</span><span class="sxs-lookup"><span data-stu-id="ace32-132">Executable</span></span></td>
<td><span data-ttu-id="ace32-133">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="ace32-133">qdv.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ace32-134"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="ace32-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="ace32-135">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="ace32-135">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ace32-136"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="ace32-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="ace32-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="ace32-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="ace32-138">備註</span><span class="sxs-lookup"><span data-stu-id="ace32-138">Remarks</span></span>

<span data-ttu-id="ace32-139">您可以使用 [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) 介面，將解碼解析度設定為 [完整]、[半大小]、[季大小] 或 [一到八個大小]。</span><span class="sxs-lookup"><span data-stu-id="ace32-139">Use the [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) interface to set the decoding resolution to full, half size, quarter size, or one-eighth size.</span></span>

<span data-ttu-id="ace32-140">**交錯**：較早版本的解碼器一律會將影片進行逐行掃描。</span><span class="sxs-lookup"><span data-stu-id="ace32-140">**Interlacing**: Earlier versions of the decoder always deinterlace the video.</span></span> <span data-ttu-id="ace32-141">從 DirectX 9.0，DV Video 解碼器可以保留交錯。</span><span class="sxs-lookup"><span data-stu-id="ace32-141">As of DirectX 9.0, the DV Video Decoder can preserve the interlacing.</span></span> <span data-ttu-id="ace32-142">這可讓 (VMR) 的影片混合轉譯器 deinterlaced 交錯式影片，以改善轉譯品質。</span><span class="sxs-lookup"><span data-stu-id="ace32-142">This enables the interlaced video to be deinterlaced by the Video Mixing Renderer (VMR), for improved rendering quality.</span></span> <span data-ttu-id="ace32-143">若要使用這項功能，下游篩選器必須支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)格式，並 \_ 以 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的 **formattype** 成員中的該值格式 VideoInfo2 表示。</span><span class="sxs-lookup"><span data-stu-id="ace32-143">To use this feature, the downstream filter must support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, indicated by that value Format\_VideoInfo2 in the **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="ace32-144">在完整解析輸出中， **VIDEOINFOHEADER2** 結構中 (**dwInterlace**) 的去交錯旗標會設為 `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` ，表示交錯的欄位。</span><span class="sxs-lookup"><span data-stu-id="ace32-144">At full resolution output, the deinterlacing flags (**dwInterlace**) in the **VIDEOINFOHEADER2** structure are set to `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave`, indicating interlaced fields.</span></span> <span data-ttu-id="ace32-145">在半解析度或較低的情況下， **dwInterlace** 會設為零，表示漸進式框架。</span><span class="sxs-lookup"><span data-stu-id="ace32-145">At half resolution or lower, **dwInterlace** is set to zero, indicating progressive frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ace32-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="ace32-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ace32-147">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="ace32-147">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="ace32-148">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="ace32-148">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




