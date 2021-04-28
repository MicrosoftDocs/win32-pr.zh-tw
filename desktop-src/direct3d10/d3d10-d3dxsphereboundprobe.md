---
description: D3DXSphereBoundProbe 函式 (D3DX10math) -決定光線是否與球體周框方塊的音量相交。
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: 'D3DXSphereBoundProbe 函式 (D3DX10math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fb5a329e39631dff626ff1c7945ad4b05f9dcd58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108466"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a><span data-ttu-id="3bd55-103">D3DXSphereBoundProbe 函式 (D3DX10math) </span><span class="sxs-lookup"><span data-stu-id="3bd55-103">D3DXSphereBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="3bd55-104">判斷光線是否與球體周框方塊的音量相交。</span><span class="sxs-lookup"><span data-stu-id="3bd55-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd55-105">語法</span><span class="sxs-lookup"><span data-stu-id="3bd55-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="3bd55-106">參數</span><span class="sxs-lookup"><span data-stu-id="3bd55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bd55-107">*pCenter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3bd55-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd55-108">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3bd55-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3bd55-109">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，指定球體的中心座標。</span><span class="sxs-lookup"><span data-stu-id="3bd55-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="3bd55-110">*Radius* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3bd55-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd55-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bd55-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3bd55-112">球體的半徑。</span><span class="sxs-lookup"><span data-stu-id="3bd55-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="3bd55-113">*pRayPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3bd55-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd55-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3bd55-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3bd55-115">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，指定光線的原點座標。</span><span class="sxs-lookup"><span data-stu-id="3bd55-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="3bd55-116">*pRayDirection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3bd55-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd55-117">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3bd55-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="3bd55-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，指定光線的方向。</span><span class="sxs-lookup"><span data-stu-id="3bd55-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="3bd55-119">此向量不應該是 (0、0、0) 但不需要標準化。</span><span class="sxs-lookup"><span data-stu-id="3bd55-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bd55-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bd55-120">Return value</span></span>

<span data-ttu-id="3bd55-121">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bd55-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3bd55-122">如果光線與球體周框方塊的音量相交，則會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="3bd55-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="3bd55-123">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3bd55-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bd55-124">備註</span><span class="sxs-lookup"><span data-stu-id="3bd55-124">Remarks</span></span>

<span data-ttu-id="3bd55-125">**D3DXSphereBoundProbe** 會決定光線是否與球體周框方塊的音量相交，而不只是球體的表面。</span><span class="sxs-lookup"><span data-stu-id="3bd55-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bd55-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bd55-126">Requirements</span></span>



| <span data-ttu-id="3bd55-127">需求</span><span class="sxs-lookup"><span data-stu-id="3bd55-127">Requirement</span></span> | <span data-ttu-id="3bd55-128">值</span><span class="sxs-lookup"><span data-stu-id="3bd55-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd55-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3bd55-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3bd55-130"><dt>D3DX10math。h</dt></span><span class="sxs-lookup"><span data-stu-id="3bd55-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="3bd55-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="3bd55-131">Library</span></span><br/> | <dl> <span data-ttu-id="3bd55-132"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bd55-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3bd55-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bd55-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd55-134">網格函數</span><span class="sxs-lookup"><span data-stu-id="3bd55-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
