---
title: 互通性概觀
description: 摘要說明您可以搭配 Direct2D 使用的各種技術。
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D，GDI 交互操作
- Direct2D，GDI + 交互操作
- Direct2D，互通性
- Direct2D，DirectWrite 交互操作
- 互通性，Direct2D
- 互通性，Direct3D
- '圖形裝置介面 (GDI) '
- 'GDI (圖形裝置介面) '
- '互通性、圖形裝置介面 (GDI) '
- 互通性，GDI +
- DirectWrite 互通性
- 互通性，DirectWrite
- Windows 影像處理元件 (WIC)
- 'WIC (Windows 影像處理元件) '
- '互通性，Windows 影像處理元件 (WIC) '
- Direct2D，WIC 互通性
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6f56c570a837a541bac9467477d4f6009bda019e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375661"
---
# <a name="interoperability-overview"></a><span data-ttu-id="f8bc5-119">互通性概觀</span><span class="sxs-lookup"><span data-stu-id="f8bc5-119">Interoperability Overview</span></span>

<span data-ttu-id="f8bc5-120">Direct2d 的主要功能之一，是讓 Direct2D 和其他轉譯平臺之間的互通性，讓開發人員可以選擇一種平臺來滿足各種需求，而不會受到任何影響。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-120">One of Direct2D's key features is enabling interoperability between Direct2D and other rendering platforms so that developers can use the specific strengths of each platform without being forced into compromises by choosing one platform for all needs.</span></span> <span data-ttu-id="f8bc5-121">本主題摘要說明 Direct2D 可互通的不同平臺。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-121">This topic summarizes the different platforms with which Direct2D is interoperable.</span></span> <span data-ttu-id="f8bc5-122">包含以下幾節。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-122">It contains the following sections.</span></span>

