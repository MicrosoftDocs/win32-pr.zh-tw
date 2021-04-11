---
title: 轉譯目標總覽
description: 描述不同類型的 Direct2D 轉譯目標，以及如何使用它們。
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D，轉譯目標
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933366"
---
# <a name="render-targets-overview"></a><span data-ttu-id="4e826-104">轉譯目標總覽</span><span class="sxs-lookup"><span data-stu-id="4e826-104">Render Targets Overview</span></span>

<span data-ttu-id="4e826-105">轉譯目標是繼承自 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 介面的資源。</span><span class="sxs-lookup"><span data-stu-id="4e826-105">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="4e826-106">轉譯目標會建立用來繪製和執行實際繪圖作業的資源。</span><span class="sxs-lookup"><span data-stu-id="4e826-106">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="4e826-107">本主題說明不同類型的 Direct2D 轉譯目標，以及如何使用它們。</span><span class="sxs-lookup"><span data-stu-id="4e826-107">This topic describes the different types of Direct2D render targets and how to use them.</span></span>

-   [<span data-ttu-id="4e826-108">呈現目標</span><span class="sxs-lookup"><span data-stu-id="4e826-108">Render Targets</span></span>](#render-targets-overview)
    -   [<span data-ttu-id="4e826-109">呈現目標功能</span><span class="sxs-lookup"><span data-stu-id="4e826-109">Render Target Features</span></span>](#render-target-features)
    -   [<span data-ttu-id="4e826-110">呈現目標資源</span><span class="sxs-lookup"><span data-stu-id="4e826-110">Render Target Resources</span></span>](#render-target-resources)
    -   [<span data-ttu-id="4e826-111">繪製命令</span><span class="sxs-lookup"><span data-stu-id="4e826-111">Drawing Commands</span></span>](#drawing-commands)
    -   [<span data-ttu-id="4e826-112">錯誤處理</span><span class="sxs-lookup"><span data-stu-id="4e826-112">Error Handling</span></span>](#error-handling)
-   [<span data-ttu-id="4e826-113">範例：將內容呈現至視窗</span><span class="sxs-lookup"><span data-stu-id="4e826-113">Example: Render Content to a Window</span></span>](#example-render-content-to-a-window)

## <a name="render-targets"></a><span data-ttu-id="4e826-114">呈現目標</span><span class="sxs-lookup"><span data-stu-id="4e826-114">Render Targets</span></span>

<span data-ttu-id="4e826-115">轉譯目標是繼承自 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 介面的資源。</span><span class="sxs-lookup"><span data-stu-id="4e826-115">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="4e826-116">轉譯目標會建立用來繪製和執行實際繪圖作業的資源。</span><span class="sxs-lookup"><span data-stu-id="4e826-116">A render target creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="4e826-117">有幾種轉譯目標可用於以下列方式呈現圖形：</span><span class="sxs-lookup"><span data-stu-id="4e826-117">There are several kinds of render targets that can be used to render graphics in the following ways:</span></span>

-   <span data-ttu-id="4e826-118">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 物件會將內容轉譯至視窗。</span><span class="sxs-lookup"><span data-stu-id="4e826-118">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) objects render content to a window.</span></span>
-   <span data-ttu-id="4e826-119">[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) 物件會轉譯成 GDI 裝置內容。</span><span class="sxs-lookup"><span data-stu-id="4e826-119">[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) objects render to a GDI device context.</span></span>
-   <span data-ttu-id="4e826-120">點陣圖轉譯目標物件會將內容轉譯為非螢幕點陣圖。</span><span class="sxs-lookup"><span data-stu-id="4e826-120">Bitmap render target objects render content to an off-screen bitmap.</span></span>
-   <span data-ttu-id="4e826-121">DXGI 轉譯目標物件會轉譯成 DXGI 介面，以搭配 Direct3D 使用。</span><span class="sxs-lookup"><span data-stu-id="4e826-121">DXGI render target objects render to a DXGI surface for use with Direct3D.</span></span>

<span data-ttu-id="4e826-122">由於轉譯目標是與特定轉譯裝置相關聯，因此它是裝置相依的資源，如果裝置已移除，就會停止運作。</span><span class="sxs-lookup"><span data-stu-id="4e826-122">Because a render target is associated with a particular rendering device, it is a device-dependent resource and ceases to function if the device is removed.</span></span>

### <a name="render-target-features"></a><span data-ttu-id="4e826-123">呈現目標功能</span><span class="sxs-lookup"><span data-stu-id="4e826-123">Render Target Features</span></span>

<span data-ttu-id="4e826-124">您可以指定轉譯目標是否使用硬體加速，以及遠端顯示是否由本機或遠端電腦所呈現。</span><span class="sxs-lookup"><span data-stu-id="4e826-124">You can specify whether a render target uses hardware acceleration and whether remote display is rendered by a local or a remote computer.</span></span> <span data-ttu-id="4e826-125">您可以設定呈現目標，以進行別名或反鋸齒呈現。</span><span class="sxs-lookup"><span data-stu-id="4e826-125">Render targets can be set up for aliased or antialiased rendering.</span></span> <span data-ttu-id="4e826-126">針對具有大量基本專案的轉譯場景，開發人員也可以在別名模式中轉譯2D 圖形，並使用 D3D 多取樣消除鋸齒來達成更高的擴充性。</span><span class="sxs-lookup"><span data-stu-id="4e826-126">For rendering scenes with a large number of primitives, a developer can also render 2-D graphics in aliased mode and use D3D multisample antialiasing to achieve greater scalability.</span></span>

<span data-ttu-id="4e826-127">轉譯目標也可以將繪圖作業分組為 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) 介面所代表的圖層。</span><span class="sxs-lookup"><span data-stu-id="4e826-127">Render targets can also group drawing operations into layers represented by the [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) interface.</span></span> <span data-ttu-id="4e826-128">當轉譯畫面格時，圖層會用來收集要組合在一起的繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="4e826-128">Layers are useful for collecting drawing operations to be composited together when rendering a frame.</span></span> <span data-ttu-id="4e826-129">在某些案例中，這可能是轉譯成點陣圖轉譯目標的實用替代方式，然後重複使用點陣圖內容，因為階層式配置成本低於 [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)。</span><span class="sxs-lookup"><span data-stu-id="4e826-129">For some scenarios, this can be a useful alternative to rendering to a bitmap render target, and then reusing the bitmap contents, as allocation costs for layering are lower than for an [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).</span></span>

<span data-ttu-id="4e826-130">轉譯目標可以建立與本身相容的新轉譯目標，這適用于中繼的非畫面轉譯，同時保留原始上設定的各種呈現目標屬性。</span><span class="sxs-lookup"><span data-stu-id="4e826-130">Render targets can create new render targets that are compatible with themselves, which is useful for intermediate off-screen rendering while retaining the various render-target properties that were set on the original.</span></span>

<span data-ttu-id="4e826-131">您也可以在 Direct2D 轉譯目標上使用 GDI 來轉譯，方法是在 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)的轉譯目標上呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，此方法上具有 [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc)和 [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc)方法，可用來取出 GDI 裝置內容。</span><span class="sxs-lookup"><span data-stu-id="4e826-131">It is also possible to render using GDI on a Direct2D render target by calling [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a render target for [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which has [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) and [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) methods on it that can be used to retrieve a GDI device context.</span></span> <span data-ttu-id="4e826-132">只有當轉譯目標是使用 [**D2D1 轉譯 \_ \_ 目標 \_ 使用 \_ GDI \_ 相容**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) 旗標集建立時，才可以透過 gdi 轉譯。</span><span class="sxs-lookup"><span data-stu-id="4e826-132">Rendering via GDI is possible only if the render target was created with the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag set.</span></span> <span data-ttu-id="4e826-133">這適用于主要以 Direct2D 轉譯，但具有擴充性模型或其他需要能夠以 GDI 轉譯之舊版內容的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4e826-133">This is useful for applications that are primarily rendering with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span> <span data-ttu-id="4e826-134">如需詳細資訊，請參閱 [Direct2D 和 GDI 互通性總覽](direct2d-and-gdi-interoperation-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="4e826-134">For more information, see the [Direct2D and GDI Interoperation Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

### <a name="render-target-resources"></a><span data-ttu-id="4e826-135">呈現目標資源</span><span class="sxs-lookup"><span data-stu-id="4e826-135">Render Target Resources</span></span>

<span data-ttu-id="4e826-136">就像 factory 一樣，轉譯目標可以建立繪圖資源。</span><span class="sxs-lookup"><span data-stu-id="4e826-136">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="4e826-137">轉譯目標所建立的任何資源都是與裝置相關的資源 (就像呈現目標) 一樣。</span><span class="sxs-lookup"><span data-stu-id="4e826-137">Any resources created by a render target are device-dependent resources (just like the render target).</span></span> <span data-ttu-id="4e826-138">轉譯目標可建立下列類型的資源：</span><span class="sxs-lookup"><span data-stu-id="4e826-138">A render target can create the following types of resources:</span></span>

-   <span data-ttu-id="4e826-139">點陣圖</span><span class="sxs-lookup"><span data-stu-id="4e826-139">Bitmaps</span></span>
-   <span data-ttu-id="4e826-140">筆刷</span><span class="sxs-lookup"><span data-stu-id="4e826-140">Brushes</span></span>
-   <span data-ttu-id="4e826-141">圖層</span><span class="sxs-lookup"><span data-stu-id="4e826-141">Layers</span></span>
-   <span data-ttu-id="4e826-142">網狀</span><span class="sxs-lookup"><span data-stu-id="4e826-142">Meshes</span></span>

### <a name="drawing-commands"></a><span data-ttu-id="4e826-143">繪製命令</span><span class="sxs-lookup"><span data-stu-id="4e826-143">Drawing Commands</span></span>

<span data-ttu-id="4e826-144">若要轉譯內容，您可以使用呈現目標繪製方法。</span><span class="sxs-lookup"><span data-stu-id="4e826-144">To render content, you use the render target drawing methods.</span></span> <span data-ttu-id="4e826-145">開始繪製之前，請先呼叫 [**ID2D1RenderTarget：： BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法。</span><span class="sxs-lookup"><span data-stu-id="4e826-145">Before you begin drawing, you call the [**ID2D1RenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method.</span></span> <span data-ttu-id="4e826-146">完成繪製之後，您會呼叫 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。</span><span class="sxs-lookup"><span data-stu-id="4e826-146">After you finished drawing, you call the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="4e826-147">在這些呼叫之間，您會使用 Draw 和 Fill 方法來呈現繪圖資源。</span><span class="sxs-lookup"><span data-stu-id="4e826-147">Between these calls, you use Draw and Fill methods to render drawing resources.</span></span> <span data-ttu-id="4e826-148">大部分的繪圖和填滿方法都採用圖形 (基本或幾何) ，以及用來填滿或大綱圖形的筆刷。</span><span class="sxs-lookup"><span data-stu-id="4e826-148">Most Draw and Fill methods take a shape (either a primitive or a geometry) and a brush for filling or outlining the shape.</span></span>

<span data-ttu-id="4e826-149">轉譯目標提供剪下、套用不透明度遮罩，以及轉換座標空間的方法。</span><span class="sxs-lookup"><span data-stu-id="4e826-149">Render targets provide methods for clipping, applying opacity masks, and transforming the coordinate space.</span></span>

<span data-ttu-id="4e826-150">Direct2D 使用左方座標系統：正 X 軸的值會繼續往右，y 軸的正值則會往下進行。</span><span class="sxs-lookup"><span data-stu-id="4e826-150">Direct2D uses a left-handed coordinate system: positive x-axis values proceed to the right and positive y-axis values proceed downward.</span></span>

### <a name="error-handling"></a><span data-ttu-id="4e826-151">錯誤處理</span><span class="sxs-lookup"><span data-stu-id="4e826-151">Error Handling</span></span>

<span data-ttu-id="4e826-152">轉譯目標繪製命令不會指出要求的作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="4e826-152">Render target drawing commands do not indicate whether the requested operation was successful.</span></span> <span data-ttu-id="4e826-153">若要找出是否有繪圖錯誤，請呼叫轉譯目標 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法或 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法來取得 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="4e826-153">To find out whether there are drawing errors, call the render target [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) method or [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method to obtain an **HRESULT**.</span></span>

## <a name="example-render-content-to-a-window"></a><span data-ttu-id="4e826-154">範例：將內容呈現至視窗</span><span class="sxs-lookup"><span data-stu-id="4e826-154">Example: Render Content to a Window</span></span>

<span data-ttu-id="4e826-155">下列範例會使用 [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) 方法來建立 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)。</span><span class="sxs-lookup"><span data-stu-id="4e826-155">The following example uses the [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) method to create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



<span data-ttu-id="4e826-156">下一個範例會使用 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) ，在視窗中繪製文字。</span><span class="sxs-lookup"><span data-stu-id="4e826-156">The next example uses the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) to draw text to the window.</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



<span data-ttu-id="4e826-157">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="4e826-157">Code has been omitted from this example.</span></span>

 

 