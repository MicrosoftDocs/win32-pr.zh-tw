---
title: Texture2D：： GatherCmpAlpha (S、float、float、int) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較。 |Texture2D：： GatherCmpAlpha (S、float、float、int) 函數
ms.assetid: 6fa60604-1eac-405d-bffa-3055569b7a09
keywords:
- GatherCmpAlpha 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a7f7fcdc6e24cac5c04068fda7f781d0bdd376a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104386350"
---
# <a name="texture2dgathercmpalphasfloatfloatint-function"></a><span data-ttu-id="afd2a-105">Texture2D：： GatherCmpAlpha (S、float、float、int) 函數</span><span class="sxs-lookup"><span data-stu-id="afd2a-105">Texture2D::GatherCmpAlpha(S,float,float,int) function</span></span>

<span data-ttu-id="afd2a-106">針對在雙線性篩選作業中使用的四個材質值，會傳回其 Alpha 元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="afd2a-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their alpha component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="afd2a-107">語法</span><span class="sxs-lookup"><span data-stu-id="afd2a-107">Syntax</span></span>

``` syntax
float4 GatherCmpAlpha(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="afd2a-108">參數</span><span class="sxs-lookup"><span data-stu-id="afd2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afd2a-109"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="afd2a-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd2a-110">類型： **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="afd2a-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="afd2a-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="afd2a-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="afd2a-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="afd2a-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd2a-113">類型： **float2**</span><span class="sxs-lookup"><span data-stu-id="afd2a-113">Type: **float2**</span></span>

<span data-ttu-id="afd2a-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="afd2a-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="afd2a-115">*比較 \_ 值* \[\]</span><span class="sxs-lookup"><span data-stu-id="afd2a-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd2a-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="afd2a-116">Type: **float**</span></span>

<span data-ttu-id="afd2a-117">要針對每個取樣值進行比較的值。</span><span class="sxs-lookup"><span data-stu-id="afd2a-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="afd2a-118">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="afd2a-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd2a-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="afd2a-119">Type: **int2**</span></span>

<span data-ttu-id="afd2a-120">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="afd2a-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afd2a-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="afd2a-121">Return value</span></span>

<span data-ttu-id="afd2a-122">類型： **float4**</span><span class="sxs-lookup"><span data-stu-id="afd2a-122">Type: **float4**</span></span>

<span data-ttu-id="afd2a-123">四個元件的值，每個元件都是每個元件的比較結果。</span><span class="sxs-lookup"><span data-stu-id="afd2a-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="afd2a-124">備註</span><span class="sxs-lookup"><span data-stu-id="afd2a-124">Remarks</span></span>

<span data-ttu-id="afd2a-125">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="afd2a-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="afd2a-126">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="afd2a-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="afd2a-127">頂點</span><span class="sxs-lookup"><span data-stu-id="afd2a-127">Vertex</span></span> | <span data-ttu-id="afd2a-128">船體</span><span class="sxs-lookup"><span data-stu-id="afd2a-128">Hull</span></span> | <span data-ttu-id="afd2a-129">網域</span><span class="sxs-lookup"><span data-stu-id="afd2a-129">Domain</span></span> | <span data-ttu-id="afd2a-130">幾何</span><span class="sxs-lookup"><span data-stu-id="afd2a-130">Geometry</span></span> | <span data-ttu-id="afd2a-131">像素</span><span class="sxs-lookup"><span data-stu-id="afd2a-131">Pixel</span></span> | <span data-ttu-id="afd2a-132">計算</span><span class="sxs-lookup"><span data-stu-id="afd2a-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="afd2a-133">x</span><span class="sxs-lookup"><span data-stu-id="afd2a-133">x</span></span>      | <span data-ttu-id="afd2a-134">x</span><span class="sxs-lookup"><span data-stu-id="afd2a-134">x</span></span>    | <span data-ttu-id="afd2a-135">x</span><span class="sxs-lookup"><span data-stu-id="afd2a-135">x</span></span>      | <span data-ttu-id="afd2a-136">x</span><span class="sxs-lookup"><span data-stu-id="afd2a-136">x</span></span>        | <span data-ttu-id="afd2a-137">x</span><span class="sxs-lookup"><span data-stu-id="afd2a-137">x</span></span>     | <span data-ttu-id="afd2a-138">x</span><span class="sxs-lookup"><span data-stu-id="afd2a-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="afd2a-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afd2a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afd2a-140">GatherCmpAlpha 方法</span><span class="sxs-lookup"><span data-stu-id="afd2a-140">GatherCmpAlpha methods</span></span>](texture2d-gathercmpalpha.md)
</dt> <dt>

[<span data-ttu-id="afd2a-141">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="afd2a-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




