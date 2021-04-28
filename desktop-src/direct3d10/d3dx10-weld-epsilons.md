---
description: D3DX10_WELD_EPSILONS 結構-在比較頂點時，指定每個頂點元件的容錯值，以判斷它們是否類似于彼此的關聯。
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: 'D3DX10_WELD_EPSILONS 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_WELD_EPSILONS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 720a10dbe4b22b69910d88d3c03cea9ded768f1b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105426"
---
# <a name="d3dx10_weld_epsilons-structure"></a><span data-ttu-id="55c37-103">D3DX10 \_ 焊縫 \_ EPSILONS 結構</span><span class="sxs-lookup"><span data-stu-id="55c37-103">D3DX10\_WELD\_EPSILONS structure</span></span>

<span data-ttu-id="55c37-104">在比較頂點時，指定每個頂點元件的容錯值，以判斷它們是否類似于一起進行焊接。</span><span class="sxs-lookup"><span data-stu-id="55c37-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="55c37-105">語法</span><span class="sxs-lookup"><span data-stu-id="55c37-105">Syntax</span></span>


```C++
typedef struct D3DX10_WELD_EPSILONS {
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
} D3DX10_WELD_EPSILONS, *LPD3DX10_WELD_EPSILONS;
```



## <a name="members"></a><span data-ttu-id="55c37-106">成員</span><span class="sxs-lookup"><span data-stu-id="55c37-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="55c37-107">**位置**</span><span class="sxs-lookup"><span data-stu-id="55c37-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="55c37-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55c37-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="55c37-109">位置</span><span class="sxs-lookup"><span data-stu-id="55c37-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="55c37-110">**BlendWeights**</span><span class="sxs-lookup"><span data-stu-id="55c37-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="55c37-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55c37-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="55c37-112">Blend 權數</span><span class="sxs-lookup"><span data-stu-id="55c37-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="55c37-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="55c37-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="55c37-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55c37-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="55c37-115">正常</span><span class="sxs-lookup"><span data-stu-id="55c37-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="55c37-116">**PSize**</span><span class="sxs-lookup"><span data-stu-id="55c37-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="55c37-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55c37-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="55c37-118">點大小值</span><span class="sxs-lookup"><span data-stu-id="55c37-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="55c37-119">**反射**</span><span class="sxs-lookup"><span data-stu-id="55c37-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="55c37-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55c37-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="55c37-121">反射光源值</span><span class="sxs-lookup"><span data-stu-id="55c37-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="55c37-122">**擴散**</span><span class="sxs-lookup"><span data-stu-id="55c37-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="55c37-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55c37-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="55c37-124">擴散光源值</span><span class="sxs-lookup"><span data-stu-id="55c37-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="55c37-125">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="55c37-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="55c37-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55c37-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="55c37-127">八個材質座標</span><span class="sxs-lookup"><span data-stu-id="55c37-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="55c37-128">**正切值**</span><span class="sxs-lookup"><span data-stu-id="55c37-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="55c37-129">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55c37-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="55c37-130">正切值</span><span class="sxs-lookup"><span data-stu-id="55c37-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="55c37-131">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="55c37-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="55c37-132">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55c37-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="55c37-133">Binormal</span><span class="sxs-lookup"><span data-stu-id="55c37-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="55c37-134">**TessFactor**</span><span class="sxs-lookup"><span data-stu-id="55c37-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="55c37-135">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55c37-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="55c37-136">鑲嵌因數</span><span class="sxs-lookup"><span data-stu-id="55c37-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55c37-137">備註</span><span class="sxs-lookup"><span data-stu-id="55c37-137">Remarks</span></span>

<span data-ttu-id="55c37-138">LPD3DXWeldEpsilons 型別定義為 D3DXWeldEpsilons 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="55c37-138">The LPD3DXWeldEpsilons type is defined as a pointer to the D3DXWeldEpsilons structure.</span></span>


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="55c37-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="55c37-139">Requirements</span></span>



| <span data-ttu-id="55c37-140">需求</span><span class="sxs-lookup"><span data-stu-id="55c37-140">Requirement</span></span> | <span data-ttu-id="55c37-141">值</span><span class="sxs-lookup"><span data-stu-id="55c37-141">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="55c37-142">標頭</span><span class="sxs-lookup"><span data-stu-id="55c37-142">Header</span></span><br/> | <dl> <span data-ttu-id="55c37-143"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="55c37-143"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55c37-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55c37-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c37-145">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="55c37-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
