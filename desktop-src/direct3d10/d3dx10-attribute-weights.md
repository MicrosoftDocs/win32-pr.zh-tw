---
description: 指定網狀加權屬性。
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: 'D3DX10_ATTRIBUTE_WEIGHTS 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 4f137c1ecc29c184c4dec3995fb0202741ce9f09
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323020"
---
# <a name="d3dx10_attribute_weights-structure"></a><span data-ttu-id="6b363-103">D3DX10 \_ 屬性 \_ 加權結構</span><span class="sxs-lookup"><span data-stu-id="6b363-103">D3DX10\_ATTRIBUTE\_WEIGHTS structure</span></span>

<span data-ttu-id="6b363-104">指定網狀加權屬性。</span><span class="sxs-lookup"><span data-stu-id="6b363-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b363-105">語法</span><span class="sxs-lookup"><span data-stu-id="6b363-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
```



## <a name="members"></a><span data-ttu-id="6b363-106">成員</span><span class="sxs-lookup"><span data-stu-id="6b363-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6b363-107">**位置**</span><span class="sxs-lookup"><span data-stu-id="6b363-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="6b363-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b363-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b363-109">位置。</span><span class="sxs-lookup"><span data-stu-id="6b363-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="6b363-110">**界限**</span><span class="sxs-lookup"><span data-stu-id="6b363-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="6b363-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b363-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b363-112">Blend 權數。</span><span class="sxs-lookup"><span data-stu-id="6b363-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="6b363-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="6b363-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="6b363-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b363-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b363-115">一般。</span><span class="sxs-lookup"><span data-stu-id="6b363-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="6b363-116">**擴散**</span><span class="sxs-lookup"><span data-stu-id="6b363-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="6b363-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b363-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b363-118">擴散光源值。</span><span class="sxs-lookup"><span data-stu-id="6b363-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="6b363-119">**反射**</span><span class="sxs-lookup"><span data-stu-id="6b363-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="6b363-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b363-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b363-121">反射光源值。</span><span class="sxs-lookup"><span data-stu-id="6b363-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="6b363-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="6b363-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="6b363-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b363-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b363-124">八個材質座標。</span><span class="sxs-lookup"><span data-stu-id="6b363-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="6b363-125">**正切值**</span><span class="sxs-lookup"><span data-stu-id="6b363-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="6b363-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b363-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b363-127">切線。</span><span class="sxs-lookup"><span data-stu-id="6b363-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="6b363-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="6b363-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="6b363-129">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b363-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6b363-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="6b363-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b363-131">備註</span><span class="sxs-lookup"><span data-stu-id="6b363-131">Remarks</span></span>

<span data-ttu-id="6b363-132">此結構描述當您計算折迭邊緣之間的相對成本時，簡化作業將如何考慮頂點資料。</span><span class="sxs-lookup"><span data-stu-id="6b363-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="6b363-133">例如，如果一般欄位為0.0，則在計算折迭的錯誤時，簡化作業將會忽略頂點一般元件。</span><span class="sxs-lookup"><span data-stu-id="6b363-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="6b363-134">但是，如果一般欄位是1.0，簡化作業將會使用頂點一般元件。</span><span class="sxs-lookup"><span data-stu-id="6b363-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="6b363-135">如果正常欄位是2.0，請將錯誤的數量加倍;如果正常欄位是4.0，則會有四個錯誤數目，依此類推。</span><span class="sxs-lookup"><span data-stu-id="6b363-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="6b363-136">LPD3DX \_ 屬性權數 \_ 型別定義為 D3DX 屬性權數結構的指標 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="6b363-136">The LPD3DX\_ATTRIBUTE\_WEIGHTS type is defined as a pointer to the D3DX\_ATTRIBUTE\_WEIGHTS structure.</span></span>


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="6b363-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b363-137">Requirements</span></span>



| <span data-ttu-id="6b363-138">需求</span><span class="sxs-lookup"><span data-stu-id="6b363-138">Requirement</span></span> | <span data-ttu-id="6b363-139">值</span><span class="sxs-lookup"><span data-stu-id="6b363-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6b363-140">標頭</span><span class="sxs-lookup"><span data-stu-id="6b363-140">Header</span></span><br/> | <dl> <span data-ttu-id="6b363-141"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b363-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b363-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b363-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b363-143">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="6b363-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
