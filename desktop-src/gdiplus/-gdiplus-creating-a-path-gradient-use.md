---
description: PathGradientBrush 類別可讓您自訂以逐漸變更的色彩填滿圖形的方式。
ms.assetid: f6a8085c-3d6a-494f-a1ee-5fa96efb1aae
title: 建立路徑漸層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ef39793547b1485525f8cf1fd5b344773e7a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554023"
---
# <a name="creating-a-path-gradient"></a><span data-ttu-id="5844d-103">建立路徑漸層</span><span class="sxs-lookup"><span data-stu-id="5844d-103">Creating a Path Gradient</span></span>

<span data-ttu-id="5844d-104">[**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush)類別可讓您自訂以逐漸變更的色彩填滿圖形的方式。</span><span class="sxs-lookup"><span data-stu-id="5844d-104">The [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class allows you to customize the way you fill a shape with gradually changing colors.</span></span> <span data-ttu-id="5844d-105">**PathGradientBrush** 物件具有界限路徑和中心點。</span><span class="sxs-lookup"><span data-stu-id="5844d-105">A **PathGradientBrush** object has a boundary path and a center point.</span></span> <span data-ttu-id="5844d-106">您可以為中心點指定一種色彩，並為界限指定另一種色彩。</span><span class="sxs-lookup"><span data-stu-id="5844d-106">You can specify one color for the center point and another color for the boundary.</span></span> <span data-ttu-id="5844d-107">您也可以針對界限中的每個點指定不同的色彩。</span><span class="sxs-lookup"><span data-stu-id="5844d-107">You can also specify separate colors for each of several points along the boundary.</span></span>

> [!Note]  
> <span data-ttu-id="5844d-108">在 GDI + 中，路徑是 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) 物件所維護的一連串直線和曲線。</span><span class="sxs-lookup"><span data-stu-id="5844d-108">In GDI+, a path is a sequence of lines and curves maintained by a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="5844d-109">如需 GDI + 路徑的詳細資訊，請參閱 [路徑](-gdiplus-paths-about.md) 和 [建立路徑和繪製路徑](-gdiplus-constructing-and-drawing-paths-use.md)。</span><span class="sxs-lookup"><span data-stu-id="5844d-109">For more information about GDI+ paths, see [Paths](-gdiplus-paths-about.md) and [Constructing and Drawing Paths](-gdiplus-constructing-and-drawing-paths-use.md).</span></span>

 

<span data-ttu-id="5844d-110">下列範例會使用路徑漸層筆刷填滿橢圓形。</span><span class="sxs-lookup"><span data-stu-id="5844d-110">The following example fills an ellipse with a path gradient brush.</span></span> <span data-ttu-id="5844d-111">中央色彩會設為藍色，並將邊界色彩設定為綠色。</span><span class="sxs-lookup"><span data-stu-id="5844d-111">The center color is set to blue and the boundary color is set to aqua.</span></span>


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



<span data-ttu-id="5844d-112">下圖顯示已填滿的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="5844d-112">The following illustration shows the filled ellipse.</span></span>

![顯示橢圓形填滿的圖例](images/pathgradient1.png)

<span data-ttu-id="5844d-114">依預設，路徑漸層筆刷不會延伸到路徑的界限之外。</span><span class="sxs-lookup"><span data-stu-id="5844d-114">By default, a path gradient brush does not extend outside the boundary of the path.</span></span> <span data-ttu-id="5844d-115">如果您使用路徑漸層筆刷來填滿超出路徑界限的形狀，則不會填滿路徑以外的螢幕區域。</span><span class="sxs-lookup"><span data-stu-id="5844d-115">If you use the path gradient brush to fill a shape that extends beyond the boundary of the path, the area of the screen outside the path will not be filled.</span></span> <span data-ttu-id="5844d-116">下圖顯示當您將上述程式碼中的 [**Graphics：： FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) 呼叫變更為時，會發生什麼事 `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` 。</span><span class="sxs-lookup"><span data-stu-id="5844d-116">The following illustration shows what happens if you change the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) call in the preceding code to `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)`.</span></span>

