---
description: 在整個 Direct3D 中，頂點描述位置及方向。 原始物件中的每個頂點都由給予它位置、色彩、紋理座標的向量，以及給予它方向的標準向量所述。
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: " (Direct3D 9 的向量、頂點和四元數) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c2e6e6e316b633359205ffd24a64aa349eeec74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509952"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a><span data-ttu-id="c886d-104"> (Direct3D 9 的向量、頂點和四元數) </span><span class="sxs-lookup"><span data-stu-id="c886d-104">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>

<span data-ttu-id="c886d-105">在整個 Direct3D 中，頂點描述位置及方向。</span><span class="sxs-lookup"><span data-stu-id="c886d-105">Throughout Direct3D, vertices describe position and orientation.</span></span> <span data-ttu-id="c886d-106">原始物件中的每個頂點都由給予它位置、色彩、紋理座標的向量，以及給予它方向的標準向量所述。</span><span class="sxs-lookup"><span data-stu-id="c886d-106">Each vertex in a primitive is described by a vector that gives its position, color, texture coordinates, and a normal vector that gives its orientation.</span></span>

<span data-ttu-id="c886d-107">四元數會將第四個元素新增至 \[ \] 定義三個分量向量的 x、y、z 值。</span><span class="sxs-lookup"><span data-stu-id="c886d-107">Quaternions add a fourth element to the \[x, y, z\] values that define a three-component-vector.</span></span> <span data-ttu-id="c886d-108">四元數是通常用於 3D 旋轉之矩陣方法的替代方法。</span><span class="sxs-lookup"><span data-stu-id="c886d-108">Quaternions are an alternative to the matrix methods that are typically used for 3D rotations.</span></span> <span data-ttu-id="c886d-109">四元數代表 3D 空間中的軸以及圍繞該軸的旋轉。</span><span class="sxs-lookup"><span data-stu-id="c886d-109">A quaternion represents an axis in 3D space and a rotation around that axis.</span></span> <span data-ttu-id="c886d-110">例如，四元數可能表示 (1,1,2) 軸及 1 弧度旋轉。</span><span class="sxs-lookup"><span data-stu-id="c886d-110">For example, a quaternion might represent a (1,1,2) axis and a rotation of 1 radian.</span></span> <span data-ttu-id="c886d-111">四元數載有重要資訊，但其真正的力量來自於您可以在其上執行兩項作業︰組合和內插補點。</span><span class="sxs-lookup"><span data-stu-id="c886d-111">Quaternions carry valuable information, but their true power comes from the two operations that you can perform on them: composition and interpolation.</span></span>

<span data-ttu-id="c886d-112">對四元數執行組合類似於結合它們。</span><span class="sxs-lookup"><span data-stu-id="c886d-112">Performing composition on quaternions is similar to combining them.</span></span> <span data-ttu-id="c886d-113">兩個四元數的組合如下圖表示。</span><span class="sxs-lookup"><span data-stu-id="c886d-113">The composition of two quaternions is notated like the following illustration.</span></span>

![四元數標記法的圖例](images/quateq.png)

<span data-ttu-id="c886d-115">兩個套用到幾何之四元數的組合表示「圍繞軸₂ 和旋轉角度₂ 旋轉幾何，然後圍繞軸₁ 和旋轉角度₁ 旋轉幾何。」</span><span class="sxs-lookup"><span data-stu-id="c886d-115">The composition of two quaternions applied to a geometry means "rotate the geometry around axis₂ by rotation₂, then rotate it around axis₁ by rotation₁."</span></span> <span data-ttu-id="c886d-116">在此情況下，Q 代表圍繞單一軸的旋轉，這是先套用 q₂ 再套用 q₁ 到幾何的結果。</span><span class="sxs-lookup"><span data-stu-id="c886d-116">In this case, Q represents a rotation around a single axis that is the result of applying q₂, then q₁ to the geometry.</span></span>

<span data-ttu-id="c886d-117">使用四元數內插補點，應用程式可以計算從某個軸和方向到另一個軸和方向順暢且合理的路徑。</span><span class="sxs-lookup"><span data-stu-id="c886d-117">Using quaternion interpolation, an application can calculate a smooth and reasonable path from one axis and orientation to another.</span></span> <span data-ttu-id="c886d-118">因此，q₁ 和 q₂ 之間內插補點提供從某個方向動畫到另一個方向的簡單方法。</span><span class="sxs-lookup"><span data-stu-id="c886d-118">Therefore, interpolation between q₁ and q₂ provides a simple way to animate from one orientation to another.</span></span>

