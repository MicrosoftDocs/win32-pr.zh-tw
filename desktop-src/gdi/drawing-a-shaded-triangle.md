---
description: 若要繪製陰影三角形，請使用三個元素和一個漸層三角形結構來定義 TRIVERTEX 結構 \_ 。
ms.assetid: 78834f92-00cb-4899-851a-1de5e3c1f4fa
title: 繪製陰影三角形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3200a1ec061d7513cbac56c8c66104154005cef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114676"
---
# <a name="drawing-a-shaded-triangle"></a>繪製陰影三角形

若要繪製陰影三角形，請使用三個元素和一個漸層 [**\_ 三角形**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle)結構來定義 [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)結構。 下列程式碼範例示範如何使用 [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) 函式，並定義漸層 \_ 填滿三角形模式來繪製陰影三角形 \_ 。


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_PAINT:
        {hdc = BeginPaint(hWnd, &ps);
// Create an array of TRIVERTEX structures that describe
// positional and color values for each vertex.
TRIVERTEX vertex[3];
vertex[0].x     = 150;
vertex[0].y     = 0;
vertex[0].Red   = 0xff00;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x0000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 0;
vertex[1].y     = 150;
vertex[1].Red   = 0x9000;
vertex[1].Green = 0x0000;
vertex[1].Blue  = 0x9000;
vertex[1].Alpha = 0x0000;

vertex[2].x     = 300;
vertex[2].y     = 150; 
vertex[2].Red   = 0x9000;
vertex[2].Green = 0x0000;
vertex[2].Blue  = 0x9000;
vertex[2].Alpha = 0x0000;

// Create a GRADIENT_TRIANGLE structure that
// references the TRIVERTEX vertices.
GRADIENT_TRIANGLE gTriangle;
gTriangle.Vertex1 = 0;
gTriangle.Vertex2 = 1;
gTriangle.Vertex3 = 2;

// Draw a shaded triangle.
GradientFill(hdc, vertex, 3, &gTriangle, 1, GRADIENT_FILL_TRIANGLE);
        EndPaint(hWnd, &ps);
        break;}
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



下圖顯示上述程式碼範例的繪圖輸出。

![圖例顯示在上邊緣以橙色填滿的三角形（從上到洋紅色）](images/gradientfilltriangle.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[點陣圖總覽](bitmaps.md)
</dt> <dt>

[點陣圖函數](bitmap-functions.md)
</dt> <dt>

[繪製陰影矩形](drawing-a-shaded-rectangle.md)
</dt> <dt>

[**EMRGRADIENTFILL**](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[**漸層 \_ 三角形**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle)
</dt> <dt>

[**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



