---
title: 延展影像和視窗
description: 延展影像和視窗
ms.assetid: 661992eb-b012-47eb-84bc-cd12834c6270
keywords:
- MCIWndGetDest 宏
- MCIWndPutDest 宏
- GetWindowRect 函式
- SetWindowPos 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38cc3072be387f549e77186886854c8cf6a40a466ca5014c4eb85469faf762b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781858"
---
# <a name="stretching-an-image-and-window"></a>延展影像和視窗

下列範例會伸展影片剪輯的影像，並變更顯示畫面格的外觀比例。 在 [MCIWnd] 視窗中顯示的畫面格為原始框架寬度的兩倍高度和三倍。 [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)和 [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)宏會取出並重新定義目的地矩形座標。 [GetWindowRect](/windows/win32/api/winuser/nf-winuser-getwindowrect)和[SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos)函數會管理 MCIWnd 視窗維度的變更。


```C++
// extern RECT rCurrent, rDest; 
 
case WM_COMMAND: 
   switch (wParam) 
   { 
       case IDM_CREATEMCIWND: 
           g_hwndMCIWnd = MCIWndCreate(hwnd, 
           g_hinst, 
           WS_CHILD | WS_VISIBLE, 
          "sample.avi"); 
           break;    
 
       case IDM_RESIZEWINDOW: // destination RECT and playback area
           GetWindowRect(g_hwndMCIWnd, &rWin);     // window size 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT
           rDest.top = rCurrent.top;               // new boundaries 
           rDest.right = rCurrent.right; 
           rDest.left = rCurrent.left + 
               ((rCurrent.left - rCurrent.right) * 3); 
           rDest.bottom = rCurrent.top + 
               ((rCurrent.bottom - rCurrent.top) * 2); 
           MCIWndPutDest(g_hwndMCIWnd, &rDest); // new RECT
           SetWindowPos(g_hwndMCIWnd,           // window to resize 
               NULL,                          // z-order: don't care 
               0, 0,                          // position: don't care
               rDest.right - rDest.left,      // width 
               (rWin.bottom - rWin.top +           // height (window - 
               (rCurrent.bottom - rCurrent.top) +  //  original RECT +
               (rDest.bottom - rDest.top)),        //  new RECT
               SWP_NOMOVE | SWP_NOZORDER | SWP_NOACTIVATE); 
           break; 
   } 
   break; 
 
   // Handle other messages here. 
```



 

 