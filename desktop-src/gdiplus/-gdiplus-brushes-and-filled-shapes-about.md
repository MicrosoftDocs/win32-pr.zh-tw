---
description: 封閉的圖形（例如矩形或橢圓形）包含外框和內部。
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: 筆刷和填滿的圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558427"
---
# <a name="brushes-and-filled-shapes"></a><span data-ttu-id="8f367-103">筆刷和填滿的圖形</span><span class="sxs-lookup"><span data-stu-id="8f367-103">Brushes and Filled Shapes</span></span>

<span data-ttu-id="8f367-104">封閉的圖形（例如矩形或橢圓形）包含外框和內部。</span><span class="sxs-lookup"><span data-stu-id="8f367-104">A closed figure such as a rectangle or an ellipse consists of an outline and an interior.</span></span> <span data-ttu-id="8f367-105">大綱是以 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件繪製，而內部則填滿筆 [**刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件。</span><span class="sxs-lookup"><span data-stu-id="8f367-105">The outline is drawn with a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and the interior is filled with a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="8f367-106">Windows GDI + 提供數個筆刷類別來填滿封閉的圖形： [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)、 [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush)、 [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)、 [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)和 [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)。</span><span class="sxs-lookup"><span data-stu-id="8f367-106">Windows GDI+ provides several brush classes for filling the interiors of closed figures: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), and [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span></span> <span data-ttu-id="8f367-107">所有這些類別都是繼承自 **筆刷** 類別。</span><span class="sxs-lookup"><span data-stu-id="8f367-107">All these classes inherit from the **Brush** class.</span></span> <span data-ttu-id="8f367-108">下圖顯示填滿實心筆刷的矩形，以及填滿影線筆刷的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="8f367-108">The following illustration shows a rectangle filled with a solid brush and an ellipse filled with a hatch brush.</span></span>

![顯示藍色矩形的圖例，以及填滿藍色影線圖樣的洋紅橢圓形](images/aboutgdip02-art17.png)

 

-   [<span data-ttu-id="8f367-110">實心筆刷</span><span class="sxs-lookup"><span data-stu-id="8f367-110">Solid Brushes</span></span>](#solid-brushes)
-   [<span data-ttu-id="8f367-111">影線筆刷</span><span class="sxs-lookup"><span data-stu-id="8f367-111">Hatch Brushes</span></span>](#hatch-brushes)
-   [<span data-ttu-id="8f367-112">材質筆刷</span><span class="sxs-lookup"><span data-stu-id="8f367-112">Texture Brushes</span></span>](#texture-brushes)
-   [<span data-ttu-id="8f367-113">漸層筆刷</span><span class="sxs-lookup"><span data-stu-id="8f367-113">Gradient Brushes</span></span>](#gradient-brushes)

## <a name="solid-brushes"></a><span data-ttu-id="8f367-114">實心筆刷</span><span class="sxs-lookup"><span data-stu-id="8f367-114">Solid Brushes</span></span>

<span data-ttu-id="8f367-115">若要填滿封閉的圖形，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 [**筆刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件。</span><span class="sxs-lookup"><span data-stu-id="8f367-115">To fill a closed shape, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="8f367-116">**Graphics** 物件提供方法（例如 [graphicswindow.fillrectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_))和 [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_))），而 **筆刷** 物件會儲存填滿的屬性，例如色彩和模式。</span><span class="sxs-lookup"><span data-stu-id="8f367-116">The **Graphics** object provides methods, such as [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) and [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), and the **Brush** object stores attributes of the fill, such as color and pattern.</span></span> <span data-ttu-id="8f367-117">**筆刷** 物件的位址會做為 fill 方法的其中一個引數傳遞。</span><span class="sxs-lookup"><span data-stu-id="8f367-117">The address of the **Brush** object is passed as one of the arguments to the fill method.</span></span> <span data-ttu-id="8f367-118">下列範例會以紅色的紅色色彩填滿橢圓形。</span><span class="sxs-lookup"><span data-stu-id="8f367-118">The following example fills an ellipse with a solid red color.</span></span>


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



<span data-ttu-id="8f367-119">請注意，在上述範例中，筆刷的型別為 [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)，其繼承自 [**筆刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush)。</span><span class="sxs-lookup"><span data-stu-id="8f367-119">Note that in the preceding example, the brush is of type [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), which inherits from [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).</span></span>

## <a name="hatch-brushes"></a><span data-ttu-id="8f367-120">影線筆刷</span><span class="sxs-lookup"><span data-stu-id="8f367-120">Hatch Brushes</span></span>

<span data-ttu-id="8f367-121">當您填滿具有影線筆刷的圖形時，您會指定前景色彩、背景色彩和影線樣式。</span><span class="sxs-lookup"><span data-stu-id="8f367-121">When you fill a shape with a hatch brush, you specify a foreground color, a background color, and a hatch style.</span></span> <span data-ttu-id="8f367-122">前景色彩是影線的色彩。</span><span class="sxs-lookup"><span data-stu-id="8f367-122">The foreground color is the color of the hatching.</span></span>


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



<span data-ttu-id="8f367-123">GDI + 提供超過50的影線樣式，在 [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle)中指定。</span><span class="sxs-lookup"><span data-stu-id="8f367-123">GDI+ provides more than 50 hatch styles, specified in [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle).</span></span> <span data-ttu-id="8f367-124">下圖顯示的三種樣式為水準、ForwardDiagonal 和交叉。</span><span class="sxs-lookup"><span data-stu-id="8f367-124">The three styles shown in the following illustration are Horizontal, ForwardDiagonal, and Cross.</span></span>

![顯示三個青灰色橢圓形的圖例，各有不同的影線樣式](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a><span data-ttu-id="8f367-126">材質筆刷</span><span class="sxs-lookup"><span data-stu-id="8f367-126">Texture Brushes</span></span>

<span data-ttu-id="8f367-127">您可以使用紋理筆刷，以點陣圖中儲存的模式來填滿圖形。</span><span class="sxs-lookup"><span data-stu-id="8f367-127">With a texture brush, you can fill a shape with a pattern stored in a bitmap.</span></span> <span data-ttu-id="8f367-128">例如，假設下圖儲存在名為 MyTexture.bmp 的磁片檔中。</span><span class="sxs-lookup"><span data-stu-id="8f367-128">For example, suppose the following picture is stored in a disk file named MyTexture.bmp.</span></span>

![以各種色彩填滿之小方塊的螢幕擷取畫面](images/aboutgdip02-art19.png)

<span data-ttu-id="8f367-130&quot;>下列範例會藉由重複儲存在 MyTexture.bmp 中的圖片來填滿橢圓形。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8f367-130&quot;>The following example fills an ellipse by repeating the picture stored in MyTexture.bmp.</span></span>


```
Image myImage(L&quot;MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



<span data-ttu-id="8f367-131">下圖顯示已填滿的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="8f367-131">The following illustration shows the filled ellipse.</span></span>

![顯示填滿先前定義之模式的省略號的圖例](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a><span data-ttu-id="8f367-133">漸層筆刷</span><span class="sxs-lookup"><span data-stu-id="8f367-133">Gradient Brushes</span></span>

<span data-ttu-id="8f367-134">您可以使用漸層筆刷來填滿圖形，其色彩會從圖形的某個部分逐漸變更為另一個部分。</span><span class="sxs-lookup"><span data-stu-id="8f367-134">You can use a gradient brush to fill a shape with a color that changes gradually from one part of the shape to another.</span></span> <span data-ttu-id="8f367-135">例如，當您從圖表的左邊移至右側時，水準漸層筆刷將會變更色彩。</span><span class="sxs-lookup"><span data-stu-id="8f367-135">For example, a horizontal gradient brush will change color as you move from the left side of a figure to the right side.</span></span> <span data-ttu-id="8f367-136">下列範例會填滿具有水準漸層筆刷的橢圓形，當您從橢圓形的左邊移至右側時，會從藍色變更為綠色。</span><span class="sxs-lookup"><span data-stu-id="8f367-136">The following example fills an ellipse with a horizontal gradient brush that changes from blue to green as you move from the left side of the ellipse to the right side.</span></span>


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



<span data-ttu-id="8f367-137">下圖顯示已填滿的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="8f367-137">The following illustration shows the filled ellipse.</span></span>

![圖例顯示具有漸層填滿的橢圓形：左邊的藍色靠右至綠色](images/aboutgdip02-art21.png)

<span data-ttu-id="8f367-139">路徑漸層筆刷可以設定為當您從圖表的中心移到界限時變更色彩。</span><span class="sxs-lookup"><span data-stu-id="8f367-139">A path gradient brush can be configured to change color as you move from the center of a figure toward the boundary.</span></span>

![ilustration 置中為深藍色的橢圓形，邊緣的陰影至淺藍色](images/aboutgdip02-art22.png)

<span data-ttu-id="8f367-141">路徑漸層筆刷相當有彈性。</span><span class="sxs-lookup"><span data-stu-id="8f367-141">Path gradient brushes are quite flexible.</span></span> <span data-ttu-id="8f367-142">用來填滿下圖中三角形的漸層筆刷，會從中間的紅色逐漸變成頂點的三種不同色彩。</span><span class="sxs-lookup"><span data-stu-id="8f367-142">The gradient brush used to fill the triangle in the following illustration changes gradually from red at the center to each of three different colors at the vertices.</span></span>

![在中間以紅色表示的三角形圖例，每個頂點的色彩為不同的色彩](images/aboutgdip02-art23.png)

 

 



