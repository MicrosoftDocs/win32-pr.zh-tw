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
# <a name="miscellaneous-mouse-operations"></a>其他滑鼠操作

前幾節已討論過滑鼠點擊和滑鼠移動。 以下是一些可以使用滑鼠來執行的其他作業。

## <a name="dragging-ui-elements"></a>拖曳 UI 元素

如果您的 UI 支援拖曳 UI 專案，則您應該在滑鼠左鍵的訊息處理常式中呼叫另一個函數： [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect)。 如果使用者起始應解釋為拖曳的滑鼠手勢， **DragDetect** 函式會傳回 **TRUE** 。 下列程式碼示範如何使用此函式。


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



以下是概念：當某個程式支援拖放時，您不希望每個滑鼠點擊都能以拖曳的方式轉譯。 否則，當使用者只是想要按一下它時，使用者可能會不小心拖曳某個東西 (例如，將它選取) 。 但是，如果滑鼠特別敏感，則在按一下時，可能很難讓滑鼠保持完美。 因此，Windows 會定義一些圖元的拖曳臨界值。 當使用者按下滑鼠按鍵時，除非滑鼠超過此臨界值，否則不會將它視為拖曳。 [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect)函式會測試是否達到此臨界值。 如果函式傳回 **TRUE**，您可以將滑鼠按一下的方式解讀為拖曳。 否則，請不要這麼做。

> [!Note]  
> 如果 [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) 傳回 **FALSE**，則當使用者放開滑鼠按鍵時，Windows 會隱藏 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) 訊息。 因此，除非您的程式目前處於支援拖曳的模式，否則請勿呼叫 **DragDetect** 。  (例如，如果已選取可拖曳的 UI 元素。在此課程模組結束時 ) ，我們會看到使用 **DragDetect** 函式的較長程式碼範例。

 

## <a name="confining-the-cursor"></a>將資料指標

有時候您可能會想要將游標限制在工作區或工作區的一部分。 [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor)函式會將資料指標的移動限制為指定的矩形。 這個矩形是以螢幕座標（而不是用戶端座標）來提供，因此點 (0，0) 表示畫面的左上角。 若要將用戶端座標轉譯為螢幕座標，請呼叫函式 [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen)。

下列程式碼會將游標範圍設為視窗的工作區。


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



[**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) 會採用 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構，但 [**ClientToScreen**](/windows/desktop/api/winuser/nf-winuser-clienttoscreen) 會採用 [**點**](/previous-versions//dd162805(v=vs.85)) 結構。 矩形是由左上角和右下角的點所定義。 您可以將資料指標限制為任何矩形區域（包括視窗以外的區域），但是將游標將到工作區是使用函式的典型方式。 將游標將至範圍外的整個區域會是不尋常的，使用者可能會察覺到它是錯誤。

若要移除限制，請使用值 **Null** 來呼叫 [**ClipCursor**](/windows/desktop/api/winuser/nf-winuser-clipcursor) 。


```C++
ClipCursor(NULL);
```



## <a name="mouse-tracking-events-hover-and-leave"></a>滑鼠追蹤事件：停留並離開

預設會停用其他兩個滑鼠訊息，但對某些應用程式而言可能很有用：

-   [**WM \_MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover)：游標停留在用戶端區域上一段固定時間。
-   [**WM \_MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave)：資料指標已離開工作區。

若要啟用這些訊息，請呼叫 [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) 函數。


```C++
    TRACKMOUSEEVENT tme;
    tme.cbSize = sizeof(tme);
    tme.hwndTrack = hwnd;
    tme.dwFlags = TME_HOVER | TME_LEAVE;
    tme.dwHoverTime = HOVER_DEFAULT;
    TrackMouseEvent(&tme);
```



[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)結構包含函數的參數。 結構的 **dwFlags** 成員包含位旗標，可指定您感興趣的追蹤訊息。 您可以選擇同時取得 [**wm \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) 和 [**wm \_ MOUSELEAVE**](/windows/desktop/inputdev/wm-mouseleave)（如下所示），或只取得這兩者的其中一個。 **DwHoverTime** 成員會指定在系統產生暫止訊息之前，滑鼠需要停留的時間長度。 以毫秒為單位提供此值。 常數 **停留 \_ 預設值** 表示使用系統預設值。

當您取得所要求的其中一個訊息之後， [**TrackMouseEvent**](/windows/desktop/api/winuser/nf-winuser-trackmouseevent) 函式就會重設。 您必須再次呼叫它來取得其他追蹤訊息。 不過，您應該等到下一個滑鼠移動訊息，然後再次呼叫 **TrackMouseEvent** 。 否則，您的視窗可能會因為追蹤訊息而淹沒。 例如，如果滑鼠暫留，系統會在滑鼠為固定時，繼續產生 [**WM \_ MOUSEHOVER**](/windows/desktop/inputdev/wm-mousehover) 訊息的資料流程。 在滑鼠移至另一個位置，並再次將滑鼠移至另一個位置時，您不需要再進行另一個 **WM \_ MOUSEHOVER**

以下是您可以用來管理滑鼠追蹤事件的小型 helper 類別。


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



下一個範例顯示如何在您的視窗程式中使用這個類別。


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



滑鼠追蹤事件需要系統進行額外的處理，因此如果您不需要，請讓它們保持停用狀態。

為了提供完整的功能，以下是查詢系統是否有預設停留時間的函式。


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



## <a name="mouse-wheel"></a>滑鼠滾輪

下列函式會檢查滑鼠滾輪是否存在。


```C++
BOOL IsMouseWheelPresent()
{
    return (GetSystemMetrics(SM_MOUSEWHEELPRESENT) != 0);
}
```



如果使用者旋轉滑鼠滾輪，具有焦點的視窗就會收到 [**WM \_ 滑鼠滾輪**](/windows/desktop/inputdev/wm-mousewheel) 訊息。 此訊息的 *wParam* 參數包含一個整數值，稱為 *delta* ，可測量滾輪的旋轉幅度。 差異會使用任意單位，其中120單位定義為執行一個「動作」所需的旋轉。 當然，動作的定義取決於您的程式。 例如，如果使用滑鼠滾輪來滾動文字，每120的旋轉單位都會滾動一行文字。

差異的正負號表示旋轉方向：

-   正面：向前旋轉，離開使用者。
-   負面：向使用者反向旋轉。

差異的值會放在 *wParam* 中，以及一些其他旗標。 使用「 [**取得 \_ 輪子 \_ DELTA \_ WPARAM**](/windows/desktop/api/winuser/nf-winuser-get_wheel_delta_wparam) 」宏來取得 DELTA 的值。


```C++
int delta = GET_WHEEL_DELTA_WPARAM(wParam);
```



如果滑鼠滾輪的解析度很高，則差異的絕對值可能會小於120。 在這種情況下，如果動作以較小的增量進行，您就可以這麼做。 例如，文字可能會以小於一行的遞增方式滾動。 否則，請累積總差異，直到滾輪旋轉足夠的時間來執行動作。 將未使用的差異儲存在變數中，當120單位累積 (正或負) 時，請執行此動作。

## <a name="next"></a>下一個

[鍵盤輸入](keyboard-input.md)

 

 