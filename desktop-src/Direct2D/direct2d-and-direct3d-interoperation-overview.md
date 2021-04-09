---
title: Direct2D 和 Direct3D 互通性概觀
description: .
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- Direct2D，Direct3D 互通性
- Direct2D，互通性
- 互通性，Direct2D
- 互通性，Direct3D
- Direct3D、互通性
- Direct3D、Direct2D 互通性
- Direct2D，DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6854481ec2a8d869467aa912252e3649e17f2501
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2020
ms.locfileid: "104093471"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a><span data-ttu-id="0b0af-111">Direct2D 和 Direct3D 互通性概觀</span><span class="sxs-lookup"><span data-stu-id="0b0af-111">Direct2D and Direct3D Interoperability Overview</span></span>

<span data-ttu-id="0b0af-112">硬體加速的2D 和3D 圖形逐漸成為非遊戲應用程式的一部分，而大部分的遊戲應用程式都是以功能表的形式使用2D 圖形，Heads-Up 會顯示 (的 HUDs) 。</span><span class="sxs-lookup"><span data-stu-id="0b0af-112">Hardware accelerated 2-D and 3-D graphics are increasingly becoming a part of non-gaming applications, and most gaming applications use 2-D graphics in the form of menus and Heads-Up Displays (HUDs).</span></span> <span data-ttu-id="0b0af-113">您可以藉由啟用傳統的2D 轉譯，以有效率的方式與 Direct3D 轉譯混合，來新增許多值。</span><span class="sxs-lookup"><span data-stu-id="0b0af-113">There is lots of value that can be added by enabling traditional 2-D rendering to be mixed with Direct3D rendering in an efficient manner.</span></span>

<span data-ttu-id="0b0af-114">本主題說明如何使用 Direct2D 和 [Direct3D](../graphics-and-multimedia.md)來整合2D 和3d 圖形。</span><span class="sxs-lookup"><span data-stu-id="0b0af-114">This topic describes how to integrate 2-D and 3-D graphics by using Direct2D and [Direct3D](../graphics-and-multimedia.md).</span></span>

<span data-ttu-id="0b0af-115">包含以下幾節。</span><span class="sxs-lookup"><span data-stu-id="0b0af-115">It contains the following sections.</span></span>

