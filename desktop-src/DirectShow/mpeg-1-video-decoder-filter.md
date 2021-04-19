---
description: MPEG-2 影片解碼篩選器
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: MPEG-2 影片解碼篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7f48e441226dee33ef949219e8008e15c9d711
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973128"
---
# <a name="mpeg-1-video-decoder-filter"></a><span data-ttu-id="fe934-103">MPEG-2 影片解碼篩選器</span><span class="sxs-lookup"><span data-stu-id="fe934-103">MPEG-1 Video Decoder Filter</span></span>

<span data-ttu-id="fe934-104">解碼 MPEG 1 影片。</span><span class="sxs-lookup"><span data-stu-id="fe934-104">Decodes MPEG-1 video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe934-105">篩選介面</span><span class="sxs-lookup"><span data-stu-id="fe934-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="fe934-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe934-107">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="fe934-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="fe934-108">MEDIATYPE_Video，FORMAT_MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="fe934-108">MEDIATYPE_Video, FORMAT_MPEGVideo</span></span><br/> <span data-ttu-id="fe934-109">下列子類型有效：</span><span class="sxs-lookup"><span data-stu-id="fe934-109">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="fe934-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span></span></li>
<li><span data-ttu-id="fe934-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe934-112">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="fe934-112">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="fe934-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"> <strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe934-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe934-114">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="fe934-114">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="fe934-115">主要類型： <strong>MEDIATYPE_Video</strong>、</span><span class="sxs-lookup"><span data-stu-id="fe934-115">Major type: <strong>MEDIATYPE_Video</strong>,</span></span><br/> <span data-ttu-id="fe934-116">格式類型： <strong>FORMAT_VideoInfo</strong> 或 <strong>FORMAT_VideoInfo2</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-116">Format type: <strong>FORMAT_VideoInfo</strong> or <strong>FORMAT_VideoInfo2</strong></span></span><br/> <span data-ttu-id="fe934-117">亞：</span><span class="sxs-lookup"><span data-stu-id="fe934-117">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="fe934-118"><strong>MEDIASUBTYPE_RGB24</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-118"><strong>MEDIASUBTYPE_RGB24</strong></span></span></li>
<li><span data-ttu-id="fe934-119"><strong>MEDIASUBTYPE_RGB32</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-119"><strong>MEDIASUBTYPE_RGB32</strong></span></span></li>
<li><span data-ttu-id="fe934-120"><strong>MEDIASUBTYPE_RGB8</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-120"><strong>MEDIASUBTYPE_RGB8</strong></span></span></li>
<li><span data-ttu-id="fe934-121"><strong>MEDIASUBTYPE_RGB555</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-121"><strong>MEDIASUBTYPE_RGB555</strong></span></span></li>
<li><span data-ttu-id="fe934-122"><strong>MEDIASUBTYPE_RGB565</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-122"><strong>MEDIASUBTYPE_RGB565</strong></span></span></li>
<li><span data-ttu-id="fe934-123"><strong>MEDIASUBTYPE_UYVY</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-123"><strong>MEDIASUBTYPE_UYVY</strong></span></span></li>
<li><span data-ttu-id="fe934-124"><strong>MEDIASUBTYPE_Y41P</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-124"><strong>MEDIASUBTYPE_Y41P</strong></span></span></li>
<li><span data-ttu-id="fe934-125"><strong>MEDIASUBTYPE_YUY2</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-125"><strong>MEDIASUBTYPE_YUY2</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe934-126">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="fe934-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="fe934-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe934-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe934-128">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="fe934-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="fe934-129"><strong>CLSID_CMpegVideoCodec</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-129"><strong>CLSID_CMpegVideoCodec</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe934-130">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="fe934-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="fe934-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span><span class="sxs-lookup"><span data-stu-id="fe934-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe934-132">可執行檔</span><span class="sxs-lookup"><span data-stu-id="fe934-132">Executable</span></span></td>
<td><span data-ttu-id="fe934-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="fe934-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe934-134"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="fe934-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="fe934-135">0x40000001</span><span class="sxs-lookup"><span data-stu-id="fe934-135">0x40000001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe934-136"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="fe934-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="fe934-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="fe934-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="fe934-138">備註</span><span class="sxs-lookup"><span data-stu-id="fe934-138">Remarks</span></span>

<span data-ttu-id="fe934-139">此篩選器可以解碼成 DirectDraw 表面。</span><span class="sxs-lookup"><span data-stu-id="fe934-139">This filter can decode into a DirectDraw Surface.</span></span> <span data-ttu-id="fe934-140">如果電腦支援 MMX，則篩選器會使用 MMX。</span><span class="sxs-lookup"><span data-stu-id="fe934-140">The filter uses MMX if the machine supports MMX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe934-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe934-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe934-142">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="fe934-142">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




