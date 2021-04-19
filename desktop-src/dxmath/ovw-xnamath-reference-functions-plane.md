---
description: 列出 DirectXMath 所提供的平面函數。
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: DirectXMath 程式庫平面函式
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b3f450b4dbaa5ed1b4348ad8b090210c14e2022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983383"
---
# <a name="directxmath-library-plane-functions"></a><span data-ttu-id="19916-103">DirectXMath 程式庫平面函式</span><span class="sxs-lookup"><span data-stu-id="19916-103">DirectXMath Library plane functions</span></span>

<span data-ttu-id="19916-104">列出 DirectXMath 所提供的平面函數。</span><span class="sxs-lookup"><span data-stu-id="19916-104">Lists the plane functions provided by DirectXMath.</span></span>

<span data-ttu-id="19916-105">這些函式會使用 XMVECTOR 4 向量來代表平面方程式的係數，Ax + By + Cz + D = 0，其中 X 元件為 A，Y 元件為 B，Z 元件為 C，而 W 元件為 D。</span><span class="sxs-lookup"><span data-stu-id="19916-105">These functions use an XMVECTOR 4-vector to represent the coefficients of the plane equation, Ax+By+Cz+D = 0, where the X-component is A, the Y-component is B, the Z-component is C, and the W-component is D.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="19916-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="19916-106">In this section</span></span>



