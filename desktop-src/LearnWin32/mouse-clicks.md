---
title: 回應滑鼠點擊
description: 回應滑鼠點擊
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c37903264ca638aeca1c0b28fb2ea7fa792660
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092721"
---
# <a name="responding-to-mouse-clicks"></a><span data-ttu-id="56a29-103">回應滑鼠點擊</span><span class="sxs-lookup"><span data-stu-id="56a29-103">Responding to Mouse Clicks</span></span>

<span data-ttu-id="56a29-104">當游標位於視窗的工作區時，如果使用者按下滑鼠按鍵，該視窗就會收到下列其中一則訊息。</span><span class="sxs-lookup"><span data-stu-id="56a29-104">If the user clicks a mouse button while the cursor is over the client area of a window, the window receives one of the following messages.</span></span>



| <span data-ttu-id="56a29-105">訊息</span><span class="sxs-lookup"><span data-stu-id="56a29-105">Message</span></span>                                        | <span data-ttu-id="56a29-106">意義</span><span class="sxs-lookup"><span data-stu-id="56a29-106">Meaning</span></span>                   |
|------------------------------------------------|---------------------------|
| [<span data-ttu-id="56a29-107">**WM \_ LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="56a29-107">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown) | <span data-ttu-id="56a29-108">向下鍵向下按鈕</span><span class="sxs-lookup"><span data-stu-id="56a29-108">Left button down</span></span>          |
| [<span data-ttu-id="56a29-109">**WM \_ LBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="56a29-109">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)     | <span data-ttu-id="56a29-110">左方按鈕向上鍵</span><span class="sxs-lookup"><span data-stu-id="56a29-110">Left button up</span></span>            |
| [<span data-ttu-id="56a29-111">**WM \_ MBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="56a29-111">**WM\_MBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-mbuttondown) | <span data-ttu-id="56a29-112">中間按鈕下移</span><span class="sxs-lookup"><span data-stu-id="56a29-112">Middle button down</span></span>        |
| [<span data-ttu-id="56a29-113">**WM \_ MBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="56a29-113">**WM\_MBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-mbuttonup)     | <span data-ttu-id="56a29-114">中間按鈕向上鍵</span><span class="sxs-lookup"><span data-stu-id="56a29-114">Middle button up</span></span>          |
| [<span data-ttu-id="56a29-115">**WM \_ RBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="56a29-115">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown) | <span data-ttu-id="56a29-116">向下鍵向下按鈕</span><span class="sxs-lookup"><span data-stu-id="56a29-116">Right button down</span></span>         |
| [<span data-ttu-id="56a29-117">**WM \_ RBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="56a29-117">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)     | <span data-ttu-id="56a29-118">向右鍵向上鍵</span><span class="sxs-lookup"><span data-stu-id="56a29-118">Right button up</span></span>           |
| [<span data-ttu-id="56a29-119">**WM \_ XBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="56a29-119">**WM\_XBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-xbuttondown) | <span data-ttu-id="56a29-120">XBUTTON1 或 XBUTTON2 向下</span><span class="sxs-lookup"><span data-stu-id="56a29-120">XBUTTON1 or XBUTTON2 down</span></span> |
| [<span data-ttu-id="56a29-121">**WM \_ XBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="56a29-121">**WM\_XBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-xbuttonup)     | <span data-ttu-id="56a29-122">XBUTTON1 或 XBUTTON2 up</span><span class="sxs-lookup"><span data-stu-id="56a29-122">XBUTTON1 or XBUTTON2 up</span></span>   |



 

<span data-ttu-id="56a29-123">回想一下，工作區是排除框架的視窗部分。</span><span class="sxs-lookup"><span data-stu-id="56a29-123">Recall that the client area is the portion of the window that excludes the frame.</span></span> <span data-ttu-id="56a29-124">如需有關用戶端區域的詳細資訊，請參閱 [什麼是視窗？](what-is-a-window-.md)</span><span class="sxs-lookup"><span data-stu-id="56a29-124">For more information about client areas, see [What Is a Window?](what-is-a-window-.md)</span></span>

### <a name="mouse-coordinates"></a><span data-ttu-id="56a29-125">滑鼠座標</span><span class="sxs-lookup"><span data-stu-id="56a29-125">Mouse Coordinates</span></span>

