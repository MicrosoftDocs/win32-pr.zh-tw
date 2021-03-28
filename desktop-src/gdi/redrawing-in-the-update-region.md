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
# <a name="redrawing-in-the-update-region"></a><span data-ttu-id="50a19-103">更新區域中的重繪</span><span class="sxs-lookup"><span data-stu-id="50a19-103">Redrawing in the Update Region</span></span>

<span data-ttu-id="50a19-104">您可以藉由判斷更新區域的大小和位置，來限制應用程式在處理 [**WM \_ 油漆**](wm-paint.md) 訊息時所執行的繪圖量。</span><span class="sxs-lookup"><span data-stu-id="50a19-104">You can limit the amount of drawing your application carries out when processing the [**WM\_PAINT**](wm-paint.md) message by determining the size and location of the update region.</span></span> <span data-ttu-id="50a19-105">由於系統會在建立視窗顯示裝置內容的裁剪區域時使用更新區域，因此您可以藉由檢查裁剪區域來間接判斷更新區域。</span><span class="sxs-lookup"><span data-stu-id="50a19-105">Because the system uses the update region when creating the clipping region for the window's display device context, you can indirectly determine the update region by examining the clipping region.</span></span>

<span data-ttu-id="50a19-106">在下列範例中，視窗程式會繪製三角形、矩形、五形和六邊形，但只有在每個圖表的全部或部分位於更新區域內時。</span><span class="sxs-lookup"><span data-stu-id="50a19-106">In the following example, the window procedure draws a triangle, a rectangle, a pentagon, and a hexagon, but only if all or a portion of each figure lies within the update region.</span></span> <span data-ttu-id="50a19-107">視窗程式會使用 [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) 函式和 100 100 矩形來判斷圖形是否在裁剪區域內 (，因此， [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)所抓取之一般裝置內容的更新區域) 。</span><span class="sxs-lookup"><span data-stu-id="50a19-107">The window procedure uses the [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) function and a 100-by-100 rectangle to determine whether a figure is within the clipping region (and therefore the update region) for the common device context retrieved by [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).</span></span>


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



<span data-ttu-id="50a19-108">此範例中每個圖形的座標都位於相同的 100 100 矩形內。</span><span class="sxs-lookup"><span data-stu-id="50a19-108">The coordinates of each figure in this example lie within the same 100-by-100 rectangle.</span></span> <span data-ttu-id="50a19-109">在繪製圖形之前，視窗程式會使用 [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) 函式，將 [視口] 原點設定為工作區的不同部分。</span><span class="sxs-lookup"><span data-stu-id="50a19-109">Before drawing a figure, the window procedure sets the viewport origin to a different part of the client area by using the [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) function.</span></span> <span data-ttu-id="50a19-110">這可防止將圖形繪製在另一個上方。</span><span class="sxs-lookup"><span data-stu-id="50a19-110">This prevents figures from being drawn one on top of the other.</span></span> <span data-ttu-id="50a19-111">變更視口來源不會影響裁剪區域，但會影響傳遞至 [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) 之矩形座標的轉譯方式。</span><span class="sxs-lookup"><span data-stu-id="50a19-111">Changing the viewport origin does not affect the clipping region, but does affect how the coordinates of the rectangle passed to [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) are interpreted.</span></span> <span data-ttu-id="50a19-112">變更來源也可讓您使用單一矩形來檢查更新區域，而不是每個圖形的個別矩形。</span><span class="sxs-lookup"><span data-stu-id="50a19-112">Changing the origin also allows you to use a single rectangle to check the update region rather than individual rectangles for each figure.</span></span>

 

 



