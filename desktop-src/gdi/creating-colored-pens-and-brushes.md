---
description: 雖然您可以在建立畫筆時指定任何色彩，但系統只會使用裝置上可用的色彩。
ms.assetid: 2ea32786-f769-4096-8f60-f924c83ca9c8
title: 建立彩色畫筆和筆刷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e487338e967f5981eaa28c2f90981f60d7e094df58317fb1af98a447622a4631
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452258"
---
# <a name="creating-colored-pens-and-brushes"></a>建立彩色畫筆和筆刷

雖然您可以在建立畫筆時指定任何色彩，但系統只會使用裝置上可用的色彩。 這表示當系統發現繪製畫筆時，系統會使用最接近的相符色彩。 建立筆刷時，如果您指定裝置不支援的色彩，系統會產生遞色色彩。 無論是哪一種情況，您都可以使用 [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) 宏來指定建立畫筆或筆刷時的色彩。


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;
    RECT clientRect;
    RECT textRect;
    HRGN bgRgn;
    HBRUSH hBrush;
    HPEN hPen;


    switch (message)
    {
    
    case WM_PAINT:
        {
        hdc = BeginPaint(hWnd, &ps);
        
        // Fill the client area with a brush
        GetClientRect(hWnd, &clientRect);
        bgRgn = CreateRectRgnIndirect(&clientRect);
        hBrush = CreateSolidBrush(RGB(200,200,200));
        FillRgn(hdc, bgRgn, hBrush);

        
        hPen = CreatePen(PS_DOT,1,RGB(0,255,0));
        SelectObject(hdc, hPen);
        SetBkColor(hdc, RGB(0,0,0));
        Rectangle(hdc, 10,10,200,200);
        
        // Text caption
        SetBkColor(hdc, RGB(255,255,255));
        SetRect(&textRect, 10, 210, 200,200);
        DrawText(hdc,TEXT("PS_DOT"),-1,&textRect, DT_CENTER | DT_NOCLIP);

        
        hPen = CreatePen(PS_DASHDOTDOT,1,RGB(0,255,255));
        SelectObject(hdc, hPen);
        SetBkColor(hdc, RGB(255,0,0));
        SelectObject(hdc,CreateSolidBrush(RGB(0,0,0)));
        Rectangle(hdc, 210,10,400,200);
        
        // Text caption
        SetBkColor(hdc, RGB(255,200,200));
        SetRect(&textRect, 210, 210, 400,200);
        DrawText(hdc,TEXT("PS_DASHDOTDOT"),-1,&textRect, DT_CENTER | DT_NOCLIP);
        

        hPen = CreatePen(PS_DASHDOT,1,RGB(255,0,0));
        SelectObject(hdc, hPen);
        SetBkColor(hdc, RGB(255,255,0));
        SelectObject(hdc,CreateSolidBrush(RGB(100,200,255)));
        Rectangle(hdc, 410,10,600,200);
        
        // Text caption
        SetBkColor(hdc, RGB(200,255,200));
        SetRect(&textRect, 410, 210, 600,200);
        DrawText(hdc,TEXT("PS_DASHDOT"),-1,&textRect, DT_CENTER | DT_NOCLIP);
        

        // When fnPenStyle is PS_SOLID, nWidth may be more than 1.
        // Also, if you set the width of any pen to be greater than 1, 
        // then it will draw a solid line, even if you try to select another style.
        hPen = CreatePen(PS_SOLID,5,RGB(255,0,0));
        SelectObject(hdc, hPen);
        // Setting the background color doesn't matter 
        // when the style is PS_SOLID
        SetBkColor(hdc, RGB(255,255,255));
        SelectObject(hdc,CreateSolidBrush(RGB(200,100,50)));
        Rectangle(hdc, 10,300,200,500);
        
        // Text caption
        SetBkColor(hdc, RGB(200,200,255));
        SetRect(&textRect, 10, 510, 200,500);
        DrawText(hdc,TEXT("PS_SOLID"),-1,&textRect, DT_CENTER | DT_NOCLIP);
    
        hPen = CreatePen(PS_DASH,1,RGB(0,255,0));
        SelectObject(hdc, hPen);
        SetBkColor(hdc, RGB(0,0,0));
        SelectObject(hdc,CreateSolidBrush(RGB(200,200,255)));
        Rectangle(hdc, 210,300,400,500);
        
        // Text caption
        SetBkColor(hdc, RGB(255,255,200));
        SetRect(&textRect, 210, 510, 400,200);
        DrawText(hdc,TEXT("PS_DASH"),-1,&textRect, DT_CENTER | DT_NOCLIP);

        hPen = CreatePen(PS_NULL,1,RGB(0,255,0));
        SelectObject(hdc, hPen);
        // Setting the background color doesn't matter 
        // when the style is PS_NULL
        SetBkColor(hdc, RGB(0,0,0));
        SelectObject(hdc,CreateSolidBrush(RGB(255,255,255)));
        Rectangle(hdc, 410,300,600,500);
        
        // Text caption
        SetBkColor(hdc, RGB(200,255,255));
        SetRect(&textRect, 410, 510, 600,500);
        DrawText(hdc,TEXT("PS_NULL"),-1,&textRect, DT_CENTER | DT_NOCLIP);
        
        
        // Clean up
        DeleteObject(bgRgn);
        DeleteObject(hBrush);
        DeleteObject(hPen);

        GetStockObject(WHITE_BRUSH);
        GetStockObject(DC_PEN);

        EndPaint(hWnd, &ps);
        break;
        }
    

    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



 

 



