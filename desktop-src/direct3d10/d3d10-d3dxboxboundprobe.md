---
description: D3DXBoxBoundProbe 函式 (D3DX10math) 決定光線是否與方塊周框方塊的音量相交。
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: 'D3DXBoxBoundProbe 函式 (D3DX10math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106978550"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a><span data-ttu-id="c12df-103">D3DXBoxBoundProbe 函式 (D3DX10math) </span><span class="sxs-lookup"><span data-stu-id="c12df-103">D3DXBoxBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="c12df-104">判斷光線是否與方塊周框方塊的音量相交。</span><span class="sxs-lookup"><span data-stu-id="c12df-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="c12df-105">語法</span><span class="sxs-lookup"><span data-stu-id="c12df-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="c12df-106">參數</span><span class="sxs-lookup"><span data-stu-id="c12df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c12df-107">*pMin* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c12df-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c12df-108">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c12df-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c12df-109">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)的指標，描述周框方塊的左下角。</span><span class="sxs-lookup"><span data-stu-id="c12df-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="c12df-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="c12df-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c12df-111">*pMax* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c12df-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c12df-112">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c12df-112">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c12df-113">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，描述周框方塊的右上角。</span><span class="sxs-lookup"><span data-stu-id="c12df-113">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="c12df-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="c12df-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c12df-115">*pRayPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c12df-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c12df-116">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c12df-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c12df-117">D3DXVECTOR3 結構的指標，指定光線的原點座標。</span><span class="sxs-lookup"><span data-stu-id="c12df-117">Pointer to a D3DXVECTOR3 structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="c12df-118">*pRayDirection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c12df-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c12df-119">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c12df-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c12df-120">D3DXVECTOR3 結構的指標，指定光線的方向。</span><span class="sxs-lookup"><span data-stu-id="c12df-120">Pointer to a D3DXVECTOR3 structure, specifying the direction of the ray.</span></span> <span data-ttu-id="c12df-121">此向量不應該是 (0、0、0) 但不需要標準化。</span><span class="sxs-lookup"><span data-stu-id="c12df-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c12df-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="c12df-122">Return value</span></span>

<span data-ttu-id="c12df-123">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c12df-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c12df-124">如果光線與方塊周框方塊的音量相交，則會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="c12df-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="c12df-125">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c12df-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c12df-126">備註</span><span class="sxs-lookup"><span data-stu-id="c12df-126">Remarks</span></span>

<span data-ttu-id="c12df-127">**D3DXBoxBoundProbe** 會決定光線是否與方塊周框方塊的音量相交，而不只是方塊的表面。</span><span class="sxs-lookup"><span data-stu-id="c12df-127">**D3DXBoxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="c12df-128">傳遞至 **D3DXBoxBoundProbe** 的值為 xmin、xmax、ymin、ymax、zmin 和 zmax。</span><span class="sxs-lookup"><span data-stu-id="c12df-128">The values passed to **D3DXBoxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="c12df-129">因此，下列定義周框方塊的角落。</span><span class="sxs-lookup"><span data-stu-id="c12df-129">Thus, the following defines the corners of the bounding box.</span></span>


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



<span data-ttu-id="c12df-130">Z 方向中的周框方塊深度為 zmax-zmin，y 方向為 ymax ymin，而 x 方向為 xmax-xmin。</span><span class="sxs-lookup"><span data-stu-id="c12df-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="c12df-131">例如，使用下列最小和最大向量、min (-1、-1、-1) 和 max (1，1，1) ，則會以下列方式定義周框方塊。</span><span class="sxs-lookup"><span data-stu-id="c12df-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a><span data-ttu-id="c12df-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="c12df-132">Requirements</span></span>



| <span data-ttu-id="c12df-133">需求</span><span class="sxs-lookup"><span data-stu-id="c12df-133">Requirement</span></span> | <span data-ttu-id="c12df-134">值</span><span class="sxs-lookup"><span data-stu-id="c12df-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c12df-135">標頭</span><span class="sxs-lookup"><span data-stu-id="c12df-135">Header</span></span>  | <span data-ttu-id="c12df-136">D3DX10math。h</span><span class="sxs-lookup"><span data-stu-id="c12df-136">D3DX10math.h</span></span> |
| <span data-ttu-id="c12df-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="c12df-137">Library</span></span> | <span data-ttu-id="c12df-138">D3DX10 .lib</span><span class="sxs-lookup"><span data-stu-id="c12df-138">D3DX10.lib</span></span>  |



## <a name="see-also"></a><span data-ttu-id="c12df-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c12df-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c12df-140">網格函數</span><span class="sxs-lookup"><span data-stu-id="c12df-140">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
