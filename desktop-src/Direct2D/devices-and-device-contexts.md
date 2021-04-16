---
title: 如何使用 Direct2D 裝置內容呈現
description: 在本主題中，您將瞭解如何在 Windows 8 中建立 Direct2D \ 32; 裝置內容。
ms.assetid: D4563FEA-767E-4B16-8F3C-3D548A64B206
keywords:
- Direct2D 裝置
- Direct2D 裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2858861956a40bf969309be474105052e4692cde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104557791"
---
# <a name="how-to-render-by-using-a-direct2d-device-context"></a><span data-ttu-id="c13cf-105">如何使用 Direct2D 裝置內容呈現</span><span class="sxs-lookup"><span data-stu-id="c13cf-105">How to render by using a Direct2D device context</span></span>

<span data-ttu-id="c13cf-106">在本主題中，您將瞭解如何在 Windows 8 中建立 [Direct2D](./direct2d-portal.md) [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 。</span><span class="sxs-lookup"><span data-stu-id="c13cf-106">In this topic you will learn about creating [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) in Windows 8.</span></span> <span data-ttu-id="c13cf-107">如果您要使用 Direct2D 開發 Windows Store 應用程式或傳統型應用程式，這項資訊適用于您。</span><span class="sxs-lookup"><span data-stu-id="c13cf-107">This information applies to you if you are developing Windows Store apps or a desktop app by using Direct2D.</span></span> <span data-ttu-id="c13cf-108">本主題說明 Direct2D 裝置內容物件的用途、如何建立該物件，以及如何轉譯和顯示 Direct2D 基本和影像的逐步指南。</span><span class="sxs-lookup"><span data-stu-id="c13cf-108">This topic describes the purpose of Direct2D device context objects, how to create that object , and a step by step guide about rendering and displaying Direct2D primitives and images.</span></span> <span data-ttu-id="c13cf-109">您也將瞭解如何切換轉譯目標，以及如何將效果新增至您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c13cf-109">You will also learn about switching render targets and adding effects to your app.</span></span>

-   [<span data-ttu-id="c13cf-110">什麼是 Direct2D 裝置？</span><span class="sxs-lookup"><span data-stu-id="c13cf-110">What is a Direct2D device?</span></span>](#what-is-a-direct2d-device)
-   [<span data-ttu-id="c13cf-111">什麼是 Direct2D 裝置內容？</span><span class="sxs-lookup"><span data-stu-id="c13cf-111">What is a Direct2D device context?</span></span>](#what-is-a-direct2d-device-context)
-   [<span data-ttu-id="c13cf-112">在 Windows 8 上使用 Direct2D 轉譯</span><span class="sxs-lookup"><span data-stu-id="c13cf-112">Rendering with Direct2D on Windows 8</span></span>](#rendering-with-direct2d-on-windows-8)
-   [<span data-ttu-id="c13cf-113">為何要使用裝置內容呈現？</span><span class="sxs-lookup"><span data-stu-id="c13cf-113">Why use a device context to render?</span></span>](#why-use-a-device-context-to-render)
-   [<span data-ttu-id="c13cf-114">如何建立 Direct2D 裝置內容以進行轉譯</span><span class="sxs-lookup"><span data-stu-id="c13cf-114">How to create a Direct2D device context for rendering</span></span>](#how-to-create-a-direct2d-device-context-for-rendering)
-   [<span data-ttu-id="c13cf-115">選取目標</span><span class="sxs-lookup"><span data-stu-id="c13cf-115">Selecting a target</span></span>](#selecting-a-target)
-   [<span data-ttu-id="c13cf-116">如何呈現和顯示</span><span class="sxs-lookup"><span data-stu-id="c13cf-116">How to render and display</span></span>](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a><span data-ttu-id="c13cf-117">什麼是 Direct2D 裝置？</span><span class="sxs-lookup"><span data-stu-id="c13cf-117">What is a Direct2D device?</span></span>

<span data-ttu-id="c13cf-118">您需要 Direct2D 裝置和 Direct3D 裝置來建立 Direct2D 裝置內容。</span><span class="sxs-lookup"><span data-stu-id="c13cf-118">You need a Direct2D device and a Direct3D device to create a Direct2D device context.</span></span> <span data-ttu-id="c13cf-119">[**Direct2D 裝置**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (公開 **ID2D1Device** 介面指標，) 代表顯示配接器。</span><span class="sxs-lookup"><span data-stu-id="c13cf-119">A [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (exposes an **ID2D1Device** interface pointer) represents a display adapter.</span></span> <span data-ttu-id="c13cf-120">Direct3D 裝置 (公開 [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) 介面指標) 與 Direct2D 裝置相關聯。</span><span class="sxs-lookup"><span data-stu-id="c13cf-120">A Direct3D device (exposes an [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) interface pointer) is associated with a Direct2D device.</span></span> <span data-ttu-id="c13cf-121">每個應用程式都必須有一個 **Direct2D 裝置**，但可以有一個以上的 **裝置**。</span><span class="sxs-lookup"><span data-stu-id="c13cf-121">Each app must have one **Direct2D device**, but can have more than one **device**.</span></span>

## <a name="what-is-a-direct2d-device-context"></a><span data-ttu-id="c13cf-122">什麼是 Direct2D 裝置內容？</span><span class="sxs-lookup"><span data-stu-id="c13cf-122">What is a Direct2D device context?</span></span>

<span data-ttu-id="c13cf-123">[Direct2D](./direct2d-portal.md) [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) (公開 **ID2D1DeviceCoNtext** 介面指標，) 代表一組您用來轉譯至目標的狀態和命令緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c13cf-123">A [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) (exposes an **ID2D1DeviceContext** interface pointer) represents a set of state and command buffers that you use to render to a target.</span></span> <span data-ttu-id="c13cf-124">您可以使用裝置所擁有的資源，在裝置內容上呼叫方法來設定管線狀態和產生轉譯命令。</span><span class="sxs-lookup"><span data-stu-id="c13cf-124">You can call methods on the device context to set pipeline state and generate rendering commands by using the resources owned by a device.</span></span>

## <a name="rendering-with-direct2d-on-windows-8"></a><span data-ttu-id="c13cf-125">在 Windows 8 上使用 Direct2D 轉譯</span><span class="sxs-lookup"><span data-stu-id="c13cf-125">Rendering with Direct2D on Windows 8</span></span>

<span data-ttu-id="c13cf-126">在 Windows 7 及更早版本上，您可以使用 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 或其他轉譯目標介面，轉譯成視窗或表面。</span><span class="sxs-lookup"><span data-stu-id="c13cf-126">On Windows 7 and earlier, you use a [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) or another render target interface to render to a window or surface.</span></span> <span data-ttu-id="c13cf-127">從 Windows 8 開始，我們不建議使用依賴 **ID2D1HwndRenderTarget** 等介面的方法來轉譯，因為它們無法與 Windows Store 應用程式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c13cf-127">Starting with Windows 8, we do not recommend rendering by using methods that rely on interfaces like **ID2D1HwndRenderTarget** because they won't work with Windows Store apps.</span></span> <span data-ttu-id="c13cf-128">如果您想要製作桌面應用程式，並仍利用 **裝置內容的** 其他功能，您可以使用 [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)轉譯為 Hwnd。</span><span class="sxs-lookup"><span data-stu-id="c13cf-128">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to render to an Hwnd if you want to make a desktop app and still take advantage of the **device context's** additional features.</span></span> <span data-ttu-id="c13cf-129">不過，在具有 [Direct2D](./direct2d-portal.md)的 Windows Store 應用程式中轉譯內容時，需要 **裝置** 內容。</span><span class="sxs-lookup"><span data-stu-id="c13cf-129">However, the **device context** is required to render content in a Windows Store apps with [Direct2D](./direct2d-portal.md).</span></span>

## <a name="why-use-a-device-context-to-render"></a><span data-ttu-id="c13cf-130">為何要使用裝置內容呈現？</span><span class="sxs-lookup"><span data-stu-id="c13cf-130">Why use a device context to render?</span></span>

-   <span data-ttu-id="c13cf-131">您可以針對 Windows Store 應用程式呈現。</span><span class="sxs-lookup"><span data-stu-id="c13cf-131">You can render for Windows Store apps.</span></span>
-   <span data-ttu-id="c13cf-132">您可以在轉譯之前、期間和之後隨時變更轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="c13cf-132">You can change the render target at any time before, during, and after rendering.</span></span> <span data-ttu-id="c13cf-133">裝置內容可確保繪製方法的呼叫會依序執行，並在您切換轉譯目標時套用它們。</span><span class="sxs-lookup"><span data-stu-id="c13cf-133">The device context ensures that the calls to drawing methods are executed in order and applies them when you switch the render target.</span></span>
-   <span data-ttu-id="c13cf-134">您可以使用一種以上的視窗類型搭配裝置內容。</span><span class="sxs-lookup"><span data-stu-id="c13cf-134">You can use more than one type of window with a device context.</span></span> <span data-ttu-id="c13cf-135">您可以使用 [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 和 [**DXGI 交換鏈**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) ，直接轉譯為 [**windows：： ui：： Core：： COREWINDOW**](/uwp/api/Windows.UI.Core.CoreWindow) 或 [**windows：： ui：： XAML：： SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel)。</span><span class="sxs-lookup"><span data-stu-id="c13cf-135">You can use a [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) to render directly to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) or a [**Windows::UI::XAML::SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel).</span></span>
-   <span data-ttu-id="c13cf-136">您可以使用 [Direct2D](./direct2d-portal.md) [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 來建立 [Direct2D 效果](effects-overview.md) ，並將影像效果或效果圖形的輸出轉譯成轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="c13cf-136">You can use the [Direct2D](./direct2d-portal.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to create [Direct2D effects](effects-overview.md) and to render the output of an image effect or effect graph to a render target.</span></span>
-   <span data-ttu-id="c13cf-137">您可以有多個 [**裝置**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)內容，這有助於改善執行緒應用程式中的效能。</span><span class="sxs-lookup"><span data-stu-id="c13cf-137">You can have multiple [**device contexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext), which can be helpful for improving performance in a threaded app.</span></span> <span data-ttu-id="c13cf-138">如需詳細資訊，請參閱 [多執行緒 Direct2D 應用程式](multi-threaded-direct2d-apps.md) 。</span><span class="sxs-lookup"><span data-stu-id="c13cf-138">See [Multithreaded Direct2D apps](multi-threaded-direct2d-apps.md) for more information.</span></span>
-   <span data-ttu-id="c13cf-139">[**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)與 direct3d 緊密交互操作，讓您更容易存取 direct3d 選項。</span><span class="sxs-lookup"><span data-stu-id="c13cf-139">The [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interoperates closely with Direct3D, giving you more access to Direct3D options.</span></span>

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a><span data-ttu-id="c13cf-140">如何建立 Direct2D 裝置內容以進行轉譯</span><span class="sxs-lookup"><span data-stu-id="c13cf-140">How to create a Direct2D device context for rendering</span></span>

<span data-ttu-id="c13cf-141">此處的程式碼會示範如何建立 Direct3D11 裝置、取得相關聯的 DXGI 裝置、建立 [**Direct2D 裝置**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)，最後建立 Direct2D [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 以供轉譯。</span><span class="sxs-lookup"><span data-stu-id="c13cf-141">The code here shows you how to create a Direct3D11 device, get the associated DXGI device, create a [**Direct2D device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device), and then finally create the Direct2D [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) for rendering.</span></span>

<span data-ttu-id="c13cf-142">以下是方法呼叫的圖表，以及此程式碼所使用的介面。</span><span class="sxs-lookup"><span data-stu-id="c13cf-142">Here is a diagram of the method calls and the interfaces this code uses.</span></span>

![direct2d 和 direct3d 裝置的圖表，以及裝置內容。](images/devicecontextdiagram.png)

> [!Note]  
> <span data-ttu-id="c13cf-144">這段程式碼假設您已有 [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) 物件。如需詳細資訊，請參閱 [**ID2D1Factory 參考頁面**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)。</span><span class="sxs-lookup"><span data-stu-id="c13cf-144">This code assumes you already have an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) object, for more information see the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>

 


```C++
    // This flag adds support for surfaces with a different color channel ordering than the API default.
    // You need it for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    
    // This array defines the set of DirectX hardware feature levels this app  supports.
    // The ordering is important and you should  preserve it.
    // Don't forget to declare your app's minimum required feature level in its
    // description.  All apps are assumed to support 9.1 unless otherwise stated.
    D3D_FEATURE_LEVEL featureLevels[] = 
    {
        D3D_FEATURE_LEVEL_11_1,
        D3D_FEATURE_LEVEL_11_0,
        D3D_FEATURE_LEVEL_10_1,
        D3D_FEATURE_LEVEL_10_0,
        D3D_FEATURE_LEVEL_9_3,
        D3D_FEATURE_LEVEL_9_2,
        D3D_FEATURE_LEVEL_9_1
    };

    // Create the DX11 API device object, and get a corresponding context.
    ComPtr<ID3D11Device> device;
    ComPtr<ID3D11DeviceContext> context;

    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of possible feature levels
            D3D11_SDK_VERSION,          
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );

    ComPtr<IDXGIDevice> dxgiDevice;
    // Obtain the underlying DXGI device of the Direct3D11 device.
    DX::ThrowIfFailed(
        device.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // Get Direct2D device's corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



<span data-ttu-id="c13cf-145">讓我們逐步解說上述程式碼範例中的步驟。</span><span class="sxs-lookup"><span data-stu-id="c13cf-145">Let's walk through the steps in the preceding code sample.</span></span>

1.  <span data-ttu-id="c13cf-146">取得 ID3D11Device 介面指標，您將需要此指標才能建立裝置內容。</span><span class="sxs-lookup"><span data-stu-id="c13cf-146">Get an ID3D11Device interface pointer you will need this to create the device context.</span></span>

    -   <span data-ttu-id="c13cf-147">宣告建立旗標以設定 BGRA 支援的 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 裝置。</span><span class="sxs-lookup"><span data-stu-id="c13cf-147">Declare the creation flags to set up the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) device for BGRA support.</span></span> <span data-ttu-id="c13cf-148">[Direct2D](./direct2d-portal.md) 需要 BGRA 色彩順序。</span><span class="sxs-lookup"><span data-stu-id="c13cf-148">[Direct2D](./direct2d-portal.md) requires BGRA color order.</span></span>
    -   <span data-ttu-id="c13cf-149">宣告 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) 專案的陣列，代表您的應用程式將支援的功能層級集合。</span><span class="sxs-lookup"><span data-stu-id="c13cf-149">Declare an array of [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) entries representing the set of feature levels that your app will support.</span></span>
        > [!Note]  
        > <span data-ttu-id="c13cf-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 會搜尋您的清單，直到找到主機系統所支援的功能層級。</span><span class="sxs-lookup"><span data-stu-id="c13cf-150">[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) searches your list until it finds the feature level supported by the host system.</span></span>

         

    -   <span data-ttu-id="c13cf-151">您可以使用 [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) 函式來建立 [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) 物件，此函式也會傳回 [**>id3d11devicecoNtext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) 物件，但此範例不需要該物件。</span><span class="sxs-lookup"><span data-stu-id="c13cf-151">Use the [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) function to create an [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) object, the function will also return an [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) object, but that object is not needed for this example.</span></span>

2.  <span data-ttu-id="c13cf-152">查詢 [**Direct3D 11 裝置**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) 以取得其 [**DXGI 裝置**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) 介面。</span><span class="sxs-lookup"><span data-stu-id="c13cf-152">Query the [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) for its [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) interface.</span></span>
3.  <span data-ttu-id="c13cf-153">藉由呼叫 [**ID2D1Factory：： CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice)方法並傳入 [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)物件來建立 [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)物件。</span><span class="sxs-lookup"><span data-stu-id="c13cf-153">Create an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) object by calling the [**ID2D1Factory::CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) method and passing in the [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) object.</span></span>
4.  <span data-ttu-id="c13cf-154">使用 [**ID2D1Device：： CreateDeviceCoNtext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext)方法建立 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)指標。</span><span class="sxs-lookup"><span data-stu-id="c13cf-154">Create an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pointer using the [**ID2D1Device::CreateDeviceContext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) method.</span></span>

## <a name="selecting-a-target"></a><span data-ttu-id="c13cf-155">選取目標</span><span class="sxs-lookup"><span data-stu-id="c13cf-155">Selecting a target</span></span>

<span data-ttu-id="c13cf-156">此處的程式碼會示範如何取得視窗背景緩衝區的 [**2 維度 Direct3D 材質**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) ，並建立連結至 [**Direct2D 裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 所呈現之材質的點陣圖目標。</span><span class="sxs-lookup"><span data-stu-id="c13cf-156">The code here shows you how to get the [**2 dimensional Direct3D texture**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) for the window back buffer and create a bitmap target that links to this texture to which the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) renders.</span></span>


```C++
        // Allocate a descriptor.
        DXGI_SWAP_CHAIN_DESC1 swapChainDesc = {0};
        swapChainDesc.Width = 0;                           // use automatic sizing
        swapChainDesc.Height = 0;
        swapChainDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM; // this is the most common swapchain format
        swapChainDesc.Stereo = false; 
        swapChainDesc.SampleDesc.Count = 1;                // don't use multi-sampling
        swapChainDesc.SampleDesc.Quality = 0;
        swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapChainDesc.BufferCount = 2;                     // use double buffering to enable flip
        swapChainDesc.Scaling = DXGI_SCALING_NONE;
        swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL; // all apps must use this SwapEffect
        swapChainDesc.Flags = 0;

        // Identify the physical adapter (GPU or card) this device is runs on.
        ComPtr<IDXGIAdapter> dxgiAdapter;
        DX::ThrowIfFailed(
            dxgiDevice->GetAdapter(&dxgiAdapter)
            );

        // Get the factory object that created the DXGI device.
        ComPtr<IDXGIFactory2> dxgiFactory;
        DX::ThrowIfFailed(
            dxgiAdapter->GetParent(IID_PPV_ARGS(&dxgiFactory))
            );

        // Get the final swap chain for this window from the DXGI factory.
        DX::ThrowIfFailed(
            dxgiFactory->CreateSwapChainForCoreWindow(
                device.Get(),
                reinterpret_cast<IUnknown*>(m_window),
                &swapChainDesc,
                nullptr,    // allow on all displays
                &m_swapChain
                )
            );

        // Ensure that DXGI doesn't queue more than one frame at a time.
        DX::ThrowIfFailed(
            dxgiDevice->SetMaximumFrameLatency(1)
            );

    // Get the backbuffer for this window which is be the final 3D render target.
    ComPtr<ID3D11Texture2D> backBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&backBuffer))
        );

    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it is directly rendered to the 
    // swap chain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_IGNORE),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // Now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



<span data-ttu-id="c13cf-157">讓我們逐步解說上述程式碼範例中的步驟。</span><span class="sxs-lookup"><span data-stu-id="c13cf-157">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="c13cf-158">配置一個 [**DXGI \_ 交換 \_ 鏈 \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) 結構，並定義 [**交換鏈**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)的設定。</span><span class="sxs-lookup"><span data-stu-id="c13cf-158">Allocate a [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and define the settings for the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

    <span data-ttu-id="c13cf-159">這些設定顯示如何建立 Windows Store 應用程式可使用之交換鏈的範例。</span><span class="sxs-lookup"><span data-stu-id="c13cf-159">These settings show an example of how to create a swap chain that a Windows Store app can use.</span></span>

2.  <span data-ttu-id="c13cf-160">取得 [**Direct3D 裝置**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) 和 [**DXGI 裝置**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) 正在其上執行的介面卡，並取得與其相關聯的 [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) 物件。</span><span class="sxs-lookup"><span data-stu-id="c13cf-160">Get the adapter that the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) are running on and get the [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) object associated with them.</span></span> <span data-ttu-id="c13cf-161">您必須使用此 **DXGI factory** ，以確保在相同的介面卡上建立 [**交換鏈**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) 。</span><span class="sxs-lookup"><span data-stu-id="c13cf-161">You must use this **DXGI factory** to ensure the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) is created on the same adapter.</span></span>

3.  <span data-ttu-id="c13cf-162">呼叫 [**IDXGIFactory2：： CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) 方法來建立交換鏈。</span><span class="sxs-lookup"><span data-stu-id="c13cf-162">Call the [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) method to create the swap chain.</span></span> <span data-ttu-id="c13cf-163">針對 Windows Store 應用程式的主視窗，請使用 [**windows：： UI：： CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) 類別。</span><span class="sxs-lookup"><span data-stu-id="c13cf-163">Use the [**Windows::UI::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) class for the main window of a Windows Store app.</span></span>

    <span data-ttu-id="c13cf-164">請務必將畫面格延遲上限設為1，以將耗電量降至最低。</span><span class="sxs-lookup"><span data-stu-id="c13cf-164">Make sure to set the maximum frame latency to 1 to minimize power consumption.</span></span>

    <span data-ttu-id="c13cf-165">如果您想要在 Windows Store 應用程式中呈現 Direct2D 內容，請參閱 [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) 方法。</span><span class="sxs-lookup"><span data-stu-id="c13cf-165">If you want to render Direct2D content in a Windows Store app, see the [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method.</span></span>

4.  <span data-ttu-id="c13cf-166">從 [**交換鏈**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)取得背面緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c13cf-166">Get the back buffer from the [**swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span> <span data-ttu-id="c13cf-167">背景緩衝區會公開由 **交換鏈** 配置的 [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d)介面</span><span class="sxs-lookup"><span data-stu-id="c13cf-167">The back buffer exposes an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) interface allocated by the **swap chain**</span></span>

5.  <span data-ttu-id="c13cf-168">宣告 [**D2D1 \_ 點陣圖 \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) 結構並設定屬性值。</span><span class="sxs-lookup"><span data-stu-id="c13cf-168">Declare a [**D2D1\_BITMAP\_PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) struct and set the property values.</span></span> <span data-ttu-id="c13cf-169">將像素格式設定為 BGRA，因為這是 [**Direct3D 裝置**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) 和 [**DXGI 裝置**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) 使用的格式。</span><span class="sxs-lookup"><span data-stu-id="c13cf-169">Set the pixel format to BGRA because this is the format the [**Direct3D device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) and the [**DXGI Device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) use.</span></span>

6.  <span data-ttu-id="c13cf-170">取得以 [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) 傳遞至 Direct2D 的背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c13cf-170">Get the back buffer as an [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) to pass to Direct2D.</span></span> <span data-ttu-id="c13cf-171">Direct2D 不會直接接受 [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) 。</span><span class="sxs-lookup"><span data-stu-id="c13cf-171">Direct2D doesn't accept an [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) directly.</span></span>

    <span data-ttu-id="c13cf-172">使用 [**ID2D1DeviceCoNtext：： CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1))方法，從背景緩衝區建立 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)物件。</span><span class="sxs-lookup"><span data-stu-id="c13cf-172">Create a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object from the back buffer using the [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method.</span></span>

7.  <span data-ttu-id="c13cf-173">現在 [**Direct2D 點陣圖**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 會連結至背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c13cf-173">Now the [**Direct2D bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is linked to the back buffer.</span></span> <span data-ttu-id="c13cf-174">將 [**Direct2D 裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 上的目標設定為 **點陣圖**。</span><span class="sxs-lookup"><span data-stu-id="c13cf-174">Set the target on the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) to the **bitmap**.</span></span>

## <a name="how-to-render-and-display"></a><span data-ttu-id="c13cf-175">如何呈現和顯示</span><span class="sxs-lookup"><span data-stu-id="c13cf-175">How to render and display</span></span>

<span data-ttu-id="c13cf-176">現在您已有目標點陣圖，您可以使用 [**Direct2D 裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)來繪製基本、影像、影像效果和文字。</span><span class="sxs-lookup"><span data-stu-id="c13cf-176">Now that you have a target bitmap, you can draw primitives, images, image effects, and text to it using the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span></span> <span data-ttu-id="c13cf-177">此處的程式碼會示範如何繪製矩形。</span><span class="sxs-lookup"><span data-stu-id="c13cf-177">The code here shows you how to draw a rectangle.</span></span>


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);

m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



<span data-ttu-id="c13cf-178">讓我們逐步解說上述程式碼範例中的步驟。</span><span class="sxs-lookup"><span data-stu-id="c13cf-178">Let's walk through the steps in the preceding code example.</span></span>

1.  <span data-ttu-id="c13cf-179">呼叫 [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) 來建立筆刷來繪製矩形。</span><span class="sxs-lookup"><span data-stu-id="c13cf-179">Call the [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) to create a brush to paint the rectangle.</span></span>
2.  <span data-ttu-id="c13cf-180">發出任何繪圖命令之前，請先呼叫 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法。</span><span class="sxs-lookup"><span data-stu-id="c13cf-180">Call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands.</span></span>
3.  <span data-ttu-id="c13cf-181">呼叫 [**graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) 方法來繪製要繪製的矩形和筆刷。</span><span class="sxs-lookup"><span data-stu-id="c13cf-181">Call the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method the rectangle to be drawn and the brush.</span></span>
4.  <span data-ttu-id="c13cf-182">完成繪製命令之後，請呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。</span><span class="sxs-lookup"><span data-stu-id="c13cf-182">Call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span>
5.  <span data-ttu-id="c13cf-183">藉由呼叫 [**IDXGISwapChain：:P 重發**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) 方法來顯示結果。</span><span class="sxs-lookup"><span data-stu-id="c13cf-183">Display the result by calling the [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method.</span></span>

<span data-ttu-id="c13cf-184">現在您可以使用 [**Direct2D 裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 將基本、影像、影像效果和文字繪製到螢幕。</span><span class="sxs-lookup"><span data-stu-id="c13cf-184">Now you can use the [**Direct2D device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) draw primitives, images, image effects, and text to the screen.</span></span>

 

 