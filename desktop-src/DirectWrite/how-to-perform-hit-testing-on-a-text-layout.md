---
title: 如何針對文字版面配置執行點擊測試
description: 提供簡短的教學課程，說明如何將點擊測試新增至 DirectWrite 應用程式，以使用 IDWriteTextLayout 介面來顯示文字。
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ca80ac641920c4e63c08f4cbb0fd9e24eb7b2d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103945730"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a><span data-ttu-id="1db4f-103">如何針對文字版面配置執行點擊測試</span><span class="sxs-lookup"><span data-stu-id="1db4f-103">How to Perform Hit Testing on a Text Layout</span></span>

<span data-ttu-id="1db4f-104">提供簡短的教學課程，說明如何將點擊測試新增至 [DirectWrite](direct-write-portal.md) 應用程式，以使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面來顯示文字。</span><span class="sxs-lookup"><span data-stu-id="1db4f-104">Provides a short tutorial about how to add hit testing to a [DirectWrite](direct-write-portal.md) application that displays text by using the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface.</span></span>

<span data-ttu-id="1db4f-105">本教學課程的結果是應用程式，會將滑鼠左鍵按下滑鼠左鍵的字元，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="1db4f-105">The result of this tutorial is an application that underlines the character that is clicked on by the left mouse button, as shown in the following screen shot.</span></span>

![[按一下此文字] 的螢幕擷取畫面](images/hittest.png)

<span data-ttu-id="1db4f-107">此如何包含下列元件：</span><span class="sxs-lookup"><span data-stu-id="1db4f-107">This how to contains the following parts:</span></span>

