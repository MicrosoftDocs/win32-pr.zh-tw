---
description: 使用無視窗模式
ms.assetid: f53cecaa-dee7-4b02-a4ac-ffbd917f73aa
title: 使用無視窗模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393b112c6d340c3440521876da08111dd4bb0e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850332"
---
# <a name="using-windowless-mode"></a><span data-ttu-id="f7dd7-103">使用無視窗模式</span><span class="sxs-lookup"><span data-stu-id="f7dd7-103">Using Windowless Mode</span></span>

<span data-ttu-id="f7dd7-104">[影片混合轉譯器篩選 7](video-mixing-renderer-filter-7.md) (VMR-7) 和 [影片混合轉譯器篩選器 9](video-mixing-renderer-filter-9.md) (VMR-9) 支援 *無視窗模式*，這代表 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)介面上的重大改進。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-104">Both the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9) support *windowless mode*, which represents a major improvement over the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="f7dd7-105">本主題說明無視窗模式和視窗模式之間的差異，以及如何使用無視窗模式。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-105">This topic describes the differences between windowless mode and windowed mode, and how to use windowless mode.</span></span>

<span data-ttu-id="f7dd7-106">為了維持與現有應用程式的回溯相容性，VMR 預設為視窗模式。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-106">To remain backward-compatible with existing applications, the VMR defaults to windowed mode.</span></span> <span data-ttu-id="f7dd7-107">在視窗模式中，轉譯器會建立自己的視窗來顯示影片。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-107">In windowed mode, the renderer creates its own window to display the video.</span></span> <span data-ttu-id="f7dd7-108">一般而言，應用程式會將影片視窗設定為應用程式視窗的子系。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-108">Typically the application sets the video window to be a child of the application window.</span></span> <span data-ttu-id="f7dd7-109">有個別的影片視窗會造成一些問題，不過：</span><span class="sxs-lookup"><span data-stu-id="f7dd7-109">The existence of a separate video window causes some problems, however:</span></span>

-   <span data-ttu-id="f7dd7-110">最重要的是，如果線上程之間傳送視窗訊息，則可能會發生鎖死。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-110">Most importantly, there is a potential for deadlocks if window messages are sent between threads.</span></span>
-   <span data-ttu-id="f7dd7-111">篩選圖形管理員必須將某些視窗訊息（例如 WM \_ 油漆）轉寄給影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-111">The Filter Graph Manager must forward certain window messages, such as WM\_PAINT, to the Video Renderer.</span></span> <span data-ttu-id="f7dd7-112">應用程式必須使用篩選圖形管理員的 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (，而不是影片轉譯器的) ，如此篩選圖形管理員就會維持正確的內部狀態。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-112">The application must use the Filter Graph Manager's implementation of [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (and not the Video Renderer's), so that the Filter Graph Manager maintains the correct internal state.</span></span>
-   <span data-ttu-id="f7dd7-113">若要從影片視窗接收滑鼠或鍵盤事件，應用程式必須設定 *訊息清空*，使影片視窗將這些訊息轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-113">To receive mouse or keyboard events from the video window, the application must set a *message drain*, causing the video window to forward these messages to the application.</span></span>
-   <span data-ttu-id="f7dd7-114">若要防止裁剪問題，影片視窗必須有正確的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-114">To prevent clipping problems, the video window must have the right window styles.</span></span>

<span data-ttu-id="f7dd7-115">無視窗模式可避免這些問題，方法是讓 VMR 直接在應用程式視窗的工作區上進行繪製，並使用 DirectDraw 來裁剪影片矩形。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-115">Windowless mode avoids these problems by having the VMR draw directly on the application window's client area, using DirectDraw to clip the video rectangle.</span></span> <span data-ttu-id="f7dd7-116">無視窗模式可大幅減少鎖死的機會。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-116">Windowless mode significantly reduces the chance of deadlocks.</span></span> <span data-ttu-id="f7dd7-117">此外，應用程式不需要設定擁有者視窗或視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-117">Also, the application does not have to set the owner window or the window styles.</span></span> <span data-ttu-id="f7dd7-118">事實上，當 VMR 處於無視窗模式時，它甚至不會公開不再需要的 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-118">In fact, when the VMR is in windowless mode, it does not even expose the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, which is no longer needed.</span></span>

<span data-ttu-id="f7dd7-119">若要使用無視窗模式，您必須明確設定 VMR。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-119">To use windowless mode, you must explicitly configure the VMR.</span></span> <span data-ttu-id="f7dd7-120">不過，您會發現更具彈性且更容易使用的視窗模式。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-120">However, you will find that is more flexible and easier to use than windowed mode.</span></span>

