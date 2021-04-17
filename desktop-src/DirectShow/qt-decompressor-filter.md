---
description: QT 解壓縮程式篩選器
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: QT 解壓縮程式篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e586eb9d65ee00509f4a434f3283bd762d535b26
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467630"
---
# <a name="qt-decompressor-filter"></a><span data-ttu-id="6e399-103">QT 解壓縮程式篩選器</span><span class="sxs-lookup"><span data-stu-id="6e399-103">QT Decompressor Filter</span></span>

<span data-ttu-id="6e399-104">此元件已從 Windows Vista 和更新版本的作業系統中移除。</span><span class="sxs-lookup"><span data-stu-id="6e399-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="6e399-105">它可在 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="6e399-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="6e399-106">QT 解壓縮程式篩選器會®2.0 影片解壓縮 Apple® QuickTime。</span><span class="sxs-lookup"><span data-stu-id="6e399-106">The QT Decompressor filter decompresses Apple® QuickTime® 2.0 video.</span></span> <span data-ttu-id="6e399-107">此格式通常用於較舊的 QuickTime 檔案中。</span><span class="sxs-lookup"><span data-stu-id="6e399-107">This format is typically used in older QuickTime files.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6e399-108">篩選介面</span><span class="sxs-lookup"><span data-stu-id="6e399-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="6e399-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e399-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e399-110">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="6e399-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="6e399-111">MEDIATYPE_Video，FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="6e399-111">MEDIATYPE_Video, FORMAT_VideoInfo</span></span><br/> <span data-ttu-id="6e399-112">下列子類型有效：</span><span class="sxs-lookup"><span data-stu-id="6e399-112">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="6e399-113">MEDIASUBTYPE_QTRpza</span><span class="sxs-lookup"><span data-stu-id="6e399-113">MEDIASUBTYPE_QTRpza</span></span></li>
<li><span data-ttu-id="6e399-114">MEDIASUBTYPE_QTSmc</span><span class="sxs-lookup"><span data-stu-id="6e399-114">MEDIASUBTYPE_QTSmc</span></span></li>
<li><span data-ttu-id="6e399-115">MEDIASUBTYPE_QTRle</span><span class="sxs-lookup"><span data-stu-id="6e399-115">MEDIASUBTYPE_QTRle</span></span></li>
<li><span data-ttu-id="6e399-116">MEDIASUBTYPE_QTJpeg</span><span class="sxs-lookup"><span data-stu-id="6e399-116">MEDIASUBTYPE_QTJpeg</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e399-117">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="6e399-117">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="6e399-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e399-118"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e399-119">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="6e399-119">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="6e399-120">MEDIATYPE_Video、MEDIASUBTYPE_Null FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="6e399-120">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e399-121">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="6e399-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="6e399-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="6e399-122"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e399-123">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="6e399-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="6e399-124">CLSID_QTDec</span><span class="sxs-lookup"><span data-stu-id="6e399-124">CLSID_QTDec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e399-125">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="6e399-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="6e399-126">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="6e399-126">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e399-127">可執行檔</span><span class="sxs-lookup"><span data-stu-id="6e399-127">Executable</span></span></td>
<td><span data-ttu-id="6e399-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="6e399-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e399-129"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="6e399-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="6e399-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="6e399-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e399-131"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="6e399-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="6e399-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="6e399-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="6e399-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e399-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e399-134">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="6e399-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




