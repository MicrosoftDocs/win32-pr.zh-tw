---
title: 轉譯 DirectWrite
description: 轉譯 DirectWrite
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa640b8963c427b9eaf1d17fd3e4691115a3965d477c5076deb1f5eb05a569db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070588"
---
# <a name="rendering-directwrite"></a>轉譯 DirectWrite

## <a name="rendering-options"></a>轉譯選項

只有 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 物件所描述之格式設定的文字可以使用 [Direct2D](../direct2d/direct2d-portal.md)來呈現，不過，有幾個選項可以呈現 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件。

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)物件描述的字串可以使用下列方法來呈現。

## <a name="1-render-using-direct2d"></a>1. 使用 Direct2D 轉譯

若要使用 Direct2D 呈現 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件，請使用 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法，如下列程式碼所示。


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



如需深入瞭解如何使用 [Direct2D](../direct2d/direct2d-portal.md)繪製 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)物件，請參閱 [開始使用與 DirectWrite](getting-started-with-directwrite.md)。

## <a name="2-render-using-a-custom-text-renderer"></a>2. 使用自訂文字轉譯器進行轉譯。

您可以使用自訂轉譯器來轉譯，方法是使用 [**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) 方法，它會採用衍生自 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 的回呼介面做為引數，如下列程式碼所示。


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



[**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw)方法會呼叫您提供的自訂轉譯器回呼的方法。 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)、 [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline)、 [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)和 [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough)方法會執行繪圖函數。

[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 會宣告用來繪製圖像執行、底線、刪除線和内嵌物件的方法。 它是由應用程式負責執行這些方法。 建立自訂文字轉譯器可讓應用程式在轉譯文字（例如自訂填滿或外框）時套用其他效果。 範例自訂文字轉譯器包含在[DirectWrite Hello World 範例](/samples/browse/?redirectedfrom=MSDN-samples)中。

## <a name="3-render-cleartype-to-a-gdi-surface"></a>3. 將 ClearType 轉譯為 GDI 表面。

轉譯成 GDI 介面其實是使用自訂文字轉譯器的範例。 不過，部分工作是以 [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) 介面的形式為您完成。

若要建立這個介面，請使用 [**IDWriteGdiInterop：： CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) 方法。

自訂文字轉譯器的 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) 方法會呼叫 [**IDWriteBitmapRenderTarget：:D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) 方法來繪製圖像。 底線、刪除線和内嵌物件的轉譯必須由您的自訂轉譯器完成。

[**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)介面會轉譯成 (DC) 在記憶體中的裝置內容。 您可以使用 [**IDWriteBitmapRenderTarget：： GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) 方法，取得此 DC 的控制碼。


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



執行繪圖之後，必須將 [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) 物件的記憶體 DC 複製到目的地 GDI 介面。

> [!Note]  
> 您也可以選擇將點陣圖傳送至另一種類型的介面，例如 GDI+ 介面。

 


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
> 您的應用程式必須負責將所有內容都呈現在視窗結尾。 這包括文字和圖形。 效能會對此造成負面影響。 此外，轉譯至記憶體 DC 不是 GDI 硬體加速。

 

如需與 GDI 交互操作的更詳細總覽，請參閱 [與 Gdi 互](interoperating-with-gdi.md)操作。

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a>4. 以透明的方式將灰階文字轉譯成 GDI 介面。  (Windows 8 和更新版本) 

從 Windows 8 開始，您可以將灰階文字透明地轉譯成 GDI 介面，以獲得更好的效能。 若要這樣做，您需要：

1.  清除記憶體 DC 以保持透明。
2.  使用灰階消除鋸齒 (DWRITE \_ 文字 \_ 消除鋸齒 \_ 模式 \_ 灰階) ，將文字轉譯成記憶體的 HDC。
3.  使用 [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) 函式，以透明的方式在最終目標 HDC 上轉譯記憶體的 hdc。
4.  視需要重複多次 (比方說，每個圖像執行一次) ，而在其他圖形之間，可以直接轉譯成最終目標 HDC，而不會被 [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) 函式覆寫。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Direct2D 轉譯](rendering-by-using-direct2d.md)
</dt> <dt>

[使用自訂文字轉譯器呈現](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[轉譯成 GDI 介面](render-to-a-gdi-surface.md)
</dt> <dt>

[與 GDI 交互操作](interoperating-with-gdi.md)
</dt> </dl>

 

 