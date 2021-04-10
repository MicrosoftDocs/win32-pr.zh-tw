---
title: 在 Direct2D 中套用轉換
description: 在 Direct2D 中套用轉換
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8edddbb3150f16428c56bd4c6da828c9b2ce594e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682367"
---
# <a name="applying-transforms-in-direct2d"></a><span data-ttu-id="bb9d8-103">在 Direct2D 中套用轉換</span><span class="sxs-lookup"><span data-stu-id="bb9d8-103">Applying Transforms in Direct2D</span></span>

<span data-ttu-id="bb9d8-104">在 [使用 Direct2D 繪圖](drawing-with-direct2d.md)時，我們看到 [**ID2D1RenderTarget：： FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) 方法繪製了一個對齊 X 軸和 y 軸的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-104">In [Drawing with Direct2D](drawing-with-direct2d.md), we saw that the [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws an ellipse that is aligned to the x- and y-axes.</span></span> <span data-ttu-id="bb9d8-105">但是，假設您想要以角度來繪製橢圓形？</span><span class="sxs-lookup"><span data-stu-id="bb9d8-105">But suppose that you want to draw an ellipse tilted at an angle?</span></span>

![顯示傾斜橢圓形的影像。](images/graphics16.png)

<span data-ttu-id="bb9d8-107">藉由使用轉換，您可以透過下列方式更改圖形。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-107">By using transforms, you can alter a shape in the following ways.</span></span>

