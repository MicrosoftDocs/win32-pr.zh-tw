---
description: 若要繪製陰影矩形，請使用兩個元素和一個漸層矩形結構來定義 TRIVERTEX 陣列 \_ 。 下列程式碼範例示範如何使用 GradientFill 函式，並定義漸層 \_ 填滿矩形模式來繪製陰影矩形 \_ 。
ms.assetid: a4277e22-03f8-470f-87e9-5aeab258b6d2
title: 繪製陰影矩形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665e76c730ada1bd8efc9967fd10e550f0aa2e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512901"
---
# <a name="drawing-a-shaded-rectangle"></a>繪製陰影矩形

若要繪製陰影矩形，請使用兩個元素和一個漸層 [**\_ 矩形**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)結構來定義 [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)陣列。 下列程式碼範例示範如何使用 [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) 函式，並定義漸層 \_ 填滿矩形模式來繪製陰影矩形 \_ 。


```C++
// Create an array of TRIVERTEX structures that describe 
// positional and color values for each vertex. For a rectangle, 
// only two vertices need to be defined: upper-left and lower-right. 
TRIVERTEX vertex[2] ;
vertex[0].x     = 0;
vertex[0].y     = 0;
vertex[0].Red   = 0x0000;
vertex[0].Green = 0x8000;
vertex[0].Blue  = 0x8000;
vertex[0].Alpha = 0x0000;

vertex[1].x     = 300;
vertex[1].y     = 80; 
vertex[1].Red   = 0x0000;
vertex[1].Green = 0xd000;
vertex[1].Blue  = 0xd000;
vertex[1].Alpha = 0x0000;

// Create a GRADIENT_RECT structure that 
// references the TRIVERTEX vertices. 
GRADIENT_RECT gRect;
gRect.UpperLeft  = 0;
gRect.LowerRight = 1;

// Draw a shaded rectangle. 
GradientFill(hdc, vertex, 2, &gRect, 1, GRADIENT_FILL_RECT_H);
```



下圖顯示上述程式碼範例的繪圖輸出。

![圖例顯示一個矩形，其左邊緣的漸層填滿是右邊的淺色](images/gradientfillrectangle.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[點陣圖總覽](bitmaps.md)
</dt> <dt>

[點陣圖函數](bitmap-functions.md)
</dt> <dt>

[繪製陰影三角形](drawing-a-shaded-triangle.md)
</dt> <dt>

[**EMRGRADIENTFILL**](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[**漸層 \_ 矩形**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)
</dt> <dt>

[**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



