---
title: 如何將内嵌物件加入至文字版面配置
description: 提供簡短的教學課程，說明如何在 DirectWrite 應用程式中加入内嵌物件，以使用 IDWriteTextLayout 介面來顯示文字。
ms.assetid: 6aa9d17c-ee30-497f-9c73-ec2fa079222b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d9ef34e38ec9b84afd887e565e76efb9618b88
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104557161"
---
# <a name="how-to-add-inline-objects-to-a-text-layout"></a><span data-ttu-id="5a07d-103">如何將内嵌物件加入至文字版面配置</span><span class="sxs-lookup"><span data-stu-id="5a07d-103">How to Add Inline Objects to a Text Layout</span></span>

<span data-ttu-id="5a07d-104">提供簡短的教學課程，說明如何在 [DirectWrite](direct-write-portal.md) 應用程式中加入内嵌物件，以使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面來顯示文字。</span><span class="sxs-lookup"><span data-stu-id="5a07d-104">Provides a short tutorial on adding inline objects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="5a07d-105">本教學課程的最終產品是應用程式，它會顯示內嵌內嵌影像的文字，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="5a07d-105">The end product of this tutorial is an application that displays text with an inline image embedded in it, as shown in the following screen shot.</span></span>

![內嵌影像的 [内嵌物件範例] 螢幕擷取畫面](images/inlineobject.png)

