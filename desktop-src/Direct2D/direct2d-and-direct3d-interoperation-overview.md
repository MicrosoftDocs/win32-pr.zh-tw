---
title: Direct2D 和 Direct3D 互通性概觀
description: Direct2D 和 Direct3D 互通性概觀
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
ms.openlocfilehash: 1aca1eac7218528e897a2a519543d80ab4ae2be3fa5d11a4107b02f1b23f2061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698188"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a>Direct2D 和 Direct3D 互通性概觀

硬體加速的2D 和3D 圖形逐漸成為非遊戲應用程式的一部分，而大部分的遊戲應用程式都是以功能表的形式使用2D 圖形，Heads-Up 會顯示 (的 HUDs) 。 您可以藉由啟用傳統的2D 轉譯，以有效率的方式與 Direct3D 轉譯混合，來新增許多值。

本主題說明如何使用 Direct2D 和 [Direct3D](../graphics-and-multimedia.md)來整合2D 和3d 圖形。

包含以下幾節。

-   [必要條件](#prerequisites)
-   [支援的 Direct3D 版本](#supported-direct3d-versions)
-   [透過 DXGI 的互通性](#interoperability-through-dxgi)
-   [使用 DXGI 介面轉譯目標寫入至 Direct3D 介面](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [建立 DXGI 介面](#creating-a-dxgi-surface)
-   [將 Direct2D 內容寫入交換鏈緩衝區](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [範例：繪製2D 背景](#example-draw-a-2-d-background)
-   [使用 Direct2D 內容作為材質](#using-direct2d-content-as-a-texture)
    -   [範例：使用 Direct2D 內容作為材質](#example-use-direct2d-content-as-a-texture)
-   [調整 DXGI 介面呈現目標的大小](#resizing-a-dxgi-surface-render-target)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

本總覽假設您已經熟悉基本的 Direct2D 繪圖作業。 如需教學課程，請參閱 [Direct2D 快速入門](direct2d-quickstart.md)。 它也假設您可以使用 [Direct3D 10.1](/windows/desktop/direct3d10/d3d10-graphics)進行程式設計。

## <a name="supported-direct3d-versions"></a>支援的 Direct3D 版本

使用 DirectX 11.0 時，Direct2D 僅支援與 Direct3D 10.1 裝置的互通性。 使用 DirectX 11.1 或更新版本時，Direct2D 也支援與 Direct3D 11 之間的互通性。

## <a name="interoperability-through-dxgi"></a>透過 DXGI 的互通性

從 Direct3D 10，Direct3D 執行時間會使用 [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) 進行資源管理。 DXGI 執行時間層提供了影片記憶體表面的跨進程共用，並作為其他視訊記憶體執行時間平臺的基礎。 Direct2D 會使用 DXGI 來與 Direct3D 交互操作。

有兩種主要方式可搭配使用 Direct2D 和 Direct3D：

-   您可以藉由取得 [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) 並使用 [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) 來建立 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)，將 Direct2D 內容寫入至 Direct3D 介面。 然後，您可以使用轉譯目標將二維介面或背景新增至三維圖形，或使用 Direct2D 繪圖作為三維度物件的材質。
-   藉由使用 [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)來建立 [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ，您可以將 Direct3D 場景寫入點陣圖，並使用 Direct2D 來呈現。

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a>使用 DXGI 介面轉譯目標寫入至 Direct3D 介面

若要寫入 Direct3D 介面，您可以取得 [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) 並將它傳遞至 [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) 方法，以建立 DXGI 介面轉譯目標。 然後，您可以使用 DXGI 介面轉譯目標，將2D 內容繪製到 DXGI 表面。

DXGI 介面轉譯目標是一種 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)。 如同其他 Direct2D 轉譯目標，您可以使用它來建立資源和發出繪製命令。

DXGI 介面轉譯目標和 DXGI 介面必須使用相同的 DXGI 格式。 如果您在建立轉譯目標時指定 [**DXGI \_ 格式 \_ 未知**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式，它會自動使用介面的格式。

DXGI 介面轉譯目標不會執行 DXGI 介面同步處理。

### <a name="creating-a-dxgi-surface"></a>建立 DXGI 介面

使用 Direct3D 10 時，有數種方式可取得 DXGI 介面。 您可以建立裝置的 [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) ，然後使用交換鏈的 [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) 方法來取得 DXGI 表面。 或者，您可以使用裝置來建立材質，然後使用該材質作為 DXGI 表面。

無論您如何建立 DXGI 介面，介面都必須使用 DXGI 介面轉譯目標所支援的其中一個 DXGI 格式。 如需清單，請參閱 [支援的像素格式和 Alpha 模式](supported-pixel-formats-and-alpha-modes.md)。

此外，與 DXGI 介面相關聯的 [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) 必須支援 BGRA DXGI 格式，才能讓介面與 Direct2D 搭配使用。 若要確保此支援，請在呼叫 [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1)方法來建立裝置時，使用 [**D3D10 \_ create \_ device \_ BGRA \_ support**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag)旗標。

下列程式碼會定義建立 [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1)的方法。 它會選取可用的最佳功能等級，並在無法使用硬體轉譯時，切換回[Windows 的 Advanced 點陣化平臺 (變形) ](./installing-the-direct2d-debug-layer.md) 。


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



下一個程式碼範例 `CreateD3DDevice` 會使用前一個範例中所示的方法，來建立可建立可與 Direct2D 搭配使用的 DXGI 介面的 Direct3D 裝置。


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



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a>將 Direct2D 內容寫入交換鏈緩衝區

將 Direct2D 內容新增至 Direct3D 場景最簡單的方式，就是使用 [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)的 [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)方法來取得 DXGI 介面，然後使用具有 [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))方法的介面來建立用來繪製2d 內容的 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 。

這種方法不會以三個維度轉譯您的內容;它不會有觀點或深度。 不過，這對幾個常見的工作很有用：

-   建立立體場景的2-d 背景。
-   在3-d 場景前方建立2D 介面。
-   轉譯 Direct2D 內容時，使用 Direct3D 取樣。

下一節將說明如何建立3-d 場景的2D 背景。

### <a name="example-draw-a-2-d-background"></a>範例：繪製2D 背景

下列步驟描述如何建立 DXGI 介面轉譯目標，並用它來繪製漸層背景。

1.  您可以使用 [**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) 方法來建立 [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (*m \_ pDevice* 變數) 的交換鏈。 交換鏈使用 [**dxgi \_ 格式 \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI 格式，這是 DIRECT2D 支援的其中一個 dxgi 格式。

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

    

2.  使用交換鏈的 [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) 方法來取得 DXGI 介面。

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  使用 DXGI 介面建立 DXGI 轉譯目標。
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



    

4.  使用呈現目標來繪製漸層背景。

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



    

此範例中省略了程式碼。

## <a name="using-direct2d-content-as-a-texture"></a>使用 Direct2D 內容作為材質

搭配使用 Direct2D 內容與 Direct3D 的另一種方式是使用 Direct2D 來產生2D 材質，然後將該材質套用至3D 模型。 若要這麼做，您可以建立 [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)、從材質取得 DXGI 介面，然後使用介面建立 dxgi 表面轉譯目標。 **ID3D10Texture2D** 介面必須使用 D3D10 系結轉譯 [**\_ \_ \_ 目標**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag)系結旗標，並使用 DXGI 介面轉譯目標所支援的 dxgi 格式。 如需支援的 DXGI 格式清單，請參閱 [支援的像素格式和 Alpha 模式](supported-pixel-formats-and-alpha-modes.md)。

### <a name="example-use-direct2d-content-as-a-texture"></a>範例：使用 Direct2D 內容作為材質

下列範例示範如何建立可轉譯成2D 材質 (（由 [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)) 代表）的 DXGI 介面轉譯目標。

1.  首先，使用 Direct3D 裝置來建立2D 材質。 紋理會使用 D3D10 系結轉譯 [**\_ \_ \_ 目標**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) 和 **D3D10 系結 \_ \_ 著色器 \_ 資源** 系結旗標，並使用 [**dxgi \_ 格式 \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI 格式（Direct2D 所支援的其中一個 dxgi 格式）。

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

    

2.  使用紋理來取得 DXGI 表面。

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  使用具有 [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) 方法的介面來取得 Direct2D 轉譯目標。

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



    

現在您已取得 Direct2D 轉譯目標，並將其與 Direct3D 材質相關聯，您可以使用轉譯目標將 Direct2D 內容繪製至該材質，也可以將該材質套用至 Direct3D 基本專案。

此範例中省略了程式碼。

## <a name="resizing-a-dxgi-surface-render-target"></a>調整 DXGI 介面呈現目標的大小

DXGI 介面轉譯目標不支援 [**ID2D1RenderTarget：： Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) 方法。 若要調整 DXGI 介面轉譯目標的大小，應用程式必須釋放並重新建立。

這種作業可能會造成效能問題。 轉譯目標可能是最後一個使用中的 Direct2D 資源，它會保留與轉譯目標之 DXGI 介面相關聯之 [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) 的參考。 如果應用程式釋出轉譯目標，並終結 **ID3D10Device1** 參考，則必須重新建立新的參考。

您可以在重新建立轉譯目標時，保留轉譯目標所建立的至少一個 Direct2D 資源，以避免這項可能耗費資源的作業。 以下是一些適用于此方法的 Direct2D 資源：

-   [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)可以間接保留的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) () 
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

為了配合此方法，您的調整大小方法應該會進行測試，以查看 Direct3D 裝置是否可用。 如果可用，請釋放並重新建立您的 DXGI 介面轉譯目標，但保留先前建立的所有資源並重複使用。 這項功能的運作方式是因為如 [資源總覽](resources-and-resource-domains.md)所述，當兩個轉譯目標都與相同的 Direct3D 裝置相關聯時，兩個轉譯目標所建立的資源都是相容的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[支援的像素格式和 Alpha 模式](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))
</dt> <dt>

[WindowsDirectX 圖形](../graphics-and-multimedia.md)
</dt> </dl>

 

 