-   <span data-ttu-id="bb9d8-108">圍繞點旋轉。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-108">Rotation around a point.</span></span>
-   <span data-ttu-id="bb9d8-109">縮放。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-109">Scaling.</span></span>
-   <span data-ttu-id="bb9d8-110">) X 或 Y 方向的轉譯 (位移。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-110">Translation (displacement in the X or Y direction).</span></span>
-   <span data-ttu-id="bb9d8-111">扭曲 (也稱為 *切變*) 。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-111">Skew (also known as *shear*).</span></span>

<span data-ttu-id="bb9d8-112">轉換是將一組點對應到一組新點的數學運算。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-112">A transform is a mathematical operation that maps a set of points to a new set of points.</span></span> <span data-ttu-id="bb9d8-113">例如，下圖顯示圍繞點 P3 旋轉的三角形。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-113">For example, the following diagram shows a triangle rotated around the point P3.</span></span> <span data-ttu-id="bb9d8-114">套用旋轉之後，點 P1 會對應到 P1 '，點 P2 會對應到 P2 '，而 point P3 會對應到本身。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-114">After the rotation is applied, the point P1 is mapped to P1', the point P2 is mapped to P2', and the point P3 maps to itself.</span></span>

![顯示圍繞點旋轉的圖表。](images/graphics17.png)

<span data-ttu-id="bb9d8-116">轉換是使用矩陣來執行的。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-116">Transforms are implemented by using matrices.</span></span> <span data-ttu-id="bb9d8-117">不過，您不需要瞭解矩陣的數學運算就能使用。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-117">However, you do not have to understand the mathematics of matrices in order to use them.</span></span> <span data-ttu-id="bb9d8-118">如果您想要深入瞭解數學，請參閱 [附錄：矩陣轉換](appendix--matrix-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-118">If you want to learn more about the math, see [Appendix: Matrix Transforms](appendix--matrix-transforms.md).</span></span>

<span data-ttu-id="bb9d8-119">若要在 Direct2D 中套用轉換，請呼叫 [**ID2D1RenderTarget：： SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) 方法。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-119">To apply a transform in Direct2D, call the [**ID2D1RenderTarget::SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) method.</span></span> <span data-ttu-id="bb9d8-120">這個方法會採用 [**D2D1 \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) 結構來定義轉換。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-120">This method takes a [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure that defines the transformation.</span></span> <span data-ttu-id="bb9d8-121">您可以藉由呼叫 [**D2D1：： Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) 類別上的方法來初始化此結構。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-121">You can initialize this structure by calling methods on the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="bb9d8-122">這個類別包含的靜態方法會傳回每一種轉換的矩陣：</span><span class="sxs-lookup"><span data-stu-id="bb9d8-122">This class contains static methods that return a matrix for each kind of transform:</span></span>

-   [<span data-ttu-id="bb9d8-123">**Matrix3x2F：：輪替**</span><span class="sxs-lookup"><span data-stu-id="bb9d8-123">**Matrix3x2F::Rotation**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   <span data-ttu-id="bb9d8-124">[**Matrix3x2F：： Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span><span class="sxs-lookup"><span data-stu-id="bb9d8-124">[**Matrix3x2F::Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span></span>
-   <span data-ttu-id="bb9d8-125">[**Matrix3x2F：：轉譯**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span><span class="sxs-lookup"><span data-stu-id="bb9d8-125">[**Matrix3x2F::Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span></span>
-   [<span data-ttu-id="bb9d8-126">**Matrix3x2F：：扭曲**</span><span class="sxs-lookup"><span data-stu-id="bb9d8-126">**Matrix3x2F::Skew**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

<span data-ttu-id="bb9d8-127">例如，下列程式碼會在 (100，100) 的點周圍套用20度的旋轉。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-127">For example, the following code applies a 20-degree rotation around the point (100, 100).</span></span>


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

<span data-ttu-id="bb9d8-128">轉換會套用至所有後續的繪圖操作，直到您再次呼叫 [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) 為止。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-128">The transform is applied to all later drawing operations until you call [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) again.</span></span> <span data-ttu-id="bb9d8-129">若要移除目前的轉換，請使用身分識別矩陣來呼叫 **SetTransform** 。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-129">To remove the current transform, call **SetTransform** with the identity matrix.</span></span> <span data-ttu-id="bb9d8-130">若要建立身分識別矩陣，請呼叫 [**Matrix3x2F：： identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) 函數。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-130">To create the identity matrix, call the [**Matrix3x2F::Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) function.</span></span>


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a><span data-ttu-id="bb9d8-131">繪製時鐘手</span><span class="sxs-lookup"><span data-stu-id="bb9d8-131">Drawing Clock Hands</span></span>

<span data-ttu-id="bb9d8-132">讓我們將圓形程式轉換成類比時鐘來放置轉換。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-132">Let's put transforms to use by converting our Circle program into an analog clock.</span></span> <span data-ttu-id="bb9d8-133">我們可以藉由新增手線來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-133">We can do this by adding lines for the hands.</span></span>

![類比時鐘程式的螢幕擷取畫面。](images/graphics18.png)

<span data-ttu-id="bb9d8-135">我們可以計算角度，然後套用旋轉轉換，而不是計算線條的座標。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-135">Instead of calculating the coordinates for the lines, we can calculate the angle and then apply a rotation transform.</span></span> <span data-ttu-id="bb9d8-136">下列程式碼顯示一個可繪製一次時鐘的函式。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-136">The following code shows a function that draws one clock hand.</span></span> <span data-ttu-id="bb9d8-137">*FAngle* 參數提供手的角度（以度為單位）。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-137">The *fAngle* parameter gives the angle of the hand, in degrees.</span></span>

```C++
void Scene::DrawClockHand(float fHandLength, float fAngle, float fStrokeWidth)
{
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(fAngle, m_ellipse.point)
            );

    // endPoint defines one end of the hand.
    D2D_POINT_2F endPoint = D2D1::Point2F(
        m_ellipse.point.x,
        m_ellipse.point.y - (m_ellipse.radiusY * fHandLength)
        );

    // Draw a line from the center of the ellipse to endPoint.
    m_pRenderTarget->DrawLine(
        m_ellipse.point, endPoint, m_pStroke, fStrokeWidth);
}
```

<span data-ttu-id="bb9d8-138">這段程式碼會繪製一條垂直線，從時鐘面的中央開始，然後結束于點 *端點*。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-138">This code draws a vertical line, starting from the center of the clock face and ending at the point *endPoint*.</span></span> <span data-ttu-id="bb9d8-139">線條是藉由套用旋轉轉換，在橢圓形的中央周圍旋轉。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-139">The line is rotated around the center of the ellipse by applying a rotation transform.</span></span> <span data-ttu-id="bb9d8-140">旋轉的中心點是形成時鐘面的橢圓形中心。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-140">The center point for the rotation is the center of ellipse that forms the clock face.</span></span>

![顯示時鐘手旋轉的圖表。](images/graphics19.png)

<span data-ttu-id="bb9d8-142">下列程式碼顯示如何繪製整個時鐘臉部。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-142">The following code shows how the whole clock face is drawn.</span></span>

```C++
void Scene::RenderScene()
{
    m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::SkyBlue));

    m_pRenderTarget->FillEllipse(m_ellipse, m_pFill);
    m_pRenderTarget->DrawEllipse(m_ellipse, m_pStroke);

    // Draw hands
    SYSTEMTIME time;
    GetLocalTime(&time);

    // 60 minutes = 30 degrees, 1 minute = 0.5 degree
    const float fHourAngle = (360.0f / 12) * (time.wHour) + (time.wMinute * 0.5f);
    const float fMinuteAngle =(360.0f / 60) * (time.wMinute);

    DrawClockHand(0.6f,  fHourAngle,   6);
    DrawClockHand(0.85f, fMinuteAngle, 4);

    // Restore the identity transformation.
    m_pRenderTarget->SetTransform( D2D1::Matrix3x2F::Identity() );
}
```

<span data-ttu-id="bb9d8-143">您可以從 [Direct2D Clock 範例](direct2d-clock-sample.md)下載完整的 Visual Studio 專案。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-143">You can download the complete Visual Studio project from [Direct2D Clock Sample](direct2d-clock-sample.md).</span></span> <span data-ttu-id="bb9d8-144"> (只是為了有趣，下載版本會將放射星形 gradiant 新增至時鐘臉部。 ) </span><span class="sxs-lookup"><span data-stu-id="bb9d8-144">(Just for fun, the download version adds a radial gradiant to the clock face.)</span></span>

## <a name="combining-transforms"></a><span data-ttu-id="bb9d8-145">合併轉換</span><span class="sxs-lookup"><span data-stu-id="bb9d8-145">Combining Transforms</span></span>

<span data-ttu-id="bb9d8-146">四個基本轉換可以藉由將兩個以上的矩陣相乘來合併。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-146">The four basic transforms can be combined by multiplying two or more matrices.</span></span> <span data-ttu-id="bb9d8-147">例如，下列程式碼會結合旋轉與轉譯。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-147">For example, the following code combines a rotation with a translation.</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="bb9d8-148">[**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f)類別提供矩陣乘法的 [**運算子 \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) 。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-148">The [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class provides [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for matrix multiplication.</span></span> <span data-ttu-id="bb9d8-149">您將矩陣相乘的順序很重要。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-149">The order in which you multiply the matrices is important.</span></span> <span data-ttu-id="bb9d8-150">設定轉換 (M x N) 表示「先套用 M，後面接著 N」。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-150">Setting a transform (M × N) means "Apply M first, followed by N."</span></span> <span data-ttu-id="bb9d8-151">例如，以下是旋轉，後面接著平移：</span><span class="sxs-lookup"><span data-stu-id="bb9d8-151">For example, here is rotation followed by translation:</span></span>

![顯示旋轉後接平移的圖表。](images/graphics20.png)

<span data-ttu-id="bb9d8-153">以下是此轉換的程式碼：</span><span class="sxs-lookup"><span data-stu-id="bb9d8-153">Here is the code for this transform:</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="bb9d8-154">現在將該轉換與反向順序中的轉換進行比較，並在後面接著旋轉。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-154">Now compare that transform with a transform in the reverse order, translation followed by rotation.</span></span>

![顯示轉譯後接旋轉的圖表。](images/graphics21.png)

<span data-ttu-id="bb9d8-156">旋轉是在原始矩形的中央周圍執行。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-156">The rotation is performed around the center of the original rectangle.</span></span> <span data-ttu-id="bb9d8-157">以下是此轉換的程式碼。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-157">Here is the code for this transform.</span></span>

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

<span data-ttu-id="bb9d8-158">如您所見，矩陣是相同的，但作業的順序已變更。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-158">As you can see, the matrices are the same, but the order of operations has changed.</span></span> <span data-ttu-id="bb9d8-159">發生這種情況是因為矩陣乘法不是可交換的： M x N ≠ N x M。</span><span class="sxs-lookup"><span data-stu-id="bb9d8-159">This happens because matrix multiplication is not commutative: M × N ≠ N × M.</span></span>

## <a name="next"></a><span data-ttu-id="bb9d8-160">下一個</span><span class="sxs-lookup"><span data-stu-id="bb9d8-160">Next</span></span>

[<span data-ttu-id="bb9d8-161">附錄：矩陣轉換</span><span class="sxs-lookup"><span data-stu-id="bb9d8-161">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)