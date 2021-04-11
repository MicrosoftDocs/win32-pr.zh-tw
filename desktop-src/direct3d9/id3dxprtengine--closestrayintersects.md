---
description: 在預先計算 radiance 傳輸中使用有效率的光線追蹤 (PRT) 模擬，以判斷光線是否與網格相交。
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'ID3DXPRTEngine：： ClosestRayIntersects 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4fd802f636077c9ec2a9f0f1060ffd43493aabf1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196417"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a><span data-ttu-id="f67cd-103">ID3DXPRTEngine：： ClosestRayIntersects 方法</span><span class="sxs-lookup"><span data-stu-id="f67cd-103">ID3DXPRTEngine::ClosestRayIntersects method</span></span>

<span data-ttu-id="f67cd-104">在預先計算 radiance 傳輸中使用有效率的光線追蹤 (PRT) 模擬，以判斷光線是否與網格相交。</span><span class="sxs-lookup"><span data-stu-id="f67cd-104">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="f67cd-105">如果找到交集，方法會傳回最接近之網格臉部的索引，以及交集點的 barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="f67cd-105">If an intersection is found, the method returns the index of the closest mesh face hit by the ray and the barycentric coordinates of the intersection point.</span></span>

## <a name="syntax"></a><span data-ttu-id="f67cd-106">語法</span><span class="sxs-lookup"><span data-stu-id="f67cd-106">Syntax</span></span>


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="f67cd-107">參數</span><span class="sxs-lookup"><span data-stu-id="f67cd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f67cd-108">*pRayPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f67cd-108">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f67cd-109">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f67cd-109">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f67cd-110">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線開始的時間點。</span><span class="sxs-lookup"><span data-stu-id="f67cd-110">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="f67cd-111">*pRayDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f67cd-111">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f67cd-112">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f67cd-112">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f67cd-113">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線的正規化方向。</span><span class="sxs-lookup"><span data-stu-id="f67cd-113">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="f67cd-114">*pFaceIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f67cd-114">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f67cd-115">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f67cd-115">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f67cd-116">目前網格臉部的索引指標，該指標是由指定光線第一個叫用的，根據目前網格前方的所有封鎖程式網格臉部堆疊。</span><span class="sxs-lookup"><span data-stu-id="f67cd-116">Pointer to the index of the current mesh face that is first hit by the given ray, based upon stacking all blocker mesh faces in front of the current mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f67cd-117">*pU* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f67cd-117">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f67cd-118">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f67cd-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f67cd-119">指標，指向三角形的頂點 0 barycentric 點擊座標 U。</span><span class="sxs-lookup"><span data-stu-id="f67cd-119">Pointer to a barycentric hit coordinate, U, for vertex 0 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="f67cd-120">*pV* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f67cd-120">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f67cd-121">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f67cd-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f67cd-122">指標，指向三角形的頂點1的 barycentric 點擊座標（V）。</span><span class="sxs-lookup"><span data-stu-id="f67cd-122">Pointer to a barycentric hit coordinate, V, for vertex 1 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="f67cd-123">*pDist* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f67cd-123">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f67cd-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f67cd-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f67cd-125">沿著光線相交點距離的指標。</span><span class="sxs-lookup"><span data-stu-id="f67cd-125">Pointer to the distance of the intersection point along the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f67cd-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="f67cd-126">Return value</span></span>

<span data-ttu-id="f67cd-127">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f67cd-127">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f67cd-128">如果光線與目前的網格相交，則傳回 **TRUE** ;否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f67cd-128">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f67cd-129">備註</span><span class="sxs-lookup"><span data-stu-id="f67cd-129">Remarks</span></span>

<span data-ttu-id="f67cd-130">使用 [**ID3DXPRTEngine：： SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) 來設定與光線相交的最小和最大距離。</span><span class="sxs-lookup"><span data-stu-id="f67cd-130">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="f67cd-131">三角形的第三個頂點 (頂點 2) 的 barycentric 座標是 1 ( U + V ) 。</span><span class="sxs-lookup"><span data-stu-id="f67cd-131">The barycentric coordinate of the third vertex (vertex 2) of the triangle is 1 - ( U + V ).</span></span>

<span data-ttu-id="f67cd-132">這個方法的執行速度比 [**ID3DXPRTEngine：： ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)慢。</span><span class="sxs-lookup"><span data-stu-id="f67cd-132">This method executes slower than [**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md).</span></span> <span data-ttu-id="f67cd-133">如果不需要交集點的位置，請使用 **ID3DXPRTEngine：： ShadowRayIntersects** 。</span><span class="sxs-lookup"><span data-stu-id="f67cd-133">Use **ID3DXPRTEngine::ShadowRayIntersects** if the location of the intersection point is not needed.</span></span>

<span data-ttu-id="f67cd-134">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="f67cd-134">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="f67cd-135">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="f67cd-135">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="f67cd-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="f67cd-136">Requirements</span></span>



| <span data-ttu-id="f67cd-137">需求</span><span class="sxs-lookup"><span data-stu-id="f67cd-137">Requirement</span></span> | <span data-ttu-id="f67cd-138">值</span><span class="sxs-lookup"><span data-stu-id="f67cd-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f67cd-139">標頭</span><span class="sxs-lookup"><span data-stu-id="f67cd-139">Header</span></span><br/>  | <dl> <span data-ttu-id="f67cd-140"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="f67cd-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f67cd-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="f67cd-141">Library</span></span><br/> | <dl> <span data-ttu-id="f67cd-142"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f67cd-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f67cd-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f67cd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f67cd-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="f67cd-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="f67cd-145">**ID3DXPRTEngine::ShadowRayIntersects**</span><span class="sxs-lookup"><span data-stu-id="f67cd-145">**ID3DXPRTEngine::ShadowRayIntersects**</span></span>](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[<span data-ttu-id="f67cd-146">**ID3DXPRTEngine::SetMinMaxIntersection**</span><span class="sxs-lookup"><span data-stu-id="f67cd-146">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