- [<span data-ttu-id="1db4f-108">步驟1：建立文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="1db4f-108">Step 1: Create a Text Layout.</span></span>](#step-1-create-a-text-layout)
- [<span data-ttu-id="1db4f-109">步驟2：加入 OnClick 方法。</span><span class="sxs-lookup"><span data-stu-id="1db4f-109">Step 2: Add an OnClick method.</span></span>](#step-2-add-an-onclick-method)
- [<span data-ttu-id="1db4f-110">步驟3：執行點擊測試。</span><span class="sxs-lookup"><span data-stu-id="1db4f-110">Step 3: Perform Hit Testing.</span></span>](#step-3-perform-hit-testing)
- [<span data-ttu-id="1db4f-111">步驟4：將按一下的文字加上底線。</span><span class="sxs-lookup"><span data-stu-id="1db4f-111">Step 4: Underline the Clicked Text.</span></span>](#step-4-underline-the-clicked-text)
- [<span data-ttu-id="1db4f-112">步驟5：處理 WM \_ LBUTTONDOWN 訊息。</span><span class="sxs-lookup"><span data-stu-id="1db4f-112">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>](/windows)

## <a name="step-1-create-a-text-layout"></a><span data-ttu-id="1db4f-113">步驟1：建立文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="1db4f-113">Step 1: Create a Text Layout.</span></span>

<span data-ttu-id="1db4f-114">若要開始，您將需要使用 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 物件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1db4f-114">To begin, you will need an application that uses an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span> <span data-ttu-id="1db4f-115">如果您已經有一個顯示文字版面配置的應用程式，請移至步驟2。</span><span class="sxs-lookup"><span data-stu-id="1db4f-115">If you already have an application that displays text with a text layout, go to Step 2.</span></span>

<span data-ttu-id="1db4f-116">若要加入文字版面配置，您必須執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="1db4f-116">To add a text layout you must do the following:</span></span>

1. <span data-ttu-id="1db4f-117">宣告 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) 介面的指標做為類別的成員。</span><span class="sxs-lookup"><span data-stu-id="1db4f-117">Declare a pointer to an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface as a member of the class.</span></span>

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. <span data-ttu-id="1db4f-118">在 **CreateDeviceIndependentResources** 方法的結尾，藉由呼叫 [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)方法來建立 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)介面物件。</span><span class="sxs-lookup"><span data-stu-id="1db4f-118">At the end of the **CreateDeviceIndependentResources** method, create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface object by calling the [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) method.</span></span>

    ```cpp
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

3. <span data-ttu-id="1db4f-119">然後，您必須將 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法的呼叫變更為 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) ，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="1db4f-119">Then, you must change the call to the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) method to [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) as shown in the following code.</span></span>

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a><span data-ttu-id="1db4f-120">步驟2：加入 OnClick 方法。</span><span class="sxs-lookup"><span data-stu-id="1db4f-120">Step 2: Add an OnClick method.</span></span>

<span data-ttu-id="1db4f-121">現在將方法加入至將使用文字版面配置之點擊測試功能的類別。</span><span class="sxs-lookup"><span data-stu-id="1db4f-121">Now add a method to the class that will use the hit testing functionality of the text layout.</span></span>

1. <span data-ttu-id="1db4f-122">在類別標頭檔中宣告 **OnClick** 方法。</span><span class="sxs-lookup"><span data-stu-id="1db4f-122">Declare an **OnClick** method in the class header file.</span></span>

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. <span data-ttu-id="1db4f-123">在類別實檔案中定義 **OnClick** 方法。</span><span class="sxs-lookup"><span data-stu-id="1db4f-123">Define an **OnClick** method in the class implementation file.</span></span>

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a><span data-ttu-id="1db4f-124">步驟3：執行點擊測試。</span><span class="sxs-lookup"><span data-stu-id="1db4f-124">Step 3: Perform Hit Testing.</span></span>

<span data-ttu-id="1db4f-125">為了判斷使用者按一下文字版面配置的位置，我們將使用 [**IDWriteTextLayout：： HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) 方法。</span><span class="sxs-lookup"><span data-stu-id="1db4f-125">To determine where the user has clicked the text layout we will use the [**IDWriteTextLayout::HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

<span data-ttu-id="1db4f-126">將下列程式新增至您在步驟2中定義的 **OnClick** 方法。</span><span class="sxs-lookup"><span data-stu-id="1db4f-126">Add the following to the **OnClick** method that you defined in Step 2.</span></span>

1. <span data-ttu-id="1db4f-127">宣告將作為參數傳遞給方法的變數。</span><span class="sxs-lookup"><span data-stu-id="1db4f-127">Declare the variables we will pass as parameters to the method.</span></span>

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    <span data-ttu-id="1db4f-128">[**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)方法會輸出下列參數。</span><span class="sxs-lookup"><span data-stu-id="1db4f-128">The [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method outputs the following parameters.</span></span>

    | <span data-ttu-id="1db4f-129">變數</span><span class="sxs-lookup"><span data-stu-id="1db4f-129">Variable</span></span>         | <span data-ttu-id="1db4f-130">描述</span><span class="sxs-lookup"><span data-stu-id="1db4f-130">Description</span></span>                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="1db4f-131">*hitTestMetrics*</span><span class="sxs-lookup"><span data-stu-id="1db4f-131">*hitTestMetrics*</span></span> | <span data-ttu-id="1db4f-132">完全封閉點擊測試位置的幾何。</span><span class="sxs-lookup"><span data-stu-id="1db4f-132">The geometry fully enclosing the hit-test location.</span></span>                                                                                     |
    | <span data-ttu-id="1db4f-133">*isInside*</span><span class="sxs-lookup"><span data-stu-id="1db4f-133">*isInside*</span></span>       | <span data-ttu-id="1db4f-134">指出點擊測試位置是否在文字字串內。</span><span class="sxs-lookup"><span data-stu-id="1db4f-134">Indicates whether the hit-test location is inside the text string or not.</span></span> <span data-ttu-id="1db4f-135">若為 FALSE，則會傳回最接近文字邊緣的位置。</span><span class="sxs-lookup"><span data-stu-id="1db4f-135">When FALSE, the position nearest the text's edge is returned.</span></span> |
    | <span data-ttu-id="1db4f-136">*isTrailingHit*</span><span class="sxs-lookup"><span data-stu-id="1db4f-136">*isTrailingHit*</span></span>  | <span data-ttu-id="1db4f-137">指出點擊測試位置是否在字元的開頭或尾端。</span><span class="sxs-lookup"><span data-stu-id="1db4f-137">Indicates whether the hit-test location is at the leading or the trailing side of the character.</span></span>                                        |

2. <span data-ttu-id="1db4f-138">呼叫 [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)物件的 [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)方法。</span><span class="sxs-lookup"><span data-stu-id="1db4f-138">Call the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method of the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    <span data-ttu-id="1db4f-139">此範例中的程式碼會傳遞位置的 *x* 和 *y* 變數，而不需要修改。</span><span class="sxs-lookup"><span data-stu-id="1db4f-139">The code in this example passes the *x* and *y* variables for the position without any modification.</span></span> <span data-ttu-id="1db4f-140">這可在此範例中完成，因為文字配置的大小與視窗的大小相同，而且源自視窗的左上角。</span><span class="sxs-lookup"><span data-stu-id="1db4f-140">This can be done in this example because the text layout is the same size as the window and originates in the upper-left corner of the window.</span></span> <span data-ttu-id="1db4f-141">如果不是這種情況，您必須決定相對於文字版面配置來源的座標。</span><span class="sxs-lookup"><span data-stu-id="1db4f-141">If this was not the case, you would have to determine the coordinates in relation to the origin of the text layout.</span></span>

## <a name="step-4-underline-the-clicked-text"></a><span data-ttu-id="1db4f-142">步驟4：將按一下的文字加上底線。</span><span class="sxs-lookup"><span data-stu-id="1db4f-142">Step 4: Underline the Clicked Text.</span></span>

<span data-ttu-id="1db4f-143">在呼叫 [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)方法之後，將下列步驟新增至您在步驟2中定義的 **OnClick** 。</span><span class="sxs-lookup"><span data-stu-id="1db4f-143">Add the following to the **OnClick** you defined in Step 2, after the call to the [**HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) method.</span></span>

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

<span data-ttu-id="1db4f-144">此程式碼會執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="1db4f-144">This code does the following.</span></span>

1. <span data-ttu-id="1db4f-145">使用 *isInside* 變數檢查點擊測試點是否在文字內。</span><span class="sxs-lookup"><span data-stu-id="1db4f-145">Checks if the hit-test point was inside the text using the *isInside* variable.</span></span>
2. <span data-ttu-id="1db4f-146">*HitTestMetrics* 結構的 **textPosition** 成員包含所按下之字元的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="1db4f-146">The **textPosition** member of the *hitTestMetrics* structure contains the zero-based index of the character clicked.</span></span>

    <span data-ttu-id="1db4f-147">藉由將此值傳遞給 [**IDWriteTextLayout：： GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) 方法，取得此字元的底線。</span><span class="sxs-lookup"><span data-stu-id="1db4f-147">Gets the underline for this character by passing this value to the [**IDWriteTextLayout::GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) method.</span></span>

3. <span data-ttu-id="1db4f-148">宣告 [**DWRITE \_ 文字 \_ 範圍**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) 變數，其起始位置設定為 **hitTestMetrics. textPosition** 且長度為1。</span><span class="sxs-lookup"><span data-stu-id="1db4f-148">Declares a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) variable with the start position set to **hitTestMetrics.textPosition** and a length of 1.</span></span>
4. <span data-ttu-id="1db4f-149">使用 [**IDWriteTextLayout：： SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) 方法切換底線。</span><span class="sxs-lookup"><span data-stu-id="1db4f-149">Toggles the underline by using the [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline) method.</span></span>

<span data-ttu-id="1db4f-150">設定底線之後，請呼叫類別的 **DrawD2DContent** 方法來重繪文字。</span><span class="sxs-lookup"><span data-stu-id="1db4f-150">After setting the underline, redraw the text by calling the **DrawD2DContent** method of the class.</span></span>

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a><span data-ttu-id="1db4f-151">步驟5：處理 WM \_ LBUTTONDOWN 訊息。</span><span class="sxs-lookup"><span data-stu-id="1db4f-151">Step 5: Handle the WM\_LBUTTONDOWN message.</span></span>

<span data-ttu-id="1db4f-152">最後，將 **WM \_ LBUTTONDOWN** 訊息新增至您應用程式的訊息處理常式，並呼叫類別的 **OnClick** 方法。</span><span class="sxs-lookup"><span data-stu-id="1db4f-152">Finally, add the **WM\_LBUTTONDOWN** message to the message handler for your application and call the **OnClick** method of the class.</span></span>

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

<span data-ttu-id="1db4f-153">**取得 \_X \_ LPARAM** 和 **GET \_ x \_ LPARAM** 宏是在 windowsx .h 標頭檔中宣告的。</span><span class="sxs-lookup"><span data-stu-id="1db4f-153">**GET\_X\_LPARAM** and **GET\_X\_LPARAM** macros are declared in the windowsx.h header file.</span></span> <span data-ttu-id="1db4f-154">他們可以輕鬆地取出滑鼠點擊的 x 和 y 位置。</span><span class="sxs-lookup"><span data-stu-id="1db4f-154">They easily retrieve the x and y position of the mouse click.</span></span>
