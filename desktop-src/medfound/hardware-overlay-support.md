---
description: 說明如何在 Direct3D 9 中使用硬體覆蓋。
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: 硬體覆蓋支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcae33cdf55de59bdcd074829d52b4c1c43ea5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988683"
---
# <a name="hardware-overlay-support"></a><span data-ttu-id="0bbaf-103">硬體覆蓋支援</span><span class="sxs-lookup"><span data-stu-id="0bbaf-103">Hardware Overlay Support</span></span>

<span data-ttu-id="0bbaf-104">硬體重迭是視訊記憶體的私人區域，可在主要介面上重迭。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-104">A hardware overlay is a dedicated area of video memory that can be overlayed on the primary surface.</span></span> <span data-ttu-id="0bbaf-105">當重迭顯示時，不會執行任何複製。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-105">No copy is performed when the overlay is displayed.</span></span> <span data-ttu-id="0bbaf-106">覆迭作業是在硬體中執行，而不需要修改主要介面中的資料。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-106">The overlay operation is performed in hardware, without modifying the data in the primary surface.</span></span>

<span data-ttu-id="0bbaf-107">使用硬體重迭來播放影片在舊版 Windows 中很常見，因為重迭對於具有高畫面播放速率的影片內容而言很有效率。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-107">The use of hardware overlays for video playback was common in earlier versions of Windows, because overlays are efficient for video content with a high frame rate.</span></span> <span data-ttu-id="0bbaf-108">從 Windows 7 開始，Direct3D 9 支援硬體覆蓋。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-108">Starting in Windows 7, Direct3D 9 supports hardware overlays.</span></span> <span data-ttu-id="0bbaf-109">這項支援主要是為了播放影片，而且與舊版 DirectDraw Api 的部分不同：</span><span class="sxs-lookup"><span data-stu-id="0bbaf-109">This support is intended primarily for video playback, and differs in some respects from earlier DirectDraw APIs:</span></span>

-   <span data-ttu-id="0bbaf-110">無法壓縮、鏡像或 deinterlaced 重迭。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-110">The overlay cannot be shrunk, mirrored, or deinterlaced.</span></span>
-   <span data-ttu-id="0bbaf-111">不支援來源色彩索引鍵和 Alpha 混色。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-111">Source color keys and alpha blending are not supported.</span></span>
-   <span data-ttu-id="0bbaf-112">如果重迭硬體支援重迭，則重迭可能會延長。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-112">Overlays can be stretched if the overlay hardware supports it.</span></span> <span data-ttu-id="0bbaf-113">否則，不支援延展。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-113">Otherwise, stretching is not supported.</span></span> <span data-ttu-id="0bbaf-114">在實務上，並非所有圖形驅動程式都支援伸展。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-114">In practice, not all graphics drivers support stretching.</span></span>
-   <span data-ttu-id="0bbaf-115">每個裝置最多支援一個重迭。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-115">Each device supports at most one overlay.</span></span>
-   <span data-ttu-id="0bbaf-116">重迭是使用目的色鍵來執行，但是 Direct3D runtime 會自動選取色彩並繪製目的矩形。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-116">Overlay is performed using a destination color key, but the Direct3D runtime automatically selects the color and draws the destination rectangle.</span></span> <span data-ttu-id="0bbaf-117">Direct3D 會自動追蹤視窗的位置，並在每次呼叫 **PresentEx** 時更新覆迭的位置。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-117">Direct3D automatically tracks the position of the window and updates the overlay position whenever the **PresentEx** is called.</span></span>

### <a name="creating-a-hardware-overlay-surface"></a><span data-ttu-id="0bbaf-118">建立硬體重迭表面</span><span class="sxs-lookup"><span data-stu-id="0bbaf-118">Creating a Hardware Overlay Surface</span></span>

