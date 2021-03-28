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
# <a name="drawing-at-timed-intervals"></a>以計時間隔繪製

您可以使用 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) 函式建立計時器，以計時間隔繪製。 藉由使用計時器以定期方式將 [**WM \_ 計時器**](../winmsg/wm-timer.md) 訊息傳送至視窗程式，應用程式可以在工作區中執行簡單的動畫，而其他應用程式則會繼續執行。

在下列範例中，應用程式會從用戶端區域的側邊，將星星彈跳。 每次視窗程式收到 [**WM \_ 計時器**](../winmsg/wm-timer.md) 訊息時，此程式會清除目前位置的星星、計算新的位置，並在新的位置內繪製星形。 程式會在處理 [**WM \_ 建立**](../winmsg/wm-create.md)訊息時呼叫 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)來啟動計時器。


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



此應用程式會使用私用裝置內容，將準備裝置內容以進行繪製所需的時間降到最低。 在處理 [**WM \_ 建立**](../winmsg/wm-create.md) 訊息時，視窗程式會抓取並初始化私用裝置內容，並將二元點陣作業模式設定為允許使用 [**相同的彙總函式呼叫**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) 來清除和繪製星形。 視窗程式也會將 [視口] 原點設定為允許使用同一組點繪製星形，不論用戶端區域中是否有星號的位置。

每當視窗必須更新時，應用程式就會使用 [**WM \_ 油漆**](wm-paint.md) 訊息來繪製星形。 只有在看不到星號時，視窗程式才會繪製星號;也就是說，只有當 [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) 訊息已清除它時才會這樣做。 視窗程式會攔截 **WM \_ ERASEBKGND** 訊息來設定 *fVisible* 變數，但是會將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ，讓系統可以繪製視窗背景。

應用程式會在視窗最小化時，使用 [**WM \_ 大小**](../winmsg/wm-size.md) 訊息來停止計時器，並在還原最小化的視窗時重新開機計時器。 視窗程式也會使用訊息來更新星號的目前位置（如果視窗的大小已減少），讓星星不再位於工作區中。 應用程式會使用 rcCurrent 所指定的結構來追蹤星形目前的位置，以定義星形的周框。 將矩形的所有角落保持在工作區中，會在區域中保留星號。 在處理 [**WM \_ 建立**](../winmsg/wm-create.md) 訊息時，視窗程式一開始會將星號放在工作區中。

 

 
