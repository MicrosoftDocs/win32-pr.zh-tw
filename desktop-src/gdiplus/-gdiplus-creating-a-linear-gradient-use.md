---
description: GDI + 提供水準、垂直和對角線的線性漸層。 依預設，線性漸層中的色彩會以一致的方式變更。 不過，您可以自訂線性漸層，讓色彩以非一致的方式變更。
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: 建立線性漸層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d66b9f5a3a07061e8b3d19140c25a9f3a33052a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550529"
---
# <a name="creating-a-linear-gradient"></a><span data-ttu-id="ae51c-105">建立線性漸層</span><span class="sxs-lookup"><span data-stu-id="ae51c-105">Creating a Linear Gradient</span></span>

<span data-ttu-id="ae51c-106">GDI + 提供水準、垂直和對角線的線性漸層。</span><span class="sxs-lookup"><span data-stu-id="ae51c-106">GDI+ provides horizontal, vertical, and diagonal linear gradients.</span></span> <span data-ttu-id="ae51c-107">依預設，線性漸層中的色彩會以一致的方式變更。</span><span class="sxs-lookup"><span data-stu-id="ae51c-107">By default, the color in a linear gradient changes uniformly.</span></span> <span data-ttu-id="ae51c-108">不過，您可以自訂線性漸層，讓色彩以非一致的方式變更。</span><span class="sxs-lookup"><span data-stu-id="ae51c-108">However, you can customize a linear gradient so that the color changes in a non-uniform fashion.</span></span>

