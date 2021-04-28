---
description: D3DXWELDEPSILONS 結構-在比較頂點時，指定每個頂點元件的容錯值，以判斷它們是否類似于一起進行焊接。
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: 'D3DXWELDEPSILONS 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWELDEPSILONS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: bb11e6f5481b1adf7cc1bac58edf40d4ac770e92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115496"
---
# <a name="d3dxweldepsilons-structure"></a><span data-ttu-id="6c552-103">D3DXWELDEPSILONS 結構</span><span class="sxs-lookup"><span data-stu-id="6c552-103">D3DXWELDEPSILONS structure</span></span>

<span data-ttu-id="6c552-104">在比較頂點時，指定每個頂點元件的容錯值，以判斷它們是否類似于一起進行焊接。</span><span class="sxs-lookup"><span data-stu-id="6c552-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c552-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c552-105">Syntax</span></span>


```C++
typedef struct _D3DXWELDEPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DXWELDEPSILONS, *LPD3DXWELDEPSILONS;
```



## <a name="members"></a><span data-ttu-id="6c552-106">成員</span><span class="sxs-lookup"><span data-stu-id="6c552-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6c552-107">**位置**</span><span class="sxs-lookup"><span data-stu-id="6c552-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="6c552-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c552-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c552-109">位置</span><span class="sxs-lookup"><span data-stu-id="6c552-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="6c552-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="6c552-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="6c552-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c552-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c552-112">Blend 權數</span><span class="sxs-lookup"><span data-stu-id="6c552-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="6c552-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="6c552-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="6c552-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c552-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c552-115">正常</span><span class="sxs-lookup"><span data-stu-id="6c552-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="6c552-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="6c552-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="6c552-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c552-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c552-118">點大小值</span><span class="sxs-lookup"><span data-stu-id="6c552-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="6c552-119">**反射**</span><span class="sxs-lookup"><span data-stu-id="6c552-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="6c552-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c552-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c552-121">反射光源值</span><span class="sxs-lookup"><span data-stu-id="6c552-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="6c552-122">**擴散**</span><span class="sxs-lookup"><span data-stu-id="6c552-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="6c552-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c552-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c552-124">擴散光源值</span><span class="sxs-lookup"><span data-stu-id="6c552-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="6c552-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="6c552-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="6c552-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c552-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c552-127">八個材質座標</span><span class="sxs-lookup"><span data-stu-id="6c552-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="6c552-128">**正切值**</span><span class="sxs-lookup"><span data-stu-id="6c552-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="6c552-129">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c552-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c552-130">正切值</span><span class="sxs-lookup"><span data-stu-id="6c552-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="6c552-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="6c552-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="6c552-132">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c552-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c552-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="6c552-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="6c552-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="6c552-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="6c552-135">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c552-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6c552-136">鑲嵌因數</span><span class="sxs-lookup"><span data-stu-id="6c552-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c552-137">備註</span><span class="sxs-lookup"><span data-stu-id="6c552-137">Remarks</span></span>

<span data-ttu-id="6c552-138">LPD3DXWELDEPSILONS 型別定義為 **D3DXWELDEPSILONS** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6c552-138">The LPD3DXWELDEPSILONS type is defined as a pointer to the **D3DXWELDEPSILONS** structure.</span></span>


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="6c552-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c552-139">Requirements</span></span>



| <span data-ttu-id="6c552-140">需求</span><span class="sxs-lookup"><span data-stu-id="6c552-140">Requirement</span></span> | <span data-ttu-id="6c552-141">值</span><span class="sxs-lookup"><span data-stu-id="6c552-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c552-142">標頭</span><span class="sxs-lookup"><span data-stu-id="6c552-142">Header</span></span><br/> | <dl> <span data-ttu-id="6c552-143"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c552-143"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c552-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c552-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c552-145">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="6c552-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="6c552-146">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="6c552-146">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 
