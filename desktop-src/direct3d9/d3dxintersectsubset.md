---
description: 將指定的光線與指定的網格子集相交。 這會提供類似的功能來 D3DXIntersect。
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: 'D3DXIntersectSubset 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 621f45d7c2a6d8ff162f539ef62153d3ae70f6e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196253"
---
# <a name="d3dxintersectsubset-function"></a><span data-ttu-id="6711f-104">D3DXIntersectSubset 函式</span><span class="sxs-lookup"><span data-stu-id="6711f-104">D3DXIntersectSubset function</span></span>

<span data-ttu-id="6711f-105">將指定的光線與指定的網格子集相交。</span><span class="sxs-lookup"><span data-stu-id="6711f-105">Intersects the specified ray with the given mesh subset.</span></span> <span data-ttu-id="6711f-106">這會提供類似的功能來 [**D3DXIntersect**](d3dxintersect.md)。</span><span class="sxs-lookup"><span data-stu-id="6711f-106">This provides similar functionality to [**D3DXIntersect**](d3dxintersect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6711f-107">語法</span><span class="sxs-lookup"><span data-stu-id="6711f-107">Syntax</span></span>


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a><span data-ttu-id="6711f-108">參數</span><span class="sxs-lookup"><span data-stu-id="6711f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6711f-109">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6711f-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6711f-110">類型： **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="6711f-110">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="6711f-111">[**ID3DXBaseMesh**](id3dxbasemesh.md)介面的指標，代表要測試的網格。</span><span class="sxs-lookup"><span data-stu-id="6711f-111">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span> <span data-ttu-id="6711f-112">網格必須進行屬性排序。</span><span class="sxs-lookup"><span data-stu-id="6711f-112">The mesh must be attribute sorted.</span></span>

</dd> <dt>

<span data-ttu-id="6711f-113">*AttribId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6711f-113">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6711f-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6711f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6711f-115">要與交集之子集的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="6711f-115">Attribute identifier of the subset to intersect with.</span></span>

</dd> <dt>

<span data-ttu-id="6711f-116">*pRayPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6711f-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6711f-117">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6711f-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6711f-118">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線開始的時間點。</span><span class="sxs-lookup"><span data-stu-id="6711f-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="6711f-119">*pRayDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6711f-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6711f-120">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6711f-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6711f-121">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線的方向。</span><span class="sxs-lookup"><span data-stu-id="6711f-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="6711f-122">*pHit* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6711f-122">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6711f-123">類型： **[ **BOOL**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6711f-123">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6711f-124">BOOL 的指標。</span><span class="sxs-lookup"><span data-stu-id="6711f-124">Pointer to a BOOL.</span></span> <span data-ttu-id="6711f-125">如果光線與網格上的三角形面相交，此值將會設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6711f-125">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="6711f-126">否則，此值會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6711f-126">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6711f-127">*pFaceIndex* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6711f-127">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6711f-128">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6711f-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6711f-129">如果 pHit 為 **TRUE**，則為最接近光線原點之臉部的索引值指標。</span><span class="sxs-lookup"><span data-stu-id="6711f-129">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="6711f-130">*pU* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6711f-130">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6711f-131">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6711f-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6711f-132">Barycentric 點擊座標的指標，U。</span><span class="sxs-lookup"><span data-stu-id="6711f-132">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="6711f-133">*pV* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6711f-133">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6711f-134">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6711f-134">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6711f-135">Barycentric 點擊座標的指標，V。</span><span class="sxs-lookup"><span data-stu-id="6711f-135">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="6711f-136">*pDist* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6711f-136">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6711f-137">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6711f-137">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6711f-138">光線交集參數距離的指標。</span><span class="sxs-lookup"><span data-stu-id="6711f-138">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="6711f-139">*ppAllHits* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6711f-139">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6711f-140">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6711f-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6711f-141">[**D3DXINTERSECTINFO**](d3dxintersectinfo.md)結構的陣列，代表所有的點擊，而不只是最接近的點擊。</span><span class="sxs-lookup"><span data-stu-id="6711f-141">Array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures, representing all hits, not just closest hits.</span></span>

</dd> <dt>

<span data-ttu-id="6711f-142">*pCountOfHits* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6711f-142">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6711f-143">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6711f-143">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6711f-144">從 ppAllHits 傳回之陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="6711f-144">Number of elements in the array returned from ppAllHits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6711f-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="6711f-145">Return value</span></span>

<span data-ttu-id="6711f-146">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6711f-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6711f-147">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6711f-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6711f-148">如果函式失敗，則傳回值可以是下列值： E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="6711f-148">If the function fails, the return value can be the following value: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6711f-149">備註</span><span class="sxs-lookup"><span data-stu-id="6711f-149">Remarks</span></span>

<span data-ttu-id="6711f-150">**D3DXIntersectSubset** 函式可讓您瞭解三角形中和周圍的點，而不受三角形實際位置的影響。</span><span class="sxs-lookup"><span data-stu-id="6711f-150">The **D3DXIntersectSubset** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="6711f-151">此函式會使用下列方程式傳回結果點： V1 + U (V2-V1) + V (V3-V1) 。</span><span class="sxs-lookup"><span data-stu-id="6711f-151">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="6711f-152">平面 V1V2V3 中的任何點都可由 barycentric 座標 (U，V) 表示。</span><span class="sxs-lookup"><span data-stu-id="6711f-152">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="6711f-153">參數 U 會控制要將多少 V2 加權至結果，而參數 V 控制要將多少 V3 加權到結果中。</span><span class="sxs-lookup"><span data-stu-id="6711f-153">The parameter U controls how much V2 gets weighted into the result and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="6711f-154">最後， \[ 1 (U + V) 的值會 \] 控制 V1 在結果中的加權量。</span><span class="sxs-lookup"><span data-stu-id="6711f-154">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="6711f-155">Barycentric 座標是一種一般座標形式。</span><span class="sxs-lookup"><span data-stu-id="6711f-155">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="6711f-156">在此內容中，使用 barycentric 座標代表座標系統中的變更。</span><span class="sxs-lookup"><span data-stu-id="6711f-156">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="6711f-157">笛卡兒座標的 true 是 barycentric 座標的 true。</span><span class="sxs-lookup"><span data-stu-id="6711f-157">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="6711f-158">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="6711f-158">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="6711f-159">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="6711f-159">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="6711f-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="6711f-160">Requirements</span></span>



| <span data-ttu-id="6711f-161">需求</span><span class="sxs-lookup"><span data-stu-id="6711f-161">Requirement</span></span> | <span data-ttu-id="6711f-162">值</span><span class="sxs-lookup"><span data-stu-id="6711f-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6711f-163">標頭</span><span class="sxs-lookup"><span data-stu-id="6711f-163">Header</span></span><br/>  | <dl> <span data-ttu-id="6711f-164"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6711f-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6711f-165">程式庫</span><span class="sxs-lookup"><span data-stu-id="6711f-165">Library</span></span><br/> | <dl> <span data-ttu-id="6711f-166"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6711f-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6711f-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6711f-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6711f-168">網格函數</span><span class="sxs-lookup"><span data-stu-id="6711f-168">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
