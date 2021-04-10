---
title: 轉換概觀
description: 介紹適用于 Windows 7 的 Microsoft Direct2D 轉換 API。 Direct2D 可讓 Win32 開發人員執行2D 圖形轉換。
ms.assetid: eea8177d-c19e-4972-a9a6-ad5d541b090f
keywords:
- Direct2D，轉換總覽
- Direct2D，座標系統
- Direct2D，轉譯目標
- Direct2D、2-d 轉換
- 2-d 轉換
- 轉換，關於
- 轉換，轉譯目標
- 轉換，物件
- 轉譯目標，轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f3678f7b194f0f0188ed907a63737a97e9e58c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933286"
---
# <a name="transforms-overview"></a><span data-ttu-id="d35a3-113">轉換概觀</span><span class="sxs-lookup"><span data-stu-id="d35a3-113">Transforms Overview</span></span>

<span data-ttu-id="d35a3-114">本主題討論 Direct2D 轉換的基本概念，並包含各種轉換的範例。</span><span class="sxs-lookup"><span data-stu-id="d35a3-114">This topic discusses the basics of Direct2D transforms and includes examples of various transforms.</span></span> <span data-ttu-id="d35a3-115">其中包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="d35a3-115">It contains the following parts:</span></span>

-   [<span data-ttu-id="d35a3-116">什麼是 Direct2D 轉換？</span><span class="sxs-lookup"><span data-stu-id="d35a3-116">What Is a Direct2D Transform?</span></span>](#what-is-a-direct2d-transform)
-   [<span data-ttu-id="d35a3-117">Direct2D 座標空間</span><span class="sxs-lookup"><span data-stu-id="d35a3-117">The Direct2D Coordinate Space</span></span>](#the-direct2d-coordinate-space)
-   [<span data-ttu-id="d35a3-118">建立轉換矩陣</span><span class="sxs-lookup"><span data-stu-id="d35a3-118">Creating Transformation Matrices</span></span>](#creating-transformation-matrices)
-   [<span data-ttu-id="d35a3-119">轉譯目標轉換</span><span class="sxs-lookup"><span data-stu-id="d35a3-119">Rendering Target Transforms</span></span>](#rendering-target-transforms)
-   [<span data-ttu-id="d35a3-120">筆刷轉換</span><span class="sxs-lookup"><span data-stu-id="d35a3-120">Brush Transforms</span></span>](#brush-transforms)
-   [<span data-ttu-id="d35a3-121">幾何轉換</span><span class="sxs-lookup"><span data-stu-id="d35a3-121">Geometry Transforms</span></span>](#geometry-transforms)
-   [<span data-ttu-id="d35a3-122">轉譯目標轉換如何影響剪輯</span><span class="sxs-lookup"><span data-stu-id="d35a3-122">How a Render Target Transform Affects Clips</span></span>](#how-a-render-target-transform-affects-clips)
-   [<span data-ttu-id="d35a3-123">總結</span><span class="sxs-lookup"><span data-stu-id="d35a3-123">Summary</span></span>](#summary)
-   [<span data-ttu-id="d35a3-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="d35a3-124">Related topics</span></span>](#related-topics)

## <a name="what-is-a-direct2d-transform"></a><span data-ttu-id="d35a3-125">什麼是 Direct2D 轉換？</span><span class="sxs-lookup"><span data-stu-id="d35a3-125">What Is a Direct2D Transform?</span></span>

<span data-ttu-id="d35a3-126">轉換會指定如何將物件的點從某個座標空間對應到另一個座標空間，或從某個位置對應到相同座標空間內的另一個位置。</span><span class="sxs-lookup"><span data-stu-id="d35a3-126">A transform specifies how to map the points of an object from one coordinate space to another or from one position to another within the same coordinate space.</span></span> <span data-ttu-id="d35a3-127">這項對應是由轉換矩陣所描述，定義為三個數據列的集合，其中有三個數據行的 FLOAT 值，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="d35a3-127">This mapping is described by a transformation matrix, defined as a collection of three rows with three columns of FLOAT values as shown in the following table.</span></span>



|                 |                 |     |
|-----------------|-----------------|-----|
| <span data-ttu-id="d35a3-128">M11Default：1。0</span><span class="sxs-lookup"><span data-stu-id="d35a3-128">M11Default: 1.0</span></span> | <span data-ttu-id="d35a3-129">M12Default：0。0</span><span class="sxs-lookup"><span data-stu-id="d35a3-129">M12Default: 0.0</span></span> | <span data-ttu-id="d35a3-130">0.0</span><span class="sxs-lookup"><span data-stu-id="d35a3-130">0.0</span></span> |
| <span data-ttu-id="d35a3-131">M21Default：0。0</span><span class="sxs-lookup"><span data-stu-id="d35a3-131">M21Default: 0.0</span></span> | <span data-ttu-id="d35a3-132">M22Default：1。0</span><span class="sxs-lookup"><span data-stu-id="d35a3-132">M22Default: 1.0</span></span> | <span data-ttu-id="d35a3-133">0.0</span><span class="sxs-lookup"><span data-stu-id="d35a3-133">0.0</span></span> |
| <span data-ttu-id="d35a3-134">M31OffsetX：0。0</span><span class="sxs-lookup"><span data-stu-id="d35a3-134">M31OffsetX: 0.0</span></span> | <span data-ttu-id="d35a3-135">M32OffsetY：0。0</span><span class="sxs-lookup"><span data-stu-id="d35a3-135">M32OffsetY: 0.0</span></span> | <span data-ttu-id="d35a3-136">1.0</span><span class="sxs-lookup"><span data-stu-id="d35a3-136">1.0</span></span> |



 

<span data-ttu-id="d35a3-137">在此矩陣中，M11、M12、M21 和 M22 成員定義了可以調整、旋轉或扭曲物件的線性轉換;OffsetX 和 OffsetY 成員會定義要在進行線性轉換之後套用的轉譯。</span><span class="sxs-lookup"><span data-stu-id="d35a3-137">In this matrix, the M11, M12, M21, and M22 members define a linear transformation that can scale, rotate, or skew an object; the OffsetX and OffsetY members define the translation to be applied after the linear transformation has been made.</span></span> <span data-ttu-id="d35a3-138">對於仿射轉換，第三個數據行中的值一律是0.0、0.0 和1.0。</span><span class="sxs-lookup"><span data-stu-id="d35a3-138">For affine transformations, the values in the third column are always 0.0, 0.0, and 1.0.</span></span>

<span data-ttu-id="d35a3-139">因為 Direct2D 僅支援仿射 (線性) 轉換，所以其轉換矩陣會定義為 3 x 2 矩陣，並省略前一個轉換矩陣的第三個數據行。</span><span class="sxs-lookup"><span data-stu-id="d35a3-139">Because Direct2D supports only affine (linear) transformations, its transformation matrix is defined as a 3-by-2 matrix, omitting the third column from the previous transformation matrix.</span></span> <span data-ttu-id="d35a3-140">下表顯示 Direct2D 轉換矩陣的版面配置。</span><span class="sxs-lookup"><span data-stu-id="d35a3-140">The following table shows the layout of the Direct2D transformation matrix.</span></span>



|                 |                 |
|-----------------|-----------------|
| <span data-ttu-id="d35a3-141">M11Default：1。0</span><span class="sxs-lookup"><span data-stu-id="d35a3-141">M11Default: 1.0</span></span> | <span data-ttu-id="d35a3-142">M12Default：0。0</span><span class="sxs-lookup"><span data-stu-id="d35a3-142">M12Default: 0.0</span></span> |
| <span data-ttu-id="d35a3-143">M21Default：0。0</span><span class="sxs-lookup"><span data-stu-id="d35a3-143">M21Default: 0.0</span></span> | <span data-ttu-id="d35a3-144">M22Default：1。0</span><span class="sxs-lookup"><span data-stu-id="d35a3-144">M22Default: 1.0</span></span> |
| <span data-ttu-id="d35a3-145">M31OffsetX：0。0</span><span class="sxs-lookup"><span data-stu-id="d35a3-145">M31OffsetX: 0.0</span></span> | <span data-ttu-id="d35a3-146">M32OffsetY：0。0</span><span class="sxs-lookup"><span data-stu-id="d35a3-146">M32OffsetY: 0.0</span></span> |



 

<span data-ttu-id="d35a3-147">在 Direct2D 中，這個 3 x 2 矩陣是以 [**D2D1 \_ 矩陣 \_ 3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) 結構表示。</span><span class="sxs-lookup"><span data-stu-id="d35a3-147">In Direct2D, this 3-by-2 matrix is represented by the [**D2D1\_MATRIX\_3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="d35a3-148">為了簡化常見的矩陣作業，Direct2D 也提供名為 [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)的類別，該類別衍生自 **D2D1 \_ 矩陣 \_ 3X2** 結構。</span><span class="sxs-lookup"><span data-stu-id="d35a3-148">To simplify common matrix operations, Direct2D also provides a class named [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f), which is derived from the **D2D1\_MATRIX\_3X2** structure.</span></span>

<span data-ttu-id="d35a3-149">[**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)的預設的函式會將物件保留為未初始化。</span><span class="sxs-lookup"><span data-stu-id="d35a3-149">The default constructor for [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) leaves the object uninitialized.</span></span> <span data-ttu-id="d35a3-150">若要取出識別矩陣，請使用 [**Matrix3x2F：： identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix)。</span><span class="sxs-lookup"><span data-stu-id="d35a3-150">To retrieve an identity matrix, use [**Matrix3x2F::Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix).</span></span>

<span data-ttu-id="d35a3-151">將身分識別轉換套用至物件時，不會變更物件的位置、形狀或大小。</span><span class="sxs-lookup"><span data-stu-id="d35a3-151">When an identity transform is applied to an object, it does not change the position, shape, or size of the object.</span></span> <span data-ttu-id="d35a3-152">它類似于將數位乘以1不會變更數位的方式。</span><span class="sxs-lookup"><span data-stu-id="d35a3-152">It is similar to the way that multiplying a number by 1 does not change the number.</span></span> <span data-ttu-id="d35a3-153">換句話說，身分識別轉換會單獨保留點的座標，而且不會將點移至新位置。</span><span class="sxs-lookup"><span data-stu-id="d35a3-153">In other words, the identity transform leaves the coordinates of points alone and does not shift the points to a new position.</span></span> <span data-ttu-id="d35a3-154">身分識別轉換以外的任何轉換將會修改物件的位置、形狀及/或大小。</span><span class="sxs-lookup"><span data-stu-id="d35a3-154">Any transform other than the identity transform will modify the position, shape, and/or size of objects.</span></span>

<span data-ttu-id="d35a3-155">轉換全都是關於座標，而且瞭解 Direct2D 座標空間對於瞭解轉換的使用而言很重要。</span><span class="sxs-lookup"><span data-stu-id="d35a3-155">Transforms are all about coordinates, and understanding the Direct2D coordinate space is important for understanding the use of transformations.</span></span>

## <a name="the-direct2d-coordinate-space"></a><span data-ttu-id="d35a3-156">Direct2D 座標空間</span><span class="sxs-lookup"><span data-stu-id="d35a3-156">The Direct2D Coordinate Space</span></span>

<span data-ttu-id="d35a3-157">Direct2D 使用左手座標空間;也就是說，正 X 軸的值會增加到右邊，且 y 軸值會向下增加。</span><span class="sxs-lookup"><span data-stu-id="d35a3-157">Direct2D uses a left-handed coordinate space; that is, positive x-axis values increase to the right and positive y-axis values increase downward.</span></span> <span data-ttu-id="d35a3-158">畫面上的所有內容都是相對於原點的位置，也就是 X 軸和 y 軸交集 (0，0) 的位置，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d35a3-158">Everything on the screen is positioned relative to the origin, which is the point where the x-axis and y-axis intersect (0, 0), as shown in the following illustration.</span></span> <span data-ttu-id="d35a3-159">Direct2D 呈現目標使用此座標空間。</span><span class="sxs-lookup"><span data-stu-id="d35a3-159">Direct2D render targets use this coordinate space.</span></span>

![左方座標空間的 X 軸和 y 軸圖例](images/coordinatespace.png)

<span data-ttu-id="d35a3-161">藉由操作轉換矩陣中的值，您可以旋轉、縮放、扭曲和移動 (轉譯) 物件。</span><span class="sxs-lookup"><span data-stu-id="d35a3-161">By manipulating values in a transformation matrix, you can rotate, scale, skew, and move (translate) an object.</span></span> <span data-ttu-id="d35a3-162">例如，如果您將 OffsetX 設定為100，並將 OffsetY 設為200，則會將物件移至右邊的100圖元和下200圖元。</span><span class="sxs-lookup"><span data-stu-id="d35a3-162">For example, if you set OffsetX to 100 and OffsetY to 200, you move the object to the right 100 pixels and down 200 pixels.</span></span>

<span data-ttu-id="d35a3-163">若要顯示物件移動的效果，您必須套用轉譯轉換來呈現目標、筆刷或幾何。</span><span class="sxs-lookup"><span data-stu-id="d35a3-163">To show the effect of the object move, you need to apply the translation transformation to render targets, brushes, or geometries.</span></span> <span data-ttu-id="d35a3-164">將轉換套用到轉譯目標會影響整個畫面，而將轉換套用至筆刷或幾何時，只會影響該特定筆刷或幾何。</span><span class="sxs-lookup"><span data-stu-id="d35a3-164">Applying a transform to render targets affects the entire screen, while applying a transform to a brush or a geometry only affects that specific brush or geometry.</span></span> <span data-ttu-id="d35a3-165">若要建立轉換矩陣，請使用 [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) 類別。</span><span class="sxs-lookup"><span data-stu-id="d35a3-165">To create a transformation matrix, use the [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span>

## <a name="creating-transformation-matrices"></a><span data-ttu-id="d35a3-166">建立轉換矩陣</span><span class="sxs-lookup"><span data-stu-id="d35a3-166">Creating Transformation Matrices</span></span>

<span data-ttu-id="d35a3-167">若要建立旋轉、縮放、扭曲和轉譯轉換， [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) 類別會提供下表所示的靜態方法。</span><span class="sxs-lookup"><span data-stu-id="d35a3-167">For creating rotation, scale, skew, and translation transformations, the [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class provides the static methods shown in the following table.</span></span> <span data-ttu-id="d35a3-168">資料表的 [範例] 資料行包含示範如何使用每個轉換方法的「如何」主題的連結。</span><span class="sxs-lookup"><span data-stu-id="d35a3-168">The Example column of the table contains links to the how-to topics that demonstrate how to use each transformation method.</span></span>



| <span data-ttu-id="d35a3-169">方法</span><span class="sxs-lookup"><span data-stu-id="d35a3-169">Method</span></span>                                                                   | <span data-ttu-id="d35a3-170">描述</span><span class="sxs-lookup"><span data-stu-id="d35a3-170">Description</span></span>                                                                                                     | <span data-ttu-id="d35a3-171">範例</span><span class="sxs-lookup"><span data-stu-id="d35a3-171">Example</span></span>                                            | <span data-ttu-id="d35a3-172">圖例</span><span class="sxs-lookup"><span data-stu-id="d35a3-172">Illustration</span></span>                                                                                                                            |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d35a3-173">**matrix3x2f：：旋轉**</span><span class="sxs-lookup"><span data-stu-id="d35a3-173">**matrix3x2f::rotate**</span></span>](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)                          | <span data-ttu-id="d35a3-174">建立具有指定角度和中心點的旋轉轉換。</span><span class="sxs-lookup"><span data-stu-id="d35a3-174">creates a rotation transformation that has the specified angle and center point.</span></span>                                | [<span data-ttu-id="d35a3-175">如何旋轉物件</span><span class="sxs-lookup"><span data-stu-id="d35a3-175">how to rotate an object</span></span>](how-to-rotate.md)       | ![以順時針方向與原始正方形中央旋轉45度的圖例](images/rotate-ovw.png)                 |
| <span data-ttu-id="d35a3-177">[**matrix3x2f：： scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span><span class="sxs-lookup"><span data-stu-id="d35a3-177">[**matrix3x2f::scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span></span> | <span data-ttu-id="d35a3-178">建立具有指定比例因數和中心點的縮放轉換。</span><span class="sxs-lookup"><span data-stu-id="d35a3-178">creates a scale transformation that has the specified scale factors and center point.</span></span>                           | [<span data-ttu-id="d35a3-179">如何調整物件</span><span class="sxs-lookup"><span data-stu-id="d35a3-179">how to scale an object</span></span>](how-to-scale.md)         | ![調整130% 的正方形圖例](images/scale-ovw.png)                                                                           |
| [<span data-ttu-id="d35a3-181">**matrix3x2f：：扭曲**</span><span class="sxs-lookup"><span data-stu-id="d35a3-181">**matrix3x2f::skew**</span></span>](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)                              | <span data-ttu-id="d35a3-182">建立具有指定 X 軸和 y 軸值和中心點的扭曲轉換。</span><span class="sxs-lookup"><span data-stu-id="d35a3-182">creates a skew transformation that has the specified x-axis and y-axis values and center point.</span></span>                 | [<span data-ttu-id="d35a3-183">如何扭曲物件</span><span class="sxs-lookup"><span data-stu-id="d35a3-183">how to skew an object</span></span>](how-to-skew.md)           | ![從 y 軸逆時針算起30度的正方形圖例](images/skew-ovw.png)                                     |
| <span data-ttu-id="d35a3-185">[**matrix3x2f：：轉譯**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span><span class="sxs-lookup"><span data-stu-id="d35a3-185">[**matrix3x2f::translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span></span>                | <span data-ttu-id="d35a3-186">建立轉譯轉換，並指定 X 軸和 y 軸方向的置換。</span><span class="sxs-lookup"><span data-stu-id="d35a3-186">creates a translation transformation and specifies the displacements in the direction of the x-axis and y-axis.</span></span> | [<span data-ttu-id="d35a3-187">如何轉譯物件</span><span class="sxs-lookup"><span data-stu-id="d35a3-187">how to translate an object</span></span>](how-to-translate.md) | ![正方形的圖，沿著正 X 軸移動20個單位，沿著正 y 軸移動10個單位](images/translation-ovw.png) |



 

## <a name="rendering-target-transforms"></a><span data-ttu-id="d35a3-189">轉譯目標轉換</span><span class="sxs-lookup"><span data-stu-id="d35a3-189">Rendering Target Transforms</span></span>

<span data-ttu-id="d35a3-190">轉譯目標是繼承自 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 介面的資源。</span><span class="sxs-lookup"><span data-stu-id="d35a3-190">A render target is a resource that inherits from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span> <span data-ttu-id="d35a3-191">它會建立用來繪製和執行實際繪圖作業的資源。</span><span class="sxs-lookup"><span data-stu-id="d35a3-191">It creates resources for drawing and performs actual drawing operations.</span></span> <span data-ttu-id="d35a3-192">它也提供轉換座標空間的方法。</span><span class="sxs-lookup"><span data-stu-id="d35a3-192">It also provides methods for transforming the coordinate space.</span></span> <span data-ttu-id="d35a3-193">您可以呼叫 [**ID2D1RenderTarget：： SetTransform**](id2d1rendertarget-settransform.md) 方法，將指定的轉換套用至轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="d35a3-193">You can call the [**ID2D1RenderTarget::SetTransform**](id2d1rendertarget-settransform.md) method to apply the specified transform to the render target.</span></span> <span data-ttu-id="d35a3-194">所有後續繪圖作業都會出現在已轉換的空間中。</span><span class="sxs-lookup"><span data-stu-id="d35a3-194">All subsequent drawing operations occur in the transformed space.</span></span>

<span data-ttu-id="d35a3-195">若要轉譯內容，請使用呈現目標的繪圖方法。</span><span class="sxs-lookup"><span data-stu-id="d35a3-195">To render content, use the render target's drawing methods.</span></span> <span data-ttu-id="d35a3-196">開始繪製之前，請先呼叫 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法。</span><span class="sxs-lookup"><span data-stu-id="d35a3-196">Before you begin drawing, call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method.</span></span> <span data-ttu-id="d35a3-197">若要完成轉譯內容，請呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。</span><span class="sxs-lookup"><span data-stu-id="d35a3-197">To finish rendering content, call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="d35a3-198">如需範例，請參閱 [如何將多個轉換套用至物件](how-to-apply-multiple-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="d35a3-198">For an example, see [How to Apply Multiple Transforms to an Object](how-to-apply-multiple-transforms.md).</span></span>

## <a name="brush-transforms"></a><span data-ttu-id="d35a3-199">筆刷轉換</span><span class="sxs-lookup"><span data-stu-id="d35a3-199">Brush Transforms</span></span>

<span data-ttu-id="d35a3-200">您可以藉由呼叫 [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))來調整筆刷上的轉換。</span><span class="sxs-lookup"><span data-stu-id="d35a3-200">You can adjust the transform on the brush by calling [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)).</span></span> <span data-ttu-id="d35a3-201">針對這項轉換，您可以將筆刷視為大型紙張以及不同轉譯基本專案， (文字、幾何、矩形等) 作為樣板。</span><span class="sxs-lookup"><span data-stu-id="d35a3-201">For this transform, you can think of the brush as a large piece of paper and of the different rendering primitives (text, geometry, rectangle and so on) as stencils.</span></span> <span data-ttu-id="d35a3-202">當您調整筆刷轉換時，就像是在樣板下滑動大量紙張，而不變更樣板本身的位置。</span><span class="sxs-lookup"><span data-stu-id="d35a3-202">When you adjust the brush transform, it is as if you were sliding the large piece of paper underneath the stencil, without changing the position of the stencil itself.</span></span> <span data-ttu-id="d35a3-203">您可以使用這項技術，將文字從黃色淡化成黑色，使其遠離3D 空間。</span><span class="sxs-lookup"><span data-stu-id="d35a3-203">You can use this technique to make the text fade from yellow to black away into 3D space.</span></span>

<span data-ttu-id="d35a3-204">當筆刷轉換是身分識別轉換時，筆刷會顯示在其繪製所在之轉譯目標的相同座標空間中。</span><span class="sxs-lookup"><span data-stu-id="d35a3-204">When the brush transform is the identity transform, brushes appear in the same coordinate space as the render target in which they are drawn.</span></span> <span data-ttu-id="d35a3-205">筆刷轉換可讓呼叫者改變筆刷座標組應至此空間的方式。</span><span class="sxs-lookup"><span data-stu-id="d35a3-205">The brush transform enables a caller to alter how brush coordinates map to this space.</span></span>

<span data-ttu-id="d35a3-206">在 Direct2D 中指定的筆刷空間，與 Windows Presentation Foundation (WPF) 不同。</span><span class="sxs-lookup"><span data-stu-id="d35a3-206">The brush space is specified differently in Direct2D than in Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="d35a3-207">在 Direct2D 中，筆刷空間不會相對於正在繪製的物件，而是轉譯目標的目前座標系統（由筆刷轉換轉換）（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d35a3-207">In Direct2D, the brush space is not relative to the object being drawn, but rather is the current coordinate system of the render target, transformed by the brush transform, if there is one.</span></span> <span data-ttu-id="d35a3-208">若要讓筆刷填滿在 WPF 中完成的物件，您必須將筆刷空間原點轉譯為物件之周框方塊的左上角，然後調整筆刷空間，讓基底磚填滿物件的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="d35a3-208">To have the brush fill an object as was done in WPF, you must translate the brush space origin to the top-left corner of the object's bounding box, and then scale the brush space so that the base tile fills the bounding box of the object.</span></span>

<span data-ttu-id="d35a3-209">如需筆刷轉換的詳細資訊，請參閱 [Direct2D 筆刷總覽](direct2d-brushes-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="d35a3-209">For more information about brush transforms, see [Direct2D Brushes Overview](direct2d-brushes-overview.md).</span></span>

## <a name="geometry-transforms"></a><span data-ttu-id="d35a3-210">幾何轉換</span><span class="sxs-lookup"><span data-stu-id="d35a3-210">Geometry Transforms</span></span>

<span data-ttu-id="d35a3-211">當您調整、移動、轉譯或扭曲幾何時，可以直接將轉換套用至特定幾何，而不是會影響整個畫面的轉譯目標轉換。</span><span class="sxs-lookup"><span data-stu-id="d35a3-211">When you scale, move, translate, or skew geometries, you can directly apply a transform to a specific geometry, not to a render target transform that would affect the entire screen.</span></span> <span data-ttu-id="d35a3-212">轉譯目標轉換通常會影響幾何的筆觸和填滿。</span><span class="sxs-lookup"><span data-stu-id="d35a3-212">A render target transform generally affects the stroke and fill of a geometry.</span></span> <span data-ttu-id="d35a3-213">相反地，geometry 轉換只會影響幾何的填滿，因為轉換會在繪製之前套用至幾何。</span><span class="sxs-lookup"><span data-stu-id="d35a3-213">By contrast, a geometry transform only affects the fill of a geometry, because the transform is applied to a geometry before it is stroked.</span></span>

> [!Note]  
> <span data-ttu-id="d35a3-214">從 Windows 8 開始，如果您將筆劃類型設定為 [**D2D1 \_ stroke \_ 轉換 \_ 類型 \_ 固定**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type) 或 [**D2D1 \_ 筆劃 \_ 轉換 \_ 類型的 \_ 細**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)項，則世界轉換不會影響筆劃。</span><span class="sxs-lookup"><span data-stu-id="d35a3-214">Starting with Windows 8, the world transform doesn't affect the stroke if you set the stroke type to [**D2D1\_STROKE\_TRANSFORM\_TYPE\_FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type) or [**D2D1\_STROKE\_TRANSFORM\_TYPE\_HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type).</span></span>

 

<span data-ttu-id="d35a3-215">您可以藉由呼叫 [**ID2D1Factory：： CreateTransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) 來建立 [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) 物件，藉以調整幾何的轉換。</span><span class="sxs-lookup"><span data-stu-id="d35a3-215">You can adjust the transform on a geometry by calling [**ID2D1Factory::CreateTransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) to create an [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) object.</span></span> <span data-ttu-id="d35a3-216">如需幾何轉換的詳細資訊，請參閱 [Direct2D 幾何總覽](direct2d-geometries-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="d35a3-216">For more information about geometry transforms, see [Direct2D Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="how-a-render-target-transform-affects-clips"></a><span data-ttu-id="d35a3-217">轉譯目標轉換如何影響剪輯</span><span class="sxs-lookup"><span data-stu-id="d35a3-217">How a Render Target Transform Affects Clips</span></span>

<span data-ttu-id="d35a3-218">轉譯目標上的轉換會影響以軸對齊的剪輯之周框方塊的計算方式。</span><span class="sxs-lookup"><span data-stu-id="d35a3-218">The transform on a render target affects how the bounding box of an axis-aligned clip is computed.</span></span> <span data-ttu-id="d35a3-219">呼叫 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) 時， *clipRect* 參數會由在轉譯目標上設定的目前世界轉換進行轉換。</span><span class="sxs-lookup"><span data-stu-id="d35a3-219">When the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) is called, the *clipRect* parameter is transformed by the current world transform that is set on the render target.</span></span> <span data-ttu-id="d35a3-220">將轉換套用至 *clipRect* 之後，就會計算 *clipRect* 的軸對齊周框方塊。</span><span class="sxs-lookup"><span data-stu-id="d35a3-220">After the transform is applied to the *clipRect*, the axis-aligned bounding box for the *clipRect* is computed.</span></span> <span data-ttu-id="d35a3-221">為了提高效率，會將內容裁剪成此軸對齊的周框方塊，而不是傳入的原始 *clipRect* 。</span><span class="sxs-lookup"><span data-stu-id="d35a3-221">For efficiency, the contents are clipped to this axis-aligned bounding box and not to the original *clipRect* that is passed in.</span></span> <span data-ttu-id="d35a3-222">下圖顯示如何將旋轉轉換套用到轉譯目標、產生的 *clipRect* 和計算軸對齊的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="d35a3-222">The following diagrams show how a rotation transform is applied to the render target, the resulting *clipRect*, and a calculated axis-aligned bounding box.</span></span>

1.  <span data-ttu-id="d35a3-223">假設下圖中的矩形是對齊螢幕圖元的呈現目標。</span><span class="sxs-lookup"><span data-stu-id="d35a3-223">Assume that the rectangle in the following illustration is a render target that is aligned to the screen pixels.</span></span>

    ![ (呈現目標) 的矩形圖例](images/pushaxisalignedclip-step1-rendertarget.png)

2.  <span data-ttu-id="d35a3-225">將旋轉轉換套用至呈現目標。</span><span class="sxs-lookup"><span data-stu-id="d35a3-225">Apply a rotation transform to the render target.</span></span> <span data-ttu-id="d35a3-226">在下圖中，黑色矩形代表原始轉譯目標，紅色虛線矩形表示已轉換的轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="d35a3-226">In the following illustration, the black rectangle represents the original render target and the red dashed rectangle represents the transformed render target.</span></span>

    ![原始矩形和旋轉矩形的圖例 (轉換的轉譯目標) ](images/pushaxisalignedclip-step2-transformed.png)

3.  <span data-ttu-id="d35a3-228">呼叫 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) 之後，會將旋轉轉換套用至 *clipRect*。</span><span class="sxs-lookup"><span data-stu-id="d35a3-228">After [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) is called, the rotation transform is applied to the *clipRect*.</span></span> <span data-ttu-id="d35a3-229">在下圖中，藍色矩形代表已轉換的 *clipRect*。</span><span class="sxs-lookup"><span data-stu-id="d35a3-229">In the following illustration, the blue rectangle represents the transformed *clipRect*.</span></span>

    ![小藍色矩形的圖例， (在旋轉矩形內的 cliprect)  (轉換的轉譯目標) ](images/pushaxisalignedclip-step3-cliprecttransformed.png)

4.  <span data-ttu-id="d35a3-231">計算軸對齊的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="d35a3-231">The axis-aligned bounding box is calculated.</span></span> <span data-ttu-id="d35a3-232">在下圖中，綠色虛線矩形表示周框方塊。</span><span class="sxs-lookup"><span data-stu-id="d35a3-232">In the following illustration, the green dashed rectangle represents the bounding box.</span></span> <span data-ttu-id="d35a3-233">所有的內容都會裁剪到此軸對齊的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="d35a3-233">All contents are clipped to this axis-aligned bounding box.</span></span>

    ![小藍色矩形上的綠色周框方塊的圖例 (cliprect) ](images/pushaxisalignedclip-step4-boundingbox.png)

## <a name="summary"></a><span data-ttu-id="d35a3-235">總結</span><span class="sxs-lookup"><span data-stu-id="d35a3-235">Summary</span></span>

<span data-ttu-id="d35a3-236">Direct2D 可讓您輕鬆地以簡化的座標空間和相關類別來轉換二維物件。</span><span class="sxs-lookup"><span data-stu-id="d35a3-236">Direct2D makes it easy to transform two-dimensional objects with simplified coordinate spaces and related classes.</span></span> <span data-ttu-id="d35a3-237">藉由使用各種類型的轉換，您可以平移、旋轉、扭曲及調整您的物件，以達到許多令人印象深刻的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="d35a3-237">By using various types of transforms, you can translate, rotate, skew, and scale your objects to achieve many impressive visual effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d35a3-238">相關主題</span><span class="sxs-lookup"><span data-stu-id="d35a3-238">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d35a3-239">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="d35a3-239">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 