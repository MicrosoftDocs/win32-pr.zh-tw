---
title: 如何將用戶端繪製效果新增至文字版面配置
description: 提供簡短的教學課程，說明如何將用戶端繪製效果新增至 DirectWrite 應用程式，以使用 IDWriteTextLayout 介面和自訂文字轉譯器來顯示文字。
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bae98813d8f8aa8fc8a7df0a1a53d11a0329c93abb22a7f60d60754b8edc91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071705"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a>如何將用戶端繪製效果新增至文字版面配置

提供簡短的教學課程，說明如何將用戶端繪製效果新增至 [DirectWrite](direct-write-portal.md)應用程式，以使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面和自訂文字轉譯器來顯示文字。

本教學課程的最終產品是一種應用程式，它會顯示具有不同色彩繪製效果之文字範圍的文字，如下列螢幕擷取畫面所示。

![[用戶端繪圖效果範例！] 的螢幕擷取畫面 不同的色彩](images/drawingeffects.png)

> [!Note]  
> 本教學課程是一個簡化的範例，說明如何建立自訂用戶端繪製效果，而不是用來繪製色彩文字的簡單方法範例。 如需詳細資訊，請參閱 [**IDWriteTextLayout：： SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) 參考頁面。

 

本教學課程包含下列部分：

