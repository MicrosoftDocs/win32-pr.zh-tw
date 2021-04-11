---
description: 建立 Recompression 圖形
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: 建立 Recompression 圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8ea604bead34c22c123bbabe5d88e985006a9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845855"
---
# <a name="building-the-recompression-graph"></a><span data-ttu-id="4d9f9-103">建立 Recompression 圖形</span><span class="sxs-lookup"><span data-stu-id="4d9f9-103">Building the Recompression Graph</span></span>

<span data-ttu-id="4d9f9-104">AVI 檔案 recompression 的一般篩選圖形看起來如下所示：</span><span class="sxs-lookup"><span data-stu-id="4d9f9-104">A typical filter graph for AVI file recompression looks like the following:</span></span>

![avi recompression 圖形](images/avi2avi4.png)

<span data-ttu-id="4d9f9-106">[AVI 分隔器篩選器](avi-splitter-filter.md)會從檔案[來源提取資料 (Async) 篩選器](file-source--async--filter.md)，並將它剖析成影片和音訊串流。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-106">The [AVI Splitter Filter](avi-splitter-filter.md) pulls data from the [File Source (Async) Filter](file-source--async--filter.md) and parses it into video and audio streams.</span></span> <span data-ttu-id="4d9f9-107">影片解壓縮程式會將壓縮的影片解碼，而影片壓縮程式會 recompressed 此影片。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-107">The video decompressor decodes the compressed video, where it is recompressed by the video compressor.</span></span> <span data-ttu-id="4d9f9-108">Decompressors 的選擇取決於原始程式檔;它會由 [智慧型 Connect](intelligent-connect.md)自動處理。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-108">The choice of decompressors depends on the source file; it will be handled automatically by [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="4d9f9-109">應用程式必須選擇壓縮程式，通常是向使用者呈現清單。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-109">The application must choose the compressor, typically by presenting a list to the user.</span></span> <span data-ttu-id="4d9f9-110"> (，請參閱 [選擇壓縮篩選](choosing-a-compression-filter.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="4d9f9-110">(See [Choosing a Compression Filter](choosing-a-compression-filter.md).)</span></span>

<span data-ttu-id="4d9f9-111">壓縮的影片接著會進入 [AVI Mux 篩選器](avi-mux-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-111">The compressed video then goes to the [AVI Mux Filter](avi-mux-filter.md).</span></span> <span data-ttu-id="4d9f9-112">此範例中的音訊串流未壓縮，因此會直接從 AVI 分隔器移至 AVI Mux。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-112">The audio stream in this example is not compressed, so it goes directly from the AVI Splitter to the AVI Mux.</span></span> <span data-ttu-id="4d9f9-113">AVI Mux 會交錯兩個數據流，而檔案 [寫入器篩選器](file-writer-filter.md) 會將輸出寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-113">The AVI Mux interleaves the two streams, and the [File Writer Filter](file-writer-filter.md) writes the output to disk.</span></span> <span data-ttu-id="4d9f9-114">請注意，即使原始檔案沒有音訊資料流程，也需要 AVI Mux。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-114">Note that the AVI Mux is required even if the original file does not have an audio stream.</span></span>

<span data-ttu-id="4d9f9-115">建立此篩選圖形最簡單的方式是使用「 [捕獲圖形](capture-graph-builder.md)產生器」，這是用來建立捕獲圖形和其他自訂篩選圖形的 DirectShow 元件。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-115">The easiest way to build this filter graph is to use the [Capture Graph Builder](capture-graph-builder.md), which is a DirectShow component for building capture graphs and other custom filter graphs.</span></span>

<span data-ttu-id="4d9f9-116">首先，呼叫 CoCreateInstance 以建立「捕獲圖形產生器」：</span><span class="sxs-lookup"><span data-stu-id="4d9f9-116">Start by calling CoCreateInstance to create the Capture Graph Builder:</span></span>


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



<span data-ttu-id="4d9f9-117">然後使用 [Capture Graph Builder] 來建立篩選圖形：</span><span class="sxs-lookup"><span data-stu-id="4d9f9-117">Then use the Capture Graph Builder to build the filter graph:</span></span>

1.  <span data-ttu-id="4d9f9-118">建立圖形的轉譯區段，其中包括 AVI Mux 篩選器和檔案 [寫入](file-writer-filter.md)器。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-118">Build the rendering section of the graph, which includes the AVI Mux filter and the [File Writer](file-writer-filter.md).</span></span>
2.  <span data-ttu-id="4d9f9-119">將來源篩選和壓縮篩選新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-119">Add the source filter and the compression filter to the graph.</span></span>
3.  <span data-ttu-id="4d9f9-120">將來源篩選連接至 MUX 篩選器。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-120">Connect the source filter to the MUX filter.</span></span> <span data-ttu-id="4d9f9-121">「捕獲圖形產生器」會插入剖析來源檔案時所需的任何分隔器和解碼篩選器。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-121">The capture graph builder inserts whatever splitter and decoder filters are needed to parse the source file.</span></span> <span data-ttu-id="4d9f9-122">它也可以透過壓縮篩選器來路由傳送影片和音訊串流。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-122">It can also route the video and audio streams through compression filters.</span></span>

<span data-ttu-id="4d9f9-123">下列各節將說明每個步驟。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-123">The following sections explain each of these steps.</span></span>

<span data-ttu-id="4d9f9-124">建立轉譯區段</span><span class="sxs-lookup"><span data-stu-id="4d9f9-124">Build the Rendering Section</span></span>

<span data-ttu-id="4d9f9-125">若要建立圖形的轉譯區段，請呼叫 [**ICaptureGraphBuilder2：： SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) 方法。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-125">To build the rendering section of the graph, call the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method.</span></span> <span data-ttu-id="4d9f9-126">這個方法會採用輸入參數，以指定輸出的媒體子類型和輸出檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-126">This method takes input parameters that specify the media subtype for the output and the name of the output file.</span></span> <span data-ttu-id="4d9f9-127">它會傳回 MUX 篩選器和檔案寫入器的指標。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-127">It returns pointers to the MUX filter and the file writer.</span></span> <span data-ttu-id="4d9f9-128">下一階段的 graph 大樓需要 MUX 篩選器。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-128">The MUX filter is needed for the next stage of graph building.</span></span> <span data-ttu-id="4d9f9-129">這個範例不需要檔案寫入器的指標，所以參數可以是 **Null**：</span><span class="sxs-lookup"><span data-stu-id="4d9f9-129">The pointer to the file writer is not needed for this example, so that parameter can be **NULL**:</span></span>


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



<span data-ttu-id="4d9f9-130">當方法傳回時，MUX 篩選具有未處理的參考計數，因此請務必稍後再釋放指標。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-130">When the method returns, the MUX filter has an outstanding reference count, so be sure to release the pointer later.</span></span>

<span data-ttu-id="4d9f9-131">下圖顯示此時間點的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-131">The following diagram shows the filter graph at this point.</span></span>

![篩選圖形的轉譯區段](images/avi2avi1.png)

<span data-ttu-id="4d9f9-133">MUX 篩選器會公開兩個介面來控制 AVI 格式：</span><span class="sxs-lookup"><span data-stu-id="4d9f9-133">The MUX filter exposes two interfaces for controlling the AVI format:</span></span>

-   <span data-ttu-id="4d9f9-134">[**IConfigInterleaving 介面**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)：設定交錯模式。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-134">[**IConfigInterleaving Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): Sets the interleaving mode.</span></span>
-   <span data-ttu-id="4d9f9-135">[**IConfigAviMux 介面**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)：設定主要資料流程和 AVI 相容性索引。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-135">[**IConfigAviMux Interface**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): Sets the master stream and the AVI compatibility index.</span></span>

<span data-ttu-id="4d9f9-136">新增來源和壓縮篩選</span><span class="sxs-lookup"><span data-stu-id="4d9f9-136">Add the Source and Compression Filters</span></span>

<span data-ttu-id="4d9f9-137">下一步是要將來源和壓縮篩選新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-137">The next step is to add the source and compression filters to the filter graph.</span></span> <span data-ttu-id="4d9f9-138">當您呼叫 SetOutputFileName 時，「捕獲圖形產生器」會自動建立篩選圖形管理員的實例。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-138">The Capture Graph Builder automatically creates an instance of the Filter Graph Manager when you call SetOutputFileName.</span></span> <span data-ttu-id="4d9f9-139">藉由呼叫 [**ICaptureGraphBuilder2：： GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) 方法取得其指標：</span><span class="sxs-lookup"><span data-stu-id="4d9f9-139">Get a pointer to it by calling the [**ICaptureGraphBuilder2::GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) method:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



<span data-ttu-id="4d9f9-140">現在呼叫 [**IGraphBuilder：： AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) 方法以新增非同步檔案來源篩選，並呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 方法以新增影片壓縮程式：</span><span class="sxs-lookup"><span data-stu-id="4d9f9-140">Now call the [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) method to add the Async File Source filter, and the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method to add the video compressor:</span></span>


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



<span data-ttu-id="4d9f9-141">此時，來源篩選和壓縮篩選不會連接到圖形中的任何其他內容，如下圖所示：</span><span class="sxs-lookup"><span data-stu-id="4d9f9-141">At this point, the source filter and the compression filter are not connected to anything else in the graph, as shown in the following illustration:</span></span>

![具有來源和壓縮篩選的篩選圖形](images/avi2avi2.png)

<span data-ttu-id="4d9f9-143">將來源連線至 Mux</span><span class="sxs-lookup"><span data-stu-id="4d9f9-143">Connect the Source to the Mux</span></span>

<span data-ttu-id="4d9f9-144">最後一個步驟是透過影片壓縮程式，將來源篩選器連線到 AVI Mux 篩選器。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-144">The final step is to connect the source filter to the AVI Mux filter, through the video compressor.</span></span> <span data-ttu-id="4d9f9-145">使用 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法，將來源篩選上的輸出連接連接到指定的接收篩選（選擇性地透過壓縮篩選）。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-145">Use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method, which connects an output pin on the source filter to a specified sink filter, optionally through a compression filter.</span></span>

<span data-ttu-id="4d9f9-146">前兩個參數指定釘選類別和媒體類型，以指定要連接的來源篩選器 pin。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-146">The first two parameters specify which of the source filter's pins to connect, by designating a pin category and a media type.</span></span> <span data-ttu-id="4d9f9-147">非同步檔案來源篩選只有一個輸出圖釘，因此這些參數應為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-147">The Async File Source filter has only one output pin, so these parameters should be **NULL**.</span></span> <span data-ttu-id="4d9f9-148">接下來的三個參數會指定來源篩選準則、壓縮篩選 (是否有任何) 和 Mux 篩選器。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-148">The next three parameters specify the source filter, the compression filter (if any), and the Mux filter.</span></span>

<span data-ttu-id="4d9f9-149">下列程式碼範例會透過影片壓縮程式呈現影片串流：</span><span class="sxs-lookup"><span data-stu-id="4d9f9-149">The following code example renders the video stream through the video compressor:</span></span>


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



<span data-ttu-id="4d9f9-150">下圖顯示到目前為止的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-150">The following diagram shows the filter graph so far.</span></span>

![轉譯的影片資料流程](images/avi2avi3.png)

<span data-ttu-id="4d9f9-152">假設原始程式檔有音訊串流， [AVI 分隔](avi-splitter-filter.md) 器篩選器已建立音訊的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-152">Assuming that the source file has an audio stream, the [AVI Splitter](avi-splitter-filter.md) filter has created an output pin for the audio.</span></span> <span data-ttu-id="4d9f9-153">若要連接此 pin，請再次呼叫 RenderStream：</span><span class="sxs-lookup"><span data-stu-id="4d9f9-153">To connect this pin, call RenderStream again:</span></span>


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



<span data-ttu-id="4d9f9-154">此處未指定壓縮篩選。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-154">Here, no compression filter is specified.</span></span> <span data-ttu-id="4d9f9-155">來源篩選的輸出釘選已連線，因此 RenderStream 方法會在分隔器篩選器上搜尋未連接的輸出 pin。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-155">The source filter's output pin is already connected, so the RenderStream method searches for an unconnected output pin on the splitter filter.</span></span> <span data-ttu-id="4d9f9-156">它會尋找音訊 pin 碼，並將它直接連接到 MUX 篩選器。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-156">It finds the audio pin and connects it directly to the MUX filter.</span></span> <span data-ttu-id="4d9f9-157">如果來源檔案沒有音訊串流，則第二次呼叫 RenderStream 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-157">If the source file does not have an audio stream, the second call to RenderStream will fail.</span></span> <span data-ttu-id="4d9f9-158">這是正常的現象。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-158">This is expected behavior.</span></span> <span data-ttu-id="4d9f9-159">圖形是在第一次呼叫 RenderStream 之後完成，因此第二次呼叫中的失敗是無害的。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-159">The graph is complete after the first call to RenderStream, so the failure in the second call is harmless.</span></span>

<span data-ttu-id="4d9f9-160">在此範例中，兩個 RenderStream 呼叫的順序很重要。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-160">In this example, the order of the two RenderStream calls is important.</span></span> <span data-ttu-id="4d9f9-161">因為第二個呼叫不會指定壓縮器，所以會從 AVI 分隔器連接任何未連接的 pin。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-161">Because the second call does not specify a compressor, it will connect any unconnected pin from the AVI Splitter.</span></span> <span data-ttu-id="4d9f9-162">如果您在另一個呼叫之前進行此呼叫，它可能會將影片資料流程連接到 AVI Mux，而不需要您的影片壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-162">If you make this call before the other one, it might connect the video stream to the AVI Mux, without your video compressor.</span></span> <span data-ttu-id="4d9f9-163">因此， (具有壓縮篩選) 的特定呼叫必須先發生。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-163">Therefore, the more specific call (with the compression filter) must happen first.</span></span>

<span data-ttu-id="4d9f9-164">先前的討論假設原始程式檔是 AVI 檔。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-164">The previous discussion has assumed that the source file is an AVI file.</span></span> <span data-ttu-id="4d9f9-165">不過，這項技術也適用于其他檔案類型，例如 MPEG 檔。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-165">However, this technique also works with other file types, such as MPEG files.</span></span> <span data-ttu-id="4d9f9-166">產生的篩選圖形會稍有不同。</span><span class="sxs-lookup"><span data-stu-id="4d9f9-166">The resulting filter graph will be somewhat different.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d9f9-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d9f9-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d9f9-168">Recompressing AVI 檔案</span><span class="sxs-lookup"><span data-stu-id="4d9f9-168">Recompressing an AVI File</span></span>](recompressing-an-avi-file.md)
</dt> </dl>

 

 



