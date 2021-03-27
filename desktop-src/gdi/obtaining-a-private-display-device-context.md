---
description: 在其視窗的工作區中執行許多繪圖作業的應用程式必須使用私用顯示 DC。
ms.assetid: 9c4ed127-a88f-4946-9d7c-f77899152c31
title: 取得私人顯示裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed679ecadd694cd8781d0de8b4409fde15d22b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691859"
---
# <a name="obtaining-a-private-display-device-context"></a>取得私人顯示裝置內容

在其視窗的工作區中執行許多繪圖作業的應用程式必須使用私用顯示 DC。 若要建立這種類型的 DC，應用程式必須在註冊視窗類別時，為 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 style 成員指定 **CS \_ OWNDC** 常數。 註冊視窗類別之後，應用程式會藉由呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函式來取得識別私用顯示 DC 的控制碼。

下列範例顯示如何建立私用顯示 DC。


```C++
#include <windows.h>    // required for all Windows-based applications  
#include <stdio.h>      // C run-time header for i/o 
#include <string.h>     // C run-time header for strtok_s  
#include "dc.h"         // specific to this program  
 
// Function prototypes. 
 
BOOL InitApplication(HINSTANCE); 
long FAR PASCAL MainWndProc(HWND, UINT, UINT, LONG); 
 
// Global variables  
 
HINSTANCE hinst;       // handle to current instance  
HDC hdc;               // display device context handle  
 
BOOL InitApplication(HINSTANCE hinstance) 
{ 
    WNDCLASS  wc; 
 
    // Fill in the window class structure with parameters  
    // describing the main window.  
 
    wc.style = CS_OWNDC;         // Private-DC constant  
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
 
    wc.hIcon = LoadIcon((HINSTANCE) NULL, 
        MAKEINTRESOURCE(IDI_APPLICATION)); 
 
    wc.hCursor = LoadCursor((HINSTANCE) NULL, 
        MAKEINTRESOURCE(IDC_ARROW)); 
 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "GenericMenu"; 
    wc.lpszClassName = "GenericWClass"; 
 
    // Register the window class and return the resulting code.  
 
    return RegisterClass(&wc); 
} 
 
LRESULT APIENTRY MainWndProc( 
        HWND hwnd,           // window handle  
        UINT message,        // type of message  
        WPARAM wParam,       // additional information  
        LPARAM lParam)       // additional information  
{ 
 
    PAINTSTRUCT ps;              // paint structure  
 
    // Retrieve a handle identifying the private DC.  
 
    hdc = GetDC(hwnd); 
 
    switch (message) 
    { 
        case WM_PAINT: 
              hdc = BeginPaint(hwnd, &ps); 
 
        // Draw and paint using private DC. 
        
                 EndPaint(hwnd, &ps);
              
        case WM_DESTROY:
                     PostQuitMessage(0);
                     break;
        default:
                return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



 

 