![圖例顯示上一個橢圓形的水準配量](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a><span data-ttu-id="5844d-118">指定界限上的點</span><span class="sxs-lookup"><span data-stu-id="5844d-118">Specifying Points on the Boundary</span></span>

<span data-ttu-id="5844d-119">下列範例會從星形形的路徑來建立路徑漸層筆刷。</span><span class="sxs-lookup"><span data-stu-id="5844d-119">The following example constructs a path gradient brush from a star-shaped path.</span></span> <span data-ttu-id="5844d-120">程式碼會呼叫 [**PathGradientBrush：： SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) 方法，將星號距心的色彩設定為紅色。</span><span class="sxs-lookup"><span data-stu-id="5844d-120">The code calls the [**PathGradientBrush::SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) method to set the color at the centroid of the star to red.</span></span> <span data-ttu-id="5844d-121">然後，程式碼會呼叫 [**PathGradientBrush：： SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors)方法，以指定不同的色彩 (儲存在 [**點**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point)陣列的個別點) 的 [**色彩**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color)陣列中。</span><span class="sxs-lookup"><span data-stu-id="5844d-121">Then the code calls the [**PathGradientBrush::SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) method to specify various colors (stored in the [**colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) array) at the individual points in the [**points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) array.</span></span> <span data-ttu-id="5844d-122">最後的程式碼語句會以路徑漸層筆刷填滿星形形路徑。</span><span class="sxs-lookup"><span data-stu-id="5844d-122">The final code statement fills the star-shaped path with the path gradient brush.</span></span>


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0),    Point(100, 50), 
                  Point(150, 50),  Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150),   Point(37, 75), 
                  Point(0, 50),    Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
```



<span data-ttu-id="5844d-123">下圖顯示填滿的星星。</span><span class="sxs-lookup"><span data-stu-id="5844d-123">The following illustration shows the filled star.</span></span>

![圖例顯示由五顆點填滿的星形，從中間到星形各點的各種色彩](images/pathgradient3.png)

<span data-ttu-id="5844d-125">下列範例會根據點陣列來建立路徑漸層筆刷。</span><span class="sxs-lookup"><span data-stu-id="5844d-125">The following example constructs a path gradient brush based on an array of points.</span></span> <span data-ttu-id="5844d-126">色彩會指派給陣列中的五個點。</span><span class="sxs-lookup"><span data-stu-id="5844d-126">A color is assigned to each of the five points in the array.</span></span> <span data-ttu-id="5844d-127">如果您要以直線連接五個點，您會得到五邊多邊形。</span><span class="sxs-lookup"><span data-stu-id="5844d-127">If you were to connect the five points by straight lines, you would get a five-sided polygon.</span></span> <span data-ttu-id="5844d-128">色彩也會指派給該多邊形的 (距心) 中心，在此範例中， (80，75) 會設定為白色。</span><span class="sxs-lookup"><span data-stu-id="5844d-128">A color is also assigned to the center (centroid) of that polygon — in this example, the center (80, 75) is set to white.</span></span> <span data-ttu-id="5844d-129">範例中的最後一個程式碼語句會使用路徑漸層筆刷來填滿矩形。</span><span class="sxs-lookup"><span data-stu-id="5844d-129">The final code statement in the example fills a rectangle with the path gradient brush.</span></span>

<span data-ttu-id="5844d-130">用來填滿矩形的色彩是 (80、75) 的白色，當您從 (80、75) 移至陣列中的點時，就會逐漸變更。</span><span class="sxs-lookup"><span data-stu-id="5844d-130">The color used to fill the rectangle is white at (80, 75) and changes gradually as you move away from (80, 75) toward the points in the array.</span></span> <span data-ttu-id="5844d-131">例如，當您從 (80、75) 移至 (0、0) 時，色彩會逐漸從白色變更為紅色，而當您從 (80，75) 移至 (160，0) 時，色彩會逐漸從白色變更為綠色。</span><span class="sxs-lookup"><span data-stu-id="5844d-131">For example, as you move from (80, 75) to (0, 0), the color changes gradually from white to red, and as you move from (80, 75) to (160, 0), the color changes gradually from white to green.</span></span>


```
// Construct a path gradient brush based on an array of points.
PointF ptsF[] = {PointF(0.0f, 0.0f), 
                 PointF(160.0f, 0.0f), 
                 PointF(160.0f, 200.0f),
                 PointF(80.0f, 150.0f),
                 PointF(0.0f, 200.0f)};

