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
ms.openlocfilehash: 735ad81a5911b16c159ffb8c63173421a55295e20e34090eb483065e1a7d311c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832991"
---
# <a name="how-to-render-by-using-a-direct2d-device-context"></a>如何使用 Direct2D 裝置內容呈現

在本主題中，您將瞭解如何在 Windows 8 中建立 [Direct2D](./direct2d-portal.md) [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)。 如果您要使用 Direct2D 來開發 Windows Store 應用程式或桌面應用程式，這項資訊適用于您。 本主題說明 Direct2D 裝置內容物件的用途、如何建立該物件，以及如何轉譯和顯示 Direct2D 基本和影像的逐步指南。 您也將瞭解如何切換轉譯目標，以及如何將效果新增至您的應用程式。

-   [什麼是 Direct2D 裝置？](#what-is-a-direct2d-device)
-   [什麼是 Direct2D 裝置內容？](#what-is-a-direct2d-device-context)
-   [在 Windows 8 上使用 Direct2D 轉譯](#rendering-with-direct2d-on-windows-8)
-   [為何要使用裝置內容呈現？](#why-use-a-device-context-to-render)
-   [如何建立 Direct2D 裝置內容以進行轉譯](#how-to-create-a-direct2d-device-context-for-rendering)
-   [選取目標](#selecting-a-target)
-   [如何呈現和顯示](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a>什麼是 Direct2D 裝置？

您需要 Direct2D 裝置和 Direct3D 裝置來建立 Direct2D 裝置內容。 [**Direct2D 裝置**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (公開 **ID2D1Device** 介面指標，) 代表顯示配接器。 Direct3D 裝置 (公開 [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) 介面指標) 與 Direct2D 裝置相關聯。 每個應用程式都必須有一個 **Direct2D 裝置**，但可以有一個以上的 **裝置**。

## <a name="what-is-a-direct2d-device-context"></a>什麼是 Direct2D 裝置內容？

[Direct2D](./direct2d-portal.md) [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) (公開 **ID2D1DeviceCoNtext** 介面指標，) 代表一組您用來轉譯至目標的狀態和命令緩衝區。 您可以使用裝置所擁有的資源，在裝置內容上呼叫方法來設定管線狀態和產生轉譯命令。

## <a name="rendering-with-direct2d-on-windows-8"></a>在 Windows 8 上使用 Direct2D 轉譯

在 Windows 7 及更早版本上，您可以使用 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)或其他轉譯目標介面，以轉譯為視窗或表面。 從 Windows 8 開始，我們不建議使用依賴 **ID2D1HwndRenderTarget** 等介面的方法來轉譯，因為它們無法與 Windows Store 應用程式搭配使用。 如果您想要製作桌面應用程式，並仍利用 **裝置內容的** 其他功能，您可以使用 [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)轉譯為 Hwnd。 不過，使用 [Direct2D](./direct2d-portal.md)在 Windows Store 應用程式中轉譯內容時，需要 **裝置** 內容。

## <a name="why-use-a-device-context-to-render"></a>為何要使用裝置內容呈現？

-   您可以針對 Windows Store 應用程式轉譯。
-   您可以在轉譯之前、期間和之後隨時變更轉譯目標。 裝置內容可確保繪製方法的呼叫會依序執行，並在您切換轉譯目標時套用它們。
-   您可以使用一種以上的視窗類型搭配裝置內容。 您可以使用 [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)和 [**DXGI 交換鏈**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)，直接轉譯成 [**Windows：： ui：： Core：： CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)或 [**Windows：： ui：： XAML：： SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel)。
-   您可以使用 [Direct2D](./direct2d-portal.md) [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 來建立 [Direct2D 效果](effects-overview.md) ，並將影像效果或效果圖形的輸出轉譯成轉譯目標。
-   您可以有多個 [**裝置**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)內容，這有助於改善執行緒應用程式中的效能。 如需詳細資訊，請參閱 [多執行緒 Direct2D 應用程式](multi-threaded-direct2d-apps.md) 。
-   [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)與 direct3d 緊密交互操作，讓您更容易存取 direct3d 選項。

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a>如何建立 Direct2D 裝置內容以進行轉譯

此處的程式碼會示範如何建立 Direct3D11 裝置、取得相關聯的 DXGI 裝置、建立 [**Direct2D 裝置**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)，最後建立 Direct2D [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 以供轉譯。

以下是方法呼叫的圖表，以及此程式碼所使用的介面。

![direct2d 和 direct3d 裝置的圖表，以及裝置內容。](images/devicecontextdiagram.png)

> [!Note]  
> 這段程式碼假設您已有 [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) 物件。如需詳細資訊，請參閱 [**ID2D1Factory 參考頁面**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)。

 


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



讓我們逐步解說上述程式碼範例中的步驟。

1.  取得 ID3D11Device 介面指標，您將需要此指標才能建立裝置內容。

    -   宣告建立旗標以設定 BGRA 支援的 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 裝置。 [Direct2D](./direct2d-portal.md) 需要 BGRA 色彩順序。
    -   宣告 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) 專案的陣列，代表您的應用程式將支援的功能層級集合。
        > [!Note]  
        > [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 會搜尋您的清單，直到找到主機系統所支援的功能層級。

         

    -   您可以使用 [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) 函式來建立 [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) 物件，此函式也會傳回 [**>id3d11devicecoNtext**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) 物件，但此範例不需要該物件。

2.  查詢 [**Direct3D 11 裝置**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) 以取得其 [**DXGI 裝置**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) 介面。
3.  藉由呼叫 [**ID2D1Factory：： CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice)方法並傳入 [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)物件來建立 [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)物件。
4.  使用 [**ID2D1Device：： CreateDeviceCoNtext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext)方法建立 [**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)指標。

## <a name="selecting-a-target"></a>選取目標

此處的程式碼會示範如何取得視窗背景緩衝區的 [**2 維度 Direct3D 材質**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) ，並建立連結至 [**Direct2D 裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 所呈現之材質的點陣圖目標。


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



讓我們逐步解說上述程式碼範例中的步驟。

1.  配置一個 [**DXGI \_ 交換 \_ 鏈 \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) 結構，並定義 [**交換鏈**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)的設定。

    這些設定顯示如何建立 Windows Store 應用程式可使用的交換鏈的範例。

2.  取得 [**Direct3D 裝置**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) 和 [**DXGI 裝置**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) 正在其上執行的介面卡，並取得與其相關聯的 [**IDXGIFactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) 物件。 您必須使用此 **DXGI factory** ，以確保在相同的介面卡上建立 [**交換鏈**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) 。

3.  呼叫 [**IDXGIFactory2：： CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) 方法來建立交換鏈。 針對 Windows Store 應用程式的主視窗，請使用 [**Windows：： UI：： CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)類別。

    請務必將畫面格延遲上限設為1，以將耗電量降至最低。

    如果您想要在 Windows 存放區應用程式中呈現 Direct2D 內容，請參閱 [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)方法。

4.  從 [**交換鏈**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)取得背面緩衝區。 背景緩衝區會公開由 **交換鏈** 配置的 [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d)介面

5.  宣告 [**D2D1 \_ 點陣圖 \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) 結構並設定屬性值。 將像素格式設定為 BGRA，因為這是 [**Direct3D 裝置**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) 和 [**DXGI 裝置**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) 使用的格式。

6.  取得以 [**IDXGISurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) 傳遞至 Direct2D 的背景緩衝區。 Direct2D 不會直接接受 [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) 。

    使用 [**ID2D1DeviceCoNtext：： CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1))方法，從背景緩衝區建立 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)物件。

7.  現在 [**Direct2D 點陣圖**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 會連結至背景緩衝區。 將 [**Direct2D 裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 上的目標設定為 **點陣圖**。

## <a name="how-to-render-and-display"></a>如何呈現和顯示

現在您已有目標點陣圖，您可以使用 [**Direct2D 裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)來繪製基本、影像、影像效果和文字。 此處的程式碼會示範如何繪製矩形。


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



讓我們逐步解說上述程式碼範例中的步驟。

1.  呼叫 [**CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) 來建立筆刷來繪製矩形。
2.  發出任何繪圖命令之前，請先呼叫 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法。
3.  呼叫 [**graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) 方法來繪製要繪製的矩形和筆刷。
4.  完成繪製命令之後，請呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。
5.  藉由呼叫 [**IDXGISwapChain：:P 重發**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) 方法來顯示結果。

現在您可以使用 [**Direct2D 裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 將基本、影像、影像效果和文字繪製到螢幕。

 

 