---
description: AVI Mux 篩選
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: AVI Mux 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3755a4d5f63e824ae08eb736a5999dcac3d7ab32
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846736"
---
# <a name="avi-mux-filter"></a><span data-ttu-id="c0c22-103">AVI Mux 篩選</span><span class="sxs-lookup"><span data-stu-id="c0c22-103">AVI Mux Filter</span></span>

<span data-ttu-id="c0c22-104">AVI Mux 篩選器接受多個輸入資料流程，並將它們交錯成 AVI 格式。</span><span class="sxs-lookup"><span data-stu-id="c0c22-104">The AVI Mux filter accepts multiple input streams and interleaves them into AVI format.</span></span> <span data-ttu-id="c0c22-105">篩選器會針對每個輸入資料流程使用不同的輸入圖釘，並針對 AVI 資料流程使用一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="c0c22-105">The filter uses separate input pins for each input stream, and one output pin for the AVI stream.</span></span>

<span data-ttu-id="c0c22-106">影片捕獲或撰寫應用程式可以使用此篩選器，將檔案以 AVI 格式儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="c0c22-106">Video capture or authoring applications can use this filter to save files to disk in AVI format.</span></span> <span data-ttu-id="c0c22-107">篩選通常會連接到檔案 [寫入](file-writer-filter.md) 器篩選器，但它可以連接到任何輸入 Pin 支援 IStream 和 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的篩選。</span><span class="sxs-lookup"><span data-stu-id="c0c22-107">The filter is typically connected to the [File Writer](file-writer-filter.md) filter, but it can connect to any filter whose input pin supports the IStream and [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0c22-108">篩選介面</span><span class="sxs-lookup"><span data-stu-id="c0c22-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="c0c22-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>、ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="c0c22-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0c22-110">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="c0c22-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="c0c22-111">對應至舊樣式 FOURCC 或 MEDIATYPE_AUXLine21Data 的任何主要型別。</span><span class="sxs-lookup"><span data-stu-id="c0c22-111">Any major type that corresponds to an old-style FOURCC, or MEDIATYPE_AUXLine21Data.</span></span> <span data-ttu-id="c0c22-112"> (需詳細資訊，請參閱 <a href="fourccmap.md"><strong>FOURCCMap 類別</strong></a>。 ) </span><span class="sxs-lookup"><span data-stu-id="c0c22-112">(For more information, see <a href="fourccmap.md"><strong>FOURCCMap Class</strong></a>.)</span></span>
<ul>
<li><span data-ttu-id="c0c22-113">如果主要類型為 MEDIATYPE_Audio，則格式必須為 FORMAT_WaveFormatEx。</span><span class="sxs-lookup"><span data-stu-id="c0c22-113">If the major type is MEDIATYPE_Audio, the format must be FORMAT_WaveFormatEx.</span></span></li>
<li><span data-ttu-id="c0c22-114">如果主要類型為 MEDIATYPE_Video，則格式必須為 FORMAT_VideoInfo 或 FORMAT_DvInfo。</span><span class="sxs-lookup"><span data-stu-id="c0c22-114">If the major type is MEDIATYPE_Video, the format must be FORMAT_VideoInfo or FORMAT_DvInfo.</span></span></li>
<li><span data-ttu-id="c0c22-115">如果主要類型為 MEDIATYPE_Interleaved，則格式必須為 FORMAT_DvInfo。</span><span class="sxs-lookup"><span data-stu-id="c0c22-115">If the major type is MEDIATYPE_Interleaved, the format must be FORMAT_DvInfo.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0c22-116">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="c0c22-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="c0c22-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、IPropertyBag、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="c0c22-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0c22-118">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="c0c22-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="c0c22-119">MEDIATYPE_Stream，MEDIASUBTYPE_Avi</span><span class="sxs-lookup"><span data-stu-id="c0c22-119">MEDIATYPE_Stream, MEDIASUBTYPE_Avi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0c22-120">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="c0c22-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="c0c22-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="c0c22-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0c22-122">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="c0c22-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="c0c22-123">CLSID_AviDest</span><span class="sxs-lookup"><span data-stu-id="c0c22-123">CLSID_AviDest</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0c22-124">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="c0c22-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="c0c22-125">CLSID_AviMuxProptyPage，CLSID_AviMuxProptyPage1</span><span class="sxs-lookup"><span data-stu-id="c0c22-125">CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0c22-126">可執行檔</span><span class="sxs-lookup"><span data-stu-id="c0c22-126">Executable</span></span></td>
<td><span data-ttu-id="c0c22-127">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="c0c22-127">qcap.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0c22-128"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="c0c22-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="c0c22-129">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="c0c22-129">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0c22-130"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="c0c22-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="c0c22-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="c0c22-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a><span data-ttu-id="c0c22-132">備註</span><span class="sxs-lookup"><span data-stu-id="c0c22-132">Remarks</span></span>

<span data-ttu-id="c0c22-133">下列備註說明 AVI Mux 篩選功能的各種層面。</span><span class="sxs-lookup"><span data-stu-id="c0c22-133">The following remarks describe various aspects of the AVI Mux filter's functionality.</span></span>

<span data-ttu-id="c0c22-134">釘選</span><span class="sxs-lookup"><span data-stu-id="c0c22-134">Pins</span></span>

<span data-ttu-id="c0c22-135">建立 AVI Mux 篩選器時，它會有一個輸入的 pin。</span><span class="sxs-lookup"><span data-stu-id="c0c22-135">When the AVI Mux filter is created, it has one input pin.</span></span> <span data-ttu-id="c0c22-136">當每個輸入 pin 連線時，篩選準則會建立新的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="c0c22-136">As each input pin is connected, the filter creates a new input pin.</span></span>

<span data-ttu-id="c0c22-137">資料流程屬性</span><span class="sxs-lookup"><span data-stu-id="c0c22-137">Stream Properties</span></span>

<span data-ttu-id="c0c22-138">輸入 pin 支援 IPropertyBag 介面，以便在個別資料流程上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="c0c22-138">The input pins support the IPropertyBag interface for setting properties on individual streams.</span></span> <span data-ttu-id="c0c22-139">目前已定義下列屬性：</span><span class="sxs-lookup"><span data-stu-id="c0c22-139">Currently, the following property is defined:</span></span>



| <span data-ttu-id="c0c22-140">屬性</span><span class="sxs-lookup"><span data-stu-id="c0c22-140">Property</span></span> | <span data-ttu-id="c0c22-141">描述</span><span class="sxs-lookup"><span data-stu-id="c0c22-141">Description</span></span>                                                           |
|----------|-----------------------------------------------------------------------|
| <span data-ttu-id="c0c22-142">NAME</span><span class="sxs-lookup"><span data-stu-id="c0c22-142">name</span></span>     | <span data-ttu-id="c0c22-143">資料流的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0c22-143">The name of the stream.</span></span> <span data-ttu-id="c0c22-144">這個屬性會寫入為 `'strn'` 區塊。</span><span class="sxs-lookup"><span data-stu-id="c0c22-144">This property is written as a `'strn'` chunk.</span></span> |



 

<span data-ttu-id="c0c22-145">如果篩選器正在執行或已暫停，IPropertyBag：： Write 方法會傳回 VFW \_ E \_ 錯誤的 \_ 狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c22-145">If the filter is running or paused, the IPropertyBag::Write method returns VFW\_E\_WRONG\_STATE.</span></span>

<span data-ttu-id="c0c22-146">畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="c0c22-146">Frame Rates</span></span>

<span data-ttu-id="c0c22-147">如果上游篩選未在 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構的 **AvgTimePerFrame** 成員中指定畫面播放速率，則 AVI Mux 會使用第一個影片畫面上的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="c0c22-147">If the upstream filter does not specify a frame rate in the **AvgTimePerFrame** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, the AVI Mux uses the time stamps on the first video frame.</span></span> <span data-ttu-id="c0c22-148">AVI 檔案格式不支援可變的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="c0c22-148">The AVI file format does not support variable frame rates.</span></span>

<span data-ttu-id="c0c22-149">捨棄的畫面格</span><span class="sxs-lookup"><span data-stu-id="c0c22-149">Dropped Frames</span></span>

<span data-ttu-id="c0c22-150">AVI Mux 篩選器會根據每個樣本的媒體時間（如果有的話）來計算已卸載的框架，或使用範例的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="c0c22-150">The AVI Mux filter calculates dropped frames based on each sample's media times, if available, or else the sample's time stamps.</span></span> <span data-ttu-id="c0c22-151">它會針對每個已捨棄的框架寫入長度為零的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="c0c22-151">It writes a zero-length index entry for every dropped frame.</span></span>

<span data-ttu-id="c0c22-152">IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="c0c22-152">IMediaSeeking</span></span>

<span data-ttu-id="c0c22-153">AVI Mux 篩選器會實 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c0c22-153">The AVI Mux filter implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface as follows:</span></span>

-   <span data-ttu-id="c0c22-154">[**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition)方法會傳回多工處理的目前進度。</span><span class="sxs-lookup"><span data-stu-id="c0c22-154">The [**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the current progress of the multiplexing.</span></span> <span data-ttu-id="c0c22-155">如果您正在轉碼檔案 (慢于即時) ，此值會比篩選圖形管理員所傳回的值更準確。</span><span class="sxs-lookup"><span data-stu-id="c0c22-155">If you are transcoding a file (slower than real time), this value is more accurate than the value returned by the Filter Graph Manager.</span></span> <span data-ttu-id="c0c22-156">如需詳細資訊，請參閱 GetCurrentPosition 參考頁面的備註一節。</span><span class="sxs-lookup"><span data-stu-id="c0c22-156">For more information, see the Remarks section of the GetCurrentPosition reference page.</span></span>
-   <span data-ttu-id="c0c22-157">[**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)方法會查詢每個上游篩選器，並傳回最長資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="c0c22-157">The [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method queries each upstream filter and returns the duration of the longest stream.</span></span> <span data-ttu-id="c0c22-158">如果這些篩選準則中有任何一個失敗 (或不支援 IMediaSeeking) ，則 AVI Mux 會傳回失敗碼，並在找到的最長持續時間內填入 *pDuration* 參數。</span><span class="sxs-lookup"><span data-stu-id="c0c22-158">If any of these filters fails the GetDuration call (or does not support IMediaSeeking), the AVI Mux returns a failure code and fills in the *pDuration* parameter with the longest duration found.</span></span> <span data-ttu-id="c0c22-159">不過，在此情況下， *pDuration* 的值不一定是最長輸入資料流程的長度。</span><span class="sxs-lookup"><span data-stu-id="c0c22-159">However, the value of *pDuration* in this case is not necessarily the length of the longest input stream.</span></span>
-   <span data-ttu-id="c0c22-160">AVI Mux 不會執行 GetStopPosition、GetPositions、GetAvailable、GetRate 或 GetPreroll 方法;也不會執行任何 Set \* 方法進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="c0c22-160">The AVI Mux does not implement the GetStopPosition, GetPositions, GetAvailable, GetRate, or GetPreroll methods; nor does it implement any Set\* methods for seeking.</span></span>

<span data-ttu-id="c0c22-161">AVI 2.0 檔案格式延伸模組</span><span class="sxs-lookup"><span data-stu-id="c0c22-161">AVI 2.0 File Format Extensions</span></span>

<span data-ttu-id="c0c22-162">DirectShow 目前支援下列 AVI 2.0 檔案格式延伸模組：</span><span class="sxs-lookup"><span data-stu-id="c0c22-162">DirectShow currently supports the following AVI 2.0 file format extensions:</span></span>

-   <span data-ttu-id="c0c22-163"> (大於 1 GB 的 AVI 檔案大小增加) </span><span class="sxs-lookup"><span data-stu-id="c0c22-163">Increased AVI file size (greater than 1 GB)</span></span>
-   <span data-ttu-id="c0c22-164">階層式索引編制</span><span class="sxs-lookup"><span data-stu-id="c0c22-164">Hierarchical indexing</span></span>

<span data-ttu-id="c0c22-165">如需詳細資訊，請參閱 OpenDML AVI M-JPEG 檔案格式 Subcommittee 所發佈之「OpenDML AVI 檔案格式延伸模組」的1.02 版。</span><span class="sxs-lookup"><span data-stu-id="c0c22-165">For more information, see version 1.02 of the "OpenDML AVI File Format Extensions" published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0c22-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="c0c22-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0c22-167">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="c0c22-167">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



