---
title: Windows 8 的 Direct2D 快速入門
description: 摘要說明使用 Direct2D 來繪製 Windows 8 所需的步驟，並提供範例程式碼。 Direct2D 是用來建立2D 圖形的原生程式碼 API。
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D，繪製矩形程式碼範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3fd732d1d18cd731f6e6caa46f456f4896f47f778f8edc824442dfee5f6ac4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825429"
---
# <a name="direct2d-quickstart-for-windows-8"></a>Windows 8 的 Direct2D 快速入門

Direct2D 是原生程式碼的立即模式 API，可用於建立2D 圖形。 本主題說明如何使用 Direct2D 來繪製至 [**Windows：： UI：： Core：： CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)。

本主題包含下列幾節：

-   [繪製簡單的矩形](#drawing-a-simple-rectangle)
-   [步驟1： Include Direct2D 標頭](#step-1-include-direct2d-header)
-   [步驟2：建立 ID2D1Factory1](#step-2-create-an-id2d1factory1)
-   [步驟3：建立 ID2D1Device 和 ID2D1DeviceCoNtext](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [步驟4：建立筆刷](#step-4-create-a-brush)
-   [步驟5：繪製矩形](#step-5-draw-the-rectangle)
-   [範例程式碼](#example-code)

## <a name="drawing-a-simple-rectangle"></a>繪製簡單的矩形

若要使用 [GDI](/windows/desktop/gdi/windows-gdi)繪製矩形，您可以處理 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息，如下列程式碼所示。


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



使用 Direct2D 繪製相同矩形的程式碼很類似：它會建立繪圖資源、描述要繪製的圖形、繪製圖形，然後釋放繪圖資源。 接下來的各節將詳細說明每個步驟。

## <a name="step-1-include-direct2d-header"></a>步驟1： Include Direct2D 標頭

除了應用程式所需的標頭之外，還包括 d2d1 .h 和 d2d1 \_ 1. h 標頭。

## <a name="step-2-create-an-id2d1factory1"></a>步驟2：建立 ID2D1Factory1

任何 Direct2D 範例所做的第一件事，就是建立 [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1)。


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



[**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1)介面是使用 Direct2D 的起點;使用 **ID2D1Factory1** 來建立 Direct2D 資源。

當您建立 factory 時，您可以指定它是多個還是單一執行緒。  (如需多執行緒處理站的詳細資訊，請參閱 [**ID2D1Factory 參考頁面**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)上的備註。 ) 此範例會建立單一執行緒 factory。

一般情況下，您的應用程式應建立一次 factory，並將其保留在應用程式的存留期內。

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a>步驟3：建立 ID2D1Device 和 ID2D1DeviceCoNtext

建立 factory 之後，請使用它來建立 Direct2D 裝置，然後使用該裝置來建立 Direct2D 裝置內容。 為了建立這些 Direct2D 物件，您必須擁有 [**Direct3D 11 裝置**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) 、 [**Dxgi 裝置**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)和 [**dxgi 交換鏈**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)。 如需建立必要必要條件的詳細資訊，請參閱 [裝置和裝置](devices-and-device-contexts.md) 內容。


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



裝置內容是一種裝置，可執行繪圖作業，並建立與裝置相關的繪圖資源，例如筆刷。 您也可以使用裝置內容將 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 連結至 DXGI 介面，以做為轉譯目標使用。 裝置內容可以轉譯成不同類型的目標。

此處的程式碼會宣告點陣圖的屬性，這些屬性會連結到轉譯為 [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)的 DXGI 交換鏈。 [**ID2D1DeviceCoNtext：： CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1))方法會從 DXGI 介面取得 Direct2D 介面。 如此一來，轉譯至目標 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 的任何動作都會轉譯至交換鏈的介面。

當您擁有 Direct2D 介面之後，請使用 [**ID2D1DeviceCoNtext：： SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) 方法將它設定為使用中轉譯目標。


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
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

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a>步驟4：建立筆刷

和工廠一樣，裝置內容也可以建立繪圖資源。 在此範例中，裝置內容會建立筆刷。


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



筆刷是繪製區域的物件，例如形狀的筆觸或幾何的填滿。 此範例中的筆刷繪製具有預先定義之純色的區域（黑色）。

Direct2D 也提供其他類型的筆刷：繪製線性和星形漸層的漸層筆刷、使用點陣圖和模式繪製的 [**點陣圖筆刷**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)，以及從 Windows 8 開始，以轉譯影像繪製的 [**影像筆刷**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)。

某些繪圖 Api 提供畫筆來繪製填滿圖案的外框和筆刷。 Direct2D 不同：它不會提供畫筆物件，而是會使用筆刷繪製外框和填滿圖案。 繪製外框時，請使用 [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)介面，或從 Windows 8 [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1)介面開始，並使用筆刷來控制路徑的筆劃作業。

筆刷只能搭配建立它的轉譯目標和相同資源網域中的其他轉譯目標使用。 一般情況下，您應該建立筆刷一次，並將其保留在建立它們的呈現目標的存留期內。 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 是獨立的例外狀況;由於建立的成本相對較小，因此您可以在每次繪製框架時建立 **ID2D1SolidColorBrush** ，而不會影響任何明顯的效能。 您也可以使用單一 **ID2D1SolidColorBrush** ，只要在每次使用時都變更其色彩或不透明度。

## <a name="step-5-draw-the-rectangle"></a>步驟5：繪製矩形

接下來，使用裝置內容來繪製矩形。


```C++
 
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



[**Graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))方法會採用兩個參數：要繪製的矩形，以及用來繪製矩形外框的筆刷。 （選擇性）您也可以指定 [筆劃寬度]、[虛線模式]、[行聯結] 和 [結束端點] 選項。

您必須在發出任何繪圖命令之前呼叫 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法，而且您必須在完成繪製命令之後呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。 **EndDraw** 方法會傳回 **HRESULT** ，指出繪圖命令是否成功。 如果未成功，ThrowIfFailed helper 函數將會擲回例外狀況。

[**IDXGISwapChain：:P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)重新傳送的方法會交換緩衝區介面與螢幕介面，以顯示結果。

## <a name="example-code"></a>程式碼範例

本主題中的程式碼會顯示 Direct2D 應用程式的基本元素。 為了簡潔起見，此主題省略了應用程式架構和錯誤處理常式代碼，該程式碼是妥善撰寫之應用程式的特性。

 

 