---
description: 判斷光線是否與此網格交集。
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: ID3DX10Mesh::Intersect 方法 (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ceed03ab21debf61371da9e53b5150d2dc83e4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986517"
---
# <a name="id3dx10meshintersect-method"></a><span data-ttu-id="ccf1a-103">ID3DX10Mesh：： Intersect 方法</span><span class="sxs-lookup"><span data-stu-id="ccf1a-103">ID3DX10Mesh::Intersect method</span></span>

<span data-ttu-id="ccf1a-104">判斷光線是否與此網格交集。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-104">Determines if a ray intersects with this mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf1a-105">語法</span><span class="sxs-lookup"><span data-stu-id="ccf1a-105">Syntax</span></span>


```C++
HRESULT Intersect(
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



## <a name="parameters"></a><span data-ttu-id="ccf1a-106">參數</span><span class="sxs-lookup"><span data-stu-id="ccf1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccf1a-107">*pRayPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccf1a-107">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf1a-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ccf1a-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ccf1a-109">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，指定光線開始的時間點。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="ccf1a-110">*pRayDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccf1a-110">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf1a-111">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ccf1a-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ccf1a-112">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，指定光線的方向。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="ccf1a-113">*pHitCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccf1a-113">*pHitCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf1a-114">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ccf1a-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ccf1a-115">光線與網格交集的次數。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-115">The number of times the ray intersected with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ccf1a-116">*pFaceIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccf1a-116">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf1a-117">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ccf1a-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ccf1a-118">如果 pHit 為 **TRUE**，則為最接近光線原點之臉部的索引值指標。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-118">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="ccf1a-119">*pU* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccf1a-119">*pU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf1a-120">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="ccf1a-120">Type: **float\***</span></span>

<span data-ttu-id="ccf1a-121">Barycentric 點擊座標的指標，U。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-121">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="ccf1a-122">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccf1a-122">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf1a-123">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="ccf1a-123">Type: **float\***</span></span>

<span data-ttu-id="ccf1a-124">Barycentric 點擊座標的指標，V。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-124">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="ccf1a-125">*pDist* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ccf1a-125">*pDist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf1a-126">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="ccf1a-126">Type: **float\***</span></span>

<span data-ttu-id="ccf1a-127">光線交集參數距離的指標。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-127">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="ccf1a-128">*ppAllHits* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ccf1a-128">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccf1a-129">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="ccf1a-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="ccf1a-130">[**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)的指標，其中包含 [**D3DX10 \_ INTERSECT \_ 資訊**](d3dx10-intersect-info.md)結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-130">Pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), containing an array of [**D3DX10\_INTERSECT\_INFO**](d3dx10-intersect-info.md) structures.</span></span> <span data-ttu-id="ccf1a-131">這是交集測試中發生的所有點擊清單。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-131">This is a list of all the hits that occurred in the intersection test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccf1a-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="ccf1a-132">Return value</span></span>

<span data-ttu-id="ccf1a-133">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ccf1a-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ccf1a-134">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ccf1a-135">備註</span><span class="sxs-lookup"><span data-stu-id="ccf1a-135">Remarks</span></span>

<span data-ttu-id="ccf1a-136">此 API 提供一種方式來瞭解三角形中和周圍的點，與三角形實際所在的位置無關。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-136">This API provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="ccf1a-137">此函式會使用下列方程式傳回結果點： V1 + U (V2-V1) + V (V3-V1) 。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="ccf1a-138">平面 V1V2V3 中的任何點都可由 barycentric 座標 (U，V) 表示。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="ccf1a-139">參數 U 會控制要將多少 V2 加權至結果中，而參數 V 控制要將多少 V3 加權到結果中。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="ccf1a-140">最後， \[ 1 (U + V) 的值會 \] 控制 V1 在結果中的加權量。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="ccf1a-141">Barycentric 座標是一種一般座標形式。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="ccf1a-142">在此內容中，使用 barycentric 座標代表座標系統中的變更。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="ccf1a-143">笛卡兒座標的 true 是 barycentric 座標的 true。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="ccf1a-144">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="ccf1a-145">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="ccf1a-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf1a-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccf1a-146">Requirements</span></span>



| <span data-ttu-id="ccf1a-147">需求</span><span class="sxs-lookup"><span data-stu-id="ccf1a-147">Requirement</span></span> | <span data-ttu-id="ccf1a-148">值</span><span class="sxs-lookup"><span data-stu-id="ccf1a-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf1a-149">標頭</span><span class="sxs-lookup"><span data-stu-id="ccf1a-149">Header</span></span><br/>  | <dl> <span data-ttu-id="ccf1a-150"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="ccf1a-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccf1a-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="ccf1a-151">Library</span></span><br/> | <dl> <span data-ttu-id="ccf1a-152"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccf1a-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccf1a-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ccf1a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf1a-154">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ccf1a-154">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ccf1a-155">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="ccf1a-155">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
