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
# <a name="render-to-a-gdi-surface"></a>轉譯成 GDI 介面

在某些情況下，您可能會想要能夠在 GDI 介面上顯示 [DirectWrite](direct-write-portal.md) 的文字。 [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)介面會封裝點陣圖和裝置內容，以將文字轉譯至。 您可以使用 [**IDWriteGdiInterop：： CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)方法來建立 **IDWriteBitmapRenderTarget** ，如下列程式碼所示。


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



若要使用 [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)來呈現，您必須執行衍生自 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 介面的自訂文字轉譯器回呼介面。 您必須執行方法來繪製圖像執行、底線、刪除線、内嵌物件等等。 如需完整的方法清單，請參閱 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 參考頁面。 並非每個方法都必須實作為，它們只會傳回 **E \_ >notimpl**，而繪圖將繼續進行。

然後，您可以使用 [**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) 方法，並傳遞您實作為參數的回呼介面，來繪製文字。 **IDWriteTextLayout：:D 原始** 方法會呼叫您提供的自訂轉譯器回呼的方法。 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)、 [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline)、 [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)和 [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough)方法會執行繪圖函數。

在 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)的執行中，呼叫 [**IDWriteBitmapRenderTarget：:D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) 方法來繪製圖像。 底線、刪除線和内嵌物件的轉譯必須由您的自訂轉譯器完成。

[**IDWriteBitmapRenderTarget：:D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) 有選擇性的 RECT out 參數，其中包含繪製文字的區域範圍。 您可以使用這項資訊，以 GDI 所提供的 [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) 函式來設定裝置內容的周框。 下列程式碼是自訂轉譯器之 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) 方法的範例執行。


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



[**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)介面會轉譯成 (DC) 在記憶體中的裝置內容。 您可以使用 [**IDWriteBitmapRenderTarget：： GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) 方法，取得此 DC 的控制碼。 一旦執行繪圖， **IDWriteBitmapRenderTarget** 物件的記憶體 DC 就必須複製到目的地 GDI 介面。

您可以使用 [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) 函式來取出周框，然後使用周框與 [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) 函數，將轉譯的 [DirectWrite](direct-write-portal.md) 文字從記憶體 DC 複製到 GDI 介面，如下列程式碼所示。


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



 

 