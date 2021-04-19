---
description: 第21行解碼篩選
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: 第21行解碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970876"
---
# <a name="line-21-decoder-filter"></a><span data-ttu-id="26567-103">第21行解碼篩選</span><span class="sxs-lookup"><span data-stu-id="26567-103">Line 21 Decoder Filter</span></span>

<span data-ttu-id="26567-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="26567-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="26567-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="26567-105">It may be altered or unavailable in subsequent versions.</span></span>

<span data-ttu-id="26567-106">這一行21的解碼篩選器會解碼第21行的資料，並將標題文字繪製到點陣圖上。</span><span class="sxs-lookup"><span data-stu-id="26567-106">This Line 21 Decoder filter decodes line 21 data and draws the caption text onto bitmaps.</span></span>

<span data-ttu-id="26567-107">輸入 pin 會連接到任何第21行的資料提供者，通常是 DVD video 解碼器或 [CC 解碼器](cc-decoder-filter.md) 篩選器。</span><span class="sxs-lookup"><span data-stu-id="26567-107">The input pin connects to any line 21 data provider, typically either a DVD video decoder or the [CC Decoder](cc-decoder-filter.md) filter.</span></span> <span data-ttu-id="26567-108">CC 解碼器提供類比電視信號 VBI 的第21行資料。</span><span class="sxs-lookup"><span data-stu-id="26567-108">The CC Decoder provides line 21 data from the VBI of an analog television signal.</span></span> <span data-ttu-id="26567-109">輸出圖釘會連接到重迭 [混音](overlay-mixer-filter.md) 器上的次要 pin 或其他影片轉譯器，例如 VMR。</span><span class="sxs-lookup"><span data-stu-id="26567-109">The output pin connects to a secondary pin on the [Overlay Mixer](overlay-mixer-filter.md) or to another video renderer, such as the VMR.</span></span>

<span data-ttu-id="26567-110">此篩選器會接受標準位元組配對格式的第21行資料，或以 DVD 作為整個圖片群組 (GOP) 的封包。</span><span class="sxs-lookup"><span data-stu-id="26567-110">This filter accepts line 21 data in the standard byte-pair format or, for DVD, as a packet for the whole group of pictures (GOP).</span></span> <span data-ttu-id="26567-111">針對 DVD video 串流中的每個 GOP，可能會有使用者資料封包，其中包含該特定 GOP 的標頭資訊和第21行資料。</span><span class="sxs-lookup"><span data-stu-id="26567-111">For every GOP in the DVD video stream, there can be a user data packet that has that particular GOP's header information and line 21 data.</span></span> <span data-ttu-id="26567-112">位元組組的格式定義于 EIA/CEA-608-B 標準中;如需詳細資訊，請參閱該標準。</span><span class="sxs-lookup"><span data-stu-id="26567-112">The format of the byte pairs is defined in the EIA/CEA-608-B standard; please refer to that standard for more information.</span></span>

<span data-ttu-id="26567-113">此篩選器有兩個版本可供使用：</span><span class="sxs-lookup"><span data-stu-id="26567-113">Two versions of this filter are available:</span></span>



| <span data-ttu-id="26567-114">篩選</span><span class="sxs-lookup"><span data-stu-id="26567-114">Filter</span></span>            | <span data-ttu-id="26567-115">CLSID</span><span class="sxs-lookup"><span data-stu-id="26567-115">CLSID</span></span>                 |
|-------------------|-----------------------|
| <span data-ttu-id="26567-116">第21行的解碼器</span><span class="sxs-lookup"><span data-stu-id="26567-116">Line 21 Decoder</span></span>   | <span data-ttu-id="26567-117">CLSID \_ Line21Decoder</span><span class="sxs-lookup"><span data-stu-id="26567-117">CLSID\_Line21Decoder</span></span>  |
| <span data-ttu-id="26567-118">第21行的解碼器2</span><span class="sxs-lookup"><span data-stu-id="26567-118">Line 21 Decoder 2</span></span> | <span data-ttu-id="26567-119">CLSID \_ Line21Decoder2</span><span class="sxs-lookup"><span data-stu-id="26567-119">CLSID\_Line21Decoder2</span></span> |



 

