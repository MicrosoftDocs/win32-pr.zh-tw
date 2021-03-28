---
description: 路徑是藉由結合線條、矩形和簡單曲線來形成。 回想一下向量圖形，下列基本組建區塊已證明是最適合用來繪製圖片的概念。
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: 路徑 (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768d01d2d945c8252125a43ee2dc79f985703da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562882"
---
# <a name="paths-gdi"></a><span data-ttu-id="bb0f4-104">路徑 (GDI+)</span><span class="sxs-lookup"><span data-stu-id="bb0f4-104">Paths (GDI+)</span></span>

<span data-ttu-id="bb0f4-105">路徑是藉由結合線條、矩形和簡單曲線來形成。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-105">Paths are formed by combining lines, rectangles, and simple curves.</span></span> <span data-ttu-id="bb0f4-106">回想一下 [向量圖形](-gdiplus-overview-of-vector-graphics-about.md) ，下列基本組建區塊已證明是最適合用來繪製圖片的概念。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-106">Recall from the [Overview of Vector Graphics](-gdiplus-overview-of-vector-graphics-about.md) that the following basic building blocks have proven to be the most useful for drawing pictures.</span></span>

-   <span data-ttu-id="bb0f4-107">線條</span><span class="sxs-lookup"><span data-stu-id="bb0f4-107">Lines</span></span>
-   <span data-ttu-id="bb0f4-108">矩形</span><span class="sxs-lookup"><span data-stu-id="bb0f4-108">Rectangles</span></span>
-   <span data-ttu-id="bb0f4-109">橢圓形</span><span class="sxs-lookup"><span data-stu-id="bb0f4-109">Ellipses</span></span>
-   <span data-ttu-id="bb0f4-110">弧</span><span class="sxs-lookup"><span data-stu-id="bb0f4-110">Arcs</span></span>
-   <span data-ttu-id="bb0f4-111">多邊形</span><span class="sxs-lookup"><span data-stu-id="bb0f4-111">Polygons</span></span>
-   <span data-ttu-id="bb0f4-112">基本曲線</span><span class="sxs-lookup"><span data-stu-id="bb0f4-112">Cardinal splines</span></span>
-   <span data-ttu-id="bb0f4-113">貝茲曲線</span><span class="sxs-lookup"><span data-stu-id="bb0f4-113">Bézier splines</span></span>

<span data-ttu-id="bb0f4-114">在 Windows GDI + 中， [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) 物件可讓您將這些建築物區塊的一連串收集到單一單位。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-114">In Windows GDI+, the [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object allows you to collect a sequence of these building blocks into a single unit.</span></span> <span data-ttu-id="bb0f4-115">然後，您可以使用圖形類別 [**:D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) [**方法，繪製**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 線條、矩形、多邊形和曲線的整個序列。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-115">The entire sequence of lines, rectangles, polygons, and curves can then be drawn with one call to the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="bb0f4-116">下圖顯示藉由結合直線、弧線、貝茲曲線和基線曲線所建立的路徑。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-116">The following illustration shows a path created by combining a line, an arc, a Bézier spline, and a cardinal spline.</span></span>

![結合線條、弧線、貝茲曲線和基線曲線的路徑圖例](images/aboutgdip02-art14.png)

<span data-ttu-id="bb0f4-118">[**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath)類別提供下列方法來建立要繪製的專案序列： [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint))、 [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_))、 [shapes.addellipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint))、 [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal))、 [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint))、 [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (用於基本曲線) 和 [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint))。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-118">The [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) class provides the following methods for creating a sequence of items to be drawn: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (for cardinal splines), and [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span></span> <span data-ttu-id="bb0f4-119">這些方法都是多載的：也就是說，每個方法都有數個不同的參數清單變化。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-119">Each of these methods is overloaded; that is, each method comes in several variations with different parameter lists.</span></span> <span data-ttu-id="bb0f4-120">例如，AddLine 方法的一種變化會接收四個整數，而 AddLine 方法的另一種變化則會接收兩個 [**點**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) 物件。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-120">For example, one variation of the AddLine method receives four integers, and another variation of the AddLine method receives two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span>

