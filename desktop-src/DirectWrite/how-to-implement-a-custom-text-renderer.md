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
# <a name="render-using-a-custom-text-renderer"></a>使用自訂文字轉譯器呈現

[DirectWrite](direct-write-portal.md)的  [**文字版面**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)配置可以由衍生自 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)的自訂文字轉譯器繪製。 您必須要有自訂轉譯器，才能利用 DirectWrite 的一些先進功能，例如轉譯成點陣圖或 GDI 介面、内嵌物件和用戶端繪製效果。 本教學課程說明 **IDWriteTextRenderer** 的方法，並提供使用 [Direct2D](../direct2d/direct2d-portal.md) 以點陣圖填滿呈現文字的範例執行。

本教學課程包含下列部分：

-   [函數](#the-constructor)
-   [DrawGlyphRun () ](#drawglyphrun)
-   [DrawUnderline () 和 DrawStrikethrough () ](#drawunderline-and-drawstrikethrough)
-   [圖元貼齊、每個 DIP 的圖元和轉換](#pixel-snapping-pixels-per-dip-and-transform)
    -   [IsPixelSnappingDisabled () ](#ispixelsnappingdisabled)
    -   [GetCurrentTransform () ](#getcurrenttransform)
    -   [GetPixelsPerDip () ](#getpixelsperdip)
-   [DrawInlineObject () ](#drawinlineobject)
-   [函式](#the-destructor)
-   [使用自訂文字轉譯器](#using-the-custom-text-renderer)

除了 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 參考頁面上所列的方法之外，您的自訂文字轉譯器還必須執行繼承自 IUnknown 的方法。

如需自訂文字轉譯器的完整原始碼，請參閱 [DirectWrite Hello World 範例](/samples/browse/?redirectedfrom=MSDN-samples)的 CustomTextRenderer .Cpp 和 CustomTextRenderer .h 檔案。

## <a name="the-constructor"></a>函數

您的自訂文字轉譯器將需要一個函式。 這個範例會使用純色和點陣圖 [Direct2D](../direct2d/direct2d-portal.md) 筆刷來呈現文字。

因此，此函式會採用下表中找到的參數和描述。



| 參數       | Description                                                                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *pD2DFactory*   | [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)物件的指標，該物件將用來建立所需的任何 Direct2D 資源。                                                                                                        |
| *Prt*           | [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)物件的指標，該物件會轉譯為文字。 |
| *pOutlineBrush* | 將用來繪製文字外框的 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 指標                                                                                                                     |
| *pFillBrush*    | 將用來填滿文字之 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 的指標。                                                                                                                                      |



 

這些會由函式儲存，如下列程式碼所示。


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



## <a name="drawglyphrun"></a>DrawGlyphRun () 

[**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)方法是文字轉譯器的主要回呼方法。 除了基準來源和測量模式以外的資訊之外，還會傳遞要轉譯的字元執行。 它也會傳遞要套用至圖像執行的用戶端繪圖效果物件。 如需詳細資訊，請參閱 [如何將用戶端繪製效果加入至文字版面](how-to-add-custom-drawing-efffects-to-a-text-layout.md) 配置主題。

此文字轉譯器實作為圖像執行的方式，會將其轉換成 [Direct2D](rendering-by-using-direct2d.md) 幾何，然後繪製和填滿幾何。 這包括下列步驟。

1.  建立 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)物件，然後使用 [**ID2D1PathGeometry：： Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open)方法取出 [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)物件。

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

    

2.  傳遞至 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)的 [**DWRITE 圖像 \_ \_ 執行**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)包含名為 *fontFace* 的 [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)物件，代表整個圖像執行的字型。 使用 [**IDWriteFontFace：： GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) 方法，將圖像的輪廓放入幾何接收器，如下列程式碼所示。

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

    

3.  填妥幾何接收器之後，請將其關閉。

    ```C++
    // Close the geometry sink
    if (SUCCEEDED(hr))
    {
        hr = pSink->Close();
    }
    ```

    

4.  必須轉譯圖像執行的來源，以便從正確的基準原點轉譯，如下列程式碼所示。

    ```C++
    // Initialize a matrix to translate the origin of the glyph run.
    D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
        1.0f, 0.0f,
        0.0f, 1.0f,
        baselineOriginX, baselineOriginY
        );
    ```

    

    *BaselineOriginX* 和 *baselineOriginY* 會以參數形式傳遞至 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)回呼方法。

5.  使用 [**ID2D1Factory：： CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) 方法，然後傳遞路徑幾何和平移矩陣，以建立已轉換的幾何。

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

    

6.  最後，繪製已轉換幾何的外框，並使用 [**ID2D1RenderTarget：:D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 和 [**ID2D1RenderTarget：： FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法，並將 [Direct2D](../direct2d/direct2d-portal.md) 筆刷儲存為成員變數來填滿。

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

    

7.  現在您已完成繪圖，請不要忘了清除在此方法中建立的物件。

    ```C++
    SafeRelease(&pPathGeometry);
    SafeRelease(&pSink);
    SafeRelease(&pTransformedGeometry);
    ```

    

## <a name="drawunderline-and-drawstrikethrough"></a>DrawUnderline () 和 DrawStrikethrough () 

[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 也具有可繪製底線和刪除線的回呼。 此範例會繪製底線或刪除線的簡單矩形，但可以繪製其他圖形。

使用 [Direct2D](../direct2d/direct2d-portal.md) 繪製底線是由下列步驟所組成。

1.  首先，建立底線的大小和形狀的 [**D2D1 \_ RECT \_ F**](../direct2d/d2d1-rect-f.md) 結構。 傳遞至 [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline)回呼方法的 [**DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline)底線結構會提供底線的位移、寬度和粗細。

    ```C++
    D2D1_RECT_F rect = D2D1::RectF(
        0,
        underline->offset,
        underline->width,
        underline->offset + underline->thickness
        );
    ```

    

2.  接下來，使用 [**ID2D1Factory：： CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))方法和初始化的 [**D2D1 \_ RECT \_ F**](../direct2d/d2d1-rect-f.md)結構來建立 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)物件。

    ```C++
    ID2D1RectangleGeometry* pRectangleGeometry = NULL;
    hr = pD2DFactory_->CreateRectangleGeometry(
            &rect, 
            &pRectangleGeometry
            );
    ```

    

3.  如同圖像執行，必須使用 [**CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) 方法，根據基準原點值轉譯底線幾何的來源。

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

    

4.  最後，繪製已轉換幾何的外框，並使用 [**ID2D1RenderTarget：:D rawgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 和 [**ID2D1RenderTarget：： FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法，並將 [Direct2D](../direct2d/direct2d-portal.md) 筆刷儲存為成員變數來填滿。

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

    

5.  現在您已完成繪圖，請不要忘了清除在此方法中建立的物件。

    ```C++
    SafeRelease(&pRectangleGeometry);
    SafeRelease(&pTransformedGeometry);
    ```

    

繪製刪除線的程式相同。 不過，刪除線會有不同的位移，且可能會有不同的寬度和粗細。

## <a name="pixel-snapping-pixels-per-dip-and-transform"></a>圖元貼齊、每個 DIP 的圖元和轉換

### <a name="ispixelsnappingdisabled"></a>IsPixelSnappingDisabled () 

呼叫這個方法來判斷是否停用圖元貼齊。 建議的預設值為 **FALSE**，這是此範例的輸出。


```C++
*isDisabled = FALSE;
```



### <a name="getcurrenttransform"></a>GetCurrentTransform () 

此範例會轉譯成 Direct2D 轉譯目標，因此請使用 [**ID2D1RenderTarget：： GetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettransform)從轉譯目標轉送轉換。


```C++
//forward the render target's transform
pRT_->GetTransform(reinterpret_cast<D2D1_MATRIX_3X2_F*>(transform));
```



### <a name="getpixelsperdip"></a>GetPixelsPerDip () 

呼叫這個方法來取得每個裝置的圖元數， (DIP) 的圖元數。


```C++
float x, yUnused;

pRT_->GetDpi(&x, &yUnused);
*pixelsPerDip = x / 96;
```



## <a name="drawinlineobject"></a>DrawInlineObject () 

自訂文字轉譯器也有繪製内嵌物件的回呼。 在此範例中， [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject) 會傳回 E \_ >notimpl。 說明如何繪製内嵌物件已超出本教學課程的範圍。 如需詳細資訊，請參閱 [如何將内嵌物件加入至文字版面](how-to-add-inline-objects-to-a-text-layout.md) 配置主題。

## <a name="the-destructor"></a>函式

請務必釋放自訂文字轉譯器類別所使用的任何指標。


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
    SafeRelease(&pOutlineBrush_);
    SafeRelease(&pFillBrush_);
}
```



## <a name="using-the-custom-text-renderer"></a>使用自訂文字轉譯器

您可以使用 [**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) 方法，以自訂轉譯器轉譯，此方法會採用衍生自 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) 的回呼介面做為引數，如下列程式碼所示。


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



[**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw)方法會呼叫您提供的自訂轉譯器回呼的方法。 上面所述的 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)、 [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline)、 [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)和 [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) 方法會執行繪圖函數。

 

 