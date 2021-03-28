---
description: 若要建立路徑，請建立 GraphicsPath 物件，然後呼叫方法（例如 AddLine 和 AddCurve），以將基本專案新增至路徑。
ms.assetid: 66faeb73-16fb-4b7f-a4d5-a90ec2590d8c
title: 從線條、曲線和形狀建立圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c473dfececcaa86347dc02efdfd62131eb9a63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943951"
---
# <a name="creating-figures-from-lines-curves-and-shapes"></a><span data-ttu-id="3ff9b-103">從線條、曲線和形狀建立圖形</span><span class="sxs-lookup"><span data-stu-id="3ff9b-103">Creating Figures from Lines, Curves, and Shapes</span></span>

<span data-ttu-id="3ff9b-104">若要建立路徑，請建立 [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) 物件，然後呼叫方法（例如 [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) 和 [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint))），以將基本專案新增至路徑。</span><span class="sxs-lookup"><span data-stu-id="3ff9b-104">To create a path, construct a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object, and then call methods, such as [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) and [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), to add primitives to the path.</span></span>

<span data-ttu-id="3ff9b-105">下列範例會建立具有單一弧線的路徑。弧線具有-180 度的掃除角度，在預設座標系統中是以逆時針表示。</span><span class="sxs-lookup"><span data-stu-id="3ff9b-105">The following example creates a path that has a single arc. The arc has a sweep angle of –180 degrees, which is counterclockwise in the default coordinate system.</span></span>


```
Pen pen(Color(255, 255, 0, 0));
GraphicsPath path;
path.AddArc(175, 50, 50, 50, 0, -180);
graphics.DrawPath(&pen, &path);
```



<span data-ttu-id="3ff9b-106">下列範例會建立具有兩個數據的路徑。</span><span class="sxs-lookup"><span data-stu-id="3ff9b-106">The following example creates a path that has two figures.</span></span> <span data-ttu-id="3ff9b-107">第一張圖是一條弧線，後面接著一行。</span><span class="sxs-lookup"><span data-stu-id="3ff9b-107">The first figure is an arc followed by a line.</span></span> <span data-ttu-id="3ff9b-108">第二張圖是一條線，後面接著曲線，後面接著一行。</span><span class="sxs-lookup"><span data-stu-id="3ff9b-108">The second figure is a line followed by a curve, followed by a line.</span></span> <span data-ttu-id="3ff9b-109">第一個圖表會保持開啟狀態，而第二個圖表則會關閉。</span><span class="sxs-lookup"><span data-stu-id="3ff9b-109">The first figure is left open, and the second figure is closed.</span></span>


```
Point points[] = {Point(40, 60), Point(50, 70), Point(30, 90)};

Pen pen(Color(255, 255, 0, 0), 2);
GraphicsPath path;

// The first figure is started automatically, so there is
// no need to call StartFigure here.
path.AddArc(175, 50, 50, 50, 0.0f, -180.0f);
path.AddLine(100, 0, 250, 20);

path.StartFigure();
path.AddLine(50, 20, 5, 90);
path.AddCurve(points, 3);
path.AddLine(50, 150, 150, 180);
path.CloseFigure();

graphics.DrawPath(&pen, &path);
```



<span data-ttu-id="3ff9b-110">除了將線條和曲線新增至路徑，您還可以加入封閉的圖形：矩形、橢圓形、圓形圖和多邊形。</span><span class="sxs-lookup"><span data-stu-id="3ff9b-110">In addition to adding lines and curves to paths, you can add closed shapes: rectangles, ellipses, pies, and polygons.</span></span> <span data-ttu-id="3ff9b-111">下列範例會建立具有兩行、一個矩形和一個橢圓形的路徑。</span><span class="sxs-lookup"><span data-stu-id="3ff9b-111">The following example creates a path that has two lines, a rectangle, and an ellipse.</span></span> <span data-ttu-id="3ff9b-112">程式碼會使用畫筆繪製路徑，並使用筆刷來填滿路徑。</span><span class="sxs-lookup"><span data-stu-id="3ff9b-112">The code uses a pen to draw the path and a brush to fill the path.</span></span>


```
GraphicsPath path;
Pen          pen(Color(255, 255, 0, 0), 2);
SolidBrush   brush(Color(255, 0, 0, 200));

path.AddLine(10, 10, 100, 40);
path.AddLine(100, 60, 30, 60);
path.AddRectangle(Rect(50, 35, 20, 40));
path.AddEllipse(10, 75, 40, 30);

graphics.DrawPath(&pen, &path);
graphics.FillPath(&brush, &path);
```



<span data-ttu-id="3ff9b-113">上述範例中的路徑有三個圖形。</span><span class="sxs-lookup"><span data-stu-id="3ff9b-113">The path in the preceding example has three figures.</span></span> <span data-ttu-id="3ff9b-114">第一個圖包含兩行，第二個圖表是由矩形所組成，而第三個圖形則包含橢圓形。</span><span class="sxs-lookup"><span data-stu-id="3ff9b-114">The first figure consists of the two lines, the second figure consists of the rectangle, and the third figure consists of the ellipse.</span></span> <span data-ttu-id="3ff9b-115">即使沒有呼叫 [**GraphicsPath：： CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) 或 [**GraphicsPath：： StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure)，仍會將本質封閉的圖形（例如矩形和省略號）視為個別的圖形。</span><span class="sxs-lookup"><span data-stu-id="3ff9b-115">Even when there are no calls to [**GraphicsPath::CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) or [**GraphicsPath::StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), intrinsically closed shapes, such as rectangles and ellipses, are considered separate figures.</span></span>

 

 



