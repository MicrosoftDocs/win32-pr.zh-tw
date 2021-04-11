---
description: 判斷光線是否與這個網格的子集相交。
ms.assetid: 31f90141-60be-4c7f-8d6a-a1a97ff26d9d
title: ID3DX10Mesh::IntersectSubset 方法 (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.IntersectSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a08d4db92dc75f40d0073367dda9a9ea26863418
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196357"
---
# <a name="id3dx10meshintersectsubset-method"></a><span data-ttu-id="6df48-103">ID3DX10Mesh：： IntersectSubset 方法</span><span class="sxs-lookup"><span data-stu-id="6df48-103">ID3DX10Mesh::IntersectSubset method</span></span>

<span data-ttu-id="6df48-104">判斷光線是否與這個網格的子集相交。</span><span class="sxs-lookup"><span data-stu-id="6df48-104">Determines if a ray intersects with a subset of this mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df48-105">語法</span><span class="sxs-lookup"><span data-stu-id="6df48-105">Syntax</span></span>


```C++
HRESULT IntersectSubset(
  [in]  UINT        AttribId,
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a><span data-ttu-id="6df48-106">參數</span><span class="sxs-lookup"><span data-stu-id="6df48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6df48-107">*AttribId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6df48-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df48-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6df48-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6df48-109">識別網格子集的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="6df48-109">Attribute ID identifying the subset of the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6df48-110">*pRayPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6df48-110">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df48-111">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6df48-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6df48-112">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，指定光線開始的時間點。</span><span class="sxs-lookup"><span data-stu-id="6df48-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="6df48-113">*pRayDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6df48-113">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df48-114">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6df48-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6df48-115">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，指定光線的方向。</span><span class="sxs-lookup"><span data-stu-id="6df48-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="6df48-116">*pHitCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6df48-116">*pHitCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df48-117">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6df48-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6df48-118">光線與網格交集的次數。</span><span class="sxs-lookup"><span data-stu-id="6df48-118">The number of times the ray intersected with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6df48-119">*pFaceIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6df48-119">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df48-120">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6df48-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6df48-121">如果 pHit 為 **TRUE**，則為最接近光線原點之臉部的索引值指標。</span><span class="sxs-lookup"><span data-stu-id="6df48-121">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="6df48-122">*pU* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6df48-122">*pU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df48-123">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="6df48-123">Type: **float\***</span></span>

<span data-ttu-id="6df48-124">Barycentric 點擊座標的指標，U。</span><span class="sxs-lookup"><span data-stu-id="6df48-124">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="6df48-125">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6df48-125">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df48-126">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="6df48-126">Type: **float\***</span></span>

<span data-ttu-id="6df48-127">Barycentric 點擊座標的指標，V。</span><span class="sxs-lookup"><span data-stu-id="6df48-127">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="6df48-128">*pDist* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6df48-128">*pDist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df48-129">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="6df48-129">Type: **float\***</span></span>

<span data-ttu-id="6df48-130">光線交集參數距離的指標。</span><span class="sxs-lookup"><span data-stu-id="6df48-130">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="6df48-131">*ppAllHits* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6df48-131">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6df48-132">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="6df48-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="6df48-133">[**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)的指標，其中包含 [**D3DX10 \_ INTERSECT \_ 資訊**](d3dx10-intersect-info.md)結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="6df48-133">Pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), containing an array of [**D3DX10\_INTERSECT\_INFO**](d3dx10-intersect-info.md) structures.</span></span> <span data-ttu-id="6df48-134">這是交集測試中發生的所有點擊清單。</span><span class="sxs-lookup"><span data-stu-id="6df48-134">This is a list of all the hits that occurred in the intersection test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6df48-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="6df48-135">Return value</span></span>

<span data-ttu-id="6df48-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6df48-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6df48-137">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6df48-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6df48-138">備註</span><span class="sxs-lookup"><span data-stu-id="6df48-138">Remarks</span></span>

<span data-ttu-id="6df48-139">此 API 提供一種方式來瞭解三角形中和周圍的點，與三角形實際所在的位置無關。</span><span class="sxs-lookup"><span data-stu-id="6df48-139">This API provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="6df48-140">此函式會使用下列方程式傳回結果點： V1 + U (V2-V1) + V (V3-V1) 。</span><span class="sxs-lookup"><span data-stu-id="6df48-140">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="6df48-141">平面 V1V2V3 中的任何點都可由 barycentric 座標 (U，V) 表示。</span><span class="sxs-lookup"><span data-stu-id="6df48-141">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="6df48-142">參數 U 會控制要將多少 V2 加權至結果中，而參數 V 控制要將多少 V3 加權到結果中。</span><span class="sxs-lookup"><span data-stu-id="6df48-142">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="6df48-143">最後， \[ 1 (U + V) 的值會 \] 控制 V1 在結果中的加權量。</span><span class="sxs-lookup"><span data-stu-id="6df48-143">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="6df48-144">Barycentric 座標是一種一般座標形式。</span><span class="sxs-lookup"><span data-stu-id="6df48-144">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="6df48-145">在此內容中，使用 barycentric 座標代表座標系統中的變更。</span><span class="sxs-lookup"><span data-stu-id="6df48-145">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="6df48-146">笛卡兒座標的 true 是 barycentric 座標的 true。</span><span class="sxs-lookup"><span data-stu-id="6df48-146">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="6df48-147">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="6df48-147">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="6df48-148">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="6df48-148">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="6df48-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="6df48-149">Requirements</span></span>



| <span data-ttu-id="6df48-150">需求</span><span class="sxs-lookup"><span data-stu-id="6df48-150">Requirement</span></span> | <span data-ttu-id="6df48-151">值</span><span class="sxs-lookup"><span data-stu-id="6df48-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6df48-152">標頭</span><span class="sxs-lookup"><span data-stu-id="6df48-152">Header</span></span><br/>  | <dl> <span data-ttu-id="6df48-153"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="6df48-153"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6df48-154">程式庫</span><span class="sxs-lookup"><span data-stu-id="6df48-154">Library</span></span><br/> | <dl> <span data-ttu-id="6df48-155"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6df48-155"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6df48-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6df48-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df48-157">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="6df48-157">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="6df48-158">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="6df48-158">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
