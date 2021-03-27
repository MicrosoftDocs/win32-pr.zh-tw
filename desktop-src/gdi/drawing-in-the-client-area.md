---
description: 您可以使用 BeginPaint 和 EndPaint 函數來準備和完成工作區中的繪圖。
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: 在工作區中繪圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e14c8492a11a7ad9764416b2453cea3264fbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848558"
---
# <a name="drawing-in-the-client-area"></a><span data-ttu-id="30595-103">在工作區中繪圖</span><span class="sxs-lookup"><span data-stu-id="30595-103">Drawing in the Client Area</span></span>

<span data-ttu-id="30595-104">您可以使用 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 和 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) 函數來準備和完成工作區中的繪圖。</span><span class="sxs-lookup"><span data-stu-id="30595-104">You use the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) functions to prepare for and complete the drawing in the client area.</span></span> <span data-ttu-id="30595-105">**BeginPaint** 會將控制碼傳回給在工作區中用於繪圖的顯示裝置內容; **EndPaint** 會結束繪製要求並釋放裝置內容。</span><span class="sxs-lookup"><span data-stu-id="30595-105">**BeginPaint** returns a handle to the display device context used for drawing in the client area; **EndPaint** ends the paint request and releases the device context.</span></span>

<span data-ttu-id="30595-106">在下列範例中，視窗程式會將 "Hello，Windows！" 訊息寫入</span><span class="sxs-lookup"><span data-stu-id="30595-106">In the following example, the window procedure writes the message "Hello, Windows!"</span></span> <span data-ttu-id="30595-107">在工作區中。</span><span class="sxs-lookup"><span data-stu-id="30595-107">in the client area.</span></span> <span data-ttu-id="30595-108">為了確定在第一次建立視窗時可以看到字串， [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 函式會在建立並顯示視窗之後立即呼叫 [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) 。</span><span class="sxs-lookup"><span data-stu-id="30595-108">To make sure the string is visible when the window is first created, the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function calls [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) immediately after creating and showing the window.</span></span> <span data-ttu-id="30595-109">這會導致 [**WM \_ 油漆**](wm-paint.md) 訊息立即傳送至視窗程式。</span><span class="sxs-lookup"><span data-stu-id="30595-109">This causes a [**WM\_PAINT**](wm-paint.md) message to be sent immediately to the window procedure.</span></span>


```C++
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
 
    switch (message) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            TextOut(hdc, 0, 0, "Hello, Windows!", 15); 
            EndPaint(hwnd, &ps); 
            return 0L; 

        // Process other messages.   
    } 
} 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    HWND hwnd; 
 
    hwnd = CreateWindowEx( 
        // parameters  
        ); 
 
    ShowWindow(hwnd, SW_SHOW); 
    UpdateWindow(hwnd); 
 
    return msg.wParam; 
} 
```



 

 
