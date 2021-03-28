---
description: Windows GDI + 提供可讓您用來在繪圖物件中暫時取代或增強部分狀態的容器。
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: 巢狀圖形容器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f9d9feac3494b423d844cb1e3da359af33eaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943946"
---
# <a name="nested-graphics-containers"></a><span data-ttu-id="c4561-103">巢狀圖形容器</span><span class="sxs-lookup"><span data-stu-id="c4561-103">Nested Graphics Containers</span></span>

<span data-ttu-id="c4561-104">Windows GDI + 提供可讓您用來在 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件中暫時取代或增強部分狀態的容器。</span><span class="sxs-lookup"><span data-stu-id="c4561-104">Windows GDI+ provides containers that you can use to temporarily replace or augment part of the state in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="c4561-105">您可以藉由呼叫 **graphics** 物件的 [**Graphics：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))方法來建立容器。</span><span class="sxs-lookup"><span data-stu-id="c4561-105">You create a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object.</span></span> <span data-ttu-id="c4561-106">您可以重複呼叫 **Graphics：： BeginContainer** 來形成嵌套的容器。</span><span class="sxs-lookup"><span data-stu-id="c4561-106">You can call **Graphics::BeginContainer** repeatedly to form nested containers.</span></span>

## <a name="transformations-in-nested-containers"></a><span data-ttu-id="c4561-107">嵌套容器中的轉換</span><span class="sxs-lookup"><span data-stu-id="c4561-107">Transformations in Nested Containers</span></span>

<span data-ttu-id="c4561-108">下列範例會在該 **圖形** 物件中建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件和容器。</span><span class="sxs-lookup"><span data-stu-id="c4561-108">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="c4561-109">**圖形** 物件的世界轉換是 x 方向的平移100單位和 y 方向的80單位。</span><span class="sxs-lookup"><span data-stu-id="c4561-109">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="c4561-110">容器的世界轉換是30度的旋轉。</span><span class="sxs-lookup"><span data-stu-id="c4561-110">The world transformation of the container is a 30-degree rotation.</span></span> <span data-ttu-id="c4561-111">程式碼會進行呼叫</span><span class="sxs-lookup"><span data-stu-id="c4561-111">The code makes the call</span></span>


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



<span data-ttu-id="c4561-112">兩次。</span><span class="sxs-lookup"><span data-stu-id="c4561-112">twice.</span></span> <span data-ttu-id="c4561-113">第一次呼叫 [**圖形：:D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) 在 *容器內*;也就是說，呼叫 [**圖形：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) 與 [**Graphics：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)之間的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c4561-113">The first call to [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is *inside the container*; that is, the call is in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer).</span></span> <span data-ttu-id="c4561-114">第二次呼叫 **圖形：:D rawrectangle** 在呼叫 **Graphics：： EndContainer** 之後。</span><span class="sxs-lookup"><span data-stu-id="c4561-114">The second call to **Graphics::DrawRectangle** is after the call to **Graphics::EndContainer**.</span></span>


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



<span data-ttu-id="c4561-115">在上述程式碼中，從容器內繪製的矩形會先由容器的世界轉換 (旋轉) ，然後由 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界轉換 (轉譯) 進行轉換。</span><span class="sxs-lookup"><span data-stu-id="c4561-115">In the preceding code, the rectangle drawn from inside the container is transformed first by the world transformation of the container (rotation) and then by the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object (translation).</span></span> <span data-ttu-id="c4561-116">從容器外部繪製的矩形只會在 **圖形** 物件的世界轉換 (轉譯) 轉換。</span><span class="sxs-lookup"><span data-stu-id="c4561-116">The rectangle drawn from outside the container is transformed only by the world transformation of the **Graphics** object (translation).</span></span> <span data-ttu-id="c4561-117">下圖顯示兩個矩形。</span><span class="sxs-lookup"><span data-stu-id="c4561-117">The following illustration shows the two rectangles.</span></span>

