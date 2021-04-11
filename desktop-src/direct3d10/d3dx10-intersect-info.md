---
description: 描述光線三角形交集。
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: 'D3DX10_INTERSECT_INFO 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_INTERSECT_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 87490e734299cba57952bb43d1ee4ffad8e014c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696687"
---
# <a name="d3dx10_intersect_info-structure"></a><span data-ttu-id="065b4-103">D3DX10 \_ INTERSECT \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="065b4-103">D3DX10\_INTERSECT\_INFO structure</span></span>

<span data-ttu-id="065b4-104">描述光線三角形交集。</span><span class="sxs-lookup"><span data-stu-id="065b4-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="065b4-105">語法</span><span class="sxs-lookup"><span data-stu-id="065b4-105">Syntax</span></span>


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a><span data-ttu-id="065b4-106">成員</span><span class="sxs-lookup"><span data-stu-id="065b4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="065b4-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="065b4-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="065b4-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="065b4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="065b4-109">命中光線的三角形索引。</span><span class="sxs-lookup"><span data-stu-id="065b4-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="065b4-110">**U**</span><span class="sxs-lookup"><span data-stu-id="065b4-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="065b4-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="065b4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="065b4-112">光線相交之三角形內的 Barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="065b4-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="065b4-113">**V**</span><span class="sxs-lookup"><span data-stu-id="065b4-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="065b4-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="065b4-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="065b4-115">光線相交之三角形內的 Barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="065b4-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="065b4-116">**Dist**</span><span class="sxs-lookup"><span data-stu-id="065b4-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="065b4-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="065b4-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="065b4-118">沿著光線發生交集的距離。</span><span class="sxs-lookup"><span data-stu-id="065b4-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="065b4-119">備註</span><span class="sxs-lookup"><span data-stu-id="065b4-119">Remarks</span></span>

<span data-ttu-id="065b4-120">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="065b4-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="065b4-121">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="065b4-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="065b4-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="065b4-122">Requirements</span></span>



| <span data-ttu-id="065b4-123">需求</span><span class="sxs-lookup"><span data-stu-id="065b4-123">Requirement</span></span> | <span data-ttu-id="065b4-124">值</span><span class="sxs-lookup"><span data-stu-id="065b4-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="065b4-125">標頭</span><span class="sxs-lookup"><span data-stu-id="065b4-125">Header</span></span><br/> | <dl> <span data-ttu-id="065b4-126"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="065b4-126"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="065b4-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="065b4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="065b4-128">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="065b4-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
