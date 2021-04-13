---
title: 轉譯 DirectWrite
description: 轉譯 DirectWrite
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7012bc4861a8befc9beb97c945dc0b03b4e761
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375933"
---
# <a name="rendering-directwrite"></a><span data-ttu-id="b0bcd-103">轉譯 DirectWrite</span><span class="sxs-lookup"><span data-stu-id="b0bcd-103">Rendering DirectWrite</span></span>

## <a name="rendering-options"></a><span data-ttu-id="b0bcd-104">轉譯選項</span><span class="sxs-lookup"><span data-stu-id="b0bcd-104">Rendering Options</span></span>

<span data-ttu-id="b0bcd-105">只有 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 物件所描述之格式設定的文字可以使用 [Direct2D](../direct2d/direct2d-portal.md)來呈現，不過，有幾個選項可以呈現 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-105">Text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="b0bcd-106">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)物件描述的字串可以使用下列方法來呈現。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-106">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

## <a name="1-render-using-direct2d"></a><span data-ttu-id="b0bcd-107">1. 使用 Direct2D 轉譯</span><span class="sxs-lookup"><span data-stu-id="b0bcd-107">1. Render using Direct2D</span></span>

<span data-ttu-id="b0bcd-108">若要使用 Direct2D 呈現 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件，請使用 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-108">To render an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using Direct2D, use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method, as shown in the following code.</span></span>


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



<span data-ttu-id="b0bcd-109">如需深入瞭解如何使用 [Direct2D](../direct2d/direct2d-portal.md)繪製 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)物件，請參閱 [使用 DirectWrite 的開始使用](getting-started-with-directwrite.md)。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-109">For a more in depth look at drawing an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using [Direct2D](../direct2d/direct2d-portal.md), see [Getting Started with DirectWrite](getting-started-with-directwrite.md).</span></span>

## <a name="2-render-using-a-custom-text-renderer"></a><span data-ttu-id="b0bcd-110">2. 使用自訂文字轉譯器進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-110">2. Render using a custom text renderer.</span></span>

<span data-ttu-id="b0bcd-111">您可以使用自訂轉譯器來轉譯，方法是使用 [**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) 方法，它會採用衍生自 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 的回呼介面做為引數，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-111">You render with a custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="b0bcd-112">[**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw)方法會呼叫您提供的自訂轉譯器回呼的方法。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-112">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="b0bcd-113">[**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)、 [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline)、 [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)和 [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough)方法會執行繪圖函數。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="b0bcd-114">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 會宣告用來繪製圖像執行、底線、刪除線和内嵌物件的方法。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-114">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) declares methods for drawing a glyph run, underline, strikethrough, and inline objects.</span></span> <span data-ttu-id="b0bcd-115">它是由應用程式負責執行這些方法。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-115">It is up to the application to implement these methods.</span></span> <span data-ttu-id="b0bcd-116">建立自訂文字轉譯器可讓應用程式在轉譯文字（例如自訂填滿或外框）時套用其他效果。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-116">Creating a custom text renderer allows the application to apply additional effects when rendering text, such as a custom fill or outline.</span></span> <span data-ttu-id="b0bcd-117">[DirectWrite Hello World 範例](/samples/browse/?redirectedfrom=MSDN-samples)中包含了範例自訂文字轉譯器。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-117">A sample custom text renderer is included in the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="3-render-cleartype-to-a-gdi-surface"></a><span data-ttu-id="b0bcd-118">3. 將 ClearType 轉譯為 GDI 表面。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-118">3. Render ClearType to a GDI surface.</span></span>

<span data-ttu-id="b0bcd-119">轉譯成 GDI 介面其實是使用自訂文字轉譯器的範例。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-119">Rendering to a GDI surface is actually an example of using a custom text renderer.</span></span> <span data-ttu-id="b0bcd-120">不過，部分工作是以 [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) 介面的形式為您完成。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-120">However, some of the work is done for you in the form of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface.</span></span>

<span data-ttu-id="b0bcd-121">若要建立這個介面，請使用 [**IDWriteGdiInterop：： CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) 方法。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-121">To create this interface, use the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method.</span></span>

<span data-ttu-id="b0bcd-122">自訂文字轉譯器的 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) 方法會呼叫 [**IDWriteBitmapRenderTarget：:D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) 方法來繪製圖像。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-122">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of your custom text renderer calls the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="b0bcd-123">底線、刪除線和内嵌物件的轉譯必須由您的自訂轉譯器完成。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-123">The rendering of the underline, strikethrough, and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="b0bcd-124">[**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)介面會轉譯成 (DC) 在記憶體中的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-124">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="b0bcd-125">您可以使用 [**IDWriteBitmapRenderTarget：： GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) 方法，取得此 DC 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-125">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span>


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



<span data-ttu-id="b0bcd-126">執行繪圖之後，必須將 [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) 物件的記憶體 DC 複製到目的地 GDI 介面。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-126">Once the drawing has been performed, the memory DC of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object must be copied to the destination GDI surface.</span></span>

