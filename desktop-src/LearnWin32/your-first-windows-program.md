---
title: 模組1。 您的第一個 Windows 計畫
description: 模組1。 您的第一個 Windows 計畫
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e09b4caf81f3498a5c36eaaf0dbc3a95f52f7dd2ba8c64d0f0f9b53d19fe2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086438"
---
# <a name="module-1-your-first-windows-program"></a>模組1。 您的第一個 Windows 計畫

在本課程模組中，我們將撰寫一個基本的 Windows 桌上型電腦程式。 它會建立並顯示空白視窗。 第一個套裝程式含大約50行程式碼，而不是計算空白行和批註。 這會是我們的起點;稍後我們將新增圖形、文字、使用者輸入和其他功能。

如果您想要瞭解如何在 Visual Studio 中建立傳統 Windows 桌面應用程式的詳細資訊，請參閱[逐步解說：建立傳統 Windows 桌面應用程式 (c + +) ](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019)。

![範例程式的螢幕擷取畫面](images/window01.png)

以下是程式的完整程式碼：


```C++
#ifndef UNICODE
#define UNICODE
#endif 

#include <windows.h>

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow)
{
    // Register the window class.
    const wchar_t CLASS_NAME[]  = L"Sample Window Class";
    
    WNDCLASS wc = { };

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = hInstance;
    wc.lpszClassName = CLASS_NAME;

    RegisterClass(&wc);

    // Create the window.

    HWND hwnd = CreateWindowEx(
        0,                              // Optional window styles.
        CLASS_NAME,                     // Window class
        L"Learn to Program Windows",    // Window text
        WS_OVERLAPPEDWINDOW,            // Window style

        // Size and position
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

        NULL,       // Parent window    
        NULL,       // Menu
        hInstance,  // Instance handle
        NULL        // Additional application data
        );

    if (hwnd == NULL)
    {
        return 0;
    }

    ShowWindow(hwnd, nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);



            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));

            EndPaint(hwnd, &ps);
        }
        return 0;

    }
    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}
```





您可以從[Windows Hello World 範例](windows-hello-world-sample.md)下載完整的 Visual Studio 專案。

提供此程式碼所執行之功能的簡短大綱可能會很有用。 稍後的主題將詳細檢查程式碼。

1.  **wWinMain** 是程式進入點。 當程式啟動時，它會註冊應用程式視窗行為的一些相關資訊。 其中一個最重要的專案是函式的位址， `WindowProc` 在此範例中名為。 此函式會定義視窗的行為，也就是其外觀、如何與使用者互動等等。
2.  接著，程式會建立視窗，並接收可唯一識別視窗的控制碼。
3.  如果成功建立視窗，程式就會進入 **while** 迴圈。 程式會一直留在此迴圈中，直到使用者關閉視窗並結束應用程式為止。

請注意，此程式不會明確呼叫函式 `WindowProc` ，即使我們說過，大部分的應用程式邏輯都是定義在哪裡。 Windows 藉由傳遞一系列 *訊息* 來與您的程式進行通訊。 **While** 迴圈內的程式碼會驅動此進程。 每次程式呼叫 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)函式時，它會間接導致 Windows 叫用 WindowProc 函數，每個訊息一次。

## <a name="in-this-section"></a>本節內容

-   [建立視窗](creating-a-window.md)
-   [視窗訊息](window-messages.md)
-   [撰寫視窗程式](writing-the-window-procedure.md)
-   [繪製視窗](painting-the-window.md)
-   [關閉視窗](closing-the-window.md)
-   [管理應用程式狀態](managing-application-state-.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[瞭解如何以 c + + 撰寫 Windows 程式](learn-to-program-for-windows.md)
</dt> <dt>

[Windows Hello世界範例](windows-hello-world-sample.md)
</dt> </dl>

 

 