<span data-ttu-id="f7dd7-121">VMR-7 篩選和 VMR-9 篩選器會公開不同的介面，但每個都有相同的步驟。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-121">The VMR-7 filter and the VMR-9 filter expose different interfaces, but the steps are equivalent for each.</span></span>

## <a name="configure-the-vmr-for-windowless-mode"></a><span data-ttu-id="f7dd7-122">設定無視窗模式的 VMR</span><span class="sxs-lookup"><span data-stu-id="f7dd7-122">Configure the VMR for Windowless Mode</span></span>

<span data-ttu-id="f7dd7-123">若要覆寫 VMR 的預設行為，請在建立篩選圖形之前設定 VMR：</span><span class="sxs-lookup"><span data-stu-id="f7dd7-123">To override the VMR's default behavior, configure the VMR before building the filter graph:</span></span>

<span data-ttu-id="f7dd7-124">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="f7dd7-124">**VMR-7**</span></span>

1.  <span data-ttu-id="f7dd7-125">建立篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-125">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="f7dd7-126">建立 VMR-7 並將它新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-126">Create the VMR-7 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="f7dd7-127">使用 **VMRMode \_ 無視窗** 旗標，在 VMR-7 上呼叫 [**IVMRFilterConfig：： SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) 。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-127">Call [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) on the VMR-7 with the **VMRMode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="f7dd7-128">針對 [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) 介面查詢 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-128">Query the VMR-7 for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
5.  <span data-ttu-id="f7dd7-129">在 VMR-7 上呼叫 [**IVMRWindowlessControl：： SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) 。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-129">Call [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) on the VMR-7.</span></span> <span data-ttu-id="f7dd7-130">指定應顯示影片的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-130">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="f7dd7-131">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="f7dd7-131">**VMR-9**</span></span>

1.  <span data-ttu-id="f7dd7-132">建立篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-132">Create the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="f7dd7-133">建立 VMR-9 並將它新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-133">Create the VMR-9 and add it to the filter graph.</span></span>
3.  <span data-ttu-id="f7dd7-134">使用 **VMR9Mode \_ 無視窗** 旗標，在 VMR-9 上呼叫 [**IVMRFilterConfig9：： SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) 。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-134">Call [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) on the VMR-9 with the **VMR9Mode\_Windowless** flag.</span></span>
4.  <span data-ttu-id="f7dd7-135">針對 [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) 介面查詢 VMR-9。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-135">Query the VMR-9 for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
5.  <span data-ttu-id="f7dd7-136">在 VMR-9 上呼叫 [**IVMRWindowlessControl9：： SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) 。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-136">Call [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) on the VMR-9.</span></span> <span data-ttu-id="f7dd7-137">指定應顯示影片的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-137">Specify a handle to the window where the video should appear.</span></span>