<span data-ttu-id="0bbaf-119">若要查詢重迭支援，請呼叫 **IDirect3D9：： GetDeviceCaps**。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-119">To query for overlay support, call **IDirect3D9::GetDeviceCaps**.</span></span> <span data-ttu-id="0bbaf-120">如果驅動程式支援硬體重迭，則會在 D3DCAPS9 中設定 D3DCAPS 重迭旗標 **\_** **。Caps** 成員。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-120">If the driver supports hardware overlay, the **D3DCAPS\_OVERLAY** flag is set in the **D3DCAPS9.Caps** member.</span></span>

<span data-ttu-id="0bbaf-121">若要瞭解給定的顯示模式是否支援特定的重迭格式，請呼叫 [**IDirect3D9ExOverlayExtension：： CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype)。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-121">To find out whether a specific overlay format is supported for a given display mode, call [**IDirect3D9ExOverlayExtension::CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).</span></span>

<span data-ttu-id="0bbaf-122">若要建立覆迭，請呼叫 **IDirect3D9Ex：： CreateDeviceEx** ，並指定 D3DSWAPEFFECT 重迭交換效果。 **\_**</span><span class="sxs-lookup"><span data-stu-id="0bbaf-122">To create the overlay, call **IDirect3D9Ex::CreateDeviceEx** and specify the **D3DSWAPEFFECT\_OVERLAY** swap effect.</span></span> <span data-ttu-id="0bbaf-123">如果硬體支援，則背景緩衝區可以使用非 RGB 格式。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-123">The back buffer can use a non-RGB format if the hardware supports it.</span></span>

<span data-ttu-id="0bbaf-124">重迭表面有下列限制：</span><span class="sxs-lookup"><span data-stu-id="0bbaf-124">Overlay surfaces have the following limitations:</span></span>

-   <span data-ttu-id="0bbaf-125">應用程式無法建立一個以上的重迭交換鏈。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-125">The application cannot create more than one overlay swap chain.</span></span>
-   <span data-ttu-id="0bbaf-126">重迭必須在視窗模式中使用。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-126">The overlay must be used in windowed mode.</span></span> <span data-ttu-id="0bbaf-127">無法在全螢幕模式中使用。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-127">It cannot be used in fullscreen mode.</span></span>
-   <span data-ttu-id="0bbaf-128">重迭交換效果必須搭配 **IDirect3DDevice9Ex** 介面使用。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-128">The overlay swap effect must be used with the **IDirect3DDevice9Ex** interface.</span></span> <span data-ttu-id="0bbaf-129">**IDirect3DDevice9** 不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-129">It is not supported for **IDirect3DDevice9**.</span></span>
-   <span data-ttu-id="0bbaf-130">無法使用多級取樣。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-130">Multisampling cannot be used.</span></span>
-   <span data-ttu-id="0bbaf-131">不支援 **D3DPRESENT \_ DONOTFLIP** 和 **D3DPRESENT \_ FLIPRESTART** 旗標。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-131">The **D3DPRESENT\_DONOTFLIP** and **D3DPRESENT\_FLIPRESTART** flags are not supported.</span></span>
-   <span data-ttu-id="0bbaf-132">無法針對重迭表面使用簡報統計資料。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-132">Presentation statistics are not available for the overlay surface.</span></span>

<span data-ttu-id="0bbaf-133">如果硬體不支援延展，建議您建立與顯示模式大的交換鏈，讓視窗可以調整大小為任何維度。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-133">If the hardware does not support stretching, it is recommended to create a swap chain as large as the display mode, so that the window can be resized to any dimensions.</span></span> <span data-ttu-id="0bbaf-134">重新建立交換鏈並不是處理調整視窗大小的最佳方式，因為這可能會造成嚴重的轉譯成品。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-134">Recreating the swap chain is not an optimal way to handle resizing the window, because it can cause severe rendering artifacts.</span></span> <span data-ttu-id="0bbaf-135">此外，由於 GPU 管理覆迭記憶體的方式，重新建立交換鏈可能會導致應用程式用盡視頻記憶體。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-135">Also, because of the way the GPU manages the overlay memory, recreating the swap chain can potentially cause an application to run out of video memory.</span></span>

