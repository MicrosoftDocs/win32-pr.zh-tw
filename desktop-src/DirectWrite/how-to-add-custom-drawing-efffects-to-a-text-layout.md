---
title: 如何將用戶端繪製效果新增至文字版面配置
description: 提供簡短的教學課程，說明如何將用戶端繪製效果新增至 DirectWrite 應用程式，該應用程式會使用 IDWriteTextLayout 介面和自訂文字轉譯器來顯示文字。
ms.assetid: b66ff814-2113-48b0-8913-3d30a5d20077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338dc1a720bde80c1daf2b4baf7c7a4bad6d2cff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023731"
---
# <a name="how-to-add-client-drawing-effects-to-a-text-layout"></a><span data-ttu-id="22fd9-103">如何將用戶端繪製效果新增至文字版面配置</span><span class="sxs-lookup"><span data-stu-id="22fd9-103">How to Add Client Drawing Effects to a Text Layout</span></span>

<span data-ttu-id="22fd9-104">提供簡短的教學課程，說明如何將用戶端繪製效果新增至 [DirectWrite](direct-write-portal.md) 應用程式，該應用程式會使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面和自訂文字轉譯器來顯示文字。</span><span class="sxs-lookup"><span data-stu-id="22fd9-104">Provides a short tutorial on adding client drawing effects to a [DirectWrite](direct-write-portal.md) application that displays text using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface and a custom text renderer.</span></span>

<span data-ttu-id="22fd9-105">本教學課程的最終產品是一種應用程式，它會顯示具有不同色彩繪製效果之文字範圍的文字，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="22fd9-105">The end product of this tutorial is an application that displays text that has ranges of text with a different color drawing effect on each, as shown in the following screen shot.</span></span>

![[用戶端繪圖效果範例！] 的螢幕擷取畫面](images/drawingeffects.png)

> [!Note]  
> <span data-ttu-id="22fd9-108">本教學課程是一個簡化的範例，說明如何建立自訂用戶端繪製效果，而不是用來繪製色彩文字的簡單方法範例。</span><span class="sxs-lookup"><span data-stu-id="22fd9-108">This tutorial is meant to be a simplified example of how to create custom client drawing effects, not an example of a simple method for drawing color text.</span></span> <span data-ttu-id="22fd9-109">如需詳細資訊，請參閱 [**IDWriteTextLayout：： SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) 參考頁面。</span><span class="sxs-lookup"><span data-stu-id="22fd9-109">See the [**IDWriteTextLayout::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) reference page for more information.</span></span>

 

