---
description: 若要使用 Windows GDI + 繪製線條，您需要建立繪圖物件和 Pen 物件。
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: 畫筆、線條和矩形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e9749b1c1af6ca4808e797d016267bb251e6fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972852"
---
# <a name="pens-lines-and-rectangles"></a><span data-ttu-id="e61a0-103">畫筆、線條和矩形</span><span class="sxs-lookup"><span data-stu-id="e61a0-103">Pens, Lines, and Rectangles</span></span>

<span data-ttu-id="e61a0-104">若要使用 Windows GDI + 繪製線條，您需要建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件。</span><span class="sxs-lookup"><span data-stu-id="e61a0-104">To draw lines with Windows GDI+ you need to create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="e61a0-105">**Graphics** 物件提供實際繪製繪圖的方法，而 **Pen** 物件會儲存線條的屬性，例如色彩、寬度和樣式。</span><span class="sxs-lookup"><span data-stu-id="e61a0-105">The **Graphics** object provides the methods that actually do the drawing, and the **Pen** object stores attributes of the line, such as color, width, and style.</span></span> <span data-ttu-id="e61a0-106">繪製線條只是呼叫 **Graphics** 物件的 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))方法。</span><span class="sxs-lookup"><span data-stu-id="e61a0-106">Drawing a line is simply a matter of calling the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object.</span></span> <span data-ttu-id="e61a0-107">**畫筆** 物件的位址會做為 DrawLine 方法的其中一個引數傳遞。</span><span class="sxs-lookup"><span data-stu-id="e61a0-107">The address of the **Pen** object is passed as one of the arguments to the DrawLine method.</span></span> <span data-ttu-id="e61a0-108">下列範例會繪製從點 (4，2) 到 (12，6) 點的直線。</span><span class="sxs-lookup"><span data-stu-id="e61a0-108">The following example draws a line from the point (4, 2) to the point (12, 6).</span></span>


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



<span data-ttu-id="e61a0-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) 是 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的多載方法，因此您可以透過數種方式提供引數給它。</span><span class="sxs-lookup"><span data-stu-id="e61a0-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="e61a0-110">例如，您可以建立兩個 [**point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) 物件，並將 **point** 物件的參考傳遞為 DrawLine 方法的引數。</span><span class="sxs-lookup"><span data-stu-id="e61a0-110">For example, you can construct two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects and pass references to the **Point** objects as arguments to the DrawLine method.</span></span>


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



<span data-ttu-id="e61a0-111">當您建立 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件時，可以指定某些屬性。</span><span class="sxs-lookup"><span data-stu-id="e61a0-111">You can specify certain attributes when you construct a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="e61a0-112">例如，一個 [畫筆](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) 的函式可讓您指定色彩和寬度。</span><span class="sxs-lookup"><span data-stu-id="e61a0-112">For example, one [Pen](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) constructor allows you to specify color and width.</span></span> <span data-ttu-id="e61a0-113">下列範例會從 (0、0) 到 (60 30) ，繪製一條寬度2的藍色線。</span><span class="sxs-lookup"><span data-stu-id="e61a0-113">The following example draws a blue line of width 2 from (0, 0) to (60, 30).</span></span>


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



