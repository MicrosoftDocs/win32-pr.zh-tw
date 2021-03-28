---
description: 您可以使用 SetTimer 函式建立計時器，以計時間隔繪製。
ms.assetid: 82f9aa5e-8e42-49cf-bcd0-785bc78fe159
title: 以計時間隔繪製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1757aca4e6be8f169aea378c52038420519ee879
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512900"
---
# <a name="drawing-at-timed-intervals"></a><span data-ttu-id="74b64-103">以計時間隔繪製</span><span class="sxs-lookup"><span data-stu-id="74b64-103">Drawing at Timed Intervals</span></span>

<span data-ttu-id="74b64-104">您可以使用 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) 函式建立計時器，以計時間隔繪製。</span><span class="sxs-lookup"><span data-stu-id="74b64-104">You can draw at timed intervals by creating a timer with the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function.</span></span> <span data-ttu-id="74b64-105">藉由使用計時器以定期方式將 [**WM \_ 計時器**](../winmsg/wm-timer.md) 訊息傳送至視窗程式，應用程式可以在工作區中執行簡單的動畫，而其他應用程式則會繼續執行。</span><span class="sxs-lookup"><span data-stu-id="74b64-105">By using a timer to send [**WM\_TIMER**](../winmsg/wm-timer.md) messages to the window procedure at regular intervals, an application can carry out simple animation in the client area while other applications continue running.</span></span>

<span data-ttu-id="74b64-106">在下列範例中，應用程式會從用戶端區域的側邊，將星星彈跳。</span><span class="sxs-lookup"><span data-stu-id="74b64-106">In the following example, the application bounces a star from side to side in the client area.</span></span> <span data-ttu-id="74b64-107">每次視窗程式收到 [**WM \_ 計時器**](../winmsg/wm-timer.md) 訊息時，此程式會清除目前位置的星星、計算新的位置，並在新的位置內繪製星形。</span><span class="sxs-lookup"><span data-stu-id="74b64-107">Each time the window procedure receives a [**WM\_TIMER**](../winmsg/wm-timer.md) message, the procedure erases the star at the current position, calculates a new position, and draws the star within the new position.</span></span> <span data-ttu-id="74b64-108">程式會在處理 [**WM \_ 建立**](../winmsg/wm-create.md)訊息時呼叫 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)來啟動計時器。</span><span class="sxs-lookup"><span data-stu-id="74b64-108">The procedure starts the timer by calling [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) while processing the [**WM\_CREATE**](../winmsg/wm-create.md) message.</span></span>


```C++
RECT rcCurrent = {0,0,20,20}; 
POINT aptStar[6] = {10,1, 1,19, 19,6, 1,6, 19,19, 10,1}; 
int X = 2, Y = -1, idTimer = -1; 
BOOL fVisible = FALSE; 
HDC hdc; 
 
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    RECT rc; 
 
    switch (message) 
    { 
        case WM_CREATE: 
 
            // Calculate the starting point.  
 
            GetClientRect(hwnd, &rc); 
            OffsetRect(&rcCurrent, rc.right / 2, rc.bottom / 2); 
 
            // Initialize the private DC.  
 
            hdc = GetDC(hwnd); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            SetROP2(hdc, R2_NOT); 
 
            // Start the timer.  
 
            SetTimer(hwnd, idTimer = 1, 10, NULL); 
            return 0L; 
 
        case WM_DESTROY: 
            KillTimer(hwnd, 1); 
            PostQuitMessage(0); 
            return 0L; 
 
        case WM_SIZE: 
            switch (wParam) 
            { 
                case SIZE_MINIMIZED: 
 
                    // Stop the timer if the window is minimized. 
 
                    KillTimer(hwnd, 1); 
                    idTimer = -1; 
                    break; 
 
                case SIZE_RESTORED: 
 
                    // Move the star back into the client area  
                    // if necessary.  
 
                    if (rcCurrent.right > (int) LOWORD(lParam)) 
                    {
                        rcCurrent.left = 
                            (rcCurrent.right = 
                                (int) LOWORD(lParam)) - 20; 
                    }
                    if (rcCurrent.bottom > (int) HIWORD(lParam)) 
                    {
                        rcCurrent.top = 
                            (rcCurrent.bottom = 
                                (int) HIWORD(lParam)) - 20; 
                    }
 
                    // Fall through to the next case.  
 
                case SIZE_MAXIMIZED: 
 
                    // Start the timer if it had been stopped.  
 
                    if (idTimer == -1) 
                        SetTimer(hwnd, idTimer = 1, 10, NULL); 
                    break; 
            } 
            return 0L; 
 
        case WM_TIMER: 
 
            // Hide the star if it is visible.  
 
            if (fVisible) 
                Polyline(hdc, aptStar, 6); 
 
            // Bounce the star off a side if necessary.  
 
            GetClientRect(hwnd, &rc); 
            if (rcCurrent.left + X < rc.left || 
                rcCurrent.right + X > rc.right) 
                X = -X; 
            if (rcCurrent.top + Y < rc.top || 
                rcCurrent.bottom + Y > rc.bottom) 
                Y = -Y; 
 
            // Show the star in its new position.  
 
            OffsetRect(&rcCurrent, X, Y); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            fVisible = Polyline(hdc, aptStar, 6); 
 
            return 0L; 
 
        case WM_ERASEBKGND: 
 
            // Erase the star.  
 
            fVisible = FALSE; 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
        case WM_PAINT: 
 
            // Show the star if it is not visible. Use BeginPaint  
            // to clear the update region.  
 
            BeginPaint(hwnd, &ps); 
            if (!fVisible) 
                fVisible = Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
    } 
    return DefWindowProc(hwnd, message, wParam, lParam); 
} 
```



