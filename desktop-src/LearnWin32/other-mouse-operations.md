---
title: 其他滑鼠操作
description: 前幾節已討論過滑鼠點擊和滑鼠移動。 以下是一些可以使用滑鼠來執行的其他作業。
ms.assetid: 6A5B953F-7032-4AA6-8B64-2E9CBB8F59F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfba63dce8116d79a557cbbbf8895f17d2a8f1b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315067"
---
# <a name="miscellaneous-mouse-operations"></a><span data-ttu-id="41d7c-104">其他滑鼠操作</span><span class="sxs-lookup"><span data-stu-id="41d7c-104">Miscellaneous Mouse Operations</span></span>

<span data-ttu-id="41d7c-105">前幾節已討論過滑鼠點擊和滑鼠移動。</span><span class="sxs-lookup"><span data-stu-id="41d7c-105">The previous sections have discussed mouse clicks and mouse movement.</span></span> <span data-ttu-id="41d7c-106">以下是一些可以使用滑鼠來執行的其他作業。</span><span class="sxs-lookup"><span data-stu-id="41d7c-106">Here are some other operations that can be performed with the mouse.</span></span>

## <a name="dragging-ui-elements"></a><span data-ttu-id="41d7c-107">拖曳 UI 元素</span><span class="sxs-lookup"><span data-stu-id="41d7c-107">Dragging UI Elements</span></span>

<span data-ttu-id="41d7c-108">如果您的 UI 支援拖曳 UI 專案，則您應該在滑鼠左鍵的訊息處理常式中呼叫另一個函數： [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect)。</span><span class="sxs-lookup"><span data-stu-id="41d7c-108">If your UI supports dragging of UI elements, there is one other function that you should call in your mouse-down message handler: [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect).</span></span> <span data-ttu-id="41d7c-109">如果使用者起始應解釋為拖曳的滑鼠手勢， **DragDetect** 函式會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="41d7c-109">The **DragDetect** function returns **TRUE** if the user initiates a mouse gesture that should be interpreted as dragging.</span></span> <span data-ttu-id="41d7c-110">下列程式碼示範如何使用此函式。</span><span class="sxs-lookup"><span data-stu-id="41d7c-110">The following code shows how to use this function.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        {
            POINT pt = { GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam) };
            if (DragDetect(m_hwnd, pt))
            {
                // Start dragging.
            }
        }
        return 0;