| <span data-ttu-id="19916-107">主題</span><span class="sxs-lookup"><span data-stu-id="19916-107">Topic</span></span>                                                               | <span data-ttu-id="19916-108">描述</span><span class="sxs-lookup"><span data-stu-id="19916-108">Description</span></span>                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19916-109">**XMPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="19916-109">**XMPlaneDot**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | <span data-ttu-id="19916-110">計算輸入平面與4D 向量之間的點乘積。</span><span class="sxs-lookup"><span data-stu-id="19916-110">Calculates the dot product between an input plane and a 4D vector.</span></span><br/>                                    |
| [<span data-ttu-id="19916-111">**XMPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="19916-111">**XMPlaneDotCoord**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | <span data-ttu-id="19916-112">計算輸入平面和3D 向量之間的點乘積。</span><span class="sxs-lookup"><span data-stu-id="19916-112">Calculates the dot product between an input plane and a 3D vector.</span></span><br/>                                    |
| [<span data-ttu-id="19916-113">**XMPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="19916-113">**XMPlaneDotNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | <span data-ttu-id="19916-114">計算平面的一般向量和3D 向量之間的點乘積。</span><span class="sxs-lookup"><span data-stu-id="19916-114">Calculates the dot product between the normal vector of a plane and a 3D vector.</span></span><br/>                      |
| [<span data-ttu-id="19916-115">**XMPlaneEqual**</span><span class="sxs-lookup"><span data-stu-id="19916-115">**XMPlaneEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | <span data-ttu-id="19916-116">判斷兩個平面是否相等。</span><span class="sxs-lookup"><span data-stu-id="19916-116">Determines if two planes are equal.</span></span><br/>                                                                   |
| [<span data-ttu-id="19916-117">**XMPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="19916-117">**XMPlaneFromPointNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | <span data-ttu-id="19916-118">計算平面的方程式，從平面中的某個點，到一般向量。</span><span class="sxs-lookup"><span data-stu-id="19916-118">Computes the equation of a plane constructed from a point in the plane and a normal vector.</span></span><br/>           |
| [<span data-ttu-id="19916-119">**XMPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="19916-119">**XMPlaneFromPoints**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | <span data-ttu-id="19916-120">計算平面中的三個點所構成平面的方程式。</span><span class="sxs-lookup"><span data-stu-id="19916-120">Computes the equation of a plane constructed from three points in the plane.</span></span><br/>                          |
| [<span data-ttu-id="19916-121">**XMPlaneIntersectLine**</span><span class="sxs-lookup"><span data-stu-id="19916-121">**XMPlaneIntersectLine**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | <span data-ttu-id="19916-122">尋找平面和直線之間的交集。</span><span class="sxs-lookup"><span data-stu-id="19916-122">Finds the intersection between a plane and a line.</span></span><br/>                                                    |
| [<span data-ttu-id="19916-123">**XMPlaneIntersectPlane**</span><span class="sxs-lookup"><span data-stu-id="19916-123">**XMPlaneIntersectPlane**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | <span data-ttu-id="19916-124">尋找兩個平面的交集。</span><span class="sxs-lookup"><span data-stu-id="19916-124">Finds the intersection of two planes.</span></span><br/>                                                                 |
| [<span data-ttu-id="19916-125">**XMPlaneIsInfinite**</span><span class="sxs-lookup"><span data-stu-id="19916-125">**XMPlaneIsInfinite**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | <span data-ttu-id="19916-126">測試平面的任何係數是否為正數或負無限大。</span><span class="sxs-lookup"><span data-stu-id="19916-126">Tests whether any of the coefficients of a plane is positive or negative infinity.</span></span><br/>                    |
| [<span data-ttu-id="19916-127">**XMPlaneIsNaN**</span><span class="sxs-lookup"><span data-stu-id="19916-127">**XMPlaneIsNaN**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | <span data-ttu-id="19916-128">測試平面的任何係數是否為 NaN。</span><span class="sxs-lookup"><span data-stu-id="19916-128">Tests whether any of the coefficients of a plane is a NaN.</span></span><br/>                                            |
| [<span data-ttu-id="19916-129">**XMPlaneNearEqual**</span><span class="sxs-lookup"><span data-stu-id="19916-129">**XMPlaneNearEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | <span data-ttu-id="19916-130">判斷兩個平面是否幾乎相等。</span><span class="sxs-lookup"><span data-stu-id="19916-130">Determines whether two planes are nearly equal.</span></span><br/>                                                       |
| [<span data-ttu-id="19916-131">**XMPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="19916-131">**XMPlaneNormalize**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | <span data-ttu-id="19916-132">正規化平面的係數，讓 x、y 和 z 的係數形成一個單元一般向量。</span><span class="sxs-lookup"><span data-stu-id="19916-132">Normalizes the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/> |
| [<span data-ttu-id="19916-133">**XMPlaneNormalizeEst**</span><span class="sxs-lookup"><span data-stu-id="19916-133">**XMPlaneNormalizeEst**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | <span data-ttu-id="19916-134">預估平面的係數，讓 x、y 和 z 的係數形成一個單元一般向量。</span><span class="sxs-lookup"><span data-stu-id="19916-134">Estimates the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/>  |
| [<span data-ttu-id="19916-135">**XMPlaneNotEqual**</span><span class="sxs-lookup"><span data-stu-id="19916-135">**XMPlaneNotEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | <span data-ttu-id="19916-136">判斷兩個平面是否不相等。</span><span class="sxs-lookup"><span data-stu-id="19916-136">Determines if two planes are unequal.</span></span><br/>                                                                 |
| [<span data-ttu-id="19916-137">**XMPlaneTransform**</span><span class="sxs-lookup"><span data-stu-id="19916-137">**XMPlaneTransform**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | <span data-ttu-id="19916-138">依指定的矩陣轉換平面。</span><span class="sxs-lookup"><span data-stu-id="19916-138">Transforms a plane by a given matrix.</span></span><br/>                                                                 |
| [<span data-ttu-id="19916-139">**XMPlaneTransformStream**</span><span class="sxs-lookup"><span data-stu-id="19916-139">**XMPlaneTransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | <span data-ttu-id="19916-140">依指定的矩陣轉換平面的資料流程。</span><span class="sxs-lookup"><span data-stu-id="19916-140">Transforms a stream of planes by a given matrix.</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="19916-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="19916-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19916-142">DirectXMath 程式庫函式</span><span class="sxs-lookup"><span data-stu-id="19916-142">DirectXMath Library Functions</span></span>](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
