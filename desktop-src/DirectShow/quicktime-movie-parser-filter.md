---
description: QuickTime 影片剖析器篩選
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: QuickTime 影片剖析器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a046e143487a1455aeeb125910bbf4452b4f947
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317756"
---
# <a name="quicktime-movie-parser-filter"></a><span data-ttu-id="efef8-103">QuickTime 影片剖析器篩選</span><span class="sxs-lookup"><span data-stu-id="efef8-103">QuickTime Movie Parser Filter</span></span>

<span data-ttu-id="efef8-104">此元件已從 Windows Vista 和更新版本的作業系統中移除。</span><span class="sxs-lookup"><span data-stu-id="efef8-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="efef8-105">它可在 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="efef8-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="efef8-106">QuickTime Movie 剖析器篩選器會將 Apple® QuickTime®資料分割成音訊和影片串流。</span><span class="sxs-lookup"><span data-stu-id="efef8-106">The QuickTime Movie Parser filter splits Apple® QuickTime® data into audio and video streams.</span></span> <span data-ttu-id="efef8-107">它支援 QuickTime 2.0 及更早版本。</span><span class="sxs-lookup"><span data-stu-id="efef8-107">It supports QuickTime 2.0 and earlier.</span></span> <span data-ttu-id="efef8-108">輸入 pin 會連接到來源篩選器，例如 [非同步檔案來源](file-source--async--filter.md) 篩選或 URL 檔案 [來源](file-source--url--filter.md) 篩選。</span><span class="sxs-lookup"><span data-stu-id="efef8-108">The input pin connects to a source filter such as the [Async File Source](file-source--async--filter.md) filter or the [URL File Source](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="efef8-109">剖析器會使用 [AVI 解壓縮](avi-decompressor-filter.md) 程式或 [QT 解壓縮](qt-decompressor-filter.md) 程式篩選器，將 QuickTime 檔案解壓縮。</span><span class="sxs-lookup"><span data-stu-id="efef8-109">The Parser uses the [AVI Decompressor](avi-decompressor-filter.md) or [QT Decompressor](qt-decompressor-filter.md) filter to decompress QuickTime files.</span></span> <span data-ttu-id="efef8-110">此篩選器會為影片串流建立一個輸出圖釘，並為音訊串流建立一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="efef8-110">The filter creates one output pin for the video stream and one output pin for the audio stream.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="efef8-111">篩選介面</span><span class="sxs-lookup"><span data-stu-id="efef8-111">Filter Interfaces</span></span></td>
<td><span data-ttu-id="efef8-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="efef8-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efef8-113">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="efef8-113">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="efef8-114">MEDIATYPE_Stream，MEDIASUBTYPE_QTMovie;</span><span class="sxs-lookup"><span data-stu-id="efef8-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efef8-115">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="efef8-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="efef8-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="efef8-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efef8-117">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="efef8-117">Output Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="efef8-118">MEDIATYPE_Video、MEDIASUBTYPE_Null FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="efef8-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></li>
<li><span data-ttu-id="efef8-119">MEDIATYPE_Audio、MEDIASUBTYPE_Null FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="efef8-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efef8-120">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="efef8-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="efef8-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="efef8-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efef8-122">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="efef8-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="efef8-123">CLSID_QuickTimeParser</span><span class="sxs-lookup"><span data-stu-id="efef8-123">CLSID_QuickTimeParser</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efef8-124">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="efef8-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="efef8-125">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="efef8-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efef8-126">可執行檔</span><span class="sxs-lookup"><span data-stu-id="efef8-126">Executable</span></span></td>
<td><span data-ttu-id="efef8-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="efef8-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efef8-128"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="efef8-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="efef8-129">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="efef8-129">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efef8-130"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="efef8-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="efef8-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="efef8-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="efef8-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="efef8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efef8-133">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="efef8-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



