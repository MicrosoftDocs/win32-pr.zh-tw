---
title: Direct2D 快速入門
description: 摘要說明使用 Direct2D 進行繪製所需的步驟，並提供範例程式碼。
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D，繪製矩形程式碼範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa59d7da057a7a9922e270d83937307762b06a40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092758"
---
# <a name="direct2d-quickstart"></a><span data-ttu-id="3d9f0-104">Direct2D 快速入門</span><span class="sxs-lookup"><span data-stu-id="3d9f0-104">Direct2D QuickStart</span></span>

<span data-ttu-id="3d9f0-105">Direct2D 是原生程式碼的立即模式 API，可用於建立2D 圖形。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-105">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="3d9f0-106">本主題說明如何在典型的 Win32 應用程式中使用 Direct2D 來繪製至 **HWND**。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-106">This topic illustrates how to use Direct2D within a typical Win32 application to draw to an **HWND**.</span></span>

> [!Note]  
> <span data-ttu-id="3d9f0-107">如果您想要建立使用 Direct2D 的 Windows Store 應用程式，請參閱 [適用于 Windows 8 主題的 Direct2D 快速入門](direct2d-quickstart-with-device-context.md) 。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-107">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="3d9f0-108">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="3d9f0-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="3d9f0-109">繪製簡單的矩形</span><span class="sxs-lookup"><span data-stu-id="3d9f0-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="3d9f0-110">步驟1： Include Direct2D 標頭</span><span class="sxs-lookup"><span data-stu-id="3d9f0-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="3d9f0-111">步驟2：建立 ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="3d9f0-111">Step 2: Create an ID2D1Factory</span></span>](#step-2-create-an-id2d1factory)
-   [<span data-ttu-id="3d9f0-112">步驟3：建立 ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="3d9f0-112">Step 3: Create an ID2D1HwndRenderTarget</span></span>](#step-3-create-an-id2d1hwndrendertarget)
-   [<span data-ttu-id="3d9f0-113">步驟4：建立筆刷</span><span class="sxs-lookup"><span data-stu-id="3d9f0-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="3d9f0-114">步驟5：繪製矩形</span><span class="sxs-lookup"><span data-stu-id="3d9f0-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="3d9f0-115">步驟6：釋放資源</span><span class="sxs-lookup"><span data-stu-id="3d9f0-115">Step 6: Release Resources</span></span>](#step-6-release-resources)
-   [<span data-ttu-id="3d9f0-116">建立簡單的 Direct2D 應用程式</span><span class="sxs-lookup"><span data-stu-id="3d9f0-116">Create a Simple Direct2D Application</span></span>](#create-a-simple-direct2d-application)
-   [<span data-ttu-id="3d9f0-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="3d9f0-117">Related topics</span></span>](#related-topics)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="3d9f0-118">繪製簡單的矩形</span><span class="sxs-lookup"><span data-stu-id="3d9f0-118">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="3d9f0-119">若要使用 [GDI](/windows/desktop/gdi/windows-gdi)繪製矩形，您可以處理 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-119">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


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



<span data-ttu-id="3d9f0-120">使用 Direct2D 繪製相同矩形的程式碼很類似：它會建立繪圖資源、描述要繪製的圖形、繪製圖形，然後釋放繪圖資源。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-120">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="3d9f0-121">接下來的各節將詳細說明每個步驟。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-121">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="3d9f0-122">步驟1： Include Direct2D 標頭</span><span class="sxs-lookup"><span data-stu-id="3d9f0-122">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="3d9f0-123">除了 Win32 應用程式所需的標頭之外，還包括 d2d1 標頭。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-123">In addition to the headers required for a Win32 application, include the d2d1.h header.</span></span>

## <a name="step-2-create-an-id2d1factory"></a><span data-ttu-id="3d9f0-124">步驟2：建立 ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="3d9f0-124">Step 2: Create an ID2D1Factory</span></span>

<span data-ttu-id="3d9f0-125">任何 Direct2D 範例所做的第一件事，就是建立 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-125">One of the first things that any Direct2D example does is create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



<span data-ttu-id="3d9f0-126">[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)介面是使用 Direct2D 的起點;使用 **ID2D1Factory** 來建立 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-126">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface is the starting point for using Direct2D; use an **ID2D1Factory** to create Direct2D resources.</span></span>

<span data-ttu-id="3d9f0-127">當您建立 factory 時，您可以指定它是多個還是單一執行緒。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-127">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="3d9f0-128"> (如需多執行緒處理站的詳細資訊，請參閱 [**ID2D1Factory 參考頁面**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)上的備註。 ) 此範例會建立單一執行緒 factory。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-128">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="3d9f0-129">一般情況下，您的應用程式應建立一次 factory，並將其保留在應用程式的存留期內。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-129">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1hwndrendertarget"></a><span data-ttu-id="3d9f0-130">步驟3：建立 ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="3d9f0-130">Step 3: Create an ID2D1HwndRenderTarget</span></span>

<span data-ttu-id="3d9f0-131">建立 factory 之後，請使用它來建立轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-131">After you create a factory, use it to create a render target.</span></span>


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



<span data-ttu-id="3d9f0-132">轉譯目標是一種裝置，可執行繪圖作業，並建立與裝置相關的繪圖資源，例如筆刷。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-132">A render target is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="3d9f0-133">不同類型的呈現目標會轉譯成不同的裝置。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-133">Different types of render targets render to different devices.</span></span> <span data-ttu-id="3d9f0-134">上述範例會使用 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)，它會呈現在螢幕的某個部分。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-134">The preceding example uses an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), which renders to a portion of the screen.</span></span>

<span data-ttu-id="3d9f0-135">可能的話，轉譯目標會使用 GPU 來加速轉譯作業和建立繪圖資源。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-135">When possible, a render target uses the GPU to accelerate rendering operations and create drawing resources.</span></span> <span data-ttu-id="3d9f0-136">否則，轉譯目標會使用 CPU 來處理轉譯指令和建立資源。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-136">Otherwise, the render target uses the CPU to process rendering instructions and create resources.</span></span> <span data-ttu-id="3d9f0-137"> (當您建立轉譯目標時，可以使用 [**D2D1 轉譯 \_ \_ 目標 \_ 類型**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) 旗標來修改此行為。 ) </span><span class="sxs-lookup"><span data-stu-id="3d9f0-137">(You can modify this behavior by using the [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) flags when you create the render target.)</span></span>

<span data-ttu-id="3d9f0-138">[**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))方法會採用三個參數。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-138">The [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method takes three parameters.</span></span> <span data-ttu-id="3d9f0-139">第一個參數是 [**D2D1 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) 結構，可指定遠端顯示選項、是否強制轉譯目標轉譯為軟體或硬體，以及 DPI。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-139">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) struct, specifies remote display options, whether to force the render target to render to software or hardware, and the DPI.</span></span> <span data-ttu-id="3d9f0-140">此範例中的程式碼會使用 [**D2D1：： RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) helper 函式來接受預設轉譯目標屬性。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-140">The code in this example uses the [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) helper function to accept default render target properties.</span></span>

<span data-ttu-id="3d9f0-141">第二個參數（ [**D2D1 \_ HWND \_ 轉譯 \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) 結構）指定要呈現內容的 **HWND** 、轉譯目標的初始大小 (以圖元為單位) ，以及其呈現 [**選項**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options)。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-141">The second parameter, a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) struct, specifies the **HWND** to which content is rendered, the initial size of the render target (in pixels), and its [**presentation options**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span></span> <span data-ttu-id="3d9f0-142">這個範例會使用 [**D2D1：： HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) helper 函數來指定 HWND 和初始大小。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-142">This example uses the [**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) helper function to specify an HWND and initial size.</span></span> <span data-ttu-id="3d9f0-143">它會使用預設的呈現選項。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-143">It uses default presentation options.</span></span>

<span data-ttu-id="3d9f0-144">第三個參數是接收呈現目標參考之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-144">The third parameter is the address of the pointer that receives the render target reference.</span></span>

<span data-ttu-id="3d9f0-145">當您建立轉譯目標並提供硬體加速時，您會在電腦的 GPU 上配置資源。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-145">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="3d9f0-146">藉由建立轉譯目標一次並保留最長的時間，您就能獲得效能優勢。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-146">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="3d9f0-147">您的應用程式應該建立轉譯目標一次，並在應用程式的存留期內保存它們，或直到收到 [**D2DERR \_ 重新建立 \_ 目標**](direct2d-error-codes.md) 錯誤為止。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-147">Your application should create render targets once and hold on to them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="3d9f0-148">當您收到此錯誤時，您必須重新建立轉譯目標 (以及它所建立) 的任何資源。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-148">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="step-4-create-a-brush"></a><span data-ttu-id="3d9f0-149">步驟4：建立筆刷</span><span class="sxs-lookup"><span data-stu-id="3d9f0-149">Step 4: Create a Brush</span></span>

<span data-ttu-id="3d9f0-150">就像 factory 一樣，轉譯目標可以建立繪圖資源。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-150">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="3d9f0-151">在此範例中，轉譯目標會建立筆刷。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-151">In this example, the render target creates a brush.</span></span>


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



<span data-ttu-id="3d9f0-152">筆刷是繪製區域的物件，例如形狀的筆觸或幾何的填滿。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-152">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="3d9f0-153">此範例中的筆刷繪製具有預先定義之純色的區域（黑色）。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-153">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="3d9f0-154">Direct2D 也會提供其他類型的筆刷：繪製線性和星形漸層的漸層筆刷，以及用點陣圖和模式繪製的點陣圖筆刷。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-154">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, and a bitmap brush for painting with bitmaps and patterns.</span></span>

<span data-ttu-id="3d9f0-155">某些繪圖 Api 提供畫筆來繪製填滿圖案的外框和筆刷。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-155">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="3d9f0-156">Direct2D 不同：它不會提供畫筆物件，而是會使用筆刷繪製外框和填滿圖案。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-156">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="3d9f0-157">繪製外框時，請搭配使用 [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) 介面與筆刷來控制路徑的筆劃作業。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-157">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface with a brush to control path stroking operations.</span></span>

<span data-ttu-id="3d9f0-158">筆刷只能搭配建立它的轉譯目標和相同資源網域中的其他轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-158">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="3d9f0-159">一般情況下，您應該建立筆刷一次，並將其保留在建立它們的呈現目標的存留期內。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-159">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="3d9f0-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 是獨立的例外狀況;由於建立的成本相對較小，因此您可以在每次繪製框架時建立 **ID2D1SolidColorBrush** ，而不會影響任何明顯的效能。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="3d9f0-161">您也可以使用單一 **ID2D1SolidColorBrush** ，只要在每次使用時都變更其色彩。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-161">You can also use a single **ID2D1SolidColorBrush** and just change its color every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="3d9f0-162">步驟5：繪製矩形</span><span class="sxs-lookup"><span data-stu-id="3d9f0-162">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="3d9f0-163">接下來，使用呈現目標來繪製矩形。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-163">Next, use the render target to draw the rectangle.</span></span>


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



<span data-ttu-id="3d9f0-164">[**Graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))方法會採用兩個參數：要繪製的矩形，以及用來繪製矩形外框的筆刷。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-164">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="3d9f0-165">（選擇性）您也可以指定 [筆劃寬度]、[虛線模式]、[行聯結] 和 [結束端點] 選項。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-165">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="3d9f0-166">您必須在發出任何繪圖命令之前呼叫 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法，而且您必須在完成繪製命令之後呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-166">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="3d9f0-167">**EndDraw** 方法會傳回 **HRESULT** ，指出繪圖命令是否成功。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-167">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span>

## <a name="step-6-release-resources"></a><span data-ttu-id="3d9f0-168">步驟6：釋放資源</span><span class="sxs-lookup"><span data-stu-id="3d9f0-168">Step 6: Release Resources</span></span>

<span data-ttu-id="3d9f0-169">如果沒有更多要繪製的框架，或當您收到 [**D2DERR \_ 重新建立 \_ 目標**](direct2d-error-codes.md) 錯誤時，請釋放轉譯目標和它所建立的任何裝置。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-169">When there are no more frames to draw, or when you receive the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error, release the render target and any devices it created.</span></span>


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



<span data-ttu-id="3d9f0-170">當您的應用程式完成使用 Direct2D 資源 (例如即將結束) 時，請釋放 Direct2D factory。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-170">When your application has finished using Direct2D resources (such as when it is about to exit), release the Direct2D factory.</span></span>


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a><span data-ttu-id="3d9f0-171">建立簡單的 Direct2D 應用程式</span><span class="sxs-lookup"><span data-stu-id="3d9f0-171">Create a Simple Direct2D Application</span></span>

<span data-ttu-id="3d9f0-172">本主題中的程式碼會顯示 Direct2D 應用程式的基本元素。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-172">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="3d9f0-173">為了簡潔起見，此主題省略了應用程式架構和錯誤處理常式代碼，該程式碼是妥善撰寫之應用程式的特性。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-173">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span> <span data-ttu-id="3d9f0-174">如需更詳細的逐步解說，以示範建立簡單 Direct2D 應用程式的完整程式碼，並示範最佳設計做法，請參閱 [建立簡單的 Direct2D 應用程式](direct2d-quickstart.md)。</span><span class="sxs-lookup"><span data-stu-id="3d9f0-174">For a more detailed walk-through that shows the complete code for creating a simple Direct2D application and demonstrates best design practices, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d9f0-175">相關主題</span><span class="sxs-lookup"><span data-stu-id="3d9f0-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d9f0-176">建立簡單的 Direct2D 應用程式</span><span class="sxs-lookup"><span data-stu-id="3d9f0-176">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

 

 