<span data-ttu-id="26567-120">第1版的篩選器是在 Microsoft® Windows® 95/98/Me 和 Windows 2000 平臺上使用。</span><span class="sxs-lookup"><span data-stu-id="26567-120">The version 1 filter is used on Microsoft® Windows® 95/98/Me and Windows 2000 platforms.</span></span> <span data-ttu-id="26567-121">第2版的篩選器可在 Microsoft Windows XP 和更新版本中使用，並會在影片混合轉譯器位於圖形中時使用。</span><span class="sxs-lookup"><span data-stu-id="26567-121">The version 2 filter is available in Microsoft Windows XP and later, and is used whenever the Video Mixing Renderer is in the graph.</span></span>

<span data-ttu-id="26567-122">下表中的資訊適用于這兩個版本的篩選：</span><span class="sxs-lookup"><span data-stu-id="26567-122">The information in the following table applies to both versions of the filter:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26567-123">篩選介面</span><span class="sxs-lookup"><span data-stu-id="26567-123">Filter Interfaces</span></span></td>
<td><span data-ttu-id="26567-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="26567-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26567-125">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="26567-125">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="26567-126">主要類型： MEDIATYPE_AUXLine21DataSubtype：</span><span class="sxs-lookup"><span data-stu-id="26567-126">Major Type: MEDIATYPE_AUXLine21DataSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="26567-127">MEDIASUBTYPE_Line21_BytePair (標準行 21) </span><span class="sxs-lookup"><span data-stu-id="26567-127">MEDIASUBTYPE_Line21_BytePair (standard line 21)</span></span></li>
<li><span data-ttu-id="26567-128">MEDIASUBTYPE_Line21_GOPPacket (DVD 行 21) </span><span class="sxs-lookup"><span data-stu-id="26567-128">MEDIASUBTYPE_Line21_GOPPacket (DVD line 21)</span></span></li>
</ul>
<span data-ttu-id="26567-129">格式類型： FORMAT_VideoInfo 或 GUID_Null</span><span class="sxs-lookup"><span data-stu-id="26567-129">Format Type: FORMAT_VideoInfo or GUID_NULL</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26567-130">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="26567-130">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="26567-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="26567-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26567-132">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="26567-132">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="26567-133">主要類型： MEDIATYPE_VideoSubtype：</span><span class="sxs-lookup"><span data-stu-id="26567-133">Major type: MEDIATYPE_VideoSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="26567-134">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="26567-134">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="26567-135">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="26567-135">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="26567-136">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="26567-136">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="26567-137">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="26567-137">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="26567-138">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="26567-138">MEDIASUBTYPE_RGB32</span></span></li>
</ul>
<span data-ttu-id="26567-139">格式類型： FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="26567-139">Format Type: FORMAT_VideoInfo</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26567-140">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="26567-140">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="26567-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="26567-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26567-142">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="26567-142">Filter CLSID</span></span></td>
<td><span data-ttu-id="26567-143">請參閱上表</span><span class="sxs-lookup"><span data-stu-id="26567-143">See previous table</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26567-144">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="26567-144">Property Page CLSID</span></span></td>
<td><span data-ttu-id="26567-145">無</span><span class="sxs-lookup"><span data-stu-id="26567-145">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26567-146">可執行檔</span><span class="sxs-lookup"><span data-stu-id="26567-146">Executable</span></span></td>
<td><span data-ttu-id="26567-147">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="26567-147">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="26567-148"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="26567-148"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="26567-149">第21行： MERIT_NORMALLine 21 的解碼器2： MERIT_NORMAL + 2</span><span class="sxs-lookup"><span data-stu-id="26567-149">Line 21 Decoder: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26567-150"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="26567-150"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="26567-151">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="26567-151">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="26567-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="26567-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26567-153">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="26567-153">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="26567-154">隱藏式輔助字幕和 Teletext</span><span class="sxs-lookup"><span data-stu-id="26567-154">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> <dt>

[<span data-ttu-id="26567-155">DVD 篩選圖形設定</span><span class="sxs-lookup"><span data-stu-id="26567-155">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




