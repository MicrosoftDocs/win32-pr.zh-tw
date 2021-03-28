---
description: 您可以設定 \_ 視窗類別的 cs HREDRAW 和 cs VREDRAW 樣式，讓應用程式在視窗變更大小時，重繪工作區的整個內容 \_ 。
ms.assetid: ed68b85e-8382-4450-b07d-0422b44dc2e3
title: 重繪整個工作區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67640d1b464173755029bef1d0feb91f215cda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991162"
---
# <a name="redrawing-the-entire-client-area"></a>重繪整個工作區

您可以設定 \_ 視窗類別的 cs HREDRAW 和 cs VREDRAW 樣式，讓應用程式在視窗變更大小時，重繪工作區的整個內容 \_ 。 根據視窗大小調整繪圖大小的應用程式會使用這些樣式，確保它們在繪製時以完全空白的用戶端區域開始。

在下列範例中，視窗程式會繪製在工作區中整齊的五指向星形。 它會使用一般裝置內容，而且必須在每次處理 [**WM \_ 繪製**](wm-paint.md) 訊息時，設定對應模式以及視窗和視口範圍。


```C++
LRESULT APIENTRY WndProc(HWMD hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
    RECT rc; 
    POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
    . 
    . 
    . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            GetClientRect(hwnd, &rc); 
            SetMapMode(hdc, MM_ANISOTROPIC); 
            SetWindowExtEx(hdc, 100, 100, NULL); 
            SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
            Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
        . 
        . 
        . 
} 
 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    WNDCLASS wc; 
 
    . 
    . 
    . 
 
        wc.style = CS_HREDRAW | CS_VREDRAW; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
 
    . 
    . 
    . 
 
        RegisterClass(&wc); 
 
    . 
    . 
    . 
 
    return msg.wParam; 
} 
```



 

 



