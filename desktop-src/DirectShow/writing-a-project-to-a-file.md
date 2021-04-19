---
description: 將專案寫入檔案
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: 將專案寫入檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f63ddbc6a021362134d420220f7e25c662553f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980325"
---
# <a name="writing-a-project-to-a-file"></a><span data-ttu-id="a173c-103">將專案寫入檔案</span><span class="sxs-lookup"><span data-stu-id="a173c-103">Writing a Project to a File</span></span>

<span data-ttu-id="a173c-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a173c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a173c-105">本文說明如何將 [DirectShow 編輯服務](directshow-editing-services.md) 專案寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="a173c-105">This article describes how to write a [DirectShow Editing Services](directshow-editing-services.md) project to a file.</span></span> <span data-ttu-id="a173c-106">首先，它會說明如何使用基本轉譯引擎來寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="a173c-106">First it describes how to write a file with the basic render engine.</span></span> <span data-ttu-id="a173c-107">然後，它會使用智慧型轉譯引擎來描述智慧型 recompression。</span><span class="sxs-lookup"><span data-stu-id="a173c-107">Then it describes smart recompression with the smart render engine.</span></span>

<span data-ttu-id="a173c-108">如需有關「DirectShow 編輯服務」如何轉譯專案的總覽，請參閱 [關於呈現引擎](about-the-render-engines.md)。</span><span class="sxs-lookup"><span data-stu-id="a173c-108">For an overview of how DirectShow Editing Services renders projects, see [About the Render Engines](about-the-render-engines.md).</span></span>

<span data-ttu-id="a173c-109">**使用基本轉譯引擎**</span><span class="sxs-lookup"><span data-stu-id="a173c-109">**Using the Basic Render Engine**</span></span>

<span data-ttu-id="a173c-110">首先，建立圖形的前端，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a173c-110">Start by building the front end of the graph, as follows:</span></span>

1.  <span data-ttu-id="a173c-111">建立轉譯引擎。</span><span class="sxs-lookup"><span data-stu-id="a173c-111">Create the render engine.</span></span>
2.  <span data-ttu-id="a173c-112">指定時間軸。</span><span class="sxs-lookup"><span data-stu-id="a173c-112">Specify the timeline.</span></span>
3.  <span data-ttu-id="a173c-113">設定呈現範圍。</span><span class="sxs-lookup"><span data-stu-id="a173c-113">Set the render range.</span></span> <span data-ttu-id="a173c-114">(選用)</span><span class="sxs-lookup"><span data-stu-id="a173c-114">(Optional)</span></span>
4.  <span data-ttu-id="a173c-115">建立圖形的前端。</span><span class="sxs-lookup"><span data-stu-id="a173c-115">Build the front end of the graph.</span></span>

<span data-ttu-id="a173c-116">下列程式碼範例顯示這些步驟。</span><span class="sxs-lookup"><span data-stu-id="a173c-116">The following code example shows these steps.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



<span data-ttu-id="a173c-117">接下來，將多工器和檔案寫入篩選器新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="a173c-117">Next, add multiplexer and file-writing filters to the filter graph.</span></span> <span data-ttu-id="a173c-118">若要這麼做，最簡單的方式就是使用「 [捕獲圖形](capture-graph-builder.md)產生器」，這是用來建立捕獲圖形的 DirectShow 元件。</span><span class="sxs-lookup"><span data-stu-id="a173c-118">The easiest way to do this is with the [Capture Graph Builder](capture-graph-builder.md), a DirectShow component for building capture graphs.</span></span> <span data-ttu-id="a173c-119">[Capture graph builder] 會公開 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面。</span><span class="sxs-lookup"><span data-stu-id="a173c-119">The capture graph builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="a173c-120">執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="a173c-120">Perform the following steps:</span></span>

