---
title: 呈現目標、裝置和資源
description: 呈現目標、裝置和資源
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeddd84e12c52e0fd0ae82dab8b5e8741a2e0891
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314929"
---
# <a name="render-targets-devices-and-resources"></a><span data-ttu-id="3de02-103">呈現目標、裝置和資源</span><span class="sxs-lookup"><span data-stu-id="3de02-103">Render Targets, Devices, and Resources</span></span>

<span data-ttu-id="3de02-104">轉譯 *目標* 只是程式將繪製的位置。</span><span class="sxs-lookup"><span data-stu-id="3de02-104">A *render target* is simply the location where your program will draw.</span></span> <span data-ttu-id="3de02-105">通常，轉譯目標是視窗 (特別是視窗的工作區) 。</span><span class="sxs-lookup"><span data-stu-id="3de02-105">Typically, the render target is a window (specifically, the client area of the window).</span></span> <span data-ttu-id="3de02-106">它也可以是記憶體中未顯示的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="3de02-106">It could also be a bitmap in memory that is not displayed.</span></span> <span data-ttu-id="3de02-107">轉譯目標會以 [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="3de02-107">A render target is represented by the [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span>

<span data-ttu-id="3de02-108">*裝置* 是一種抽象概念，代表實際繪製圖元的任何內容。</span><span class="sxs-lookup"><span data-stu-id="3de02-108">A *device* is an abstraction that represents whatever actually draws the pixels.</span></span> <span data-ttu-id="3de02-109">硬體裝置使用 GPU 以加快效能，而軟體裝置則使用 CPU。</span><span class="sxs-lookup"><span data-stu-id="3de02-109">A hardware device uses the GPU for faster performance, whereas a software device uses the CPU.</span></span> <span data-ttu-id="3de02-110">應用程式不會建立裝置。</span><span class="sxs-lookup"><span data-stu-id="3de02-110">The application does not create the device.</span></span> <span data-ttu-id="3de02-111">相反地，當應用程式建立轉譯目標時，會隱含地建立裝置。</span><span class="sxs-lookup"><span data-stu-id="3de02-111">Instead, the device is created implicitly when the application creates the render target.</span></span> <span data-ttu-id="3de02-112">每個轉譯目標都與特定裝置相關聯，也就是硬體或軟體。</span><span class="sxs-lookup"><span data-stu-id="3de02-112">Each render target is associated with a particular device, either hardware or software.</span></span>

![顯示呈現目標和裝置之間關聯性的圖表。](images/graphics09.png)

<span data-ttu-id="3de02-114">*資源* 是程式用來繪製的物件。</span><span class="sxs-lookup"><span data-stu-id="3de02-114">A *resource* is an object that the program uses for drawing.</span></span> <span data-ttu-id="3de02-115">以下是 Direct2D 中定義的一些資源範例：</span><span class="sxs-lookup"><span data-stu-id="3de02-115">Here are some examples of resources that are defined in Direct2D:</span></span>

-   <span data-ttu-id="3de02-116">**筆刷**。</span><span class="sxs-lookup"><span data-stu-id="3de02-116">**Brush**.</span></span> <span data-ttu-id="3de02-117">控制線條和區域的繪製方式。</span><span class="sxs-lookup"><span data-stu-id="3de02-117">Controls how lines and regions are painted.</span></span> <span data-ttu-id="3de02-118">筆刷類型包含純色筆刷和漸層筆刷。</span><span class="sxs-lookup"><span data-stu-id="3de02-118">Brush types include solid-color brushes and gradient brushes.</span></span>
-   <span data-ttu-id="3de02-119">**筆觸樣式**。</span><span class="sxs-lookup"><span data-stu-id="3de02-119">**Stroke style**.</span></span> <span data-ttu-id="3de02-120">控制線條的外觀，例如虛線或純色。</span><span class="sxs-lookup"><span data-stu-id="3de02-120">Controls the appearance of a line—for example, dashed or solid.</span></span>
-   <span data-ttu-id="3de02-121">**Geometry**。</span><span class="sxs-lookup"><span data-stu-id="3de02-121">**Geometry**.</span></span> <span data-ttu-id="3de02-122">表示線條和曲線的集合。</span><span class="sxs-lookup"><span data-stu-id="3de02-122">Represents a collection of lines and curves.</span></span>
-   <span data-ttu-id="3de02-123">**網格**。</span><span class="sxs-lookup"><span data-stu-id="3de02-123">**Mesh**.</span></span> <span data-ttu-id="3de02-124">由三角形組成的圖形。</span><span class="sxs-lookup"><span data-stu-id="3de02-124">A shape formed out of triangles.</span></span> <span data-ttu-id="3de02-125">不同于幾何資料（必須在轉譯之前轉換），GPU 可以直接使用網格資料。</span><span class="sxs-lookup"><span data-stu-id="3de02-125">Mesh data can be consumed directly by the GPU, unlike geometry data, which must be converted before rendering.</span></span>

<span data-ttu-id="3de02-126">轉譯目標也會被視為一種資源類型。</span><span class="sxs-lookup"><span data-stu-id="3de02-126">Render targets are also considered a type of resource.</span></span>

<span data-ttu-id="3de02-127">有些資源會因硬體加速而受益。</span><span class="sxs-lookup"><span data-stu-id="3de02-127">Some resources benefit from hardware acceleration.</span></span> <span data-ttu-id="3de02-128">此類型的資源一律與特定裝置相關聯，也就是硬體 (GPU) 或軟體 (CPU) 。</span><span class="sxs-lookup"><span data-stu-id="3de02-128">A resource of this type is always associated with a particular device, either hardware (GPU) or software (CPU).</span></span> <span data-ttu-id="3de02-129">這種類型的資源稱為 *裝置相依*。</span><span class="sxs-lookup"><span data-stu-id="3de02-129">This type of resource is called *device-dependent*.</span></span> <span data-ttu-id="3de02-130">筆刷和網格是與裝置相關的資源範例。</span><span class="sxs-lookup"><span data-stu-id="3de02-130">Brushes and meshes are examples of device-dependent resources.</span></span> <span data-ttu-id="3de02-131">如果裝置變得無法使用，就必須為新裝置重新建立資源。</span><span class="sxs-lookup"><span data-stu-id="3de02-131">If the device becomes unavailable, the resource must be re-created for a new device.</span></span>

<span data-ttu-id="3de02-132">無論使用何種裝置，其他資源都會保留在 CPU 記憶體中。</span><span class="sxs-lookup"><span data-stu-id="3de02-132">Other resources are kept in CPU memory, regardless of what device is used.</span></span> <span data-ttu-id="3de02-133">這些資源與 *裝置無關*，因為它們並未與特定裝置建立關聯。</span><span class="sxs-lookup"><span data-stu-id="3de02-133">These resources are *device-independent*, because they are not associated with a particular device.</span></span> <span data-ttu-id="3de02-134">裝置變更時，並不需要重新建立與裝置無關的資源。</span><span class="sxs-lookup"><span data-stu-id="3de02-134">It is not necessary to re-create device-independent resources when the device changes.</span></span> <span data-ttu-id="3de02-135">筆觸樣式和幾何是與裝置無關的資源。</span><span class="sxs-lookup"><span data-stu-id="3de02-135">Stroke styles and geometries are device-independent resources.</span></span>

<span data-ttu-id="3de02-136">每個資源的 MSDN 檔會指出資源是與裝置相關或與裝置無關。</span><span class="sxs-lookup"><span data-stu-id="3de02-136">The MSDN documentation for each resource states whether the resource is device-dependent or device-independent.</span></span> <span data-ttu-id="3de02-137">每個資源類型都是以衍生自 [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource)的介面表示。</span><span class="sxs-lookup"><span data-stu-id="3de02-137">Every resource type is represented by an interface that derives from [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource).</span></span> <span data-ttu-id="3de02-138">例如，筆刷會以 [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) 介面表示。</span><span class="sxs-lookup"><span data-stu-id="3de02-138">For example, brushes are represented by the [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) interface.</span></span>

## <a name="the-direct2d-factory-object"></a><span data-ttu-id="3de02-139">Direct2D Factory 物件</span><span class="sxs-lookup"><span data-stu-id="3de02-139">The Direct2D Factory Object</span></span>

<span data-ttu-id="3de02-140">使用 Direct2D 的第一個步驟是建立 Direct2D factory 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="3de02-140">The first step when using Direct2D is to create an instance of the Direct2D factory object.</span></span> <span data-ttu-id="3de02-141">在電腦程式設計中， *factory* 是建立其他物件的物件。</span><span class="sxs-lookup"><span data-stu-id="3de02-141">In computer programming, a *factory* is an object that creates other objects.</span></span> <span data-ttu-id="3de02-142">Direct2D factory 會建立下列類型的物件：</span><span class="sxs-lookup"><span data-stu-id="3de02-142">The Direct2D factory creates the following types of objects:</span></span>

-   <span data-ttu-id="3de02-143">呈現目標。</span><span class="sxs-lookup"><span data-stu-id="3de02-143">Render targets.</span></span>
-   <span data-ttu-id="3de02-144">與裝置無關的資源，例如筆劃樣式和幾何。</span><span class="sxs-lookup"><span data-stu-id="3de02-144">Device-independent resources, such as stroke styles and geometries.</span></span>

<span data-ttu-id="3de02-145">裝置依存資源（例如筆刷和點陣圖）是由轉譯目標物件所建立。</span><span class="sxs-lookup"><span data-stu-id="3de02-145">Device-dependent resources, such as brushes and bitmaps, are created by the render target object.</span></span>

![顯示 direct2d factory 的圖表。](images/graphics10.png)

<span data-ttu-id="3de02-147">若要建立 Direct2D factory 物件，請呼叫 [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) 函數。</span><span class="sxs-lookup"><span data-stu-id="3de02-147">To create the Direct2D factory object, call the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



<span data-ttu-id="3de02-148">第一個參數是指定建立選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="3de02-148">The first parameter is a flag that specifies creation options.</span></span> <span data-ttu-id="3de02-149">**D2D1 \_ FACTORY 型 \_ 別 \_ 單個 \_ 執行緒** 旗標表示您將不會從多個執行緒呼叫 Direct2D。</span><span class="sxs-lookup"><span data-stu-id="3de02-149">The **D2D1\_FACTORY\_TYPE\_SINGLE\_THREADED** flag means that you will not call Direct2D from multiple threads.</span></span> <span data-ttu-id="3de02-150">若要支援來自多個執行緒的呼叫，請指定 **D2D1 \_ FACTORY \_ 類型 \_ 多 \_ 執行緒**。</span><span class="sxs-lookup"><span data-stu-id="3de02-150">To support calls from multiple threads, specify **D2D1\_FACTORY\_TYPE\_MULTI\_THREADED**.</span></span> <span data-ttu-id="3de02-151">如果您的程式使用單一執行緒來呼叫 Direct2D，則單一執行緒選項更有效率。</span><span class="sxs-lookup"><span data-stu-id="3de02-151">If your program uses a single thread to call into Direct2D, the single-threaded option is more efficient.</span></span>

<span data-ttu-id="3de02-152">[**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)函數的第二個參數會接收 [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="3de02-152">The second parameter to the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function receives a pointer to the [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) interface.</span></span>

<span data-ttu-id="3de02-153">您應該在第一個 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息之前建立 Direct2D factory 物件。</span><span class="sxs-lookup"><span data-stu-id="3de02-153">You should create the Direct2D factory object before the first [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="3de02-154">[**WM \_ 建立**](/windows/desktop/winmsg/wm-create)訊息處理常式是建立 factory 的絕佳位置：</span><span class="sxs-lookup"><span data-stu-id="3de02-154">The [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message handler is a good place to create the factory:</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a><span data-ttu-id="3de02-155">建立 Direct2D 資源</span><span class="sxs-lookup"><span data-stu-id="3de02-155">Creating Direct2D Resources</span></span>

<span data-ttu-id="3de02-156">Circle 程式會使用下列與裝置相關的資源：</span><span class="sxs-lookup"><span data-stu-id="3de02-156">The Circle program uses the following device-dependent resources:</span></span>

-   <span data-ttu-id="3de02-157">與應用程式視窗相關聯的呈現目標。</span><span class="sxs-lookup"><span data-stu-id="3de02-157">A render target that is associated with the application window.</span></span>
-   <span data-ttu-id="3de02-158">用來繪製圓形的單色筆刷。</span><span class="sxs-lookup"><span data-stu-id="3de02-158">A solid-color brush to paint the circle.</span></span>

<span data-ttu-id="3de02-159">每個資源都是以 COM 介面表示：</span><span class="sxs-lookup"><span data-stu-id="3de02-159">Each of these resources is represented by a COM interface:</span></span>

-   <span data-ttu-id="3de02-160">[**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget)介面代表呈現目標。</span><span class="sxs-lookup"><span data-stu-id="3de02-160">The [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) interface represents the render target.</span></span>
-   <span data-ttu-id="3de02-161">[**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush)介面代表筆刷。</span><span class="sxs-lookup"><span data-stu-id="3de02-161">The [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interface represents the brush.</span></span>

<span data-ttu-id="3de02-162">Circle 程式會將這些介面的指標儲存為類別的成員變數 `MainWindow` ：</span><span class="sxs-lookup"><span data-stu-id="3de02-162">The Circle program stores pointers to these interfaces as member variables of the `MainWindow` class:</span></span>


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



<span data-ttu-id="3de02-163">下列程式碼會建立這兩個資源。</span><span class="sxs-lookup"><span data-stu-id="3de02-163">The following code creates these two resources.</span></span>


```C++
HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}
```



<span data-ttu-id="3de02-164">若要建立視窗的呈現目標，請在 Direct2D factory 上呼叫 [**ID2D1Factory：： CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) 方法。</span><span class="sxs-lookup"><span data-stu-id="3de02-164">To create a render target for a window, call the [**ID2D1Factory::CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method on the Direct2D factory.</span></span>

-   <span data-ttu-id="3de02-165">第一個參數會指定任何類型之轉譯目標通用的選項。</span><span class="sxs-lookup"><span data-stu-id="3de02-165">The first parameter specifies options that are common to any type of render target.</span></span> <span data-ttu-id="3de02-166">在這裡，我們會藉由呼叫 helper 函式 [**D2D1：： RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties)來傳遞預設選項。</span><span class="sxs-lookup"><span data-stu-id="3de02-166">Here, we pass in default options by calling the helper function [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).</span></span>
-   <span data-ttu-id="3de02-167">第二個參數指定視窗的控制碼加上轉譯目標的大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="3de02-167">The second parameter specifies the handle to the window plus the size of the render target, in pixels.</span></span>
-   <span data-ttu-id="3de02-168">第三個參數會接收 [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 指標。</span><span class="sxs-lookup"><span data-stu-id="3de02-168">The third parameter receives an [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) pointer.</span></span>

<span data-ttu-id="3de02-169">若要建立單色筆刷，請在呈現目標上呼叫 [**ID2D1RenderTarget：： CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) 方法。</span><span class="sxs-lookup"><span data-stu-id="3de02-169">To create the solid-color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method on the render target.</span></span> <span data-ttu-id="3de02-170">色彩會以 [**D2D1 \_ 色 \_ F**](/windows/desktop/Direct2D/d2d1-color-f) 值的形式提供。</span><span class="sxs-lookup"><span data-stu-id="3de02-170">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) value.</span></span> <span data-ttu-id="3de02-171">如需 Direct2D 中色彩的詳細資訊，請參閱 [在 Direct2D 中使用色彩](using-color-in-direct2d.md)。</span><span class="sxs-lookup"><span data-stu-id="3de02-171">For more information about colors in Direct2D, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>

<span data-ttu-id="3de02-172">另請注意，如果轉譯目標已存在，則 `CreateGraphicsResources` 方法會傳回 **\_ [確定]** ，而不執行任何操作。</span><span class="sxs-lookup"><span data-stu-id="3de02-172">Also, notice that if the render target already exists, the `CreateGraphicsResources` method returns **S\_OK** without doing anything.</span></span> <span data-ttu-id="3de02-173">在下一個主題中，這項設計的原因將會明顯。</span><span class="sxs-lookup"><span data-stu-id="3de02-173">The reason for this design will become clear in the next topic.</span></span>

## <a name="next"></a><span data-ttu-id="3de02-174">下一個</span><span class="sxs-lookup"><span data-stu-id="3de02-174">Next</span></span>

[<span data-ttu-id="3de02-175">使用 Direct2D 繪製</span><span class="sxs-lookup"><span data-stu-id="3de02-175">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)

 

 