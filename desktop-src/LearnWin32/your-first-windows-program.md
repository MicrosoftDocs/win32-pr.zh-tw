---
title: 模組1。 您的第一個 Windows 程式
description: 模組1。 您的第一個 Windows 程式
ms.assetid: 73848144-bf02-4382-a476-7f5a35447727
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6515b012f968707379ebf24023c3d282c50d6fd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110946"
---
# <a name="module-1-your-first-windows-program"></a><span data-ttu-id="78288-105">模組1。</span><span class="sxs-lookup"><span data-stu-id="78288-105">Module 1.</span></span> <span data-ttu-id="78288-106">您的第一個 Windows 程式</span><span class="sxs-lookup"><span data-stu-id="78288-106">Your First Windows Program</span></span>

<span data-ttu-id="78288-107">在本課程模組中，我們將撰寫一個基本的 Windows 桌面程式。</span><span class="sxs-lookup"><span data-stu-id="78288-107">In this module, we will write a minimal Windows desktop program.</span></span> <span data-ttu-id="78288-108">它會建立並顯示空白視窗。</span><span class="sxs-lookup"><span data-stu-id="78288-108">All it does is create and show a blank window.</span></span> <span data-ttu-id="78288-109">第一個套裝程式含大約50行程式碼，而不是計算空白行和批註。</span><span class="sxs-lookup"><span data-stu-id="78288-109">This first program contains about 50 lines of code, not counting blank lines and comments.</span></span> <span data-ttu-id="78288-110">這會是我們的起點;稍後我們將新增圖形、文字、使用者輸入和其他功能。</span><span class="sxs-lookup"><span data-stu-id="78288-110">It will be our starting point; later we'll add graphics, text, user input, and other features.</span></span>

<span data-ttu-id="78288-111">如果您想要瞭解如何在 Visual Studio 中建立傳統 Windows 傳統型應用程式的詳細資訊，請參閱  [逐步解說：建立傳統的 Windows 桌面應用程式 (c + +) ](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019)。</span><span class="sxs-lookup"><span data-stu-id="78288-111">If you are looking for more details on how to create a traditional Windows desktop application in Visual Studio, check out  [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span>

![範例程式的螢幕擷取畫面](images/window01.png)

<span data-ttu-id="78288-113">以下是程式的完整程式碼：</span><span class="sxs-lookup"><span data-stu-id="78288-113">Here is the complete code for the program:</span></span>


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





<span data-ttu-id="78288-114">您可以從 [Windows Hello World 範例](windows-hello-world-sample.md)下載完整的 Visual Studio 專案。</span><span class="sxs-lookup"><span data-stu-id="78288-114">You can download the complete Visual Studio project from [Windows Hello World Sample](windows-hello-world-sample.md).</span></span>

<span data-ttu-id="78288-115">提供此程式碼所執行之功能的簡短大綱可能會很有用。</span><span class="sxs-lookup"><span data-stu-id="78288-115">It may be useful to give a brief outline of what this code does.</span></span> <span data-ttu-id="78288-116">稍後的主題將詳細檢查程式碼。</span><span class="sxs-lookup"><span data-stu-id="78288-116">Later topics will examine the code in detail.</span></span>

1.  <span data-ttu-id="78288-117">**wWinMain** 是程式進入點。</span><span class="sxs-lookup"><span data-stu-id="78288-117">**wWinMain** is the program entry point.</span></span> <span data-ttu-id="78288-118">當程式啟動時，它會註冊應用程式視窗行為的一些相關資訊。</span><span class="sxs-lookup"><span data-stu-id="78288-118">When the program starts, it registers some information about the behavior of the application window.</span></span> <span data-ttu-id="78288-119">其中一個最重要的專案是函式的位址， `WindowProc` 在此範例中名為。</span><span class="sxs-lookup"><span data-stu-id="78288-119">One of the most important items is the address of a function, named `WindowProc` in this example.</span></span> <span data-ttu-id="78288-120">此函式會定義視窗的行為，也就是其外觀、如何與使用者互動等等。</span><span class="sxs-lookup"><span data-stu-id="78288-120">This function defines the behavior of the window—its appearance, how it interacts with the user, and so forth.</span></span>
2.  <span data-ttu-id="78288-121">接著，程式會建立視窗，並接收可唯一識別視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="78288-121">Next, the program creates the window and receives a handle that uniquely identifies the window.</span></span>
3.  <span data-ttu-id="78288-122">如果成功建立視窗，程式就會進入 **while** 迴圈。</span><span class="sxs-lookup"><span data-stu-id="78288-122">If the window is created successfully, the program enters a **while** loop.</span></span> <span data-ttu-id="78288-123">程式會一直留在此迴圈中，直到使用者關閉視窗並結束應用程式為止。</span><span class="sxs-lookup"><span data-stu-id="78288-123">The program remains in this loop until the user closes the window and exits the application.</span></span>

<span data-ttu-id="78288-124">請注意，此程式不會明確呼叫函式 `WindowProc` ，即使我們說過，大部分的應用程式邏輯都是定義在哪裡。</span><span class="sxs-lookup"><span data-stu-id="78288-124">Notice that the program does not explicitly call the `WindowProc` function, even though we said this is where most of the application logic is defined.</span></span> <span data-ttu-id="78288-125">Windows 會藉由傳遞一系列 *訊息* 來與您的程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="78288-125">Windows communicates with your program by passing it a series of *messages*.</span></span> <span data-ttu-id="78288-126">**While** 迴圈內的程式碼會驅動此進程。</span><span class="sxs-lookup"><span data-stu-id="78288-126">The code inside the **while** loop drives this process.</span></span> <span data-ttu-id="78288-127">每次程式呼叫 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) 函式時，它會間接讓 Windows 叫用 WindowProc 函數，每個訊息一次。</span><span class="sxs-lookup"><span data-stu-id="78288-127">Each time the program calls the [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function, it indirectly causes Windows to invoke the WindowProc function, once for each message.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="78288-128">本節內容</span><span class="sxs-lookup"><span data-stu-id="78288-128">In this section</span></span>

-   [<span data-ttu-id="78288-129">建立視窗</span><span class="sxs-lookup"><span data-stu-id="78288-129">Creating a Window</span></span>](creating-a-window.md)
-   [<span data-ttu-id="78288-130">視窗訊息</span><span class="sxs-lookup"><span data-stu-id="78288-130">Window Messages</span></span>](window-messages.md)
-   [<span data-ttu-id="78288-131">撰寫視窗程式</span><span class="sxs-lookup"><span data-stu-id="78288-131">Writing the Window Procedure</span></span>](writing-the-window-procedure.md)
-   [<span data-ttu-id="78288-132">繪製視窗</span><span class="sxs-lookup"><span data-stu-id="78288-132">Painting the Window</span></span>](painting-the-window.md)
-   [<span data-ttu-id="78288-133">關閉視窗</span><span class="sxs-lookup"><span data-stu-id="78288-133">Closing the Window</span></span>](closing-the-window.md)
-   [<span data-ttu-id="78288-134">管理應用程式狀態</span><span class="sxs-lookup"><span data-stu-id="78288-134">Managing Application State</span></span>](managing-application-state-.md)

## <a name="related-topics"></a><span data-ttu-id="78288-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="78288-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78288-136">學習如何以 c + + 撰寫 Windows 程式</span><span class="sxs-lookup"><span data-stu-id="78288-136">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> <dt>

[<span data-ttu-id="78288-137">Windows Hello World 範例</span><span class="sxs-lookup"><span data-stu-id="78288-137">Windows Hello World Sample</span></span>](windows-hello-world-sample.md)
</dt> </dl>

 

 
