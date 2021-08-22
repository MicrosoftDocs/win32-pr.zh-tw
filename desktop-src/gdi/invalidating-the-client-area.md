---
description: 系統不是 WM 油漆訊息的唯一來源 \_ 。 InvalidateRect 或 InvalidateRgn 函式可以間接產生 \_ 您視窗的 WM 油漆訊息。 這些函式會將一部分或部分的工作區標示為不正確 (，必須重新繪製) 。
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: 使工作區失效
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94a3a5b4e6903c549331788f9e81947dca44e7a699bb1a633bce46525585b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558658"
---
# <a name="invalidating-the-client-area"></a>使工作區失效

系統不是 [**WM \_ 油漆**](wm-paint.md) 訊息的唯一來源。 [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)或 [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn)函式可以間接產生您視窗的 **WM \_ 油漆** 訊息。 這些函式會將一部分或部分的工作區標示為不正確 (，必須重新繪製) 。

在下列範例中，當處理 [**WM \_ 字元**](../inputdev/wm-char.md) 訊息時，視窗程式會使整個工作區失效。 這可讓使用者藉由輸入數位並查看結果來變更圖形;當應用程式訊息佇列中沒有其他訊息時，就會繪製這些結果。


```C++
RECT rc;
POINT aptPentagon[6] = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]  = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
POINT *ppt = aptPentagon; 
int cpt = 6; 
 
  . 
  . 
  . 
 
case WM_CHAR: 
    switch (wParam) 
    { 
        case '5': 
            ppt = aptPentagon; 
            cpt = 6; 
            break; 
        case '6': 
            ppt = aptHexagon; 
            cpt = 7; 
            break; 
    } 
    InvalidateRect(hwnd, NULL, TRUE); 
    return 0L; 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    Polyline(hdc, ppt, cpt); 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



在此範例中， [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)所使用的 **Null** 引數會指定整個工作區;**TRUE** 引數會使背景清除。 如果您不想讓應用程式等到應用程式訊息佇列沒有其他訊息，請使用 [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) 函式強制立即傳送 [**WM \_ 油漆**](wm-paint.md) 訊息。 如果工作區有任何不正確部分， **UpdateWindow** 會將指定視窗的 **WM \_ 油漆** 訊息直接傳送至視窗程式。

 

 