```



<span data-ttu-id="41d7c-111">以下是概念：當某個程式支援拖放時，您不希望每個滑鼠點擊都能以拖曳的方式轉譯。</span><span class="sxs-lookup"><span data-stu-id="41d7c-111">Here's the idea: When a program supports drag and drop, you don't want every mouse click to be interpreted as a drag.</span></span> <span data-ttu-id="41d7c-112">否則，當使用者只是想要按一下它時，使用者可能會不小心拖曳某個東西 (例如，將它選取) 。</span><span class="sxs-lookup"><span data-stu-id="41d7c-112">Otherwise, the user might accidentally drag something when he or she simply meant to click on it (for example, to select it).</span></span> <span data-ttu-id="41d7c-113">但是，如果滑鼠特別敏感，則在按一下時，可能很難讓滑鼠保持完美。</span><span class="sxs-lookup"><span data-stu-id="41d7c-113">But if a mouse is particularly sensitive, it can be hard to keep the mouse perfectly still while clicking.</span></span> <span data-ttu-id="41d7c-114">因此，Windows 會定義一些圖元的拖曳臨界值。</span><span class="sxs-lookup"><span data-stu-id="41d7c-114">Therefore, Windows defines a drag threshold of a few pixels.</span></span> <span data-ttu-id="41d7c-115">當使用者按下滑鼠按鍵時，除非滑鼠超過此臨界值，否則不會將它視為拖曳。</span><span class="sxs-lookup"><span data-stu-id="41d7c-115">When the user presses the mouse button, it is not considered a drag unless the mouse crosses this threshold.</span></span> <span data-ttu-id="41d7c-116">[**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect)函式會測試是否達到此臨界值。</span><span class="sxs-lookup"><span data-stu-id="41d7c-116">The [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function tests whether this threshold is reached.</span></span> <span data-ttu-id="41d7c-117">如果函式傳回 **TRUE**，您可以將滑鼠按一下的方式解讀為拖曳。</span><span class="sxs-lookup"><span data-stu-id="41d7c-117">If the function returns **TRUE**, you can interpret the mouse click as a drag.</span></span> <span data-ttu-id="41d7c-118">否則，請不要這麼做。</span><span class="sxs-lookup"><span data-stu-id="41d7c-118">Otherwise, do not.</span></span>

> [!Note]  
> <span data-ttu-id="41d7c-119">如果 [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) 傳回 **FALSE**，則當使用者放開滑鼠按鍵時，Windows 會隱藏 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) 訊息。</span><span class="sxs-lookup"><span data-stu-id="41d7c-119">If [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) returns **FALSE**, Windows suppresses the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message when the user releases the mouse button.</span></span> <span data-ttu-id="41d7c-120">因此，除非您的程式目前處於支援拖曳的模式，否則請勿呼叫 **DragDetect** 。</span><span class="sxs-lookup"><span data-stu-id="41d7c-120">Therefore, do not call **DragDetect** unless your program is currently in a mode that supports dragging.</span></span> <span data-ttu-id="41d7c-121"> (例如，如果已選取可拖曳的 UI 元素。在此課程模組結束時 ) ，我們會看到使用 **DragDetect** 函式的較長程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="41d7c-121">(For example, if a draggable UI element is already selected.) At the end of this module, we will see a longer code example that uses the **DragDetect** function.</span></span>

 

## <a name="confining-the-cursor"></a><span data-ttu-id="41d7c-122">將資料指標</span><span class="sxs-lookup"><span data-stu-id="41d7c-122">Confining the Cursor</span></span>

<span data-ttu-id="41d7c-123">有時候您可能會想要將游標限制在工作區或工作區的一部分。</span><span class="sxs-lookup"><span data-stu-id="41d7c-123">Sometimes you might want to restrict the cursor to the client area or a portion of the client area.</span></span> <span data-ttu-id="41d7c-124">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor)函式會將資料指標的移動限制為指定的矩形。</span><span class="sxs-lookup"><span data-stu-id="41d7c-124">The [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) function restricts the movement of the cursor to a specified rectangle.</span></span> <span data-ttu-id="41d7c-125">這個矩形是以螢幕座標（而不是用戶端座標）來提供，因此點 (0，0) 表示畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="41d7c-125">This rectangle is given in screen coordinates, rather than client coordinates, so the point (0, 0) means the upper left corner of the screen.</span></span> <span data-ttu-id="41d7c-126">若要將用戶端座標轉譯為螢幕座標，請呼叫函式 [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen)。</span><span class="sxs-lookup"><span data-stu-id="41d7c-126">To translate client coordinates into screen coordinates, call the function [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen).</span></span>

<span data-ttu-id="41d7c-127">下列程式碼會將游標範圍設為視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="41d7c-127">The following code confines the cursor to the client area of the window.</span></span>


```C++
    // Get the window client area.
    RECT rc;
    GetClientRect(m_hwnd, &rc);

    // Convert the client area to screen coordinates.
    POINT pt = { rc.left, rc.top };
    POINT pt2 = { rc.right, rc.bottom };
    ClientToScreen(m_hwnd, &pt);
    ClientToScreen(m_hwnd, &pt2);
    SetRect(&rc, pt.x, pt.y, pt2.x, pt2.y);

    // Confine the cursor.
    ClipCursor(&rc);
