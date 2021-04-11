---
description: 使用 Capture Graph Builder 建立圖形
ms.assetid: 0329c4f0-ee6f-423e-b38b-169204e3a31c
title: 使用 Capture Graph Builder 建立圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e48347a73cdac545723ac226cc58a0175dec5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846728"
---
# <a name="building-graphs-with-the-capture-graph-builder"></a><span data-ttu-id="8b279-103">使用 Capture Graph Builder 建立圖形</span><span class="sxs-lookup"><span data-stu-id="8b279-103">Building Graphs with the Capture Graph Builder</span></span>

<span data-ttu-id="8b279-104">不論其名稱，Capture Graph Builder 都可用於建立許多種類的自訂篩選圖形，而不只是捕捉圖形。</span><span class="sxs-lookup"><span data-stu-id="8b279-104">Despite its name, the Capture Graph Builder is useful for building many kinds of custom filter graphs, not only capture graphs.</span></span> <span data-ttu-id="8b279-105">本文提供如何使用此物件的簡短總覽。</span><span class="sxs-lookup"><span data-stu-id="8b279-105">This article provides a brief overview of how to use this object.</span></span>

<span data-ttu-id="8b279-106">[Capture Graph Builder] 會公開 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面。</span><span class="sxs-lookup"><span data-stu-id="8b279-106">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="8b279-107">首先，呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 以建立「捕獲圖形產生器」和「篩選圖形管理員」。</span><span class="sxs-lookup"><span data-stu-id="8b279-107">Start by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="8b279-108">然後藉由呼叫 [**ICaptureGraphBuilder2：： SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) 與篩選圖形管理員的指標，初始化 Capture Graph Builder，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8b279-108">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager, as follows:</span></span>


```C++
IGraphBuilder *pGraph = NULL;
ICaptureGraphBuilder2 *pBuilder = NULL;

// Create the Filter Graph Manager.
HRESULT hr =  CoCreateInstance(CLSID_FilterGraph, NULL,
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);

if (SUCCEEDED(hr))
{
    // Create the Capture Graph Builder.
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL,
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, 
        (void **)&pBuilder);
    if (SUCCEEDED(hr))
    {
        pBuilder->SetFiltergraph(pGraph);
    }
};
```



## <a name="connecting-filters"></a><span data-ttu-id="8b279-109">連接篩選</span><span class="sxs-lookup"><span data-stu-id="8b279-109">Connecting Filters</span></span>

<span data-ttu-id="8b279-110">[**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)方法會將兩個或三個篩選器一起連接在一個鏈中。</span><span class="sxs-lookup"><span data-stu-id="8b279-110">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method connects two or three filters together in a chain.</span></span> <span data-ttu-id="8b279-111">一般來說，當每個篩選準則的輸入 pin 或輸出 pin 類型相同時，方法的效果最好。</span><span class="sxs-lookup"><span data-stu-id="8b279-111">Generally, the method works best when each filter has no more than one input pin or output pin of the same type.</span></span> <span data-ttu-id="8b279-112">這項討論一開始會忽略 **RenderStream** 的前兩個參數，並將焦點放在最後三個參數。</span><span class="sxs-lookup"><span data-stu-id="8b279-112">This discussion begins by ignoring the first two parameters of **RenderStream** and focusing on the last three parameters.</span></span> <span data-ttu-id="8b279-113">第三個參數是 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) 指標，可將篩選 (指定為 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面指標) 或輸出釘選 (做為 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標) 。</span><span class="sxs-lookup"><span data-stu-id="8b279-113">The third parameter is an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer, which can specify either a filter (as an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface pointer) or an output pin (as an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface pointer).</span></span> <span data-ttu-id="8b279-114">第四個和第五個參數指定 **IBaseFilter** 指標。</span><span class="sxs-lookup"><span data-stu-id="8b279-114">The fourth and fifth parameters specify **IBaseFilter** pointers.</span></span> <span data-ttu-id="8b279-115">**RenderStream** 方法會連接鏈中的所有三個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="8b279-115">The **RenderStream** method connects all three filters in a chain.</span></span> <span data-ttu-id="8b279-116">例如，假設 *A*、 *B* 和 *C* 是篩選準則。</span><span class="sxs-lookup"><span data-stu-id="8b279-116">For example, suppose that *A*, *B*, and *C* are filters.</span></span> <span data-ttu-id="8b279-117">假設現在每個篩選都只有一個輸入 pin 和一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="8b279-117">Assume for now that each filter has exactly one input pin and one output pin.</span></span> <span data-ttu-id="8b279-118">下列呼叫會將 A 連接到 B，然後從 B 到 C：</span><span class="sxs-lookup"><span data-stu-id="8b279-118">The following call connects A to B, and then B to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
</dl>

