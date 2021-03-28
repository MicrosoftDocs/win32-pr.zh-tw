---
description: 您可以繪製自己的視窗背景，而不是讓系統為您繪製。
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: 繪製自訂視窗背景
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a88bec680a6f35e84f5444fc90a45f98da533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972697"
---
# <a name="drawing-a-custom-window-background"></a>繪製自訂視窗背景

您可以繪製自己的視窗背景，而不是讓系統為您繪製。 大部分的應用程式會在註冊視窗類別時，指定類別背景筆刷的筆刷控制碼或系統色彩值;系統會使用筆刷或色彩來繪製背景。 但是，如果您將類別背景筆刷設定為 **Null**，系統就會在每次必須繪製視窗背景時，將 [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) 訊息傳送至您的視窗程式，讓您繪製自訂背景。

在下列範例中，視窗程式會繪製一個在視窗中整齊的大型棋盤圖樣。 此程式會使用白色筆刷來填滿工作區，然後使用灰色筆刷繪製 13 20 到20個矩形。 繪製背景時要使用的顯示裝置內容，是在訊息的 *wParam* 參數中指定。


```C++
HBRUSH hbrWhite, hbrGray; 
 
  . 
  . 
  . 
 
case WM_CREATE: 
    hbrWhite = GetStockObject(WHITE_BRUSH); 
    hbrGray  = GetStockObject(GRAY_BRUSH); 
    return 0L; 
 
case WM_ERASEBKGND: 
    hdc = (HDC) wParam; 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    FillRect(hdc, &rc, hbrWhite); 
 
    for (i = 0; i < 13; i++) 
    { 
        x = (i * 40) % 100; 
        y = ((i * 40) / 100) * 20; 
        SetRect(&rc, x, y, x + 20, y + 20); 
        FillRect(hdc, &rc, hbrGray); 
    } 
  return 1L; 
```



如果應用程式繪製自己的最小化視窗，系統也會將 [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) 訊息傳送至視窗程式，以繪製最小化視窗的背景。 您可以使用 [**WM \_ 油漆**](wm-paint.md) 所使用的相同技術來判斷視窗是否最小化，也就是呼叫 [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) 函式，並檢查傳回值 **TRUE**。

 

 
