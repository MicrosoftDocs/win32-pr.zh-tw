---
description: AVI 分隔器篩選
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: AVI 分隔器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24335511e9b7b866c85792c2036a4d4b6d089f2a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909656"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="8c774-103">AVI 分隔器篩選</span><span class="sxs-lookup"><span data-stu-id="8c774-103">AVI Splitter Filter</span></span>

<span data-ttu-id="8c774-104">AVI 分隔器篩選器是用來播放 AVI 檔。</span><span class="sxs-lookup"><span data-stu-id="8c774-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="8c774-105">它接受 AVI 格式的資料，並將其分割成其組成的資料流程，以進行進一步的處理和/或轉譯。</span><span class="sxs-lookup"><span data-stu-id="8c774-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



| <span data-ttu-id="8c774-106">標籤</span><span class="sxs-lookup"><span data-stu-id="8c774-106">Label</span></span> | <span data-ttu-id="8c774-107">值</span><span class="sxs-lookup"><span data-stu-id="8c774-107">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c774-108">篩選介面</span><span class="sxs-lookup"><span data-stu-id="8c774-108">Filter Interfaces</span></span>                        | <span data-ttu-id="8c774-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="8c774-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="8c774-110">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="8c774-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="8c774-111">媒體媒體 \_ 、MEDIASUBTYPE \_ Avi</span><span class="sxs-lookup"><span data-stu-id="8c774-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="8c774-112">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="8c774-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="8c774-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8c774-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="8c774-114">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="8c774-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="8c774-115">通常是媒體或 **媒體 \_** 媒體的 **媒體 \_** 。</span><span class="sxs-lookup"><span data-stu-id="8c774-115">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="8c774-116">確切的類型取決於檔案的內容、是否壓縮檔案，以及使用何種編解碼器。</span><span class="sxs-lookup"><span data-stu-id="8c774-116">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="8c774-117">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="8c774-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="8c774-118">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、IPropertyBag、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8c774-118">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="8c774-119">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="8c774-119">Filter CLSID</span></span>                             | <span data-ttu-id="8c774-120">CLSID \_ AviSplitter</span><span class="sxs-lookup"><span data-stu-id="8c774-120">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="8c774-121">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="8c774-121">Property Page CLSID</span></span>                      | <span data-ttu-id="8c774-122">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="8c774-122">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="8c774-123">可執行檔</span><span class="sxs-lookup"><span data-stu-id="8c774-123">Executable</span></span>                               | <span data-ttu-id="8c774-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="8c774-124">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="8c774-125">優點</span><span class="sxs-lookup"><span data-stu-id="8c774-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="8c774-126">一般的業績 \_</span><span class="sxs-lookup"><span data-stu-id="8c774-126">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="8c774-127">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="8c774-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="8c774-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="8c774-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="8c774-129">備註</span><span class="sxs-lookup"><span data-stu-id="8c774-129">Remarks</span></span>

<span data-ttu-id="8c774-130">此篩選通常會連接到其輸入 pin 的 [非同步檔案來源](file-source--async--filter.md) 篩選。</span><span class="sxs-lookup"><span data-stu-id="8c774-130">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="8c774-131">它可以連線到輸出 pin 支援 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 的任何篩選器，並提供正確的媒體類型給 AVI 分隔器篩選的輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="8c774-131">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="8c774-132">AVI 分隔器上的輸出圖釘支援 IPropertyBag：： Read 方法，以便從個別資料流程讀取屬性。</span><span class="sxs-lookup"><span data-stu-id="8c774-132">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="8c774-133">目前已定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="8c774-133">Currently, the following property is defined.</span></span>



| <span data-ttu-id="8c774-134">屬性</span><span class="sxs-lookup"><span data-stu-id="8c774-134">Property</span></span> | <span data-ttu-id="8c774-135">描述</span><span class="sxs-lookup"><span data-stu-id="8c774-135">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c774-136">NAME</span><span class="sxs-lookup"><span data-stu-id="8c774-136">name</span></span>     | <span data-ttu-id="8c774-137">傳回從 AVI 檔案中的區塊取得的資料流程名稱 `'strn'` 。</span><span class="sxs-lookup"><span data-stu-id="8c774-137">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="8c774-138">如果這個區塊不存在，Read 方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="8c774-138">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="8c774-139">IPropertyBag：： Write 方法會傳回 E \_ FAIL。</span><span class="sxs-lookup"><span data-stu-id="8c774-139">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="8c774-140">[Avi Mux](avi-mux-filter.md)篩選支援 IPropertyBag：： Write，可將資料流程屬性儲存到 AVI 檔案中。</span><span class="sxs-lookup"><span data-stu-id="8c774-140">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="8c774-141">AVI 分隔器不允許下游篩選器使用自己的配置器。</span><span class="sxs-lookup"><span data-stu-id="8c774-141">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="8c774-142">檔案中交錯的持續時間會決定 AVI 分隔器將配置多少記憶體來處理它。</span><span class="sxs-lookup"><span data-stu-id="8c774-142">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="8c774-143">交錯在一個第二個區塊中的檔案需要更多的記憶體來處理，而不是將交錯期間設定為一或兩個畫面格的檔案。</span><span class="sxs-lookup"><span data-stu-id="8c774-143">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="8c774-144">在新式電腦上，除非您同時執行 AVI 分隔器的多個實例，否則這通常不是問題。</span><span class="sxs-lookup"><span data-stu-id="8c774-144">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="8c774-145">尋求</span><span class="sxs-lookup"><span data-stu-id="8c774-145">Seeking</span></span>

<span data-ttu-id="8c774-146">如果檔案包含影片資料流程，AVI 分隔器支援依框架編號搜尋。</span><span class="sxs-lookup"><span data-stu-id="8c774-146">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="8c774-147">若要啟用以框架為基礎的搜尋，請在 [篩選圖形管理員](filter-graph-manager.md)上以值 **時間 \_ 格式 \_ 框架** 呼叫 [**IMediaSeeking：： SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 。</span><span class="sxs-lookup"><span data-stu-id="8c774-147">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="8c774-148">如果檔案包含音訊串流，AVI 分隔器支援依樣本數進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="8c774-148">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="8c774-149">若要啟用以範例為基礎的搜尋，請使用值 **時間 \_ 格式 \_ 範例**，在篩選圖形管理員上呼叫 [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) 。</span><span class="sxs-lookup"><span data-stu-id="8c774-149">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="8c774-150">在這兩種情況下，該資料流程的輸出圖釘都必須連接到轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="8c774-150">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c774-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c774-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c774-152">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="8c774-152">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



