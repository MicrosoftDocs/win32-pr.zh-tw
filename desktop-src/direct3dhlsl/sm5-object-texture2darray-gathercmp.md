---
title: Texture2DArray：： GatherCmp (S、float、float、int) 函數
description: 針對要在雙線性篩選作業中使用的四個材質值，會傳回與比較值的比較。 |Texture2DArray：： GatherCmp (S、float、float、int) 函數
ms.assetid: 7bb86448-cc73-4423-9ef4-149427cffc95
keywords:
- GatherCmp 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbac4c231f7a7070d3ca4549f3d1189b81292b8c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973972"
---
# <a name="texture2darraygathercmpsfloatfloatint-function"></a><span data-ttu-id="ce488-105">Texture2DArray：： GatherCmp (S、float、float、int) 函數</span><span class="sxs-lookup"><span data-stu-id="ce488-105">Texture2DArray::GatherCmp(S,float,float,int) function</span></span>

<span data-ttu-id="ce488-106">針對要在雙線性篩選作業中使用的四個材質值，會傳回與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="ce488-106">For four texel values that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce488-107">語法</span><span class="sxs-lookup"><span data-stu-id="ce488-107">Syntax</span></span>

``` syntax
float4 GatherCmp(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="ce488-108">參數</span><span class="sxs-lookup"><span data-stu-id="ce488-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce488-109"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="ce488-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce488-110">類型： **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="ce488-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="ce488-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="ce488-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ce488-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce488-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce488-113">類型： **float3**</span><span class="sxs-lookup"><span data-stu-id="ce488-113">Type: **float3**</span></span>

<span data-ttu-id="ce488-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="ce488-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ce488-115">*比較 \_ 值* \[\]</span><span class="sxs-lookup"><span data-stu-id="ce488-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce488-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="ce488-116">Type: **float**</span></span>

<span data-ttu-id="ce488-117">要針對每個取樣值進行比較的值。</span><span class="sxs-lookup"><span data-stu-id="ce488-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="ce488-118">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce488-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce488-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="ce488-119">Type: **int2**</span></span>

<span data-ttu-id="ce488-120">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="ce488-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce488-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce488-121">Return value</span></span>

<span data-ttu-id="ce488-122">類型： **float4**</span><span class="sxs-lookup"><span data-stu-id="ce488-122">Type: **float4**</span></span>

<span data-ttu-id="ce488-123">四個元件的值，每個元件都是每個元件的比較結果。</span><span class="sxs-lookup"><span data-stu-id="ce488-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce488-124">備註</span><span class="sxs-lookup"><span data-stu-id="ce488-124">Remarks</span></span>

<span data-ttu-id="ce488-125">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="ce488-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ce488-126">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="ce488-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ce488-127">頂點</span><span class="sxs-lookup"><span data-stu-id="ce488-127">Vertex</span></span> | <span data-ttu-id="ce488-128">船體</span><span class="sxs-lookup"><span data-stu-id="ce488-128">Hull</span></span> | <span data-ttu-id="ce488-129">網域</span><span class="sxs-lookup"><span data-stu-id="ce488-129">Domain</span></span> | <span data-ttu-id="ce488-130">幾何</span><span class="sxs-lookup"><span data-stu-id="ce488-130">Geometry</span></span> | <span data-ttu-id="ce488-131">像素</span><span class="sxs-lookup"><span data-stu-id="ce488-131">Pixel</span></span> | <span data-ttu-id="ce488-132">計算</span><span class="sxs-lookup"><span data-stu-id="ce488-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ce488-133">x</span><span class="sxs-lookup"><span data-stu-id="ce488-133">x</span></span>      | <span data-ttu-id="ce488-134">x</span><span class="sxs-lookup"><span data-stu-id="ce488-134">x</span></span>    | <span data-ttu-id="ce488-135">x</span><span class="sxs-lookup"><span data-stu-id="ce488-135">x</span></span>      | <span data-ttu-id="ce488-136">x</span><span class="sxs-lookup"><span data-stu-id="ce488-136">x</span></span>        | <span data-ttu-id="ce488-137">x</span><span class="sxs-lookup"><span data-stu-id="ce488-137">x</span></span>     | <span data-ttu-id="ce488-138">x</span><span class="sxs-lookup"><span data-stu-id="ce488-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ce488-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce488-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce488-140">GatherCmp 方法</span><span class="sxs-lookup"><span data-stu-id="ce488-140">GatherCmp methods</span></span>](texture2darray-gathercmp.md)
</dt> <dt>

[<span data-ttu-id="ce488-141">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ce488-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




