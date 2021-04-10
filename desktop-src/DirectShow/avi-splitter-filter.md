---
description: AVI 分隔器篩選
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: AVI 分隔器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61b9a60c4c42aafa875c166ae08ccdf337793c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109713"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="1f514-103">AVI 分隔器篩選</span><span class="sxs-lookup"><span data-stu-id="1f514-103">AVI Splitter Filter</span></span>

<span data-ttu-id="1f514-104">AVI 分隔器篩選器是用來播放 AVI 檔。</span><span class="sxs-lookup"><span data-stu-id="1f514-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="1f514-105">它接受 AVI 格式的資料，並將其分割成其組成的資料流程，以進行進一步的處理和/或轉譯。</span><span class="sxs-lookup"><span data-stu-id="1f514-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



|                                          |                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f514-106">篩選介面</span><span class="sxs-lookup"><span data-stu-id="1f514-106">Filter Interfaces</span></span>                        | <span data-ttu-id="1f514-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="1f514-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="1f514-108">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="1f514-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="1f514-109">媒體媒體 \_ 、MEDIASUBTYPE \_ Avi</span><span class="sxs-lookup"><span data-stu-id="1f514-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="1f514-110">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="1f514-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="1f514-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1f514-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="1f514-112">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="1f514-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="1f514-113">通常是媒體或 **媒體 \_** 媒體的 **媒體 \_** 。</span><span class="sxs-lookup"><span data-stu-id="1f514-113">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="1f514-114">確切的類型取決於檔案的內容、是否壓縮檔案，以及使用何種編解碼器。</span><span class="sxs-lookup"><span data-stu-id="1f514-114">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="1f514-115">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="1f514-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="1f514-116">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、IPropertyBag、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1f514-116">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="1f514-117">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="1f514-117">Filter CLSID</span></span>                             | <span data-ttu-id="1f514-118">CLSID \_ AviSplitter</span><span class="sxs-lookup"><span data-stu-id="1f514-118">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="1f514-119">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="1f514-119">Property Page CLSID</span></span>                      | <span data-ttu-id="1f514-120">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="1f514-120">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="1f514-121">可執行檔</span><span class="sxs-lookup"><span data-stu-id="1f514-121">Executable</span></span>                               | <span data-ttu-id="1f514-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1f514-122">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="1f514-123">優點</span><span class="sxs-lookup"><span data-stu-id="1f514-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="1f514-124">一般的業績 \_</span><span class="sxs-lookup"><span data-stu-id="1f514-124">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="1f514-125">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="1f514-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="1f514-126">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="1f514-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="1f514-127">備註</span><span class="sxs-lookup"><span data-stu-id="1f514-127">Remarks</span></span>

<span data-ttu-id="1f514-128">此篩選通常會連接到其輸入 pin 的 [非同步檔案來源](file-source--async--filter.md) 篩選。</span><span class="sxs-lookup"><span data-stu-id="1f514-128">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="1f514-129">它可以連線到輸出 pin 支援 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 的任何篩選器，並提供正確的媒體類型給 AVI 分隔器篩選的輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="1f514-129">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="1f514-130">AVI 分隔器上的輸出圖釘支援 IPropertyBag：： Read 方法，以便從個別資料流程讀取屬性。</span><span class="sxs-lookup"><span data-stu-id="1f514-130">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="1f514-131">目前已定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="1f514-131">Currently, the following property is defined.</span></span>



| <span data-ttu-id="1f514-132">屬性</span><span class="sxs-lookup"><span data-stu-id="1f514-132">Property</span></span> | <span data-ttu-id="1f514-133">描述</span><span class="sxs-lookup"><span data-stu-id="1f514-133">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f514-134">NAME</span><span class="sxs-lookup"><span data-stu-id="1f514-134">name</span></span>     | <span data-ttu-id="1f514-135">傳回從 AVI 檔案中的區塊取得的資料流程名稱 `'strn'` 。</span><span class="sxs-lookup"><span data-stu-id="1f514-135">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="1f514-136">如果這個區塊不存在，Read 方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="1f514-136">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="1f514-137">IPropertyBag：： Write 方法會傳回 E \_ FAIL。</span><span class="sxs-lookup"><span data-stu-id="1f514-137">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="1f514-138">[Avi Mux](avi-mux-filter.md)篩選支援 IPropertyBag：： Write，可將資料流程屬性儲存到 AVI 檔案中。</span><span class="sxs-lookup"><span data-stu-id="1f514-138">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="1f514-139">AVI 分隔器不允許下游篩選器使用自己的配置器。</span><span class="sxs-lookup"><span data-stu-id="1f514-139">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="1f514-140">檔案中交錯的持續時間會決定 AVI 分隔器將配置多少記憶體來處理它。</span><span class="sxs-lookup"><span data-stu-id="1f514-140">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="1f514-141">交錯在一個第二個區塊中的檔案需要更多的記憶體來處理，而不是將交錯期間設定為一或兩個畫面格的檔案。</span><span class="sxs-lookup"><span data-stu-id="1f514-141">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="1f514-142">在新式電腦上，除非您同時執行 AVI 分隔器的多個實例，否則這通常不是問題。</span><span class="sxs-lookup"><span data-stu-id="1f514-142">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="1f514-143">尋求</span><span class="sxs-lookup"><span data-stu-id="1f514-143">Seeking</span></span>

<span data-ttu-id="1f514-144">如果檔案包含影片資料流程，AVI 分隔器支援依框架編號搜尋。</span><span class="sxs-lookup"><span data-stu-id="1f514-144">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="1f514-145">若要啟用以框架為基礎的搜尋，請在 [篩選圖形管理員](filter-graph-manager.md)上以值 **時間 \_ 格式 \_ 框架** 呼叫 [**IMediaSeeking：： SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 。</span><span class="sxs-lookup"><span data-stu-id="1f514-145">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="1f514-146">如果檔案包含音訊串流，AVI 分隔器支援依樣本數進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="1f514-146">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="1f514-147">若要啟用以範例為基礎的搜尋，請使用值 **時間 \_ 格式 \_ 範例**，在篩選圖形管理員上呼叫 [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 。</span><span class="sxs-lookup"><span data-stu-id="1f514-147">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="1f514-148">在這兩種情況下，該資料流程的輸出圖釘都必須連接到轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="1f514-148">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f514-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f514-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f514-150">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="1f514-150">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