-   [<span data-ttu-id="ae51c-109">水平線性漸層</span><span class="sxs-lookup"><span data-stu-id="ae51c-109">Horizontal Linear Gradients</span></span>](#horizontal-linear-gradients)
-   [<span data-ttu-id="ae51c-110">自訂線性漸層</span><span class="sxs-lookup"><span data-stu-id="ae51c-110">Customizing Linear Gradients</span></span>](#customizing-linear-gradients)
-   [<span data-ttu-id="ae51c-111">對角線的線性漸層</span><span class="sxs-lookup"><span data-stu-id="ae51c-111">Diagonal Linear Gradients</span></span>](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a><span data-ttu-id="ae51c-112">水平線性漸層</span><span class="sxs-lookup"><span data-stu-id="ae51c-112">Horizontal Linear Gradients</span></span>

<span data-ttu-id="ae51c-113">下列範例會使用水平線性漸層筆刷來填滿線條、橢圓形和矩形：</span><span class="sxs-lookup"><span data-stu-id="ae51c-113">The following example uses a horizontal linear gradient brush to fill a line, an ellipse, and a rectangle:</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // opaque red
   Color(255, 0, 0, 255));  // opaque blue

Pen pen(&linGrBrush);

graphics.DrawLine(&pen, 0, 10, 200, 10);
graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



<span data-ttu-id="ae51c-114">[**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)的函式會接收四個引數：兩個點和兩個色彩。</span><span class="sxs-lookup"><span data-stu-id="ae51c-114">The [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor receives four arguments: two points and two colors.</span></span> <span data-ttu-id="ae51c-115">第一個點 (0、10) 會與第一個色彩 (紅色) 相關聯，而第二個點 (200，10) 會與第二個色彩 (藍色) 相關聯。</span><span class="sxs-lookup"><span data-stu-id="ae51c-115">The first point (0, 10) is associated with the first color (red), and the second point (200, 10) is associated with the second color (blue).</span></span> <span data-ttu-id="ae51c-116">如您所預期，從 (0、10) 到 (200）繪製的線條，10) 變更從紅色逐漸變成藍色。</span><span class="sxs-lookup"><span data-stu-id="ae51c-116">As you would expect, the line drawn from (0, 10) to (200, 10) changes gradually from red to blue.</span></span>

<span data-ttu-id="ae51c-117">點中的 10s (50、10) 和 (200，10) 並不重要。</span><span class="sxs-lookup"><span data-stu-id="ae51c-117">The 10s in the points (50, 10) and (200, 10) are not important.</span></span> <span data-ttu-id="ae51c-118">重要的是，兩個點都有相同的第二個座標，也就是將它們連接的線條是水準的。</span><span class="sxs-lookup"><span data-stu-id="ae51c-118">What's important is that the two points have the same second coordinate — the line connecting them is horizontal.</span></span> <span data-ttu-id="ae51c-119">由於水準座標是從0到200，因此橢圓形和矩形也會從紅色逐漸變更為藍色。</span><span class="sxs-lookup"><span data-stu-id="ae51c-119">The ellipse and the rectangle also change gradually from red to blue as the horizontal coordinate goes from 0 to 200.</span></span>

<span data-ttu-id="ae51c-120">下圖顯示線條、橢圓形和矩形。</span><span class="sxs-lookup"><span data-stu-id="ae51c-120">The following illustration shows the line, the ellipse, and the rectangle.</span></span> <span data-ttu-id="ae51c-121">請注意，色彩漸層會在水準座標增加超過200的情況下自行重複。</span><span class="sxs-lookup"><span data-stu-id="ae51c-121">Note that the color gradient repeats itself as the horizontal coordinate increases beyond 200.</span></span>

![圖例顯示水準漸層，其填滿線條和橢圓形，以及長度超過橢圓形的矩形](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a><span data-ttu-id="ae51c-123">自訂線性漸層</span><span class="sxs-lookup"><span data-stu-id="ae51c-123">Customizing Linear Gradients</span></span>

<span data-ttu-id="ae51c-124">在上述範例中，當您從水準座標0移至200的水準座標時，色彩元件會呈線性變化。</span><span class="sxs-lookup"><span data-stu-id="ae51c-124">In the preceding example, the color components change linearly as you move from a horizontal coordinate of 0 to a horizontal coordinate of 200.</span></span> <span data-ttu-id="ae51c-125">例如，其第一個座標是介於0到200的中間點，會有一個藍色元件，介於0到255的中間。</span><span class="sxs-lookup"><span data-stu-id="ae51c-125">For example, a point whose first coordinate is halfway between 0 and 200 will have a blue component that is halfway between 0 and 255.</span></span>

<span data-ttu-id="ae51c-126">GDI + 可讓您調整從漸層的某個邊緣到另一個邊緣的色彩變化方式。</span><span class="sxs-lookup"><span data-stu-id="ae51c-126">GDI+ allows you to adjust the way a color varies from one edge of a gradient to the other.</span></span> <span data-ttu-id="ae51c-127">假設您想要根據下表建立從黑色變更為紅色的漸層筆刷。</span><span class="sxs-lookup"><span data-stu-id="ae51c-127">Suppose you want to create a gradient brush that changes from black to red according to the following table.</span></span>



| <span data-ttu-id="ae51c-128">水準座標</span><span class="sxs-lookup"><span data-stu-id="ae51c-128">Horizontal coordinate</span></span> | <span data-ttu-id="ae51c-129">RGB 元件</span><span class="sxs-lookup"><span data-stu-id="ae51c-129">RGB components</span></span> |
|-----------------------|----------------|
| <span data-ttu-id="ae51c-130">0</span><span class="sxs-lookup"><span data-stu-id="ae51c-130">0</span></span>                     | <span data-ttu-id="ae51c-131">(0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="ae51c-131">(0, 0, 0)</span></span>      |
| <span data-ttu-id="ae51c-132">40</span><span class="sxs-lookup"><span data-stu-id="ae51c-132">40</span></span>                    | <span data-ttu-id="ae51c-133">(128, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="ae51c-133">(128, 0, 0)</span></span>    |
| <span data-ttu-id="ae51c-134">200</span><span class="sxs-lookup"><span data-stu-id="ae51c-134">200</span></span>                   | <span data-ttu-id="ae51c-135">(255, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="ae51c-135">(255, 0, 0)</span></span>    |



 

<span data-ttu-id="ae51c-136">請注意，當水準座標只是從0到200的20% 時，紅色元件的一半濃度。</span><span class="sxs-lookup"><span data-stu-id="ae51c-136">Note that the red component is at half intensity when the horizontal coordinate is only 20 percent of the way from 0 to 200.</span></span>

<span data-ttu-id="ae51c-137">下列範例會呼叫 [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)物件的 [**LinearGradientBrush：： SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend)方法，將三個相對濃度與三個相對位置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ae51c-137">The following example calls the [**LinearGradientBrush::SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) method of a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) object to associate three relative intensities with three relative positions.</span></span> <span data-ttu-id="ae51c-138">如上表所示，0.5 的相對濃度與0.2 的相對位置相關聯。</span><span class="sxs-lookup"><span data-stu-id="ae51c-138">As in the preceding table, a relative intensity of 0.5 is associated with a relative position of 0.2.</span></span> <span data-ttu-id="ae51c-139">程式碼會以漸層筆刷填滿橢圓形和矩形。</span><span class="sxs-lookup"><span data-stu-id="ae51c-139">The code fills an ellipse and a rectangle with the gradient brush.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 0, 0, 0),     // opaque black 
   Color(255, 255, 0, 0));  // opaque red

REAL relativeIntensities[] = {0.0f, 0.5f, 1.0f};
REAL relativePositions[]   = {0.0f, 0.2f, 1.0f};

linGrBrush.SetBlend(relativeIntensities, relativePositions, 3);

graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



<span data-ttu-id="ae51c-140">下圖顯示產生的橢圓形和矩形。</span><span class="sxs-lookup"><span data-stu-id="ae51c-140">The following illustration shows the resulting ellipse and rectangle.</span></span>

![圖例顯示水準漸層，其會填滿小於橢圓形的橢圓形和矩形](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a><span data-ttu-id="ae51c-142">對角線的線性漸層</span><span class="sxs-lookup"><span data-stu-id="ae51c-142">Diagonal Linear Gradients</span></span>

<span data-ttu-id="ae51c-143">上述範例中的漸層是水準的;也就是說，當您沿著任何水平線移動時，色彩會逐漸變更。</span><span class="sxs-lookup"><span data-stu-id="ae51c-143">The gradients in the preceding examples have been horizontal; that is, the color changes gradually as you move along any horizontal line.</span></span> <span data-ttu-id="ae51c-144">您也可以定義垂直漸層和對角線漸層。</span><span class="sxs-lookup"><span data-stu-id="ae51c-144">You can also define vertical gradients and diagonal gradients.</span></span> <span data-ttu-id="ae51c-145">下列程式碼會將 (0、0) 和 (200，100) 的點傳遞至 [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) 的函式。</span><span class="sxs-lookup"><span data-stu-id="ae51c-145">The following code passes the points (0, 0) and (200, 100) to a [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) constructor.</span></span> <span data-ttu-id="ae51c-146">藍色的色彩與 (0、0) ，而綠色的色彩則與 (200，100) 相關聯。</span><span class="sxs-lookup"><span data-stu-id="ae51c-146">The color blue is associated with (0, 0), and the color green is associated with (200, 100).</span></span> <span data-ttu-id="ae51c-147">具有畫筆寬度 10) 的線條 (，並以線性漸層筆刷填滿橢圓形。</span><span class="sxs-lookup"><span data-stu-id="ae51c-147">A line (with pen width 10) and an ellipse are filled with the linear gradient brush.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 0),
   Point(200, 100),
   Color(255, 0, 0, 255),   // opaque blue
   Color(255, 0, 255, 0));  // opaque green

Pen pen(&linGrBrush, 10);

graphics.DrawLine(&pen, 0, 0, 600, 300);
graphics.FillEllipse(&linGrBrush, 10, 100, 200, 100);
```



<span data-ttu-id="ae51c-148">下圖顯示線條和橢圓形。</span><span class="sxs-lookup"><span data-stu-id="ae51c-148">The following illustration shows the line and the ellipse.</span></span> <span data-ttu-id="ae51c-149">請注意，當您沿著任何直線移動到直線，而該線條與通過 (0、0) 和 (200，100) 之間的任何直線移動時，橢圓形中的色彩會逐漸變更。</span><span class="sxs-lookup"><span data-stu-id="ae51c-149">Note that the color in the ellipse changes gradually as you move along any line that is parallel to the line passing through (0, 0) and (200, 100).</span></span>

![圖例顯示填滿橢圓形和對角線的對角線漸層](images/lineargradient3.png)

 

 