<span data-ttu-id="5a07d-107">本教學課程包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="5a07d-107">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="5a07d-108">步驟1：建立文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="5a07d-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="5a07d-109">步驟2：定義衍生自 IDWriteInlineObject 介面的類別。</span><span class="sxs-lookup"><span data-stu-id="5a07d-109">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>](#step-2-define-a-class-derived-from-the-idwriteinlineobject-interface)
-   [<span data-ttu-id="5a07d-110">步驟3：執行內嵌物件類別。</span><span class="sxs-lookup"><span data-stu-id="5a07d-110">Step 3: Implement the Inline Object Class.</span></span>](#step-3-implement-the-inline-object-class)
    -   [<span data-ttu-id="5a07d-111">函數。</span><span class="sxs-lookup"><span data-stu-id="5a07d-111">The Constructor.</span></span>](#the-constructor)
    -   [<span data-ttu-id="5a07d-112">Draw 方法。</span><span class="sxs-lookup"><span data-stu-id="5a07d-112">The Draw Method.</span></span>](#the-draw-method)
    -   [<span data-ttu-id="5a07d-113">GetMetrics 方法。</span><span class="sxs-lookup"><span data-stu-id="5a07d-113">The GetMetrics Method.</span></span>](#the-getmetrics-method)
    -   [<span data-ttu-id="5a07d-114">GetOverhangMetrics 方法。</span><span class="sxs-lookup"><span data-stu-id="5a07d-114">The GetOverhangMetrics Method.</span></span>](#the-getoverhangmetrics-method)
    -   [<span data-ttu-id="5a07d-115">GetBreakConditions 方法。</span><span class="sxs-lookup"><span data-stu-id="5a07d-115">The GetBreakConditions Method.</span></span>](#the-getbreakconditions-method)
-   [<span data-ttu-id="5a07d-116">步驟4：建立 InlineImage 類別的實例，並將它加入至文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="5a07d-116">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>](#step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="5a07d-117">步驟1：建立文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="5a07d-117">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="5a07d-118">若要開始，您將需要具有 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5a07d-118">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="5a07d-119">如果您的應用程式會顯示具有文字版面配置的文字，請跳至步驟2。</span><span class="sxs-lookup"><span data-stu-id="5a07d-119">If you already have an application that displays text with a text layout, skip to Step 2.</span></span>

<span data-ttu-id="5a07d-120">若要加入文字版面配置，您必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="5a07d-120">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="5a07d-121">宣告 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面的指標做為類別的成員。</span><span class="sxs-lookup"><span data-stu-id="5a07d-121">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="5a07d-122">在 CreateDeviceIndependentResources 方法的結尾，藉由呼叫 [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)方法來建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面物件。</span><span class="sxs-lookup"><span data-stu-id="5a07d-122">At the end of the CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="5a07d-123">然後，您必須將 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法的呼叫變更為 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="5a07d-123">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), as shown in the following code.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

## <a name="step-2-define-a-class-derived-from-the-idwriteinlineobject-interface"></a><span data-ttu-id="5a07d-124">步驟2：定義衍生自 IDWriteInlineObject 介面的類別。</span><span class="sxs-lookup"><span data-stu-id="5a07d-124">Step 2: Define a class derived from the IDWriteInlineObject interface.</span></span>

<span data-ttu-id="5a07d-125">[DirectWrite](direct-write-portal.md)中的内嵌物件支援是由 [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)介面提供。</span><span class="sxs-lookup"><span data-stu-id="5a07d-125">Support for inline objects in [DirectWrite](direct-write-portal.md) is provided by the [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) interface.</span></span> <span data-ttu-id="5a07d-126">若要使用内嵌物件，您必須執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="5a07d-126">To use inline objects, you must implement this interface.</span></span> <span data-ttu-id="5a07d-127">它會處理内嵌物件的繪製，以及提供度量和其他資訊給轉譯器。</span><span class="sxs-lookup"><span data-stu-id="5a07d-127">It handles the drawing of the inline object, as well as providing metrics and other information to the renderer.</span></span>

<span data-ttu-id="5a07d-128">建立新的標頭檔，並宣告名為 InlineImage 的介面，該介面衍生自 [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)。</span><span class="sxs-lookup"><span data-stu-id="5a07d-128">Create a new header file and declare an interface called InlineImage, derived from [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject).</span></span>

<span data-ttu-id="5a07d-129">除了從 IUnknown 繼承的 QueryInterface、AddRef 和 Release 之外，此類別必須有下列方法：</span><span class="sxs-lookup"><span data-stu-id="5a07d-129">In addition to QueryInterface, AddRef, and Release inherited from IUnknown, this class must have the following methods:</span></span>

-   [<span data-ttu-id="5a07d-130">**Draw**</span><span class="sxs-lookup"><span data-stu-id="5a07d-130">**Draw**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)
-   [<span data-ttu-id="5a07d-131">**GetMetrics**</span><span class="sxs-lookup"><span data-stu-id="5a07d-131">**GetMetrics**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics)
-   [<span data-ttu-id="5a07d-132">**GetOverhangMetrics**</span><span class="sxs-lookup"><span data-stu-id="5a07d-132">**GetOverhangMetrics**</span></span>](idwriteinlineobject-getoverhangmetrics.md)
-   [<span data-ttu-id="5a07d-133">**GetBreakConditions**</span><span class="sxs-lookup"><span data-stu-id="5a07d-133">**GetBreakConditions**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getbreakconditions)

## <a name="step-3-implement-the-inline-object-class"></a><span data-ttu-id="5a07d-134">步驟3：執行內嵌物件類別。</span><span class="sxs-lookup"><span data-stu-id="5a07d-134">Step 3: Implement the Inline Object Class.</span></span>

<span data-ttu-id="5a07d-135">建立新的 c + + 檔案（名為 InlineImage），以進行類別的執行。</span><span class="sxs-lookup"><span data-stu-id="5a07d-135">Create a new C++ file, named InlineImage.cpp, for the class implementation.</span></span> <span data-ttu-id="5a07d-136">除了 LoadBitmapFromFile 方法和繼承自 IUnknown 介面的方法之外，InlineImage 類別是由下列方法所組成。</span><span class="sxs-lookup"><span data-stu-id="5a07d-136">In addition to the LoadBitmapFromFile method and the methods inherited from the IUnknown interface, the InlineImage class is made up of the following methods.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="5a07d-137">函數。</span><span class="sxs-lookup"><span data-stu-id="5a07d-137">The Constructor.</span></span>


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



<span data-ttu-id="5a07d-138">此函式的第一個引數是要呈現內嵌影像的 ID2D1RenderTarget。</span><span class="sxs-lookup"><span data-stu-id="5a07d-138">The first argument of the constructor is the ID2D1RenderTarget that the inline image will be rendered to.</span></span> <span data-ttu-id="5a07d-139">這會儲存以供稍後繪製時使用。</span><span class="sxs-lookup"><span data-stu-id="5a07d-139">This is stored for use later when drawing.</span></span>

<span data-ttu-id="5a07d-140">轉譯目標、IWICImagingFactory 和檔案名 uri 都會傳遞給載入點陣圖的 LoadBitmapFromFile 方法，並將點陣圖大小 (寬度和高度) 儲存在 rect \_ 成員變數中。</span><span class="sxs-lookup"><span data-stu-id="5a07d-140">The render target, IWICImagingFactory, and the filename uri are all passed to the LoadBitmapFromFile method that loads the bitmap and stores the bitmap size (width and height) in the rect\_ member variable.</span></span>

### <a name="the-draw-method"></a><span data-ttu-id="5a07d-141">Draw 方法。</span><span class="sxs-lookup"><span data-stu-id="5a07d-141">The Draw Method.</span></span>

<span data-ttu-id="5a07d-142">[**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw)方法是 [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer)物件在需要繪製内嵌物件時所呼叫的回呼。</span><span class="sxs-lookup"><span data-stu-id="5a07d-142">The [**Draw**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-draw) method is a callback that is called by the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) object when the inline object needs to be drawn.</span></span> <span data-ttu-id="5a07d-143">文字版面配置不會直接呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="5a07d-143">The text layout does not call this method directly.</span></span>


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



<span data-ttu-id="5a07d-144">在此情況下，使用 [**ID2D1RenderTarget：:D rawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) 方法來繪製點陣圖：不過，您可以使用任何繪圖的方法。</span><span class="sxs-lookup"><span data-stu-id="5a07d-144">In this case, drawing the bitmap is done by using the [**ID2D1RenderTarget::DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) method; however, any method for drawing can be used.</span></span>

### <a name="the-getmetrics-method"></a><span data-ttu-id="5a07d-145">GetMetrics 方法。</span><span class="sxs-lookup"><span data-stu-id="5a07d-145">The GetMetrics Method.</span></span>


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



<span data-ttu-id="5a07d-146">針對 [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) 方法，將寬度、高度和基準儲存在 DWRITE 的 [**\_ 內嵌 \_ 物件 \_ 度量**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) 結構中。</span><span class="sxs-lookup"><span data-stu-id="5a07d-146">For the [**GetMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwriteinlineobject-getmetrics) method, store the width, height and baseline in an [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) structure.</span></span> <span data-ttu-id="5a07d-147">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 會呼叫這個回呼函式來取得内嵌物件的度量。</span><span class="sxs-lookup"><span data-stu-id="5a07d-147">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the measurement of the inline object.</span></span>

### <a name="the-getoverhangmetrics-method"></a><span data-ttu-id="5a07d-148">GetOverhangMetrics 方法。</span><span class="sxs-lookup"><span data-stu-id="5a07d-148">The GetOverhangMetrics Method.</span></span>


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



<span data-ttu-id="5a07d-149">在此情況下，不需要任何懸垂，因此 [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) 方法會傳回所有的零。</span><span class="sxs-lookup"><span data-stu-id="5a07d-149">In this case, no overhang is necessary, so the [**GetOverhangMetrics**](idwriteinlineobject-getoverhangmetrics.md) method returns all zeros.</span></span>

### <a name="the-getbreakconditions-method"></a><span data-ttu-id="5a07d-150">GetBreakConditions 方法。</span><span class="sxs-lookup"><span data-stu-id="5a07d-150">The GetBreakConditions Method.</span></span>


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



## <a name="step-4-create-an-instance-of-the-inlineimage-class-and-add-it-to-the-text-layout"></a><span data-ttu-id="5a07d-151">步驟4：建立 InlineImage 類別的實例，並將它加入至文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="5a07d-151">Step 4: Create an Instance of the InlineImage Class and Add it to the Text Layout.</span></span>

<span data-ttu-id="5a07d-152">最後，在 CreateDeviceDependentResources 方法中，建立 InlineImage 類別的實例，並將它加入至文字配置。</span><span class="sxs-lookup"><span data-stu-id="5a07d-152">Finally, in the CreateDeviceDependentResources method, create an instance of the InlineImage class and add it to the text layout.</span></span> <span data-ttu-id="5a07d-153">由於它會保存 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)的參考（也就是裝置相依資源），而且 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 是使用轉譯目標所建立，因此，InlineImage 也會相依于裝置，而且必須重新建立轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="5a07d-153">Because it holds a reference to the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), which is a device dependent resource, and the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is created by using the render target, the InlineImage is also device dependent and must be recreated if the render target is recreated.</span></span>


```C++
// Create an InlineObject.
pInlineImage_ = new InlineImage(pRT_, pWICFactory_, L"img1.jpg");

DWRITE_TEXT_RANGE textRange = {14, 1};

pTextLayout_->SetInlineObject(pInlineImage_, textRange);
```



<span data-ttu-id="5a07d-154">[**IDWriteTextLayout：： SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject)方法會接受文字範圍結構。</span><span class="sxs-lookup"><span data-stu-id="5a07d-154">The [**IDWriteTextLayout::SetInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject) method takes a text range structure.</span></span> <span data-ttu-id="5a07d-155">此物件適用于此處指定的範圍，而且會隱藏範圍中的任何文字。</span><span class="sxs-lookup"><span data-stu-id="5a07d-155">The object applies to the range specified here, and any text in the range will be suppressed.</span></span> <span data-ttu-id="5a07d-156">如果文字範圍的長度為0，則不會繪製物件。</span><span class="sxs-lookup"><span data-stu-id="5a07d-156">If the length of the text range is 0, the object will not be drawn.</span></span>

<span data-ttu-id="5a07d-157">在此範例中，會有一個星號 (\*) 作為影像顯示位置的預留位置。</span><span class="sxs-lookup"><span data-stu-id="5a07d-157">In this example, there is an asterisk (\*) as a place holder in the position where the image will be displayed.</span></span>


```C++
// The string to display.  The '*' character will be suppressed by our image.
wszText_ = L"Inline Object * Example";
cTextLength_ = wcslen(wszText_);
```



<span data-ttu-id="5a07d-158">由於 InlineImage 類別相依于 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)，因此您必須在釋放轉譯目標時釋放它。</span><span class="sxs-lookup"><span data-stu-id="5a07d-158">Since the InlineImage class is dependent on the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), you must release it when you release the render target.</span></span>


```C++
SafeRelease(&pInlineImage_);
```



 

 