-   [<span data-ttu-id="0b0af-116">先決條件</span><span class="sxs-lookup"><span data-stu-id="0b0af-116">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="0b0af-117">支援的 Direct3D 版本</span><span class="sxs-lookup"><span data-stu-id="0b0af-117">Supported Direct3D Versions</span></span>](#supported-direct3d-versions)
-   [<span data-ttu-id="0b0af-118">透過 DXGI 的互通性</span><span class="sxs-lookup"><span data-stu-id="0b0af-118">Interoperability Through DXGI</span></span>](#interoperability-through-dxgi)
-   [<span data-ttu-id="0b0af-119">使用 DXGI 介面轉譯目標寫入至 Direct3D 介面</span><span class="sxs-lookup"><span data-stu-id="0b0af-119">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [<span data-ttu-id="0b0af-120">建立 DXGI 介面</span><span class="sxs-lookup"><span data-stu-id="0b0af-120">Creating a DXGI Surface</span></span>](#creating-a-dxgi-surface)
-   [<span data-ttu-id="0b0af-121">將 Direct2D 內容寫入交換鏈緩衝區</span><span class="sxs-lookup"><span data-stu-id="0b0af-121">Writing Direct2D Content to a Swap Chain Buffer</span></span>](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [<span data-ttu-id="0b0af-122">範例：繪製2D 背景</span><span class="sxs-lookup"><span data-stu-id="0b0af-122">Example: Draw a 2-D Background</span></span>](#example-draw-a-2-d-background)
-   [<span data-ttu-id="0b0af-123">使用 Direct2D 內容作為材質</span><span class="sxs-lookup"><span data-stu-id="0b0af-123">Using Direct2D Content as a Texture</span></span>](#using-direct2d-content-as-a-texture)
    -   [<span data-ttu-id="0b0af-124">範例：使用 Direct2D 內容作為材質</span><span class="sxs-lookup"><span data-stu-id="0b0af-124">Example: Use Direct2D Content as a Texture</span></span>](#example-use-direct2d-content-as-a-texture)
-   [<span data-ttu-id="0b0af-125">調整 DXGI 介面呈現目標的大小</span><span class="sxs-lookup"><span data-stu-id="0b0af-125">Resizing a DXGI Surface Render Target</span></span>](#resizing-a-dxgi-surface-render-target)
-   [<span data-ttu-id="0b0af-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b0af-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="0b0af-127">必要條件</span><span class="sxs-lookup"><span data-stu-id="0b0af-127">Prerequisites</span></span>

<span data-ttu-id="0b0af-128">本總覽假設您已經熟悉基本的 Direct2D 繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="0b0af-128">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="0b0af-129">如需教學課程，請參閱 [Direct2D 快速入門](direct2d-quickstart.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0af-129">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="0b0af-130">它也假設您可以使用 [Direct3D 10.1](/windows/desktop/direct3d10/d3d10-graphics)進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="0b0af-130">It also assumes that you can program by using [Direct3D 10.1](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

## <a name="supported-direct3d-versions"></a><span data-ttu-id="0b0af-131">支援的 Direct3D 版本</span><span class="sxs-lookup"><span data-stu-id="0b0af-131">Supported Direct3D Versions</span></span>

<span data-ttu-id="0b0af-132">使用 DirectX 11.0 時，Direct2D 僅支援與 Direct3D 10.1 裝置的互通性。</span><span class="sxs-lookup"><span data-stu-id="0b0af-132">With DirectX 11.0, Direct2D supports interoperability with Direct3D 10.1 devices only.</span></span> <span data-ttu-id="0b0af-133">使用 DirectX 11.1 或更新版本時，Direct2D 也支援與 Direct3D 11 之間的互通性。</span><span class="sxs-lookup"><span data-stu-id="0b0af-133">With DirectX 11.1 or later, Direct2D supports interoperability with Direct3D 11 as well.</span></span>

## <a name="interoperability-through-dxgi"></a><span data-ttu-id="0b0af-134">透過 DXGI 的互通性</span><span class="sxs-lookup"><span data-stu-id="0b0af-134">Interoperability Through DXGI</span></span>

<span data-ttu-id="0b0af-135">從 Direct3D 10，Direct3D 執行時間會使用 [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) 進行資源管理。</span><span class="sxs-lookup"><span data-stu-id="0b0af-135">As of Direct3D 10, the Direct3D runtime uses [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) for resource management.</span></span> <span data-ttu-id="0b0af-136">DXGI 執行時間層提供了影片記憶體表面的跨進程共用，並作為其他視訊記憶體執行時間平臺的基礎。</span><span class="sxs-lookup"><span data-stu-id="0b0af-136">The DXGI runtime layer provides cross-process sharing of video memory surfaces and serves as the foundation for other video memory-based runtime platforms.</span></span> <span data-ttu-id="0b0af-137">Direct2D 會使用 DXGI 來與 Direct3D 交互操作。</span><span class="sxs-lookup"><span data-stu-id="0b0af-137">Direct2D uses DXGI to interoperate with Direct3D.</span></span>

<span data-ttu-id="0b0af-138">有兩種主要方式可搭配使用 Direct2D 和 Direct3D：</span><span class="sxs-lookup"><span data-stu-id="0b0af-138">There are two primary ways to use Direct2D and Direct3D together:</span></span>

-   <span data-ttu-id="0b0af-139">您可以藉由取得 [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) 並使用 [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) 來建立 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)，將 Direct2D 內容寫入至 Direct3D 介面。</span><span class="sxs-lookup"><span data-stu-id="0b0af-139">You can write Direct2D content to a Direct3D surface by obtaining an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and using it with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="0b0af-140">然後，您可以使用轉譯目標將二維介面或背景新增至三維圖形，或使用 Direct2D 繪圖作為三維度物件的材質。</span><span class="sxs-lookup"><span data-stu-id="0b0af-140">You can then use the render target to add a two-dimensional interface or background to three-dimensional graphics, or use a Direct2D drawing as a texture for a three dimensional object.</span></span>
-   <span data-ttu-id="0b0af-141">藉由使用 [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)來建立 [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ，您可以將 Direct3D 場景寫入點陣圖，並使用 Direct2D 來呈現。</span><span class="sxs-lookup"><span data-stu-id="0b0af-141">By using [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) from an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface), you can write a Direct3D scene to a bitmap and render it with Direct2D.</span></span>

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a><span data-ttu-id="0b0af-142">使用 DXGI 介面轉譯目標寫入至 Direct3D 介面</span><span class="sxs-lookup"><span data-stu-id="0b0af-142">Writing to a Direct3D Surface with a DXGI Surface Render Target</span></span>

<span data-ttu-id="0b0af-143">若要寫入 Direct3D 介面，您可以取得 [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) 並將它傳遞至 [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) 方法，以建立 DXGI 介面轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="0b0af-143">To write to a Direct3D surface, you obtain an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) and pass it to the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create a DXGI surface render target.</span></span> <span data-ttu-id="0b0af-144">然後，您可以使用 DXGI 介面轉譯目標，將2D 內容繪製到 DXGI 表面。</span><span class="sxs-lookup"><span data-stu-id="0b0af-144">You can then use the DXGI surface render target to draw 2-D content to the DXGI surface.</span></span>

<span data-ttu-id="0b0af-145">DXGI 介面轉譯目標是一種 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)。</span><span class="sxs-lookup"><span data-stu-id="0b0af-145">A DXGI surface render target is a kind of [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span> <span data-ttu-id="0b0af-146">如同其他 Direct2D 轉譯目標，您可以使用它來建立資源和發出繪製命令。</span><span class="sxs-lookup"><span data-stu-id="0b0af-146">Like other Direct2D render targets, you can use it to create resources and issue drawing commands.</span></span>

<span data-ttu-id="0b0af-147">DXGI 介面轉譯目標和 DXGI 介面必須使用相同的 DXGI 格式。</span><span class="sxs-lookup"><span data-stu-id="0b0af-147">The DXGI surface render target and the DXGI surface must use the same DXGI format.</span></span> <span data-ttu-id="0b0af-148">如果您在建立轉譯目標時指定 [**DXGI \_ 格式 \_ 未知**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式，它會自動使用介面的格式。</span><span class="sxs-lookup"><span data-stu-id="0b0af-148">If you specify the [**DXGI\_FORMAT\_UNKOWN**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format when you create the render target, it will automatically use the surface's format.</span></span>

<span data-ttu-id="0b0af-149">DXGI 介面轉譯目標不會執行 DXGI 介面同步處理。</span><span class="sxs-lookup"><span data-stu-id="0b0af-149">The DXGI surface render target does not perform DXGI surface synchronization.</span></span>

### <a name="creating-a-dxgi-surface"></a><span data-ttu-id="0b0af-150">建立 DXGI 介面</span><span class="sxs-lookup"><span data-stu-id="0b0af-150">Creating a DXGI Surface</span></span>

<span data-ttu-id="0b0af-151">使用 Direct3D 10 時，有數種方式可取得 DXGI 介面。</span><span class="sxs-lookup"><span data-stu-id="0b0af-151">With Direct3D 10, there are several ways to obtain a DXGI surface.</span></span> <span data-ttu-id="0b0af-152">您可以建立裝置的 [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) ，然後使用交換鏈的 [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) 方法來取得 DXGI 表面。</span><span class="sxs-lookup"><span data-stu-id="0b0af-152">You can create an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) for a device, then use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span> <span data-ttu-id="0b0af-153">或者，您可以使用裝置來建立材質，然後使用該材質作為 DXGI 表面。</span><span class="sxs-lookup"><span data-stu-id="0b0af-153">Or, you can use a device to create a texture, then use that texture as a DXGI surface.</span></span>

<span data-ttu-id="0b0af-154">無論您如何建立 DXGI 介面，介面都必須使用 DXGI 介面轉譯目標所支援的其中一個 DXGI 格式。</span><span class="sxs-lookup"><span data-stu-id="0b0af-154">Regardless of how you create the DXGI surface, the surface must use one of the DXGI formats supported by DXGI surface render targets.</span></span> <span data-ttu-id="0b0af-155">如需清單，請參閱 [支援的像素格式和 Alpha 模式](supported-pixel-formats-and-alpha-modes.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0af-155">For a list, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

<span data-ttu-id="0b0af-156">此外，與 DXGI 介面相關聯的 [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) 必須支援 BGRA DXGI 格式，才能讓介面與 Direct2D 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="0b0af-156">Additionally, the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the DXGI surface must support BGRA DXGI formats for the surface to work with Direct2D.</span></span> <span data-ttu-id="0b0af-157">若要確保此支援，請在呼叫 [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1)方法來建立裝置時，使用 [**D3D10 \_ create \_ device \_ BGRA \_ support**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag)旗標。</span><span class="sxs-lookup"><span data-stu-id="0b0af-157">To ensure this support, use the [**D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag when you call the [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) method to create the device.</span></span>

<span data-ttu-id="0b0af-158">下列程式碼會定義建立 [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1)的方法。</span><span class="sxs-lookup"><span data-stu-id="0b0af-158">The following code defines a method that creates an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1).</span></span> <span data-ttu-id="0b0af-159">它會選取可用的最佳功能等級，並在硬體轉譯無法使用時，切換回 [Windows Advanced 點陣化平臺 (變形) ](./installing-the-direct2d-debug-layer.md) 。</span><span class="sxs-lookup"><span data-stu-id="0b0af-159">It selects the best feature level available and falls back to [Windows Advanced Rasterization Platform (WARP)](./installing-the-direct2d-debug-layer.md) when hardware rendering is not available.</span></span>


```C++
HRESULT DXGISampleApp::CreateD3DDevice(
    IDXGIAdapter *pAdapter,
    D3D10_DRIVER_TYPE driverType,
    UINT flags,
    ID3D10Device1 **ppDevice
    )
{
    HRESULT hr = S_OK;

    static const D3D10_FEATURE_LEVEL1 levelAttempts[] =
    {
        D3D10_FEATURE_LEVEL_10_0,
        D3D10_FEATURE_LEVEL_9_3,
        D3D10_FEATURE_LEVEL_9_2,
        D3D10_FEATURE_LEVEL_9_1,
    };

    for (UINT level = 0; level < ARRAYSIZE(levelAttempts); level++)
    {
        ID3D10Device1 *pDevice = NULL;
        hr = D3D10CreateDevice1(
            pAdapter,
            driverType,
            NULL,
            flags,
            levelAttempts[level],
            D3D10_1_SDK_VERSION,
            &pDevice
            );

        if (SUCCEEDED(hr))
        {
            // transfer reference
            *ppDevice = pDevice;
            pDevice = NULL;
            break;
        }

    }

    return hr;
}
```



<span data-ttu-id="0b0af-160">下一個程式碼範例 `CreateD3DDevice` 會使用前一個範例中所示的方法，來建立可建立可與 Direct2D 搭配使用的 DXGI 介面的 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="0b0af-160">The next code example uses the `CreateD3DDevice` method shown in the previous example to create a Direct3D device that can create DXGI surfaces for use with Direct2D.</span></span>


```C++
// Create device
hr = CreateD3DDevice(
    NULL,
    D3D10_DRIVER_TYPE_HARDWARE,
    nDeviceFlags,
    &pDevice
    );

if (FAILED(hr))
{
    hr = CreateD3DDevice(
        NULL,
        D3D10_DRIVER_TYPE_WARP,
        nDeviceFlags,
        &pDevice
        );
}
```



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a><span data-ttu-id="0b0af-161">將 Direct2D 內容寫入交換鏈緩衝區</span><span class="sxs-lookup"><span data-stu-id="0b0af-161">Writing Direct2D Content to a Swap Chain Buffer</span></span>

<span data-ttu-id="0b0af-162">將 Direct2D 內容新增至 Direct3D 場景最簡單的方式，就是使用 [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)的 [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)方法來取得 DXGI 介面，然後使用具有 [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))方法的介面來建立用來繪製2d 內容的 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 。</span><span class="sxs-lookup"><span data-stu-id="0b0af-162">The simplest way to add Direct2D content to a Direct3D scene is to use the [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method of an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) to obtain a DXGI surface, then use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to create an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) with which to draw your 2-D content.</span></span>

<span data-ttu-id="0b0af-163">這種方法不會以三個維度轉譯您的內容;它不會有觀點或深度。</span><span class="sxs-lookup"><span data-stu-id="0b0af-163">This approach does not render your content in three dimensions; it will not have perspective or depth.</span></span> <span data-ttu-id="0b0af-164">不過，這對幾個常見的工作很有用：</span><span class="sxs-lookup"><span data-stu-id="0b0af-164">However, it is useful for several common tasks:</span></span>

-   <span data-ttu-id="0b0af-165">建立立體場景的2-d 背景。</span><span class="sxs-lookup"><span data-stu-id="0b0af-165">Creating a 2-D background for a 3-D scene.</span></span>
-   <span data-ttu-id="0b0af-166">在3-d 場景前方建立2D 介面。</span><span class="sxs-lookup"><span data-stu-id="0b0af-166">Creating a 2-D interface in front of a 3-D scene.</span></span>
-   <span data-ttu-id="0b0af-167">轉譯 Direct2D 內容時，使用 Direct3D 取樣。</span><span class="sxs-lookup"><span data-stu-id="0b0af-167">Using Direct3D multisampling when rendering Direct2D content.</span></span>

<span data-ttu-id="0b0af-168">下一節將說明如何建立3-d 場景的2D 背景。</span><span class="sxs-lookup"><span data-stu-id="0b0af-168">The next section shows how to create a 2-D background for a 3-D scene.</span></span>

### <a name="example-draw-a-2-d-background"></a><span data-ttu-id="0b0af-169">範例：繪製2D 背景</span><span class="sxs-lookup"><span data-stu-id="0b0af-169">Example: Draw a 2-D Background</span></span>

<span data-ttu-id="0b0af-170">下列步驟描述如何建立 DXGI 介面轉譯目標，並用它來繪製漸層背景。</span><span class="sxs-lookup"><span data-stu-id="0b0af-170">The following steps describe how to create a DXGI surface render target and use it to draw a gradient background.</span></span>

1.  <span data-ttu-id="0b0af-171">您可以使用 [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) 方法來建立 [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (*m \_ pDevice* 變數) 的交換鏈。</span><span class="sxs-lookup"><span data-stu-id="0b0af-171">Use the [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) method to create a swap chain for an [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (the *m\_pDevice* variable).</span></span> <span data-ttu-id="0b0af-172">交換鏈使用 [**dxgi \_ 格式 \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI 格式，這是 DIRECT2D 支援的其中一個 dxgi 格式。</span><span class="sxs-lookup"><span data-stu-id="0b0af-172">The swap chain uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

```C++
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&m_pDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&pDXGIDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDXGIDevice->GetAdapter(&pAdapter);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAdapter->GetParent(IID_PPV_ARGS(&pDXGIFactory));
    }
    if (SUCCEEDED(hr))
    {
        DXGI_SWAP_CHAIN_DESC swapDesc;
        ::ZeroMemory(&swapDesc, sizeof(swapDesc));

        swapDesc.BufferDesc.Width = nWidth;
        swapDesc.BufferDesc.Height = nHeight;
        swapDesc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
        swapDesc.BufferDesc.RefreshRate.Numerator = 60;
        swapDesc.BufferDesc.RefreshRate.Denominator = 1;
        swapDesc.SampleDesc.Count = 1;
        swapDesc.SampleDesc.Quality = 0;
        swapDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapDesc.BufferCount = 1;
        swapDesc.OutputWindow = m_hwnd;
        swapDesc.Windowed = TRUE;

        hr = pDXGIFactory->CreateSwapChain(m_pDevice, &swapDesc, &m_pSwapChain);
    }
```

    

2.  <span data-ttu-id="0b0af-173">使用交換鏈的 [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) 方法來取得 DXGI 介面。</span><span class="sxs-lookup"><span data-stu-id="0b0af-173">Use the swap chain's [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) method to obtain a DXGI surface.</span></span>

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  <span data-ttu-id="0b0af-174">使用 DXGI 介面建立 DXGI 轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="0b0af-174">Use the DXGI surface to create a DXGI render target.</span></span>
```C++
    // Create the DXGI Surface Render Target.
    FLOAT dpiX;
    FLOAT dpiY;
    m_pD2DFactory->GetDesktopDpi(&dpiX, &dpiY);

    D2D1_RENDER_TARGET_PROPERTIES props =
        D2D1::RenderTargetProperties(
            D2D1_RENDER_TARGET_TYPE_DEFAULT,
            D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
            dpiX,
            dpiY
            );

    // Create a Direct2D render target which can draw into the surface in the swap chain

    
hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pBackBuffer,
        &props,
        &m_pBackBufferRT
        );
    
```



    

4.  <span data-ttu-id="0b0af-175">使用呈現目標來繪製漸層背景。</span><span class="sxs-lookup"><span data-stu-id="0b0af-175">Use the render target to draw a gradient background.</span></span>

```C++
    // Swap chain will tell us how big the back buffer is
    DXGI_SWAP_CHAIN_DESC swapDesc;
    hr = m_pSwapChain->GetDesc(&swapDesc);

    if (SUCCEEDED(hr))
    {

    
// Draw a gradient background.
    if (m_pBackBufferRT)
    {
        D2D1_SIZE_F targetSize = m_pBackBufferRT->GetSize();

        m_pBackBufferRT->BeginDraw();

        m_pBackBufferGradientBrush->SetTransform(
            D2D1::Matrix3x2F::Scale(targetSize)
            );

        D2D1_RECT_F rect = D2D1::RectF(
            0.0f,
            0.0f,
            targetSize.width,
            targetSize.height
            );

        m_pBackBufferRT->FillRectangle(&rect, m_pBackBufferGradientBrush);

        hr = m_pBackBufferRT->EndDraw();
    }
```



    

<span data-ttu-id="0b0af-176">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="0b0af-176">Code is omitted from this sample.</span></span>

## <a name="using-direct2d-content-as-a-texture"></a><span data-ttu-id="0b0af-177">使用 Direct2D 內容作為材質</span><span class="sxs-lookup"><span data-stu-id="0b0af-177">Using Direct2D Content as a Texture</span></span>

<span data-ttu-id="0b0af-178">搭配使用 Direct2D 內容與 Direct3D 的另一種方式是使用 Direct2D 來產生2D 材質，然後將該材質套用至3D 模型。</span><span class="sxs-lookup"><span data-stu-id="0b0af-178">Another way to use Direct2D content with Direct3D is to use Direct2D to generate a 2-D texture and then apply that texture to a 3-D model.</span></span> <span data-ttu-id="0b0af-179">若要這麼做，您可以建立 [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)、從材質取得 DXGI 介面，然後使用介面建立 dxgi 表面轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="0b0af-179">You do this by creating an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), obtaining a DXGI surface from the texture, and then using the surface to create a DXGI surface render target.</span></span> <span data-ttu-id="0b0af-180">**ID3D10Texture2D** 介面必須使用 D3D10 系結轉譯 [**\_ \_ \_ 目標**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag)系結旗標，並使用 DXGI 介面轉譯目標所支援的 dxgi 格式。</span><span class="sxs-lookup"><span data-stu-id="0b0af-180">The **ID3D10Texture2D** surface must use the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) bind flag and use a DXGI format supported by DXGI surface render targets.</span></span> <span data-ttu-id="0b0af-181">如需支援的 DXGI 格式清單，請參閱 [支援的像素格式和 Alpha 模式](supported-pixel-formats-and-alpha-modes.md)。</span><span class="sxs-lookup"><span data-stu-id="0b0af-181">For a list of supported DXGI formats, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

### <a name="example-use-direct2d-content-as-a-texture"></a><span data-ttu-id="0b0af-182">範例：使用 Direct2D 內容作為材質</span><span class="sxs-lookup"><span data-stu-id="0b0af-182">Example: Use Direct2D Content as a Texture</span></span>

<span data-ttu-id="0b0af-183">下列範例示範如何建立可轉譯成2D 材質 (（由 [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)) 代表）的 DXGI 介面轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="0b0af-183">The following examples show how to create a DXGI surface render target that renders to a 2-D texture (represented by an [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).</span></span>

1.  <span data-ttu-id="0b0af-184">首先，使用 Direct3D 裝置來建立2D 材質。</span><span class="sxs-lookup"><span data-stu-id="0b0af-184">First, use a Direct3D device to create a 2-D texture.</span></span> <span data-ttu-id="0b0af-185">紋理會使用 D3D10 系結轉譯 [**\_ \_ \_ 目標**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) 和 **D3D10 系結 \_ \_ 著色器 \_ 資源** 系結旗標，並使用 [**dxgi \_ 格式 \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI 格式（Direct2D 所支援的其中一個 dxgi 格式）。</span><span class="sxs-lookup"><span data-stu-id="0b0af-185">The texture uses the [**D3D10\_BIND\_RENDER\_TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) and **D3D10\_BIND\_SHADER\_RESOURCE** bind flags, and it uses the [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI format, one of the DXGI formats supported by Direct2D.</span></span>

```C++
    // Allocate a offscreen D3D surface for D2D to render our 2D content into
    D3D10_TEXTURE2D_DESC texDesc;
    texDesc.ArraySize = 1;
    texDesc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
    texDesc.CPUAccessFlags = 0;
    texDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
    texDesc.Height = 512;
    texDesc.Width = 512;
    texDesc.MipLevels = 1;
    texDesc.MiscFlags = 0;
    texDesc.SampleDesc.Count = 1;
    texDesc.SampleDesc.Quality = 0;
    texDesc.Usage = D3D10_USAGE_DEFAULT;

    hr = m_pDevice->CreateTexture2D(&texDesc, NULL, &m_pOffscreenTexture);
```

    

2.  <span data-ttu-id="0b0af-186">使用紋理來取得 DXGI 表面。</span><span class="sxs-lookup"><span data-stu-id="0b0af-186">Use the texture to obtain a DXGI surface.</span></span>

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  <span data-ttu-id="0b0af-187">使用具有 [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) 方法的介面來取得 Direct2D 轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="0b0af-187">Use the surface with the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method to obtain a Direct2D render target.</span></span>

```C++
    if (SUCCEEDED(hr))
    {
        // Create a D2D render target which can draw into our offscreen D3D
        // surface. Given that we use a constant size for the texture, we
        // fix the DPI at 96.
        D2D1_RENDER_TARGET_PROPERTIES props =
            D2D1::RenderTargetProperties(
                D2D1_RENDER_TARGET_TYPE_DEFAULT,
                D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
                96,
                96
                );

    
    hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
            pDxgiSurface,
            &props,
            &m_pRenderTarget
            );
    }
```



    

<span data-ttu-id="0b0af-188">現在您已取得 Direct2D 轉譯目標，並將其與 Direct3D 材質相關聯，您可以使用轉譯目標將 Direct2D 內容繪製至該材質，也可以將該材質套用至 Direct3D 基本專案。</span><span class="sxs-lookup"><span data-stu-id="0b0af-188">Now that you have obtained a Direct2D render target and associated it with a Direct3D texture, you can use the render target to draw Direct2D content to that texture, and you can apply that texture to Direct3D primitives.</span></span>

<span data-ttu-id="0b0af-189">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="0b0af-189">Code is omitted from this sample.</span></span>

## <a name="resizing-a-dxgi-surface-render-target"></a><span data-ttu-id="0b0af-190">調整 DXGI 介面呈現目標的大小</span><span class="sxs-lookup"><span data-stu-id="0b0af-190">Resizing a DXGI Surface Render Target</span></span>

<span data-ttu-id="0b0af-191">DXGI 介面轉譯目標不支援 [**ID2D1RenderTarget：： Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) 方法。</span><span class="sxs-lookup"><span data-stu-id="0b0af-191">DXGI surface render targets do not support the [**ID2D1RenderTarget::Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) method.</span></span> <span data-ttu-id="0b0af-192">若要調整 DXGI 介面轉譯目標的大小，應用程式必須釋放並重新建立。</span><span class="sxs-lookup"><span data-stu-id="0b0af-192">To resize a DXGI surface render target, the application must release and re-create it.</span></span>

<span data-ttu-id="0b0af-193">這種作業可能會造成效能問題。</span><span class="sxs-lookup"><span data-stu-id="0b0af-193">This operation can potentially create performance issues.</span></span> <span data-ttu-id="0b0af-194">轉譯目標可能是最後一個使用中的 Direct2D 資源，它會保留與轉譯目標之 DXGI 介面相關聯之 [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) 的參考。</span><span class="sxs-lookup"><span data-stu-id="0b0af-194">The render target might be the last active Direct2D resource that keeps a reference to the [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) associated with the render target's DXGI surface.</span></span> <span data-ttu-id="0b0af-195">如果應用程式釋出轉譯目標，並終結 **ID3D10Device1** 參考，則必須重新建立新的參考。</span><span class="sxs-lookup"><span data-stu-id="0b0af-195">If the application releases the render target and the **ID3D10Device1** reference is destroyed, a new one must be recreated.</span></span>

<span data-ttu-id="0b0af-196">您可以在重新建立轉譯目標時，保留轉譯目標所建立的至少一個 Direct2D 資源，以避免這項可能耗費資源的作業。</span><span class="sxs-lookup"><span data-stu-id="0b0af-196">You can avoid this potentially expensive operation by keeping at least one Direct2D resource that was created by the render target while you re-create that render target.</span></span> <span data-ttu-id="0b0af-197">以下是一些適用于此方法的 Direct2D 資源：</span><span class="sxs-lookup"><span data-stu-id="0b0af-197">The following are some Direct2D resources that work for this approach:</span></span>

-   <span data-ttu-id="0b0af-198">[**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)可以間接保留的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) () </span><span class="sxs-lookup"><span data-stu-id="0b0af-198">[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (which may be held indirectly by an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))</span></span>
-   [<span data-ttu-id="0b0af-199">**ID2D1Layer**</span><span class="sxs-lookup"><span data-stu-id="0b0af-199">**ID2D1Layer**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [<span data-ttu-id="0b0af-200">**ID2D1Mesh**</span><span class="sxs-lookup"><span data-stu-id="0b0af-200">**ID2D1Mesh**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

<span data-ttu-id="0b0af-201">為了配合此方法，您的調整大小方法應該會進行測試，以查看 Direct3D 裝置是否可用。</span><span class="sxs-lookup"><span data-stu-id="0b0af-201">To accommodate this approach, your resize method should test to see whether the Direct3D device is available.</span></span> <span data-ttu-id="0b0af-202">如果可用，請釋放並重新建立您的 DXGI 介面轉譯目標，但保留先前建立的所有資源並重複使用。</span><span class="sxs-lookup"><span data-stu-id="0b0af-202">If it is available, release and re-create your DXGI surface render targets, but keep all the resources that they created previously and reuse them.</span></span> <span data-ttu-id="0b0af-203">這項功能的運作方式是因為如 [資源總覽](resources-and-resource-domains.md)所述，當兩個轉譯目標都與相同的 Direct3D 裝置相關聯時，兩個轉譯目標所建立的資源都是相容的。</span><span class="sxs-lookup"><span data-stu-id="0b0af-203">This works because, as described in the [Resources Overview](resources-and-resource-domains.md), resources created by two render targets are compatible when both render targets are associated with the same Direct3D device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b0af-204">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b0af-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b0af-205">支援的像素格式和 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="0b0af-205">Supported Pixel Formats and Alpha Modes</span></span>](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

<span data-ttu-id="0b0af-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="0b0af-206">[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))</span></span>
</dt> <dt>

[<span data-ttu-id="0b0af-207">Windows DirectX 圖形</span><span class="sxs-lookup"><span data-stu-id="0b0af-207">Windows DirectX Graphics</span></span>](../graphics-and-multimedia.md)
</dt> </dl>

 

 