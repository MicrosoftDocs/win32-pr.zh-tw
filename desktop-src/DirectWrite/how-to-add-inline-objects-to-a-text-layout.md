---
title: 如何將内嵌物件加入至文字版面配置
description: 提供簡短的教學課程，說明如何在使用 IDWriteTextLayout 介面顯示文字的 DirectWrite 應用程式中加入内嵌物件。
ms.assetid: 6aa9d17c-ee30-497f-9c73-ec2fa079222b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca4969ded311bbaa4e87e5b70f1df1379c4ca549d2db06c8d1186ba548c77a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902890"
---
# <a name="how-to-add-inline-objects-to-a-text-layout"></a>如何將内嵌物件加入至文字版面配置

提供簡短的教學課程，說明如何在使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面顯示文字的 [DirectWrite](direct-write-portal.md)應用程式中加入内嵌物件。

本教學課程的最終產品是應用程式，它會顯示內嵌內嵌影像的文字，如下列螢幕擷取畫面所示。

![內嵌影像的 [内嵌物件範例] 螢幕擷取畫面](images/inlineobject.png)

本教學課程包含下列部分：

-   [步驟1：建立文字版面配置。](#step-1-create-a-text-layout)
-   [步驟2：定義衍生自 IDWriteInlineObject 介面的類別。](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [步驟3：執行內嵌物件類別。](#step-3-implement-the-inline-object-class)
    -   [函數。](#the-constructor)
    -   [Draw 方法。](#the-draw-method)
    -   [GetMetrics 方法。](#the-getmetrics-method)
    -   [GetOverhangMetrics 方法。](#the-getoverhangmetrics-method)
    -   [GetBreakConditions 方法。](#the-getbreakconditions-method)
-   [步驟4：建立 InlineImage 類別的實例，並將它加入至文字版面配置。](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a>步驟1：建立文字版面配置。

若要開始，您將需要具有 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件的應用程式。 如果您的應用程式會顯示具有文字版面配置的文字，請跳至步驟2。

若要加入文字版面配置，您必須執行下列動作：

1.  宣告 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面的指標做為類別的成員。
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  在 CreateDeviceIndependentResources 方法的結尾，藉由呼叫 [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)方法來建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面物件。
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

    

3.  然後，您必須將 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法的呼叫變更為 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)，如下列程式碼所示。
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a>步驟2：定義衍生自 IDWriteInlineObject 介面的類別。

[DirectWrite](direct-write-portal.md)中的内嵌物件支援是由 [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)介面提供。 若要使用内嵌物件，您必須執行這個介面。 它會處理内嵌物件的繪製，以及提供度量和其他資訊給轉譯器。

建立新的標頭檔，並宣告名為 InlineImage 的介面，該介面衍生自 [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)。

除了從 IUnknown 繼承的 QueryInterface、AddRef 和 Release 之外，此類別必須有下列方法：

-   [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md)
-   [**GetBreakConditions**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a>步驟3：執行內嵌物件類別。

建立新的 c + + 檔案（名為 InlineImage），以進行類別的執行。 除了 LoadBitmapFromFile 方法和繼承自 IUnknown 介面的方法之外，InlineImage 類別是由下列方法所組成。

### <a name="the-constructor"></a>函數。


```C++
InlineImage::InlineImage(
    ID2D1RenderTarget *pRenderTarget, 
    IWICImagingFactory *pIWICFactory,
    PCWSTR uri
    )
{
    // Save the render target for later.
    pRT_ = pRenderTarget;

    pRT_->AddRef();

    // Load the bitmap from a file.
    LoadBitmapFromFile(
        pRenderTarget,
        pIWICFactory,
        uri,
        &pBitmap_
        );
}
```



此函式的第一個引數是要呈現內嵌影像的 ID2D1RenderTarget。 這會儲存以供稍後繪製時使用。

轉譯目標、IWICImagingFactory 和檔案名 uri 都會傳遞給載入點陣圖的 LoadBitmapFromFile 方法，並將點陣圖大小 (寬度和高度) 儲存在 rect \_ 成員變數中。

### <a name="the-draw-method"></a>Draw 方法。

[**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)方法是 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)物件在需要繪製内嵌物件時所呼叫的回呼。 文字版面配置不會直接呼叫這個方法。


```C++
HRESULT STDMETHODCALLTYPE InlineImage::Draw(
    __maybenull void* clientDrawingContext,
    IDWriteTextRenderer* renderer,
    FLOAT originX,
    FLOAT originY,
    BOOL isSideways,
    BOOL isRightToLeft,
    IUnknown* clientDrawingEffect
    )
{
    float height    = rect_.bottom - rect_.top;
    float width     = rect_.right  - rect_.left;
    D2D1_RECT_F destRect  = {originX, originY, originX + width, originY + height};

    pRT_->DrawBitmap(pBitmap_, destRect);

    return S_OK;
}
```



在此情況下，使用 [**ID2D1RenderTarget：:D rawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) 方法來繪製點陣圖：不過，您可以使用任何繪圖的方法。

### <a name="the-getmetrics-method"></a>GetMetrics 方法。


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetMetrics(
    __out DWRITE_INLINE_OBJECT_METRICS* metrics
    )
{
    DWRITE_INLINE_OBJECT_METRICS inlineMetrics = {};
    inlineMetrics.width     = rect_.right  - rect_.left;
    inlineMetrics.height    = rect_.bottom - rect_.top;
    inlineMetrics.baseline  = baseline_;
    *metrics = inlineMetrics;
    return S_OK;
}
```



針對 [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) 方法，將寬度、高度和基準儲存在 DWRITE 的 [**\_ 內嵌 \_ 物件 \_ 度量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) 結構中。 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 會呼叫這個回呼函式來取得内嵌物件的度量。

### <a name="the-getoverhangmetrics-method"></a>GetOverhangMetrics 方法。


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetOverhangMetrics(
    __out DWRITE_OVERHANG_METRICS* overhangs
    )
{
    overhangs->left      = 0;
    overhangs->top       = 0;
    overhangs->right     = 0;
    overhangs->bottom    = 0;
    return S_OK;
}
```



在此情況下，不需要任何懸垂，因此 [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) 方法會傳回所有的零。

### <a name="the-getbreakconditions-method"></a>GetBreakConditions 方法。


```C++
HRESULT STDMETHODCALLTYPE InlineImage::GetBreakConditions(
    __out DWRITE_BREAK_CONDITION* breakConditionBefore,
    __out DWRITE_BREAK_CONDITION* breakConditionAfter
    )
{
    *breakConditionBefore = DWRITE_BREAK_CONDITION_NEUTRAL;
    *breakConditionAfter  = DWRITE_BREAK_CONDITION_NEUTRAL;
    return S_OK;
}
```



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a>步驟4：建立 InlineImage 類別的實例，並將它加入至文字版面配置。

最後，在 CreateDeviceDependentResources 方法中，建立 InlineImage 類別的實例，並將它加入至文字配置。 由於它會保存 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)的參考（也就是裝置相依資源），而且 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 是使用轉譯目標所建立，因此，InlineImage 也會相依于裝置，而且必須重新建立轉譯目標。


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



[**IDWriteTextLayout：： SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject)方法會接受文字範圍結構。 此物件適用于此處指定的範圍，而且會隱藏範圍中的任何文字。 如果文字範圍的長度為0，則不會繪製物件。

在此範例中，會有一個星號 (\*) 作為影像顯示位置的預留位置。


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



由於 InlineImage 類別相依于 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)，因此您必須在釋放轉譯目標時釋放它。


```C++
SafeRelease(&pInlineImage_);
```



 

 