1.  <span data-ttu-id="a173c-121">建立「capture graph 建立器」的實例。</span><span class="sxs-lookup"><span data-stu-id="a173c-121">Create an instance of the capture graph builder.</span></span>
2.  <span data-ttu-id="a173c-122">取得圖形的指標，並將其傳遞至 graph builder。</span><span class="sxs-lookup"><span data-stu-id="a173c-122">Obtain a pointer to the graph and pass it to the graph builder.</span></span>
3.  <span data-ttu-id="a173c-123">指定輸出檔案的名稱和媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a173c-123">Specify the name and media type of the output file.</span></span> <span data-ttu-id="a173c-124">此步驟也會取得 mux 篩選的指標，稍後需要此篩選器。</span><span class="sxs-lookup"><span data-stu-id="a173c-124">This step also obtains a pointer to the mux filter, which is required later.</span></span>

<span data-ttu-id="a173c-125">下列程式碼範例顯示這些步驟。</span><span class="sxs-lookup"><span data-stu-id="a173c-125">The following code example shows these steps.</span></span>


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



<span data-ttu-id="a173c-126">最後，將前端的輸出圖釘連接至 mux 篩選器。</span><span class="sxs-lookup"><span data-stu-id="a173c-126">Finally, connect the output pins on the front end to the mux filter.</span></span>

1.  <span data-ttu-id="a173c-127">取出群組的數目。</span><span class="sxs-lookup"><span data-stu-id="a173c-127">Retrieve the number of groups.</span></span>
2.  <span data-ttu-id="a173c-128">針對每個 pin，取得釘選的指標。</span><span class="sxs-lookup"><span data-stu-id="a173c-128">For each pin, obtain a pointer to the pin.</span></span>
3.  <span data-ttu-id="a173c-129">（選擇性）建立壓縮篩選準則的實例，以壓縮資料流程。</span><span class="sxs-lookup"><span data-stu-id="a173c-129">Optionally, create an instance of a compression filter to compress the stream.</span></span> <span data-ttu-id="a173c-130">[壓縮程式] 的類型會視群組的媒體類型而定。</span><span class="sxs-lookup"><span data-stu-id="a173c-130">The type of compressor will depend on the media type of the group.</span></span> <span data-ttu-id="a173c-131">您可以使用 [系統裝置](system-device-enumerator.md) 列舉值來列舉可用的壓縮篩選。</span><span class="sxs-lookup"><span data-stu-id="a173c-131">You can use the [System Device Enumerator](system-device-enumerator.md) to enumerate the available compression filters.</span></span> <span data-ttu-id="a173c-132">如需詳細資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="a173c-132">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>
4.  <span data-ttu-id="a173c-133">（選擇性）設定壓縮參數，例如金鑰畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="a173c-133">Optionally, set compression parameters such as the key-frame rate.</span></span> <span data-ttu-id="a173c-134">本文稍後會詳細討論此步驟。</span><span class="sxs-lookup"><span data-stu-id="a173c-134">This step is discussed in detail later in the article.</span></span>
5.  <span data-ttu-id="a173c-135">呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)。</span><span class="sxs-lookup"><span data-stu-id="a173c-135">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="a173c-136">這個方法會取得釘選的指標，壓縮篩選器 (是否有任何) 和多工器。</span><span class="sxs-lookup"><span data-stu-id="a173c-136">This method takes pointers to the pin, the compression filter (if any), and the multiplexer.</span></span>

<span data-ttu-id="a173c-137">下列程式碼範例示範如何連接輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="a173c-137">The following code example shows how to connect the output pins.</span></span>


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



<span data-ttu-id="a173c-138">若要設定壓縮參數 (步驟4（先前) ），請使用 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) 介面。</span><span class="sxs-lookup"><span data-stu-id="a173c-138">To set compression parameters (step 4, previously), use the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface.</span></span> <span data-ttu-id="a173c-139">此介面會公開于壓縮篩選的輸出圖釘上。</span><span class="sxs-lookup"><span data-stu-id="a173c-139">This interface is exposed on the output pins of compression filters.</span></span> <span data-ttu-id="a173c-140">列舉壓縮篩選器的釘選，然後查詢每個輸出的 pin 以進行 **IAMVideoCompression**。</span><span class="sxs-lookup"><span data-stu-id="a173c-140">Enumerate the compression filter's pins, and query each output pin for **IAMVideoCompression**.</span></span> <span data-ttu-id="a173c-141"> (如需列舉釘選的詳細資訊，請參閱 [列舉釘](enumerating-pins.md)選。 ) 務必釋出您在此步驟中取得的所有介面指標。</span><span class="sxs-lookup"><span data-stu-id="a173c-141">(For information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).) Be sure to release all the interface pointers that you obtained during this step.</span></span>

