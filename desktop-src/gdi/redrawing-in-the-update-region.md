---
description: 您可以藉 \_ 由判斷更新區域的大小和位置，來限制應用程式在處理 WM 油漆訊息時所執行的繪圖量。
ms.assetid: 3407014d-6427-45e9-8be4-b8037ca5438f
title: 更新區域中的重繪
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f90518db1a66b98fc7f4bd5961f2cfa581bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991163"
---
# <a name="redrawing-in-the-update-region"></a>更新區域中的重繪

您可以藉由判斷更新區域的大小和位置，來限制應用程式在處理 [**WM \_ 油漆**](wm-paint.md) 訊息時所執行的繪圖量。 由於系統會在建立視窗顯示裝置內容的裁剪區域時使用更新區域，因此您可以藉由檢查裁剪區域來間接判斷更新區域。

在下列範例中，視窗程式會繪製三角形、矩形、五形和六邊形，但只有在每個圖表的全部或部分位於更新區域內時。 視窗程式會使用 [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) 函式和 100 100 矩形來判斷圖形是否在裁剪區域內 (，因此， [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)所抓取之一般裝置內容的更新區域) 。


```C++
POINT aptTriangle[4]  = {50,2, 98,86,  2,86, 50,2}, 
      aptRectangle[5] = { 2,2, 98,2,  98,98,  2,98, 2,2}, 
      aptPentagon[6]  = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]   = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
  . 
  . 
  . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            SetRect(&rc, 0, 0, 100, 100); 
 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptTriangle, 4); 
 
            SetViewportOrgEx(hdc, 100, 0, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptRectangle, 5); 
 
            SetViewportOrgEx(hdc, 0, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptPentagon, 6); 
 
            SetViewportOrgEx(hdc, 100, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptHexagon, 7); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
  . 
  . 
  . 
```



此範例中每個圖形的座標都位於相同的 100 100 矩形內。 在繪製圖形之前，視窗程式會使用 [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) 函式，將 [視口] 原點設定為工作區的不同部分。 這可防止將圖形繪製在另一個上方。 變更視口來源不會影響裁剪區域，但會影響傳遞至 [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) 之矩形座標的轉譯方式。 變更來源也可讓您使用單一矩形來檢查更新區域，而不是每個圖形的個別矩形。

 

 



