---
description: 指定網狀加權屬性。
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: 'D3DXATTRIBUTEWEIGHTS 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 49725e410fb700c7ecb93fd56a8db367d7f982a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000363"
---
# <a name="d3dxattributeweights-structure"></a><span data-ttu-id="ac83a-103">D3DXATTRIBUTEWEIGHTS 結構</span><span class="sxs-lookup"><span data-stu-id="ac83a-103">D3DXATTRIBUTEWEIGHTS structure</span></span>

<span data-ttu-id="ac83a-104">指定網狀加權屬性。</span><span class="sxs-lookup"><span data-stu-id="ac83a-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac83a-105">語法</span><span class="sxs-lookup"><span data-stu-id="ac83a-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="members"></a><span data-ttu-id="ac83a-106">成員</span><span class="sxs-lookup"><span data-stu-id="ac83a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ac83a-107">**位置**</span><span class="sxs-lookup"><span data-stu-id="ac83a-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="ac83a-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac83a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac83a-109">位置。</span><span class="sxs-lookup"><span data-stu-id="ac83a-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="ac83a-110">**界限**</span><span class="sxs-lookup"><span data-stu-id="ac83a-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="ac83a-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac83a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac83a-112">Blend 權數。</span><span class="sxs-lookup"><span data-stu-id="ac83a-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="ac83a-113">**Normal**</span><span class="sxs-lookup"><span data-stu-id="ac83a-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="ac83a-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac83a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac83a-115">一般。</span><span class="sxs-lookup"><span data-stu-id="ac83a-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="ac83a-116">**擴散**</span><span class="sxs-lookup"><span data-stu-id="ac83a-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="ac83a-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac83a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac83a-118">擴散光源值。</span><span class="sxs-lookup"><span data-stu-id="ac83a-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="ac83a-119">**反射**</span><span class="sxs-lookup"><span data-stu-id="ac83a-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="ac83a-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac83a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac83a-121">反射光源值。</span><span class="sxs-lookup"><span data-stu-id="ac83a-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="ac83a-122">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="ac83a-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="ac83a-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac83a-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac83a-124">八個材質座標。</span><span class="sxs-lookup"><span data-stu-id="ac83a-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="ac83a-125">**正切值**</span><span class="sxs-lookup"><span data-stu-id="ac83a-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="ac83a-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac83a-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac83a-127">切線。</span><span class="sxs-lookup"><span data-stu-id="ac83a-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="ac83a-128">**Binormal**</span><span class="sxs-lookup"><span data-stu-id="ac83a-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="ac83a-129">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac83a-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac83a-130">Binormal.</span><span class="sxs-lookup"><span data-stu-id="ac83a-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac83a-131">備註</span><span class="sxs-lookup"><span data-stu-id="ac83a-131">Remarks</span></span>

<span data-ttu-id="ac83a-132">此結構描述當您計算折迭邊緣之間的相對成本時，簡化作業將如何考慮頂點資料。</span><span class="sxs-lookup"><span data-stu-id="ac83a-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="ac83a-133">例如，如果一般欄位為0.0，則在計算折迭的錯誤時，簡化作業將會忽略頂點一般元件。</span><span class="sxs-lookup"><span data-stu-id="ac83a-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="ac83a-134">但是，如果一般欄位是1.0，簡化作業將會使用頂點一般元件。</span><span class="sxs-lookup"><span data-stu-id="ac83a-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="ac83a-135">如果正常欄位是2.0，請將錯誤的數量加倍;如果正常欄位是4.0，則會有四個錯誤數目，依此類推。</span><span class="sxs-lookup"><span data-stu-id="ac83a-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="ac83a-136">LPD3DXATTRIBUTEWEIGHTS 型別定義為 **D3DXATTRIBUTEWEIGHTS** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ac83a-136">The LPD3DXATTRIBUTEWEIGHTS type is defined as a pointer to the **D3DXATTRIBUTEWEIGHTS** structure.</span></span>


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="ac83a-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac83a-137">Requirements</span></span>



| <span data-ttu-id="ac83a-138">需求</span><span class="sxs-lookup"><span data-stu-id="ac83a-138">Requirement</span></span> | <span data-ttu-id="ac83a-139">值</span><span class="sxs-lookup"><span data-stu-id="ac83a-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac83a-140">標頭</span><span class="sxs-lookup"><span data-stu-id="ac83a-140">Header</span></span><br/> | <dl> <span data-ttu-id="ac83a-141"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac83a-141"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac83a-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac83a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac83a-143">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="ac83a-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="ac83a-144">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="ac83a-144">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 