<span data-ttu-id="8b279-119">所有連線都是「智慧型」的，也就是說，其他篩選器會視需要新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="8b279-119">All connections are "intelligent," meaning that additional filters are added to the graph as needed.</span></span> <span data-ttu-id="8b279-120">如需詳細資訊，請參閱 [智慧型 Connect](intelligent-connect.md)。</span><span class="sxs-lookup"><span data-stu-id="8b279-120">For details, see [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="8b279-121">若只連接兩個篩選器，請將中間值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8b279-121">To connect just two filters, set the middle value to **NULL**.</span></span> <span data-ttu-id="8b279-122">例如，這個呼叫會將 A 連接到 C：</span><span class="sxs-lookup"><span data-stu-id="8b279-122">For example, this call connects A to C:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, C)`  
</dl>

<span data-ttu-id="8b279-123">您可以呼叫方法兩次，以建立較長的鏈：</span><span class="sxs-lookup"><span data-stu-id="8b279-123">You can create longer chains by calling the method twice:</span></span>

<dl> `RenderStream(NULL, NULL, A, B, C)`  
`RenderStream(NULL, NULL, C, D, E)`  
</dl>

<span data-ttu-id="8b279-124">如果最後一個參數為 **Null**，則方法會自動尋找預設轉譯器。</span><span class="sxs-lookup"><span data-stu-id="8b279-124">If the last parameter is **NULL**, the method automatically locates a default renderer.</span></span> <span data-ttu-id="8b279-125">它會使用影片的 [影片](video-renderer-filter.md) 轉譯器，以及適用于音訊的 [DirectSound](directsound-renderer-filter.md) 轉譯器。</span><span class="sxs-lookup"><span data-stu-id="8b279-125">It uses the [Video Renderer](video-renderer-filter.md) for video and the [DirectSound Renderer](directsound-renderer-filter.md) for audio.</span></span> <span data-ttu-id="8b279-126">因此：</span><span class="sxs-lookup"><span data-stu-id="8b279-126">Thus:</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, NULL)`  
</dl>

<span data-ttu-id="8b279-127">相當於</span><span class="sxs-lookup"><span data-stu-id="8b279-127">is equivalent to</span></span>

<dl> `RenderStream(NULL, NULL, A, NULL, R)`  
</dl>

<span data-ttu-id="8b279-128">其中 *R* 是適當的轉譯器。</span><span class="sxs-lookup"><span data-stu-id="8b279-128">where *R* is the appropriate renderer.</span></span> <span data-ttu-id="8b279-129">不過，若要連接視頻混合轉譯器篩選器，而不是影片轉譯器，您必須明確指定。</span><span class="sxs-lookup"><span data-stu-id="8b279-129">To connect the Video Mixing Renderer filter instead of the Video Renderer, however, you must specify it explicitly.</span></span>

<span data-ttu-id="8b279-130">如果您在第三個參數中指定篩選，而不是使用 pin 碼，您可能需要指定連接所應使用的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="8b279-130">If you specify a filter in the third parameter, rather than a pin, you may need to indicate which output pin should be used for the connection.</span></span> <span data-ttu-id="8b279-131">這是方法前兩個參數的用途。</span><span class="sxs-lookup"><span data-stu-id="8b279-131">That is the purpose of the method's first two parameters.</span></span> <span data-ttu-id="8b279-132">第一個參數只適用于 capture 篩選。</span><span class="sxs-lookup"><span data-stu-id="8b279-132">The first parameter applies only to capture filters.</span></span> <span data-ttu-id="8b279-133">它會指定指出釘選類別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8b279-133">It specifies a GUID that indicates a pin category.</span></span> <span data-ttu-id="8b279-134">如需完整的類別清單，請參閱 [釘選屬性集](pin-property-set.md)。</span><span class="sxs-lookup"><span data-stu-id="8b279-134">For a complete list of categories, see [Pin Property Set](pin-property-set.md).</span></span> <span data-ttu-id="8b279-135">以下兩個類別對所有的捕獲篩選都有效：</span><span class="sxs-lookup"><span data-stu-id="8b279-135">Two of the categories are valid for all capture filters:</span></span>

-   <span data-ttu-id="8b279-136">**釘選 \_ 類別 \_ 捕獲**</span><span class="sxs-lookup"><span data-stu-id="8b279-136">**PIN\_CATEGORY\_CAPTURE**</span></span>
-   <span data-ttu-id="8b279-137">**釘選 \_ 類別 \_ 預覽**</span><span class="sxs-lookup"><span data-stu-id="8b279-137">**PIN\_CATEGORY\_PREVIEW**</span></span>

<span data-ttu-id="8b279-138">如果捕捉篩選未提供個別的 pin 供捕捉和預覽，則 [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法會插入 [智慧型的 t](smart-tee-filter.md) a 濾波器，將資料流程分割成捕獲資料流程和預覽資料流程。</span><span class="sxs-lookup"><span data-stu-id="8b279-138">If a capture filter does not supply separate pins for capture and preview, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method inserts a [Smart Tee](smart-tee-filter.md) filter, which splits the stream into a capture stream and a preview stream.</span></span> <span data-ttu-id="8b279-139">從應用程式的觀點來看，您可以直接將所有的捕獲篩選器視為具有個別的 pin，並忽略圖形的基礎拓撲。</span><span class="sxs-lookup"><span data-stu-id="8b279-139">From the application's standpoint, you can simply treat all capture filters as having separate pins and ignore the underlying topology of the graph.</span></span>

<span data-ttu-id="8b279-140">針對 [檔案捕獲]，將捕捉 pin 連接至 mux 篩選器。</span><span class="sxs-lookup"><span data-stu-id="8b279-140">For file capture, connect the capture pin to a mux filter.</span></span> <span data-ttu-id="8b279-141">若為即時預覽，請將預覽釘選到轉譯器。</span><span class="sxs-lookup"><span data-stu-id="8b279-141">For live preview, connect the preview pin to a renderer.</span></span> <span data-ttu-id="8b279-142">如果您切換兩個類別，則圖形可能會在檔案捕獲期間卸載過多的畫面格數目;但是，如果圖表已正確連接，它會視需要卸載預覽畫面格，以維持捕獲資料流程的輸送量。</span><span class="sxs-lookup"><span data-stu-id="8b279-142">If you switch the two categories, the graph might drop an excessive number of frames during the file capture; but if the graph is connected properly, it drops preview frames as needed in order to maintain throughput on the capture stream.</span></span>

<span data-ttu-id="8b279-143">下列範例顯示如何連接兩個數據流：</span><span class="sxs-lookup"><span data-stu-id="8b279-143">The following example shows how to connect both streams:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, NULL, pCapFilter, NULL, pMux);
// Preview:
pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="8b279-144">某些 capture 濾波器也支援隱藏式輔助字幕，以 **釘選 \_ 類別 \_ VBI** 表示。</span><span class="sxs-lookup"><span data-stu-id="8b279-144">Some capture filters also support closed captions, indicated by **PIN\_CATEGORY\_VBI**.</span></span> <span data-ttu-id="8b279-145">若要將隱藏式輔助字幕捕捉至檔案，請將此類別轉譯為 mux 篩選器。</span><span class="sxs-lookup"><span data-stu-id="8b279-145">To capture the closed captions to a file, render this category to the mux filter.</span></span> <span data-ttu-id="8b279-146">若要在預覽視窗中查看隱藏式輔助字幕，請連接到轉譯器：</span><span class="sxs-lookup"><span data-stu-id="8b279-146">To view the closed captions in your preview window, connect to the renderer:</span></span>


```C++
// Capture to file:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, pMux);
// Preview on screen:
pBuilder->RenderStream(&PIN_CATEGORY_VBI, NULL, pCapFilter, NULL, NULL);
```



<span data-ttu-id="8b279-147">[**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)的第二個參數會識別媒體類型，而且通常是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="8b279-147">The second parameter to [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) identifies the media type, and is typically one of the following:</span></span>

-   <span data-ttu-id="8b279-148">媒體 \_ 媒體</span><span class="sxs-lookup"><span data-stu-id="8b279-148">MEDIATYPE\_Audio</span></span>
-   <span data-ttu-id="8b279-149">媒體 \_ 媒體</span><span class="sxs-lookup"><span data-stu-id="8b279-149">MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="8b279-150">以 \_) 交錯 (DV 的媒體</span><span class="sxs-lookup"><span data-stu-id="8b279-150">MEDIATYPE\_Interleaved (DV)</span></span>

<span data-ttu-id="8b279-151">只要篩選的輸出圖釘支援慣用媒體類型的列舉，您就可以使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="8b279-151">You can use this parameter whenever the filter's output pins support the enumeration of preferred media types.</span></span> <span data-ttu-id="8b279-152">針對檔案來源，[Capture Graph Builder] 會視需要自動新增剖析器篩選，然後查詢剖析器上的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="8b279-152">For file sources, the Capture Graph Builder automatically adds a parser filter if needed, and then queries the media types on the parser.</span></span> <span data-ttu-id="8b279-153"> (如需範例，請參閱 [RECOMPRESSING AVI](recompressing-an-avi-file.md)檔。 ) 此外，如果鏈中的最後一個篩選器有數個輸入圖釘，方法會嘗試列舉其媒體類型。</span><span class="sxs-lookup"><span data-stu-id="8b279-153">(For an example, see [Recompressing an AVI File](recompressing-an-avi-file.md).) Also, if the last filter in the chain has several input pins, the method attempts to enumerate their media types.</span></span> <span data-ttu-id="8b279-154">不過，並非所有篩選都支援此功能。</span><span class="sxs-lookup"><span data-stu-id="8b279-154">However, not all filters support this functionality.</span></span>

## <a name="finding-interfaces-on-filters-and-pins"></a><span data-ttu-id="8b279-155">尋找篩選和釘選介面</span><span class="sxs-lookup"><span data-stu-id="8b279-155">Finding Interfaces on Filters and Pins</span></span>

<span data-ttu-id="8b279-156">建立圖形之後，您通常需要找出圖形中的篩選和釘選所公開的各種介面。</span><span class="sxs-lookup"><span data-stu-id="8b279-156">After you build a graph, you will typically need to locate various interfaces exposed by filters and pins in the graph.</span></span> <span data-ttu-id="8b279-157">例如，「捕捉」篩選器可能會公開 [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) 介面，而篩選的輸出圖釘可能會公開 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 介面。</span><span class="sxs-lookup"><span data-stu-id="8b279-157">For example, a capture filter might expose the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface, while the filter's output pins might expose the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface.</span></span>

<span data-ttu-id="8b279-158">尋找介面最簡單的方式是使用 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 方法。</span><span class="sxs-lookup"><span data-stu-id="8b279-158">The simplest way to find an interface is to use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method.</span></span> <span data-ttu-id="8b279-159">這個方法會將圖形 (篩選和釘選) ，直到它找到所需的介面為止。</span><span class="sxs-lookup"><span data-stu-id="8b279-159">This method walks the graph (filters and pins) until it locates the desired interface.</span></span> <span data-ttu-id="8b279-160">您可以指定搜尋的起點，也可以限制搜尋從起始點篩選上游或下游。</span><span class="sxs-lookup"><span data-stu-id="8b279-160">You can specify the starting point for the search, and you can limit the search to filters upstream or downstream from the starting point.</span></span>

<span data-ttu-id="8b279-161">下列範例會在影片預覽釘選上搜尋 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 介面：</span><span class="sxs-lookup"><span data-stu-id="8b279-161">The following example searches for the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on a video preview pin:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
HRESULT hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, 
    &MEDIATYPE_Video,
    pVCap, 
    IID_IAMStreamConfig, 
    (void**)&pConfig
);
if (SUCCESSFUL(hr))
{
    /* ... */
    pConfig->Release();
}
```