<span data-ttu-id="56a29-126">在所有這些訊息中， *lParam* 參數都包含滑鼠指標的 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="56a29-126">In all of these messages, the *lParam* parameter contains the x- and y-coordinates of the mouse pointer.</span></span> <span data-ttu-id="56a29-127">*LParam* 的最低16位包含 x 座標，後面的16個位包含 y 座標。</span><span class="sxs-lookup"><span data-stu-id="56a29-127">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="56a29-128">使用 [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 並 [**取得 \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏，將座標從 *LPARAM* 解壓縮。</span><span class="sxs-lookup"><span data-stu-id="56a29-128">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="56a29-129">這些宏會定義在標頭檔 WindowsX 中。</span><span class="sxs-lookup"><span data-stu-id="56a29-129">These macros are defined in the header file WindowsX.h.</span></span>

<span data-ttu-id="56a29-130">在64位的 Windows 上， *lParam* 是64位值。</span><span class="sxs-lookup"><span data-stu-id="56a29-130">On 64-bit Windows, *lParam* is 64-bit value.</span></span> <span data-ttu-id="56a29-131">不使用 *lParam* 的上方32位。</span><span class="sxs-lookup"><span data-stu-id="56a29-131">The upper 32 bits of *lParam* are not used.</span></span> <span data-ttu-id="56a29-132">MSDN 檔提及 *lParam* 的「低序位單字」和「高序位單字」。</span><span class="sxs-lookup"><span data-stu-id="56a29-132">The MSDN documentation mentions the "low-order word" and "high-order word" of *lParam*.</span></span> <span data-ttu-id="56a29-133">在64位的情況下，這表示較低的32位的低和高序位字組。</span><span class="sxs-lookup"><span data-stu-id="56a29-133">In the 64-bit case, this means the low- and high-order words of the lower 32 bits.</span></span> <span data-ttu-id="56a29-134">宏會將正確的值解壓縮，因此，如果您使用這些值，就會是安全的。</span><span class="sxs-lookup"><span data-stu-id="56a29-134">The macros extract the right values, so if you use them, you will be safe.</span></span>

<span data-ttu-id="56a29-135">滑鼠座標以圖元為單位，而不是與裝置無關的圖元 (Dip) ，而且會相對於視窗的工作區進行測量。</span><span class="sxs-lookup"><span data-stu-id="56a29-135">Mouse coordinates are given in pixels, not device-independent pixels (DIPs), and are measured relative to the client area of the window.</span></span> <span data-ttu-id="56a29-136">座標為帶正負號的值。</span><span class="sxs-lookup"><span data-stu-id="56a29-136">Coordinates are signed values.</span></span> <span data-ttu-id="56a29-137">在工作區左邊和左邊的位置具有負座標，如果您在視窗外追蹤滑鼠位置，這就很重要。</span><span class="sxs-lookup"><span data-stu-id="56a29-137">Positions above and to the left of the client area have negative coordinates, which is important if you track the mouse position outside the window.</span></span> <span data-ttu-id="56a29-138">在稍後的主題中，我們將瞭解如何在 [視窗外捕捉滑鼠移動](mouse-movement.md)。</span><span class="sxs-lookup"><span data-stu-id="56a29-138">We will see how to do that in a later topic, [Capturing Mouse Movement Outside the Window](mouse-movement.md).</span></span>

### <a name="additional-flags"></a><span data-ttu-id="56a29-139">其他旗標</span><span class="sxs-lookup"><span data-stu-id="56a29-139">Additional Flags</span></span>

<span data-ttu-id="56a29-140">*WParam* 參數包含位 **or** of 旗標，表示另一個滑鼠按鍵的狀態以及 SHIFT 和 CTRL 鍵。</span><span class="sxs-lookup"><span data-stu-id="56a29-140">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span>



| <span data-ttu-id="56a29-141">旗標</span><span class="sxs-lookup"><span data-stu-id="56a29-141">Flag</span></span>             | <span data-ttu-id="56a29-142">意義</span><span class="sxs-lookup"><span data-stu-id="56a29-142">Meaning</span></span>                          |
|------------------|----------------------------------|
| <span data-ttu-id="56a29-143">**MK \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="56a29-143">**MK\_CONTROL**</span></span>  | <span data-ttu-id="56a29-144">CTRL 鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="56a29-144">The CTRL key is down.</span></span>            |
| <span data-ttu-id="56a29-145">**MK \_ LBUTTON**</span><span class="sxs-lookup"><span data-stu-id="56a29-145">**MK\_LBUTTON**</span></span>  | <span data-ttu-id="56a29-146">左邊的滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="56a29-146">The left mouse button is down.</span></span>   |
| <span data-ttu-id="56a29-147">**MK \_ MBUTTON**</span><span class="sxs-lookup"><span data-stu-id="56a29-147">**MK\_MBUTTON**</span></span>  | <span data-ttu-id="56a29-148">中間的滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="56a29-148">The middle mouse button is down.</span></span> |
| <span data-ttu-id="56a29-149">**MK \_ RBUTTON**</span><span class="sxs-lookup"><span data-stu-id="56a29-149">**MK\_RBUTTON**</span></span>  | <span data-ttu-id="56a29-150">滑鼠右鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="56a29-150">The right mouse button is down.</span></span>  |
| <span data-ttu-id="56a29-151">**MK \_ 移位**</span><span class="sxs-lookup"><span data-stu-id="56a29-151">**MK\_SHIFT**</span></span>    | <span data-ttu-id="56a29-152">SHIFT 鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="56a29-152">The SHIFT key is down.</span></span>           |
| <span data-ttu-id="56a29-153">**MK \_ XBUTTON1**</span><span class="sxs-lookup"><span data-stu-id="56a29-153">**MK\_XBUTTON1**</span></span> | <span data-ttu-id="56a29-154">[XBUTTON1] 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="56a29-154">The XBUTTON1 button is down.</span></span>     |
| <span data-ttu-id="56a29-155">**MK \_ XBUTTON2**</span><span class="sxs-lookup"><span data-stu-id="56a29-155">**MK\_XBUTTON2**</span></span> | <span data-ttu-id="56a29-156">[XBUTTON2] 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="56a29-156">The XBUTTON2 button is down.</span></span>     |



 

<span data-ttu-id="56a29-157">沒有旗標表示未按下對應的按鈕或按鍵。</span><span class="sxs-lookup"><span data-stu-id="56a29-157">The absence of a flag means the corresponding button or key was not pressed.</span></span> <span data-ttu-id="56a29-158">例如，若要測試 CTRL 鍵是否已關閉：</span><span class="sxs-lookup"><span data-stu-id="56a29-158">For example, to test whether the CTRL key is down:</span></span>


```C++
if (wParam & MK_CONTROL) { ...
```



<span data-ttu-id="56a29-159">如果您需要尋找 CTRL 和 SHIFT 以外的其他按鍵狀態，請使用 [[鍵盤輸入](keyboard-input.md)] 中所述的 [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate)函數。</span><span class="sxs-lookup"><span data-stu-id="56a29-159">If you need to find the state of other keys besides CTRL and SHIFT, use the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function, which is described in [Keyboard Input](keyboard-input.md).</span></span>

<span data-ttu-id="56a29-160">[**Wm \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown)和 [**wm \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup)視窗訊息同時適用于 XBUTTON1 和 XBUTTON2。</span><span class="sxs-lookup"><span data-stu-id="56a29-160">The [**WM\_XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) and [**WM\_XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) window messages apply to both XBUTTON1 and XBUTTON2.</span></span> <span data-ttu-id="56a29-161">*WParam* 參數指出按一下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="56a29-161">The *wParam* parameter indicates which button was clicked.</span></span>


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a><span data-ttu-id="56a29-162">按兩下</span><span class="sxs-lookup"><span data-stu-id="56a29-162">Double Clicks</span></span>

<span data-ttu-id="56a29-163">根據預設，視窗不會收到按兩下的通知。</span><span class="sxs-lookup"><span data-stu-id="56a29-163">A window does not receive double-click notifications by default.</span></span> <span data-ttu-id="56a29-164">若要接收按兩下，請在註冊視窗類別時，在 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構中設定 **CS \_ DBLCLKS** 旗標。</span><span class="sxs-lookup"><span data-stu-id="56a29-164">To receive double clicks, set the **CS\_DBLCLKS** flag in the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure when you register the window class.</span></span>


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



<span data-ttu-id="56a29-165">如果您設定 **CS \_ DBLCLKS** 旗標（如所示），此視窗將會收到按兩下通知。</span><span class="sxs-lookup"><span data-stu-id="56a29-165">If you set the **CS\_DBLCLKS** flag as shown, the window will receive double-click notifications.</span></span> <span data-ttu-id="56a29-166">按兩下會以名稱中有 "DBLCLK" 的視窗訊息表示。</span><span class="sxs-lookup"><span data-stu-id="56a29-166">A double click is indicated by a window message with "DBLCLK" in the name.</span></span> <span data-ttu-id="56a29-167">例如，按兩下滑鼠左鍵會產生下列一連串的訊息：</span><span class="sxs-lookup"><span data-stu-id="56a29-167">For example, a double click on the left mouse button produces the following sequence of messages:</span></span>

<dl>

[<span data-ttu-id="56a29-168">**WM \_ LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="56a29-168">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)  
[<span data-ttu-id="56a29-169">**WM \_ LBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="56a29-169">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
[<span data-ttu-id="56a29-170">**WM \_ LBUTTONDBLCLK**</span><span class="sxs-lookup"><span data-stu-id="56a29-170">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)  
[<span data-ttu-id="56a29-171">**WM \_ LBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="56a29-171">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

<span data-ttu-id="56a29-172">實際上，通常會產生的第二個 [**wm \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 訊息會變成 [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) 訊息。</span><span class="sxs-lookup"><span data-stu-id="56a29-172">In effect, the second [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message that would normally be generated becomes a [**WM\_LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) message.</span></span> <span data-ttu-id="56a29-173">對等的訊息會定義為 right、中間和 XBUTTON 按鈕。</span><span class="sxs-lookup"><span data-stu-id="56a29-173">Equivalent messages are defined for right, middle, and XBUTTON buttons.</span></span>

<span data-ttu-id="56a29-174">在您看到按兩下訊息之前，無法分辨一下第一次按下滑鼠，就是按兩下開始。</span><span class="sxs-lookup"><span data-stu-id="56a29-174">Until you get the double-click message, there is no way to tell that the first mouse click is the start of a double click.</span></span> <span data-ttu-id="56a29-175">因此，按兩下動作應該會繼續執行以第一次按一下滑鼠的動作。</span><span class="sxs-lookup"><span data-stu-id="56a29-175">Therefore, a double-click action should continue an action that begins with the first mouse click.</span></span> <span data-ttu-id="56a29-176">例如，在 Windows Shell 中，只要按一下，就會選取資料夾，然後按兩下以開啟資料夾。</span><span class="sxs-lookup"><span data-stu-id="56a29-176">For example, in the Windows Shell, a single click selects a folder, while a double click opens the folder.</span></span>

## <a name="non-client-mouse-messages"></a><span data-ttu-id="56a29-177">非用戶端滑鼠訊息</span><span class="sxs-lookup"><span data-stu-id="56a29-177">Non-client Mouse Messages</span></span>

<span data-ttu-id="56a29-178">系統會為視窗的非工作區中所發生的滑鼠事件定義一組個別的訊息。</span><span class="sxs-lookup"><span data-stu-id="56a29-178">A separate set of messages are defined for mouse events that occur within the non-client area of the window.</span></span> <span data-ttu-id="56a29-179">這些訊息的名稱中會有字母 "NC"。</span><span class="sxs-lookup"><span data-stu-id="56a29-179">These messages have the letters "NC" in the name.</span></span> <span data-ttu-id="56a29-180">例如， [**wm \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) 與 [**wm \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)的非用戶端相等。</span><span class="sxs-lookup"><span data-stu-id="56a29-180">For example, [**WM\_NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) is the non-client equivalent of [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span></span> <span data-ttu-id="56a29-181">一般的應用程式不會攔截這些訊息，因為 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會正確處理這些訊息。</span><span class="sxs-lookup"><span data-stu-id="56a29-181">A typical application will not intercept these messages, because the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function handles these messages correctly.</span></span> <span data-ttu-id="56a29-182">不過，它們對某些 advanced 函式很有用。</span><span class="sxs-lookup"><span data-stu-id="56a29-182">However, they can be useful for certain advanced functions.</span></span> <span data-ttu-id="56a29-183">例如，您可以使用這些訊息在標題列中執行自訂行為。</span><span class="sxs-lookup"><span data-stu-id="56a29-183">For example, you could use these messages to implement custom behavior in the title bar.</span></span> <span data-ttu-id="56a29-184">如果您處理這些訊息，您通常應該在之後將它們傳遞給 **DefWindowProc** 。</span><span class="sxs-lookup"><span data-stu-id="56a29-184">If you do handle these messages, you should generally pass them to **DefWindowProc** afterward.</span></span> <span data-ttu-id="56a29-185">否則，您的應用程式將會中斷標準功能，例如拖曳或最小化視窗。</span><span class="sxs-lookup"><span data-stu-id="56a29-185">Otherwise, your application will break standard functionality such as dragging or minimizing the window.</span></span>

## <a name="next"></a><span data-ttu-id="56a29-186">下一個</span><span class="sxs-lookup"><span data-stu-id="56a29-186">Next</span></span>

[<span data-ttu-id="56a29-187">滑鼠移動</span><span class="sxs-lookup"><span data-stu-id="56a29-187">Mouse Movement</span></span>](mouse-movement.md)

 

 