PathGradientBrush pBrush(ptsF, 5);

// An array of five points was used to construct the path gradient
// brush. Set the color of each point in that array.
Color colors[] = {Color(255, 255, 0, 0),  // (0, 0) red
                  Color(255, 0, 255, 0),  // (160, 0) green
                  Color(255, 0, 255, 0),  // (160, 200) green
                  Color(255, 0, 0, 255),  // (80, 150) blue
                  Color(255, 255, 0, 0)}; // (0, 200) red

int count = 5;
pBrush.SetSurroundColors(colors, &count);

// Set the center color to white.
pBrush.SetCenterColor(Color(255, 255, 255, 255));

// Use the path gradient brush to fill a rectangle.
graphics.FillRectangle(&pBrush, Rect(0, 0, 180, 220));
```



<span data-ttu-id="5844d-132">請注意，上述程式碼中沒有 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) 物件。</span><span class="sxs-lookup"><span data-stu-id="5844d-132">Note that there is no [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object in the preceding code.</span></span> <span data-ttu-id="5844d-133">範例中的特定 [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) 函式會接收指向陣列的指標，但不需要 **GraphicsPath** 物件。</span><span class="sxs-lookup"><span data-stu-id="5844d-133">The particular [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) constructor in the example receives a pointer to an array of points but does not require a **GraphicsPath** object.</span></span> <span data-ttu-id="5844d-134">另外也請注意，路徑漸層筆刷用來填滿矩形，而不是路徑。</span><span class="sxs-lookup"><span data-stu-id="5844d-134">Also, note that the path gradient brush is used to fill a rectangle, not a path.</span></span> <span data-ttu-id="5844d-135">矩形大於用來定義筆刷的路徑，因此，筆刷不會繪製某些矩形。</span><span class="sxs-lookup"><span data-stu-id="5844d-135">The rectangle is larger than the path used to define the brush, so some of the rectangle is not painted by the brush.</span></span> <span data-ttu-id="5844d-136">下圖顯示 (虛線) 的矩形，以及路徑漸層筆刷繪製的矩形部分。</span><span class="sxs-lookup"><span data-stu-id="5844d-136">The following illustration shows the rectangle (dotted line) and the portion of the rectangle painted by the path gradient brush.</span></span>

![顯示以虛線分隔的矩形（以多色彩漸層部分繪製）的圖例](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a><span data-ttu-id="5844d-138">自訂路徑漸層</span><span class="sxs-lookup"><span data-stu-id="5844d-138">Customizing a Path Gradient</span></span>

<span data-ttu-id="5844d-139">自訂路徑漸層筆刷的其中一種方式是設定其焦點比例。</span><span class="sxs-lookup"><span data-stu-id="5844d-139">One way to customize a path gradient brush is to set its focus scales.</span></span> <span data-ttu-id="5844d-140">焦點比例會指定位於主要路徑內的內部路徑。</span><span class="sxs-lookup"><span data-stu-id="5844d-140">The focus scales specify an inner path that lies inside the main path.</span></span> <span data-ttu-id="5844d-141">中間色彩會顯示在該內部路徑內的所有位置，而不是只顯示在中心點。</span><span class="sxs-lookup"><span data-stu-id="5844d-141">The center color is displayed everywhere inside that inner path rather than only at the center point.</span></span> <span data-ttu-id="5844d-142">若要設定路徑漸層筆刷的焦點比例，請呼叫 [**PathGradientBrush：： SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) 方法。</span><span class="sxs-lookup"><span data-stu-id="5844d-142">To set the focus scales of a path gradient brush, call the [**PathGradientBrush::SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) method.</span></span>

<span data-ttu-id="5844d-143">下列範例會根據橢圓形路徑建立路徑漸層筆刷。</span><span class="sxs-lookup"><span data-stu-id="5844d-143">The following example creates a path gradient brush based on an elliptical path.</span></span> <span data-ttu-id="5844d-144">程式碼會將界限色彩設定為藍色，將中間色彩設定為青色，然後使用路徑漸層筆刷來填滿橢圓路徑。</span><span class="sxs-lookup"><span data-stu-id="5844d-144">The code sets the boundary color to blue, sets the center color to aqua, and then uses the path gradient brush to fill the elliptical path.</span></span>

<span data-ttu-id="5844d-145">接下來，程式碼會設定路徑漸層筆刷的焦點縮放比例。</span><span class="sxs-lookup"><span data-stu-id="5844d-145">Next the code sets the focus scales of the path gradient brush.</span></span> <span data-ttu-id="5844d-146">X 焦點比例會設定為0.3，而 y 焦點尺規會設定為0.8。</span><span class="sxs-lookup"><span data-stu-id="5844d-146">The x focus scale is set to 0.3, and the y focus scale is set to 0.8.</span></span> <span data-ttu-id="5844d-147">程式碼會呼叫 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的 [**Graphics：： TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform)方法，以便後續的 [**graphics：： FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)呼叫會填滿位於第一個橢圓形右邊的省略號。</span><span class="sxs-lookup"><span data-stu-id="5844d-147">The code calls the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills an ellipse that sits to the right of the first ellipse.</span></span>

<span data-ttu-id="5844d-148">若要查看焦點尺規的效果，請想像將其中心與主要橢圓形共用的小橢圓形。</span><span class="sxs-lookup"><span data-stu-id="5844d-148">To see the effect of the focus scales, imagine a small ellipse that shares its center with the main ellipse.</span></span> <span data-ttu-id="5844d-149">小規模的 (內部) 橢圓形是以0.3 的比例水準縮放)  (的主要橢圓形，以及0.8 的因數垂直。</span><span class="sxs-lookup"><span data-stu-id="5844d-149">The small (inner) ellipse is the main ellipse scaled (about its center) horizontally by a factor of 0.3 and vertically by a factor of 0.8.</span></span> <span data-ttu-id="5844d-150">當您從外部橢圓形的界限移至內部橢圓形的界限時，色彩會從藍色逐漸變更為青色。</span><span class="sxs-lookup"><span data-stu-id="5844d-150">As you move from the boundary of the outer ellipse to the boundary of the inner ellipse, the color changes gradually from blue to aqua.</span></span> <span data-ttu-id="5844d-151">當您從內部橢圓形的界限移至共用中心時，色彩會維持綠色。</span><span class="sxs-lookup"><span data-stu-id="5844d-151">As you move from the boundary of the inner ellipse to the shared center, the color remains aqua.</span></span>


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 200, 100);

// Create a path gradient brush based on the elliptical path.
PathGradientBrush pthGrBrush(&path);
pthGrBrush.SetGammaCorrection(TRUE);

// Set the color along the entire boundary to blue.
Color color(Color(255, 0, 0, 255));
INT num = 1;
pthGrBrush.SetSurroundColors(&color, &num);

// Set the center color to aqua.
pthGrBrush.SetCenterColor(Color(255, 0, 255, 255));
 
// Use the path gradient brush to fill the ellipse. 
graphics.FillPath(&pthGrBrush, &path);

// Set the focus scales for the path gradient brush.
pthGrBrush.SetFocusScales(0.3f, 0.8f);

// Use the path gradient brush to fill the ellipse again.
// Show this filled ellipse to the right of the first filled ellipse.
graphics.TranslateTransform(220.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



<span data-ttu-id="5844d-152">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="5844d-152">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="5844d-153">左邊的橢圓形只有在中心點才會是綠色。</span><span class="sxs-lookup"><span data-stu-id="5844d-153">The ellipse on the left is aqua only at the center point.</span></span> <span data-ttu-id="5844d-154">右側的省略號在內部路徑內的任何地方都是綠色。</span><span class="sxs-lookup"><span data-stu-id="5844d-154">The ellipse on the right is aqua everywhere inside the inner path.</span></span>

![此圖顯示兩個從青色到藍色的省略號：第一個是淺綠色;第二個還有更多](images/focusscales1.png)

<span data-ttu-id="5844d-156">自訂路徑漸層筆刷的另一種方式，是指定預設色彩的陣列和插補位置的陣列。</span><span class="sxs-lookup"><span data-stu-id="5844d-156">Another way to customize a path gradient brush is to specify an array of preset colors and an array of interpolation positions.</span></span>

<span data-ttu-id="5844d-157">下列範例會根據三角形建立路徑漸層筆刷。</span><span class="sxs-lookup"><span data-stu-id="5844d-157">The following example creates a path gradient brush based on a triangle.</span></span> <span data-ttu-id="5844d-158">程式碼會呼叫路徑漸層筆刷的 [**PathGradientBrush：： SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) 方法，以指定插補色彩的陣列 (深綠色、青色、藍色) 和插補位置陣列 (0、0.25、1) 。</span><span class="sxs-lookup"><span data-stu-id="5844d-158">The code calls the [**PathGradientBrush::SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) method of the path gradient brush to specify an array of interpolation colors (dark green, aqua, blue) and an array of interpolation positions (0, 0.25, 1).</span></span> <span data-ttu-id="5844d-159">當您從三角形的界限移至中央點時，色彩會逐漸從深綠色變成青色，然後從青色變成藍色。</span><span class="sxs-lookup"><span data-stu-id="5844d-159">As you move from the boundary of the triangle to the center point, the color changes gradually from dark green to aqua and then from aqua to blue.</span></span> <span data-ttu-id="5844d-160">從深綠色變成青色的變更會在25% 的距離之間，從深綠色到藍色。</span><span class="sxs-lookup"><span data-stu-id="5844d-160">The change from dark green to aqua happens in 25 percent of the distance from dark green to blue.</span></span>


```
// Vertices of the triangle
Point points[] = {Point(100, 0), 
                  Point(200, 200), 
                  Point(0, 200)};