```



<span data-ttu-id="41d7c-128">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) 會採用 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構，但 [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) 會採用 [**點**](/previous-versions//dd162805(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="41d7c-128">[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) takes a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure, but [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) takes a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="41d7c-129">矩形是由左上角和右下角的點所定義。</span><span class="sxs-lookup"><span data-stu-id="41d7c-129">A rectangle is defined by its top-left and bottom-right points.</span></span> <span data-ttu-id="41d7c-130">您可以將資料指標限制為任何矩形區域（包括視窗以外的區域），但是將游標將到工作區是使用函式的典型方式。</span><span class="sxs-lookup"><span data-stu-id="41d7c-130">You can confine the cursor to any rectangular area, including areas outside the window, but confining the cursor to the client area is a typical way to use the function.</span></span> <span data-ttu-id="41d7c-131">將游標將至範圍外的整個區域會是不尋常的，使用者可能會察覺到它是錯誤。</span><span class="sxs-lookup"><span data-stu-id="41d7c-131">Confining the cursor to a region entirely outside your window would be unusual, and users would probably perceive it as a bug.</span></span>

<span data-ttu-id="41d7c-132">若要移除限制，請使用值 **Null** 來呼叫 [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) 。</span><span class="sxs-lookup"><span data-stu-id="41d7c-132">To remove the restriction, call [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) with the value **NULL**.</span></span>


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a><span data-ttu-id="41d7c-133">滑鼠追蹤事件：停留並離開</span><span class="sxs-lookup"><span data-stu-id="41d7c-133">Mouse Tracking Events: Hover and Leave</span></span>

<span data-ttu-id="41d7c-134">預設會停用其他兩個滑鼠訊息，但對某些應用程式而言可能很有用：</span><span class="sxs-lookup"><span data-stu-id="41d7c-134">Two other mouse messages are disabled by default, but may be useful for some applications:</span></span>

-   <span data-ttu-id="41d7c-135">[**WM \_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover)：游標停留在用戶端區域上一段固定時間。</span><span class="sxs-lookup"><span data-stu-id="41d7c-135">[**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover): The cursor has hovered over the client area for a fixed period of time.</span></span>
-   <span data-ttu-id="41d7c-136">[**WM \_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave)：資料指標已離開工作區。</span><span class="sxs-lookup"><span data-stu-id="41d7c-136">[**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave): The cursor has left the client area.</span></span>

<span data-ttu-id="41d7c-137">若要啟用這些訊息，請呼叫 [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) 函數。</span><span class="sxs-lookup"><span data-stu-id="41d7c-137">To enable these messages, call the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function.</span></span>


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



<span data-ttu-id="41d7c-138">[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)結構包含函數的參數。</span><span class="sxs-lookup"><span data-stu-id="41d7c-138">The [**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent) structure contains the parameters for the function.</span></span> <span data-ttu-id="41d7c-139">結構的 **dwFlags** 成員包含位旗標，可指定您感興趣的追蹤訊息。</span><span class="sxs-lookup"><span data-stu-id="41d7c-139">The **dwFlags** member of the structure contains bit flags that specify which tracking messages you are interested in.</span></span> <span data-ttu-id="41d7c-140">您可以選擇同時取得 [**wm \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) 和 [**wm \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave)（如下所示），或只取得這兩者的其中一個。</span><span class="sxs-lookup"><span data-stu-id="41d7c-140">You can choose to get both [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) and [**WM\_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave), as shown here, or just one of the two.</span></span> <span data-ttu-id="41d7c-141">**DwHoverTime** 成員會指定在系統產生暫止訊息之前，滑鼠需要停留的時間長度。</span><span class="sxs-lookup"><span data-stu-id="41d7c-141">The **dwHoverTime** member specifies how long the mouse needs to hover before the system generates a hover message.</span></span> <span data-ttu-id="41d7c-142">以毫秒為單位提供此值。</span><span class="sxs-lookup"><span data-stu-id="41d7c-142">This value is given in milliseconds.</span></span> <span data-ttu-id="41d7c-143">常數 **停留 \_ 預設值** 表示使用系統預設值。</span><span class="sxs-lookup"><span data-stu-id="41d7c-143">The constant **HOVER\_DEFAULT** means to use the system default.</span></span>

<span data-ttu-id="41d7c-144">當您取得所要求的其中一個訊息之後， [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) 函式就會重設。</span><span class="sxs-lookup"><span data-stu-id="41d7c-144">After you get one of the messages that you requested, the [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) function resets.</span></span> <span data-ttu-id="41d7c-145">您必須再次呼叫它來取得其他追蹤訊息。</span><span class="sxs-lookup"><span data-stu-id="41d7c-145">You must call it again to get another tracking message.</span></span> <span data-ttu-id="41d7c-146">不過，您應該等到下一個滑鼠移動訊息，然後再次呼叫 **TrackMouseEvent** 。</span><span class="sxs-lookup"><span data-stu-id="41d7c-146">However, you should wait until the next mouse-move message before calling **TrackMouseEvent** again.</span></span> <span data-ttu-id="41d7c-147">否則，您的視窗可能會因為追蹤訊息而淹沒。</span><span class="sxs-lookup"><span data-stu-id="41d7c-147">Otherwise, your window might be flooded with tracking messages.</span></span> <span data-ttu-id="41d7c-148">例如，如果滑鼠暫留，系統會在滑鼠為固定時，繼續產生 [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) 訊息的資料流程。</span><span class="sxs-lookup"><span data-stu-id="41d7c-148">For example, if the mouse is hovering, the system would continue to generate a stream of [**WM\_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) messages while the mouse is stationary.</span></span> <span data-ttu-id="41d7c-149">在滑鼠移至另一個位置，並再次將滑鼠移至另一個位置時，您不需要再進行另一個 **WM \_ MOUSEHOVER**</span><span class="sxs-lookup"><span data-stu-id="41d7c-149">You don't actually want another **WM\_MOUSEHOVER** message until the mouse moves to another spot and hovers again.</span></span>

<span data-ttu-id="41d7c-150">以下是您可以用來管理滑鼠追蹤事件的小型 helper 類別。</span><span class="sxs-lookup"><span data-stu-id="41d7c-150">Here is a small helper class that you can use to manage mouse-tracking events.</span></span>


```C++
class MouseTrackEvents
{
    bool m_bMouseTracking;

public:
    MouseTrackEvents() : m_bMouseTracking(false)
    {
    }
    
