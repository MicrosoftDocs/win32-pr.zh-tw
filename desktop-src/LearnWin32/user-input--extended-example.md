---
title: 使用者輸入擴充範例
description: .
ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdde7f14dda356d0f65103c77e3b73c2f0de50a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104568540"
---
# <a name="user-input-extended-example"></a><span data-ttu-id="33346-103">使用者輸入：擴充的範例</span><span class="sxs-lookup"><span data-stu-id="33346-103">User Input: Extended Example</span></span>

<span data-ttu-id="33346-104">讓我們結合已瞭解的使用者輸入內容，以建立簡單的繪圖程式。</span><span class="sxs-lookup"><span data-stu-id="33346-104">Let's combine everything that we have learned about user input to create a simple drawing program.</span></span> <span data-ttu-id="33346-105">以下是程式的螢幕擷取畫面：</span><span class="sxs-lookup"><span data-stu-id="33346-105">Here is a screen shot of the program:</span></span>

![繪圖程式的螢幕擷取畫面](images/input03.png)

<span data-ttu-id="33346-107">使用者可以使用數種不同的色彩來繪製省略號，然後選取、移動或刪除省略號。</span><span class="sxs-lookup"><span data-stu-id="33346-107">The user can draw ellipses in several different colors, and select, move, or delete ellipses.</span></span> <span data-ttu-id="33346-108">為了讓 UI 保持簡單，程式不會讓使用者選取橢圓形色彩。</span><span class="sxs-lookup"><span data-stu-id="33346-108">To keep the UI simple, the program does not let the user select the ellipse colors.</span></span> <span data-ttu-id="33346-109">相反地，程式會自動迴圈顯示預先定義的色彩清單。</span><span class="sxs-lookup"><span data-stu-id="33346-109">Instead, the program automatically cycles through a predefined list of colors.</span></span> <span data-ttu-id="33346-110">程式不支援省略號以外的任何圖形。</span><span class="sxs-lookup"><span data-stu-id="33346-110">The program does not support any shapes other than ellipses.</span></span> <span data-ttu-id="33346-111">很明顯地，此計畫不會贏得任何對圖形軟體的獎勵。</span><span class="sxs-lookup"><span data-stu-id="33346-111">Obviously, this program will not win any awards for graphics software.</span></span> <span data-ttu-id="33346-112">不過，它仍然是從中學習的實用範例。</span><span class="sxs-lookup"><span data-stu-id="33346-112">However, it is still a useful example to learn from.</span></span> <span data-ttu-id="33346-113">您可以從 [簡單的繪圖範例](simple-drawing-sample.md)下載完整的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="33346-113">You can download the complete source code from [Simple Drawing Sample](simple-drawing-sample.md).</span></span> <span data-ttu-id="33346-114">本節只會討論一些重點。</span><span class="sxs-lookup"><span data-stu-id="33346-114">This section will just cover some highlights.</span></span>