<span data-ttu-id="bb0f4-121">將線條、矩形和貝茲曲線新增至路徑的方法具有複數附屬方法，可在單一呼叫中將數個專案新增至路徑： [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint))、 [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))和 [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint))。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-121">The methods for adding lines, rectangles, and Bézier splines to a path have plural companion methods that add several items to the path in a single call: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint)), and [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span></span> <span data-ttu-id="bb0f4-122">此外， [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) 方法也有附屬方法 [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint))，它會將封閉曲線新增至路徑。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-122">Also, the [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) method has a companion method, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), that adds a closed curve to the path.</span></span>

<span data-ttu-id="bb0f4-123">若要繪製路徑，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件、 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件和 [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) 物件。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-123">To draw a path, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="bb0f4-124">**Graphics** 物件提供 [**圖形：:D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath)方法，而 **Pen** 物件會儲存路徑的屬性，例如線條寬度和色彩。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-124">The **Graphics** object provides the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method, and the **Pen** object stores attributes of the path, such as line width and color.</span></span> <span data-ttu-id="bb0f4-125">**GraphicsPath** 物件會儲存組成路徑的線條、矩形和曲線序列。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-125">The **GraphicsPath** object stores the sequence of lines, rectangles, and curves that make up the path.</span></span> <span data-ttu-id="bb0f4-126">**Pen** 物件和 **GraphicsPath** 物件的位址會做為引數傳遞給 **圖形：:D rawpath** 方法。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-126">The addresses of the **Pen** object and the **GraphicsPath** object are passed as arguments to the **Graphics::DrawPath** method.</span></span> <span data-ttu-id="bb0f4-127">下列範例會繪製包含線條、橢圓形和貝茲曲線的路徑。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-127">The following example draws a path that consists of a line, an ellipse, and a Bézier spline.</span></span>


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="bb0f4-128">下圖顯示路徑。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-128">The following illustration shows the path.</span></span>

![以線條、橢圓形和貝茲曲線組成的路徑圖例](images/aboutgdip02-art15.png)

<span data-ttu-id="bb0f4-130">除了將線條、矩形和曲線新增至路徑，您還可以將路徑新增至路徑。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-130">In addition to adding lines, rectangles, and curves to a path, you can add paths to a path.</span></span> <span data-ttu-id="bb0f4-131">這可讓您結合現有的路徑來形成大型、複雜的路徑。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-131">This allows you to combine existing paths to form large, complex paths.</span></span> <span data-ttu-id="bb0f4-132">下列程式碼會將 **graphicsPath1** 和 **GraphicsPath2** 新增至 **myGraphicsPath**。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-132">The following code adds **graphicsPath1** and **graphicsPath2** to **myGraphicsPath**.</span></span> <span data-ttu-id="bb0f4-133">[**GraphicsPath：： AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath)方法的第二個參數會指定加入的路徑是否連接至現有的路徑。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-133">The second parameter of the [**GraphicsPath::AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) method specifies whether the added path is connected to the existing path.</span></span>


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



<span data-ttu-id="bb0f4-134">您可以新增其他兩個專案至路徑：字串和圓形圖。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-134">There are two other items you can add to a path: strings and pies.</span></span> <span data-ttu-id="bb0f4-135">圓形圖是橢圓形內部的一部分。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-135">A pie is a portion of the interior of an ellipse.</span></span> <span data-ttu-id="bb0f4-136">下列範例會建立從弧線、基線曲線、字串和圓形圖的路徑。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-136">The following example creates a path from an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="bb0f4-137">下圖顯示路徑。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-137">The following illustration shows the path.</span></span> <span data-ttu-id="bb0f4-138">請注意，不需要連接路徑;弧線、基線曲線、字串和圓形圖會分開。</span><span class="sxs-lookup"><span data-stu-id="bb0f4-138">Note that a path does not have to be connected; the arc, cardinal spline, string, and pie are separated.</span></span>

![由中斷連接線組成的路徑圖例：弧形、基線曲線、字串和圓形圖](images/aboutgdip02-art16.png)

 

 