### <a name="new-d3dpresent_parameters-flags"></a><span data-ttu-id="0bbaf-136">新的 D3DPRESENT \_ 參數旗標</span><span class="sxs-lookup"><span data-stu-id="0bbaf-136">New D3DPRESENT\_PARAMETERS Flags</span></span>

<span data-ttu-id="0bbaf-137">下列 **D3DPRESENT \_ 參數** 旗標是針對建立覆迭而定義的。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-137">The following **D3DPRESENT\_PARAMETERS** flags are defined for creating overlays.</span></span>



| <span data-ttu-id="0bbaf-138">旗標</span><span class="sxs-lookup"><span data-stu-id="0bbaf-138">Flag</span></span>                                      | <span data-ttu-id="0bbaf-139">描述</span><span class="sxs-lookup"><span data-stu-id="0bbaf-139">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbaf-140">**D3DPRESENTFLAG 重迭 \_ \_ LIMITEDRGB**</span><span class="sxs-lookup"><span data-stu-id="0bbaf-140">**D3DPRESENTFLAG\_OVERLAY\_LIMITEDRGB**</span></span>   | <span data-ttu-id="0bbaf-141">RGB 範圍是16–235。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-141">The RGB range is 16–235.</span></span> <span data-ttu-id="0bbaf-142">預設值為0–255。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-142">The default is 0–255.</span></span> <br/> <span data-ttu-id="0bbaf-143">需要 **D3DOVERLAYCAPS \_ LIMITEDRANGERGB** 功能。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-143">Requires the **D3DOVERLAYCAPS\_LIMITEDRANGERGB** capability.</span></span><br/>                                                 |
| <span data-ttu-id="0bbaf-144">**D3DPRESENTFLAG 重迭 \_ \_ YCbCr \_ BT709**</span><span class="sxs-lookup"><span data-stu-id="0bbaf-144">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_BT709**</span></span> | <span data-ttu-id="0bbaf-145">YUV 色彩使用709定義。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-145">YUV colors use the BT.709 definition.</span></span> <span data-ttu-id="0bbaf-146">預設值為 BT. 601。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-146">The default is BT.601.</span></span> <br/> <span data-ttu-id="0bbaf-147">需要 **D3DOVERLAYCAPS \_ YCbCr \_ BT709** 功能。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-147">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT709** capability.</span></span><br/>                                      |
| <span data-ttu-id="0bbaf-148">**D3DPRESENTFLAG 重迭 \_ \_ YCbCr \_ xvYCC**</span><span class="sxs-lookup"><span data-stu-id="0bbaf-148">**D3DPRESENTFLAG\_OVERLAY\_YCbCr\_xvYCC**</span></span> | <span data-ttu-id="0bbaf-149">使用外延 YCbCr (xvYCC) 輸出資料。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-149">Output the data by using extended YCbCr (xvYCC).</span></span><br/> <span data-ttu-id="0bbaf-150">需要 **D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ xvYCC** 或 **D3DOVERLAYCAPS \_ YCbCr \_ BT709 \_ xvYCC** 的功能。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-150">Requires the **D3DOVERLAYCAPS\_YCbCr\_BT601\_xvYCC** or **D3DOVERLAYCAPS\_YCbCr\_BT709\_xvYCC** capability.</span></span><br/> |



 

### <a name="using-hardware-overlays"></a><span data-ttu-id="0bbaf-151">使用硬體覆蓋</span><span class="sxs-lookup"><span data-stu-id="0bbaf-151">Using Hardware Overlays</span></span>

<span data-ttu-id="0bbaf-152">為了顯示重迭表面，應用程式會呼叫 **IDirect3DDevice9Ex：:P resentex**。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-152">To display the overlay surface, the application calls **IDirect3DDevice9Ex::PresentEx**.</span></span> <span data-ttu-id="0bbaf-153">Direct3D runtime 會自動繪製目的色鍵。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-153">The Direct3D runtime automatically draws the destination color key.</span></span>

