---
description: 您可以繪製自己的最小化視窗，而不是讓系統為您繪製。
ms.assetid: 607d987a-5bdc-46bc-bde7-6dc52745ac79
title: 繪製最小化視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced1f3205243ea098856517590d58caee851329a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386175"
---
# <a name="drawing-a-minimized-window"></a>繪製最小化視窗

您可以繪製自己的最小化視窗，而不是讓系統為您繪製。 大部分的應用程式會在註冊視窗的視窗類別時定義類別圖示，而系統則會在視窗最小化時繪製圖示。 但是，如果您將類別圖示設定為 **Null**，系統會在視窗最小化時，將 [**WM \_ 油漆**](wm-paint.md) 訊息傳送至您的視窗程式，讓視窗程式在最小化視窗中繪製。

在下列範例中，視窗程式會在最小化的視窗中繪製星形。 此程式會使用 [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) 函式來判斷何時最小化視窗。 這可確保只有在視窗最小化時，才會繪製星號。


```C++
POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
  . 
  . 
  . 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
 
    // Determine whether the window is minimized.  
 
    if (IsIconic(hwnd)) 
    { 
        GetClientRect(hwnd, &rc); 
        SetMapMode(hdc, MM_ANISOTROPIC); 
        SetWindowExtEx(hdc, 100, 100, NULL); 
        SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
        Polyline(hdc, aptStar, 6); 
    } 
    else 
    { 
        TextOut(hdc, 0,0, "Hello, Windows!", 15); 
    } 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



您可以藉由將 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **hIcon** 成員設定為 **null** ，然後再呼叫 window 類別的 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)函式，將類別圖示設定為 **null** 。

 

 
