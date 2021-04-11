---
description: DV 影片編碼器篩選器
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: DV 影片編碼器篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b91da15fda0597e9b943c78fd5a6716021a3ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935670"
---
# <a name="dv-video-encoder-filter"></a><span data-ttu-id="cdfe1-103">DV 影片編碼器篩選器</span><span class="sxs-lookup"><span data-stu-id="cdfe1-103">DV Video Encoder Filter</span></span>

<span data-ttu-id="cdfe1-104">此篩選會將未壓縮的影片串流編碼為數位視訊 (DV) 。</span><span class="sxs-lookup"><span data-stu-id="cdfe1-104">This filter encodes an uncompressed video stream into digital video (DV).</span></span> <span data-ttu-id="cdfe1-105">它會提供自訂介面 [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)，以設定編碼解析度和格式。</span><span class="sxs-lookup"><span data-stu-id="cdfe1-105">It provides a custom interface, [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc), for setting the encoding resolution and format.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cdfe1-106">篩選介面</span><span class="sxs-lookup"><span data-stu-id="cdfe1-106">Filter Interfaces</span></span></td>
<td><span data-ttu-id="cdfe1-107"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>、 <strong>IPersistStream</strong>、 <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="cdfe1-107"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cdfe1-108">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="cdfe1-108">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="cdfe1-109">主要類型： MEDIATYPE_VideoThe 下列子類型有效：</span><span class="sxs-lookup"><span data-stu-id="cdfe1-109">Major type: MEDIATYPE_VideoThe following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="cdfe1-110">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="cdfe1-110">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="cdfe1-111">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="cdfe1-111">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="cdfe1-112">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="cdfe1-112">MEDIASUBTYPE_RGB555</span></span></li>
</ul></li>
<li><span data-ttu-id="cdfe1-113">格式類型： FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="cdfe1-113">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cdfe1-114">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="cdfe1-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="cdfe1-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="cdfe1-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cdfe1-116">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="cdfe1-116">Output Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="cdfe1-117">主要類型： MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="cdfe1-117">Major type: MEDIATYPE_Video</span></span></li>
<li><span data-ttu-id="cdfe1-118">子類型： MEDIASUBTYPE_dvsd</span><span class="sxs-lookup"><span data-stu-id="cdfe1-118">Subtype: MEDIASUBTYPE_dvsd</span></span></li>
<li><span data-ttu-id="cdfe1-119">格式類型： FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="cdfe1-119">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cdfe1-120">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="cdfe1-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="cdfe1-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="cdfe1-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cdfe1-122">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="cdfe1-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="cdfe1-123">CLSID_DVVideoEnc</span><span class="sxs-lookup"><span data-stu-id="cdfe1-123">CLSID_DVVideoEnc</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cdfe1-124">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="cdfe1-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="cdfe1-125">CLSID_DVEncPropertiesPage</span><span class="sxs-lookup"><span data-stu-id="cdfe1-125">CLSID_DVEncPropertiesPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cdfe1-126">可執行檔</span><span class="sxs-lookup"><span data-stu-id="cdfe1-126">Executable</span></span></td>
<td><span data-ttu-id="cdfe1-127">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="cdfe1-127">qdv.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cdfe1-128"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="cdfe1-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="cdfe1-129">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="cdfe1-129">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cdfe1-130"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="cdfe1-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="cdfe1-131">CLSID_VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="cdfe1-131">CLSID_VideoCompressorCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="cdfe1-132">備註</span><span class="sxs-lookup"><span data-stu-id="cdfe1-132">Remarks</span></span>

<span data-ttu-id="cdfe1-133">若為16位的影片 (MEDIASUBTYPE \_ RGB555 或 MEDIASUBTYPE \_ RGB565) ，則輸入必須為 720 x 480 圖元（NTSC）或 720 x 576 圖元（代表 PAL）。</span><span class="sxs-lookup"><span data-stu-id="cdfe1-133">For 16-bit video (MEDIASUBTYPE\_RGB555 or MEDIASUBTYPE\_RGB565), the input must be 720 x 480 pixels for NTSC, or 720 x 576 pixels for PAL.</span></span> <span data-ttu-id="cdfe1-134">若是24位的影片，輸入上沒有大小限制。</span><span class="sxs-lookup"><span data-stu-id="cdfe1-134">For 24-bit video, there are no size constraints on the input.</span></span>

<span data-ttu-id="cdfe1-135">適用于 NTSC 的輸出一律是 720 x 480，或適用于 PAL 的 720 x 576;24位影片會調整成符合這些尺寸。</span><span class="sxs-lookup"><span data-stu-id="cdfe1-135">The output is always 720 x 480 for NTSC or 720 x 576 for PAL; 24-bit video is scaled to fit these dimensions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdfe1-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="cdfe1-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdfe1-137">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="cdfe1-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="cdfe1-138">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="cdfe1-138">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




