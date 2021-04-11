---
description: 在預先計算 radiance 傳輸中使用有效率的光線追蹤 (PRT) 模擬，以判斷光線是否與網格相交。 通常用來判斷指定的點是否在陰影中。
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'ID3DXPRTEngine：： ShadowRayIntersects 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 701aa4c89ee6a9d657721d872565c9b2056bb435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035373"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a><span data-ttu-id="9f961-104">ID3DXPRTEngine：： ShadowRayIntersects 方法</span><span class="sxs-lookup"><span data-stu-id="9f961-104">ID3DXPRTEngine::ShadowRayIntersects method</span></span>

<span data-ttu-id="9f961-105">在預先計算 radiance 傳輸中使用有效率的光線追蹤 (PRT) 模擬，以判斷光線是否與網格相交。</span><span class="sxs-lookup"><span data-stu-id="9f961-105">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="9f961-106">通常用來判斷指定的點是否在陰影中。</span><span class="sxs-lookup"><span data-stu-id="9f961-106">Typically used to determine whether a given point is in shadow.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f961-107">語法</span><span class="sxs-lookup"><span data-stu-id="9f961-107">Syntax</span></span>


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a><span data-ttu-id="9f961-108">參數</span><span class="sxs-lookup"><span data-stu-id="9f961-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f961-109">*pRayPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f961-109">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f961-110">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f961-110">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9f961-111">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線開始的時間點。</span><span class="sxs-lookup"><span data-stu-id="9f961-111">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="9f961-112">*pRayDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f961-112">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f961-113">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f961-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9f961-114">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線的正規化方向。</span><span class="sxs-lookup"><span data-stu-id="9f961-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f961-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f961-115">Return value</span></span>

<span data-ttu-id="9f961-116">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f961-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f961-117">如果光線與目前的網格相交，則傳回 **TRUE** ;否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9f961-117">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f961-118">備註</span><span class="sxs-lookup"><span data-stu-id="9f961-118">Remarks</span></span>

<span data-ttu-id="9f961-119">使用 [**ID3DXPRTEngine：： SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) 來設定與光線相交的最小和最大距離。</span><span class="sxs-lookup"><span data-stu-id="9f961-119">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="9f961-120">這個方法的執行速度比 [**ID3DXPRTEngine：： ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)更快。</span><span class="sxs-lookup"><span data-stu-id="9f961-120">This method executes faster than [**ID3DXPRTEngine::ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f961-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f961-121">Requirements</span></span>



| <span data-ttu-id="9f961-122">需求</span><span class="sxs-lookup"><span data-stu-id="9f961-122">Requirement</span></span> | <span data-ttu-id="9f961-123">值</span><span class="sxs-lookup"><span data-stu-id="9f961-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f961-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9f961-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9f961-125"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f961-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9f961-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="9f961-126">Library</span></span><br/> | <dl> <span data-ttu-id="9f961-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f961-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9f961-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f961-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f961-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="9f961-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="9f961-130">**ID3DXPRTEngine::ClosestRayIntersects**</span><span class="sxs-lookup"><span data-stu-id="9f961-130">**ID3DXPRTEngine::ClosestRayIntersects**</span></span>](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[<span data-ttu-id="9f961-131">**ID3DXPRTEngine::SetMinMaxIntersection**</span><span class="sxs-lookup"><span data-stu-id="9f961-131">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