> [!Note]  
> <span data-ttu-id="b0bcd-127">您也可以選擇將點陣圖傳送至另一種類型的介面，例如 GDI + 介面。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-127">You also have the option of transferring the bitmap to another type of surface, such as a GDI+ surface.</span></span>

 


```C++
// Transfer from DWrite's rendering target to the window.
BitBlt(
    hdc,
    0, 0,
    size.cx, size.cy,
    memoryHdc,
    0, 0, 
    SRCCOPY | NOMIRRORBITMAP
    );
```



> [!Note]  
> <span data-ttu-id="b0bcd-128">您的應用程式必須負責將所有內容都呈現在視窗結尾。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-128">Your app has the responsibility to render everything to the window in the end.</span></span> <span data-ttu-id="b0bcd-129">這包括文字和圖形。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-129">This includes text and graphics.</span></span> <span data-ttu-id="b0bcd-130">效能會對此造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-130">There is a performance penalty to this.</span></span> <span data-ttu-id="b0bcd-131">此外，轉譯至記憶體 DC 不是 GDI 硬體加速。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-131">Additionally, rendering to a memory DC is not GDI hardware accelerated.</span></span>

 

<span data-ttu-id="b0bcd-132">如需與 GDI 交互操作的更詳細總覽，請參閱 [與 Gdi 互](interoperating-with-gdi.md)操作。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-132">For a more detailed overview of interoperating with GDI see [Interoperating with GDI](interoperating-with-gdi.md).</span></span>

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a><span data-ttu-id="b0bcd-133">4. 以透明的方式將灰階文字轉譯成 GDI 介面。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-133">4. Render Grayscale Text Transparently to a GDI Surface.</span></span> <span data-ttu-id="b0bcd-134"> (Windows 8 和更新版本) </span><span class="sxs-lookup"><span data-stu-id="b0bcd-134">(Windows 8 and later)</span></span>

<span data-ttu-id="b0bcd-135">從 Windows 8 開始，您可以將灰階文字透明地轉譯成 GDI 介面，以獲得更好的效能。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-135">Starting in Windows 8, you can render grayscale text transparently to a GDI surface for better performance.</span></span> <span data-ttu-id="b0bcd-136">若要這樣做，您需要：</span><span class="sxs-lookup"><span data-stu-id="b0bcd-136">To do this you need to:</span></span>

1.  <span data-ttu-id="b0bcd-137">清除記憶體 DC 以保持透明。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-137">Clear the memory DC to transparent.</span></span>
2.  <span data-ttu-id="b0bcd-138">使用灰階消除鋸齒 (DWRITE \_ 文字 \_ 消除鋸齒 \_ 模式 \_ 灰階) ，將文字轉譯成記憶體的 HDC。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-138">Render text to the memory HDC using grayscale antialiasing (DWRITE\_TEXT\_ANTIALIAS\_MODE\_GRAYSCALE).</span></span>
3.  <span data-ttu-id="b0bcd-139">使用 [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) 函式，以透明的方式在最終目標 HDC 上轉譯記憶體的 hdc。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-139">Use the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function to render the memory HDC transparently on top of the final target HDC.</span></span>
4.  <span data-ttu-id="b0bcd-140">視需要重複多次 (比方說，每個圖像執行一次) ，而在其他圖形之間，可以直接轉譯成最終目標 HDC，而不會被 [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) 函式覆寫。</span><span class="sxs-lookup"><span data-stu-id="b0bcd-140">Repeat as many times as necessary (say, once per glyph run) and in between other graphics may be rendered directly to the final target HDC without being overwritten by the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>


```C++
pRT_->SetTextAntialiasMode(DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE);

pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

BLENDFUNCTION blendFunction = { 0 };  
blendFunction.BlendOp = AC_SRC_OVER;  
blendFunction.SourceConstantAlpha = 255;  
blendFunction.AlphaFormat = AC_SRC_ALPHA;

AlphaBlend(  
        hdc,  
        0, 0,  
        width, height,  
        pRT_->GetMemoryDC(),  
        0, 0,  
        width, height,  
        blendFunction  
        );

```



## <a name="related-topics"></a><span data-ttu-id="b0bcd-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="b0bcd-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0bcd-142">使用 Direct2D 轉譯</span><span class="sxs-lookup"><span data-stu-id="b0bcd-142">Render Using Direct2D</span></span>](rendering-by-using-direct2d.md)
</dt> <dt>

[<span data-ttu-id="b0bcd-143">使用自訂文字轉譯器呈現</span><span class="sxs-lookup"><span data-stu-id="b0bcd-143">Render Using a Custom Text Renderer</span></span>](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[<span data-ttu-id="b0bcd-144">轉譯成 GDI 介面</span><span class="sxs-lookup"><span data-stu-id="b0bcd-144">Render to a GDI surface</span></span>](render-to-a-gdi-surface.md)
</dt> <dt>

[<span data-ttu-id="b0bcd-145">與 GDI 交互操作</span><span class="sxs-lookup"><span data-stu-id="b0bcd-145">Interoperating with GDI</span></span>](interoperating-with-gdi.md)
</dt> </dl>

 

 