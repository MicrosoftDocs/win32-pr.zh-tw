---
description: 圖形狀態 &\# 8212; 裁剪區域、轉換和品質設定 &\# 8212; 儲存在繪圖物件中。
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: 圖形容器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8bf6469d0835137be1bb76b7727fd961bba16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560102"
---
# <a name="graphics-containers"></a><span data-ttu-id="4100c-103">圖形容器</span><span class="sxs-lookup"><span data-stu-id="4100c-103">Graphics Containers</span></span>

<span data-ttu-id="4100c-104">圖形狀態（剪下區域、轉換和品質設定）會儲存在 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件中。</span><span class="sxs-lookup"><span data-stu-id="4100c-104">Graphics state — clipping region, transformations, and quality settings — is stored in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="4100c-105">Windows GDI + 可讓您使用容器，在 **圖形** 物件中暫時取代或增強部分狀態。</span><span class="sxs-lookup"><span data-stu-id="4100c-105">Windows GDI+ allows you to temporarily replace or augment part of the state in a **Graphics** object by using a container.</span></span> <span data-ttu-id="4100c-106">您可以藉由呼叫 **graphics 物件的** [**Graphics：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))方法來啟動容器，然後藉由呼叫 [**graphics：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)方法來結束容器。</span><span class="sxs-lookup"><span data-stu-id="4100c-106">You start a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object, and you end a container by calling the [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) method.</span></span> <span data-ttu-id="4100c-107">在 **graphics：： BeginContainer** 與 **Graphics：： EndContainer** 之間，您對 **圖形** 物件所做的任何狀態變更都屬於容器，而不會覆寫 **圖形** 物件的現有狀態。</span><span class="sxs-lookup"><span data-stu-id="4100c-107">In between **Graphics::BeginContainer** and **Graphics::EndContainer**, any state changes you make to the **Graphics** object belong to the container and do not overwrite the existing state of the **Graphics** object.</span></span>

<span data-ttu-id="4100c-108">下列範例會在 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件中建立容器。</span><span class="sxs-lookup"><span data-stu-id="4100c-108">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="4100c-109">**圖形** 物件的世界轉換是將200單位轉譯為右邊的轉換，而容器的世界轉換則是轉譯100單位。</span><span class="sxs-lookup"><span data-stu-id="4100c-109">The world transformation of the **Graphics** object is a translation 200 units to the right, and the world transformation of the container is a translation 100 units down.</span></span>


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



<span data-ttu-id="4100c-110">請注意，在上述範例中， `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` 在對 [**graphics：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) 和 [**graphics：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) 的呼叫之間進行的語句，會產生不同的矩形，而不是呼叫 **圖形：： EndContainer** 之後所做的相同語句。</span><span class="sxs-lookup"><span data-stu-id="4100c-110">Note that in the previous example, the statement `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` made in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produces a different rectangle than the same statement made after the call to **Graphics::EndContainer**.</span></span> <span data-ttu-id="4100c-111">只有水準轉譯會套用至在容器外部進行的 **graphicswindow.drawrectangle** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="4100c-111">Only the horizontal translation applies to the **DrawRectangle** call made outside of the container.</span></span> <span data-ttu-id="4100c-112">這兩種轉換（200單位的水準轉譯和100單位的垂直轉譯）適用于 [**圖形：:D**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) 在容器內進行的 rawrectangle 呼叫。</span><span class="sxs-lookup"><span data-stu-id="4100c-112">Both transformations — the horizontal translation of 200 units and the vertical translation of 100 units — apply to the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) call made inside the container.</span></span> <span data-ttu-id="4100c-113">下圖顯示兩個矩形。</span><span class="sxs-lookup"><span data-stu-id="4100c-113">The following illustration shows the two rectangles.</span></span>

![視窗的螢幕擷取畫面，其中有兩個以藍色畫筆繪製的矩形，一個位於另一個上方](images/aboutgdip05-art17.png)

<span data-ttu-id="4100c-115">容器可以嵌套在容器內。</span><span class="sxs-lookup"><span data-stu-id="4100c-115">Containers can be nested within containers.</span></span> <span data-ttu-id="4100c-116">下列範例會在 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件內建立容器，並在第一個容器內建立另一個容器。</span><span class="sxs-lookup"><span data-stu-id="4100c-116">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and another container within the first container.</span></span> <span data-ttu-id="4100c-117">**圖形** 物件的世界轉換是 x 方向的平移100單位和 y 方向的80單位。</span><span class="sxs-lookup"><span data-stu-id="4100c-117">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="4100c-118">第一個容器的世界轉換是30度的旋轉。</span><span class="sxs-lookup"><span data-stu-id="4100c-118">The world transformation of the first container is a 30-degree rotation.</span></span> <span data-ttu-id="4100c-119">第二個容器的世界轉換是以 x 方向的2因數來進行調整。</span><span class="sxs-lookup"><span data-stu-id="4100c-119">The world transformation of the second container is a scaling by a factor of 2 in the x direction.</span></span> <span data-ttu-id="4100c-120">對圖形進行的呼叫 [**：:D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) 方法是在第二個容器內進行。</span><span class="sxs-lookup"><span data-stu-id="4100c-120">A call to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) method is made inside the second container.</span></span>


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



