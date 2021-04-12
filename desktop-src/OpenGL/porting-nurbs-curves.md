---
title: 移植 NURBS 曲線
description: 繪製 NURBS 曲線的 OpenGL 函式與鳶尾花 GL 函數非常類似。 您可以使用 gluNurbsCurve 函式指定節點序列和控制點，此函式必須包含在 gluBeginCurve/gluEndCurve 配對內。
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- 鳶尾花 GL 移植，NURBS 曲線
- 從鳶尾花 GL、NURBS 曲線移植
- 從鳶尾花 GL （NURBS 曲線）移植至 OpenGL
- 從鳶尾花 GL、NURBS 曲線移植的 OpenGL
- NURBS 曲線
- 曲線
- 鳶尾花 GL 移植，曲線
- 從鳶尾花 GL、曲線移植
- 從鳶尾花 GL （曲線）移植至 OpenGL
- 從鳶尾花 GL、曲線移植的 OpenGL
- 'NURBS (非統一的有理 B 曲線) '
- '非統一的有理 B 曲線 (NURBS) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372366"
---
# <a name="porting-nurbs-curves"></a><span data-ttu-id="cba7f-116">移植 NURBS 曲線</span><span class="sxs-lookup"><span data-stu-id="cba7f-116">Porting NURBS Curves</span></span>

<span data-ttu-id="cba7f-117">繪製 NURBS 曲線的 OpenGL 函式與鳶尾花 GL 函數非常類似。</span><span class="sxs-lookup"><span data-stu-id="cba7f-117">The OpenGL functions for drawing NURBS curves are very similar to the IRIS GL functions.</span></span> <span data-ttu-id="cba7f-118">您可以使用 [**gluNurbsCurve**](glunurbscurve.md)函式指定節點序列和控制點，此函數必須包含在 [**gluBeginCurve**](glubegincurve.md)  /  [**gluEndCurve**](gluendcurve.md)配對內。</span><span class="sxs-lookup"><span data-stu-id="cba7f-118">You specify knot sequences and control points using a [**gluNurbsCurve**](glunurbscurve.md) function, which must be contained within a [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) pair.</span></span>

