---
description: DVD 瀏覽器篩選
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: DVD 瀏覽器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53bb1c6f46e3dd846ffccda32fece2c2f04c8992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467725"
---
# <a name="dvd-navigator-filter"></a><span data-ttu-id="1f775-103">DVD 瀏覽器篩選</span><span class="sxs-lookup"><span data-stu-id="1f775-103">DVD Navigator Filter</span></span>

<span data-ttu-id="1f775-104">DVD 瀏覽器篩選器是 DVD-Video 播放篩選圖形的來源篩選。</span><span class="sxs-lookup"><span data-stu-id="1f775-104">The DVD Navigator filter is the source filter for a DVD-Video playback filter graph.</span></span> <span data-ttu-id="1f775-105">它會開啟 DVD-Video 磁片區中所有必要的檔案、流覽線性 DVD-Video，然後剖析產生的 MPEG-2 程式串流、將資料流程分割成三種 (的影片、音訊、子圖片) 輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="1f775-105">It opens all necessary files in a DVD-Video volume, navigates through the linear DVD-Video .vob files, and parses the resulting MPEG-2 program stream, splitting the stream into three (video, audio, subpicture) output pins.</span></span>

<span data-ttu-id="1f775-106">DVD 瀏覽器篩選器也會執行 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 和 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) 介面，讓 DVD 播放應用程式控制 DVD-Video 播放。</span><span class="sxs-lookup"><span data-stu-id="1f775-106">The DVD Navigator filter also implements the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interfaces that enable a DVD playback application to control DVD-Video playback.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f775-107">篩選介面</span><span class="sxs-lookup"><span data-stu-id="1f775-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="1f775-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>、 <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-108"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f775-109">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="1f775-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="1f775-110">MEDIATYPE_Stream，MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="1f775-110">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f775-111">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="1f775-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="1f775-112">不適用。</span><span class="sxs-lookup"><span data-stu-id="1f775-112">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f775-113">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="1f775-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="1f775-114">基底類型：</span><span class="sxs-lookup"><span data-stu-id="1f775-114">Base types:</span></span><br/>
<ul>
<li><span data-ttu-id="1f775-115">影片： <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>、 <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-115">Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="1f775-116">音訊： <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>， <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-116">Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="1f775-117">子圖片： <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>、 <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-117">Subpicture: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="1f775-118">擴充類型：</span><span class="sxs-lookup"><span data-stu-id="1f775-118">Extended types:</span></span><br/> <span data-ttu-id="1f775-119">視訊：</span><span class="sxs-lookup"><span data-stu-id="1f775-119">Video:</span></span><br/>
<ul>
<li><span data-ttu-id="1f775-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>， <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-120"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="1f775-121"><strong>MEDIATYPE_Video</strong>， <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-121"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
<li><span data-ttu-id="1f775-122"><strong>MEDIATYPE_MPEG2_PES</strong>， <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-122"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></span></span></li>
</ul>
<span data-ttu-id="1f775-123">音訊：</span><span class="sxs-lookup"><span data-stu-id="1f775-123">Audio:</span></span><br/>
<ul>
<li><span data-ttu-id="1f775-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>， <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-124"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="1f775-125"><strong>MEDIATYPE_Audio</strong>， <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-125"><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
<li><span data-ttu-id="1f775-126"><strong>MEDIATYPE_MPEG2_PES</strong>， <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-126"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></span></span></li>
</ul>
<span data-ttu-id="1f775-127">子圖片</span><span class="sxs-lookup"><span data-stu-id="1f775-127">Subpicture:</span></span><br/>
<ul>
<li><span data-ttu-id="1f775-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>， <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-128"><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="1f775-129"><strong>MEDIATYPE_Video</strong>， <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-129"><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
<li><span data-ttu-id="1f775-130"><strong>MEDIATYPE_MPEG2_PES</strong>， <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span><span class="sxs-lookup"><span data-stu-id="1f775-130"><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></span></span></li>
</ul>
<span data-ttu-id="1f775-131">若要啟用擴充類型，請呼叫 <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2：： SetOption</strong></a> ，並設定</span><span class="sxs-lookup"><span data-stu-id="1f775-131">To enable the extended types, call <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2::SetOption</strong></a> and set the</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f775-132">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="1f775-132">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="1f775-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f775-133"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f775-134">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="1f775-134">Filter CLSID</span></span></td>
<td><span data-ttu-id="1f775-135">CLSID_DVDNavigator</span><span class="sxs-lookup"><span data-stu-id="1f775-135">CLSID_DVDNavigator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f775-136">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="1f775-136">Property Page CLSID</span></span></td>
<td><span data-ttu-id="1f775-137">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="1f775-137">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f775-138">可執行檔</span><span class="sxs-lookup"><span data-stu-id="1f775-138">Executable</span></span></td>
<td><span data-ttu-id="1f775-139">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="1f775-139">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f775-140"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="1f775-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="1f775-141">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="1f775-141">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f775-142"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="1f775-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="1f775-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="1f775-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="1f775-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f775-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f775-145">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="1f775-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="1f775-146">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="1f775-146">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




