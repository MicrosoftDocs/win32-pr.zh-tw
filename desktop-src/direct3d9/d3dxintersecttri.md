---
description: D3DXIntersectTri 函數 (D3DX9Mesh) -計算光線和三角形的交集。
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: 'D3DXIntersectTri 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectTri
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33d45beda51a7a2c80debafbab864c2accb33653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098266"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a><span data-ttu-id="ee6fa-103">D3DXIntersectTri 函式 (D3DX9Mesh) </span><span class="sxs-lookup"><span data-stu-id="ee6fa-103">D3DXIntersectTri function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="ee6fa-104">計算光線和三角形的交集。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee6fa-105">語法</span><span class="sxs-lookup"><span data-stu-id="ee6fa-105">Syntax</span></span>


```C++
BOOL D3DXIntersectTri(
  _In_  const D3DXVECTOR3 *p0,
  _In_  const D3DXVECTOR3 *p1,
  _In_  const D3DXVECTOR3 *p2,
  _In_  const D3DXVECTOR3 *pRayPos,
  _In_  const D3DXVECTOR3 *pRayDir,
  _Out_       FLOAT       *pU,
  _Out_       FLOAT       *pV,
  _Out_       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="ee6fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee6fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee6fa-107">*p0* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee6fa-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6fa-108">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ee6fa-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ee6fa-109">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，描述第一個三角形頂點的位置。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="ee6fa-110">*p1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee6fa-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6fa-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ee6fa-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ee6fa-112">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，描述第二個三角形頂點的位置。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="ee6fa-113">*p2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee6fa-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6fa-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ee6fa-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ee6fa-115">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，描述第三個三角形頂點的位置。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="ee6fa-116">*pRayPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee6fa-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6fa-117">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ee6fa-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ee6fa-118">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線開始的時間點。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="ee6fa-119">*pRayDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee6fa-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6fa-120">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ee6fa-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ee6fa-121">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線的方向。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="ee6fa-122">*pU* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ee6fa-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6fa-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee6fa-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ee6fa-124">Barycentric 點擊座標、U。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="ee6fa-125">*pV* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ee6fa-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6fa-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee6fa-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ee6fa-127">Barycentric 點擊座標，V。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="ee6fa-128">*pDist* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ee6fa-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee6fa-129">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee6fa-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ee6fa-130">光線交集參數距離。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee6fa-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee6fa-131">Return value</span></span>

<span data-ttu-id="ee6fa-132">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee6fa-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee6fa-133">如果光線與三角形的區域相交，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="ee6fa-134">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee6fa-135">備註</span><span class="sxs-lookup"><span data-stu-id="ee6fa-135">Remarks</span></span>

<span data-ttu-id="ee6fa-136">[**D3DXIntersect**](d3dxintersect.md)函式可讓您瞭解三角形中和周圍的點，而不受三角形實際位置的影響。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-136">The [**D3DXIntersect**](d3dxintersect.md) function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="ee6fa-137">此函式會使用下列方程式傳回結果點： V1 + U (V2-V1) + V (V3-V1) 。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="ee6fa-138">平面 V1V2V3 中的任何點都可由 barycentric 座標 (U，V) 表示。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="ee6fa-139">參數 U 會控制要將多少 V2 加權至結果中，而參數 V 控制要將多少 V3 加權到結果中。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="ee6fa-140">最後， \[ 1 (U + V) 的值會 \] 控制 V1 在結果中的加權量。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="ee6fa-141">Barycentric 座標是一種一般座標形式。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="ee6fa-142">在此內容中，使用 barycentric 座標代表座標系統中的變更。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="ee6fa-143">笛卡兒座標的 true 是 barycentric 座標的 true。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="ee6fa-144">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="ee6fa-145">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="ee6fa-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee6fa-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee6fa-146">Requirements</span></span>



| <span data-ttu-id="ee6fa-147">需求</span><span class="sxs-lookup"><span data-stu-id="ee6fa-147">Requirement</span></span> | <span data-ttu-id="ee6fa-148">值</span><span class="sxs-lookup"><span data-stu-id="ee6fa-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee6fa-149">標頭</span><span class="sxs-lookup"><span data-stu-id="ee6fa-149">Header</span></span><br/>  | <dl> <span data-ttu-id="ee6fa-150"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee6fa-150"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ee6fa-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="ee6fa-151">Library</span></span><br/> | <dl> <span data-ttu-id="ee6fa-152"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee6fa-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ee6fa-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee6fa-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee6fa-154">網格函數</span><span class="sxs-lookup"><span data-stu-id="ee6fa-154">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
