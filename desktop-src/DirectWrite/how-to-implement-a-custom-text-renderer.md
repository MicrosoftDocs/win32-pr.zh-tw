---
title: 使用自訂文字轉譯器呈現
description: DirectWrite \ 160; 文字版面配置可以由衍生自 IDWriteTextRenderer 的自訂文字轉譯器繪製。
ms.assetid: a5b09733-24b2-408e-a1f9-cf7ad20c5c63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cda56fc5cc38a62e48a2f62066edfec2327e9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375884"
---
# <a name="render-using-a-custom-text-renderer"></a><span data-ttu-id="b3295-103">使用自訂文字轉譯器呈現</span><span class="sxs-lookup"><span data-stu-id="b3295-103">Render Using a Custom Text Renderer</span></span>

<span data-ttu-id="b3295-104">[DirectWrite](direct-write-portal.md)的  [**文字版面**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)配置可以由衍生自 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)的自訂文字轉譯器繪製。</span><span class="sxs-lookup"><span data-stu-id="b3295-104">A [DirectWrite](direct-write-portal.md) [**text layout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) can be drawn by a custom text renderer derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer).</span></span> <span data-ttu-id="b3295-105">您必須要有自訂轉譯器，才能利用 DirectWrite 的一些先進功能，例如轉譯成點陣圖或 GDI 介面、内嵌物件和用戶端繪製效果。</span><span class="sxs-lookup"><span data-stu-id="b3295-105">A custom renderer is required to take advantage of some advanced features of DirectWrite, such as rendering to a bitmap or GDI surface, inline objects, and client drawing effects.</span></span> <span data-ttu-id="b3295-106">本教學課程說明 **IDWriteTextRenderer** 的方法，並提供使用 [Direct2D](../direct2d/direct2d-portal.md) 以點陣圖填滿呈現文字的範例執行。</span><span class="sxs-lookup"><span data-stu-id="b3295-106">This tutorial describes the methods of **IDWriteTextRenderer**, and provides an example implementation that uses [Direct2D](../direct2d/direct2d-portal.md) to render text with a bitmap fill.</span></span>

