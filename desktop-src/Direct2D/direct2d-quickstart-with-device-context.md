---
title: Windows 8 的 Direct2D 快速入門
description: 摘要說明使用 Direct2D 來繪製 Windows 8 所需的步驟，並提供範例程式碼。 Direct2D 是用來建立2D 圖形的原生程式碼 API。
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D，繪製矩形程式碼範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43442e57ed0949bdf39fc05ce1a69fded42b4b3d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406141"
---
# <a name="direct2d-quickstart-for-windows-8"></a><span data-ttu-id="62a9a-105">Windows 8 的 Direct2D 快速入門</span><span class="sxs-lookup"><span data-stu-id="62a9a-105">Direct2D Quickstart for Windows 8</span></span>

<span data-ttu-id="62a9a-106">Direct2D 是原生程式碼的立即模式 API，可用於建立2D 圖形。</span><span class="sxs-lookup"><span data-stu-id="62a9a-106">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="62a9a-107">本主題說明如何使用 Direct2D 來繪製至 [**Windows：： UI：： Core：： CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)。</span><span class="sxs-lookup"><span data-stu-id="62a9a-107">This topic illustrates how to use Direct2D to draw to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

<span data-ttu-id="62a9a-108">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="62a9a-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="62a9a-109">繪製簡單的矩形</span><span class="sxs-lookup"><span data-stu-id="62a9a-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="62a9a-110">步驟1： Include Direct2D 標頭</span><span class="sxs-lookup"><span data-stu-id="62a9a-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="62a9a-111">步驟2：建立 ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="62a9a-111">Step 2: Create an ID2D1Factory1</span></span>](#step-2-create-an-id2d1factory1)
-   [<span data-ttu-id="62a9a-112">步驟3：建立 ID2D1Device 和 ID2D1DeviceCoNtext</span><span class="sxs-lookup"><span data-stu-id="62a9a-112">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [<span data-ttu-id="62a9a-113">步驟4：建立筆刷</span><span class="sxs-lookup"><span data-stu-id="62a9a-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="62a9a-114">步驟5：繪製矩形</span><span class="sxs-lookup"><span data-stu-id="62a9a-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="62a9a-115">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="62a9a-115">Example code</span></span>](#example-code)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="62a9a-116">繪製簡單的矩形</span><span class="sxs-lookup"><span data-stu-id="62a9a-116">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="62a9a-117">若要使用 [GDI](/windows/desktop/gdi/windows-gdi)繪製矩形，您可以處理 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="62a9a-117">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


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



<span data-ttu-id="62a9a-118">使用 Direct2D 繪製相同矩形的程式碼很類似：它會建立繪圖資源、描述要繪製的圖形、繪製圖形，然後釋放繪圖資源。</span><span class="sxs-lookup"><span data-stu-id="62a9a-118">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="62a9a-119">接下來的各節將詳細說明每個步驟。</span><span class="sxs-lookup"><span data-stu-id="62a9a-119">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="62a9a-120">步驟1： Include Direct2D 標頭</span><span class="sxs-lookup"><span data-stu-id="62a9a-120">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="62a9a-121">除了應用程式所需的標頭之外，還包括 d2d1 .h 和 d2d1 \_ 1. h 標頭。</span><span class="sxs-lookup"><span data-stu-id="62a9a-121">In addition to the headers required for the application, include the d2d1.h and d2d1\_1.h headers.</span></span>

## <a name="step-2-create-an-id2d1factory1"></a><span data-ttu-id="62a9a-122">步驟2：建立 ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="62a9a-122">Step 2: Create an ID2D1Factory1</span></span>

<span data-ttu-id="62a9a-123">任何 Direct2D 範例所做的第一件事，就是建立 [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1)。</span><span class="sxs-lookup"><span data-stu-id="62a9a-123">One of the first things that any Direct2D example does is create an [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span></span>


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



<span data-ttu-id="62a9a-124">[**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1)介面是使用 Direct2D 的起點;使用 **ID2D1Factory1** 來建立 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="62a9a-124">The [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface is the starting point for using Direct2D; use an **ID2D1Factory1** to create Direct2D resources.</span></span>

<span data-ttu-id="62a9a-125">當您建立 factory 時，您可以指定它是多個還是單一執行緒。</span><span class="sxs-lookup"><span data-stu-id="62a9a-125">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="62a9a-126"> (如需多執行緒處理站的詳細資訊，請參閱 [**ID2D1Factory 參考頁面**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)上的備註。 ) 此範例會建立單一執行緒 factory。</span><span class="sxs-lookup"><span data-stu-id="62a9a-126">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="62a9a-127">一般情況下，您的應用程式應建立一次 factory，並將其保留在應用程式的存留期內。</span><span class="sxs-lookup"><span data-stu-id="62a9a-127">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a><span data-ttu-id="62a9a-128">步驟3：建立 ID2D1Device 和 ID2D1DeviceCoNtext</span><span class="sxs-lookup"><span data-stu-id="62a9a-128">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>

<span data-ttu-id="62a9a-129">建立 factory 之後，請使用它來建立 Direct2D 裝置，然後使用該裝置來建立 Direct2D 裝置內容。</span><span class="sxs-lookup"><span data-stu-id="62a9a-129">After you create a factory, use it to create a Direct2D device and then use the device to create a Direct2D device context.</span></span> <span data-ttu-id="62a9a-130">為了建立這些 Direct2D 物件，您必須擁有 [**Direct3D 11 裝置**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) 、 [**Dxgi 裝置**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)和 [**dxgi 交換鏈**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)。</span><span class="sxs-lookup"><span data-stu-id="62a9a-130">In order to create these Direct2D objects, you must have a [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , a [**DXGI device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice), and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="62a9a-131">如需建立必要必要條件的詳細資訊，請參閱 [裝置和裝置](devices-and-device-contexts.md) 內容。</span><span class="sxs-lookup"><span data-stu-id="62a9a-131">See [Devices and Device Contexts](devices-and-device-contexts.md) for info on creating the necessary prerequisites.</span></span>


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



<span data-ttu-id="62a9a-132">裝置內容是一種裝置，可執行繪圖作業，並建立與裝置相關的繪圖資源，例如筆刷。</span><span class="sxs-lookup"><span data-stu-id="62a9a-132">A device context is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="62a9a-133">您也可以使用裝置內容將 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 連結至 DXGI 介面，以做為轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="62a9a-133">You also use the device context to link a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) to a DXGI surface to use as a render target.</span></span> <span data-ttu-id="62a9a-134">裝置內容可以轉譯成不同類型的目標。</span><span class="sxs-lookup"><span data-stu-id="62a9a-134">The device context can render to different types of targets.</span></span>

<span data-ttu-id="62a9a-135">此處的程式碼會宣告點陣圖的屬性，這些屬性會連結到轉譯為 [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)的 DXGI 交換鏈。</span><span class="sxs-lookup"><span data-stu-id="62a9a-135">The code here declares the properties for bitmap that links to a DXGI swap chain that renders to a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span> <span data-ttu-id="62a9a-136">[**ID2D1DeviceCoNtext：： CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1))方法會從 DXGI 介面取得 Direct2D 介面。</span><span class="sxs-lookup"><span data-stu-id="62a9a-136">The [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method gets a Direct2D surface from the DXGI surface.</span></span> <span data-ttu-id="62a9a-137">如此一來，轉譯至目標 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 的任何動作都會轉譯至交換鏈的介面。</span><span class="sxs-lookup"><span data-stu-id="62a9a-137">This makes it so anything rendered to the target [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is rendered to the surface of the swap chain.</span></span>

<span data-ttu-id="62a9a-138">當您擁有 Direct2D 介面之後，請使用 [**ID2D1DeviceCoNtext：： SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) 方法將它設定為使用中轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="62a9a-138">Once you have the Direct2D surface, use the [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) method to set it as the active render target.</span></span>


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



## <a name="step-4-create-a-brush"></a><span data-ttu-id="62a9a-139">步驟4：建立筆刷</span><span class="sxs-lookup"><span data-stu-id="62a9a-139">Step 4: Create a Brush</span></span>

<span data-ttu-id="62a9a-140">和工廠一樣，裝置內容也可以建立繪圖資源。</span><span class="sxs-lookup"><span data-stu-id="62a9a-140">Like a factory, a device context can create drawing resources.</span></span> <span data-ttu-id="62a9a-141">在此範例中，裝置內容會建立筆刷。</span><span class="sxs-lookup"><span data-stu-id="62a9a-141">In this example, the device context creates a brush.</span></span>


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



<span data-ttu-id="62a9a-142">筆刷是繪製區域的物件，例如形狀的筆觸或幾何的填滿。</span><span class="sxs-lookup"><span data-stu-id="62a9a-142">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="62a9a-143">此範例中的筆刷繪製具有預先定義之純色的區域（黑色）。</span><span class="sxs-lookup"><span data-stu-id="62a9a-143">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="62a9a-144">Direct2D 也提供其他類型的筆刷：繪製線性和星形漸層的漸層筆刷、使用點陣圖和模式繪製的 [**點陣圖筆刷**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) ，以及從 Windows 8 開始，以轉譯影像繪製的 [**影像筆刷**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) 。</span><span class="sxs-lookup"><span data-stu-id="62a9a-144">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, a [**bitmap brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) for painting with bitmaps and patterns, and starting in Windows 8, an [**image brush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) for painting with a rendered image.</span></span>

<span data-ttu-id="62a9a-145">某些繪圖 Api 提供畫筆來繪製填滿圖案的外框和筆刷。</span><span class="sxs-lookup"><span data-stu-id="62a9a-145">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="62a9a-146">Direct2D 不同：它不會提供畫筆物件，而是會使用筆刷繪製外框和填滿圖案。</span><span class="sxs-lookup"><span data-stu-id="62a9a-146">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="62a9a-147">繪製外框時，請使用 [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) 介面，或從 Windows 8 [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) 介面開始，並使用筆刷來控制路徑的筆劃作業。</span><span class="sxs-lookup"><span data-stu-id="62a9a-147">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface, or starting in Windows 8 the [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) interface, with a brush to control path stroking operations.</span></span>

<span data-ttu-id="62a9a-148">筆刷只能搭配建立它的轉譯目標和相同資源網域中的其他轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="62a9a-148">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="62a9a-149">一般情況下，您應該建立筆刷一次，並將其保留在建立它們的呈現目標的存留期內。</span><span class="sxs-lookup"><span data-stu-id="62a9a-149">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="62a9a-150">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 是獨立的例外狀況;由於建立的成本相對較小，因此您可以在每次繪製框架時建立 **ID2D1SolidColorBrush** ，而不會影響任何明顯的效能。</span><span class="sxs-lookup"><span data-stu-id="62a9a-150">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="62a9a-151">您也可以使用單一 **ID2D1SolidColorBrush** ，只要在每次使用時都變更其色彩或不透明度。</span><span class="sxs-lookup"><span data-stu-id="62a9a-151">You can also use a single **ID2D1SolidColorBrush** and just change its color or opacity every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="62a9a-152">步驟5：繪製矩形</span><span class="sxs-lookup"><span data-stu-id="62a9a-152">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="62a9a-153">接下來，使用裝置內容來繪製矩形。</span><span class="sxs-lookup"><span data-stu-id="62a9a-153">Next, use the device context to draw the rectangle.</span></span>


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



<span data-ttu-id="62a9a-154">[**Graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))方法會採用兩個參數：要繪製的矩形，以及用來繪製矩形外框的筆刷。</span><span class="sxs-lookup"><span data-stu-id="62a9a-154">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="62a9a-155">（選擇性）您也可以指定 [筆劃寬度]、[虛線模式]、[行聯結] 和 [結束端點] 選項。</span><span class="sxs-lookup"><span data-stu-id="62a9a-155">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="62a9a-156">您必須在發出任何繪圖命令之前呼叫 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法，而且您必須在完成繪製命令之後呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。</span><span class="sxs-lookup"><span data-stu-id="62a9a-156">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="62a9a-157">**EndDraw** 方法會傳回 **HRESULT** ，指出繪圖命令是否成功。</span><span class="sxs-lookup"><span data-stu-id="62a9a-157">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span> <span data-ttu-id="62a9a-158">如果未成功，ThrowIfFailed helper 函數將會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="62a9a-158">If it is not successful, the ThrowIfFailed helper function will throw an exception.</span></span>

<span data-ttu-id="62a9a-159">[**IDXGISwapChain：:P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)重新傳送的方法會交換緩衝區介面與螢幕介面，以顯示結果。</span><span class="sxs-lookup"><span data-stu-id="62a9a-159">The [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method swaps the buffer surface with the on screen surface to display the result.</span></span>

## <a name="example-code"></a><span data-ttu-id="62a9a-160">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="62a9a-160">Example code</span></span>

<span data-ttu-id="62a9a-161">本主題中的程式碼會顯示 Direct2D 應用程式的基本元素。</span><span class="sxs-lookup"><span data-stu-id="62a9a-161">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="62a9a-162">為了簡潔起見，此主題省略了應用程式架構和錯誤處理常式代碼，該程式碼是妥善撰寫之應用程式的特性。</span><span class="sxs-lookup"><span data-stu-id="62a9a-162">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span>

 

 