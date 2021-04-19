---
description: 判斷光線是否與球體周框方塊的音量相交。
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: 'D3DXSphereBoundProbe 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbab8a49165a87f73037ae25230d67b02222fc15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986735"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a><span data-ttu-id="d3361-103">D3DXSphereBoundProbe 函式 (D3DX9Mesh) </span><span class="sxs-lookup"><span data-stu-id="d3361-103">D3DXSphereBoundProbe function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="d3361-104">判斷光線是否與球體周框方塊的音量相交。</span><span class="sxs-lookup"><span data-stu-id="d3361-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3361-105">語法</span><span class="sxs-lookup"><span data-stu-id="d3361-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="d3361-106">參數</span><span class="sxs-lookup"><span data-stu-id="d3361-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3361-107">*pCenter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3361-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3361-108">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d3361-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d3361-109">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定球體的中心座標。</span><span class="sxs-lookup"><span data-stu-id="d3361-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="d3361-110">*Radius* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3361-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3361-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3361-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3361-112">球體的半徑。</span><span class="sxs-lookup"><span data-stu-id="d3361-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="d3361-113">*pRayPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3361-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3361-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d3361-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d3361-115">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線的原點座標。</span><span class="sxs-lookup"><span data-stu-id="d3361-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="d3361-116">*pRayDirection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3361-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3361-117">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d3361-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d3361-118">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線的方向。</span><span class="sxs-lookup"><span data-stu-id="d3361-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="d3361-119">此向量不應該是 (0、0、0) 但不需要標準化。</span><span class="sxs-lookup"><span data-stu-id="d3361-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3361-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3361-120">Return value</span></span>

<span data-ttu-id="d3361-121">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3361-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3361-122">如果光線與球體周框方塊的音量相交，則會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="d3361-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="d3361-123">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d3361-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3361-124">備註</span><span class="sxs-lookup"><span data-stu-id="d3361-124">Remarks</span></span>

<span data-ttu-id="d3361-125">**D3DXSphereBoundProbe** 會決定光線是否與球體周框方塊的音量相交，而不只是球體的表面。</span><span class="sxs-lookup"><span data-stu-id="d3361-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3361-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3361-126">Requirements</span></span>



| <span data-ttu-id="d3361-127">需求</span><span class="sxs-lookup"><span data-stu-id="d3361-127">Requirement</span></span> | <span data-ttu-id="d3361-128">值</span><span class="sxs-lookup"><span data-stu-id="d3361-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3361-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d3361-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d3361-130"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3361-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d3361-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3361-131">Library</span></span><br/> | <dl> <span data-ttu-id="d3361-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3361-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3361-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3361-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3361-134">網格函數</span><span class="sxs-lookup"><span data-stu-id="d3361-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
