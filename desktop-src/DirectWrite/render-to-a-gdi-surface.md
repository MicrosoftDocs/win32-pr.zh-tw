---
title: 轉譯成 GDI 介面
description: 轉譯成 GDI 介面
ms.assetid: a6096ff5-1e6e-4edb-b455-ea5d205072ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff292feb2250a4dd81abeb62d8ee48ebfb4488b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382694"
---
# <a name="render-to-a-gdi-surface"></a><span data-ttu-id="5e5e3-103">轉譯成 GDI 介面</span><span class="sxs-lookup"><span data-stu-id="5e5e3-103">Render to a GDI Surface</span></span>

<span data-ttu-id="5e5e3-104">在某些情況下，您可能會想要能夠在 GDI 介面上顯示 [DirectWrite](direct-write-portal.md) 的文字。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-104">In some cases, you may want to be able to display [DirectWrite](direct-write-portal.md) text on a GDI surface.</span></span> <span data-ttu-id="5e5e3-105">[**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)介面會封裝點陣圖和裝置內容，以將文字轉譯至。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-105">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface encapsulates a bitmap and device context to render text onto.</span></span> <span data-ttu-id="5e5e3-106">您可以使用 [**IDWriteGdiInterop：： CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)方法來建立 **IDWriteBitmapRenderTarget** ，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-106">You create an **IDWriteBitmapRenderTarget** by using the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method, as shown in the following code.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



<span data-ttu-id="5e5e3-107">若要使用 [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)來呈現，您必須執行衍生自 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 介面的自訂文字轉譯器回呼介面。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-107">To render with an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), you must implement a custom text renderer callback interface derived from the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) interface.</span></span> <span data-ttu-id="5e5e3-108">您必須執行方法來繪製圖像執行、底線、刪除線、内嵌物件等等。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-108">You must implement methods for drawing a glyph run, underline, strikethrough, inline objects, and so on.</span></span> <span data-ttu-id="5e5e3-109">如需完整的方法清單，請參閱 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 參考頁面。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-109">For a complete list of the methods, see the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page.</span></span> <span data-ttu-id="5e5e3-110">並非每個方法都必須實作為，它們只會傳回 **E \_ >notimpl**，而繪圖將繼續進行。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-110">Not every method must be implemented, they can just return **E\_NOTIMPL**, and drawing will continue.</span></span>

<span data-ttu-id="5e5e3-111">然後，您可以使用 [**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) 方法，並傳遞您實作為參數的回呼介面，來繪製文字。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-111">You can then draw the text by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method and passing the callback interface that you implemented as a parameter.</span></span> <span data-ttu-id="5e5e3-112">**IDWriteTextLayout：:D 原始** 方法會呼叫您提供的自訂轉譯器回呼的方法。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-112">The **IDWriteTextLayout::Draw** method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="5e5e3-113">[**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)、 [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline)、 [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)和 [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough)方法會執行繪圖函數。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="5e5e3-114">在 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)的執行中，呼叫 [**IDWriteBitmapRenderTarget：:D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) 方法來繪製圖像。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-114">In your implementation of [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), call the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="5e5e3-115">底線、刪除線和内嵌物件的轉譯必須由您的自訂轉譯器完成。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-115">The rendering of the underline, strikethrough and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="5e5e3-116">[**IDWriteBitmapRenderTarget：:D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) 有選擇性的 RECT out 參數，其中包含繪製文字的區域範圍。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-116">[**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) has an optional RECT out parameter that contains the bounds of the area where the text was drawn.</span></span> <span data-ttu-id="5e5e3-117">您可以使用這項資訊，以 GDI 所提供的 [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) 函式來設定裝置內容的周框。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-117">You can use this information to set the bounding rectangle for the device context with the [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) function that is provided by GDI.</span></span> <span data-ttu-id="5e5e3-118">下列程式碼是自訂轉譯器之 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) 方法的範例執行。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-118">The following code is an example implementation of the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of a custom renderer.</span></span>


```C++
STDMETHODIMP GdiTextRenderer::DrawGlyphRun(
    __maybenull void* clientDrawingContext,
    FLOAT baselineOriginX,
    FLOAT baselineOriginY,
    DWRITE_MEASURING_MODE measuringMode,
    __in DWRITE_GLYPH_RUN const* glyphRun,
    __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
    IUnknown* clientDrawingEffect
    )
{
    HRESULT hr = S_OK;

    // Pass on the drawing call to the render target to do the real work.
    RECT dirtyRect = {0};

    hr = pRenderTarget_->DrawGlyphRun(
        baselineOriginX,
        baselineOriginY,
        measuringMode,
        glyphRun,
        pRenderingParams_,
        RGB(0,200,255),
        &dirtyRect
        );
    

    return hr;
}
```



<span data-ttu-id="5e5e3-119">[**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)介面會轉譯成 (DC) 在記憶體中的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-119">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="5e5e3-120">您可以使用 [**IDWriteBitmapRenderTarget：： GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) 方法，取得此 DC 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-120">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span> <span data-ttu-id="5e5e3-121">一旦執行繪圖， **IDWriteBitmapRenderTarget** 物件的記憶體 DC 就必須複製到目的地 GDI 介面。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-121">As soon as the drawing has been performed, the memory DC of the **IDWriteBitmapRenderTarget** object must be copied to the destination GDI surface.</span></span>

<span data-ttu-id="5e5e3-122">您可以使用 [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) 函式來取出周框，然後使用周框與 [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) 函數，將轉譯的 [DirectWrite](direct-write-portal.md) 文字從記憶體 DC 複製到 GDI 介面，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="5e5e3-122">You can retrieve the bounding rectangle by using the [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) function, then use the bounding rectangle with the [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) function to copy the rendered [DirectWrite](direct-write-portal.md) text from the memory DC to the GDI surface as shown in the following code.</span></span>


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



 

 