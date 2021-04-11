---
description: AVI 繪製篩選
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: AVI 繪製篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6d6b318b7a1f7e762fc0806186114fb9256f5c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108621"
---
# <a name="avi-draw-filter"></a><span data-ttu-id="cf223-103">AVI 繪製篩選</span><span class="sxs-lookup"><span data-stu-id="cf223-103">AVI Draw Filter</span></span>

<span data-ttu-id="cf223-104">當影片輸出到外部 NTSC 電視監視器時，會自動將 AVI 繪圖篩選器提取到播放圖形，而不是 [Avi 解壓縮](avi-decompressor-filter.md) 程式。</span><span class="sxs-lookup"><span data-stu-id="cf223-104">The AVI Draw filter is pulled automatically into a playback graph instead of the [AVI Decompressor](avi-decompressor-filter.md) when video is being output to an external NTSC television monitor.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf223-105">篩選介面</span><span class="sxs-lookup"><span data-stu-id="cf223-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="cf223-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf223-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf223-107">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="cf223-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="cf223-108">主要類型： MEDIATYPE_VideoSubtypes：</span><span class="sxs-lookup"><span data-stu-id="cf223-108">Major Type: MEDIATYPE_VideoSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="cf223-109">MEDIASUBTYPE_MJPG</span><span class="sxs-lookup"><span data-stu-id="cf223-109">MEDIASUBTYPE_MJPG</span></span></li>
<li><span data-ttu-id="cf223-110">MEDIASUBTYPE_TVMJ</span><span class="sxs-lookup"><span data-stu-id="cf223-110">MEDIASUBTYPE_TVMJ</span></span></li>
<li><span data-ttu-id="cf223-111">MEDIASUBTYPE_WAKE</span><span class="sxs-lookup"><span data-stu-id="cf223-111">MEDIASUBTYPE_WAKE</span></span></li>
<li><span data-ttu-id="cf223-112">MEDIASUBTYPE_CFCC</span><span class="sxs-lookup"><span data-stu-id="cf223-112">MEDIASUBTYPE_CFCC</span></span></li>
<li><span data-ttu-id="cf223-113">MEDIASUBTYPE_IJPG</span><span class="sxs-lookup"><span data-stu-id="cf223-113">MEDIASUBTYPE_IJPG</span></span></li>
<li><span data-ttu-id="cf223-114">MEDIASUBTYPE_Plum</span><span class="sxs-lookup"><span data-stu-id="cf223-114">MEDIASUBTYPE_Plum</span></span></li>
<li><span data-ttu-id="cf223-115">MEDIASUBTYPE_DVCS</span><span class="sxs-lookup"><span data-stu-id="cf223-115">MEDIASUBTYPE_DVCS</span></span></li>
<li><span data-ttu-id="cf223-116">MEDIASUBTYPE_DVSD</span><span class="sxs-lookup"><span data-stu-id="cf223-116">MEDIASUBTYPE_DVSD</span></span></li>
<li><span data-ttu-id="cf223-117">MEDIASUBTYPE_MDVF</span><span class="sxs-lookup"><span data-stu-id="cf223-117">MEDIASUBTYPE_MDVF</span></span></li>
<li><span data-ttu-id="cf223-118">格式類型： FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="cf223-118">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf223-119">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="cf223-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="cf223-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf223-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf223-121">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="cf223-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="cf223-122">MEDIATYPE_Video，MEDIASUBTYPE_Null</span><span class="sxs-lookup"><span data-stu-id="cf223-122">MEDIATYPE_Video, MEDIASUBTYPE_NULL</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf223-123">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="cf223-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="cf223-124"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf223-124"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf223-125">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="cf223-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="cf223-126">CLSID_AVIDraw</span><span class="sxs-lookup"><span data-stu-id="cf223-126">CLSID_AVIDraw</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf223-127">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="cf223-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="cf223-128">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="cf223-128">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf223-129">可執行檔</span><span class="sxs-lookup"><span data-stu-id="cf223-129">Executable</span></span></td>
<td><span data-ttu-id="cf223-130">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="cf223-130">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf223-131"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="cf223-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="cf223-132">MERIT_NORMAL + 100</span><span class="sxs-lookup"><span data-stu-id="cf223-132">MERIT_NORMAL + 100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf223-133"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="cf223-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="cf223-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="cf223-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="cf223-135">備註</span><span class="sxs-lookup"><span data-stu-id="cf223-135">Remarks</span></span>

<span data-ttu-id="cf223-136">由於 AVI Draw 篩選和 [VFW Capture 篩選器](vfw-capture-filter.md) 都連接到相同的硬體，因此它們不能在相同的篩選圖形中。</span><span class="sxs-lookup"><span data-stu-id="cf223-136">Since the AVI Draw filter and the [VFW Capture Filter](vfw-capture-filter.md) both connect to the same hardware, they cannot be in the same filter graph.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf223-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="cf223-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf223-138">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="cf223-138">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