<span data-ttu-id="4100c-121">下圖顯示橢圓形。</span><span class="sxs-lookup"><span data-stu-id="4100c-121">The following illustration shows the ellipse.</span></span>

![視窗的螢幕擷取畫面，其中包含旋轉的藍色橢圓形，其中心標示為 (100，80) ](images/aboutgdip05-art18.png)

<span data-ttu-id="4100c-123">請注意，這三個轉換都適用于 [**圖形：:D**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) 在第二個 (最內層) 容器中進行的 rawellipse 呼叫。</span><span class="sxs-lookup"><span data-stu-id="4100c-123">Note that all three transformations apply to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) call made in the second (innermost) container.</span></span> <span data-ttu-id="4100c-124">另外也請注意轉換的順序：第一次調整，然後旋轉，然後轉譯。</span><span class="sxs-lookup"><span data-stu-id="4100c-124">Also note the order of the transformations: first scale, then rotate, then translate.</span></span> <span data-ttu-id="4100c-125">最內層的轉換會先套用，而最外層的轉換最後會套用。</span><span class="sxs-lookup"><span data-stu-id="4100c-125">The innermost transformation is applied first, and the outermost transformation is applied last.</span></span>

<span data-ttu-id="4100c-126">[**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的任何屬性都可以設定在容器中， (在圖形的呼叫之間 [**：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))和 [**graphics：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)) 。</span><span class="sxs-lookup"><span data-stu-id="4100c-126">Any property of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be set inside a container (in between calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="4100c-127">例如，您可以在容器內設定裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="4100c-127">For example, a clipping region can be set inside a container.</span></span> <span data-ttu-id="4100c-128">任何在容器內完成的繪圖都會限制為該容器的裁剪區域，而且也會限制為任何外部容器的裁剪區域和 **圖形** 物件本身的裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="4100c-128">Any drawing done inside the container will be restricted to the clipping region of that container and will also be restricted to the clipping regions of any outer containers and the clipping region of the **Graphics** object itself.</span></span>

<span data-ttu-id="4100c-129">到目前為止所討論的屬性（世界轉換和裁剪區域）都會由嵌套容器合併。</span><span class="sxs-lookup"><span data-stu-id="4100c-129">The properties discussed so far — the world transformation and the clipping region — are combined by nested containers.</span></span> <span data-ttu-id="4100c-130">其他屬性會暫時由嵌套容器取代。</span><span class="sxs-lookup"><span data-stu-id="4100c-130">Other properties are temporarily replaced by a nested container.</span></span> <span data-ttu-id="4100c-131">例如，如果您將平滑模式設定為在容器內 SmoothingModeAntiAlias，則在該容器內呼叫的任何繪圖方法都會使用消除鋸齒平滑模式，但是在 [**圖形：： EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) 之後呼叫的繪圖方法會使用在 [**圖形：： BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit))呼叫之前所處的平滑模式。</span><span class="sxs-lookup"><span data-stu-id="4100c-131">For example, if you set the smoothing mode to SmoothingModeAntiAlias within a container, any drawing methods called inside that container will use the antialias smoothing mode, but drawing methods called after [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will use the smoothing mode that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

<span data-ttu-id="4100c-132">如需合併 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和容器之世界轉換的另一個範例，假設您想要繪製眼睛，並將它放在一系列臉部的不同位置。</span><span class="sxs-lookup"><span data-stu-id="4100c-132">For another example of combining the world transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container, suppose you want to draw an eye and place it at various locations on a sequence of faces.</span></span> <span data-ttu-id="4100c-133">下列範例會在座標系統的原點繪製中央的眼睛。</span><span class="sxs-lookup"><span data-stu-id="4100c-133">The following example draws an eye centered at the origin of the coordinate system.</span></span>


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



<span data-ttu-id="4100c-134">下圖顯示眼睛和座標軸。</span><span class="sxs-lookup"><span data-stu-id="4100c-134">The following illustration shows the eye and the coordinate axes.</span></span>

![圖例顯示由三個省略號組成的眼睛：大綱、鳶尾花和小學生各有一個橢圓形](images/aboutgdip05-art19.png)

<span data-ttu-id="4100c-136">上述範例中定義的 DrawEye 函式會接收 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的位址，並立即在該 **圖形** 物件中建立容器。</span><span class="sxs-lookup"><span data-stu-id="4100c-136">The DrawEye function, defined in the previous example receives the address of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and immediately creates a container within that **Graphics** object.</span></span> <span data-ttu-id="4100c-137">此容器會將呼叫 DrawEye 函式的任何程式碼，從 DrawEye 函數執行期間所做的屬性設定中隔離。</span><span class="sxs-lookup"><span data-stu-id="4100c-137">This container insulates any code that calls the DrawEye function from property settings made during the execution of the DrawEye function.</span></span> <span data-ttu-id="4100c-138">例如，DrawEye 函式中的程式碼會設定 **Graphics** 物件的裁剪區域，但是當 DrawEye 將控制權傳回給呼叫常式時，裁剪區域就會與呼叫 DrawEye 之前的相同。</span><span class="sxs-lookup"><span data-stu-id="4100c-138">For example, code in the DrawEye function sets the clipping region of the **Graphics** object, but when DrawEye returns control to the calling routine, the clipping region will be as it was before the call to DrawEye.</span></span>

<span data-ttu-id="4100c-139">下列範例會繪製三個橢圓形 (臉部) ，每一個都有眼睛。</span><span class="sxs-lookup"><span data-stu-id="4100c-139">The following example draws three ellipses (faces), each with an eye inside.</span></span>


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



<span data-ttu-id="4100c-140">下圖顯示三個省略號。</span><span class="sxs-lookup"><span data-stu-id="4100c-140">The following illustration shows the three ellipses.</span></span>

![視窗的螢幕擷取畫面，其中包含三個省略號，每個都包含不同大小和旋轉的眼睛](images/aboutgdip05-art20.png)

<span data-ttu-id="4100c-142">在先前的範例中，所有的省略號都是使用呼叫來繪製 `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` ，這會繪製以座標系統原點為中心的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="4100c-142">In the previous example, all ellipses are drawn with the call `DrawEllipse(&myBlackPen, -40, -60, 80, 120)`, which draws an ellipse centered at the origin of the coordinate system.</span></span> <span data-ttu-id="4100c-143">您可以藉由設定 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件的世界轉換，將橢圓形移離工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="4100c-143">The ellipses are moved away from the upper-left corner of the client area by setting the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="4100c-144">此語句會導致第一個橢圓形的中心為 (100，100) 。</span><span class="sxs-lookup"><span data-stu-id="4100c-144">The statement causes the first ellipse to be centered at (100, 100).</span></span> <span data-ttu-id="4100c-145">此語句會導致第二個橢圓形的中心成為第一個橢圓形中間的100個單位。</span><span class="sxs-lookup"><span data-stu-id="4100c-145">The statement causes the center of the second ellipse to be 100 units to the right of the center of the first ellipse.</span></span> <span data-ttu-id="4100c-146">同樣地，第三個橢圓形的中心是第二個橢圓形中央的100單位。</span><span class="sxs-lookup"><span data-stu-id="4100c-146">Likewise, the center of the third ellipse is 100 units to the right of the center of the second ellipse.</span></span>

<span data-ttu-id="4100c-147">上一個範例中的容器用來轉換相對於指定橢圓形中心的眼睛。</span><span class="sxs-lookup"><span data-stu-id="4100c-147">The containers in the previous example are used to transform the eye relative to the center of a given ellipse.</span></span> <span data-ttu-id="4100c-148">第一眼是在沒有轉換的橢圓中央繪製，因此 DrawEye 呼叫不在容器內。</span><span class="sxs-lookup"><span data-stu-id="4100c-148">The first eye is drawn at the center of the ellipse with no transformation, so the DrawEye call is not inside a container.</span></span> <span data-ttu-id="4100c-149">第二眼是旋轉40度，並繪製在橢圓形中央上方的30個單位，因此 DrawEye 函式和設定轉換的方法會在容器內呼叫。</span><span class="sxs-lookup"><span data-stu-id="4100c-149">The second eye is rotated 40 degrees and drawn 30 units above the center of the ellipse, so the DrawEye function and the methods that set the transformation are called inside a container.</span></span> <span data-ttu-id="4100c-150">第三個眼睛會在橢圓形的中央伸展和旋轉並繪製。</span><span class="sxs-lookup"><span data-stu-id="4100c-150">The third eye is stretched and rotated and drawn at the center of the ellipse.</span></span> <span data-ttu-id="4100c-151">就像第二眼一樣，DrawEye 函式和設定轉換的方法會在容器內呼叫。</span><span class="sxs-lookup"><span data-stu-id="4100c-151">As with the second eye, the DrawEye function and the methods that set the transformation are called inside a container.</span></span>

 

 