<span data-ttu-id="0bbaf-154">以下是針對重迭定義的 **PresentEx** 旗標。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-154">The following **PresentEx** flags are defined for overlays.</span></span>



| <span data-ttu-id="0bbaf-155">旗標</span><span class="sxs-lookup"><span data-stu-id="0bbaf-155">Flag</span></span>                              | <span data-ttu-id="0bbaf-156">描述</span><span class="sxs-lookup"><span data-stu-id="0bbaf-156">Description</span></span>                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bbaf-157">**D3DPRESENT \_ UPDATECOLORKEY**</span><span class="sxs-lookup"><span data-stu-id="0bbaf-157">**D3DPRESENT\_UPDATECOLORKEY**</span></span>    | <span data-ttu-id="0bbaf-158">如果桌面視窗管理員 (DWM) 組合已停用，請設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-158">Set this flag if Desktop Window Manager (DWM) composition is disabled.</span></span> <span data-ttu-id="0bbaf-159">此旗標會導致 Direct3D 重繪色彩索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-159">This flag causes Direct3D to redraw the color key.</span></span><br/> <span data-ttu-id="0bbaf-160">如果已啟用 DWM，則不需要此旗標，因為 Direct3D 會在 DWM 用來重新導向的介面上繪製一次色彩鍵。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-160">If DWM is enabled, this flag is not required, because Direct3D draws the color key once on the surface that DWM uses for redirection.</span></span><br/> |
| <span data-ttu-id="0bbaf-161">**D3DPRESENT \_ HIDEOVERLAY**</span><span class="sxs-lookup"><span data-stu-id="0bbaf-161">**D3DPRESENT\_HIDEOVERLAY**</span></span>       | <span data-ttu-id="0bbaf-162">隱藏覆迭。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-162">Hides the overlay.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="0bbaf-163">**D3DPRESENT \_ UPDATEOVERLAYONLY**</span><span class="sxs-lookup"><span data-stu-id="0bbaf-163">**D3DPRESENT\_UPDATEOVERLAYONLY**</span></span> | <span data-ttu-id="0bbaf-164">更新覆迭而不變更內容。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-164">Updates the overlay without changing the contents.</span></span><br/> <span data-ttu-id="0bbaf-165">如果視窗在影片暫停時移動，這個旗標就很有用。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-165">This flag is useful if the window moves while the video is paused.</span></span><br/>                                                                                                                                           |



 

<span data-ttu-id="0bbaf-166">應用程式應該準備好處理下列案例：</span><span class="sxs-lookup"><span data-stu-id="0bbaf-166">An application should be prepared to handle the following cases:</span></span>

-   <span data-ttu-id="0bbaf-167">如果另一個應用程式正在使用覆迭， **PresentEx** 會傳回 **D3DERR \_ NOTAVAILABLE**。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-167">If another application is using the overlay, **PresentEx** returns **D3DERR\_NOTAVAILABLE**.</span></span>
-   <span data-ttu-id="0bbaf-168">如果將視窗移到另一個監視器，應用程式必須重新建立交換鏈。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-168">If the window is moved to another monitor, the application must recreate the swap chain.</span></span> <span data-ttu-id="0bbaf-169">否則，若應用程式呼叫 **PresentEx** 以在不同的監視器上顯示覆迭，則 **PresentEx** 會傳回 **D3DERR \_ INVALIDDEVICE**。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-169">Otherwise, if the application calls **PresentEx** to display the overlay on a different monitor, **PresentEx** returns **D3DERR\_INVALIDDEVICE**.</span></span>
-   <span data-ttu-id="0bbaf-170">如果顯示模式變更，Direct3D 會嘗試還原覆迭。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-170">If the display mode changes, Direct3D attempts to restore the overlay.</span></span> <span data-ttu-id="0bbaf-171">如果新的模式不支援重迭， **PresentEx** 會傳回 **D3DERR \_ UNSUPPORTEDOVERLAY**。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-171">If the new mode does not support the overlay, **PresentEx** returns **D3DERR\_UNSUPPORTEDOVERLAY**.</span></span>