    void OnMouseMove(HWND hwnd)
    {
        if (!m_bMouseTracking)
        {
            // Enable mouse tracking.
            TRACKMOUSEEVENT tme;
            tme.cbSize = sizeof(tme);
            tme.hwndTrack = hwnd;
            tme.dwFlags = TME_HOVER | TME_LEAVE;
            tme.dwHoverTime = HOVER_DEFAULT;
            TrackMouseEvent(&tme);
            m_bMouseTracking = true;
        }
    }
    void Reset(HWND hwnd)
    {
        m_bMouseTracking = false;
    }
};
```



<span data-ttu-id="41d7c-151">下一個範例顯示如何在您的視窗程式中使用這個類別。</span><span class="sxs-lookup"><span data-stu-id="41d7c-151">The next example shows how to use this class in your window procedure.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_MOUSEMOVE:
        mouseTrack.OnMouseMove(m_hwnd);  // Start tracking.

        // TODO: Handle the mouse-move message.

        return 0;

    case WM_MOUSELEAVE:

        // TODO: Handle the mouse-leave message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    case WM_MOUSEHOVER:

        // TODO: Handle the mouse-hover message.

        mouseTrack.Reset(m_hwnd);
        return 0;

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="41d7c-152">滑鼠追蹤事件需要系統進行額外的處理，因此如果您不需要，請讓它們保持停用狀態。</span><span class="sxs-lookup"><span data-stu-id="41d7c-152">Mouse tracking events require additional processing by the system, so leave them disabled if you do not need them.</span></span>

<span data-ttu-id="41d7c-153">為了提供完整的功能，以下是查詢系統是否有預設停留時間的函式。</span><span class="sxs-lookup"><span data-stu-id="41d7c-153">For completeness, here is a function that queries the system for the default hover timeout.</span></span>


```C++
UINT GetMouseHoverTime()
{
    UINT msec; 
    if (SystemParametersInfo(SPI_GETMOUSEHOVERTIME, 0, &msec, 0))
    {   
        return msec;
    }
    else
    {
        return 0;
    }
}
```



## <a name="mouse-wheel"></a><span data-ttu-id="41d7c-154">滑鼠滾輪</span><span class="sxs-lookup"><span data-stu-id="41d7c-154">Mouse Wheel</span></span>

<span data-ttu-id="41d7c-155">下列函式會檢查滑鼠滾輪是否存在。</span><span class="sxs-lookup"><span data-stu-id="41d7c-155">The following function checks if a mouse wheel is present.</span></span>


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



<span data-ttu-id="41d7c-156">如果使用者旋轉滑鼠滾輪，具有焦點的視窗就會收到 [**WM \_ 滑鼠滾輪**](/windows/desktop/inputdev/wm-mousewheel) 訊息。</span><span class="sxs-lookup"><span data-stu-id="41d7c-156">If the user rotates the mouse wheel, the window with focus receives a [**WM\_MOUSEWHEEL**](/windows/desktop/inputdev/wm-mousewheel) message.</span></span> <span data-ttu-id="41d7c-157">此訊息的 *wParam* 參數包含一個整數值，稱為 *delta* ，可測量滾輪的旋轉幅度。</span><span class="sxs-lookup"><span data-stu-id="41d7c-157">The *wParam* parameter of this message contains an integer value called the *delta* that measures how far the wheel was rotated.</span></span> <span data-ttu-id="41d7c-158">差異會使用任意單位，其中120單位定義為執行一個「動作」所需的旋轉。</span><span class="sxs-lookup"><span data-stu-id="41d7c-158">The delta uses arbitrary units, where 120 units is defined as the rotation needed to perform one "action."</span></span> <span data-ttu-id="41d7c-159">當然，動作的定義取決於您的程式。</span><span class="sxs-lookup"><span data-stu-id="41d7c-159">Of course, the definition of an action depends on your program.</span></span> <span data-ttu-id="41d7c-160">例如，如果使用滑鼠滾輪來滾動文字，每120的旋轉單位都會滾動一行文字。</span><span class="sxs-lookup"><span data-stu-id="41d7c-160">For example, if the mouse wheel is used to scroll text, each 120 units of rotation would scroll one line of text.</span></span>

<span data-ttu-id="41d7c-161">差異的正負號表示旋轉方向：</span><span class="sxs-lookup"><span data-stu-id="41d7c-161">The sign of the delta indicates the direction of rotation:</span></span>

-   <span data-ttu-id="41d7c-162">正面：向前旋轉，離開使用者。</span><span class="sxs-lookup"><span data-stu-id="41d7c-162">Positive: Rotate forward, away from the user.</span></span>
-   <span data-ttu-id="41d7c-163">負面：向使用者反向旋轉。</span><span class="sxs-lookup"><span data-stu-id="41d7c-163">Negative: Rotate backward, toward the user.</span></span>

<span data-ttu-id="41d7c-164">差異的值會放在 *wParam* 中，以及一些其他旗標。</span><span class="sxs-lookup"><span data-stu-id="41d7c-164">The value of the delta is placed in *wParam* along with some additional flags.</span></span> <span data-ttu-id="41d7c-165">使用「 [**取得 \_ 輪子 \_ DELTA \_ WPARAM**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) 」宏來取得 DELTA 的值。</span><span class="sxs-lookup"><span data-stu-id="41d7c-165">Use the [**GET\_WHEEL\_DELTA\_WPARAM**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) macro to get the value of the delta.</span></span>


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="41d7c-166">如果滑鼠滾輪的解析度很高，則差異的絕對值可能會小於120。</span><span class="sxs-lookup"><span data-stu-id="41d7c-166">If the mouse wheel has a high resolution, the absolute value of the delta might be less than 120.</span></span> <span data-ttu-id="41d7c-167">在這種情況下，如果動作以較小的增量進行，您就可以這麼做。</span><span class="sxs-lookup"><span data-stu-id="41d7c-167">In that case, if it makes sense for the action to occur in smaller increments, you can do so.</span></span> <span data-ttu-id="41d7c-168">例如，文字可能會以小於一行的遞增方式滾動。</span><span class="sxs-lookup"><span data-stu-id="41d7c-168">For example, text could scroll by increments of less than one line.</span></span> <span data-ttu-id="41d7c-169">否則，請累積總差異，直到滾輪旋轉足夠的時間來執行動作。</span><span class="sxs-lookup"><span data-stu-id="41d7c-169">Otherwise, accumulate the total delta until the wheel rotates enough to perform the action.</span></span> <span data-ttu-id="41d7c-170">將未使用的差異儲存在變數中，當120單位累積 (正或負) 時，請執行此動作。</span><span class="sxs-lookup"><span data-stu-id="41d7c-170">Store the unused delta in a variable, and when 120 units accumulate (either positive or negative), perform the action.</span></span>

## <a name="next"></a><span data-ttu-id="41d7c-171">下一個</span><span class="sxs-lookup"><span data-stu-id="41d7c-171">Next</span></span>

[<span data-ttu-id="41d7c-172">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="41d7c-172">Keyboard Input</span></span>](keyboard-input.md)

 

 