<span data-ttu-id="a173c-142">在您建立篩選圖形之後，請在篩選圖形管理員上呼叫 [**IMediaControl：： Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 方法。</span><span class="sxs-lookup"><span data-stu-id="a173c-142">After you build the filter graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method on the filter graph manager.</span></span> <span data-ttu-id="a173c-143">當篩選圖形執行時，它會將資料寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="a173c-143">As the filter graph runs, it writes the data to a file.</span></span> <span data-ttu-id="a173c-144">使用事件通知來等候播放完成。</span><span class="sxs-lookup"><span data-stu-id="a173c-144">Use event notification to wait for playback to complete.</span></span> <span data-ttu-id="a173c-145"> (查看 [回應事件](responding-to-events.md)) 。播放完成時，您必須明確呼叫 [**IMediaControl：： stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) 以停止篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="a173c-145">(See [Responding to Events](responding-to-events.md).) When playback finishes, you must explicitly call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) to stop the filter graph.</span></span> <span data-ttu-id="a173c-146">否則，就不會正確寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="a173c-146">Otherwise, the file is not written correctly.</span></span>

<span data-ttu-id="a173c-147">**使用智慧型轉譯引擎**</span><span class="sxs-lookup"><span data-stu-id="a173c-147">**Using the Smart Render Engine**</span></span>

<span data-ttu-id="a173c-148">若要取得智慧 recompression 的優點，請使用智慧型轉譯引擎取代基本轉譯引擎。</span><span class="sxs-lookup"><span data-stu-id="a173c-148">To get the benefits of smart recompression, use the smart render engine in place of the basic render engine.</span></span> <span data-ttu-id="a173c-149">建立圖形的步驟幾乎相同。</span><span class="sxs-lookup"><span data-stu-id="a173c-149">The steps in building the graph are almost the same.</span></span> <span data-ttu-id="a173c-150">主要差異在於，壓縮是在圖形的前端處理，而不是在檔案寫入區段中處理。</span><span class="sxs-lookup"><span data-stu-id="a173c-150">The major difference is that compression is handled in the front end of the graph, not in the file-writing section.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a173c-151">請勿使用智慧型轉譯引擎來讀取或寫入 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="a173c-151">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

<span data-ttu-id="a173c-152">每個影片群組都有一個屬性，可指定該群組的壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="a173c-152">Each video group has a property that specifies the compression format for that group.</span></span> <span data-ttu-id="a173c-153">壓縮格式必須完全符合群組的高度、寬度、位深度和畫面播放速率的未壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="a173c-153">The compression format must exactly match the group's uncompressed format in height, width, bit depth, and frame rate.</span></span> <span data-ttu-id="a173c-154">智慧型轉譯引擎會使用壓縮格式來建立圖形。</span><span class="sxs-lookup"><span data-stu-id="a173c-154">The smart render engine uses the compression format when it constructs the graph.</span></span> <span data-ttu-id="a173c-155">設定壓縮格式之前，請務必藉由呼叫 [**IAMTimelineGroup：： SetMediaType**](iamtimelinegroup-setmediatype.md)，為該群組設定未壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="a173c-155">Before you set the compression format, make sure to set the uncompressed format for that group by calling [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md).</span></span>

