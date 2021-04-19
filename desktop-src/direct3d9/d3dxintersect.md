---
description: 判斷光線是否與網格交集。
ms.assetid: 325f5b40-80ba-4400-a143-bae41146ab07
title: 'D3DXIntersect 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc877fb1301e01b05184625ba2e92a2c680cfa9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997390"
---
# <a name="d3dxintersect-function"></a><span data-ttu-id="815bc-103">D3DXIntersect 函式</span><span class="sxs-lookup"><span data-stu-id="815bc-103">D3DXIntersect function</span></span>

<span data-ttu-id="815bc-104">判斷光線是否與網格交集。</span><span class="sxs-lookup"><span data-stu-id="815bc-104">Determines if a ray intersects with a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="815bc-105">語法</span><span class="sxs-lookup"><span data-stu-id="815bc-105">Syntax</span></span>


```C++
HRESULT D3DXIntersect(
  _In_        LPD3DXBASEMESH pMesh,
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



## <a name="parameters"></a><span data-ttu-id="815bc-106">參數</span><span class="sxs-lookup"><span data-stu-id="815bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="815bc-107">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="815bc-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="815bc-108">類型： **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="815bc-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="815bc-109">[**ID3DXBaseMesh**](id3dxbasemesh.md)介面的指標，代表要測試的網格。</span><span class="sxs-lookup"><span data-stu-id="815bc-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="815bc-110">*pRayPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="815bc-110">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="815bc-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="815bc-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="815bc-112">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線開始的時間點。</span><span class="sxs-lookup"><span data-stu-id="815bc-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="815bc-113">*pRayDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="815bc-113">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="815bc-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="815bc-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="815bc-115">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線的方向。</span><span class="sxs-lookup"><span data-stu-id="815bc-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="815bc-116">*pHit* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="815bc-116">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="815bc-117">類型： **[ **BOOL**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="815bc-117">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="815bc-118">BOOL 的指標。</span><span class="sxs-lookup"><span data-stu-id="815bc-118">Pointer to a BOOL.</span></span> <span data-ttu-id="815bc-119">如果光線與網格上的三角形面相交，此值將會設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="815bc-119">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="815bc-120">否則，此值會設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="815bc-120">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="815bc-121">*pFaceIndex* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="815bc-121">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="815bc-122">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="815bc-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="815bc-123">如果 pHit 為 **TRUE**，則為最接近光線原點之臉部的索引值指標。</span><span class="sxs-lookup"><span data-stu-id="815bc-123">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="815bc-124">*pU* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="815bc-124">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="815bc-125">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="815bc-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="815bc-126">Barycentric 點擊座標的指標，U。</span><span class="sxs-lookup"><span data-stu-id="815bc-126">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="815bc-127">*pV* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="815bc-127">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="815bc-128">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="815bc-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="815bc-129">Barycentric 點擊座標的指標，V。</span><span class="sxs-lookup"><span data-stu-id="815bc-129">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="815bc-130">*pDist* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="815bc-130">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="815bc-131">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="815bc-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="815bc-132">光線交集參數距離的指標。</span><span class="sxs-lookup"><span data-stu-id="815bc-132">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="815bc-133">*ppAllHits* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="815bc-133">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="815bc-134">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="815bc-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="815bc-135">[**ID3DXBuffer**](id3dxbuffer.md)物件的指標，其中包含 [**D3DXINTERSECTINFO**](d3dxintersectinfo.md)結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="815bc-135">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) object, containing an array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="815bc-136">*pCountOfHits* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="815bc-136">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="815bc-137">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="815bc-137">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="815bc-138">DWORD 的指標，其中包含 ppAllHits 陣列中的專案數。</span><span class="sxs-lookup"><span data-stu-id="815bc-138">Pointer to a DWORD that contains the number of entries in the ppAllHits array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="815bc-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="815bc-139">Return value</span></span>

<span data-ttu-id="815bc-140">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="815bc-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="815bc-141">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="815bc-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="815bc-142">如果函式失敗，則傳回值可以是： E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="815bc-142">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="815bc-143">備註</span><span class="sxs-lookup"><span data-stu-id="815bc-143">Remarks</span></span>

<span data-ttu-id="815bc-144">**D3DXIntersect** 函式可讓您瞭解三角形中和周圍的點，而不受三角形實際位置的影響。</span><span class="sxs-lookup"><span data-stu-id="815bc-144">The **D3DXIntersect** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="815bc-145">此函式會使用下列方程式傳回結果點： V1 + U (V2-V1) + V (V3-V1) 。</span><span class="sxs-lookup"><span data-stu-id="815bc-145">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="815bc-146">平面 V1V2V3 中的任何點都可由 barycentric 座標 (U，V) 表示。</span><span class="sxs-lookup"><span data-stu-id="815bc-146">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="815bc-147">參數 U 會控制要將多少 V2 加權至結果中，而參數 V 控制要將多少 V3 加權到結果中。</span><span class="sxs-lookup"><span data-stu-id="815bc-147">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="815bc-148">最後， \[ 1 (U + V) 的值會 \] 控制 V1 在結果中的加權量。</span><span class="sxs-lookup"><span data-stu-id="815bc-148">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="815bc-149">Barycentric 座標是一種一般座標形式。</span><span class="sxs-lookup"><span data-stu-id="815bc-149">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="815bc-150">在此內容中，使用 barycentric 座標代表座標系統中的變更。</span><span class="sxs-lookup"><span data-stu-id="815bc-150">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="815bc-151">笛卡兒座標的 true 是 barycentric 座標的 true。</span><span class="sxs-lookup"><span data-stu-id="815bc-151">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="815bc-152">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="815bc-152">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="815bc-153">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="815bc-153">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="815bc-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="815bc-154">Requirements</span></span>



| <span data-ttu-id="815bc-155">需求</span><span class="sxs-lookup"><span data-stu-id="815bc-155">Requirement</span></span> | <span data-ttu-id="815bc-156">值</span><span class="sxs-lookup"><span data-stu-id="815bc-156">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="815bc-157">標頭</span><span class="sxs-lookup"><span data-stu-id="815bc-157">Header</span></span><br/>  | <dl> <span data-ttu-id="815bc-158"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="815bc-158"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="815bc-159">程式庫</span><span class="sxs-lookup"><span data-stu-id="815bc-159">Library</span></span><br/> | <dl> <span data-ttu-id="815bc-160"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="815bc-160"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="815bc-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="815bc-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="815bc-162">網格函數</span><span class="sxs-lookup"><span data-stu-id="815bc-162">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
