---
description: MPEG-2 資料流程分隔器篩選
ms.assetid: abadf37f-2876-496d-90e7-77c3475a0064
title: MPEG-2 資料流程分隔器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec47e5ad8df16446c588beec2c5d1c2606b9b1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109648"
---
# <a name="mpeg-1-stream-splitter-filter"></a><span data-ttu-id="78684-103">MPEG-2 資料流程分隔器篩選</span><span class="sxs-lookup"><span data-stu-id="78684-103">MPEG-1 Stream Splitter Filter</span></span>

<span data-ttu-id="78684-104">此篩選器會將 MPEG-2 系統資料流程分割成其元件音訊和影片串流。</span><span class="sxs-lookup"><span data-stu-id="78684-104">This filter splits an MPEG-1 system stream into its component audio and video streams.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="78684-105">篩選介面</span><span class="sxs-lookup"><span data-stu-id="78684-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="78684-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="78684-106"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78684-107">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="78684-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="78684-108">主要類型： MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="78684-108">Major type: MEDIATYPE_Stream</span></span><br/> <span data-ttu-id="78684-109">亞：</span><span class="sxs-lookup"><span data-stu-id="78684-109">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="78684-110">MEDIASUBTYPE_MPEG1System</span><span class="sxs-lookup"><span data-stu-id="78684-110">MEDIASUBTYPE_MPEG1System</span></span></li>
<li><span data-ttu-id="78684-111">MEDIASUBTYPE_MPEG1VideoCD</span><span class="sxs-lookup"><span data-stu-id="78684-111">MEDIASUBTYPE_MPEG1VideoCD</span></span></li>
<li><span data-ttu-id="78684-112">MEDIASUBTYPE_Audio</span><span class="sxs-lookup"><span data-stu-id="78684-112">MEDIASUBTYPE_Audio</span></span></li>
<li><span data-ttu-id="78684-113">MEDIASUBTYPE_Video</span><span class="sxs-lookup"><span data-stu-id="78684-113">MEDIASUBTYPE_Video</span></span></li>
</ul>
<span data-ttu-id="78684-114">請參閱<a href="mpeg-1-media-types.md"> <strong>Mpeg-2 媒體類型</strong></a></span><span class="sxs-lookup"><span data-stu-id="78684-114">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78684-115">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="78684-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="78684-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="78684-116"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78684-117">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="78684-117">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="78684-118">主要類型： MEDIATYPE_Audio 或 MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="78684-118">Major type: MEDIATYPE_Audio or MEDIATYPE_Video</span></span><br/> <span data-ttu-id="78684-119">子類型： MEDIASUBTYPE_MPEG1Payload 或 MEDIASUBTYPE_MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="78684-119">Subtype: MEDIASUBTYPE_MPEG1Payload or MEDIASUBTYPE_MPEG1Packet</span></span><br/> <span data-ttu-id="78684-120">請參閱<a href="mpeg-1-media-types.md"> <strong>Mpeg-2 媒體類型</strong></a></span><span class="sxs-lookup"><span data-stu-id="78684-120">See <a href="mpeg-1-media-types.md"><strong>MPEG-1 Media Types</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78684-121">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="78684-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="78684-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="78684-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78684-123">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="78684-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="78684-124">CLSID_MPEG1Splitter</span><span class="sxs-lookup"><span data-stu-id="78684-124">CLSID_MPEG1Splitter</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78684-125">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="78684-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="78684-126">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="78684-126">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78684-127">可執行檔</span><span class="sxs-lookup"><span data-stu-id="78684-127">Executable</span></span></td>
<td><span data-ttu-id="78684-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="78684-128">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78684-129"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="78684-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="78684-130">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="78684-130">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78684-131"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="78684-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="78684-132">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="78684-132">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="78684-133">備註</span><span class="sxs-lookup"><span data-stu-id="78684-133">Remarks</span></span>

<span data-ttu-id="78684-134">此檔案僅支援透過 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 的提取模式;它不支援 push 模式。</span><span class="sxs-lookup"><span data-stu-id="78684-134">This file supports pull mode via [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) only; it does not support push mode.</span></span>

<span data-ttu-id="78684-135">由於 MPEG-2 內容未建立索引，因此搜尋可能非常近似。</span><span class="sxs-lookup"><span data-stu-id="78684-135">Because MPEG-1 content is not indexed, seeking can be very approximate.</span></span> <span data-ttu-id="78684-136">通常適用于固定位元速率的 MPEG-2 系統串流 (通常是針對視訊 CD) 產生的硬體。</span><span class="sxs-lookup"><span data-stu-id="78684-136">It is usually good for a fixed bitrate MPEG-1 system stream (which is usually hardware generated for video CD).</span></span>

<span data-ttu-id="78684-137">篩選準則支援 [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) 介面，可用於抓取 ID3 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="78684-137">The filter supports the [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) interface for retrieving ID3 metadata.</span></span>

<span data-ttu-id="78684-138">並非所有 MPEG 範例都有時間戳記。</span><span class="sxs-lookup"><span data-stu-id="78684-138">Not all MPEG samples have time stamps.</span></span> <span data-ttu-id="78684-139">MPEG 範例上缺少時間戳記並不是錯誤。</span><span class="sxs-lookup"><span data-stu-id="78684-139">The lack of a time stamp on an MPEG sample is not an error.</span></span> <span data-ttu-id="78684-140">若為篩選開發人員，這表示如果 [**IMediaSample：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime)失敗，您就不應該從輸入 Pin 的 **Receive** 方法傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="78684-140">For filter developers, this means that you should not return an error code from your input pin's **Receive** method if [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) fails.</span></span> <span data-ttu-id="78684-141">如果 **Receive** 傳回 S 以外的任何值 \_ ，則會導致分隔器停止傳送範例。</span><span class="sxs-lookup"><span data-stu-id="78684-141">If **Receive** returns any value other than S\_OK, it will cause the splitter to stop sending samples.</span></span>

<span data-ttu-id="78684-142">如果檔案包含影片資料流程，則 MPEG-2 資料流程分隔器支援依框架編號搜尋。</span><span class="sxs-lookup"><span data-stu-id="78684-142">If the file contains a video stream, the MPEG-1 Stream Splitter supports seeking by frame number.</span></span> <span data-ttu-id="78684-143">若要啟用以框架為基礎的搜尋，請在 [篩選圖形管理員](filter-graph-manager.md)上以值 **時間 \_ 格式 \_ 框架** 呼叫 [**IMediaSeeking：： SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 。</span><span class="sxs-lookup"><span data-stu-id="78684-143">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78684-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="78684-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78684-145">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="78684-145">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