<span data-ttu-id="f7dd7-138">現在請呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 或其他圖形建立方法，以建立篩選圖形的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-138">Now build the rest of the filter graph by calling [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or other graph-building methods.</span></span> <span data-ttu-id="f7dd7-139">篩選圖形管理員會自動使用您新增至圖形的 VMR 實例。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-139">The Filter Graph Manager automatically uses the instance of the VMR that you added to the graph.</span></span> <span data-ttu-id="f7dd7-140"> (如需發生此情況的詳細資訊，請參閱 [智慧型連接](intelligent-connect.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="f7dd7-140">(For details on why this happens, see [Intelligent Connect](intelligent-connect.md).)</span></span>

<span data-ttu-id="f7dd7-141">下列程式碼顯示 helper 函式，此函式會建立 VMR-7、將它新增至圖形，並設定無視窗模式。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-141">The following code shows a helper function that creates the VMR-7, adds it to the graph, and sets up windowless mode.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    HWND hwndApp,                  // Window to hold the video. 
    IGraphBuilder* pGraph,         // Pointer to the Filter Graph Manager. 
    IVMRWindowlessControl** ppWc   // Receives a pointer to the VMR.
    ) 
{ 
    if (!pGraph || !ppWc) 
    {
        return E_POINTER;
    }
    IBaseFilter* pVmr = NULL; 
    IVMRWindowlessControl* pWc = NULL; 
    // Create the VMR. 
    HRESULT hr = CoCreateInstance(CLSID_VideoMixingRenderer, NULL, 
        CLSCTX_INPROC, IID_IBaseFilter, (void**)&pVmr); 
    if (FAILED(hr))
    {
        return hr;
    }
    
    // Add the VMR to the filter graph.
    hr = pGraph->AddFilter(pVmr, L"Video Mixing Renderer"); 
    if (FAILED(hr)) 
    {
        pVmr->Release();
        return hr;
    }
    // Set the rendering mode.  
    IVMRFilterConfig* pConfig; 
    hr = pVmr->QueryInterface(IID_IVMRFilterConfig, (void**)&pConfig); 
    if (SUCCEEDED(hr)) 
    { 
        hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
        pConfig->Release(); 
    }
    if (SUCCEEDED(hr))
    {
        // Set the window. 
        hr = pVmr->QueryInterface(IID_IVMRWindowlessControl, (void**)&pWc);
        if( SUCCEEDED(hr)) 
        { 
            hr = pWc->SetVideoClippingWindow(hwndApp); 
            if (SUCCEEDED(hr))
            {
                *ppWc = pWc; // Return this as an AddRef'd pointer. 
            }
            else
            {
                // An error occurred, so release the interface.
                pWc->Release();
            }
        } 
    } 
    pVmr->Release(); 
    return hr; 
} 
```



<span data-ttu-id="f7dd7-142">此函式假設只會顯示一個影片資料流程，而不會在影片上混用靜態點陣圖。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-142">This function assumes that are displaying only one video stream and are not mixing a static bitmap over the video.</span></span> <span data-ttu-id="f7dd7-143">如需詳細資訊，請參閱 [VMR 無視窗模式](vmr-windowless-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-143">For details, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span> <span data-ttu-id="f7dd7-144">您會呼叫此函式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f7dd7-144">You would call this function as follows:</span></span>


```C++
IVMRWindowlessControl *pWc = NULL;
hr = InitWindowlessVMR(hwnd, pGraph, &g_pWc);
if (SUCCEEDED(hr))
{
    // Build the graph. For example:
    pGraph->RenderFile(wszMyFileName, 0);
    // Release the VMR interface when you are done.
    pWc->Release();
}
```



## <a name="position-the-video"></a><span data-ttu-id="f7dd7-145">定位影片</span><span class="sxs-lookup"><span data-stu-id="f7dd7-145">Position the Video</span></span>

<span data-ttu-id="f7dd7-146">設定 VMR 後，下一個步驟是設定影片的位置。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-146">After configuring the VMR, the next step is to set the position of the video.</span></span> <span data-ttu-id="f7dd7-147">有兩個要考慮的矩形： *來源* 矩形和 *目的地* 矩形。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-147">There are two rectangles to consider, the *source* rectangle and the *destination* rectangle.</span></span> <span data-ttu-id="f7dd7-148">來源矩形會定義影片中要顯示的部分。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-148">The source rectangle defines which portion of the video to display.</span></span> <span data-ttu-id="f7dd7-149">目的地矩形會在視窗的工作區中指定將包含影片的區域。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-149">The destination rectangle specifies the region in the window's client area that will contain the video.</span></span> <span data-ttu-id="f7dd7-150">VMR 會將影片影像裁剪至來源矩形，並伸展裁剪影像以符合目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-150">The VMR crops the video image to the source rectangle and stretches the cropped image to fit the destination rectangle.</span></span>

<span data-ttu-id="f7dd7-151">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="f7dd7-151">**VMR-7**</span></span>

1.  <span data-ttu-id="f7dd7-152">呼叫 [**IVMRWindowlessControl：： SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) 方法來指定這兩個矩形。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-152">Call the [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="f7dd7-153">來源矩形必須等於或小於原生影片大小;您可以使用 [**IVMRWindowlessControl：： GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) 方法來取得原生影片大小。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-153">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl::GetNativeVideoSize**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="f7dd7-154">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="f7dd7-154">**VMR-9**</span></span>

1.  <span data-ttu-id="f7dd7-155">呼叫 [**IVMRWindowlessControl9：： SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) 方法來指定這兩個矩形。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-155">Call the [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) method to specify both rectangles.</span></span>
2.  <span data-ttu-id="f7dd7-156">來源矩形必須等於或小於原生影片大小;您可以使用 [**IVMRWindowlessControl9：： GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) 方法來取得原生影片大小。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-156">The source rectangle must be equal to or smaller than the native video size; you can use the [**IVMRWindowlessControl9::GetNativeVideoSize**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-getnativevideosize) method to get the native video size.</span></span>

<span data-ttu-id="f7dd7-157">例如，下列程式碼會設定 VMR-7 的來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-157">For example, the following code sets the source and destination rectangles for the VMR-7.</span></span> <span data-ttu-id="f7dd7-158">它會將來源矩形設定為與整個影片影像相等，而目的地矩形等於整個視窗工作區：</span><span class="sxs-lookup"><span data-stu-id="f7dd7-158">It sets the source rectangle equal to the entire video image, and the destination rectangle equal to the entire window client area:</span></span>


```C++
// Find the native video size.
long lWidth, lHeight; 
HRESULT hr = g_pWc->GetNativeVideoSize(&lWidth, &lHeight, NULL, NULL); 
if (SUCCEEDED(hr))
{
    RECT rcSrc, rcDest; 
    // Set the source rectangle.
    SetRect(&rcSrc, 0, 0, lWidth, lHeight); 
    
    // Get the window client area.
    GetClientRect(hwnd, &rcDest); 
    // Set the destination rectangle.
    SetRect(&rcDest, 0, 0, rcDest.right, rcDest.bottom); 
    
    // Set the video position.
    hr = g_pWc->SetVideoPosition(&rcSrc, &rcDest); 
}
```



<span data-ttu-id="f7dd7-159">如果您想要讓影片佔用工作區的較小部分，請修改 *rcDest* 參數。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-159">If you want to video to occupy a smaller portion of the client area, modify the *rcDest* parameter.</span></span> <span data-ttu-id="f7dd7-160">如果您想要裁剪影片影像，請修改 *rcSrc* 參數。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-160">If you want to crop the video image, modify the *rcSrc* parameter.</span></span>

## <a name="handle-window-messages"></a><span data-ttu-id="f7dd7-161">處理視窗訊息</span><span class="sxs-lookup"><span data-stu-id="f7dd7-161">Handle Window Messages</span></span>

<span data-ttu-id="f7dd7-162">因為 VMR 沒有自己的視窗，所以如果需要重新繪製或調整影片的大小，就必須通知它。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-162">Because the VMR does not have its own window, it must be notified if it need to repaint or resize the video.</span></span> <span data-ttu-id="f7dd7-163">藉由呼叫所列出的 VMR 方法來回應下列視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-163">Respond to the following window messages by calling the VMR methods listed.</span></span>

<span data-ttu-id="f7dd7-164">**VMR-7**</span><span class="sxs-lookup"><span data-stu-id="f7dd7-164">**VMR-7**</span></span>

1.  <span data-ttu-id="f7dd7-165">[**WM \_繪製**](../gdi/wm-paint.md)。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-165">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="f7dd7-166">呼叫 [**IVMRWindowlessControl：： RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo)。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-166">Call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span> <span data-ttu-id="f7dd7-167">這個方法會導致 VMR-7 重新繪製最新的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-167">This method causes the VMR-7 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="f7dd7-168">[**WM \_DISPLAYCHANGE**](../gdi/wm-displaychange.md)： Call [**IVMRWindowlessControl：:D isplaymodechanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged)。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-168">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span> <span data-ttu-id="f7dd7-169">這個方法會通知 VMR-7 影片必須在新的解析度或色彩深度上顯示。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-169">This method notifies the VMR-7 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="f7dd7-170">[**WM \_大小**](../winmsg/wm-size.md) 或 [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md)：重新計算影片的位置並呼叫 [**IVMRWindowlessControl：： SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) ，以更新位置（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-170">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition) to update the position, if needed.</span></span>

<span data-ttu-id="f7dd7-171">**VMR-9**</span><span class="sxs-lookup"><span data-stu-id="f7dd7-171">**VMR-9**</span></span>

1.  <span data-ttu-id="f7dd7-172">[**WM \_繪製**](../gdi/wm-paint.md)。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-172">[**WM\_PAINT**](../gdi/wm-paint.md).</span></span> <span data-ttu-id="f7dd7-173">呼叫 [**IVMRWindowlessControl9：： RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo)。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-173">Call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span> <span data-ttu-id="f7dd7-174">這個方法會導致 VMR-9 重新繪製最新的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-174">This method causes the VMR-9 to repaint the most recent video frame.</span></span>
2.  <span data-ttu-id="f7dd7-175">[**WM \_DISPLAYCHANGE**](../gdi/wm-displaychange.md)： Call [**IVMRWindowlessControl9：:D isplaymodechanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged)。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-175">[**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md): Call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span> <span data-ttu-id="f7dd7-176">這個方法會通知 VMR-9 影片必須以新的解析度或色彩深度顯示。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-176">This method notifies the VMR-9 that the video must be shown at a new resolution or color depth.</span></span>
3.  <span data-ttu-id="f7dd7-177">[**WM \_大小**](../winmsg/wm-size.md) 或 [**WM \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md)：重新計算影片的位置並呼叫 [**IVMRWindowlessControl9：： SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) ，以更新位置（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-177">[**WM\_SIZE**](../winmsg/wm-size.md) or [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md): Recalculate the position of the video and call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition) to update the position, if needed.</span></span>

> [!Note]  
> <span data-ttu-id="f7dd7-178">[**Wm \_ WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md)訊息的預設處理常式會傳送 [**wm \_ 大小**](../winmsg/wm-size.md)的訊息。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-178">The default handler for the [**WM\_WINDOWPOSCHANGED**](../winmsg/wm-windowposchanged.md) message sends a [**WM\_SIZE**](../winmsg/wm-size.md) message.</span></span> <span data-ttu-id="f7dd7-179">但是，如果您的應用程式會攔截 **wm \_ WINDOWPOSCHANGED** ，而不將它傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)，您應該在 **Wm \_ WINDOWPOSCHANGED** 處理常式中呼叫 **SetVideoPosition** ，除了您的 **wm \_ 大小** 處理常式。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-179">But if your application intercepts **WM\_WINDOWPOSCHANGED** and does not pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), you should call **SetVideoPosition** in your **WM\_WINDOWPOSCHANGED** handler, in addition to your **WM\_SIZE** handler.</span></span>

 

<span data-ttu-id="f7dd7-180">下列範例顯示 [**WM \_ 油漆**](../gdi/wm-paint.md) 訊息處理常式。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-180">The following example shows a [**WM\_PAINT**](../gdi/wm-paint.md) message handler.</span></span> <span data-ttu-id="f7dd7-181">它會繪製用戶端矩形所定義的區域減去影片矩形。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-181">It paints a region defined by the client rectangle minus the video rectangle.</span></span> <span data-ttu-id="f7dd7-182">請勿在影片矩形上繪製，因為 VMR 會在其上繪製，導致閃爍。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-182">Do not draw onto the video rectangle, because the VMR will paint over it, causing flickering.</span></span> <span data-ttu-id="f7dd7-183">基於相同的原因，請勿在視窗類別中設定背景筆刷。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-183">For the same reason, do not set a background brush in your window class.</span></span>


```C++
void OnPaint(HWND hwnd) 
{ 
    PAINTSTRUCT ps; 
    HDC         hdc; 
    RECT        rcClient; 
    GetClientRect(hwnd, &rcClient); 
    hdc = BeginPaint(hwnd, &ps); 
    if (g_pWc != NULL) 
    { 
        // Find the region where the application can paint by subtracting 
        // the video destination rectangle from the client area.
        // (Assume that g_rcDest was calculated previously.)
        HRGN rgnClient = CreateRectRgnIndirect(&rcClient); 
        HRGN rgnVideo  = CreateRectRgnIndirect(&g_rcDest);  
        CombineRgn(rgnClient, rgnClient, rgnVideo, RGN_DIFF);  
        
        // Paint on window.
        HBRUSH hbr = GetSysColorBrush(COLOR_BTNFACE); 
        FillRgn(hdc, rgnClient, hbr); 

        // Clean up.
        DeleteObject(hbr); 
        DeleteObject(rgnClient); 
        DeleteObject(rgnVideo); 

        // Request the VMR to paint the video.
        HRESULT hr = g_pWc->RepaintVideo(hwnd, hdc);  
    } 
    else  // There is no video, so paint the whole client area. 
    { 
        FillRect(hdc, &rc2, (HBRUSH)(COLOR_BTNFACE + 1)); 
    } 
    EndPaint(hwnd, &ps); 
} 
```



<span data-ttu-id="f7dd7-184">雖然您必須回應 [**wm \_ 油漆**](../gdi/wm-paint.md) 訊息，但您不需要在 **wm \_ 油漆** 訊息之間執行任何動作來更新影片。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-184">Although you must respond to [**WM\_PAINT**](../gdi/wm-paint.md) messages, there is nothing you need to do between **WM\_PAINT** messages to update the video.</span></span> <span data-ttu-id="f7dd7-185">如這個範例所示，無視窗模式可讓您將影片影像視為視窗上的自我繪圖區域。</span><span class="sxs-lookup"><span data-stu-id="f7dd7-185">As this example shows, windowless mode lets you treat the video image simply as a self-drawing region on the window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7dd7-186">相關主題</span><span class="sxs-lookup"><span data-stu-id="f7dd7-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7dd7-187">使用影片混合轉譯器</span><span class="sxs-lookup"><span data-stu-id="f7dd7-187">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="f7dd7-188">影片轉譯</span><span class="sxs-lookup"><span data-stu-id="f7dd7-188">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