-   [步驟1：建立文字版面配置](#step-1-create-a-text-layout)
-   [步驟2：執行自訂繪製效果類別](#step-2-implement-a-custom-drawing-effect-class)
-   [步驟3：執行自訂文字轉譯器類別](#step-3-implement-a-custom-text-renderer-class)
    -   [函數](#the-constructor)
    -   [DrawGlyphRun 方法](#the-drawglyphrun-method)
    -   [函式](#the-destructor)
-   [步驟4：建立文字轉譯器](#step-4-create-the-text-renderer)
-   [步驟5：將色彩繪製效果物件具現化](#step-5-instantiate-the-color-drawing-effect-objects)
-   [步驟6：設定特定文字範圍的繪圖效果](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [步驟7：使用自訂轉譯器繪製文字版面配置](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [步驟8：清除](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a>步驟1：建立文字版面配置

若要開始，您將需要具有 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件的應用程式。 如果您的應用程式會顯示具有文字版面配置的文字，或您正在使用自訂的 DrawingEffect 範例程式碼，請跳至步驟2。

若要加入文字版面配置，您必須執行下列動作：

1.  宣告 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面的指標做為類別的成員。
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  在 **CreateDeviceIndependentResources** 方法的結尾，藉由呼叫 [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)方法來建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面物件。
    ```C++
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    
    ```

    

3.  最後，請記得釋出函式中的文字版面配置。
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a>步驟2：執行自訂繪製效果類別

除了繼承自 IUnknown 的方法以外，自訂用戶端繪製效果介面沒有任何要求必須執行的需求。 在此情況下， **ColorDrawingEffect** 類別只會保存 [**D2D1 \_ COLOR \_ F**](../direct2d/d2d1-color-f.md) 值，並宣告取得和設定此值的方法，以及可設定一開始色彩的函式。

將用戶端繪製效果套用至 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件中的文字範圍之後，繪製效果會傳遞至要轉譯之任何圖像執行的 [**IDWriteTextRenderer：:D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) 方法。 然後，文字轉譯器可以使用繪製效果的方法。

用戶端繪製效果可以像您想要的一樣複雜、攜帶更多資訊，而不是在此範例中，以及提供方法來改變圖像、建立要用於繪圖的物件等等。

## <a name="step-3-implement-a-custom-text-renderer-class"></a>步驟3：執行自訂文字轉譯器類別

為了充分利用用戶端繪製效果，您必須先執行自訂文字轉譯器。 此文字轉譯器會將 [**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) 方法傳遞給它的繪製效果，套用至繪製的圖像執行。

### <a name="the-constructor"></a>函數

自訂文字轉譯器的函式會儲存將用來建立 [Direct2D](../direct2d/direct2d-portal.md)物件的 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)物件，以及要在其上繪製文字的 Direct2D 呈現目標。


```C++
CustomTextRenderer::CustomTextRenderer(
    ID2D1Factory* pD2DFactory, 
    ID2D1HwndRenderTarget* pRT
    )
:
cRefCount_(0), 
pD2DFactory_(pD2DFactory), 
pRT_(pRT)
{
    pD2DFactory_->AddRef();
    pRT_->AddRef();
}
```



### <a name="the-drawglyphrun-method"></a>DrawGlyphRun 方法

圖像執行是一組共用相同格式的圖像，包括用戶端繪製效果。 [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)方法會處理指定之圖像執行的文字呈現。

首先，建立 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) 和 [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)，然後使用 [**IDWriteFontFace：： GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline)來取得圖像執行大綱。 然後使用 [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory：： CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) 方法來轉換幾何的原點，如下列程式碼所示。


```C++
HRESULT hr = S_OK;

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

// Close the geometry sink
if (SUCCEEDED(hr))
{
    hr = pSink->Close();
}

// Initialize a matrix to translate the origin of the glyph run.
D2D1::Matrix3x2F const matrix = D2D1::Matrix3x2F(
    1.0f, 0.0f,
    0.0f, 1.0f,
    baselineOriginX, baselineOriginY
    );

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



接下來，宣告 [Direct2D](../direct2d/direct2d-portal.md) 實心筆刷物件。


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



如果 *clientDrawingEffect* 參數不是 Null，請查詢 **ColorDrawingEffect** 介面的物件。 這將會運作，因為您會將此類別設定為文字版面設定物件文字範圍的用戶端繪製效果。

一旦您有 **ColorDrawingEffect** 介面的指標，您就可以使用 **GetColor** 方法來取得它所儲存的 [**D2D1 \_ COLOR \_ F**](../direct2d/d2d1-color-f.md)值。 然後，使用 **D2D1 \_ 色彩 \_ F** 來建立該色彩的 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 。

如果 *clientDrawingEffect* 參數為 **Null**，則只需建立黑色 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)。


```C++
// If there is a drawing effect create a color brush using it, otherwise create a black brush.
if (clientDrawingEffect != NULL)
{
    // Go from IUnknown to ColorDrawingEffect.
    ColorDrawingEffect *colorDrawingEffect;

    clientDrawingEffect->QueryInterface(__uuidof(ColorDrawingEffect), reinterpret_cast<void**>(&colorDrawingEffect));

    // Get the color from the ColorDrawingEffect object.
    D2D1_COLOR_F color;

    colorDrawingEffect->GetColor(&color);

    // Create the brush using the color pecified by our ColorDrawingEffect object.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            color,
            &pBrush);
    }

    SafeRelease(&colorDrawingEffect);
}
else
{
    // Create a black brush.
    if (SUCCEEDED(hr))
    {
        hr = pRT_->CreateSolidColorBrush(
            D2D1::ColorF(
            D2D1::ColorF::Black
            ),
            &pBrush);
    }
}
```



最後，繪製外框幾何，並使用您剛才建立的純色筆刷來填滿。


```C++
if (SUCCEEDED(hr))
{
    // Draw the outline of the glyph run
    pRT_->DrawGeometry(
        pTransformedGeometry,
        pBrush
        );

    // Fill in the glyph run
    pRT_->FillGeometry(
        pTransformedGeometry,
        pBrush
        );
}
```



### <a name="the-destructor"></a>函式

別忘了釋放 [Direct2D](../direct2d/direct2d-portal.md) factory，並在函式中轉譯目標。


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a>步驟4：建立文字轉譯器

在 **CreateDeviceDependent** 資源中，建立自訂文字轉譯器物件。 它是裝置相依的，因為它會使用本身相依的 **ID2D1RenderTarget**。


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a>步驟5：將色彩繪製效果物件具現化

以紅色、綠色和藍色具現化 **ColorDrawingEffect** 物件。


```C++
// Instantiate some custom color drawing effects.
redDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Red
        )
    );

blueDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Blue
        )
    );

greenDrawingEffect_ = new ColorDrawingEffect(
    D2D1::ColorF(
        D2D1::ColorF::Green
        )
    );
```



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a>步驟6：設定特定文字範圍的繪圖效果

使用 [**IDWriteTextLayou：： SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) 方法和 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) 結構，設定特定文字範圍的繪製效果。


```C++
// Set the drawing effects.

// Red.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {0,
                                   14};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(redDrawingEffect_, textRange);
    }
}

// Blue.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {14,
                                   7};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(blueDrawingEffect_, textRange);
    }
}

// Green.
if (SUCCEEDED(hr))
{
    // Set the drawing effect for the specified range.
    DWRITE_TEXT_RANGE textRange = {21,
                                   8};
    if (SUCCEEDED(hr))
    {
        hr = pTextLayout_->SetDrawingEffect(greenDrawingEffect_, textRange);
    }
}
```



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a>步驟7：使用自訂轉譯器繪製文字版面配置

您必須呼叫 [**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) 方法，而不是 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 或 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法。


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a>步驟8：清除

在 DemoApp 的函式中，釋放自訂文字轉譯器。


```C++
SafeRelease(&pTextRenderer_);
```



之後，新增程式碼以釋出用戶端繪製效果類別。


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 