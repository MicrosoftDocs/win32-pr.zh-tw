---
description: 本主題是在 DirectShow 中進行音訊/影片播放教學課程的步驟4。
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: 步驟4：新增影片轉譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17a0622909525f69cf64fd374c8512a8fa9bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992620"
---
# <a name="step-4-add-the-video-renderer"></a><span data-ttu-id="24431-103">步驟4：新增影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="24431-103">Step 4: Add the Video Renderer</span></span>

<span data-ttu-id="24431-104">本主題是 [在 DirectShow 中進行音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟4。</span><span class="sxs-lookup"><span data-stu-id="24431-104">This topic is step 4 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="24431-105">完整的程式碼會顯示在「 [DirectShow 播放」範例](directshow-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="24431-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="24431-106">DirectShow 提供數種可轉譯影片的不同篩選：</span><span class="sxs-lookup"><span data-stu-id="24431-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="24431-107">[**增強的影片轉譯器篩選器**](enhanced-video-renderer-filter.md) (EVR) </span><span class="sxs-lookup"><span data-stu-id="24431-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="24431-108">[影片混合轉譯器篩選器 9](video-mixing-renderer-filter-9.md) (VMR-9) </span><span class="sxs-lookup"><span data-stu-id="24431-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="24431-109">[影片混合轉譯器篩選器 7](video-mixing-renderer-filter-7.md) (VMR-7) </span><span class="sxs-lookup"><span data-stu-id="24431-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="24431-110">如需這些篩選之間差異的詳細資訊，請參閱 [選擇正確的影片](choosing-the-right-renderer.md)轉譯器。</span><span class="sxs-lookup"><span data-stu-id="24431-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="24431-111">在本教學課程中，每個影片轉譯器篩選都是由類別所包裝，以摘要它們之間的部分差異。</span><span class="sxs-lookup"><span data-stu-id="24431-111">In this tutorial, each video renderer filter is wrapped by a class that abstracts some of the differences between them.</span></span> <span data-ttu-id="24431-112">這些類別都是衍生自名為的抽象基類 `CVideoRenderer` 。</span><span class="sxs-lookup"><span data-stu-id="24431-112">These classes all derive from an abstract base class named `CVideoRenderer`.</span></span> <span data-ttu-id="24431-113">的宣告 `CVideoRenderer` 會在 [步驟2： Declare CVideoRenderer 和衍生類別](step-2--declare-cvideorenderer-and-derived-classes.md)中顯示。</span><span class="sxs-lookup"><span data-stu-id="24431-113">The declaration of `CVideoRenderer` is shown in [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

<span data-ttu-id="24431-114">下列方法會先嘗試依序建立每個影片轉譯器、EVR、VMR-9 和最後一個 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="24431-114">The following method tries to create each video renderer in turn, starting with the EVR, then the VMR-9, and finally the VMR-7.</span></span>


```C++
HRESULT DShowPlayer::CreateVideoRenderer()
{
    HRESULT hr = E_FAIL;

    enum { Try_EVR, Try_VMR9, Try_VMR7 };

    for (DWORD i = Try_EVR; i <= Try_VMR7; i++)
    {
        switch (i)
        {
        case Try_EVR:
            m_pVideo = new (std::nothrow) CEVR();
            break;

        case Try_VMR9:
            m_pVideo = new (std::nothrow) CVMR9();
            break;

        case Try_VMR7:
            m_pVideo = new (std::nothrow) CVMR7();
            break;
        }

        if (m_pVideo == NULL)
        {
            hr = E_OUTOFMEMORY;
            break;
        }

        hr = m_pVideo->AddToGraph(m_pGraph, m_hwnd);
        if (SUCCEEDED(hr))
        {
            break;
        }

        delete m_pVideo;
        m_pVideo = NULL;
    }
    return hr;
}

```



### <a name="evr-filter"></a><span data-ttu-id="24431-115">EVR 篩選</span><span class="sxs-lookup"><span data-stu-id="24431-115">EVR Filter</span></span>

<span data-ttu-id="24431-116">下列程式碼會建立 EVR 篩選，並將其新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="24431-116">The following code creates the EVR filter and adds it to the filter graph.</span></span> <span data-ttu-id="24431-117">`AddFilterByCLSID`此範例中使用的函式會顯示在主題[依 CLSID 新增篩選器](add-a-filter-by-clsid.md)中。</span><span class="sxs-lookup"><span data-stu-id="24431-117">The function `AddFilterByCLSID` used in this example is shown in the topic [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>


```C++
HRESULT CEVR::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pEVR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_EnhancedVideoRenderer, 
        &pEVR, L"EVR");

    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitializeEVR(pEVR, hwnd, &m_pVideoDisplay);
    if (FAILED(hr))
    {
        goto done;
    }

    // Note: Because IMFVideoDisplayControl is a service interface,
    // you cannot QI the pointer to get back the IBaseFilter pointer.
    // Therefore, we need to cache the IBaseFilter pointer.

    m_pEVR = pEVR;
    m_pEVR->AddRef();

done:
    SafeRelease(&pEVR);
    return hr;
}
```



<span data-ttu-id="24431-118">`InitializeEVR`函數會初始化 EVR 篩選。</span><span class="sxs-lookup"><span data-stu-id="24431-118">The `InitializeEVR` function initializes the EVR filter.</span></span> <span data-ttu-id="24431-119">此函式會執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="24431-119">This function performs the following steps.</span></span>

1.  <span data-ttu-id="24431-120">查詢 [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) 介面的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="24431-120">Queries the filter for the [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="24431-121">呼叫 [**IMFGetService：： GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) 來取得 [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="24431-121">Calls [**IMFGetService::GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span>
3.  <span data-ttu-id="24431-122">呼叫 [**IMFVideoDisplayControl：： SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) 來設定影片視窗。</span><span class="sxs-lookup"><span data-stu-id="24431-122">Calls [**IMFVideoDisplayControl::SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) to set the video window.</span></span>
4.  <span data-ttu-id="24431-123">呼叫 [**IMFVideoDisplayControl：： SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) 來設定 EVR，以保持影片的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="24431-123">Calls [**IMFVideoDisplayControl::SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) to configure the EVR to preserve the video aspect ratio.</span></span>

<span data-ttu-id="24431-124">下列程式碼顯示 `InitializeEVR` 函數。</span><span class="sxs-lookup"><span data-stu-id="24431-124">The following code shows the `InitializeEVR` function.</span></span>


```C++
HRESULT InitializeEVR( 
    IBaseFilter *pEVR,              // Pointer to the EVR
    HWND hwnd,                      // Clipping window
    IMFVideoDisplayControl** ppDisplayControl
    ) 
{ 
    IMFGetService *pGS = NULL;
    IMFVideoDisplayControl *pDisplay = NULL;

    HRESULT hr = pEVR->QueryInterface(IID_PPV_ARGS(&pGS)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGS->GetService(MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&pDisplay));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pDisplay->SetVideoWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pDisplay->SetAspectRatioMode(MFVideoARMode_PreservePicture);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IMFVideoDisplayControl pointer to the caller.
    *ppDisplayControl = pDisplay;
    (*ppDisplayControl)->AddRef();

done:
    SafeRelease(&pGS);
    SafeRelease(&pDisplay);
    return hr; 
} 
```



<span data-ttu-id="24431-125">建立圖表之後，會 `DShowPlayer::RenderStreams` 呼叫 `CVideoRenderer::FinalizeGraph` 。</span><span class="sxs-lookup"><span data-stu-id="24431-125">After the graph is built, the `DShowPlayer::RenderStreams` calls `CVideoRenderer::FinalizeGraph`.</span></span> <span data-ttu-id="24431-126">這個方法會執行任何最終初始化或清除。</span><span class="sxs-lookup"><span data-stu-id="24431-126">This method performs any final initialization or cleanup.</span></span> <span data-ttu-id="24431-127">下列程式碼示範 `CEVR` 此方法的執行方式。</span><span class="sxs-lookup"><span data-stu-id="24431-127">The following code shows the `CEVR` implementation of this method.</span></span>


```C++
HRESULT CEVR::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pEVR == NULL)
    {
        return S_OK;
    }

    BOOL bRemoved;
    HRESULT hr = RemoveUnconnectedRenderer(pGraph, m_pEVR, &bRemoved);
    if (bRemoved)
    {
        SafeRelease(&m_pEVR);
        SafeRelease(&m_pVideoDisplay);
    }
    return hr;
}
```



<span data-ttu-id="24431-128">如果 EVR 未連接到任何其他篩選，這個方法會從圖形中移除 EVR。</span><span class="sxs-lookup"><span data-stu-id="24431-128">If the EVR is not connected to any other filter, this method removes the EVR from the graph.</span></span> <span data-ttu-id="24431-129">如果媒體檔案未包含影片資料流程，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="24431-129">This can occur if the media file does not contain a video stream.</span></span>

### <a name="vmr-9-filter"></a><span data-ttu-id="24431-130">VMR-9 篩選</span><span class="sxs-lookup"><span data-stu-id="24431-130">VMR-9 Filter</span></span>

<span data-ttu-id="24431-131">下列程式碼會建立 VMR 9 篩選器，並將它新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="24431-131">The following code creates the VMR-9 filter and adds it to the filter graph.</span></span>


```C++
HRESULT CVMR9::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer9, 
        &pVMR, L"VMR-9");
    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR 
        // is connected.
        hr = InitWindowlessVMR9(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



<span data-ttu-id="24431-132">此函 `InitWindowlessVMR9` 式會初始化無視窗模式的 VMR-9。</span><span class="sxs-lookup"><span data-stu-id="24431-132">The `InitWindowlessVMR9` function initializes the VMR-9 for windowless mode.</span></span> <span data-ttu-id="24431-133"> (如需無視窗模式的詳細資訊，請參閱 [VMR 無視窗模式](vmr-windowless-mode.md)。 ) 此函式會執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="24431-133">(For more information about windowless mode, see [VMR Windowless Mode](vmr-windowless-mode.md).) This function performs the following steps.</span></span>

1.  <span data-ttu-id="24431-134">查詢 VMR-9 篩選器的 [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) 介面。</span><span class="sxs-lookup"><span data-stu-id="24431-134">Queries the VMR-9 filter for the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) interface.</span></span>
2.  <span data-ttu-id="24431-135">呼叫 [**IVMRFilterConfig9：： SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) 方法來設定無視窗模式。</span><span class="sxs-lookup"><span data-stu-id="24431-135">Calls the [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="24431-136">查詢 VMR-9 篩選器的 [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) 介面。</span><span class="sxs-lookup"><span data-stu-id="24431-136">Queries the VMR-9 filter for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
4.  <span data-ttu-id="24431-137">呼叫 [**IVMRWindowlessControl9：： SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) 方法來設定影片視窗。</span><span class="sxs-lookup"><span data-stu-id="24431-137">Calls the [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="24431-138">呼叫 [**IVMRWindowlessControl9：： SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) 方法以保存影片外觀比例。</span><span class="sxs-lookup"><span data-stu-id="24431-138">Calls the [**IVMRWindowlessControl9::SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="24431-139">下列程式碼顯示 `InitWindowlessVMR9` 函數。</span><span class="sxs-lookup"><span data-stu-id="24431-139">The following code shows the `InitWindowlessVMR9` function.</span></span>


```C++
HRESULT InitWindowlessVMR9( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl9** ppWC   // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig9 * pConfig = NULL; 
    IVMRWindowlessControl9 *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMR9Mode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR9ARMode_LetterBox);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



<span data-ttu-id="24431-140">`CVMR9::FinalizeGraph`方法會檢查 VMR-9 篩選是否已連接，如果不是，則會將它從篩選圖形中移除。</span><span class="sxs-lookup"><span data-stu-id="24431-140">The `CVMR9::FinalizeGraph` method checks if the VMR-9 filter is connected, and if not, removes it from the filter graph.</span></span>


```C++
HRESULT CVMR9::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



### <a name="vmr-7-filter"></a><span data-ttu-id="24431-141">VMR-7 篩選</span><span class="sxs-lookup"><span data-stu-id="24431-141">VMR-7 Filter</span></span>

<span data-ttu-id="24431-142">VMR-7 篩選器的步驟幾乎與 VMR 9 的步驟相同，但會改用 VMR-7 介面。</span><span class="sxs-lookup"><span data-stu-id="24431-142">The steps for the VMR-7 filter are nearly identical to those for the VMR-9, except the VMR-7 interfaces are used instead.</span></span> <span data-ttu-id="24431-143">下列程式碼會建立 VMR-7 篩選器，並將它新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="24431-143">The following code creates the VMR-7 filter and adds it to the filter graph.</span></span>


```C++
HRESULT CVMR7::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer, 
        &pVMR, L"VMR-7");

    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR
        // is connected.
        hr = InitWindowlessVMR(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



<span data-ttu-id="24431-144">`InitWindowlessVMR`函數會初始化無視窗模式的 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="24431-144">The `InitWindowlessVMR` function initializes the VMR-7 for windowless mode.</span></span> <span data-ttu-id="24431-145">此函式會執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="24431-145">This function performs the following steps.</span></span>

1.  <span data-ttu-id="24431-146">查詢 [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) 介面的 VMR-7 篩選。</span><span class="sxs-lookup"><span data-stu-id="24431-146">Queries the VMR-7 filter for the [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) interface.</span></span>
2.  <span data-ttu-id="24431-147">呼叫 [**IVMRFilterConfig：： SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) 方法來設定無視窗模式。</span><span class="sxs-lookup"><span data-stu-id="24431-147">Calls the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="24431-148">查詢 [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) 介面的 VMR-7 篩選。</span><span class="sxs-lookup"><span data-stu-id="24431-148">Queries the VMR-7 filter for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
4.  <span data-ttu-id="24431-149">呼叫 [**IVMRWindowlessControl：： SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) 方法來設定影片視窗。</span><span class="sxs-lookup"><span data-stu-id="24431-149">Calls the [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="24431-150">呼叫 [**IVMRWindowlessControl：： SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) 方法以保存影片外觀比例。</span><span class="sxs-lookup"><span data-stu-id="24431-150">Calls the [**IVMRWindowlessControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="24431-151">下列程式碼顯示 `InitWindowlessVMR` 函數。</span><span class="sxs-lookup"><span data-stu-id="24431-151">The following code shows the `InitWindowlessVMR` function.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl** ppWC    // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig* pConfig = NULL; 
    IVMRWindowlessControl *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR_ARMODE_LETTER_BOX);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



<span data-ttu-id="24431-152">`CVMR7::FinalizeGraph`方法會檢查 VMR-7 篩選是否已連接，如果不是，則會將它從篩選圖形中移除。</span><span class="sxs-lookup"><span data-stu-id="24431-152">The `CVMR7::FinalizeGraph` method checks if the VMR-7 filter is connected, and if not, removes it from the filter graph.</span></span>


```C++
HRESULT CVMR7::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="24431-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="24431-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24431-154">DirectShow 播放範例</span><span class="sxs-lookup"><span data-stu-id="24431-154">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="24431-155">使用 DirectShow EVR 篩選器</span><span class="sxs-lookup"><span data-stu-id="24431-155">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="24431-156">使用影片混合轉譯器</span><span class="sxs-lookup"><span data-stu-id="24431-156">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