> [!Note]  
> <span data-ttu-id="8b279-162">主題 [尋找篩選或釘選上的介面](find-an-interface-on-a-filter-or-pin.md) 時，會顯示使用 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 介面而非 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)的替代方法。</span><span class="sxs-lookup"><span data-stu-id="8b279-162">The topic [Find an Interface on a Filter or Pin](find-an-interface-on-a-filter-or-pin.md) shows an alternative approach that uses the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface instead of [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2).</span></span> <span data-ttu-id="8b279-163">使用哪一種方法取決於您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8b279-163">Which approach to use depends on your application.</span></span> <span data-ttu-id="8b279-164">如果您的應用程式已經使用 **ICaptureGraphBuilder2** 來建立圖形，則 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 是不錯的方法。</span><span class="sxs-lookup"><span data-stu-id="8b279-164">If your application already uses **ICaptureGraphBuilder2** to build the graph, then [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) is a good approach.</span></span> <span data-ttu-id="8b279-165">否則，請考慮使用 **IGraphBuilder** 方法。</span><span class="sxs-lookup"><span data-stu-id="8b279-165">Otherwise, consider using the **IGraphBuilder** methods.</span></span>

 

## <a name="finding-pins"></a><span data-ttu-id="8b279-166">尋找釘選</span><span class="sxs-lookup"><span data-stu-id="8b279-166">Finding Pins</span></span>

