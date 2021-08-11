---
description: 您可以允許使用者在處理 WM MOUSEMOVE 訊息時，讓您的視窗程式繪製，以利用滑鼠來繪製線條 \_ 。
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: 使用滑鼠繪圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de7c75c768dcdd330e04a0877bacf59b63d59a6eeb9707011faff6a6b15055c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250400"
---
# <a name="drawing-with-the-mouse"></a>使用滑鼠繪圖

您可以允許使用者在處理 [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) 訊息時，讓您的視窗程式繪製，以利用滑鼠來繪製線條。 當使用者在視窗內移動資料指標時，系統會將 **WM \_ MOUSEMOVE** 訊息傳送至視窗程式。 若要繪製線條，視窗程式可以取出顯示裝置內容，並在視窗中的目前和先前的游標位置之間繪製線條。

在下列範例中，當使用者按下滑鼠左鍵並按住滑鼠左鍵 (傳送 [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) 訊息) 時，視窗程式會準備進行繪製。 當使用者將游標移到視窗內時，視窗程式會收到一連串的 [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) 訊息。 針對每個訊息，視窗程式會繪製一條連接先前位置和目前位置的線。 為了繪製這一行，程式會使用 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 來取出顯示裝置內容;然後，只要繪製完成，而且在從訊息傳回之前，程式就會使用 [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) 函式來釋放顯示裝置內容。 當使用者放開滑鼠按鍵時，視窗程式就會清除旗標，而繪圖會停止 (傳送 [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) 訊息) 。


```C++
BOOL fDraw = FALSE; 
POINT ptPrevious; 
 
  . 
  . 
  . 
 
case WM_LBUTTONDOWN: 
    fDraw = TRUE; 
    ptPrevious.x = LOWORD(lParam); 
    ptPrevious.y = HIWORD(lParam); 
    return 0L; 
 
case WM_LBUTTONUP: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, LOWORD(lParam), HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    fDraw = FALSE; 
    return 0L; 
 
case WM_MOUSEMOVE: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, ptPrevious.x = LOWORD(lParam), 
          ptPrevious.y = HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    return 0L; 
```



啟用繪圖的應用程式（如這個範例所示）通常會記錄點或線條，讓您可以在視窗更新時重新繪製線條。 繪圖應用程式通常會使用記憶體裝置內容和相關聯的點陣圖來儲存使用滑鼠繪製的線條。

 

 