<span data-ttu-id="cba7f-119">下表列出用來繪製 NURBS 曲線的鳶尾花 GL 函式，以及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="cba7f-119">The following table lists the IRIS GL functions for drawing NURBS curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="cba7f-120">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="cba7f-120">IRIS GL function</span></span> | <span data-ttu-id="cba7f-121">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="cba7f-121">OpenGL function</span></span>                        | <span data-ttu-id="cba7f-122">意義</span><span class="sxs-lookup"><span data-stu-id="cba7f-122">Meaning</span></span>                     |
|------------------|----------------------------------------|-----------------------------|
| <span data-ttu-id="cba7f-123">**bgncurve**</span><span class="sxs-lookup"><span data-stu-id="cba7f-123">**bgncurve**</span></span>     | [<span data-ttu-id="cba7f-124">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="cba7f-124">**gluBeginCurve**</span></span>](glubegincurve.md) | <span data-ttu-id="cba7f-125">開始曲線定義。</span><span class="sxs-lookup"><span data-stu-id="cba7f-125">Begins a curve definition.</span></span>  |
| <span data-ttu-id="cba7f-126">**nurbscurve**</span><span class="sxs-lookup"><span data-stu-id="cba7f-126">**nurbscurve**</span></span>   | [<span data-ttu-id="cba7f-127">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="cba7f-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="cba7f-128">指定曲線屬性。</span><span class="sxs-lookup"><span data-stu-id="cba7f-128">Specifies curve attributes.</span></span> |
| <span data-ttu-id="cba7f-129">**endcurve**</span><span class="sxs-lookup"><span data-stu-id="cba7f-129">**endcurve**</span></span>     | [<span data-ttu-id="cba7f-130">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="cba7f-130">**gluEndCurve**</span></span>](gluendcurve.md)     | <span data-ttu-id="cba7f-131">結束曲線定義。</span><span class="sxs-lookup"><span data-stu-id="cba7f-131">Ends a curve definition.</span></span>    |



 

<span data-ttu-id="cba7f-132">藉由將位置、材質和色彩座標呈現為開始/結束配對內的個別 **gluNurbsCurve** 來建立關聯。</span><span class="sxs-lookup"><span data-stu-id="cba7f-132">Associate position, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** inside the begin/end pair.</span></span> <span data-ttu-id="cba7f-133">您可以針對單一 **gluBeginCurve/gluEndCurve** 配對內的每個色彩、位置和材質資料片段，進行一個以上的 **gluNurbsCurve** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="cba7f-133">You can make no more than one call to **gluNurbsCurve** for each piece of color, position, and texture data within a single **gluBeginCurve/gluEndCurve** pair.</span></span> <span data-ttu-id="cba7f-134">您必須確實進行一個呼叫，以描述曲線的位置 (GL \_ MAP1 \_ 頂點 \_ 3 或 gl \_ MAP1 \_ 頂點 \_ 4 描述) 。</span><span class="sxs-lookup"><span data-stu-id="cba7f-134">You must make exactly one call to describe the position of the curve (a GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4 description).</span></span> <span data-ttu-id="cba7f-135">當您呼叫 **gluEndCurve** 時，會將曲線鑲嵌成線段，然後轉譯。</span><span class="sxs-lookup"><span data-stu-id="cba7f-135">When you call **gluEndCurve**, the curve is tessellated into line segments and then rendered.</span></span>

<span data-ttu-id="cba7f-136">下表列出鳶尾花 GL 和 OpenGL NURBS 曲線類型。</span><span class="sxs-lookup"><span data-stu-id="cba7f-136">The following table lists IRIS GL and OpenGL NURBS curve types.</span></span>



| <span data-ttu-id="cba7f-137">鳶尾花 GL 類型</span><span class="sxs-lookup"><span data-stu-id="cba7f-137">IRIS GL type</span></span> | <span data-ttu-id="cba7f-138">OpenGL 類型</span><span class="sxs-lookup"><span data-stu-id="cba7f-138">OpenGL type</span></span>                  | <span data-ttu-id="cba7f-139">意義</span><span class="sxs-lookup"><span data-stu-id="cba7f-139">Meaning</span></span>                                 |
|--------------|------------------------------|-----------------------------------------|
| <span data-ttu-id="cba7f-140">N \_ V3D</span><span class="sxs-lookup"><span data-stu-id="cba7f-140">N\_V3D</span></span>       | <span data-ttu-id="cba7f-141">GL \_ MAP1 \_ 頂點 \_ 3</span><span class="sxs-lookup"><span data-stu-id="cba7f-141">GL\_MAP1\_VERTEX\_3</span></span>          | <span data-ttu-id="cba7f-142">多項式曲線。</span><span class="sxs-lookup"><span data-stu-id="cba7f-142">Polynomial curve.</span></span>                       |
| <span data-ttu-id="cba7f-143">N \_ V3DR</span><span class="sxs-lookup"><span data-stu-id="cba7f-143">N\_V3DR</span></span>      | <span data-ttu-id="cba7f-144">GL \_ MAP1 \_ 頂點 \_ 4</span><span class="sxs-lookup"><span data-stu-id="cba7f-144">GL\_MAP1\_VERTEX\_4</span></span>          | <span data-ttu-id="cba7f-145">有理數曲線。</span><span class="sxs-lookup"><span data-stu-id="cba7f-145">Rational curve.</span></span>                         |
|              | <span data-ttu-id="cba7f-146">GL \_ MAP1 \_ 材質 \_ COORD\_\*</span><span class="sxs-lookup"><span data-stu-id="cba7f-146">GL\_MAP1\_TEXTURE\_COORD\_\*</span></span> | <span data-ttu-id="cba7f-147">控制點是材質座標。</span><span class="sxs-lookup"><span data-stu-id="cba7f-147">Control points are texture coordinates.</span></span> |
|              | <span data-ttu-id="cba7f-148">GL \_ MAP1 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="cba7f-148">GL\_MAP1\_NORMAL</span></span>             | <span data-ttu-id="cba7f-149">控制點是法線。</span><span class="sxs-lookup"><span data-stu-id="cba7f-149">Control points are normals.</span></span>             |



 

<span data-ttu-id="cba7f-150">如需可用評估工具類型的詳細資訊，請參閱 [**glMap1**](glmap1.md)。</span><span class="sxs-lookup"><span data-stu-id="cba7f-150">For more information on available evaluator types, see [**glMap1**](glmap1.md).</span></span>

<span data-ttu-id="cba7f-151">??</span><span class="sxs-lookup"><span data-stu-id="cba7f-151">??</span></span>

 

 