<span data-ttu-id="e61a0-114">[**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)物件也有屬性（例如虛線樣式），您可以用來指定線條的功能。</span><span class="sxs-lookup"><span data-stu-id="e61a0-114">The [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object also has attributes, such as dash style, that you can use to specify features of the line.</span></span> <span data-ttu-id="e61a0-115">例如，下列範例會繪製從 (100，50) 到 (300，80) 的虛線。</span><span class="sxs-lookup"><span data-stu-id="e61a0-115">For example, the following example draws a dashed line from (100, 50) to (300, 80).</span></span>


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



<span data-ttu-id="e61a0-116">您可以使用 [ [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) ] 物件的各種方法來設定該線條的許多屬性。</span><span class="sxs-lookup"><span data-stu-id="e61a0-116">You can use various methods of the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to set many more attributes of the line.</span></span> <span data-ttu-id="e61a0-117">[**Pen：： SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap)和 [**Pen：： SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap)方法會指定線條結尾的外觀;結尾可以是平面、正方形、圓角、三角形或自訂形狀。</span><span class="sxs-lookup"><span data-stu-id="e61a0-117">The [**Pen::SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) and [**Pen::SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) methods specify the appearance of the ends of the line; the ends can be flat, square, rounded, triangular, or a custom shape.</span></span> <span data-ttu-id="e61a0-118">[**Pen：： SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin)方法可讓您指定連接線是否為斜接 (聯結) 、斜面、圓角或裁剪的尖角。</span><span class="sxs-lookup"><span data-stu-id="e61a0-118">The [**Pen::SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method lets you specify whether connected lines are mitered (joined with sharp corners), beveled, rounded, or clipped.</span></span> <span data-ttu-id="e61a0-119">下圖顯示具有各種端點和聯結樣式的行。</span><span class="sxs-lookup"><span data-stu-id="e61a0-119">The following illustration shows lines with various cap and join styles.</span></span>

![這兩行的圖解，示範圓角和圓形結束、圓角和斜接角，以及兩個箭號樣式](images/aboutgdip02-art04.png)

<span data-ttu-id="e61a0-121">使用 GDI + 繪製矩形類似于繪製線條。</span><span class="sxs-lookup"><span data-stu-id="e61a0-121">Drawing rectangles with GDI+ is similar to drawing lines.</span></span> <span data-ttu-id="e61a0-122">若要繪製矩形，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件。</span><span class="sxs-lookup"><span data-stu-id="e61a0-122">To draw a rectangle, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="e61a0-123">**Graphics** 物件提供 [graphicswindow.drawrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint))方法，而 **Pen** 物件會儲存屬性，例如線條寬度和色彩。</span><span class="sxs-lookup"><span data-stu-id="e61a0-123">The **Graphics** object provides a [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores attributes, such as line width and color.</span></span> <span data-ttu-id="e61a0-124">**畫筆** 物件的位址會做為 graphicswindow.drawrectangle 方法的其中一個引數傳遞。</span><span class="sxs-lookup"><span data-stu-id="e61a0-124">The address of the **Pen** object is passed as one of the arguments to the DrawRectangle method.</span></span> <span data-ttu-id="e61a0-125">下列範例會在 (100、50) 、寬度為80且高度為40的情況下，繪製一個矩形，其左上角。</span><span class="sxs-lookup"><span data-stu-id="e61a0-125">The following example draws a rectangle with its upper-left corner at (100, 50), a width of 80, and a height of 40.</span></span>


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



<span data-ttu-id="e61a0-126">[Graphicswindow.drawrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) 是 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的多載方法，因此您可以透過數種方式提供引數給它。</span><span class="sxs-lookup"><span data-stu-id="e61a0-126">[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="e61a0-127">例如，您可以建立 [**rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) 物件，並將 **rect** 物件的參考傳遞為 graphicswindow.drawrectangle 方法的引數。</span><span class="sxs-lookup"><span data-stu-id="e61a0-127">For example, you can construct a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawRectangle method.</span></span>


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



<span data-ttu-id="e61a0-128">[**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect)物件有方法可操作和收集矩形的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e61a0-128">A [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object has methods for manipulating and gathering information about the rectangle.</span></span> <span data-ttu-id="e61a0-129">例如，擴充和[位移](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_))方法會變更矩形的[大小和位置](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint))。</span><span class="sxs-lookup"><span data-stu-id="e61a0-129">For example, the [Inflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) and [Offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) methods change the size and position of the rectangle.</span></span> <span data-ttu-id="e61a0-130">[**Rect：： IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith)方法會告訴您矩形是否與另一個指定的矩形相交，而 [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint))方法會告訴您指定的點是否在矩形內。</span><span class="sxs-lookup"><span data-stu-id="e61a0-130">The [**Rect::IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) method tells you whether the rectangle intersects another given rectangle, and the [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) method tells you whether a given point is inside the rectangle.</span></span>

 

 