<span data-ttu-id="33346-115">省略號是在程式中以包含橢圓形資料 ([**D2D1 \_ 橢圓形**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) 和 color ([**D2D1 \_ color \_ F**](/windows/desktop/Direct2D/d2d1-color-f)) 的結構來表示。</span><span class="sxs-lookup"><span data-stu-id="33346-115">Ellipses are represented in the program by a structure that contains the ellipse data ([**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) and the color ([**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f)).</span></span> <span data-ttu-id="33346-116">結構也會定義兩個方法：用來繪製橢圓形的方法，以及用來執行點擊測試的方法。</span><span class="sxs-lookup"><span data-stu-id="33346-116">The structure also defines two methods: a method to draw the ellipse, and a method to perform hit testing.</span></span>


```C++
struct MyEllipse
{
    D2D1_ELLIPSE    ellipse;
    D2D1_COLOR_F    color;

    void Draw(ID2D1RenderTarget *pRT, ID2D1SolidColorBrush *pBrush)
    {
        pBrush->SetColor(color);
        pRT->FillEllipse(ellipse, pBrush);
        pBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black));
        pRT->DrawEllipse(ellipse, pBrush, 1.0f);
    }

    BOOL HitTest(float x, float y)
    {
        const float a = ellipse.radiusX;
        const float b = ellipse.radiusY;
        const float x1 = x - ellipse.point.x;
        const float y1 = y - ellipse.point.y;
        const float d = ((x1 * x1) / (a * a)) + ((y1 * y1) / (b * b));
        return d <= 1.0f;
    }
};
```



<span data-ttu-id="33346-117">程式會使用相同的純色筆刷來繪製每個橢圓形的填滿和外框，並視需要變更色彩。</span><span class="sxs-lookup"><span data-stu-id="33346-117">The program uses the same solid-color brush to draw the fill and outline for every ellipse, changing the color as needed.</span></span> <span data-ttu-id="33346-118">在 Direct2D 中，變更單色筆刷的色彩是有效率的作業。</span><span class="sxs-lookup"><span data-stu-id="33346-118">In Direct2D, changing the color of a solid-color brush is an efficient operation.</span></span> <span data-ttu-id="33346-119">因此，單色筆刷物件支援 [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) 方法。</span><span class="sxs-lookup"><span data-stu-id="33346-119">So, the solid-color brush object supports a [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) method.</span></span>

<span data-ttu-id="33346-120">省略號會儲存在 STL **清單** 容器中：</span><span class="sxs-lookup"><span data-stu-id="33346-120">The ellipses are stored in an STL **list** container:</span></span>


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> <span data-ttu-id="33346-121">**共用的 \_ ptr** 是在 TR1 中新增至 c + +，並在 c + + 0x 中正規化的智慧型指標類別。</span><span class="sxs-lookup"><span data-stu-id="33346-121">**shared\_ptr** is a smart-pointer class that was added to C++ in TR1 and formalized in C++0x.</span></span> <span data-ttu-id="33346-122">Visual Studio 2010 新增對 **共用 \_ pt** r 和其他 C + + 0x 功能的支援。</span><span class="sxs-lookup"><span data-stu-id="33346-122">Visual Studio 2010 adds support for **shared\_pt** r and other C++0x features.</span></span> <span data-ttu-id="33346-123">如需詳細資訊，請參閱 *MSDN 雜誌* [Visual Studio 2010 中的探索新的 c + + 和 MFC 功能](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010)。</span><span class="sxs-lookup"><span data-stu-id="33346-123">For more information, see [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span></span> <span data-ttu-id="33346-124"> (此資源可能無法在某些語言及國家/地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="33346-124">(This resource may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="33346-125">此程式有三種模式：</span><span class="sxs-lookup"><span data-stu-id="33346-125">The program has three modes:</span></span>

-   <span data-ttu-id="33346-126">繪圖模式。</span><span class="sxs-lookup"><span data-stu-id="33346-126">Draw mode.</span></span> <span data-ttu-id="33346-127">使用者可以繪製新的省略號。</span><span class="sxs-lookup"><span data-stu-id="33346-127">The user can draw new ellipses.</span></span>
-   <span data-ttu-id="33346-128">選取模式。</span><span class="sxs-lookup"><span data-stu-id="33346-128">Selection mode.</span></span> <span data-ttu-id="33346-129">使用者可以選取省略號。</span><span class="sxs-lookup"><span data-stu-id="33346-129">The user can select an ellipse.</span></span>
-   <span data-ttu-id="33346-130">拖曳模式。</span><span class="sxs-lookup"><span data-stu-id="33346-130">Drag mode.</span></span> <span data-ttu-id="33346-131">使用者可以拖曳選取的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="33346-131">The user can drag a selected ellipse.</span></span>

<span data-ttu-id="33346-132">使用者可以使用 [快速鍵對應表](accelerator-tables.md)中所述的相同鍵盤快速鍵，在繪製模式與選取模式之間切換。</span><span class="sxs-lookup"><span data-stu-id="33346-132">The user can switch between draw mode and selection mode by using the same keyboard shortcuts described in [Accelerator Tables](accelerator-tables.md).</span></span> <span data-ttu-id="33346-133">在選取模式中，如果使用者按一下橢圓形，程式就會切換至拖曳模式。</span><span class="sxs-lookup"><span data-stu-id="33346-133">From selection mode, the program switches to drag mode if the user clicks on an ellipse.</span></span> <span data-ttu-id="33346-134">當使用者放開滑鼠按鍵時，就會切換回選取模式。</span><span class="sxs-lookup"><span data-stu-id="33346-134">It switches back to selection mode when the user releases the mouse button.</span></span> <span data-ttu-id="33346-135">目前的選取專案會儲存為省略號清單中的反覆運算器。</span><span class="sxs-lookup"><span data-stu-id="33346-135">The current selection is stored as an iterator into the list of ellipses.</span></span> <span data-ttu-id="33346-136">Helper 方法 `MainWindow::Selection` 會傳回所選橢圓形的指標，如果沒有選取範圍，則會傳回值 **nullptr** 。</span><span class="sxs-lookup"><span data-stu-id="33346-136">The helper method `MainWindow::Selection` returns a pointer to the selected ellipse, or the value **nullptr** if there is no selection.</span></span>


```C++
    list<shared_ptr<MyEllipse>>::iterator   selection;
     
    shared_ptr<MyEllipse> Selection() 
    { 
        if (selection == ellipses.end()) 
        { 
            return nullptr;
        }
        else
        {
            return (*selection);
        }
    }

    void    ClearSelection() { selection = ellipses.end(); }
```



<span data-ttu-id="33346-137">下表摘要說明在三種模式中的滑鼠輸入效果。</span><span class="sxs-lookup"><span data-stu-id="33346-137">The following table summarizes the effects of mouse input in each of the three modes.</span></span>



| <span data-ttu-id="33346-138">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="33346-138">Mouse Input</span></span>      | <span data-ttu-id="33346-139">繪圖模式</span><span class="sxs-lookup"><span data-stu-id="33346-139">Draw Mode</span></span>                                          | <span data-ttu-id="33346-140">選取模式</span><span class="sxs-lookup"><span data-stu-id="33346-140">Selection Mode</span></span>                                                                                                                               | <span data-ttu-id="33346-141">拖曳模式</span><span class="sxs-lookup"><span data-stu-id="33346-141">Drag Mode</span></span>                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="33346-142">向下鍵向下按鈕</span><span class="sxs-lookup"><span data-stu-id="33346-142">Left button down</span></span> | <span data-ttu-id="33346-143">設定滑鼠捕捉並開始繪製新的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="33346-143">Set mouse capture and start to draw a new ellipse.</span></span> | <span data-ttu-id="33346-144">釋放目前的選取範圍並執行點擊測試。</span><span class="sxs-lookup"><span data-stu-id="33346-144">Release the current selection and perform a hit test.</span></span> <span data-ttu-id="33346-145">如果叫用省略號，請捕捉游標、選取省略號，然後切換至拖曳模式。</span><span class="sxs-lookup"><span data-stu-id="33346-145">If an ellipse is hit, capture the cursor, select the ellipse, and switch to drag mode.</span></span> | <span data-ttu-id="33346-146">不進行動作。</span><span class="sxs-lookup"><span data-stu-id="33346-146">No action.</span></span>                 |
| <span data-ttu-id="33346-147">滑鼠移動</span><span class="sxs-lookup"><span data-stu-id="33346-147">Mouse move</span></span>       | <span data-ttu-id="33346-148">如果左按鈕已關閉，則調整橢圓形的大小。</span><span class="sxs-lookup"><span data-stu-id="33346-148">If the left button is down, resize the ellipse.</span></span>    | <span data-ttu-id="33346-149">不進行動作。</span><span class="sxs-lookup"><span data-stu-id="33346-149">No action.</span></span>                                                                                                                                   | <span data-ttu-id="33346-150">移動選取的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="33346-150">Move the selected ellipse.</span></span> |
| <span data-ttu-id="33346-151">左方按鈕向上鍵</span><span class="sxs-lookup"><span data-stu-id="33346-151">Left button up</span></span>   | <span data-ttu-id="33346-152">停止繪圖橢圓形。</span><span class="sxs-lookup"><span data-stu-id="33346-152">Stop drawing the ellipse.</span></span>                          | <span data-ttu-id="33346-153">不進行動作。</span><span class="sxs-lookup"><span data-stu-id="33346-153">No action.</span></span>                                                                                                                                   | <span data-ttu-id="33346-154">切換至選取模式。</span><span class="sxs-lookup"><span data-stu-id="33346-154">Switch to selection mode.</span></span>  |



 

<span data-ttu-id="33346-155">類別中的下列方法會 `MainWindow` 處理 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 訊息。</span><span class="sxs-lookup"><span data-stu-id="33346-155">The following method in the `MainWindow` class handles [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) messages.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if (mode == DrawMode)
    {
        POINT pt = { pixelX, pixelY };

        if (DragDetect(m_hwnd, pt))
        {
            SetCapture(m_hwnd);
        
            // Start a new ellipse.
            InsertEllipse(dipX, dipY);
        }
    }
    else
    {
        ClearSelection();

        if (HitTest(dipX, dipY))
        {
            SetCapture(m_hwnd);

            ptMouse = Selection()->ellipse.point;
            ptMouse.x -= dipX;
            ptMouse.y -= dipY;

            SetMode(DragMode);
        }
    }
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



<span data-ttu-id="33346-156">滑鼠座標會以圖元傳遞給這個方法，然後轉換為 Dip。</span><span class="sxs-lookup"><span data-stu-id="33346-156">Mouse coordinates are passed to this method in pixels, and then converted to DIPs.</span></span> <span data-ttu-id="33346-157">請務必不要混淆這兩個單元。</span><span class="sxs-lookup"><span data-stu-id="33346-157">It is important not to confuse these two units.</span></span> <span data-ttu-id="33346-158">例如， [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) 函式使用圖元，但繪製和點擊測試使用 dip。</span><span class="sxs-lookup"><span data-stu-id="33346-158">For example, the [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function uses pixels, but drawing and hit-testing use DIPs.</span></span> <span data-ttu-id="33346-159">一般規則是 windows 或滑鼠輸入的相關函式使用圖元，而 Direct2D 和 DirectWrite 則使用 Dip。</span><span class="sxs-lookup"><span data-stu-id="33346-159">The general rule is that functions related to windows or mouse input use pixels, while Direct2D and DirectWrite use DIPs.</span></span> <span data-ttu-id="33346-160">一律以高 DPI 設定測試程式，並記得將您的程式標示為 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="33346-160">Always test your program at a high-DPI setting, and remember to mark your program as DPI-aware.</span></span> <span data-ttu-id="33346-161">如需詳細資訊，請參閱 [DPI 和 Device-Independent 圖元](dpi-and-device-independent-pixels.md)。</span><span class="sxs-lookup"><span data-stu-id="33346-161">For more information, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span>

<span data-ttu-id="33346-162">以下是處理 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息的程式碼。</span><span class="sxs-lookup"><span data-stu-id="33346-162">Here is the code that handles [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages.</span></span>


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if ((flags & MK_LBUTTON) && Selection())
    { 
        if (mode == DrawMode)
        {
            // Resize the ellipse.
            const float width = (dipX - ptMouse.x) / 2;
            const float height = (dipY - ptMouse.y) / 2;
            const float x1 = ptMouse.x + width;
            const float y1 = ptMouse.y + height;

            Selection()->ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);
        }
        else if (mode == DragMode)
        {
            // Move the ellipse.
            Selection()->ellipse.point.x = dipX + ptMouse.x;
            Selection()->ellipse.point.y = dipY + ptMouse.y;
        }
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="33346-163">先前的 [範例：繪製圓形](mouse-movement.md)中會說明調整橢圓形大小的邏輯。</span><span class="sxs-lookup"><span data-stu-id="33346-163">The logic to resize an ellipse was described previously, in the section [Example: Drawing Circles](mouse-movement.md).</span></span> <span data-ttu-id="33346-164">也請注意 [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="33346-164">Also note the call to [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="33346-165">這可確保重新繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="33346-165">This makes sure that the window is repainted.</span></span> <span data-ttu-id="33346-166">下列程式碼會處理 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) 訊息。</span><span class="sxs-lookup"><span data-stu-id="33346-166">The following code handles [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    if ((mode == DrawMode) && Selection())
    {
        ClearSelection();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
    else if (mode == DragMode)
    {
        SetMode(SelectMode);
    }
    ReleaseCapture(); 
}
```



<span data-ttu-id="33346-167">如您所見，滑鼠輸入的訊息處理常式全都有分支程式碼，視目前的模式而定。</span><span class="sxs-lookup"><span data-stu-id="33346-167">As you can see, the message handlers for mouse input all have branching code, depending on the current mode.</span></span> <span data-ttu-id="33346-168">這是這個相當簡單程式的可接受設計。</span><span class="sxs-lookup"><span data-stu-id="33346-168">That is an acceptable design for this fairly simple program.</span></span> <span data-ttu-id="33346-169">但是，如果加入新的模式，它可能很快就會變得太複雜。</span><span class="sxs-lookup"><span data-stu-id="33346-169">However, it could quickly become too complex if new modes are added.</span></span> <span data-ttu-id="33346-170">針對較大的程式， (MVC) 架構的模型視圖控制器可能是更好的設計。</span><span class="sxs-lookup"><span data-stu-id="33346-170">For a larger program, a model-view-controller (MVC) architecture might be a better design.</span></span> <span data-ttu-id="33346-171">在這種架構中，負責處理使用者輸入的 *控制器* 會與 *模型* 分開，以管理應用程式資料。</span><span class="sxs-lookup"><span data-stu-id="33346-171">In this kind of architecture, the *controller*, which handles user input, is separated from the *model*, which manages application data.</span></span>

<span data-ttu-id="33346-172">當程式切換模式時，游標會變更以將意見反應提供給使用者。</span><span class="sxs-lookup"><span data-stu-id="33346-172">When the program switches modes, the cursor changes to give feedback to the user.</span></span>


```C++
void MainWindow::SetMode(Mode m)
{
    mode = m;

    // Update the cursor
    LPWSTR cursor;
    switch (mode)
    {
    case DrawMode:
        cursor = IDC_CROSS;
        break;

    case SelectMode:
        cursor = IDC_HAND;
        break;

    case DragMode:
        cursor = IDC_SIZEALL;
        break;
    }

    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
}
```



<span data-ttu-id="33346-173">最後，請記得在視窗收到 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 訊息時設定游標：</span><span class="sxs-lookup"><span data-stu-id="33346-173">And finally, remember to set the cursor when the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message:</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a><span data-ttu-id="33346-174">總結</span><span class="sxs-lookup"><span data-stu-id="33346-174">Summary</span></span>

<span data-ttu-id="33346-175">在本課程模組中，您已瞭解如何處理滑鼠和鍵盤輸入;如何定義鍵盤快速鍵;以及如何更新游標影像，以反映程式的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="33346-175">In this module, you learned how to handle mouse and keyboard input; how to define keyboard shortcuts; and how to update the cursor image to reflect the current state of the program.</span></span>

 

 