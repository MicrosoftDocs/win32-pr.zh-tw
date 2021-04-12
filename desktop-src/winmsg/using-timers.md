---
description: 本主題說明如何建立和終結計時器，以及如何使用計時器以指定的間隔來陷印滑鼠輸入。
ms.assetid: eee54078-759f-4fd4-9cf4-10a8bde888b7
title: 使用計時器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c6479aca9d5394c2ad9ade87dd77b1474f31f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320248"
---
# <a name="using-timers"></a>使用計時器

本主題說明如何建立和終結計時器，以及如何使用計時器以指定的間隔來陷印滑鼠輸入。

本主題包含下列各節。

-   [建立計時器](#creating-a-timer)
-   [終結計時器](#destroying-a-timer)
-   [使用計時器函式來陷印滑鼠輸入](#using-timer-functions-to-trap-mouse-input)
-   [相關主題](#related-topics)

## <a name="creating-a-timer"></a>建立計時器

下列範例會使用 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) 函數來建立兩個計時器。 第一個計時器會設定為每隔10秒，第二個計時器為每五分鐘一次。


```
// Set two timers. 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER1,            // timer identifier 
    10000,                 // 10-second interval 
    (TIMERPROC) NULL);     // no timer callback 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER2,            // timer identifier 
    300000,                // five-minute interval 
    (TIMERPROC) NULL);     // no timer callback 
```



若要處理這些計時器產生的 [**wm \_ 計時器**](wm-timer.md) 訊息，請將 **wm \_ 計時器** case 語句新增至 *hwnd* 參數的視窗程式。


```
case WM_TIMER: 
 
    switch (wParam) 
    { 
        case IDT_TIMER1: 
            // process the 10-second timer 
 
             return 0; 
 
        case IDT_TIMER2: 
            // process the five-minute timer 

            return 0; 
    } 
```



應用程式也可以建立其 [**WM \_ 計時器**](wm-timer.md) 訊息不是由主視窗程式處理，而是由應用程式定義的回呼函式處理的計時器，如下列程式碼範例所示，它會建立計時器並使用回呼函式 **MyTimerProc** 來處理計時器的 **WM \_ 計時器** 訊息。


```
// Set the timer. 
 
SetTimer(hwnd,                // handle to main window 
    IDT_TIMER3,               // timer identifier 
    5000,                     // 5-second interval 
    (TIMERPROC) MyTimerProc); // timer callback
```



**MyTimerProc** 的呼叫慣例必須以 [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc)回呼函數為基礎。

如果您的應用程式在未指定視窗控制碼的情況下建立計時器，則您的應用程式必須監視適用于 [**WM \_ 計時器**](wm-timer.md) 訊息的訊息佇列，並將其分派至適當的視窗。


```
HWND hwndTimer;   // handle to window for timer messages 
MSG msg;          // message structure 
 
    while (GetMessage(&msg, // message structure 
            NULL,           // handle to window to receive the message 
               0,           // lowest message to examine 
               0))          // highest message to examine 
    { 
 
        // Post WM_TIMER messages to the hwndTimer procedure. 
 
        if (msg.message == WM_TIMER) 
        { 
            msg.hwnd = hwndTimer; 
        } 
 
        TranslateMessage(&msg); // translates virtual-key codes 
        DispatchMessage(&msg);  // dispatches message to window 
    } 
```



## <a name="destroying-a-timer"></a>終結計時器

應用程式應該使用 [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) 函式來摧毀不再需要的計時器。 下列範例會終結常數所識別的計時器 IDT \_ TIMER1、IDT \_ TIMER2 和 IDT \_ TIMER3。


```
// Destroy the timers. 
 
KillTimer(hwnd, IDT_TIMER1); 
KillTimer(hwnd, IDT_TIMER2); 
KillTimer(hwnd, IDT_TIMER3); 
```



## <a name="using-timer-functions-to-trap-mouse-input"></a>使用計時器函式來陷印滑鼠輸入

有時候，當您在螢幕上有滑鼠指標時，就必須避免更多輸入。 完成此動作的其中一種方法是建立特殊的常式，以在發生特定事件之前，先將滑鼠輸入設陷。 許多開發人員將此常式稱為「建立 mousetrap」。

下列範例會使用 [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) 和 [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) 函式來捕捉滑鼠輸入。 **SetTimer** 會建立每10秒傳送一次 [**WM \_ 計時器**](wm-timer.md) 訊息的計時器。 每次應用程式收到 **WM \_ 計時器** 訊息時，就會記錄滑鼠指標位置。 如果目前的位置與先前的位置相同，而且應用程式的主視窗最小化，則應用程式會將滑鼠指標移至圖示。 當應用程式關閉時， **KillTimer** 會停止計時器。


```
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
UINT uResult;               // SetTimer's return value 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the initial cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,             // handle to main window 
    IDT_MOUSETRAP,                   // timer identifier 
    10000,                           // 10-second interval 
    (TIMERPROC) NULL);               // no timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM  lParam)     // additional information 
{ 
 
    HDC hdc;        // handle to device context 
    POINT pt;       // current cursor location 
    RECT rc;        // location of minimized window 
 
    switch (message) 
    { 
        //
        // Process other messages. 
        // 
 
        case WM_TIMER: 
        // If the window is minimized, compare the current 
        // cursor position with the one from 10 seconds 
        // earlier. If the cursor position has not changed, 
        // move the cursor to the icon. 
 
            if (IsIconic(hwnd)) 
            { 
                GetCursorPos(&pt); 
 
                if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
                { 
                    GetWindowRect(hwnd, &rc); 
                    SetCursorPos(rc.left, rc.top); 
                } 
                else 
                { 
                    ptOld.x = pt.x; 
                    ptOld.y = pt.y; 
                } 
            } 
 
            return 0; 
 
        case WM_DESTROY: 
 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
```



雖然下列範例也會示範如何捕捉滑鼠輸入，但它會透過應用程式定義的回呼函式 **MyTimerProc** 來處理 [**WM \_ 計時器**](wm-timer.md)訊息，而不是透過應用程式的訊息佇列。


```
UINT uResult;               // SetTimer's return value 
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the current cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,      // handle to main window 
    IDT_MOUSETRAP,            // timer identifier 
    10000,                    // 10-second interval 
    (TIMERPROC) MyTimerProc); // timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM   lParam)    // additional information 
{ 
 
    HDC hdc;            // handle to device context 
 
    switch (message) 
    { 
    // 
    // Process other messages. 
    // 
 
        case WM_DESTROY: 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
 
// MyTimerProc is an application-defined callback function that 
// processes WM_TIMER messages. 
 
VOID CALLBACK MyTimerProc( 
    HWND hwnd,        // handle to window for timer messages 
    UINT message,     // WM_TIMER message 
    UINT idTimer,     // timer identifier 
    DWORD dwTime)     // current system time 
{ 
 
    RECT rc; 
    POINT pt; 
 
    // If the window is minimized, compare the current 
    // cursor position with the one from 10 seconds earlier. 
    // If the cursor position has not changed, move the 
    // cursor to the icon. 
 
    if (IsIconic(hwnd)) 
    { 
        GetCursorPos(&pt); 
 
        if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
        { 
            GetWindowRect(hwnd, &rc); 
            SetCursorPos(rc.left, rc.top); 
        } 
        else 
        { 
            ptOld.x = pt.x; 
            ptOld.y = pt.y; 
        } 
    } 
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於計時器](about-timers.md)
</dt> </dl>

 

 
