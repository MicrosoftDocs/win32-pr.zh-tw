---
description: 多邊形是具有三個或更多直邊的封閉圖。
ms.assetid: f1155341-83f3-4805-8d42-a1910515db31
title: 多邊形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67ec2d062579df0510c100a80d06715be4199e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690336"
---
# <a name="polygons"></a><span data-ttu-id="e8a4a-103">多邊形</span><span class="sxs-lookup"><span data-stu-id="e8a4a-103">Polygons</span></span>

<span data-ttu-id="e8a4a-104">多邊形是具有三個或更多直邊的封閉圖。</span><span class="sxs-lookup"><span data-stu-id="e8a4a-104">A polygon is a closed figure with three or more straight sides.</span></span> <span data-ttu-id="e8a4a-105">例如，三角形是三邊的多邊形，矩形是具有四邊的多邊形，而五邊是具有五邊的多邊形。</span><span class="sxs-lookup"><span data-stu-id="e8a4a-105">For example, a triangle is a polygon with three sides, a rectangle is a polygon with four sides, and a pentagon is a polygon with five sides.</span></span> <span data-ttu-id="e8a4a-106">下圖顯示數個多邊形。</span><span class="sxs-lookup"><span data-stu-id="e8a4a-106">The following illustration shows several polygons.</span></span>

![圖例顯示不同圖形、大小和色彩的五個多邊形](images/aboutgdip02-art07.png)

<span data-ttu-id="e8a4a-108">若要繪製多邊形，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件、 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件和 [**點**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) 陣列 (或 [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)) 物件。</span><span class="sxs-lookup"><span data-stu-id="e8a4a-108">To draw a polygon, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and an array of [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (or [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)) objects.</span></span> <span data-ttu-id="e8a4a-109">**Graphics** 物件提供 [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint))方法。</span><span class="sxs-lookup"><span data-stu-id="e8a4a-109">The **Graphics** object provides the [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="e8a4a-110">**Pen** 物件會儲存多邊形的屬性，例如線條寬度和色彩，而 **Point** 物件的陣列則會儲存以直線連接的點。</span><span class="sxs-lookup"><span data-stu-id="e8a4a-110">The **Pen** object stores attributes of the polygon, such as line width and color, and the array of **Point** objects stores the points to be connected by straight lines.</span></span> <span data-ttu-id="e8a4a-111">**Pen** 物件的位址和 **Point** 物件的陣列會以引數的形式傳遞至 DrawPolygon 方法。</span><span class="sxs-lookup"><span data-stu-id="e8a4a-111">The addresses of the **Pen** object and the array of **Point** objects are passed as arguments to the DrawPolygon method.</span></span> <span data-ttu-id="e8a4a-112">下列範例會繪製三側多邊形。</span><span class="sxs-lookup"><span data-stu-id="e8a4a-112">The following example draws a three-sided polygon.</span></span> <span data-ttu-id="e8a4a-113">請注意， **myPointArray** 中只有三個點： (0、0) 、 (50、30) 和 (30 60) 。</span><span class="sxs-lookup"><span data-stu-id="e8a4a-113">Note that there are only three points in **myPointArray**: (0, 0), (50, 30), and (30, 60).</span></span> <span data-ttu-id="e8a4a-114">DrawPolygon 方法會藉由繪製從 (30，60) 回到起點 (0，0) ; 的直線，來自動關閉多邊形。</span><span class="sxs-lookup"><span data-stu-id="e8a4a-114">The DrawPolygon method automatically closes the polygon by drawing a line from (30, 60) back to the starting point (0, 0);</span></span>


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



<span data-ttu-id="e8a4a-115">下圖顯示多邊形。</span><span class="sxs-lookup"><span data-stu-id="e8a4a-115">The following illustration shows the polygon.</span></span>

![針對座標軸顯示三角形的圖例](images/aboutgdip02-art08.png)

 

 



