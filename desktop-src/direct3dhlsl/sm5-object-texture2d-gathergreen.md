---
title: Texture2D：： GatherGreen (S，float，int) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。 |Texture2D：： GatherGreen (S，float，int) 函數
ms.assetid: 97e1fb52-75f4-4e73-93f1-98b7a5925efc
keywords:
- GatherGreen 函式 HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 722d7a3ac90fa3083b8f42f7704f5c9e0aeb1829
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992002"
---
# <a name="texture2dgathergreensfloatint-function"></a><span data-ttu-id="4f663-105">Texture2D：： GatherGreen (S，float，int) 函數</span><span class="sxs-lookup"><span data-stu-id="4f663-105">Texture2D::GatherGreen(S,float,int) function</span></span>

<span data-ttu-id="4f663-106">針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="4f663-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f663-107">語法</span><span class="sxs-lookup"><span data-stu-id="4f663-107">Syntax</span></span>

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="4f663-108">參數</span><span class="sxs-lookup"><span data-stu-id="4f663-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f663-109"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="4f663-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f663-110">類型：**取樣** 器</span><span class="sxs-lookup"><span data-stu-id="4f663-110">Type: **sampler**</span></span>

<span data-ttu-id="4f663-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="4f663-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="4f663-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4f663-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f663-113">類型： **float2**</span><span class="sxs-lookup"><span data-stu-id="4f663-113">Type: **float2**</span></span>

<span data-ttu-id="4f663-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="4f663-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="4f663-115">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4f663-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f663-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="4f663-116">Type: **int2**</span></span>

<span data-ttu-id="4f663-117">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="4f663-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f663-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f663-118">Return value</span></span>

<span data-ttu-id="4f663-119">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="4f663-119">Type: **TemplateType**</span></span>

<span data-ttu-id="4f663-120">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="4f663-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f663-121">備註</span><span class="sxs-lookup"><span data-stu-id="4f663-121">Remarks</span></span>

<span data-ttu-id="4f663-122">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="4f663-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="4f663-123">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="4f663-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4f663-124">頂點</span><span class="sxs-lookup"><span data-stu-id="4f663-124">Vertex</span></span> | <span data-ttu-id="4f663-125">船體</span><span class="sxs-lookup"><span data-stu-id="4f663-125">Hull</span></span> | <span data-ttu-id="4f663-126">網域</span><span class="sxs-lookup"><span data-stu-id="4f663-126">Domain</span></span> | <span data-ttu-id="4f663-127">幾何</span><span class="sxs-lookup"><span data-stu-id="4f663-127">Geometry</span></span> | <span data-ttu-id="4f663-128">像素</span><span class="sxs-lookup"><span data-stu-id="4f663-128">Pixel</span></span> | <span data-ttu-id="4f663-129">計算</span><span class="sxs-lookup"><span data-stu-id="4f663-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4f663-130">x</span><span class="sxs-lookup"><span data-stu-id="4f663-130">x</span></span>      | <span data-ttu-id="4f663-131">x</span><span class="sxs-lookup"><span data-stu-id="4f663-131">x</span></span>    | <span data-ttu-id="4f663-132">x</span><span class="sxs-lookup"><span data-stu-id="4f663-132">x</span></span>      | <span data-ttu-id="4f663-133">x</span><span class="sxs-lookup"><span data-stu-id="4f663-133">x</span></span>        | <span data-ttu-id="4f663-134">x</span><span class="sxs-lookup"><span data-stu-id="4f663-134">x</span></span>     | <span data-ttu-id="4f663-135">x</span><span class="sxs-lookup"><span data-stu-id="4f663-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4f663-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f663-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f663-137">GatherGreen 方法</span><span class="sxs-lookup"><span data-stu-id="4f663-137">GatherGreen methods</span></span>](texture2d-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="4f663-138">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4f663-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




