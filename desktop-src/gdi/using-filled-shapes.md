---
description: 本節說明如何使用填滿的形狀函數。 此範例會使用應用程式的主視窗程式，讓使用者能夠繪製具有圓角的橢圓形、矩形和矩形。
ms.assetid: c5fc3346-e5d7-49c0-979b-10d91ab965c5
title: 使用填滿的圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03092c0eea329759b70c18c4fa8247081ca99fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194453"
---
# <a name="using-filled-shapes"></a>使用填滿的圖形

本節說明如何使用填滿的形狀函數。 此範例會使用應用程式的主視窗程式，讓使用者能夠繪製具有圓角的橢圓形、矩形和矩形。

使用者可以從功能表中選取特定圖形、將游標放在)  (圖形的左上角，將游標置於圖形的左上角，然後拖曳滑鼠，直到取得所需的維度為止，藉此繪製填滿的形狀。

下圖顯示使用本節中的範例程式碼繪製的三個填滿形狀。

![顯示圓形和兩個 rectagles 的螢幕擷取畫面--一個具有正方形邊角，另一個具有圓角](images/fillshape.png)

若要讓使用者繪製填滿的圖形，請在您的應用程式中包含下列快顯視窗。


```C++
   POPUP "Filled &Shapes"
   {
      MENUITEM "&Ellipse",   IDM_ELLIPSE
      MENUITEM "&Rectangle", IDM_RECTANGLE
      MENUITEM "R&oundRect", IDM_ROUNDRECT
   }
```



功能表範本中的功能表項目值是您必須在應用程式的標頭檔中定義如下的常數。


```C++
#define IDM_ELLIPSE    1100
#define IDM_RECTANGLE  1200
#define IDM_ROUNDRECT  1300
```



最後，在您的應用程式中包含下列視窗程式。


```C++
BOOL CALLBACK MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, 
                          LPARAM lParam) 
{ 
    HDC hdc;          // handle to device context (DC)  
    PAINTSTRUCT ps;   // paint data for Begin/EndPaint  
    POINT ptClientUL; // client area upper left corner  
    POINT ptClientLR; // client area lower right corner  
    static HDC hdcCompat; // handle to DC for bitmap  
    static POINT pt;      // x- and y-coordinates of cursor  
    static RECT rcTarget; // rect to receive filled shape  
    static RECT rcClient; // client area rectangle  
    static BOOL fSizeEllipse; // TRUE if ellipse is sized  
    static BOOL fDrawEllipse;   // TRUE if ellipse is drawn  
    static BOOL fDrawRectangle; // TRUE if rectangle is drawn  
    static BOOL fSizeRectangle; // TRUE if rectangle is sized  
    static BOOL fSizeRoundRect; // TRUE if rounded rect is sized  
    static BOOL fDrawRoundRect; // TRUE if rounded rect is drawn  
    static int nEllipseWidth;   // width for round corners  
    static int nEllipseHeight;  // height for round corners  
 
    switch (uMsg) 
    { 
        case WM_COMMAND: 
            switch (wParam) 
            { 

                // Set the appropriate flag to indicate which  
                // filled shape the user is drawing.  

                case IDM_ELLIPSE: 
                    fSizeEllipse = TRUE; 
                break; 
 
                case IDM_RECTANGLE: 
                    fSizeRectangle = TRUE; 
                break; 
 
                case IDM_ROUNDRECT: 
                    fSizeRoundRect = TRUE; 
                break; 
 
                default: 
                    return DefWindowProc(hwnd, uMsg, wParam, 
                         lParam); 
            } 
            break; 
 
 
        case WM_CREATE: 
            nEllipseWidth = 20; 
            nEllipseHeight = 20; 
 
            return 0; 
 
        case WM_PAINT: 
 
 
            BeginPaint(hwnd, &ps); 
 
            // Because the default brush is white, select  
            // a different brush into the device context  
            // to demonstrate the painting of filled shapes.  
 
            SelectObject(ps.hdc, GetStockObject(GRAY_BRUSH)); 
 
            // If one of the filled shape "draw" flags is TRUE,  
            // draw the corresponding shape.  
 
            if (fDrawEllipse) 
            {
                Ellipse(ps.hdc, rcTarget.left, rcTarget.top, 
                    rcTarget.right, rcTarget.bottom); 
                fDrawEllipse = FALSE; 
                rcTarget.left = rcTarget.right = 0; 
                rcTarget.top = rcTarget.bottom = 0; 
            } 
 
            if (fDrawRectangle) 
            {
                Rectangle(ps.hdc, rcTarget.left, rcTarget.top, 
                    rcTarget.right, rcTarget.bottom); 
                fDrawRectangle = FALSE; 
                rcTarget.left = rcTarget.right = 0; 
                rcTarget.top = rcTarget.bottom = 0; 
            } 
 
            if (fDrawRoundRect) 
            {
                RoundRect(ps.hdc, rcTarget.left, rcTarget.top, 
                    rcTarget.right, rcTarget.bottom, 
                    nEllipseWidth, nEllipseHeight); 
                fDrawRectangle = FALSE; 
                rcTarget.left = rcTarget.right = 0; 
                rcTarget.top = rcTarget.bottom = 0; 
            } 
 
            EndPaint(hwnd, &ps); 
            break; 
 
        case WM_SIZE: 
 
            // Convert the client coordinates of the client area  
            // rectangle to screen coordinates and save them in a  
            // rectangle. The rectangle is passed to the ClipCursor  
            // function during WM_LBUTTONDOWN processing.  
 
            GetClientRect(hwnd, &rcClient); 
            ptClientUL.x = rcClient.left; 
            ptClientUL.y = rcClient.top; 
            ptClientLR.x = rcClient.right; 
            ptClientLR.y = rcClient.bottom; 
            ClientToScreen(hwnd, &ptClientUL); 
            ClientToScreen(hwnd, &ptClientLR); 
            SetRect(&rcClient, ptClientUL.x, ptClientUL.y, 
                ptClientLR.x, ptClientLR.y); 
            return 0; 
 
        case WM_LBUTTONDOWN: 
 
            // Restrict the cursor to the client area.  
            // This ensures that the window receives a matching  
            // WM_LBUTTONUP message.  
 
            ClipCursor(&rcClient); 
 
            // Save the coordinates of the cursor.  
 
            pt.x = (LONG) LOWORD(lParam); 
            pt.y = (LONG) HIWORD(lParam); 
 
            // If the user chooses one of the filled shapes,  
            // set the appropriate flag to indicate that the  
            // shape is being sized.  
 
             if (fDrawEllipse) 
                fSizeEllipse = TRUE; 
 
            return 0; 
 
        case WM_MOUSEMOVE: 
 
            // If one of the "size" flags is set, draw  
            // the target rectangle as the user drags  
            // the mouse.  
 
            if ((wParam && MK_LBUTTON) 
                    && (fSizeEllipse || fSizeRectangle 
                    || fSizeRoundRect)) 
            {  
 
                // Set the mixing mode so that the pen color is the  
                // inverse of the background color. The previous  
                // rectangle can then be erased by drawing  
                // another rectangle on top of it.  
 
                hdc = GetDC(hwnd); 
                SetROP2(hdc, R2_NOTXORPEN); 
 
                // If a previous target rectangle exists, erase  
                // it by drawing another rectangle on top.  
 
                if (!IsRectEmpty(&rcTarget)) 
                {
                    Rectangle(hdc, rcTarget.left, rcTarget.top, 
                        rcTarget.right, rcTarget.bottom); 
                }

                // Save the coordinates of the target rectangle.  
                // Avoid invalid rectangles by ensuring that the  
                // value of the left coordinate is greater than  
                // that of the right, and that the value of the  
                // bottom coordinate is greater than that of  
                // the top.  
 
                if ((pt.x < (LONG) LOWORD(lParam)) && 
                        (pt.y > (LONG) HIWORD(lParam))) 
                {
                    SetRect(&rcTarget, pt.x, HIWORD(lParam), 
                        LOWORD(lParam), pt.y); 
                } 
 
                else if ((pt.x > (LONG) LOWORD(lParam)) && 
                        (pt.y > (LONG) HIWORD(lParam))) 
                {
                    SetRect(&rcTarget, LOWORD(lParam), 
                        HIWORD(lParam), pt.x, pt.y); 
                }
 
                else if ((pt.x > (LONG) LOWORD(lParam)) && 
                        (pt.y < (LONG) HIWORD(lParam))) 
                {
                    SetRect(&rcTarget, LOWORD(lParam), pt.y, 
                        pt.x, HIWORD(lParam)); 
                }
                else 
                {
                    SetRect(&rcTarget, pt.x, pt.y, LOWORD(lParam), 
                        HIWORD(lParam)); 
                }
 
                // Draw the new target rectangle.  
 
                Rectangle(hdc, rcTarget.left, rcTarget.top, 
                    rcTarget.right, rcTarget.bottom); 
                ReleaseDC(hwnd, hdc); 
            } 
            return 0; 
 
        case WM_LBUTTONUP: 
 
            // If one of the "size" flags is TRUE, reset it to FALSE,  
            // and then set the corresponding "draw" flag. Invalidate  
            // the appropriate rectangle and issue a WM_PAINT message.  
 
            if (fSizeEllipse) 
            { 
                fSizeEllipse = FALSE; 
                fDrawEllipse = TRUE; 
            } 
 
            if (fSizeRectangle) 
            { 
                fSizeRectangle = FALSE; 
                fDrawRectangle = TRUE; 
            } 
 
            if (fSizeRoundRect) 
            { 
                fSizeRoundRect = FALSE; 
                fDrawRoundRect = TRUE; 
            } 
 
            if (fDrawEllipse || fDrawRectangle || fDrawRoundRect) 
            { 
                InvalidateRect(hwnd, &rcTarget, TRUE); 
                UpdateWindow(hwnd); 
            } 
 
            // Release the cursor.  
 
            ClipCursor((LPRECT) NULL); 
            return 0; 
 
        case WM_DESTROY: 
 
            // Destroy the background brush, compatible bitmap,  
            // and bitmap.  
 
            DeleteDC(hdcCompat); 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return (LRESULT) NULL; 
} 
```



 

 



