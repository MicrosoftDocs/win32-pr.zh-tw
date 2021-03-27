---
description: 當使用者在功能表中按一下 [剪下] 之後，應用程式會使用使用者所建立之矩形的座標來定義裁剪區域。
ms.assetid: 5ae60181-c72e-4a28-99eb-e23d35c46685
title: 裁剪輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc0181340b03421815ebe0f5cd8328d4793a406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943811"
---
# <a name="clipping-output"></a>裁剪輸出

當使用者在功能表中按一下 [剪下] 之後，應用程式會使用使用者所建立之矩形的座標來定義裁剪區域。 在定義裁剪區域，並將其選取到應用程式的裝置內容之後，應用程式會重繪點陣圖影像。 應用程式會執行下列工作，如下所示。


```C++
// These variables are required for clipping.  
 
static POINT ptUpperLeft; 
static POINT ptLowerRight; 
static POINT aptRect[5]; 
static POINT ptTmp; 
static POINTS ptsTmp; 
static BOOL fDefineRegion; 
static BOOL fRegionExists; 
static HRGN hrgn; 
static RECT rctTmp; 
int i; 
 
case WM_COMMAND: 
    switch (wParam) 
    { 
 
    case IDM_CLIP: 
 
    hdc = GetDC(hwnd); 
 
    // Retrieve the application's client rectangle and paint  
    // with the default (white) brush.  
 
    GetClientRect(hwnd, &rctTmp); 
    FillRect(hdc, &rctTmp, GetStockObject(WHITE_BRUSH)); 
 
    // Use the rect coordinates to define a clipping region.  
 
    hrgn = CreateRectRgn(aptRect[0].x, aptRect[0].y, 
        aptRect[2].x, aptRect[2].y); 
    SelectClipRgn(hdc, hrgn); 
 
    // Transfer (draw) the bitmap into the clipped rectangle.  
 
    BitBlt(hdc, 
       0, 0, 
       bmp.bmWidth, bmp.bmHeight, 
       hdcCompatible, 
       0, 0, 
       SRCCOPY); 
 
    ReleaseDC(hwnd, hdc); 
    break; 
    }
```



 

 