<span data-ttu-id="8b279-167">一般來說，您可能需要在篩選器上找出個別的 pin，不過在大部分情況下， [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 和 [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 方法會為您節省問題。</span><span class="sxs-lookup"><span data-stu-id="8b279-167">Less commonly, you may need to locate an individual pin on a filter, although in most cases the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) and [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) methods will save you the trouble.</span></span> <span data-ttu-id="8b279-168">如果您需要在篩選準則中尋找特定的 pin， [**ICaptureGraphBuilder2：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) helper 方法會很有用。</span><span class="sxs-lookup"><span data-stu-id="8b279-168">If you do need to find a particular pin on a filter, the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) helper method is useful.</span></span> <span data-ttu-id="8b279-169">指定類別、媒體類型 (影片或音訊) 、方向，以及 pin 是否必須連接。</span><span class="sxs-lookup"><span data-stu-id="8b279-169">Specify the category, the media type (video or audio), the direction, and whether the pin must be unconnected.</span></span>

<span data-ttu-id="8b279-170">例如，下列程式碼會在捕獲篩選器上搜尋未連接的影片預覽 pin：</span><span class="sxs-lookup"><span data-stu-id="8b279-170">For example, the following code searches for an unconnected video preview pin on a capture filter:</span></span>


```C++
IPin *pPin = NULL;
hr = pBuild->FindPin(
    pCap,                   // Pointer to the filter to search.
    PINDIR_OUTPUT,          // Search for an output pin.
    &PIN_CATEGORY_PREVIEW,  // Search for a preview pin.
    &MEDIATYPE_Video,       // Search for a video pin.
    TRUE,                   // The pin must be unconnected. 
    0,                      // Return the first matching pin (index 0).
    &pPin);                 // This variable receives the IPin pointer.
if (SUCCESSFUL(hr))
{
    /* ... */
    pPin->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="8b279-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b279-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b279-172">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="8b279-172">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
