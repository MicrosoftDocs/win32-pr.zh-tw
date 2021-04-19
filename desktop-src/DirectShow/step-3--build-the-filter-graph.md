---
description: 本主題是在 DirectShow 中進行音訊/影片播放教學課程的步驟3。
ms.assetid: 45679c14-2671-420d-9766-61f2b2bb713a
title: 步驟3：建立篩選圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a770ad823a2578fab88a09cc44a3c7f2be4a4ca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979301"
---
# <a name="step-3-build-the-filter-graph"></a><span data-ttu-id="90268-103">步驟3：建立篩選圖形</span><span class="sxs-lookup"><span data-stu-id="90268-103">Step 3: Build the Filter Graph</span></span>

<span data-ttu-id="90268-104">本主題是 [在 DirectShow 中進行音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟3。</span><span class="sxs-lookup"><span data-stu-id="90268-104">This topic is step 3 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="90268-105">完整的程式碼會顯示在「 [DirectShow 播放」範例](directshow-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="90268-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="90268-106">下一步是建立篩選圖形來播放媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="90268-106">The next step is to build a filter graph to play the media file.</span></span>

### <a name="opening-a-media-file"></a><span data-ttu-id="90268-107">開啟媒體檔案</span><span class="sxs-lookup"><span data-stu-id="90268-107">Opening a Media File</span></span>

<span data-ttu-id="90268-108">`DShowPlayer::OpenFile`方法會開啟媒體檔案以供播放。</span><span class="sxs-lookup"><span data-stu-id="90268-108">The `DShowPlayer::OpenFile` method opens a media file for playback.</span></span> <span data-ttu-id="90268-109">這個方法會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="90268-109">This method does the following:</span></span>

1.  <span data-ttu-id="90268-110">建立新的 (空白) 篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="90268-110">Creates a new (empty) filter graph.</span></span>
2.  <span data-ttu-id="90268-111">呼叫 [**IGraphBuilder：： AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) ，以新增指定檔案的來源篩選。</span><span class="sxs-lookup"><span data-stu-id="90268-111">Calls [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add a source filter for the specified file.</span></span>
3.  <span data-ttu-id="90268-112">轉譯來源篩選上的資料流程。</span><span class="sxs-lookup"><span data-stu-id="90268-112">Renders the streams on the source filter.</span></span>


```C++
HRESULT DShowPlayer::OpenFile(PCWSTR pszFileName)
{
    IBaseFilter *pSource = NULL;

    // Create a new filter graph. (This also closes the old one, if any.)
    HRESULT hr = InitializeGraph();
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the source filter to the graph.
    hr = m_pGraph->AddSourceFilter(pszFileName, NULL, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Try to render the streams.
    hr = RenderStreams(pSource);

done:
    if (FAILED(hr))
    {
        TearDownGraph();
    }
    SafeRelease(&pSource);
    return hr;
}
```



### <a name="creating-the-filter-graph-manager"></a><span data-ttu-id="90268-113">建立篩選圖形管理員</span><span class="sxs-lookup"><span data-stu-id="90268-113">Creating the Filter Graph Manager</span></span>

<span data-ttu-id="90268-114">`DShowPlayer::InitializeGraph`方法會建立新的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="90268-114">The `DShowPlayer::InitializeGraph` method creates a new filter graph.</span></span> <span data-ttu-id="90268-115">這個方法會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="90268-115">This method does the following:</span></span>

1.  <span data-ttu-id="90268-116">呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立 [篩選圖形管理員](filter-graph-manager.md)的新實例。</span><span class="sxs-lookup"><span data-stu-id="90268-116">Calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="90268-117">查詢 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 和 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 介面的篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="90268-117">Queries the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>
3.  <span data-ttu-id="90268-118">呼叫 [**IMediaEventEx：： SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) 來設定事件通知。</span><span class="sxs-lookup"><span data-stu-id="90268-118">Calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) to set up event notification.</span></span> <span data-ttu-id="90268-119">如需詳細資訊，請參閱 [DirectShow 中的事件通知](event-notification-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="90268-119">For more information, see [Event Notification in DirectShow](event-notification-in-directshow.md).</span></span>


```C++
HRESULT DShowPlayer::InitializeGraph()
{
    TearDownGraph();

    // Create the Filter Graph Manager.
    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set up event notification.
    hr = m_pEvent->SetNotifyWindow((OAHWND)m_hwnd, WM_GRAPH_EVENT, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = STATE_STOPPED;

done:
    return hr;
}
```



### <a name="rendering-the-streams"></a><span data-ttu-id="90268-120">轉譯資料流程</span><span class="sxs-lookup"><span data-stu-id="90268-120">Rendering the Streams</span></span>

<span data-ttu-id="90268-121">下一步是將來源篩選連接至一或多個轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="90268-121">The next step is to connect the source filter to one or more renderer filters.</span></span>

<span data-ttu-id="90268-122">`DShowPlayer::RenderStreams`方法會執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="90268-122">The `DShowPlayer::RenderStreams` method performs the following steps.</span></span>

1.  <span data-ttu-id="90268-123">查詢 [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) 介面的篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="90268-123">Queries the Filter Graph Manager for the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface.</span></span>
2.  <span data-ttu-id="90268-124">將影片轉譯器篩選器新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="90268-124">Adds a video renderer filter to the filter graph.</span></span>
3.  <span data-ttu-id="90268-125">將 [DirectSound 轉譯器篩選](directsound-renderer-filter.md) 新增至篩選圖形，以支援音訊播放。</span><span class="sxs-lookup"><span data-stu-id="90268-125">Adds the [DirectSound Renderer Filter](directsound-renderer-filter.md) to the filter graph, to support audio playback.</span></span> <span data-ttu-id="90268-126">如需將篩選準則加入至篩選圖形的詳細資訊，請參閱 [依 CLSID 加入篩選](add-a-filter-by-clsid.md)。</span><span class="sxs-lookup"><span data-stu-id="90268-126">For more information about adding filters to the filter graph, see [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>
4.  <span data-ttu-id="90268-127">列舉來源篩選器上的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="90268-127">Enumerates the output pins on the source filter.</span></span> <span data-ttu-id="90268-128">如需列舉釘選的詳細資訊，請參閱 [列舉釘](enumerating-pins.md)選。</span><span class="sxs-lookup"><span data-stu-id="90268-128">For more information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).</span></span>
5.  <span data-ttu-id="90268-129">針對每個 pin，呼叫 [**IFilterGraph2：： RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) 方法。</span><span class="sxs-lookup"><span data-stu-id="90268-129">For each pin, calls the [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) method.</span></span> <span data-ttu-id="90268-130">這個方法會將輸出圖釘連接到轉譯器篩選器，視需要加入中繼篩選器，如 (的) 。</span><span class="sxs-lookup"><span data-stu-id="90268-130">This method connects the output pin to a renderer filter, adding intermediate filters if needed (such as decoders).</span></span>
6.  <span data-ttu-id="90268-131">呼叫 `CVideoRenderer::FinalizeGraph` 以完成影片轉譯器的初始化。</span><span class="sxs-lookup"><span data-stu-id="90268-131">Calls `CVideoRenderer::FinalizeGraph` to finish initializing the video renderer.</span></span>
7.  <span data-ttu-id="90268-132">如果篩選未連接到另一個篩選器，則移除 [DirectSound](directsound-renderer-filter.md) 轉譯器篩選。</span><span class="sxs-lookup"><span data-stu-id="90268-132">Removes the [DirectSound Renderer](directsound-renderer-filter.md) filter if that filter is not connected to another filter.</span></span> <span data-ttu-id="90268-133">如果來源檔案不包含音訊資料流程，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="90268-133">This can occur if the source file does not contain an audio stream.</span></span>


```C++
// Render the streams from a source filter. 

HRESULT DShowPlayer::RenderStreams(IBaseFilter *pSource)
{
    BOOL bRenderedAnyPin = FALSE;

    IFilterGraph2 *pGraph2 = NULL;
    IEnumPins *pEnum = NULL;
    IBaseFilter *pAudioRenderer = NULL;
    HRESULT hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&pGraph2));
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the video renderer to the graph
    hr = CreateVideoRenderer();
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the DSound Renderer to the graph.
    hr = AddFilterByCLSID(m_pGraph, CLSID_DSoundRender, 
        &pAudioRenderer, L"Audio Renderer");
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate the pins on the source filter.
    hr = pSource->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    // Loop through all the pins
    IPin *pPin;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {           
        // Try to render this pin. 
        // It's OK if we fail some pins, if at least one pin renders.
        HRESULT hr2 = pGraph2->RenderEx(pPin, AM_RENDEREX_RENDERTOEXISTINGRENDERERS, NULL);

        pPin->Release();
        if (SUCCEEDED(hr2))
        {
            bRenderedAnyPin = TRUE;
        }
    }

    hr = m_pVideo->FinalizeGraph(m_pGraph);
    if (FAILED(hr))
    {
        goto done;
    }

    // Remove the audio renderer, if not used.
    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(m_pGraph, pAudioRenderer, &bRemoved);

done:
    SafeRelease(&pEnum);
    SafeRelease(&pAudioRenderer);
    SafeRelease(&pGraph2);

    // If we succeeded to this point, make sure we rendered at least one 
    // stream.
    if (SUCCEEDED(hr))
    {
        if (!bRenderedAnyPin)
        {
            hr = VFW_E_CANNOT_RENDER;
        }
    }
    return hr;
}
```



<span data-ttu-id="90268-134">以下是在 `RemoveUnconnectedRenderer` 上一個範例中使用的函式程式碼。</span><span class="sxs-lookup"><span data-stu-id="90268-134">Here is the code for the `RemoveUnconnectedRenderer` function, which is used in the previous example.</span></span>


```C++
HRESULT RemoveUnconnectedRenderer(IGraphBuilder *pGraph, IBaseFilter *pRenderer, BOOL *pbRemoved)
{
    IPin *pPin = NULL;

    *pbRemoved = FALSE;

    // Look for a connected input pin on the renderer.

    HRESULT hr = FindConnectedPin(pRenderer, PINDIR_INPUT, &pPin);
    SafeRelease(&pPin);

    // If this function succeeds, the renderer is connected, so we don't remove it.
    // If it fails, it means the renderer is not connected to anything, so
    // we remove it.

    if (FAILED(hr))
    {
        hr = pGraph->RemoveFilter(pRenderer);
        *pbRemoved = TRUE;
    }

    return hr;
}
```



### <a name="releasing-the-filter-graph"></a><span data-ttu-id="90268-135">釋放篩選圖形</span><span class="sxs-lookup"><span data-stu-id="90268-135">Releasing the Filter Graph</span></span>

<span data-ttu-id="90268-136">當應用程式結束時，它必須釋放篩選圖形，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="90268-136">When the application exits, it must release the filter graph, as shown in the following code.</span></span>


```C++
void DShowPlayer::TearDownGraph()
{
    // Stop sending event messages
    if (m_pEvent)
    {
        m_pEvent->SetNotifyWindow((OAHWND)NULL, NULL, NULL);
    }

    SafeRelease(&m_pGraph);
    SafeRelease(&m_pControl);
    SafeRelease(&m_pEvent);

    delete m_pVideo;
    m_pVideo = NULL;

    m_state = STATE_NO_GRAPH;
}
```



<span data-ttu-id="90268-137">下一 [步：步驟4：新增影片](step-4--add-the-video-renderer.md)轉譯器。</span><span class="sxs-lookup"><span data-stu-id="90268-137">Next: [Step 4: Add the Video Renderer](step-4--add-the-video-renderer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="90268-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="90268-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90268-139">在 DirectShow 播放音訊/影片</span><span class="sxs-lookup"><span data-stu-id="90268-139">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="90268-140">DirectShow 播放範例</span><span class="sxs-lookup"><span data-stu-id="90268-140">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="90268-141">建立篩選圖形</span><span class="sxs-lookup"><span data-stu-id="90268-141">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="90268-142">一般 Graph-Building 技術</span><span class="sxs-lookup"><span data-stu-id="90268-142">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 
