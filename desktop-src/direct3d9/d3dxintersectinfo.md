---
description: D3DXINTERSECTINFO 結構-描述光線三角形交集。
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: 'D3DXINTERSECTINFO 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINTERSECTINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: f4a63c7f4a479bfbe9dcb49f485ce0acb8db6486
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098286"
---
# <a name="d3dxintersectinfo-structure"></a><span data-ttu-id="8bfa1-103">D3DXINTERSECTINFO 結構</span><span class="sxs-lookup"><span data-stu-id="8bfa1-103">D3DXINTERSECTINFO structure</span></span>

<span data-ttu-id="8bfa1-104">描述光線三角形交集。</span><span class="sxs-lookup"><span data-stu-id="8bfa1-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bfa1-105">語法</span><span class="sxs-lookup"><span data-stu-id="8bfa1-105">Syntax</span></span>


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a><span data-ttu-id="8bfa1-106">成員</span><span class="sxs-lookup"><span data-stu-id="8bfa1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8bfa1-107">**FaceIndex**</span><span class="sxs-lookup"><span data-stu-id="8bfa1-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="8bfa1-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8bfa1-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8bfa1-109">命中光線的三角形索引。</span><span class="sxs-lookup"><span data-stu-id="8bfa1-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="8bfa1-110">**U**</span><span class="sxs-lookup"><span data-stu-id="8bfa1-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="8bfa1-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8bfa1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8bfa1-112">光線相交之三角形內的 Barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="8bfa1-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="8bfa1-113">**V**</span><span class="sxs-lookup"><span data-stu-id="8bfa1-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="8bfa1-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8bfa1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8bfa1-115">光線相交之三角形內的 Barycentric 座標。</span><span class="sxs-lookup"><span data-stu-id="8bfa1-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="8bfa1-116">**Dist**</span><span class="sxs-lookup"><span data-stu-id="8bfa1-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="8bfa1-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8bfa1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8bfa1-118">沿著光線發生交集的距離。</span><span class="sxs-lookup"><span data-stu-id="8bfa1-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8bfa1-119">備註</span><span class="sxs-lookup"><span data-stu-id="8bfa1-119">Remarks</span></span>

<span data-ttu-id="8bfa1-120">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="8bfa1-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="8bfa1-121">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="8bfa1-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bfa1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bfa1-122">Requirements</span></span>



| <span data-ttu-id="8bfa1-123">需求</span><span class="sxs-lookup"><span data-stu-id="8bfa1-123">Requirement</span></span> | <span data-ttu-id="8bfa1-124">值</span><span class="sxs-lookup"><span data-stu-id="8bfa1-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bfa1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8bfa1-125">Header</span></span><br/> | <dl> <span data-ttu-id="8bfa1-126"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="8bfa1-126"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bfa1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bfa1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bfa1-128">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="8bfa1-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
