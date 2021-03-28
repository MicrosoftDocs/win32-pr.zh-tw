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
# <a name="drawing-a-shaded-rectangle"></a><span data-ttu-id="ea724-104">繪製陰影矩形</span><span class="sxs-lookup"><span data-stu-id="ea724-104">Drawing a Shaded Rectangle</span></span>

<span data-ttu-id="ea724-105">若要繪製陰影矩形，請使用兩個元素和一個漸層 [**\_ 矩形**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)結構來定義 [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)陣列。</span><span class="sxs-lookup"><span data-stu-id="ea724-105">To draw a shaded rectangle, define a [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) array with two elements and a single [**GRADIENT\_RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect) structure.</span></span> <span data-ttu-id="ea724-106">下列程式碼範例示範如何使用 [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) 函式，並定義漸層 \_ 填滿矩形模式來繪製陰影矩形 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ea724-106">The following code example shows how to draw a shaded rectangle using the [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) function with the GRADIENT\_FILL\_RECT mode defined.</span></span>


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



<span data-ttu-id="ea724-107">下圖顯示上述程式碼範例的繪圖輸出。</span><span class="sxs-lookup"><span data-stu-id="ea724-107">The following image shows the drawing output of the preceding code example.</span></span>

![圖例顯示一個矩形，其左邊緣的漸層填滿是右邊的淺色](images/gradientfillrectangle.png)

## <a name="related-topics"></a><span data-ttu-id="ea724-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="ea724-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea724-110">點陣圖總覽</span><span class="sxs-lookup"><span data-stu-id="ea724-110">Bitmaps Overview</span></span>](bitmaps.md)
</dt> <dt>

[<span data-ttu-id="ea724-111">點陣圖函數</span><span class="sxs-lookup"><span data-stu-id="ea724-111">Bitmap Functions</span></span>](bitmap-functions.md)
</dt> <dt>

[<span data-ttu-id="ea724-112">繪製陰影三角形</span><span class="sxs-lookup"><span data-stu-id="ea724-112">Drawing a Shaded Triangle</span></span>](drawing-a-shaded-triangle.md)
</dt> <dt>

[<span data-ttu-id="ea724-113">**EMRGRADIENTFILL**</span><span class="sxs-lookup"><span data-stu-id="ea724-113">**EMRGRADIENTFILL**</span></span>](/windows/win32/api/wingdi/ns-wingdi-emrgradientfill)
</dt> <dt>

[<span data-ttu-id="ea724-114">**漸層 \_ 矩形**</span><span class="sxs-lookup"><span data-stu-id="ea724-114">**GRADIENT\_RECT**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)
</dt> <dt>

[<span data-ttu-id="ea724-115">**GradientFill**</span><span class="sxs-lookup"><span data-stu-id="ea724-115">**GradientFill**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)
</dt> <dt>

[<span data-ttu-id="ea724-116">**TRIVERTEX**</span><span class="sxs-lookup"><span data-stu-id="ea724-116">**TRIVERTEX**</span></span>](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)
</dt> </dl>

 

 



