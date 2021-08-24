---
description: 您可以使用 BeginPaint 和 EndPaint 函數來準備和完成工作區中的繪圖。
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: 在工作區中繪圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d01331ae60a7814602f6c10c0d9109ae665da39aa140223e31ac03303048b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832018"
---
# <a name="drawing-in-the-client-area"></a>在工作區中繪圖

您可以使用 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 和 [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) 函數來準備和完成工作區中的繪圖。 **BeginPaint** 會將控制碼傳回給在工作區中用於繪圖的顯示裝置內容; **EndPaint** 會結束繪製要求並釋放裝置內容。

在下列範例中，視窗程式會將 "Hello，Windows！" 訊息寫入 在工作區中。 為了確定在第一次建立視窗時可以看到字串， [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 函式會在建立並顯示視窗之後立即呼叫 [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) 。 這會導致 [**WM \_ 油漆**](wm-paint.md) 訊息立即傳送至視窗程式。


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



 

 
