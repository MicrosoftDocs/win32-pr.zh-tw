---
title: Texture2DArray：：搜集 (S、float、int) 函數
description: 傳回要在雙線性篩選作業中使用的四個材質值。 |Texture2DArray：：搜集 (S、float、int) 函數
ms.assetid: b0355158-01c8-45a1-bb5d-29a8c43b1685
keywords:
- 收集函數 HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46866df18a0836b311443a3dd411d74dfa7fb126
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991887"
---
# <a name="texture2darraygathersfloatint-function"></a><span data-ttu-id="b261b-105">Texture2DArray：：搜集 (S、float、int) 函數</span><span class="sxs-lookup"><span data-stu-id="b261b-105">Texture2DArray::Gather(S,float,int) function</span></span>

<span data-ttu-id="b261b-106">傳回要在雙線性篩選作業中使用的四個材質值。</span><span class="sxs-lookup"><span data-stu-id="b261b-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b261b-107">語法</span><span class="sxs-lookup"><span data-stu-id="b261b-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="b261b-108">參數</span><span class="sxs-lookup"><span data-stu-id="b261b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b261b-109"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="b261b-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b261b-110">類型：**取樣** 器</span><span class="sxs-lookup"><span data-stu-id="b261b-110">Type: **sampler**</span></span>

<span data-ttu-id="b261b-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="b261b-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="b261b-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b261b-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b261b-113">類型： **float3**</span><span class="sxs-lookup"><span data-stu-id="b261b-113">Type: **float3**</span></span>

<span data-ttu-id="b261b-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="b261b-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="b261b-115">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b261b-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b261b-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="b261b-116">Type: **int2**</span></span>

<span data-ttu-id="b261b-117">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="b261b-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b261b-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b261b-118">Return value</span></span>

<span data-ttu-id="b261b-119">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="b261b-119">Type: **TemplateType**</span></span>

<span data-ttu-id="b261b-120">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="b261b-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b261b-121">備註</span><span class="sxs-lookup"><span data-stu-id="b261b-121">Remarks</span></span>

<span data-ttu-id="b261b-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="b261b-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b261b-123">頂點</span><span class="sxs-lookup"><span data-stu-id="b261b-123">Vertex</span></span> | <span data-ttu-id="b261b-124">船體</span><span class="sxs-lookup"><span data-stu-id="b261b-124">Hull</span></span> | <span data-ttu-id="b261b-125">網域</span><span class="sxs-lookup"><span data-stu-id="b261b-125">Domain</span></span> | <span data-ttu-id="b261b-126">幾何</span><span class="sxs-lookup"><span data-stu-id="b261b-126">Geometry</span></span> | <span data-ttu-id="b261b-127">像素</span><span class="sxs-lookup"><span data-stu-id="b261b-127">Pixel</span></span> | <span data-ttu-id="b261b-128">計算</span><span class="sxs-lookup"><span data-stu-id="b261b-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b261b-129">x</span><span class="sxs-lookup"><span data-stu-id="b261b-129">x</span></span>      | <span data-ttu-id="b261b-130">x</span><span class="sxs-lookup"><span data-stu-id="b261b-130">x</span></span>    | <span data-ttu-id="b261b-131">x</span><span class="sxs-lookup"><span data-stu-id="b261b-131">x</span></span>      | <span data-ttu-id="b261b-132">x</span><span class="sxs-lookup"><span data-stu-id="b261b-132">x</span></span>        | <span data-ttu-id="b261b-133">x</span><span class="sxs-lookup"><span data-stu-id="b261b-133">x</span></span>     | <span data-ttu-id="b261b-134">x</span><span class="sxs-lookup"><span data-stu-id="b261b-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b261b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b261b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b261b-136">收集方法</span><span class="sxs-lookup"><span data-stu-id="b261b-136">Gather methods</span></span>](texture2darray-gather.md)
</dt> <dt>

[<span data-ttu-id="b261b-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="b261b-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




