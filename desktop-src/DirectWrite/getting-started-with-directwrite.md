---
title: 使用 DirectWrite 開始使用教學課程
description: 本檔將說明如何使用 DirectWrite 和 Direct2D 來建立包含單一格式的簡單文字，以及包含多個格式的文字。
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite，教學課程
- DirectWrite，快速入門教學課程
- DirectWrite、Direct2D
- Direct2D
- DirectWrite，IDWriteTextLayout 介面
- IDWriteTextLayout 介面
- DirectWrite，IDWriteTypography 介面
- IDWriteTypography 介面
- DirectWrite，IDWriteTextFormat 介面
- IDWriteTextFormat 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fb385ff78650a16599a32d76d7c51ba575de47
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315862"
---
# <a name="tutorial-getting-started-with-directwrite"></a><span data-ttu-id="b3924-113">教學課程：使用 DirectWrite 開始使用</span><span class="sxs-lookup"><span data-stu-id="b3924-113">Tutorial: Getting Started with DirectWrite</span></span>

<span data-ttu-id="b3924-114">本檔將說明如何使用 [DirectWrite](direct-write-portal.md) 和 [Direct2D](rendering-by-using-direct2d.md) 來建立包含單一格式的簡單文字，以及包含多個格式的文字。</span><span class="sxs-lookup"><span data-stu-id="b3924-114">This document shows you how to use [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to create simple text that contains a single format, and then text that contains multiple formats.</span></span>

<span data-ttu-id="b3924-115">本教學課程包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="b3924-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="b3924-116">原始程式碼</span><span class="sxs-lookup"><span data-stu-id="b3924-116">Source Code</span></span>](#source-code)
-   [<span data-ttu-id="b3924-117">繪製簡單文字</span><span class="sxs-lookup"><span data-stu-id="b3924-117">Drawing Simple Text</span></span>](#drawing-simple-text)
    -   [<span data-ttu-id="b3924-118">第1部分：宣告 DirectWrite 和 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="b3924-118">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>](#part-1-declare-directwrite-and-direct2d-resources)
    -   [<span data-ttu-id="b3924-119">第2部分：建立與裝置無關的資源。</span><span class="sxs-lookup"><span data-stu-id="b3924-119">Part 2: Create Device Independent Resources.</span></span>](#part-2-create-device-independent-resources)
    -   [<span data-ttu-id="b3924-120">第3部分：建立 Device-Dependent 資源。</span><span class="sxs-lookup"><span data-stu-id="b3924-120">Part 3: Create Device-Dependent Resources.</span></span>](#part-3-create-device-dependent-resources)
    -   [<span data-ttu-id="b3924-121">第4部分：使用 Direct2D DrawText 方法繪製文字。</span><span class="sxs-lookup"><span data-stu-id="b3924-121">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [<span data-ttu-id="b3924-122">第5部分：使用 Direct2D 轉譯視窗內容</span><span class="sxs-lookup"><span data-stu-id="b3924-122">Part 5: Render the Window Contents Using Direct2D</span></span>](#part-5-render-the-window-contents-using-direct2d)
-   [<span data-ttu-id="b3924-123">繪製具有多種格式的文字。</span><span class="sxs-lookup"><span data-stu-id="b3924-123">Drawing Text with Multiple Formats.</span></span>](#drawing-text-with-multiple-formats)
    -   [<span data-ttu-id="b3924-124">第1部分：建立 IDWriteTextLayout 介面。</span><span class="sxs-lookup"><span data-stu-id="b3924-124">Part 1: Create an IDWriteTextLayout Interface.</span></span>](#part-1-create-an-idwritetextlayout-interface)
    -   [<span data-ttu-id="b3924-125">第2部分：使用 IDWriteTextLayout 套用格式。</span><span class="sxs-lookup"><span data-stu-id="b3924-125">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>](#part-2-applying-formatting-with-idwritetextlayout)
    -   [<span data-ttu-id="b3924-126">第3部分：使用 IDWriteTypography 新增印刷樣式功能。</span><span class="sxs-lookup"><span data-stu-id="b3924-126">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>](#part-3-adding-typographic-features-with-idwritetypography)
    -   [<span data-ttu-id="b3924-127">第4部分：使用 Direct2D DrawTextLayout 方法繪製文字。</span><span class="sxs-lookup"><span data-stu-id="b3924-127">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a><span data-ttu-id="b3924-128">原始程式碼</span><span class="sxs-lookup"><span data-stu-id="b3924-128">Source Code</span></span>

<span data-ttu-id="b3924-129">本總覽所顯示的原始程式碼取自 [DirectWrite Hello World 範例](/samples/browse/?redirectedfrom=MSDN-samples)。</span><span class="sxs-lookup"><span data-stu-id="b3924-129">The source code shown in this overview is taken from the [DirectWrite Hello World sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="b3924-130">每個部分都是在不同的類別中執行 (SimpleText 和 MultiformattedText) ，而且會顯示在另一個子視窗中。</span><span class="sxs-lookup"><span data-stu-id="b3924-130">Each part is implemented in a separate class (SimpleText and MultiformattedText) and is displayed in a separate child window.</span></span> <span data-ttu-id="b3924-131">每個類別都代表一個 Microsoft Win32 視窗。</span><span class="sxs-lookup"><span data-stu-id="b3924-131">Each class represents a Microsoft Win32 window.</span></span> <span data-ttu-id="b3924-132">除了 *WndProc* 方法，每個類別都包含下列方法：</span><span class="sxs-lookup"><span data-stu-id="b3924-132">In addition to the *WndProc* method, each class contains the following methods:</span></span>



| <span data-ttu-id="b3924-133">函式</span><span class="sxs-lookup"><span data-stu-id="b3924-133">Function</span></span>                              | <span data-ttu-id="b3924-134">描述</span><span class="sxs-lookup"><span data-stu-id="b3924-134">Description</span></span>                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3924-135">**CreateDeviceIndependentResources**</span><span class="sxs-lookup"><span data-stu-id="b3924-135">**CreateDeviceIndependentResources**</span></span>  | <span data-ttu-id="b3924-136">建立與裝置無關的資源，讓它們可以在任何地方重複使用。</span><span class="sxs-lookup"><span data-stu-id="b3924-136">Creates resources that are device independent, so they can be reused anywhere.</span></span>                      |
| <span data-ttu-id="b3924-137">**DiscardDeviceIndependentResources**</span><span class="sxs-lookup"><span data-stu-id="b3924-137">**DiscardDeviceIndependentResources**</span></span> | <span data-ttu-id="b3924-138">不再需要與裝置無關的資源時，會加以釋放。</span><span class="sxs-lookup"><span data-stu-id="b3924-138">Releases the device-independent resources after they are no longer needed.</span></span>                          |
| <span data-ttu-id="b3924-139">**CreateDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="b3924-139">**CreateDeviceResources**</span></span>             | <span data-ttu-id="b3924-140">建立與特定裝置系結的資源，例如筆刷和轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="b3924-140">Creates resources, such as brushes and render targets, that are tied to a particular device.</span></span>        |
| <span data-ttu-id="b3924-141">**DiscardDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="b3924-141">**DiscardDeviceResources**</span></span>            | <span data-ttu-id="b3924-142">不再需要裝置相依的資源之後，再加以釋放。</span><span class="sxs-lookup"><span data-stu-id="b3924-142">Releases the device-dependent resources after they are no longer needed.</span></span>                            |
| <span data-ttu-id="b3924-143">**DrawD2DContent**</span><span class="sxs-lookup"><span data-stu-id="b3924-143">**DrawD2DContent**</span></span>                    | <span data-ttu-id="b3924-144">使用 [Direct2D](../direct2d/direct2d-portal.md) 來呈現至螢幕。</span><span class="sxs-lookup"><span data-stu-id="b3924-144">Uses [Direct2D](../direct2d/direct2d-portal.md) to render to the screen.</span></span>                              |
| <span data-ttu-id="b3924-145">**DrawText**</span><span class="sxs-lookup"><span data-stu-id="b3924-145">**DrawText**</span></span>                          | <span data-ttu-id="b3924-146">使用 [Direct2D](../direct2d/direct2d-portal.md)繪製文字字串。</span><span class="sxs-lookup"><span data-stu-id="b3924-146">Draws the text string by using [Direct2D](../direct2d/direct2d-portal.md).</span></span>                            |
| <span data-ttu-id="b3924-147">**OnResize**</span><span class="sxs-lookup"><span data-stu-id="b3924-147">**OnResize**</span></span>                          | <span data-ttu-id="b3924-148">當視窗大小變更時，調整 [Direct2D](../direct2d/direct2d-portal.md) 轉譯目標的大小。</span><span class="sxs-lookup"><span data-stu-id="b3924-148">Resizes the [Direct2D](../direct2d/direct2d-portal.md) render target when the window size is changed.</span></span> |



 

<span data-ttu-id="b3924-149">您可以使用所提供的範例，或使用下列指示，將 [DirectWrite](direct-write-portal.md) 和 [Direct2D](rendering-by-using-direct2d.md) 新增至您自己的 Win32 應用程式。</span><span class="sxs-lookup"><span data-stu-id="b3924-149">You can use the sample provided, or use the instructions that follow to add [DirectWrite](direct-write-portal.md) and [Direct2D](rendering-by-using-direct2d.md) to your own Win32 application.</span></span> <span data-ttu-id="b3924-150">如需範例和相關聯專案檔案的詳細資訊，請參閱 [DirectWriteHelloWorld 範例](/samples/browse/?redirectedfrom=MSDN-samples)。</span><span class="sxs-lookup"><span data-stu-id="b3924-150">For more information about the sample and the associated project files, see the [DirectWriteHelloWorld sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="drawing-simple-text"></a><span data-ttu-id="b3924-151">繪製簡單文字</span><span class="sxs-lookup"><span data-stu-id="b3924-151">Drawing Simple Text</span></span>

<span data-ttu-id="b3924-152">本節說明如何使用 [DirectWrite](direct-write-portal.md) 和 [Direct2D](../direct2d/direct2d-portal.md) 轉譯具有單一格式的簡單文字，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="b3924-152">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render simple text that has a single format, as shown in the following screen shot.</span></span>

!["hello world using directwrite！" 的螢幕擷取畫面](images/simplecropped.png)

<span data-ttu-id="b3924-155">在螢幕上繪製簡單的文字需要四個元件：</span><span class="sxs-lookup"><span data-stu-id="b3924-155">Drawing simple text to the screen requires four components:</span></span>

-   <span data-ttu-id="b3924-156">要呈現的字元字串。</span><span class="sxs-lookup"><span data-stu-id="b3924-156">A character string to render.</span></span>
-   <span data-ttu-id="b3924-157">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)的實例。</span><span class="sxs-lookup"><span data-stu-id="b3924-157">An instance of [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span>
-   <span data-ttu-id="b3924-158">要包含文字的區域維度。</span><span class="sxs-lookup"><span data-stu-id="b3924-158">The dimensions of the area to contain the text.</span></span>
-   <span data-ttu-id="b3924-159">可以呈現文字的物件。</span><span class="sxs-lookup"><span data-stu-id="b3924-159">An object that can render the text.</span></span> <span data-ttu-id="b3924-160">在本教學課程中。</span><span class="sxs-lookup"><span data-stu-id="b3924-160">In this tutorial.</span></span> <span data-ttu-id="b3924-161">您可以使用 [Direct2D](../direct2d/direct2d-portal.md) 轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="b3924-161">you use a [Direct2D](../direct2d/direct2d-portal.md) render target.</span></span>

<span data-ttu-id="b3924-162">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)介面描述用來格式化文字的字型系列名稱、大小、粗細、樣式和延展，並描述地區設定資訊。</span><span class="sxs-lookup"><span data-stu-id="b3924-162">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface describes the font-family name, size, weight, style, and stretch used to format text, and it describes locale information.</span></span> <span data-ttu-id="b3924-163">**IDWriteTextFormat** 也會定義用來設定和取得下列屬性的方法：</span><span class="sxs-lookup"><span data-stu-id="b3924-163">**IDWriteTextFormat** also defines methods for setting and getting the following properties:</span></span>

-   <span data-ttu-id="b3924-164">行距。</span><span class="sxs-lookup"><span data-stu-id="b3924-164">The line spacing.</span></span>
-   <span data-ttu-id="b3924-165">相對於版面配置方塊左邊緣與右邊緣的文字對齊方式。</span><span class="sxs-lookup"><span data-stu-id="b3924-165">The text alignment relative to the left and right edges of the layout box.</span></span>
-   <span data-ttu-id="b3924-166">相對於版面配置方塊頂端和底部的段落對齊。</span><span class="sxs-lookup"><span data-stu-id="b3924-166">The paragraph alignment relative to the top and bottom of the layout box.</span></span>
-   <span data-ttu-id="b3924-167">讀取方向。</span><span class="sxs-lookup"><span data-stu-id="b3924-167">The reading direction.</span></span>
-   <span data-ttu-id="b3924-168">溢出配置方塊之文字的文字修剪細微性。</span><span class="sxs-lookup"><span data-stu-id="b3924-168">The text trimming granularity for text that overflows the layout box.</span></span>
-   <span data-ttu-id="b3924-169">遞增定位停駐點。</span><span class="sxs-lookup"><span data-stu-id="b3924-169">The incremental tab stop.</span></span>
-   <span data-ttu-id="b3924-170">段落流程方向。</span><span class="sxs-lookup"><span data-stu-id="b3924-170">The paragraph flow direction.</span></span>

<span data-ttu-id="b3924-171">使用本檔中所述的兩個程式的文字來繪製文字時，必須要有 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 介面。</span><span class="sxs-lookup"><span data-stu-id="b3924-171">The [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is required for drawing text that uses both of the processes described in this document .</span></span>

<span data-ttu-id="b3924-172">您必須要有 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)實例，才能建立 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)物件或任何其他 [DirectWrite](direct-write-portal.md)物件。</span><span class="sxs-lookup"><span data-stu-id="b3924-172">Before you can create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, or any other [DirectWrite](direct-write-portal.md) object, you need an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) instance.</span></span> <span data-ttu-id="b3924-173">您可以使用 **IDWriteFactory** 來建立 **IDWriteTextFormat** 實例和其他 DirectWrite 物件。</span><span class="sxs-lookup"><span data-stu-id="b3924-173">You use an **IDWriteFactory** to create **IDWriteTextFormat** instances and other DirectWrite objects.</span></span> <span data-ttu-id="b3924-174">若要取得 factory 實例，請使用 [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) 函數。</span><span class="sxs-lookup"><span data-stu-id="b3924-174">To obtain a factory instance, use the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function.</span></span>

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a><span data-ttu-id="b3924-175">第1部分：宣告 DirectWrite 和 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="b3924-175">Part 1: Declare DirectWrite and Direct2D Resources.</span></span>

<span data-ttu-id="b3924-176">在這個部分中，您會宣告稍後將用來建立和顯示文字的物件，做為您類別的私用資料成員。</span><span class="sxs-lookup"><span data-stu-id="b3924-176">In this part, you declare the objects that you will use later for creating and displaying text as private data members of your class.</span></span> <span data-ttu-id="b3924-177">[DirectWrite](direct-write-portal.md)的所有介面、函式和資料類型都是在 *dwrite .h* 標頭檔中宣告，而 [Direct2D](../direct2d/direct2d-portal.md)的所有介面、函數和資料類型都是在 *d2d1* 中宣告;如果您尚未這麼做，請在您的專案中包含這些標頭。</span><span class="sxs-lookup"><span data-stu-id="b3924-177">All of the interfaces, functions, and datatypes for [DirectWrite](direct-write-portal.md) are declared in the *dwrite.h* header file, and those for [Direct2D](../direct2d/direct2d-portal.md) are declared in the *d2d1.h*; if you haven't already done this, include these headers in your project.</span></span>

1.  <span data-ttu-id="b3924-178">在您的類別標頭檔中 (SimpleText) ，將 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) 和 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 介面的指標宣告為私用成員。</span><span class="sxs-lookup"><span data-stu-id="b3924-178">In your class header file (SimpleText.h), declare pointers to [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) and [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interfaces as private members.</span></span>
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  <span data-ttu-id="b3924-179">宣告成員以保存要呈現的文字字串和字串的長度。</span><span class="sxs-lookup"><span data-stu-id="b3924-179">Declare members to hold the text string to render and the length of the string.</span></span>
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  <span data-ttu-id="b3924-180">宣告 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)、 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)和 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 介面的指標，以使用 [Direct2D](../direct2d/direct2d-portal.md)來呈現文字。</span><span class="sxs-lookup"><span data-stu-id="b3924-180">Declare pointers to [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), and [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces for rendering the text with [Direct2D](../direct2d/direct2d-portal.md).</span></span>
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a><span data-ttu-id="b3924-181">第2部分：建立與裝置無關的資源。</span><span class="sxs-lookup"><span data-stu-id="b3924-181">Part 2: Create Device Independent Resources.</span></span>

<span data-ttu-id="b3924-182">[Direct2D](rendering-by-using-direct2d.md) 提供兩種類型的資源：與裝置相關的資源，以及與裝置無關的資源。</span><span class="sxs-lookup"><span data-stu-id="b3924-182">[Direct2D](rendering-by-using-direct2d.md) provides two types of resources: device-dependent resources and device-independent resources.</span></span> <span data-ttu-id="b3924-183">與裝置相關的資源會與轉譯裝置相關聯，且如果移除該裝置，將無法再運作。</span><span class="sxs-lookup"><span data-stu-id="b3924-183">Device-dependent resources are associated with a rendering device and no longer function if that device is removed.</span></span> <span data-ttu-id="b3924-184">另一方面，與裝置無關的資源可以是應用程式範圍的最後一個。</span><span class="sxs-lookup"><span data-stu-id="b3924-184">Device-independent resources, on the other hand, can last for the scope of your application.</span></span>

<span data-ttu-id="b3924-185">[DirectWrite](direct-write-portal.md) 資源與裝置無關。</span><span class="sxs-lookup"><span data-stu-id="b3924-185">[DirectWrite](direct-write-portal.md) resources are device-independent.</span></span>

<span data-ttu-id="b3924-186">在本節中，您會建立應用程式所使用的裝置獨立資源。</span><span class="sxs-lookup"><span data-stu-id="b3924-186">In this section, you create the device-independent resources that are used by your application.</span></span> <span data-ttu-id="b3924-187">這些資源必須透過呼叫介面的 **發行** 方法來釋放。</span><span class="sxs-lookup"><span data-stu-id="b3924-187">These resources must be freed with a call to the **Release** method of the interface.</span></span>

<span data-ttu-id="b3924-188">某些使用的資源必須只建立一次，且不會系結至裝置。</span><span class="sxs-lookup"><span data-stu-id="b3924-188">Some of the resources that are used have to be created only one time and are not tied to a device.</span></span> <span data-ttu-id="b3924-189">這些資源的初始化會放在 *SimpleText：： CreateDeviceIndependentResources* 方法中，此方法會在初始化類別時呼叫。</span><span class="sxs-lookup"><span data-stu-id="b3924-189">The initialization for these resources is put in the *SimpleText::CreateDeviceIndependentResources* method, which is called when initializing the class.</span></span>

1.  <span data-ttu-id="b3924-190">在類別實 (中的 *SimpleText：： CreateDeviceIndependentResources* 方法內，在 SimpleText .cpp) 中，呼叫 [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) 函式來建立 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) 介面，這是所有 [Direct2D](../direct2d/direct2d-portal.md) 物件的根 factory 介面。</span><span class="sxs-lookup"><span data-stu-id="b3924-190">Inside the *SimpleText::CreateDeviceIndependentResources* method in the class implementation file (SimpleText.cpp), call the [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) function to create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface, which is the root factory interface for all [Direct2D](../direct2d/direct2d-portal.md) objects.</span></span> <span data-ttu-id="b3924-191">您可以使用相同的 factory 來具現化其他 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="b3924-191">You use the same factory to instantiate other Direct2D resources.</span></span>
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  <span data-ttu-id="b3924-192">呼叫 [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) 函式來建立 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) 介面，這是所有 [DirectWrite](direct-write-portal.md) 物件的根 factory 介面。</span><span class="sxs-lookup"><span data-stu-id="b3924-192">Call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function to create an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface, which is the root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span> <span data-ttu-id="b3924-193">您可以使用相同的 factory 來具現化其他 DirectWrite 資源。</span><span class="sxs-lookup"><span data-stu-id="b3924-193">You use the same factory to instantiate other DirectWrite resources.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  <span data-ttu-id="b3924-194">初始化文字字串並儲存其長度。</span><span class="sxs-lookup"><span data-stu-id="b3924-194">Initialize the text string and store its length.</span></span>

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  <span data-ttu-id="b3924-195">使用 [**IDWriteFactory：： CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat)方法建立 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)介面物件。</span><span class="sxs-lookup"><span data-stu-id="b3924-195">Create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface object by using the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method.</span></span> <span data-ttu-id="b3924-196">**IDWriteTextFormat** 指定將用來轉譯文字字串的字型、粗細、延展、樣式和地區設定。</span><span class="sxs-lookup"><span data-stu-id="b3924-196">The **IDWriteTextFormat** specifies the font, weight, stretch, style, and locale that will be used to render the text string.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  <span data-ttu-id="b3924-197">藉由呼叫 [**IDWriteTextFormat：： SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) 和 [**IDWriteTextFormat：： SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) 方法，以水準和垂直方式將文字置中。</span><span class="sxs-lookup"><span data-stu-id="b3924-197">Center the text horizontally and vertically by calling the [**IDWriteTextFormat::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) and [**IDWriteTextFormat::SetParagraphAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) methods.</span></span>
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

<span data-ttu-id="b3924-198">在此部分中，您已將應用程式所使用的裝置獨立資源初始化。</span><span class="sxs-lookup"><span data-stu-id="b3924-198">In this part, you initialized the device-independent resources that are used by your application.</span></span> <span data-ttu-id="b3924-199">在下一個部分中，您會初始化裝置相依的資源。</span><span class="sxs-lookup"><span data-stu-id="b3924-199">In the next part, you initialize the device-dependent resources.</span></span>

### <a name="part-3-create-device-dependent-resources"></a><span data-ttu-id="b3924-200">第3部分：建立 Device-Dependent 資源。</span><span class="sxs-lookup"><span data-stu-id="b3924-200">Part 3: Create Device-Dependent Resources.</span></span>

<span data-ttu-id="b3924-201">在此部分中，您會建立 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 和 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 來呈現您的文字。</span><span class="sxs-lookup"><span data-stu-id="b3924-201">In this part, you create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) for rendering your text.</span></span>

<span data-ttu-id="b3924-202">轉譯目標是一種 Direct2D 物件，它會建立繪圖資源，並將繪製命令轉譯成轉譯裝置。</span><span class="sxs-lookup"><span data-stu-id="b3924-202">A render target is a Direct2D object that creates drawing resources and renders drawing commands to a rendering device.</span></span> <span data-ttu-id="b3924-203">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)是呈現至 **HWND** 的轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="b3924-203">An [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) is a render target that renders to an **HWND**.</span></span>

<span data-ttu-id="b3924-204">轉譯目標可以建立的繪圖資源之一，是繪製大綱、填滿和文字的筆刷。</span><span class="sxs-lookup"><span data-stu-id="b3924-204">One of the drawing resources that a render target can create is a brush for painting outlines, fills, and text.</span></span> <span data-ttu-id="b3924-205">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)會以純色繪製。</span><span class="sxs-lookup"><span data-stu-id="b3924-205">An [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints with a solid color.</span></span>

<span data-ttu-id="b3924-206">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)和 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)介面都是在建立時系結至轉譯裝置，而且必須在裝置變成無效時予以釋放和重新建立。</span><span class="sxs-lookup"><span data-stu-id="b3924-206">Both the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) and the [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interfaces are bound to a rendering device when they are created and must be released and recreated if the device becomes invalid.</span></span>

1.  <span data-ttu-id="b3924-207">在 SimpleText：： CreateDeviceResources 方法中，檢查呈現目標指標是否為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b3924-207">Inside the SimpleText::CreateDeviceResources method, check whether the render target pointer is **NULL**.</span></span> <span data-ttu-id="b3924-208">如果是，請取出轉譯區域的大小，然後建立該大小的 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 。</span><span class="sxs-lookup"><span data-stu-id="b3924-208">If it is, retrieve the size of the render area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of that size.</span></span> <span data-ttu-id="b3924-209">使用 **ID2D1HwndRenderTarget** 來建立 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)。</span><span class="sxs-lookup"><span data-stu-id="b3924-209">Use the **ID2D1HwndRenderTarget** to create an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  <span data-ttu-id="b3924-210">在 SimpleText：:D iscardDeviceResources 方法中，釋放筆刷和轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="b3924-210">In the SimpleText::DiscardDeviceResources method, release both the brush and render target.</span></span>
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

<span data-ttu-id="b3924-211">現在您已建立轉譯目標和筆刷，接下來您可以使用它們來呈現文字。</span><span class="sxs-lookup"><span data-stu-id="b3924-211">Now that you have created a render target and a brush, you can use them to render your text.</span></span>

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a><span data-ttu-id="b3924-212">第4部分：使用 Direct2D DrawText 方法繪製文字。</span><span class="sxs-lookup"><span data-stu-id="b3924-212">Part 4: Draw Text By Using the Direct2D DrawText Method.</span></span>

1.  <span data-ttu-id="b3924-213">在您類別的 SimpleText：:D rawText 方法中，藉由取出轉譯區域的維度來定義文字版面配置的區域，並建立具有相同維度的 [Direct2D](../direct2d/direct2d-portal.md) 矩形。</span><span class="sxs-lookup"><span data-stu-id="b3924-213">In the SimpleText::DrawText method of your class, define the area for the text layout by retrieving the dimensions of the rendering area, and create a [Direct2D](../direct2d/direct2d-portal.md) rectangle that has the same dimensions.</span></span>
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  <span data-ttu-id="b3924-214">使用 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法和 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 物件將文字轉譯至螢幕。</span><span class="sxs-lookup"><span data-stu-id="b3924-214">Use the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method and the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object to render text to the screen.</span></span> <span data-ttu-id="b3924-215">**ID2D1RenderTarget：:D rawtext** 方法會採用下列參數：</span><span class="sxs-lookup"><span data-stu-id="b3924-215">The **ID2D1RenderTarget::DrawText** method takes the following parameters:</span></span>
    -   <span data-ttu-id="b3924-216">要轉譯的字串。</span><span class="sxs-lookup"><span data-stu-id="b3924-216">A string to render.</span></span>
    -   <span data-ttu-id="b3924-217">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b3924-217">A pointer to an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface.</span></span>
    -   <span data-ttu-id="b3924-218">[Direct2D](../direct2d/direct2d-portal.md)版面配置矩形。</span><span class="sxs-lookup"><span data-stu-id="b3924-218">A [Direct2D](../direct2d/direct2d-portal.md) layout rectangle.</span></span>
    -   <span data-ttu-id="b3924-219">公開 [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)之介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b3924-219">A pointer to an interface that exposes [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).</span></span>

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a><span data-ttu-id="b3924-220">第5部分：使用 Direct2D 轉譯視窗內容</span><span class="sxs-lookup"><span data-stu-id="b3924-220">Part 5: Render the Window Contents Using Direct2D</span></span>

<span data-ttu-id="b3924-221">若要在收到繪製訊息時使用 [Direct2D](../direct2d/direct2d-portal.md) 來呈現視窗的內容，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="b3924-221">To render the contents of the window by using [Direct2D](../direct2d/direct2d-portal.md) when a paint message is received, do the following:</span></span>

1.  <span data-ttu-id="b3924-222">藉由呼叫第3部分中所實行的 SimpleText：： CreateDeviceResources 方法，來建立裝置相依的資源。</span><span class="sxs-lookup"><span data-stu-id="b3924-222">Create the device dependent resources by calling the SimpleText::CreateDeviceResources method implemented in Part 3.</span></span>
2.  <span data-ttu-id="b3924-223">呼叫呈現目標的 [**ID2D1HwndRenderTarget：： BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法。</span><span class="sxs-lookup"><span data-stu-id="b3924-223">Call the [**ID2D1HwndRenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method of the render target.</span></span>
3.  <span data-ttu-id="b3924-224">藉由呼叫 [**ID2D1HwndRenderTarget：： clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) 方法來清除呈現目標。</span><span class="sxs-lookup"><span data-stu-id="b3924-224">Clear the render target by calling the [**ID2D1HwndRenderTarget::Clear**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) method.</span></span>
4.  <span data-ttu-id="b3924-225">呼叫 SimpleText：:D rawText 方法，在第4部分中執行。</span><span class="sxs-lookup"><span data-stu-id="b3924-225">Call the SimpleText::DrawText method, implemented in Part 4.</span></span>
5.  <span data-ttu-id="b3924-226">呼叫呈現目標的 [**ID2D1HwndRenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。</span><span class="sxs-lookup"><span data-stu-id="b3924-226">Call the [**ID2D1HwndRenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method of the render target.</span></span>
6.  <span data-ttu-id="b3924-227">如有必要，請捨棄裝置相依的資源，讓它們可以在重繪視窗時重新建立。</span><span class="sxs-lookup"><span data-stu-id="b3924-227">If it is necessary, discard the device-dependent resources so that they can be recreated when the window is redrawn.</span></span>


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



<span data-ttu-id="b3924-228">SimpleText 類別是在 SimpleText 和 SimpleText 中執行。</span><span class="sxs-lookup"><span data-stu-id="b3924-228">The SimpleText class is implemented in SimpleText.h and SimpleText.cpp.</span></span>

## <a name="drawing-text-with-multiple-formats"></a><span data-ttu-id="b3924-229">繪製具有多種格式的文字。</span><span class="sxs-lookup"><span data-stu-id="b3924-229">Drawing Text with Multiple Formats.</span></span>

<span data-ttu-id="b3924-230">本節說明如何使用 [DirectWrite](direct-write-portal.md) 和 [Direct2D](../direct2d/direct2d-portal.md) 轉譯具有多種格式的文字，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="b3924-230">This section shows how to use [DirectWrite](direct-write-portal.md) and [Direct2D](../direct2d/direct2d-portal.md) to render text with multiple formats, as shown in the following screen shot.</span></span>

!["hello world using directwrite！" 的螢幕擷取畫面，其中有一些不同樣式、大小和格式的部分](images/multiformattedcropped.png)

<span data-ttu-id="b3924-232">本節的程式碼會實作為 [DWriteHelloWorld 範例](/samples/browse/?redirectedfrom=MSDN-samples)中的 MultiformattedText 類別。</span><span class="sxs-lookup"><span data-stu-id="b3924-232">The code for this section is implemented as the MultiformattedText class in the [DWriteHelloWorld Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span> <span data-ttu-id="b3924-233">它是根據上一節中的步驟。</span><span class="sxs-lookup"><span data-stu-id="b3924-233">It is based on the steps from the previous section.</span></span>

<span data-ttu-id="b3924-234">若要建立多格式的文字，您可以使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面，以及上一節所介紹的 [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) 介面。</span><span class="sxs-lookup"><span data-stu-id="b3924-234">To create multi-formatted text, you use the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface in addition to the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface introduced in the previous section.</span></span> <span data-ttu-id="b3924-235">**IDWriteTextLayout** 介面會描述文字區塊的格式設定和版面配置。</span><span class="sxs-lookup"><span data-stu-id="b3924-235">The **IDWriteTextLayout** interface describes the formatting and layout of a block of text.</span></span> <span data-ttu-id="b3924-236">除了 **IDWriteTextFormat** 物件所指定的預設格式之外，也可以使用 **IDWriteTextLayout** 來變更特定範圍的文字格式。</span><span class="sxs-lookup"><span data-stu-id="b3924-236">In addition to default formatting specified by an **IDWriteTextFormat** object, the formatting for specific ranges of text can be changed by using **IDWriteTextLayout**.</span></span> <span data-ttu-id="b3924-237">這包括字型系列名稱、大小、粗細、樣式、延展、刪除線和底線。</span><span class="sxs-lookup"><span data-stu-id="b3924-237">This includes font family name, size, weight, style, stretch, strikethrough, and underlining.</span></span>

<span data-ttu-id="b3924-238">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 也提供點擊測試方法。</span><span class="sxs-lookup"><span data-stu-id="b3924-238">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) also provides hit-testing methods.</span></span> <span data-ttu-id="b3924-239">這些方法所傳回的點擊測試度量，會相對於使用 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)介面的 [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)方法建立 **IDWriteTextLayout** 介面物件時所指定的版面配置方塊。</span><span class="sxs-lookup"><span data-stu-id="b3924-239">The hit-testing metrics returned by these methods are relative to the layout box specified when the **IDWriteTextLayout** interface object is created by using the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="b3924-240">[**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography)介面是用來將選擇性的 [OpenType](../intl/opentype-font-format.md)印刷樣式功能新增至文字配置，例如花飾字和替代的樣式文字集。</span><span class="sxs-lookup"><span data-stu-id="b3924-240">The [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface is used to add optional [OpenType](../intl/opentype-font-format.md) typographic features to a text layout, such as swashes and alternative stylistic text sets.</span></span> <span data-ttu-id="b3924-241">您可以藉由呼叫 **IDWriteTypography** 介面的 [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature)方法，將印刷樣式功能加入至文字配置內的特定文字範圍。</span><span class="sxs-lookup"><span data-stu-id="b3924-241">Typographic features can be added to a specific range of text within a text layout by calling the [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method of the **IDWriteTypography** interface.</span></span> <span data-ttu-id="b3924-242">這個方法會接收 [**DWRITE \_ 字型 \_ 功能**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) 結構作為參數，其中包含 **DWRITE \_ 字型 \_ 功能 \_ 標記** 列舉常數和 **UINT32** 執行參數。</span><span class="sxs-lookup"><span data-stu-id="b3924-242">This method receives a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) structure as a parameter that contains a **DWRITE\_FONT\_FEATURE\_TAG** enumeration constant and a **UINT32** execution parameter.</span></span> <span data-ttu-id="b3924-243">您可以在 microsoft.com 上的 [Opentype 版面配置標記](https://www.microsoft.com/typography/otspec/features_ae.htm) 登錄中找到已註冊的 opentype 功能清單。</span><span class="sxs-lookup"><span data-stu-id="b3924-243">A list of registered OpenType features can be found at the [OpenType Layout Tag Registry](https://www.microsoft.com/typography/otspec/features_ae.htm) on microsoft.com.</span></span> <span data-ttu-id="b3924-244">如需對等的 DirectWrite 列舉常數，請參閱 **DWRITE \_ 字型 \_ 功能 \_ 標記**。</span><span class="sxs-lookup"><span data-stu-id="b3924-244">For the equivalent DirectWrite enumeration constants, see **DWRITE\_FONT\_FEATURE\_TAG**.</span></span>

### <a name="part-1-create-an-idwritetextlayout-interface"></a><span data-ttu-id="b3924-245">第1部分：建立 IDWriteTextLayout 介面。</span><span class="sxs-lookup"><span data-stu-id="b3924-245">Part 1: Create an IDWriteTextLayout Interface.</span></span>

1.  <span data-ttu-id="b3924-246">宣告 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面的指標，作為 MultiformattedText 類別的成員。</span><span class="sxs-lookup"><span data-stu-id="b3924-246">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the MultiformattedText class.</span></span>
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  <span data-ttu-id="b3924-247">在 MultiformattedText：： CreateDeviceIndependentResources 方法的結尾，藉由呼叫 [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)方法來建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面物件。</span><span class="sxs-lookup"><span data-stu-id="b3924-247">At the end of the MultiformattedText::CreateDeviceIndependentResources method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span> <span data-ttu-id="b3924-248">**IDWriteTextLayout** 介面提供額外的格式設定功能，例如將不同格式套用至選取的文字部分的能力。</span><span class="sxs-lookup"><span data-stu-id="b3924-248">The **IDWriteTextLayout** interface provides additional formatting features, such as the ability to apply different formats to selected portions of text.</span></span>
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

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a><span data-ttu-id="b3924-249">第2部分：使用 IDWriteTextLayout 套用格式。</span><span class="sxs-lookup"><span data-stu-id="b3924-249">Part 2: Applying Formatting with IDWriteTextLayout.</span></span>

<span data-ttu-id="b3924-250">您可以使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面，將格式化（例如字型大小、粗細和底線）套用至要顯示之文字的子字串。</span><span class="sxs-lookup"><span data-stu-id="b3924-250">Formatting, such as the font size, weight, and underlining, can be applied to substrings of the text to be displayed by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

1.  <span data-ttu-id="b3924-251">藉由宣告 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) 和呼叫 [**IDWriteTextLayout：： SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) 方法，將 "DirectWrite" 的子字串 "Di" 設定為100的字型大小。</span><span class="sxs-lookup"><span data-stu-id="b3924-251">Set the font size for the substring "Di" of "DirectWrite" to 100 by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) and calling the [**IDWriteTextLayout::SetFontSize**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize) method.</span></span>
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  <span data-ttu-id="b3924-252">藉由呼叫 [**IDWriteTextLayout：： SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) 方法，對子字串 "DirectWrite" 加上底線。</span><span class="sxs-lookup"><span data-stu-id="b3924-252">Underline the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  <span data-ttu-id="b3924-253">藉由呼叫 [**IDWriteTextLayout：： SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) 方法，將子字串 "DirectWrite" 的字型粗細設定為粗體。</span><span class="sxs-lookup"><span data-stu-id="b3924-253">Set the font weight to bold for the substring "DirectWrite" by calling the [**IDWriteTextLayout::SetFontWeight**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight) method.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a><span data-ttu-id="b3924-254">第3部分：使用 IDWriteTypography 新增印刷樣式功能。</span><span class="sxs-lookup"><span data-stu-id="b3924-254">Part 3: Adding Typographic Features with IDWriteTypography.</span></span>

1.  <span data-ttu-id="b3924-255">藉由呼叫 [**IDWriteFactory：： CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography)方法，宣告並建立 [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography)介面物件。</span><span class="sxs-lookup"><span data-stu-id="b3924-255">Declare and create an [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) interface object by calling the [**IDWriteFactory::CreateTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography) method.</span></span>
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  <span data-ttu-id="b3924-256">藉由宣告已指定樣式設定7的 [**DWRITE \_ 字型 \_ 功能**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) 物件，並呼叫 [**IDWriteTypography：： AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) 方法，來加入字型功能。</span><span class="sxs-lookup"><span data-stu-id="b3924-256">Add a font feature by declaring a [**DWRITE\_FONT\_FEATURE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) object that has the stylistic set 7 specified and calling the [**IDWriteTypography::AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) method.</span></span>
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  <span data-ttu-id="b3924-257">藉由宣告 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) 變數，並呼叫 [**IDWriteTextLayout：： SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) 方法並傳入文字範圍，設定文字配置以使用整個字串的印刷樣式。</span><span class="sxs-lookup"><span data-stu-id="b3924-257">Set the text layout to use the typography over the whole string by declaring a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable and calling the [**IDWriteTextLayout::SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) method and passing in the text range.</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  <span data-ttu-id="b3924-258">在 MultiformattedText：： OnResize 方法中設定 text layout 物件的新寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="b3924-258">Set the new width and height for the text layout object in the MultiformattedText::OnResize method.</span></span>
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a><span data-ttu-id="b3924-259">第4部分：使用 Direct2D DrawTextLayout 方法繪製文字。</span><span class="sxs-lookup"><span data-stu-id="b3924-259">Part 4: Draw Text Using the Direct2D DrawTextLayout Method.</span></span>

<span data-ttu-id="b3924-260">若要使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件所指定的文字版面配置設定來繪製文字，請將 MultiformattedText：:D rawtext 方法中的程式碼變更為使用 [**IDWriteTextLayout：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)。</span><span class="sxs-lookup"><span data-stu-id="b3924-260">To draw the text with the text layout settings specified by the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, change the code in the MultiformattedText::DrawText method to use [**IDWriteTextLayout::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).</span></span>

1.  <span data-ttu-id="b3924-261">Delcare [**D2D1 \_ 點的 \_ 2f**](../direct2d/d2d1-point-2f.md) 變數，並將它設定為視窗的左上角。</span><span class="sxs-lookup"><span data-stu-id="b3924-261">Delcare a [**D2D1\_POINT\_2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.</span></span>
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  <span data-ttu-id="b3924-262">藉由呼叫 [Direct2D](../direct2d/direct2d-portal.md)轉譯目標的 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)方法並傳遞 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)指標，將文字繪製到螢幕。</span><span class="sxs-lookup"><span data-stu-id="b3924-262">Draw the text to the screen by calling the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method of the [Direct2D](../direct2d/direct2d-portal.md) render target and passing the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) pointer.</span></span>
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

<span data-ttu-id="b3924-263">MultiformattedText 類別是在 MultiformattedText 和 MultiformattedText 中執行。</span><span class="sxs-lookup"><span data-stu-id="b3924-263">The MultiformattedText class is implemented in MultiformattedText.h and MultiformattedText.cpp.</span></span>

 

 