<span data-ttu-id="b3295-107">本教學課程包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="b3295-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="b3295-108">函數</span><span class="sxs-lookup"><span data-stu-id="b3295-108">The Constructor</span></span>](#the-constructor)
-   [<span data-ttu-id="b3295-109">DrawGlyphRun () </span><span class="sxs-lookup"><span data-stu-id="b3295-109">DrawGlyphRun()</span></span>](#drawglyphrun)
-   [<span data-ttu-id="b3295-110">DrawUnderline () 和 DrawStrikethrough () </span><span class="sxs-lookup"><span data-stu-id="b3295-110">DrawUnderline() and DrawStrikethrough()</span></span>](#drawunderline-and-drawstrikethrough)
-   [<span data-ttu-id="b3295-111">圖元貼齊、每個 DIP 的圖元和轉換</span><span class="sxs-lookup"><span data-stu-id="b3295-111">Pixel Snapping, Pixels per DIP, and Transform</span></span>](#pixel-snapping-pixels-per-dip-and-transform)
    -   [<span data-ttu-id="b3295-112">IsPixelSnappingDisabled () </span><span class="sxs-lookup"><span data-stu-id="b3295-112">IsPixelSnappingDisabled()</span></span>](#ispixelsnappingdisabled)
    -   [<span data-ttu-id="b3295-113">GetCurrentTransform () </span><span class="sxs-lookup"><span data-stu-id="b3295-113">GetCurrentTransform()</span></span>](#getcurrenttransform)
    -   [<span data-ttu-id="b3295-114">GetPixelsPerDip () </span><span class="sxs-lookup"><span data-stu-id="b3295-114">GetPixelsPerDip()</span></span>](#getpixelsperdip)
-   [<span data-ttu-id="b3295-115">DrawInlineObject () </span><span class="sxs-lookup"><span data-stu-id="b3295-115">DrawInlineObject()</span></span>](#drawinlineobject)
-   [<span data-ttu-id="b3295-116">函式</span><span class="sxs-lookup"><span data-stu-id="b3295-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="b3295-117">使用自訂文字轉譯器</span><span class="sxs-lookup"><span data-stu-id="b3295-117">Using the Custom Text Renderer</span></span>](#using-the-custom-text-renderer)

<span data-ttu-id="b3295-118">除了 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 參考頁面上所列的方法之外，您的自訂文字轉譯器還必須執行繼承自 IUnknown 的方法。</span><span class="sxs-lookup"><span data-stu-id="b3295-118">Your custom text renderer must implement the methods inherited from IUnknown in addition to the methods listed on the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page and below.</span></span>

<span data-ttu-id="b3295-119">如需自訂文字轉譯器的完整原始碼，請參閱 [DirectWrite Hello World 範例](/samples/browse/?redirectedfrom=MSDN-samples)的 CustomTextRenderer .Cpp 和 CustomTextRenderer .h 檔案。</span><span class="sxs-lookup"><span data-stu-id="b3295-119">For the full source code for the custom text renderer, see the CustomTextRenderer.cpp and CustomTextRenderer.h files of the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="the-constructor"></a><span data-ttu-id="b3295-120">函數</span><span class="sxs-lookup"><span data-stu-id="b3295-120">The Constructor</span></span>

<span data-ttu-id="b3295-121">您的自訂文字轉譯器將需要一個函式。</span><span class="sxs-lookup"><span data-stu-id="b3295-121">Your custom text renderer will need a constructor.</span></span> <span data-ttu-id="b3295-122">這個範例會使用純色和點陣圖 [Direct2D](../direct2d/direct2d-portal.md) 筆刷來呈現文字。</span><span class="sxs-lookup"><span data-stu-id="b3295-122">This example uses both solid and bitmap [Direct2D](../direct2d/direct2d-portal.md) brushes to render the text.</span></span>

<span data-ttu-id="b3295-123">因此，此函式會採用下表中找到的參數和描述。</span><span class="sxs-lookup"><span data-stu-id="b3295-123">Because of this, the constructor takes the parameters found in the table below with descriptions.</span></span>



| <span data-ttu-id="b3295-124">參數</span><span class="sxs-lookup"><span data-stu-id="b3295-124">Parameter</span></span>       | <span data-ttu-id="b3295-125">Description</span><span class="sxs-lookup"><span data-stu-id="b3295-125">Description</span></span>                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3295-126">*pD2DFactory*</span><span class="sxs-lookup"><span data-stu-id="b3295-126">*pD2DFactory*</span></span>   | <span data-ttu-id="b3295-127">[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)物件的指標，該物件將用來建立所需的任何 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="b3295-127">A pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create any Direct2D resources that are needed.</span></span>                                                                                                        |
| <span data-ttu-id="b3295-128">*Prt*</span><span class="sxs-lookup"><span data-stu-id="b3295-128">*pRT*</span></span>           | <span data-ttu-id="b3295-129">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)物件的指標，該物件會轉譯為文字。</span><span class="sxs-lookup"><span data-stu-id="b3295-129">A pointer to the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object that the text will be rendered to.</span></span> |
| <span data-ttu-id="b3295-130">*pOutlineBrush*</span><span class="sxs-lookup"><span data-stu-id="b3295-130">*pOutlineBrush*</span></span> | <span data-ttu-id="b3295-131">將用來繪製文字外框的 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 指標</span><span class="sxs-lookup"><span data-stu-id="b3295-131">A pointer to the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) that will be use to draw outline of the text</span></span>                                                                                                                     |
| <span data-ttu-id="b3295-132">*pFillBrush*</span><span class="sxs-lookup"><span data-stu-id="b3295-132">*pFillBrush*</span></span>    | <span data-ttu-id="b3295-133">將用來填滿文字之 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 的指標。</span><span class="sxs-lookup"><span data-stu-id="b3295-133">A pointer to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that will be used to fill the text.</span></span>                                                                                                                                      |



 

<span data-ttu-id="b3295-134">這些會由函式儲存，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="b3295-134">These will be stored by the constructor as shown in the following code.</span></span>


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT, 
    ID2D1SolidColorBrush* pOutlineBrush, 
    ID2D1BitmapBrush* pFillBrush
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT), 
pOutlineBrush_(pOutlineBrush), 
pFillBrush_(pFillBrush)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
    pOutlineBrush_->AddRef();
    pFillBrush_->AddRef();
}
```



## <a name="drawglyphrun"></a><span data-ttu-id="b3295-135">DrawGlyphRun () </span><span class="sxs-lookup"><span data-stu-id="b3295-135">DrawGlyphRun()</span></span>

<span data-ttu-id="b3295-136">[**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)方法是文字轉譯器的主要回呼方法。</span><span class="sxs-lookup"><span data-stu-id="b3295-136">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method is the main callback method of the text renderer.</span></span> <span data-ttu-id="b3295-137">除了基準來源和測量模式以外的資訊之外，還會傳遞要轉譯的字元執行。</span><span class="sxs-lookup"><span data-stu-id="b3295-137">It is passed a run of glyphs to be rendered in addition to information such as the baseline origin and measuring mode.</span></span> <span data-ttu-id="b3295-138">它也會傳遞要套用至圖像執行的用戶端繪圖效果物件。</span><span class="sxs-lookup"><span data-stu-id="b3295-138">It also passes a client drawing effect object to be applied to the glyph run.</span></span> <span data-ttu-id="b3295-139">如需詳細資訊，請參閱 [如何將用戶端繪製效果加入至文字版面](how-to-add-custom-drawing-efffects-to-a-text-layout.md) 配置主題。</span><span class="sxs-lookup"><span data-stu-id="b3295-139">For more information, see the [How to Add Client Drawing Effects to a Text Layout](how-to-add-custom-drawing-efffects-to-a-text-layout.md) topic.</span></span>

<span data-ttu-id="b3295-140">此文字轉譯器實作為圖像執行的方式，會將其轉換成 [Direct2D](rendering-by-using-direct2d.md) 幾何，然後繪製和填滿幾何。</span><span class="sxs-lookup"><span data-stu-id="b3295-140">This text renderer implementation renders glyph runs by converting them to [Direct2D](rendering-by-using-direct2d.md) geometries and then drawing and filling the geometries.</span></span> <span data-ttu-id="b3295-141">這包括下列步驟。</span><span class="sxs-lookup"><span data-stu-id="b3295-141">This consists of the following steps.</span></span>

1.  <span data-ttu-id="b3295-142">建立 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)物件，然後使用 [**ID2D1PathGeometry：： Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open)方法取出 [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)物件。</span><span class="sxs-lookup"><span data-stu-id="b3295-142">Create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) object, and then retrieve the [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) object by using the [**ID2D1PathGeometry::Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method.</span></span>

    ```C++
    // Create the path geometry.
    ID2D1PathGeometry* pPathGeometry = NULL;
    hr = pD2DFactory_->CreatePathGeometry(
            &pPathGeometry
            );

    // Write to the path geometry using the geometry sink.
    ID2D1GeometrySink* pSink = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Open(
            &pSink
            );
    }
    ```

    

2.  <span data-ttu-id="b3295-143">傳遞至 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)的 [**DWRITE 圖像 \_ \_ 執行**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)包含名為 *fontFace* 的 [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)物件，代表整個圖像執行的字型。</span><span class="sxs-lookup"><span data-stu-id="b3295-143">The [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) that is passed to [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) contains a [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object, named *fontFace*, that represents the font face for the whole glyph run.</span></span> <span data-ttu-id="b3295-144">使用 [**IDWriteFontFace：： GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) 方法，將圖像的輪廓放入幾何接收器，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="b3295-144">Put the outline of the glyph run into the geometry sink by using the [**IDWriteFontFace:: GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) method, as shown in the following code.</span></span>

    ```C++
    // Get the glyph run outline geometries back from DirectWrite and place them within the
    // geometry sink.
    if (SUCCEEDED(hr))
    {
        hr = glyphRun->fontFace->GetGlyphRunOutline(
            glyphRun->fontEmSize,
            glyphRun->glyphIndices,
            glyphRun->glyphAdvances,
            glyphRun->glyphOffsets,
            glyphRun->glyphCount,
            glyphRun->isSideways,
            glyphRun->bidiLevel%2,
            pSink
            );
    }
    ```

    

3.  <span data-ttu-id="b3295-145">填妥幾何接收器之後，請將其關閉。</span><span class="sxs-lookup"><span data-stu-id="b3295-145">After filling the geometry sink, close it.</span></span>

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  <span data-ttu-id="b3295-146">必須轉譯圖像執行的來源，以便從正確的基準原點轉譯，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="b3295-146">The origin of the glyph run must be translated so that it is rendered from the correct baseline origin, as shown in the following code.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    <span data-ttu-id="b3295-147">*BaselineOriginX* 和 *baselineOriginY* 會以參數形式傳遞至 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)回呼方法。</span><span class="sxs-lookup"><span data-stu-id="b3295-147">The *baselineOriginX* and *baselineOriginY* are passed as parameters to the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback method.</span></span>

5.  <span data-ttu-id="b3295-148">使用 [**ID2D1Factory：： CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) 方法，然後傳遞路徑幾何和平移矩陣，以建立已轉換的幾何。</span><span class="sxs-lookup"><span data-stu-id="b3295-148">Create the transformed geometry by using the [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method and passing the path geometry and the translation matrix.</span></span>

    ```C++
    // Create the transformed geometry
    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pPathGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

6.  <span data-ttu-id="b3295-149">最後，繪製已轉換幾何的外框，並使用 [**ID2D1RenderTarget：:D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 和 [**ID2D1RenderTarget：： FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法，並將 [Direct2D](../direct2d/direct2d-portal.md) 筆刷儲存為成員變數來填滿。</span><span class="sxs-lookup"><span data-stu-id="b3295-149">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

7.  <span data-ttu-id="b3295-150">現在您已完成繪圖，請不要忘了清除在此方法中建立的物件。</span><span class="sxs-lookup"><span data-stu-id="b3295-150">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a><span data-ttu-id="b3295-151">DrawUnderline () 和 DrawStrikethrough () </span><span class="sxs-lookup"><span data-stu-id="b3295-151">DrawUnderline() and DrawStrikethrough()</span></span>

<span data-ttu-id="b3295-152">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 也具有可繪製底線和刪除線的回呼。</span><span class="sxs-lookup"><span data-stu-id="b3295-152">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) also has callbacks for drawing the underline and strikethrough.</span></span> <span data-ttu-id="b3295-153">此範例會繪製底線或刪除線的簡單矩形，但可以繪製其他圖形。</span><span class="sxs-lookup"><span data-stu-id="b3295-153">This example draws a simple rectangle for an underline or strikethrough, but other shapes can be drawn.</span></span>

<span data-ttu-id="b3295-154">使用 [Direct2D](../direct2d/direct2d-portal.md) 繪製底線是由下列步驟所組成。</span><span class="sxs-lookup"><span data-stu-id="b3295-154">Drawing an underline by using [Direct2D](../direct2d/direct2d-portal.md) consists of the following steps.</span></span>

1.  <span data-ttu-id="b3295-155">首先，建立底線的大小和形狀的 [**D2D1 \_ RECT \_ F**](../direct2d/d2d1-rect-f.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="b3295-155">First, create a [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure of the size and shape of the underline.</span></span> <span data-ttu-id="b3295-156">傳遞至 [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline)回呼方法的 [**DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline)底線結構會提供底線的位移、寬度和粗細。</span><span class="sxs-lookup"><span data-stu-id="b3295-156">The [**DWRITE\_UNDERLINE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) structure that is passed to the [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) callback method provides the offset, width, and thickness of the underline.</span></span>

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  <span data-ttu-id="b3295-157">接下來，使用 [**ID2D1Factory：： CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))方法和初始化的 [**D2D1 \_ RECT \_ F**](../direct2d/d2d1-rect-f.md)結構來建立 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)物件。</span><span class="sxs-lookup"><span data-stu-id="b3295-157">Next, create an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) object by using the [**ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)) method and the initialized [**D2D1\_RECT\_F**](../direct2d/d2d1-rect-f.md) structure.</span></span>

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  <span data-ttu-id="b3295-158">如同圖像執行，必須使用 [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) 方法，根據基準原點值轉譯底線幾何的來源。</span><span class="sxs-lookup"><span data-stu-id="b3295-158">As with the glyph run, the origin of the underline geometry must be translated, based on the baseline origin values, by using the [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method.</span></span>

    ```C++
    // Initialize a matrix to translate the origin of the underline
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );

    ID2D1TransformedGeometry* pTransformedGeometry = NULL;
    if (SUCCEEDED(hr))
    {
        hr = pD2DFactory_->CreateTransformedGeometry(
            pRectangleGeometry,
            &matrix,
            &pTransformedGeometry
            );
    }
    ```

    

4.  <span data-ttu-id="b3295-159">最後，繪製已轉換幾何的外框，並使用 [**ID2D1RenderTarget：:D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 和 [**ID2D1RenderTarget：： FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法，並將 [Direct2D](../direct2d/direct2d-portal.md) 筆刷儲存為成員變數來填滿。</span><span class="sxs-lookup"><span data-stu-id="b3295-159">Finally, draw the outline of the transformed geometry, and fill it by using the [**ID2D1RenderTarget::DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) and [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods and the [Direct2D](../direct2d/direct2d-portal.md) brushes stored as member variables.</span></span>

    ```C++
        // Draw the outline of the glyph run
        pRT_->DrawGeometry(
            pTransformedGeometry,
            pOutlineBrush_
            );

        // Fill in the glyph run
        pRT_->FillGeometry(
            pTransformedGeometry,
            pFillBrush_
            );
    ```

    

5.  <span data-ttu-id="b3295-160">現在您已完成繪圖，請不要忘了清除在此方法中建立的物件。</span><span class="sxs-lookup"><span data-stu-id="b3295-160">Now that you are finished drawing, do not forget to clean up the objects that were created in this method.</span></span>

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

<span data-ttu-id="b3295-161">繪製刪除線的程式相同。</span><span class="sxs-lookup"><span data-stu-id="b3295-161">The process for drawing a strikethrough is the same.</span></span> <span data-ttu-id="b3295-162">不過，刪除線會有不同的位移，且可能會有不同的寬度和粗細。</span><span class="sxs-lookup"><span data-stu-id="b3295-162">However, the strikethrough will have a different offset, and likely a different width and thickness.</span></span>

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a><span data-ttu-id="b3295-163">圖元貼齊、每個 DIP 的圖元和轉換</span><span class="sxs-lookup"><span data-stu-id="b3295-163">Pixel Snapping, Pixels per DIP, and Transform</span></span>

### <a name="ispixelsnappingdisabled"></a><span data-ttu-id="b3295-164">IsPixelSnappingDisabled () </span><span class="sxs-lookup"><span data-stu-id="b3295-164">IsPixelSnappingDisabled()</span></span>

<span data-ttu-id="b3295-165">呼叫這個方法來判斷是否停用圖元貼齊。</span><span class="sxs-lookup"><span data-stu-id="b3295-165">This method is called to determine whether pixel snapping is disabled.</span></span> <span data-ttu-id="b3295-166">建議的預設值為 **FALSE**，這是此範例的輸出。</span><span class="sxs-lookup"><span data-stu-id="b3295-166">The recommended default is **FALSE**, and that is the output of this example.</span></span>


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a><span data-ttu-id="b3295-167">GetCurrentTransform () </span><span class="sxs-lookup"><span data-stu-id="b3295-167">GetCurrentTransform()</span></span>

<span data-ttu-id="b3295-168">此範例會轉譯成 Direct2D 轉譯目標，因此請使用 [**ID2D1RenderTarget：： GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform)從轉譯目標轉送轉換。</span><span class="sxs-lookup"><span data-stu-id="b3295-168">This example renders to a Direct2D render target, so forward the transform from the render target using [**ID2D1RenderTarget::GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform).</span></span>


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a><span data-ttu-id="b3295-169">GetPixelsPerDip () </span><span class="sxs-lookup"><span data-stu-id="b3295-169">GetPixelsPerDip()</span></span>

<span data-ttu-id="b3295-170">呼叫這個方法來取得每個裝置的圖元數， (DIP) 的圖元數。</span><span class="sxs-lookup"><span data-stu-id="b3295-170">This method is called to get the number of pixels per Device Independent Pixel (DIP).</span></span>


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a><span data-ttu-id="b3295-171">DrawInlineObject () </span><span class="sxs-lookup"><span data-stu-id="b3295-171">DrawInlineObject()</span></span>

<span data-ttu-id="b3295-172">自訂文字轉譯器也有繪製内嵌物件的回呼。</span><span class="sxs-lookup"><span data-stu-id="b3295-172">A custom text renderer also has a callback for drawing inline objects.</span></span> <span data-ttu-id="b3295-173">在此範例中， [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) 會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="b3295-173">In this example, [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) returns E\_NOTIMPL.</span></span> <span data-ttu-id="b3295-174">說明如何繪製内嵌物件已超出本教學課程的範圍。</span><span class="sxs-lookup"><span data-stu-id="b3295-174">An explanation of how to draw inline objects is beyond the scope of this tutorial.</span></span> <span data-ttu-id="b3295-175">如需詳細資訊，請參閱 [如何將内嵌物件加入至文字版面](how-to-add-inline-objects-to-a-text-layout.md) 配置主題。</span><span class="sxs-lookup"><span data-stu-id="b3295-175">For more information, see the [How to Add Inline Objects to a Text Layout](how-to-add-inline-objects-to-a-text-layout.md) topic.</span></span>

## <a name="the-destructor"></a><span data-ttu-id="b3295-176">函式</span><span class="sxs-lookup"><span data-stu-id="b3295-176">The Destructor</span></span>

<span data-ttu-id="b3295-177">請務必釋放自訂文字轉譯器類別所使用的任何指標。</span><span class="sxs-lookup"><span data-stu-id="b3295-177">It is important to release any pointers that were used by the custom text renderer class.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a><span data-ttu-id="b3295-178">使用自訂文字轉譯器</span><span class="sxs-lookup"><span data-stu-id="b3295-178">Using the Custom Text Renderer</span></span>

<span data-ttu-id="b3295-179">您可以使用 [**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) 方法，以自訂轉譯器轉譯，此方法會採用衍生自 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 的回呼介面做為引數，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="b3295-179">You render with the custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="b3295-180">[**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw)方法會呼叫您提供的自訂轉譯器回呼的方法。</span><span class="sxs-lookup"><span data-stu-id="b3295-180">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="b3295-181">上面所述的 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)、 [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline)、 [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)和 [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) 方法會執行繪圖函數。</span><span class="sxs-lookup"><span data-stu-id="b3295-181">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods described above perform the drawing functions.</span></span>

 

 