// No GraphicsPath object is created. The PathGradient
// brush is constructed directly from the array of points.
PathGradientBrush pthGrBrush(points, 3);

Color presetColors[] = {
   Color(255, 0, 128, 0),    // Dark green
   Color(255, 0, 255, 255),  // Aqua
   Color(255, 0, 0, 255)};   // Blue

REAL interpPositions[] = {
   0.0f,   // Dark green is at the boundary of the triangle.
   0.25f,  // Aqua is 25 percent of the way from the boundary
           // to the center point.
   1.0f};  // Blue is at the center point.
                  
pthGrBrush.SetInterpolationColors(presetColors, interpPositions, 3);

// Fill a rectangle that is larger than the triangle
// specified in the Point array. The portion of the
// rectangle outside the triangle will not be painted.
graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);
```



<span data-ttu-id="5844d-161">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="5844d-161">The following illustration shows the output of the preceding code.</span></span>

![圖例顯示三角形，從中間的藍色到淺綠色，到邊緣的綠色](images/pathgradient4.png)

## <a name="setting-the-center-point"></a><span data-ttu-id="5844d-163">設定中心點</span><span class="sxs-lookup"><span data-stu-id="5844d-163">Setting the Center Point</span></span>

<span data-ttu-id="5844d-164">根據預設，路徑漸層筆刷的中心點是在用來建立筆刷的路徑距心。</span><span class="sxs-lookup"><span data-stu-id="5844d-164">By default, the center point of a path gradient brush is at the centroid of the path used to construct the brush.</span></span> <span data-ttu-id="5844d-165">您可以藉由呼叫 [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush)類別的 [**PathGradientBrush：： SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_))方法，來變更中心點的位置。</span><span class="sxs-lookup"><span data-stu-id="5844d-165">You can change the location of the center point by calling the [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) method of the [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class.</span></span>

<span data-ttu-id="5844d-166">下列範例會根據橢圓形建立路徑漸層筆刷。</span><span class="sxs-lookup"><span data-stu-id="5844d-166">The following example creates a path gradient brush based on an ellipse.</span></span> <span data-ttu-id="5844d-167">橢圓形的中心位於 (70、35) ，但路徑漸層筆刷的中心點設定為 (120，40) 。</span><span class="sxs-lookup"><span data-stu-id="5844d-167">The center of the ellipse is at (70, 35), but the center point of the path gradient brush is set to (120, 40).</span></span>


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the center point to a location that is not the centroid of the path.
pthGrBrush.SetCenterPoint(Point(120, 40));

// Set the color at the center point to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



<span data-ttu-id="5844d-168">下圖顯示已填滿的橢圓形和軌跡漸層筆刷的中心點。</span><span class="sxs-lookup"><span data-stu-id="5844d-168">The following illustration shows the filled ellipse and the center point of the path gradient brush.</span></span>

![圖例顯示從接近一端的中心點填滿藍色至淺綠色的橢圓形](images/pathgradient5.png)

<span data-ttu-id="5844d-170">您可以將路徑漸層筆刷的中心點設定為用來建立筆刷的路徑之外的位置。</span><span class="sxs-lookup"><span data-stu-id="5844d-170">You can set the center point of a path gradient brush to a location outside the path that was used to construct the brush.</span></span> <span data-ttu-id="5844d-171">在上述程式碼中，如果您將 [**PathGradientBrush：： SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) 的呼叫取代為 `pthGrBrush.SetCenterPoint(Point(145, 35))` ，您將會得到下列結果。</span><span class="sxs-lookup"><span data-stu-id="5844d-171">In the preceding code, if you replace the call to [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) with `pthGrBrush.SetCenterPoint(Point(145, 35))`, you will get the following result.</span></span>

![顯示橢圓形的圖例，從位於橢圓形邊緣以外的中心點填滿紅色到黃色](images/pathgradient6.png)

<span data-ttu-id="5844d-173">在上圖中，位於橢圓形最右邊的點並不是純藍色 (雖然它們非常接近) 。</span><span class="sxs-lookup"><span data-stu-id="5844d-173">In the preceding illustration, the points at the far right of the ellipse are not pure blue (although they are very close).</span></span> <span data-ttu-id="5844d-174">漸層中的色彩會被視為已允許填滿 (145，35) ，而色彩則已達到純藍色 (0、0、255) 。</span><span class="sxs-lookup"><span data-stu-id="5844d-174">The colors in the gradient are positioned as if the fill had been allowed to reach the point (145, 35), the color would have reached pure blue (0, 0, 255).</span></span> <span data-ttu-id="5844d-175">但填滿永遠不會達到 (145，35) ，因為路徑漸層筆刷只會在其路徑內繪製。</span><span class="sxs-lookup"><span data-stu-id="5844d-175">But the fill never reaches (145, 35) because a path gradient brush paints only inside its path.</span></span>

 

 
