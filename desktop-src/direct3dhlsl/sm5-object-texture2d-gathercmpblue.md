---
title: Texture2D：： GatherCmpBlue (S、float、float、int) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其藍色元件與比較值的比較。 |Texture2D：： GatherCmpBlue (S、float、float、int) 函數
ms.assetid: d8e03c55-18f1-4598-a700-9ba3a680d78a
keywords:
- GatherCmpBlue 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eedeb21141c1e694effe4eb8c7be70c828aa0a3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991930"
---
# <a name="texture2dgathercmpbluesfloatfloatint-function"></a><span data-ttu-id="62bc6-105">Texture2D：： GatherCmpBlue (S、float、float、int) 函數</span><span class="sxs-lookup"><span data-stu-id="62bc6-105">Texture2D::GatherCmpBlue(S,float,float,int) function</span></span>

<span data-ttu-id="62bc6-106">針對在雙線性篩選作業中使用的四個材質值，會傳回其藍色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="62bc6-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="62bc6-107">語法</span><span class="sxs-lookup"><span data-stu-id="62bc6-107">Syntax</span></span>

``` syntax
float4 GatherCmpBlue(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="62bc6-108">參數</span><span class="sxs-lookup"><span data-stu-id="62bc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62bc6-109"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="62bc6-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62bc6-110">類型： **SamplerComparisonState**</span><span class="sxs-lookup"><span data-stu-id="62bc6-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="62bc6-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="62bc6-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="62bc6-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62bc6-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62bc6-113">類型： **float2**</span><span class="sxs-lookup"><span data-stu-id="62bc6-113">Type: **float2**</span></span>

<span data-ttu-id="62bc6-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="62bc6-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="62bc6-115">*比較 \_ 值* \[\]</span><span class="sxs-lookup"><span data-stu-id="62bc6-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62bc6-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="62bc6-116">Type: **float**</span></span>

<span data-ttu-id="62bc6-117">要針對每個取樣值進行比較的值。</span><span class="sxs-lookup"><span data-stu-id="62bc6-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="62bc6-118">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62bc6-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62bc6-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="62bc6-119">Type: **int2**</span></span>

<span data-ttu-id="62bc6-120">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="62bc6-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62bc6-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="62bc6-121">Return value</span></span>

<span data-ttu-id="62bc6-122">類型： **float4**</span><span class="sxs-lookup"><span data-stu-id="62bc6-122">Type: **float4**</span></span>

<span data-ttu-id="62bc6-123">四個元件的值，每個元件都是每個元件的比較結果。</span><span class="sxs-lookup"><span data-stu-id="62bc6-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="62bc6-124">備註</span><span class="sxs-lookup"><span data-stu-id="62bc6-124">Remarks</span></span>

<span data-ttu-id="62bc6-125">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="62bc6-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="62bc6-126">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="62bc6-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="62bc6-127">頂點</span><span class="sxs-lookup"><span data-stu-id="62bc6-127">Vertex</span></span> | <span data-ttu-id="62bc6-128">船體</span><span class="sxs-lookup"><span data-stu-id="62bc6-128">Hull</span></span> | <span data-ttu-id="62bc6-129">網域</span><span class="sxs-lookup"><span data-stu-id="62bc6-129">Domain</span></span> | <span data-ttu-id="62bc6-130">幾何</span><span class="sxs-lookup"><span data-stu-id="62bc6-130">Geometry</span></span> | <span data-ttu-id="62bc6-131">像素</span><span class="sxs-lookup"><span data-stu-id="62bc6-131">Pixel</span></span> | <span data-ttu-id="62bc6-132">計算</span><span class="sxs-lookup"><span data-stu-id="62bc6-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="62bc6-133">x</span><span class="sxs-lookup"><span data-stu-id="62bc6-133">x</span></span>      | <span data-ttu-id="62bc6-134">x</span><span class="sxs-lookup"><span data-stu-id="62bc6-134">x</span></span>    | <span data-ttu-id="62bc6-135">x</span><span class="sxs-lookup"><span data-stu-id="62bc6-135">x</span></span>      | <span data-ttu-id="62bc6-136">x</span><span class="sxs-lookup"><span data-stu-id="62bc6-136">x</span></span>        | <span data-ttu-id="62bc6-137">x</span><span class="sxs-lookup"><span data-stu-id="62bc6-137">x</span></span>     | <span data-ttu-id="62bc6-138">x</span><span class="sxs-lookup"><span data-stu-id="62bc6-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="62bc6-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62bc6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62bc6-140">GatherCmpBlue 方法</span><span class="sxs-lookup"><span data-stu-id="62bc6-140">GatherCmpBlue methods</span></span>](texture2d-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="62bc6-141">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="62bc6-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