<span data-ttu-id="c886d-119">當您一起使用組合和內插補點時，它讓您輕鬆進行看似複雜的幾何操作。</span><span class="sxs-lookup"><span data-stu-id="c886d-119">When you use composition and interpolation together, they provide you with a simple way to manipulate a geometry in a manner that appears complex.</span></span> <span data-ttu-id="c886d-120">例如，想像您有想要旋轉到特定方向的幾何。</span><span class="sxs-lookup"><span data-stu-id="c886d-120">For example, imagine that you have a geometry that you want to rotate to a given orientation.</span></span> <span data-ttu-id="c886d-121">您知道您想要將它圍繞軸₂ 旋轉 r₂ 度，然後圍繞軸₁ 旋轉 r₁ 度，但您不知道最終四元數。</span><span class="sxs-lookup"><span data-stu-id="c886d-121">You know that you want to rotate it r₂ degrees around axis₂, then rotate it r₁ degrees around axis₁, but you don't know the final quaternion.</span></span> <span data-ttu-id="c886d-122">使用組合，您可能會在幾何上組合兩個旋轉，取得單一四元數結果。</span><span class="sxs-lookup"><span data-stu-id="c886d-122">By using composition, you could combine the two rotations on the geometry to get a single quaternion that is the result.</span></span> <span data-ttu-id="c886d-123">然後，您可以從原始四元數到組合四元數內插值，達到平滑轉換。</span><span class="sxs-lookup"><span data-stu-id="c886d-123">Then, you could interpolate from the original to the composed quaternion to achieve a smooth transition from one to the other.</span></span>