![視窗的螢幕擷取畫面，其中有兩個紅色矩形位於相同的點，但有不同的旋轉](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a><span data-ttu-id="c4561-119">在嵌套容器中裁剪</span><span class="sxs-lookup"><span data-stu-id="c4561-119">Clipping in Nested Containers</span></span>

<span data-ttu-id="c4561-120">下列範例說明嵌套容器如何處理裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="c4561-120">The following example illustrates how nested containers handle clipping regions.</span></span> <span data-ttu-id="c4561-121">程式碼會建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和該 **圖形** 物件內的容器。</span><span class="sxs-lookup"><span data-stu-id="c4561-121">The code creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container within that **Graphics** object.</span></span> <span data-ttu-id="c4561-122">**圖形** 物件的裁剪區域是一個矩形，而容器的裁剪區域則是一個橢圓形。</span><span class="sxs-lookup"><span data-stu-id="c4561-122">The clipping region of the **Graphics** object is a rectangle, and the clipping region of the container is an ellipse.</span></span> <span data-ttu-id="c4561-123">此程式碼會對圖形進行兩個呼叫 [**：:D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) 方法。</span><span class="sxs-lookup"><span data-stu-id="c4561-123">The code makes two calls to the [**Graphics::DrawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method.</span></span> <span data-ttu-id="c4561-124">第一次呼叫 **圖形：:D rawline** 在容器內，而第二次呼叫圖形 **：:D rawline** 是在呼叫 [**Graphics：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)) 之後 (容器之外。</span><span class="sxs-lookup"><span data-stu-id="c4561-124">The first call to **Graphics::DrawLine** is inside the container, and the second call to **Graphics::DrawLine** is outside the container (after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="c4561-125">這兩個裁剪區域的交集會裁剪第一行。</span><span class="sxs-lookup"><span data-stu-id="c4561-125">The first line is clipped by the intersection of the two clipping regions.</span></span> <span data-ttu-id="c4561-126">第二行只會由 **圖形** 物件的矩形裁剪區域裁剪。</span><span class="sxs-lookup"><span data-stu-id="c4561-126">The second line is clipped only by the rectangular clipping region of the **Graphics** object.</span></span>


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



<span data-ttu-id="c4561-127">下圖顯示兩個剪下的行。</span><span class="sxs-lookup"><span data-stu-id="c4561-127">The following illustration shows the two clipped lines.</span></span>

![矩形內橢圓形的圖例，其中有一個線條由橢圓形剪下，另一個線條由矩形裁剪](images/nestedcontainers2.png)

<span data-ttu-id="c4561-129">如同上述兩個範例所示，轉換和裁剪區域在嵌套的容器中是累計的。</span><span class="sxs-lookup"><span data-stu-id="c4561-129">As the two preceding examples show, transformations and clipping regions are cumulative in nested containers.</span></span> <span data-ttu-id="c4561-130">如果您設定容器和 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界轉換，則這兩種轉換將會套用至從容器內繪製的專案。</span><span class="sxs-lookup"><span data-stu-id="c4561-130">If you set the world transformations of the container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, both transformations will apply to items drawn from inside the container.</span></span> <span data-ttu-id="c4561-131">容器的轉換將會先套用，而 **圖形** 物件的轉換將會第二個套用。</span><span class="sxs-lookup"><span data-stu-id="c4561-131">The transformation of the container will be applied first, and the transformation of the **Graphics** object will be applied second.</span></span> <span data-ttu-id="c4561-132">如果您設定容器和 **圖形** 物件的裁剪區域，則從容器內繪製的專案將會被兩個裁剪區域的交集所修剪。</span><span class="sxs-lookup"><span data-stu-id="c4561-132">If you set the clipping regions of the container and the **Graphics** object, items drawn from inside the container will be clipped by the intersection of the two clipping regions.</span></span>

## <a name="quality-settings-in-nested-containers"></a><span data-ttu-id="c4561-133">嵌套容器中的品質設定</span><span class="sxs-lookup"><span data-stu-id="c4561-133">Quality Settings in Nested Containers</span></span>

<span data-ttu-id="c4561-134">在嵌套容器中 ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)、 [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)和 like) 的品質設定不是累積的;相反地，容器的品質設定會暫時取代 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的品質設定。</span><span class="sxs-lookup"><span data-stu-id="c4561-134">Quality settings ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the like) in nested containers are not cumulative; rather, the quality settings of the container temporarily replace the quality settings of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="c4561-135">當您建立新的容器時，該容器的品質設定會設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="c4561-135">When you create a new container, the quality settings for that container are set to default values.</span></span> <span data-ttu-id="c4561-136">例如，假設您有一個具有平滑模式 [\* \* \* \* SmoothingModeAntiAlias \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)\* \* 的 **圖形** 物件。</span><span class="sxs-lookup"><span data-stu-id="c4561-136">For example, suppose you have a **Graphics** object with a smoothing mode of [\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode).</span></span> <span data-ttu-id="c4561-137">當您建立容器時，容器內的平滑模式是預設的平滑模式。</span><span class="sxs-lookup"><span data-stu-id="c4561-137">When you create a container, the smoothing mode inside the container is the default smoothing mode.</span></span> <span data-ttu-id="c4561-138">您可以自由設定容器的平滑模式，而從容器內繪製的任何專案都會根據您設定的模式繪製。</span><span class="sxs-lookup"><span data-stu-id="c4561-138">You are free to set the smoothing mode of the container, and any items drawn from inside the container will be drawn according to the mode you set.</span></span> <span data-ttu-id="c4561-139">在呼叫 [**圖形：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)之後繪製的專案，將會根據在 [**圖形：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))的呼叫之前所處的平滑模式 ([\* \* \* \* SmoothingModeAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) \*) 繪製。</span><span class="sxs-lookup"><span data-stu-id="c4561-139">Items drawn after the call to [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will be drawn according to the smoothing mode ([\*\*\*\*SmoothingModeAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)) that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

## <a name="several-layers-of-nested-containers"></a><span data-ttu-id="c4561-140">多層的嵌套容器</span><span class="sxs-lookup"><span data-stu-id="c4561-140">Several Layers of Nested Containers</span></span>

<span data-ttu-id="c4561-141">您不受限於 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件中的一個容器。</span><span class="sxs-lookup"><span data-stu-id="c4561-141">You are not limited to one container in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="c4561-142">您可以建立一系列的容器，每個都在上述各嵌套，而且您可以指定每個這些嵌套容器的世界轉換、剪下區域和品質設定。</span><span class="sxs-lookup"><span data-stu-id="c4561-142">You can create a sequence of containers, each nested in the preceding, and you can specify the world transformation, clipping region, and quality settings of each of those nested containers.</span></span> <span data-ttu-id="c4561-143">如果您從最內層的容器內呼叫繪圖方法，轉換將依序套用，從最內層的容器開始，並以最外層的容器結束。</span><span class="sxs-lookup"><span data-stu-id="c4561-143">If you call a drawing method from inside the innermost container, the transformations will be applied in order, starting with the innermost container and ending with the outermost container.</span></span> <span data-ttu-id="c4561-144">從最內層容器內繪製的專案，將會由所有裁剪區域的交集來裁剪。</span><span class="sxs-lookup"><span data-stu-id="c4561-144">Items drawn from inside the innermost container will be clipped by the intersection of all the clipping regions.</span></span>

<span data-ttu-id="c4561-145">下列範例會建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件，並將其文字轉譯提示設定為 [\* \* \* \* TextRenderingHintAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* \*。</span><span class="sxs-lookup"><span data-stu-id="c4561-145">The following example creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and sets its text rendering hint to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="c4561-146">程式碼會建立兩個容器，一個在另一個容器內。</span><span class="sxs-lookup"><span data-stu-id="c4561-146">The code creates two containers, one nested within the other.</span></span> <span data-ttu-id="c4561-147">外部容器的文字轉譯提示會設定為 [\* \* \* \* TextRenderingHintSingleBitPerPixel \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)\* *，而內部容器的文字轉譯提示會設定為 [\* \* \* \* TextRenderingHintAntiAlias \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* \*。</span><span class="sxs-lookup"><span data-stu-id="c4561-147">The text rendering hint of the outer container is set to [\*\*\*\*TextRenderingHintSingleBitPerPixel\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint), and the text rendering hint of the inner container is set to [\*\*\*\*TextRenderingHintAntiAlias\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint).</span></span> <span data-ttu-id="c4561-148">此程式碼會繪製三個字串：一個來自內部容器、一個來自外部容器，另一個來自 **圖形** 物件本身。</span><span class="sxs-lookup"><span data-stu-id="c4561-148">The code draws three strings: one from the inner container, one from the outer container, and one from the **Graphics** object itself.</span></span>


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



<span data-ttu-id="c4561-149">下圖顯示三個字串。</span><span class="sxs-lookup"><span data-stu-id="c4561-149">The following illustration shows the three strings.</span></span> <span data-ttu-id="c4561-150">從內部容器和 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件繪製的字串會透過消除鋸齒來進行平滑處理。</span><span class="sxs-lookup"><span data-stu-id="c4561-150">The strings drawn from the inner container and the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object are smoothed by antialiasing.</span></span> <span data-ttu-id="c4561-151">因為 TextRenderingHintSingleBitPerPixel 設定，所以從外部容器繪製的字串不會因消除鋸齒而經過平滑處理。</span><span class="sxs-lookup"><span data-stu-id="c4561-151">The string drawn from the outer container is not smoothed by antialiasing because of the TextRenderingHintSingleBitPerPixel setting.</span></span>

![矩形的圖例，其中包含相同的字串。只有第一行和最後一行的字元是平滑的](images/nestedcontainers3.png)

 

 
