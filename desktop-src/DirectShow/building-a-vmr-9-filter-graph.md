---
description: 建立 VMR 9 篩選圖形
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: 建立 VMR 9 篩選圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846567"
---
# <a name="building-a-vmr-9-filter-graph"></a><span data-ttu-id="b94e4-103">建立 VMR 9 篩選圖形</span><span class="sxs-lookup"><span data-stu-id="b94e4-103">Building a VMR-9 Filter Graph</span></span>

<span data-ttu-id="b94e4-104">由於影片混合轉譯器9篩選 (VMR-9) 不是預設的影片轉譯器，因此使用 VMR-9 的應用程式必須明確地將它新增至圖形並進行連接。</span><span class="sxs-lookup"><span data-stu-id="b94e4-104">Because the Video Mixing Renderer 9 Filter (VMR-9) is not the default video renderer, an application that uses the VMR-9 must explicitly add it to the graph and connect it.</span></span> <span data-ttu-id="b94e4-105">本節提供兩種不同的方法，可使用 VMR-9 建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="b94e4-105">This section presents two different approaches to building filter graphs with the VMR-9.</span></span>

<span data-ttu-id="b94e4-106">使用 Capture Graph Builder</span><span class="sxs-lookup"><span data-stu-id="b94e4-106">Using the Capture Graph Builder</span></span>

<span data-ttu-id="b94e4-107">「捕獲圖形產生器」是用來建立自訂篩選圖形的協助程式物件。</span><span class="sxs-lookup"><span data-stu-id="b94e4-107">The Capture Graph Builder is a helper object for building custom filter graphs.</span></span> <span data-ttu-id="b94e4-108">您可以使用它來建立 VMR 9 圖形，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b94e4-108">You can use it to build VMR-9 graphs as follows:</span></span>

1.  <span data-ttu-id="b94e4-109">建立並初始化「Capture Graph 建立器」，如「 [捕獲圖形](about-the-capture-graph-builder.md)產生器」主題所述。</span><span class="sxs-lookup"><span data-stu-id="b94e4-109">Create and initialize the Capture Graph Builder, as described in the topic [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
2.  <span data-ttu-id="b94e4-110">呼叫 CoCreateInstance 以建立 VMR-9：</span><span class="sxs-lookup"><span data-stu-id="b94e4-110">Call CoCreateInstance to create the VMR-9:</span></span>
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  <span data-ttu-id="b94e4-111">在篩選圖形管理員上呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) ，將 VMR-9 新增至篩選圖形：</span><span class="sxs-lookup"><span data-stu-id="b94e4-111">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) on the Filter Graph Manager to add the VMR-9 to the filter graph:</span></span>
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  <span data-ttu-id="b94e4-112">呼叫 [**IGraphBuilder：： AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) 以新增影片檔案的來源篩選：</span><span class="sxs-lookup"><span data-stu-id="b94e4-112">Call [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add a source filter for the video file:</span></span>
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  <span data-ttu-id="b94e4-113">呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法，以將影片資料流程轉譯為 VMR：</span><span class="sxs-lookup"><span data-stu-id="b94e4-113">Call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to render the video stream to the VMR:</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  <span data-ttu-id="b94e4-114">（選擇性）再次呼叫 RenderStream，以轉譯音訊串流：</span><span class="sxs-lookup"><span data-stu-id="b94e4-114">Optionally, call RenderStream again to render the audio stream:</span></span>
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

<span data-ttu-id="b94e4-115">您可以針對每個原始程式檔呼叫 AddSourceFilter 和 RenderStream，以混合數個影片串流。</span><span class="sxs-lookup"><span data-stu-id="b94e4-115">You can mix several video streams by calling AddSourceFilter and RenderStream for each source file.</span></span>

<span data-ttu-id="b94e4-116">使用篩選圖形管理員</span><span class="sxs-lookup"><span data-stu-id="b94e4-116">Using the Filter Graph Manager</span></span>

<span data-ttu-id="b94e4-117">如果您不想使用 [Capture Graph Builder]，可以使用 [篩選圖形管理員] 上的方法來建立 VMR 9 圖形，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b94e4-117">If you prefer not to use the Capture Graph Builder, you can build a VMR-9 graph simply using methods on the Filter Graph Manager, as follows:</span></span>

1.  <span data-ttu-id="b94e4-118">建立 VMR-9 並將它新增至圖形，如先前的程式所示。</span><span class="sxs-lookup"><span data-stu-id="b94e4-118">Create the VMR-9 and add it to the graph, as shown in the previous procedure.</span></span>
2.  <span data-ttu-id="b94e4-119">使用 AddSourceFilter 來新增影片檔案的來源篩選器，如先前的程式所示。</span><span class="sxs-lookup"><span data-stu-id="b94e4-119">Use AddSourceFilter to add a source filter for the video file, as shown in the previous procedure.</span></span>
3.  <span data-ttu-id="b94e4-120">如果您想要轉譯音訊，請建立 [DirectSound](directsound-renderer-filter.md) 轉譯器篩選器的實例，並將它加入至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="b94e4-120">If you want to render the audio, create an instance of the [DirectSound Renderer](directsound-renderer-filter.md) filter and add it to the filter graph.</span></span>
4.  <span data-ttu-id="b94e4-121">使用 IBaseFilter：： EnumPins 方法來尋找來源篩選器上的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="b94e4-121">Use the IBaseFilter::EnumPins method to find an output pin on the source filter.</span></span> <span data-ttu-id="b94e4-122">如需詳細資料，請參閱 [列舉釘](enumerating-pins.md) 選。</span><span class="sxs-lookup"><span data-stu-id="b94e4-122">See [Enumerating Pins](enumerating-pins.md) for details.</span></span>
5.  <span data-ttu-id="b94e4-123">查詢 IFilterGraph2 介面的篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="b94e4-123">Query the Filter Graph Manager for the IFilterGraph2 interface.</span></span>
6.  <span data-ttu-id="b94e4-124">使用 AM RenderEx RENDERTOEXISTINGRENDERERS 旗標呼叫 [**IFilterGraph2：： RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="b94e4-124">Call [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) with the AM\_RENDEREX\_RENDERTOEXISTINGRENDERERS flag.</span></span> <span data-ttu-id="b94e4-125">此呼叫只會使用已在圖形中的轉譯器篩選器（在此案例中為 VMR-9 和 DirectSound 轉譯器）來呈現輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="b94e4-125">This call renders the output pin, using only the renderer filters already in the graph — in this case, the VMR-9 and the DirectSound Renderer.</span></span> <span data-ttu-id="b94e4-126">這可防止智慧型 Connect 邏輯將預設影片轉譯器新增至圖形，這會讓 VMR-9 保持未連接。</span><span class="sxs-lookup"><span data-stu-id="b94e4-126">This prevents the Intelligent Connect logic from adding the default video renderer to the graph, which would leave the VMR-9 unconnected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b94e4-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="b94e4-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b94e4-128">使用 Capture Graph Builder 建立圖形</span><span class="sxs-lookup"><span data-stu-id="b94e4-128">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