<span data-ttu-id="22fd9-110">本教學課程包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="22fd9-110">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="22fd9-111">步驟1：建立文字版面配置</span><span class="sxs-lookup"><span data-stu-id="22fd9-111">Step 1: Create a Text Layout</span></span>](#step-1-create-a-text-layout)
-   [<span data-ttu-id="22fd9-112">步驟2：執行自訂繪製效果類別</span><span class="sxs-lookup"><span data-stu-id="22fd9-112">Step 2: Implement a Custom Drawing Effect Class</span></span>](#step-2-implement-a-custom-drawing-effect-class)
-   [<span data-ttu-id="22fd9-113">步驟3：執行自訂文字轉譯器類別</span><span class="sxs-lookup"><span data-stu-id="22fd9-113">Step 3: Implement a Custom Text Renderer Class</span></span>](#step-3-implement-a-custom-text-renderer-class)
    -   [<span data-ttu-id="22fd9-114">函數</span><span class="sxs-lookup"><span data-stu-id="22fd9-114">The Constructor</span></span>](#the-constructor)
    -   [<span data-ttu-id="22fd9-115">DrawGlyphRun 方法</span><span class="sxs-lookup"><span data-stu-id="22fd9-115">The DrawGlyphRun Method</span></span>](#the-drawglyphrun-method)
    -   [<span data-ttu-id="22fd9-116">函式</span><span class="sxs-lookup"><span data-stu-id="22fd9-116">The Destructor</span></span>](#the-destructor)
-   [<span data-ttu-id="22fd9-117">步驟4：建立文字轉譯器</span><span class="sxs-lookup"><span data-stu-id="22fd9-117">Step 4: Create the Text Renderer</span></span>](#step-4-create-the-text-renderer)
-   [<span data-ttu-id="22fd9-118">步驟5：將色彩繪製效果物件具現化</span><span class="sxs-lookup"><span data-stu-id="22fd9-118">Step 5: Instantiate the Color Drawing Effect Objects</span></span>](#step-5-instantiate-the-color-drawing-effect-objects)
-   [<span data-ttu-id="22fd9-119">步驟6：設定特定文字範圍的繪圖效果</span><span class="sxs-lookup"><span data-stu-id="22fd9-119">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>](#step-6-set-the-drawing-effect-for-specific-text-ranges)
-   [<span data-ttu-id="22fd9-120">步驟7：使用自訂轉譯器繪製文字版面配置</span><span class="sxs-lookup"><span data-stu-id="22fd9-120">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>](#step-7-draw-the-text-layout-using-the-custom-renderer)
-   [<span data-ttu-id="22fd9-121">步驟8：清除</span><span class="sxs-lookup"><span data-stu-id="22fd9-121">Step 8: Clean up</span></span>](#step-8-clean-up)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="22fd9-122">步驟1：建立文字版面配置</span><span class="sxs-lookup"><span data-stu-id="22fd9-122">Step 1: Create a Text Layout</span></span>

<span data-ttu-id="22fd9-123">若要開始，您將需要具有 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="22fd9-123">To begin, you will need an application with an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="22fd9-124">如果您的應用程式會顯示具有文字版面配置的文字，或您正在使用自訂的 DrawingEffect 範例程式碼，請跳至步驟2。</span><span class="sxs-lookup"><span data-stu-id="22fd9-124">If you already have an application that displays text with a text layout, or you are using the Custom DrawingEffect Example Code, skip to Step 2.</span></span>

<span data-ttu-id="22fd9-125">若要加入文字版面配置，您必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="22fd9-125">To add a text layout you must do the following:</span></span>

1.  <span data-ttu-id="22fd9-126">宣告 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面的指標做為類別的成員。</span><span class="sxs-lookup"><span data-stu-id="22fd9-126">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="22fd9-127">在 **CreateDeviceIndependentResources** 方法的結尾，藉由呼叫 [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)方法來建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面物件。</span><span class="sxs-lookup"><span data-stu-id="22fd9-127">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>
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

    

3.  <span data-ttu-id="22fd9-128">最後，請記得釋出函式中的文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="22fd9-128">Finally, remember to release the text layout in the destructor.</span></span>
    ```C++
    SafeRelease(&pTextLayout_);
    ```

    

## <a name="step-2-implement-a-custom-drawing-effect-class"></a><span data-ttu-id="22fd9-129">步驟2：執行自訂繪製效果類別</span><span class="sxs-lookup"><span data-stu-id="22fd9-129">Step 2: Implement a Custom Drawing Effect Class</span></span>

<span data-ttu-id="22fd9-130">除了繼承自 IUnknown 的方法以外，自訂用戶端繪製效果介面沒有任何要求必須執行的需求。</span><span class="sxs-lookup"><span data-stu-id="22fd9-130">Other than the methods inherited from IUnknown, a custom client drawing effect interface has no requirements as to what it must implement.</span></span> <span data-ttu-id="22fd9-131">在此情況下， **ColorDrawingEffect** 類別只會保存 [**D2D1 \_ COLOR \_ F**](../direct2d/d2d1-color-f.md) 值，並宣告取得和設定此值的方法，以及可設定一開始色彩的函式。</span><span class="sxs-lookup"><span data-stu-id="22fd9-131">In this case, the **ColorDrawingEffect** class simply holds a [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value and declares methods to get and set this value, as well as a constructor that can set the color initially.</span></span>

<span data-ttu-id="22fd9-132">將用戶端繪製效果套用至 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件中的文字範圍之後，繪製效果會傳遞至要轉譯之任何圖像執行的 [**IDWriteTextRenderer：:D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) 方法。</span><span class="sxs-lookup"><span data-stu-id="22fd9-132">After a client drawing effect is applied to a text range in a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, the drawing effect is passed to the [**IDWriteTextRenderer::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of any glyph run that is to be rendered.</span></span> <span data-ttu-id="22fd9-133">然後，文字轉譯器可以使用繪製效果的方法。</span><span class="sxs-lookup"><span data-stu-id="22fd9-133">The methods of the drawing effect are then available to the text renderer.</span></span>

<span data-ttu-id="22fd9-134">用戶端繪製效果可以像您想要的一樣複雜、攜帶更多資訊，而不是在此範例中，以及提供方法來改變圖像、建立要用於繪圖的物件等等。</span><span class="sxs-lookup"><span data-stu-id="22fd9-134">A client drawing effect can be as complex as you want to make it, carrying more information than in this example, as well as providing methods to alter glyphs, create objects to be used for drawing, and so on.</span></span>

## <a name="step-3-implement-a-custom-text-renderer-class"></a><span data-ttu-id="22fd9-135">步驟3：執行自訂文字轉譯器類別</span><span class="sxs-lookup"><span data-stu-id="22fd9-135">Step 3: Implement a Custom Text Renderer Class</span></span>

<span data-ttu-id="22fd9-136">為了充分利用用戶端繪製效果，您必須先執行自訂文字轉譯器。</span><span class="sxs-lookup"><span data-stu-id="22fd9-136">In order to take advantage of a client drawing effect, you must implement a custom text renderer.</span></span> <span data-ttu-id="22fd9-137">此文字轉譯器會將 [**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) 方法傳遞給它的繪製效果，套用至繪製的圖像執行。</span><span class="sxs-lookup"><span data-stu-id="22fd9-137">This text renderer will apply the drawing effect passed to it by the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method to the glyph run being drawn.</span></span>

### <a name="the-constructor"></a><span data-ttu-id="22fd9-138">函數</span><span class="sxs-lookup"><span data-stu-id="22fd9-138">The Constructor</span></span>

<span data-ttu-id="22fd9-139">自訂文字轉譯器的函式會儲存將用來建立 [Direct2D](../direct2d/direct2d-portal.md)物件的 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)物件，以及要在其上繪製文字的 Direct2D 呈現目標。</span><span class="sxs-lookup"><span data-stu-id="22fd9-139">The constructor for the custom text renderer stores the [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object that will be used to create [Direct2D](../direct2d/direct2d-portal.md) objects, and the Direct2D render target that the text will be drawn on to.</span></span>


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



### <a name="the-drawglyphrun-method"></a><span data-ttu-id="22fd9-140">DrawGlyphRun 方法</span><span class="sxs-lookup"><span data-stu-id="22fd9-140">The DrawGlyphRun Method</span></span>

<span data-ttu-id="22fd9-141">圖像執行是一組共用相同格式的圖像，包括用戶端繪製效果。</span><span class="sxs-lookup"><span data-stu-id="22fd9-141">A glyph run is a set of glyphs that share the same format, including the client drawing effect.</span></span> <span data-ttu-id="22fd9-142">[**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)方法會處理指定之圖像執行的文字呈現。</span><span class="sxs-lookup"><span data-stu-id="22fd9-142">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method takes care of the text rendering for a specified glyph run.</span></span>

<span data-ttu-id="22fd9-143">首先，建立 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) 和 [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)，然後使用 [**IDWriteFontFace：： GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline)來取得圖像執行大綱。</span><span class="sxs-lookup"><span data-stu-id="22fd9-143">First, create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink), and then retrieve the glyph run outline by using [**IDWriteFontFace::GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline).</span></span> <span data-ttu-id="22fd9-144">然後使用 [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory：： CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) 方法來轉換幾何的原點，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="22fd9-144">Then transform the origin of the geometry by using the [Direct2D](../direct2d/direct2d-portal.md) [**ID2D1Factory::CreateTransformedGeometry**](../direct2d/id2d1factory-createtransformedgeometry.md) method, as shown in the following code.</span></span>


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



<span data-ttu-id="22fd9-145">接下來，宣告 [Direct2D](../direct2d/direct2d-portal.md) 實心筆刷物件。</span><span class="sxs-lookup"><span data-stu-id="22fd9-145">Next, declare a [Direct2D](../direct2d/direct2d-portal.md) solid brush object.</span></span>


```C++
ID2D1SolidColorBrush* pBrush = NULL;
```



<span data-ttu-id="22fd9-146">如果 *clientDrawingEffect* 參數不是 Null，請查詢 **ColorDrawingEffect** 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="22fd9-146">If the *clientDrawingEffect* parameter is not NULL, query the object for the **ColorDrawingEffect** interface.</span></span> <span data-ttu-id="22fd9-147">這將會運作，因為您會將此類別設定為文字版面設定物件文字範圍的用戶端繪製效果。</span><span class="sxs-lookup"><span data-stu-id="22fd9-147">This will work because you will set this class as the client drawing effect on text ranges of the text layout object.</span></span>

<span data-ttu-id="22fd9-148">一旦您有 **ColorDrawingEffect** 介面的指標，您就可以使用 **GetColor** 方法來取得它所儲存的 [**D2D1 \_ COLOR \_ F**](../direct2d/d2d1-color-f.md)值。</span><span class="sxs-lookup"><span data-stu-id="22fd9-148">Once you have a pointer to the **ColorDrawingEffect** interface, you can retrieve the [**D2D1\_COLOR\_F**](../direct2d/d2d1-color-f.md) value that it stores using the **GetColor** method.</span></span> <span data-ttu-id="22fd9-149">然後，使用 **D2D1 \_ 色彩 \_ F** 來建立該色彩的 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 。</span><span class="sxs-lookup"><span data-stu-id="22fd9-149">Then, use the **D2D1\_COLOR\_F** to create a [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) in that color.</span></span>

<span data-ttu-id="22fd9-150">如果 *clientDrawingEffect* 參數為 **Null**，則只需建立黑色 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)。</span><span class="sxs-lookup"><span data-stu-id="22fd9-150">If the *clientDrawingEffect* parameter is **NULL**, then just create a black [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


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



<span data-ttu-id="22fd9-151">最後，繪製外框幾何，並使用您剛才建立的純色筆刷來填滿。</span><span class="sxs-lookup"><span data-stu-id="22fd9-151">Finally, draw the outline geometry and fill it using the solid color brush that you just created.</span></span>


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



### <a name="the-destructor"></a><span data-ttu-id="22fd9-152">函式</span><span class="sxs-lookup"><span data-stu-id="22fd9-152">The Destructor</span></span>

<span data-ttu-id="22fd9-153">別忘了釋放 [Direct2D](../direct2d/direct2d-portal.md) factory，並在函式中轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="22fd9-153">Don't forget to release the [Direct2D](../direct2d/direct2d-portal.md) factory and render target in the destructor.</span></span>


```C++
CustomTextRenderer::~CustomTextRenderer()
{
    SafeRelease(&pD2DFactory_);
    SafeRelease(&pRT_);
}
```



## <a name="step-4-create-the-text-renderer"></a><span data-ttu-id="22fd9-154">步驟4：建立文字轉譯器</span><span class="sxs-lookup"><span data-stu-id="22fd9-154">Step 4: Create the Text Renderer</span></span>

<span data-ttu-id="22fd9-155">在 **CreateDeviceDependent** 資源中，建立自訂文字轉譯器物件。</span><span class="sxs-lookup"><span data-stu-id="22fd9-155">In the **CreateDeviceDependent** resources, create the custom text renderer object.</span></span> <span data-ttu-id="22fd9-156">它是裝置相依的，因為它會使用本身相依的 **ID2D1RenderTarget**。</span><span class="sxs-lookup"><span data-stu-id="22fd9-156">It is device dependent because it uses the **ID2D1RenderTarget**, which is itself device dependent.</span></span>


```C++
// Create the text renderer
pTextRenderer_ = new CustomTextRenderer(
                        pD2DFactory_,
                        pRT_
                        );
```



## <a name="step-5-instantiate-the-color-drawing-effect-objects"></a><span data-ttu-id="22fd9-157">步驟5：將色彩繪製效果物件具現化</span><span class="sxs-lookup"><span data-stu-id="22fd9-157">Step 5: Instantiate the Color Drawing Effect Objects</span></span>

<span data-ttu-id="22fd9-158">以紅色、綠色和藍色具現化 **ColorDrawingEffect** 物件。</span><span class="sxs-lookup"><span data-stu-id="22fd9-158">Instantiate **ColorDrawingEffect** objects in red, green, and blue.</span></span>


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



## <a name="step-6-set-the-drawing-effect-for-specific-text-ranges"></a><span data-ttu-id="22fd9-159">步驟6：設定特定文字範圍的繪圖效果</span><span class="sxs-lookup"><span data-stu-id="22fd9-159">Step 6: Set the Drawing Effect for Specific Text Ranges</span></span>

<span data-ttu-id="22fd9-160">使用 [**IDWriteTextLayou：： SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) 方法和 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) 結構，設定特定文字範圍的繪製效果。</span><span class="sxs-lookup"><span data-stu-id="22fd9-160">Set the drawing effect for specific ranges of text by using the [**IDWriteTextLayou::SetDrawingEffect**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect) method and a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) struct.</span></span>


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



## <a name="step-7-draw-the-text-layout-using-the-custom-renderer"></a><span data-ttu-id="22fd9-161">步驟7：使用自訂轉譯器繪製文字版面配置</span><span class="sxs-lookup"><span data-stu-id="22fd9-161">Step 7: Draw the Text Layout Using the Custom Renderer</span></span>

<span data-ttu-id="22fd9-162">您必須呼叫 [**IDWriteTextLayout：:D 原始**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) 方法，而不是 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 或 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法。</span><span class="sxs-lookup"><span data-stu-id="22fd9-162">You must call the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method rather than the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) or [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) methods.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



## <a name="step-8-clean-up"></a><span data-ttu-id="22fd9-163">步驟8：清除</span><span class="sxs-lookup"><span data-stu-id="22fd9-163">Step 8: Clean up</span></span>

<span data-ttu-id="22fd9-164">在 DemoApp 的函式中，釋放自訂文字轉譯器。</span><span class="sxs-lookup"><span data-stu-id="22fd9-164">In the DemoApp destructor, release the custom text renderer.</span></span>


```C++
SafeRelease(&pTextRenderer_);
```



<span data-ttu-id="22fd9-165">之後，新增程式碼以釋出用戶端繪製效果類別。</span><span class="sxs-lookup"><span data-stu-id="22fd9-165">After that, add code to release the client drawing effect classes.</span></span>


```C++
SafeRelease(&redDrawingEffect_);
SafeRelease(&blueDrawingEffect_);
SafeRelease(&greenDrawingEffect_);
```



 

 