<span data-ttu-id="c886d-124">D3DX 公用程式程式庫包含可協助您使用四元數的函數。</span><span class="sxs-lookup"><span data-stu-id="c886d-124">The D3DX utility library includes functions that help you work with quaternions.</span></span> <span data-ttu-id="c886d-125">例如， [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) 函式會將旋轉值新增至定義旋轉軸的向量，並將結果傳回 [**D3DXQUATERNION**](d3dxquaternion.md) 結構所定義的四元數。</span><span class="sxs-lookup"><span data-stu-id="c886d-125">For example, the [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) function adds a rotation value to a vector that defines an axis of rotation, and returns the result in a quaternion defined by a [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span> <span data-ttu-id="c886d-126">此外， [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) 函數會撰寫四元數，而 [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) 則會在兩個四元數之間執行球形線性插補。</span><span class="sxs-lookup"><span data-stu-id="c886d-126">Additionally, the [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) function composes quaternions and the [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) performs spherical linear interpolation between two quaternions.</span></span>

<span data-ttu-id="c886d-127">Direct3D 應用程式可使用下列函式來簡化處理四元數的工作。</span><span class="sxs-lookup"><span data-stu-id="c886d-127">Direct3D applications can use the following functions to simplify the task of working with quaternions.</span></span>

-   [<span data-ttu-id="c886d-128">**D3DXQuaternionBaryCentric**</span><span class="sxs-lookup"><span data-stu-id="c886d-128">**D3DXQuaternionBaryCentric**</span></span>](d3dxquaternionbarycentric.md)
-   [<span data-ttu-id="c886d-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="c886d-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
-   [<span data-ttu-id="c886d-130">**D3DXQuaternionDot**</span><span class="sxs-lookup"><span data-stu-id="c886d-130">**D3DXQuaternionDot**</span></span>](d3dxquaterniondot.md)
-   [<span data-ttu-id="c886d-131">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="c886d-131">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
-   [<span data-ttu-id="c886d-132">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="c886d-132">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
-   [<span data-ttu-id="c886d-133">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="c886d-133">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
-   [<span data-ttu-id="c886d-134">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="c886d-134">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
-   [<span data-ttu-id="c886d-135">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="c886d-135">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
-   [<span data-ttu-id="c886d-136">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="c886d-136">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
-   [<span data-ttu-id="c886d-137">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="c886d-137">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
-   [<span data-ttu-id="c886d-138">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="c886d-138">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
-   [<span data-ttu-id="c886d-139">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="c886d-139">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
-   [<span data-ttu-id="c886d-140">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="c886d-140">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
-   [<span data-ttu-id="c886d-141">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="c886d-141">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
-   [<span data-ttu-id="c886d-142">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="c886d-142">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
-   [<span data-ttu-id="c886d-143">**D3DXQuaternionSlerp**</span><span class="sxs-lookup"><span data-stu-id="c886d-143">**D3DXQuaternionSlerp**</span></span>](d3dxquaternionslerp.md)
-   [<span data-ttu-id="c886d-144">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="c886d-144">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
-   [<span data-ttu-id="c886d-145">**D3DXQuaternionToAxisAngle**</span><span class="sxs-lookup"><span data-stu-id="c886d-145">**D3DXQuaternionToAxisAngle**</span></span>](d3dxquaterniontoaxisangle.md)

<span data-ttu-id="c886d-146">Direct3D 應用程式可使用下列函式來簡化使用三個元件向量的工作。</span><span class="sxs-lookup"><span data-stu-id="c886d-146">Direct3D applications can use the following functions to simplify the task of working with three-component-vectors.</span></span>

-   [<span data-ttu-id="c886d-147">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="c886d-147">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
-   [<span data-ttu-id="c886d-148">**D3DXVec3BaryCentric**</span><span class="sxs-lookup"><span data-stu-id="c886d-148">**D3DXVec3BaryCentric**</span></span>](d3dxvec3barycentric.md)
-   [<span data-ttu-id="c886d-149">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="c886d-149">**D3DXVec3CatmullRom**</span></span>](d3dxvec3catmullrom.md)
-   [<span data-ttu-id="c886d-150">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="c886d-150">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
-   [<span data-ttu-id="c886d-151">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="c886d-151">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
-   [<span data-ttu-id="c886d-152">**D3DXVec3Hermite**</span><span class="sxs-lookup"><span data-stu-id="c886d-152">**D3DXVec3Hermite**</span></span>](d3dxvec3hermite.md)
-   [<span data-ttu-id="c886d-153">**D3DXVec3Length**</span><span class="sxs-lookup"><span data-stu-id="c886d-153">**D3DXVec3Length**</span></span>](d3dxvec3length.md)
-   [<span data-ttu-id="c886d-154">**D3DXVec3LengthSq**</span><span class="sxs-lookup"><span data-stu-id="c886d-154">**D3DXVec3LengthSq**</span></span>](d3dxvec3lengthsq.md)
-   [<span data-ttu-id="c886d-155">**D3DXVec3Lerp**</span><span class="sxs-lookup"><span data-stu-id="c886d-155">**D3DXVec3Lerp**</span></span>](d3dxvec3lerp.md)
-   [<span data-ttu-id="c886d-156">**D3DXVec3Maximize**</span><span class="sxs-lookup"><span data-stu-id="c886d-156">**D3DXVec3Maximize**</span></span>](d3dxvec3maximize.md)
-   [<span data-ttu-id="c886d-157">**D3DXVec3Minimize**</span><span class="sxs-lookup"><span data-stu-id="c886d-157">**D3DXVec3Minimize**</span></span>](d3dxvec3minimize.md)
-   [<span data-ttu-id="c886d-158">**D3DXVec3Normalize**</span><span class="sxs-lookup"><span data-stu-id="c886d-158">**D3DXVec3Normalize**</span></span>](d3dxvec3normalize.md)
-   [<span data-ttu-id="c886d-159">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="c886d-159">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
-   [<span data-ttu-id="c886d-160">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="c886d-160">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
-   [<span data-ttu-id="c886d-161">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="c886d-161">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
-   [<span data-ttu-id="c886d-162">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="c886d-162">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
-   [<span data-ttu-id="c886d-163">**D3DXVec3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="c886d-163">**D3DXVec3TransformCoord**</span></span>](d3dxvec3transformcoord.md)
-   [<span data-ttu-id="c886d-164">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="c886d-164">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
-   [<span data-ttu-id="c886d-165">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="c886d-165">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)

<span data-ttu-id="c886d-166">D3DX 公用程式程式庫所提供的 [數學](dx9-graphics-reference-d3dx-functions-math.md) 函式包含許多額外的函式，可簡化使用雙和四個元件向量的工作。</span><span class="sxs-lookup"><span data-stu-id="c886d-166">Many additional functions that simplify tasks using two- and four-component-vectors are included among the [Math Functions](dx9-graphics-reference-d3dx-functions-math.md) supplied by the D3DX utility library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c886d-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="c886d-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c886d-168">座標系統和幾何</span><span class="sxs-lookup"><span data-stu-id="c886d-168">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