-   [<span data-ttu-id="f8bc5-123">GDI 互通性</span><span class="sxs-lookup"><span data-stu-id="f8bc5-123">GDI Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="f8bc5-124">GDI + 互通性</span><span class="sxs-lookup"><span data-stu-id="f8bc5-124">GDI+ Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="f8bc5-125">Direct3D 互通性</span><span class="sxs-lookup"><span data-stu-id="f8bc5-125">Direct3D Interoperability</span></span>](#direct3d-interoperability)
-   [<span data-ttu-id="f8bc5-126">DirectWrite 互通性</span><span class="sxs-lookup"><span data-stu-id="f8bc5-126">DirectWrite Interoperability</span></span>](#directwrite-interoperability)
-   [<span data-ttu-id="f8bc5-127">Windows 影像處理元件 (WIC) 互通性</span><span class="sxs-lookup"><span data-stu-id="f8bc5-127">Windows Imaging Component (WIC) Interoperability</span></span>](#windows-imaging-component-wic-interoperability)
-   [<span data-ttu-id="f8bc5-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8bc5-128">Related topics</span></span>](#related-topics)

<span data-ttu-id="f8bc5-129">下圖摘要說明 Direct2D 可互通的不同平臺，並列出一些可提供互通性的方法和介面。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-129">The following diagram summarizes the different platforms with which Direct2D is interoperable and lists some methods and interfaces that provide interoperability.</span></span>

![direct2d 交互操作之平臺的圖表，包括 direct3d 10.1、directwrite、wic、gdi + 和 gdi](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a><span data-ttu-id="f8bc5-131">GDI 互通性</span><span class="sxs-lookup"><span data-stu-id="f8bc5-131">GDI Interoperability</span></span>

<span data-ttu-id="f8bc5-132">Direct2D 可啟用與 GDI 之間的雙向互通性。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-132">Direct2D enables two-way interoperability with GDI.</span></span> <span data-ttu-id="f8bc5-133">您可以使用 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) 將 Direct2D 內容寫入 (DC) 的 GDI [裝置](/windows/desktop/gdi/device-contexts) 內容，也可以使用 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) 來取得呈現目標的 DC 標記法。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-133">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to a GDI [device context](/windows/desktop/gdi/device-contexts) (DC), or you can use [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to obtain a DC representation of a render target.</span></span>

<span data-ttu-id="f8bc5-134">如需詳細資訊和範例，請參閱 [Direct2D 和 GDI 互通性總覽](direct2d-and-gdi-interoperation-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-134">For more information and examples, see the [Direct2D and GDI Interoperability Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="f8bc5-135">GDI + 互通性</span><span class="sxs-lookup"><span data-stu-id="f8bc5-135">GDI+ Interoperability</span></span>

<span data-ttu-id="f8bc5-136">您可以使用 gdi + 搭配 Direct2D，方式與 GDI 相同。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-136">You can use GDI+ with Direct2D in the same manner as GDI.</span></span> <span data-ttu-id="f8bc5-137">您可以使用 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) 將 Direct2D 內容寫入至與 gdi + 內容相同的 DC。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-137">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to the same DC as your GDI+ content.</span></span> <span data-ttu-id="f8bc5-138">這種方法可讓您開始將 Direct2D 內容新增至主要使用 GDI + 轉譯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-138">This approach enables you to start adding Direct2D content to applications that primarily render by using GDI+.</span></span>

<span data-ttu-id="f8bc5-139">您也可以使用 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) 來提供使用 Direct2D 寫入之 GDI DC 的存取權，然後使用 [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) 方法來建立物件。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-139">You can also use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to provide access to a GDI DC that writes by using Direct2D, and then use the [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) method to create a object.</span></span> <span data-ttu-id="f8bc5-140">這種方法適用于主要以 Direct2D 轉譯的應用程式，但具有擴充性模型或其他需要能夠使用 GDI + 轉譯的舊版內容。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-140">This approach is useful for applications that primarily render with Direct2D, but have an extensibility model or other legacy content that requires the ability to render with GDI+.</span></span>

## <a name="direct3d-interoperability"></a><span data-ttu-id="f8bc5-141">Direct3D 互通性</span><span class="sxs-lookup"><span data-stu-id="f8bc5-141">Direct3D Interoperability</span></span>

<span data-ttu-id="f8bc5-142">Direct2D 可以使用由 [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) 方法建立的 DXGI 介面轉譯目標 (，) 寫入 [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface)。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-142">Direct2D can use a DXGI surface render target (created by the [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method) to write to an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface).</span></span> <span data-ttu-id="f8bc5-143">此動作可讓您將2D 背景和介面新增至3-d 場景，並使用 Direct2D 內容做為3D 模型的材質。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-143">This action enables you to add 2-D backgrounds and interfaces to 3-D scenes and use Direct2D content as a texture for a 3-D model.</span></span> <span data-ttu-id="f8bc5-144">Direct2D 也可以採用 [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) ，並使用 [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) 方法來建立點陣圖表示。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-144">Direct2D can also take an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) and use the [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) method to create a bitmap representation.</span></span>

<span data-ttu-id="f8bc5-145">如需詳細資訊和範例，請參閱 [Direct2D 和 Direct3D 互通性總覽](direct2d-and-direct3d-interoperation-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-145">For more information and examples, see the [Direct2D and Direct3D Interoperability Overview](direct2d-and-direct3d-interoperation-overview.md).</span></span>

## <a name="directwrite-interoperability"></a><span data-ttu-id="f8bc5-146">DirectWrite 互通性</span><span class="sxs-lookup"><span data-stu-id="f8bc5-146">DirectWrite Interoperability</span></span>

<span data-ttu-id="f8bc5-147">Direct2D 與 DirectWrite 緊密整合。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-147">Direct2D is tightly integrated with DirectWrite.</span></span> <span data-ttu-id="f8bc5-148">Direct2D 藉由提供 [**DrawText**](id2d1rendertarget-drawtext.md)、 [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)和 [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) 方法，讓您輕鬆地轉譯 DirectWrite 的內容。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-148">Direct2D makes it easy to render DirectWrite content by providing the [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), and [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) methods.</span></span>

## <a name="windows-imaging-component-wic-interoperability"></a><span data-ttu-id="f8bc5-149">Windows 影像處理元件 (WIC) 互通性</span><span class="sxs-lookup"><span data-stu-id="f8bc5-149">Windows Imaging Component (WIC) Interoperability</span></span>

<span data-ttu-id="f8bc5-150">Direct2D 提供 [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)、 [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)和 [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) 方法來操作 WIC 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="f8bc5-150">Direct2D provides the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap), and [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) methods for manipulating WIC bitmaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8bc5-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8bc5-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8bc5-152">Direct2D 和 GDI 互通性總覽</span><span class="sxs-lookup"><span data-stu-id="f8bc5-152">Direct2D and GDI Interoperability Overview</span></span>](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[<span data-ttu-id="f8bc5-153">Direct2D 和 Direct3D 互通性概觀</span><span class="sxs-lookup"><span data-stu-id="f8bc5-153">Direct2D and Direct3D Interoperability Overview</span></span>](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 