### <a name="example-code"></a><span data-ttu-id="0bbaf-172">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="0bbaf-172">Example Code</span></span>

<span data-ttu-id="0bbaf-173">下列範例顯示如何建立重迭表面。</span><span class="sxs-lookup"><span data-stu-id="0bbaf-173">The following example shows how to create an overlay surface.</span></span>


```C++
const UINT VIDEO_WIDTH = 256;
const UINT VIDEO_HEIGHT = 256;

HRESULT CreateHWOverlay(
    HWND hwnd, 
    IDirect3D9Ex *pD3D, 
    IDirect3DDevice9Ex **ppDevice
    )
{
    *ppDevice = NULL;

    D3DCAPS9                caps;
    ZeroMemory(&caps, sizeof(caps));

    HRESULT hr = pD3D->GetDeviceCaps(
        D3DADAPTER_DEFAULT,
        D3DDEVTYPE_HAL,
        &caps
        );

    if (FAILED(hr))
    {
        return hr;
    }

    // Check if overlay is supported.
    if (!(caps.Caps & D3DCAPS_OVERLAY))
    {
        return D3DERR_UNSUPPORTEDOVERLAY;
    }

    D3DOVERLAYCAPS          overlayCaps = { 0 };

    IDirect3DDevice9Ex           *pDevice = NULL;
    IDirect3D9ExOverlayExtension *pOverlay = NULL;

    // Check specific overlay capabilities.
    hr = pD3D->QueryInterface(IID_PPV_ARGS(&pOverlay));

    if (SUCCEEDED(hr))
    {
        hr = pOverlay->CheckDeviceOverlayType(
            D3DADAPTER_DEFAULT,
            D3DDEVTYPE_HAL,
            VIDEO_WIDTH,
            VIDEO_HEIGHT,
            D3DFMT_X8R8G8B8,
            NULL,
            D3DDISPLAYROTATION_IDENTITY,
            &overlayCaps
            );
    }

    // Create the overlay.
    if (SUCCEEDED(hr))
    {

        DWORD flags =   D3DCREATE_FPU_PRESERVE | 
                        D3DCREATE_MULTITHREADED | 
                        D3DCREATE_SOFTWARE_VERTEXPROCESSING;

        
        D3DPRESENT_PARAMETERS   pp = { 0 };

        pp.BackBufferWidth = overlayCaps.MaxOverlayDisplayWidth;
        pp.BackBufferHeight = overlayCaps.MaxOverlayDisplayHeight;
        pp.BackBufferFormat = D3DFMT_X8R8G8B8;
        pp.SwapEffect = D3DSWAPEFFECT_OVERLAY;
        pp.hDeviceWindow = hwnd;
        pp.Windowed = TRUE;
        pp.Flags = D3DPRESENTFLAG_VIDEO;
        pp.FullScreen_RefreshRateInHz = D3DPRESENT_RATE_DEFAULT;
        pp.PresentationInterval       = D3DPRESENT_INTERVAL_ONE;

        hr = pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL,
            NULL, flags, &pp, NULL, &pDevice);
    }

    if (SUCCEEDED(hr))
    {
        (*ppDevice) = pDevice;
        (*ppDevice)->AddRef();
    }

    SafeRelease(&pD3D);
    SafeRelease(&pDevice);
    SafeRelease(&pOverlay);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="0bbaf-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="0bbaf-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bbaf-175">Direct3D 影片 Api</span><span class="sxs-lookup"><span data-stu-id="0bbaf-175">Direct3D Video APIs</span></span>](direct3d-video-apis.md)
</dt> </dl>

 

 