<span data-ttu-id="74b64-109">此應用程式會使用私用裝置內容，將準備裝置內容以進行繪製所需的時間降到最低。</span><span class="sxs-lookup"><span data-stu-id="74b64-109">This application uses a private device context to minimize the time required to prepare the device context for drawing.</span></span> <span data-ttu-id="74b64-110">在處理 [**WM \_ 建立**](../winmsg/wm-create.md) 訊息時，視窗程式會抓取並初始化私用裝置內容，並將二元點陣作業模式設定為允許使用 [**相同的彙總函式呼叫**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) 來清除和繪製星形。</span><span class="sxs-lookup"><span data-stu-id="74b64-110">The window procedure retrieves and initializes the private device context when processing the [**WM\_CREATE**](../winmsg/wm-create.md) message, setting the binary raster operation mode to allow the star to be erased and drawn using the same call to the [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) function.</span></span> <span data-ttu-id="74b64-111">視窗程式也會將 [視口] 原點設定為允許使用同一組點繪製星形，不論用戶端區域中是否有星號的位置。</span><span class="sxs-lookup"><span data-stu-id="74b64-111">The window procedure also sets the viewport origin to allow the star to be drawn using the same set of points regardless of the star's position in the client area.</span></span>

<span data-ttu-id="74b64-112">每當視窗必須更新時，應用程式就會使用 [**WM \_ 油漆**](wm-paint.md) 訊息來繪製星形。</span><span class="sxs-lookup"><span data-stu-id="74b64-112">The application uses the [**WM\_PAINT**](wm-paint.md) message to draw the star whenever the window must be updated.</span></span> <span data-ttu-id="74b64-113">只有在看不到星號時，視窗程式才會繪製星號;也就是說，只有當 [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) 訊息已清除它時才會這樣做。</span><span class="sxs-lookup"><span data-stu-id="74b64-113">The window procedure draws the star only if it is not visible; that is, only if it has been erased by the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message.</span></span> <span data-ttu-id="74b64-114">視窗程式會攔截 **WM \_ ERASEBKGND** 訊息來設定 *fVisible* 變數，但是會將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ，讓系統可以繪製視窗背景。</span><span class="sxs-lookup"><span data-stu-id="74b64-114">The window procedure intercepts the **WM\_ERASEBKGND** message to set the *fVisible* variable, but passes the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) so that the system can draw the window background.</span></span>

<span data-ttu-id="74b64-115">應用程式會在視窗最小化時，使用 [**WM \_ 大小**](../winmsg/wm-size.md) 訊息來停止計時器，並在還原最小化的視窗時重新開機計時器。</span><span class="sxs-lookup"><span data-stu-id="74b64-115">The application uses the [**WM\_SIZE**](../winmsg/wm-size.md) message to stop the timer when the window is minimized and to restart the timer when the minimized window is restored.</span></span> <span data-ttu-id="74b64-116">視窗程式也會使用訊息來更新星號的目前位置（如果視窗的大小已減少），讓星星不再位於工作區中。</span><span class="sxs-lookup"><span data-stu-id="74b64-116">The window procedure also uses the message to update the current position of the star if the size of the window has been reduced so that the star is no longer in the client area.</span></span> <span data-ttu-id="74b64-117">應用程式會使用 rcCurrent 所指定的結構來追蹤星形目前的位置，以定義星形的周框。</span><span class="sxs-lookup"><span data-stu-id="74b64-117">The application keeps track of the star's current position by using the structure specified by rcCurrent, which defines the bounding rectangle for the star.</span></span> <span data-ttu-id="74b64-118">將矩形的所有角落保持在工作區中，會在區域中保留星號。</span><span class="sxs-lookup"><span data-stu-id="74b64-118">Keeping all corners of the rectangle in the client area keeps the star in the area.</span></span> <span data-ttu-id="74b64-119">在處理 [**WM \_ 建立**](../winmsg/wm-create.md) 訊息時，視窗程式一開始會將星號放在工作區中。</span><span class="sxs-lookup"><span data-stu-id="74b64-119">The window procedure initially centers the star in the client area when processing the [**WM\_CREATE**](../winmsg/wm-create.md) message.</span></span>

 

 