<span data-ttu-id="a173c-156">若要設定群組的壓縮格式，請呼叫 [**IAMTimelineGroup：： SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a173c-156">To set a group's compression format, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span> <span data-ttu-id="a173c-157">這個方法會採用 [**SCompFmt0**](scompfmt0.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a173c-157">This method takes a pointer to an [**SCompFmt0**](scompfmt0.md) structure.</span></span> <span data-ttu-id="a173c-158">**SCompFmt0** 結構有兩個成員： **nFormatId**，其必須為零 **，而**[**媒體類型為 AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構。</span><span class="sxs-lookup"><span data-stu-id="a173c-158">The **SCompFmt0** structure has two members: **nFormatId**, which must be zero, and **MediaType**, which is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="a173c-159">使用格式資訊來初始化 **AM \_ 媒體 \_ 類型** 結構。</span><span class="sxs-lookup"><span data-stu-id="a173c-159">Initialize the **AM\_MEDIA\_TYPE** structure with the format information.</span></span>

> [!Note]  
> <span data-ttu-id="a173c-160">如果您想要讓最終專案具有與其中一個原始程式檔相同的格式，您可以 \_ 使用媒體偵測器 \_ ，直接從原始程式檔取得 AM 媒體類型結構。</span><span class="sxs-lookup"><span data-stu-id="a173c-160">If you want the final project to have the same format as one of your source files, you can get the AM\_MEDIA\_TYPE structure directly from the source file, using the media detector.</span></span> <span data-ttu-id="a173c-161">請參閱 [**IMediaDet：： get \_ StreamMediaType**](imediadet-get-streammediatype.md)。</span><span class="sxs-lookup"><span data-stu-id="a173c-161">See [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md).</span></span>

 

<span data-ttu-id="a173c-162">將 [**SCompFmt0**](scompfmt0.md) 變數轉換為 **long** 類型的指標，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="a173c-162">Cast the [**SCompFmt0**](scompfmt0.md) variable to a pointer of type **long**, as shown in the following example.</span></span>


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



<span data-ttu-id="a173c-163">智慧型轉譯引擎會自動搜尋相容的壓縮篩選。</span><span class="sxs-lookup"><span data-stu-id="a173c-163">The smart render engine automatically searches for a compatible compression filter.</span></span> <span data-ttu-id="a173c-164">您也可以藉由呼叫 [**ISmartRenderEngine：： SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md)來指定群組的壓縮篩選。</span><span class="sxs-lookup"><span data-stu-id="a173c-164">You can also specify a compression filter for a group by calling [**ISmartRenderEngine::SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).</span></span>

<span data-ttu-id="a173c-165">若要建立圖形，請使用上一節中針對基本轉譯引擎所述的相同步驟。</span><span class="sxs-lookup"><span data-stu-id="a173c-165">To build the graph, use the same steps that were described for the Basic Render Engine in the previous section.</span></span> <span data-ttu-id="a173c-166">唯一的差異如下：</span><span class="sxs-lookup"><span data-stu-id="a173c-166">The only differences are the following:</span></span>

-   <span data-ttu-id="a173c-167">使用智慧型轉譯引擎，而不是基本轉譯引擎。</span><span class="sxs-lookup"><span data-stu-id="a173c-167">Use the smart render engine, not the basic render engine.</span></span> <span data-ttu-id="a173c-168">類別識別碼是 CLSID \_ SmartRenderEngine。</span><span class="sxs-lookup"><span data-stu-id="a173c-168">The class identifier is CLSID\_SmartRenderEngine.</span></span>
-   <span data-ttu-id="a173c-169">在您建立前端之後，但在呈現輸出圖釘之前，請設定壓縮參數。</span><span class="sxs-lookup"><span data-stu-id="a173c-169">Set compression parameters after you build the front end but before you render the output pins.</span></span> <span data-ttu-id="a173c-170">呼叫 [**ISmartRenderEngine：： GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) 方法，以取得群組壓縮篩選的指標。</span><span class="sxs-lookup"><span data-stu-id="a173c-170">Call the [**ISmartRenderEngine::GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) method to obtain a pointer to a group's compression filter.</span></span> <span data-ttu-id="a173c-171">然後查詢 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) 介面，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="a173c-171">Then query for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, as described previously.</span></span>
-   <span data-ttu-id="a173c-172">當您呈現輸出圖釘時，不需要插入壓縮篩選。</span><span class="sxs-lookup"><span data-stu-id="a173c-172">When you render the output pins, there is no need to insert a compression filter.</span></span> <span data-ttu-id="a173c-173">資料流程已壓縮。</span><span class="sxs-lookup"><span data-stu-id="a173c-173">The stream is already compressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a173c-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="a173c-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a173c-175">轉譯專案</span><span class="sxs-lookup"><span data-stu-id="a173c-175">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



