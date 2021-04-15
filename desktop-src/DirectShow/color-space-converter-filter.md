---
description: 色彩空間轉換器篩選
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: 色彩空間轉換器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f054ee03dd65cf619a697d4441b4d09279e7b912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467557"
---
# <a name="color-space-converter-filter"></a><span data-ttu-id="33940-103">色彩空間轉換器篩選</span><span class="sxs-lookup"><span data-stu-id="33940-103">Color Space Converter Filter</span></span>

<span data-ttu-id="33940-104">這項轉換篩選會從一種 RGB 色彩類型轉換成另一種 RGB 類型，例如24位和8位 RGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="33940-104">This transform filter converts from one RGB color type to another RGB type, such as between 24-bit and 8-bit RGB color.</span></span> <span data-ttu-id="33940-105">由於這種類型的轉換在影片解壓縮程式中通常會更有效率地處理，因此當資料流程來源包含未壓縮的 RGB 框架時，就會使用色彩空間轉換器的主要用途。</span><span class="sxs-lookup"><span data-stu-id="33940-105">Since this type of conversion is generally handled more efficiently within a video decompressor, the main use of the Color Space Converter is when the stream source consists of uncompressed RGB frames.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33940-106">篩選介面</span><span class="sxs-lookup"><span data-stu-id="33940-106">Filter Interfaces</span></span></td>
<td><span data-ttu-id="33940-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="33940-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33940-108">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="33940-108">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="33940-109">MEDIATYPE_Video，FORMAT_VideoInfo。</span><span class="sxs-lookup"><span data-stu-id="33940-109">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="33940-110">下列子類型有效：</span><span class="sxs-lookup"><span data-stu-id="33940-110">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="33940-111">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="33940-111">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="33940-112">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="33940-112">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="33940-113">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="33940-113">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="33940-114">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="33940-114">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="33940-115">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="33940-115">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33940-116">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="33940-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="33940-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="33940-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33940-118">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="33940-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="33940-119">MEDIATYPE_Video，FORMAT_VideoInfo。</span><span class="sxs-lookup"><span data-stu-id="33940-119">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="33940-120">下列子類型有效：</span><span class="sxs-lookup"><span data-stu-id="33940-120">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="33940-121">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="33940-121">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="33940-122">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="33940-122">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="33940-123">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="33940-123">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="33940-124">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="33940-124">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="33940-125">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="33940-125">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33940-126">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="33940-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="33940-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="33940-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33940-128">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="33940-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="33940-129">CLSID_Colour</span><span class="sxs-lookup"><span data-stu-id="33940-129">CLSID_Colour</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33940-130">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="33940-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="33940-131">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="33940-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33940-132">可執行檔</span><span class="sxs-lookup"><span data-stu-id="33940-132">Executable</span></span></td>
<td><span data-ttu-id="33940-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="33940-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33940-134"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="33940-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="33940-135">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="33940-135">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33940-136"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="33940-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="33940-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="33940-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="33940-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="33940-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33940-139">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="33940-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




