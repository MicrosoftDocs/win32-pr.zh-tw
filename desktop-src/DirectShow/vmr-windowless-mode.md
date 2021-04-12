---
description: VMR 無視窗模式
ms.assetid: 0dc871d2-79c4-4bf8-96ef-13c4d1ab4497
title: VMR 無視窗模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b137fbc1351f2bbe5ed38673b681e45558675d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318724"
---
# <a name="vmr-windowless-mode"></a><span data-ttu-id="7d693-103">VMR 無視窗模式</span><span class="sxs-lookup"><span data-stu-id="7d693-103">VMR Windowless Mode</span></span>

<span data-ttu-id="7d693-104">無視窗模式是應用程式在應用程式視窗內轉譯影片的慣用方式。</span><span class="sxs-lookup"><span data-stu-id="7d693-104">Windowless mode is the preferred way for applications to render video inside an application window.</span></span> <span data-ttu-id="7d693-105">在無視窗模式中，影片混合轉譯器不會載入其視窗管理員元件，因此不支援 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 或 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面。</span><span class="sxs-lookup"><span data-stu-id="7d693-105">In windowless mode, the Video Mixing Renderer does not load its Window Manager component, and therefore does not support the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) or [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interfaces.</span></span> <span data-ttu-id="7d693-106">相反地，應用程式會提供播放視窗，並在工作區中設定目的地矩形，讓 VMR 繪製影片。</span><span class="sxs-lookup"><span data-stu-id="7d693-106">Instead, the application provides the playback window and sets a destination rectangle in the client area for the VMR to draw the video.</span></span> <span data-ttu-id="7d693-107">VMR 會使用 DirectDraw 的 clipper 物件，以確保影片會裁剪到應用程式的視窗，且不會出現在任何其他視窗上。</span><span class="sxs-lookup"><span data-stu-id="7d693-107">The VMR uses a DirectDraw clipper object to ensure that the video is clipped to the application's window and does not appear on any other windows.</span></span> <span data-ttu-id="7d693-108">VMR 不會將應用程式的視窗子類別化，也不會安裝任何系統/進程勾點。</span><span class="sxs-lookup"><span data-stu-id="7d693-108">The VMR does not subclass the application's window or install any system/process hooks.</span></span>

<span data-ttu-id="7d693-109">在無視窗模式中，連接期間的事件順序以及轉換至執行狀態的順序如下：</span><span class="sxs-lookup"><span data-stu-id="7d693-109">In windowless mode, the sequence of events during connection and transition to the run state is as follows:</span></span>

-   <span data-ttu-id="7d693-110">上游篩選器會提出 VMR 可接受或拒絕的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="7d693-110">The upstream filter proposes a media type, which the VMR either accepts or rejects.</span></span>
-   <span data-ttu-id="7d693-111">如果媒體類型為 [已接受]，VMR 會呼叫配置器提供者來取得 DirectDraw 表面。</span><span class="sxs-lookup"><span data-stu-id="7d693-111">If the media type is accepted, the VMR calls the allocator-presenter to obtain a DirectDraw surface.</span></span> <span data-ttu-id="7d693-112">如果介面已成功建立，則圖釘會連線，而且 VMR 已準備好轉換成執行狀態。</span><span class="sxs-lookup"><span data-stu-id="7d693-112">If the surface is created successfully, the pins connect and the VMR is ready to transition into the run state.</span></span>
-   <span data-ttu-id="7d693-113">當篩選圖形執行時，此解碼器會呼叫 **GetBuffer** 以從配置器取得媒體範例。</span><span class="sxs-lookup"><span data-stu-id="7d693-113">When the filter graph runs, the decoder calls **GetBuffer** to get a media sample from the allocator.</span></span> <span data-ttu-id="7d693-114">VMR 會查詢配置器提供者，以確保其 DirectDraw 介面上的圖元深度、矩形大小和其他參數與內送影片相容。</span><span class="sxs-lookup"><span data-stu-id="7d693-114">The VMR queries the allocator-presenter to ensure that the pixel depth, rectangle size, and other parameters on its DirectDraw surface are compatible with the incoming video.</span></span> <span data-ttu-id="7d693-115">如果相容，VMR 會將 DirectDraw 介面傳回給解碼器。</span><span class="sxs-lookup"><span data-stu-id="7d693-115">If they are compatible, the VMR returns the DirectDraw surface to the decoder.</span></span> <span data-ttu-id="7d693-116">在解碼器解碼成介面之後，VMR 的核心同步處理單位會驗證時間戳記。</span><span class="sxs-lookup"><span data-stu-id="7d693-116">After the decoder has decoded into the surface, the VMR's Core Synchronization Unit validates the time stamps.</span></span> <span data-ttu-id="7d693-117">此單元會封鎖 **接收** 呼叫，直到呈現時間到達為止。</span><span class="sxs-lookup"><span data-stu-id="7d693-117">This unit blocks the **Receive** call until the presentation time arrives.</span></span> <span data-ttu-id="7d693-118">此時，VMR 會在配置器顯示器上呼叫 **PresentImage** ，以呈現圖形配接器的介面。</span><span class="sxs-lookup"><span data-stu-id="7d693-118">At that point, the VMR calls **PresentImage** on the allocator-presenter, which presents the surface to the graphics card.</span></span>

<span data-ttu-id="7d693-119">下圖顯示具有多個輸入資料流程的無視窗模式 VMR。</span><span class="sxs-lookup"><span data-stu-id="7d693-119">The following illustration shows the VMR in windowless mode with multiple input streams.</span></span>

![以無視窗模式 vmr](images/vmr-windowless-mult-streams.png)

<span data-ttu-id="7d693-121">**設定無視窗模式的 VMR-7**</span><span class="sxs-lookup"><span data-stu-id="7d693-121">**Configuring the VMR-7 for Windowless Mode**</span></span>

<span data-ttu-id="7d693-122">若要設定無視窗模式的 VMR-7，請在連接任何 VMR 的輸入圖釘之前，執行下列所有步驟：</span><span class="sxs-lookup"><span data-stu-id="7d693-122">To configure the VMR-7 for windowless mode, perform all of the following steps before connecting any of the VMR's input pins:</span></span>

1.  <span data-ttu-id="7d693-123">建立篩選器，並將它新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="7d693-123">Create the filter and add it to the graph.</span></span>
2.  <span data-ttu-id="7d693-124">使用 VMRMode 無視窗旗標呼叫 [**IVMRFilterConfig：： SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) 方法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7d693-124">Call the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method with the VMRMode\_Windowless flag.</span></span>
3.  <span data-ttu-id="7d693-125">（選擇性）藉由呼叫 [**IVMRFilterConfig：： SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams)，設定多個輸入資料流程的 VMR。</span><span class="sxs-lookup"><span data-stu-id="7d693-125">Optionally, configure the VMR for multiple input streams by calling [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="7d693-126">VMR 會建立每個資料流程的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="7d693-126">The VMR creates an input pin for each stream.</span></span> <span data-ttu-id="7d693-127">您可以使用 [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) 介面來設定資料流程的迭置順序和其他參數。</span><span class="sxs-lookup"><span data-stu-id="7d693-127">Use the [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) interface to set the Z-order and other parameters for the stream.</span></span> <span data-ttu-id="7d693-128">如需詳細資訊，請參閱 [使用多個資料流程 (混合模式) 的 VMR ](vmr-with-multiple-streams--mixing-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="7d693-128">For more information, see [VMR with Multiple Streams (Mixing Mode)](vmr-with-multiple-streams--mixing-mode.md).</span></span>

    <span data-ttu-id="7d693-129">如果您未呼叫 **SetNumberOfStreams**，VMR-7 會預設為一個輸入的 pin。</span><span class="sxs-lookup"><span data-stu-id="7d693-129">If you do not call **SetNumberOfStreams**, the VMR-7 defaults to one input pin.</span></span> <span data-ttu-id="7d693-130">連接輸入連接之後，就無法變更 pin 數目。</span><span class="sxs-lookup"><span data-stu-id="7d693-130">After the input pins are connected, the number of pins cannot be changed.</span></span>

4.  <span data-ttu-id="7d693-131">呼叫 [**IVMRWindowlessControl：： SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) ，以指定將出現轉譯影片的視窗。</span><span class="sxs-lookup"><span data-stu-id="7d693-131">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) to specify the window in which the rendered video will appear.</span></span>

<span data-ttu-id="7d693-132">完成這些步驟之後，您就可以連接 VMR 篩選器的輸入接點。</span><span class="sxs-lookup"><span data-stu-id="7d693-132">Once these steps are completed, you can connect the VMR filter's input pins.</span></span> <span data-ttu-id="7d693-133">建立圖形的方式有很多種，例如直接連接釘選、使用智慧型連接方法（例如 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)），或使用 Capture graph Builder 的 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法。</span><span class="sxs-lookup"><span data-stu-id="7d693-133">There are various ways to build the graph, such as connecting pins directly, using Intelligent Connect methods such as [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), or using the Capture Graph Builder's [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method.</span></span> <span data-ttu-id="7d693-134">如需詳細資訊，請參閱 [一般 Graph-Building 技術](general-graph-building-techniques.md)。</span><span class="sxs-lookup"><span data-stu-id="7d693-134">For more information, see [General Graph-Building Techniques](general-graph-building-techniques.md).</span></span>

<span data-ttu-id="7d693-135">若要設定影片在應用程式視窗中的位置，請呼叫 [**IVMRWindowlessControl：： SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) 方法。</span><span class="sxs-lookup"><span data-stu-id="7d693-135">To set the position of the video within the application window, call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method.</span></span> <span data-ttu-id="7d693-136">[**IVMRWindowlessControl：： GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize)方法會傳回原生影片大小。</span><span class="sxs-lookup"><span data-stu-id="7d693-136">The [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method returns the native video size.</span></span> <span data-ttu-id="7d693-137">在播放期間，應用程式應該通知 VMR 下列 Windows 訊息：</span><span class="sxs-lookup"><span data-stu-id="7d693-137">During playback, the application should notify the VMR of the following Windows messages:</span></span>

-   <span data-ttu-id="7d693-138">WM \_ 油漆：呼叫 [**IVMRWindowlessControl：： RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) 來重新繪製影像。</span><span class="sxs-lookup"><span data-stu-id="7d693-138">WM\_PAINT: Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo) to repaint the image.</span></span>
-   <span data-ttu-id="7d693-139">WM \_ DISPLAYCHANGE： Call [**IVMRWindowlessControl：:D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged)。</span><span class="sxs-lookup"><span data-stu-id="7d693-139">WM\_DISPLAYCHANGE: Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="7d693-140">VMR 會採取任何必要動作，以在新的解析度或色彩深度顯示影片。</span><span class="sxs-lookup"><span data-stu-id="7d693-140">The VMR takes any actions that are needed to display the video at the new resolution or color depth.</span></span>
-   <span data-ttu-id="7d693-141">WM \_ 大小：重新計算影片的位置，然後視需要再次呼叫 [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) 。</span><span class="sxs-lookup"><span data-stu-id="7d693-141">WM\_SIZE: Recalculate the position of the video and call [**SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) again if necessary.</span></span>

> [!Note]  
> <span data-ttu-id="7d693-142">MFC 應用程式必須定義空的 WM \_ ERASEBKGND 訊息處理常式，否則影片顯示區域將無法正確地重新繪製。</span><span class="sxs-lookup"><span data-stu-id="7d693-142">MFC applications must define an empty WM\_ERASEBKGND message handler, or the video display area will not repaint correctly.</span></span>

 

<span data-ttu-id="7d693-143">**設定無視窗模式的 VMR-9**</span><span class="sxs-lookup"><span data-stu-id="7d693-143">**Configuring the VMR-9 for Windowless Mode**</span></span>

<span data-ttu-id="7d693-144">若要設定無視窗模式的 VMR-9，請使用針對無視窗模式 VMR-7 所述的步驟，但使用 [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) 和 [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) 介面。</span><span class="sxs-lookup"><span data-stu-id="7d693-144">To configure the VMR-9 for windowless mode, use the steps described for the VMR-7 for Windowless mode, but use the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) and [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interfaces.</span></span> <span data-ttu-id="7d693-145">唯一的差別在於 VMR-9 預設會建立四個輸入圖釘，而不是一個輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="7d693-145">The only significant difference is that the VMR-9 creates four input pins by default, rather than one input pin.</span></span> <span data-ttu-id="7d693-146">因此，如果您要混合四個以上的視頻串流，則只需要呼叫 **SetNumberOfStreams** 。</span><span class="sxs-lookup"><span data-stu-id="7d693-146">Therefore, you only need to call **SetNumberOfStreams** if you are mixing more than four video streams.</span></span>

<span data-ttu-id="7d693-147">**範例程式碼**</span><span class="sxs-lookup"><span data-stu-id="7d693-147">**Example Code**</span></span>

<span data-ttu-id="7d693-148">下列程式碼示範如何建立 VMR-7 篩選器，將它新增至 DirectShow 篩選圖形，然後讓 VMR 進入無視窗模式。</span><span class="sxs-lookup"><span data-stu-id="7d693-148">The following code shows how to create a VMR-7 filter, add it to the DirectShow filter graph, and then put the VMR into windowless mode.</span></span> <span data-ttu-id="7d693-149">若為 VMR-9，請使用 \_ **CoCreateInstance** 中的 CLSID VideoMixingRenderer9 和對應的 VMR-9 介面。</span><span class="sxs-lookup"><span data-stu-id="7d693-149">For the VMR-9, use CLSID\_VideoMixingRenderer9 in **CoCreateInstance** and the corresponding VMR-9 interfaces.</span></span>


```C++
HRESULT InitializeWindowlessVMR(
    HWND hwndApp,         // Application window.
    IFilterGraph* pFG,    // Pointer to the Filter Graph Manager.
    IVMRWindowlessControl** ppWc,  // Receives the interface.
    DWORD dwNumStreams,  // Number of streams to use.
    BOOL fBlendAppImage  // Are we alpha-blending a bitmap?
    )
{
    IBaseFilter* pVmr = NULL;
    IVMRWindowlessControl* pWc = NULL;
    *ppWc = NULL;

    // Create the VMR and add it to the filter graph.
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL,
       CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pFG->AddFilter(pVmr, L"Video Mixing Renderer");
    if (FAILED(hr))
    {
        pVmr->Release();
        return hr;
    }

    // Set the rendering mode and number of streams.  
    IVMRFilterConfig* pConfig;
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig);
    if (SUCCEEDED(hr)) 
    {
        pConfig->SetRenderingMode(VMRMode_Windowless);

        // Set the VMR-7 to mixing mode if you want more than one video
        // stream, or you want to mix a static bitmap over the video.
        // (The VMR-9 defaults to mixing mode with four inputs.)
        if (dwNumStreams > 1 || fBlendAppImage) 
        {
            pConfig->SetNumberOfStreams(dwNumStreams);
        }
        pConfig->Release();

        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if (SUCCEEDED(hr)) 
        {
            pWc->SetVideoClippingWindow(hwndApp);
            *ppWc = pWc;  // The caller must release this interface.
        }
    }
    pVmr->Release();

    // Now the VMR can be connected to other filters.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="7d693-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d693-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d693-151">使用無視窗模式</span><span class="sxs-lookup"><span data-stu-id="7d693-151">Using Windowless Mode</span></span>](using-windowless-mode.md)
</dt> </dl>

 

 



