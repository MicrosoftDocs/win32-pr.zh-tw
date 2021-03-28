---
title: Texture2D：： GatherRed (S，float，int) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較。 |Texture2D：： GatherRed (S，float，int) 函數
ms.assetid: 6d2d1556-d52f-4625-93ca-34da399f9a8b
keywords:
- GatherRed 函式 HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f05196063f6a17cc34865157c17a92bc2bb116bf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974225"
---
# <a name="texture2dgatherredsfloatint-function"></a><span data-ttu-id="08741-105">Texture2D：： GatherRed (S，float，int) 函數</span><span class="sxs-lookup"><span data-stu-id="08741-105">Texture2D::GatherRed(S,float,int) function</span></span>

<span data-ttu-id="08741-106">針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="08741-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="08741-107">語法</span><span class="sxs-lookup"><span data-stu-id="08741-107">Syntax</span></span>

``` syntax
TemplateType GatherRed(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="08741-108">參數</span><span class="sxs-lookup"><span data-stu-id="08741-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08741-109"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="08741-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08741-110">類型：**取樣** 器</span><span class="sxs-lookup"><span data-stu-id="08741-110">Type: **sampler**</span></span>

<span data-ttu-id="08741-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="08741-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="08741-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="08741-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08741-113">類型： **float2**</span><span class="sxs-lookup"><span data-stu-id="08741-113">Type: **float2**</span></span>

<span data-ttu-id="08741-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="08741-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="08741-115">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="08741-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08741-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="08741-116">Type: **int2**</span></span>

<span data-ttu-id="08741-117">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="08741-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08741-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="08741-118">Return value</span></span>

<span data-ttu-id="08741-119">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="08741-119">Type: **TemplateType**</span></span>

<span data-ttu-id="08741-120">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="08741-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="08741-121">備註</span><span class="sxs-lookup"><span data-stu-id="08741-121">Remarks</span></span>

<span data-ttu-id="08741-122">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="08741-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="08741-123">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="08741-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="08741-124">頂點</span><span class="sxs-lookup"><span data-stu-id="08741-124">Vertex</span></span> | <span data-ttu-id="08741-125">船體</span><span class="sxs-lookup"><span data-stu-id="08741-125">Hull</span></span> | <span data-ttu-id="08741-126">網域</span><span class="sxs-lookup"><span data-stu-id="08741-126">Domain</span></span> | <span data-ttu-id="08741-127">幾何</span><span class="sxs-lookup"><span data-stu-id="08741-127">Geometry</span></span> | <span data-ttu-id="08741-128">像素</span><span class="sxs-lookup"><span data-stu-id="08741-128">Pixel</span></span> | <span data-ttu-id="08741-129">計算</span><span class="sxs-lookup"><span data-stu-id="08741-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="08741-130">x</span><span class="sxs-lookup"><span data-stu-id="08741-130">x</span></span>      | <span data-ttu-id="08741-131">x</span><span class="sxs-lookup"><span data-stu-id="08741-131">x</span></span>    | <span data-ttu-id="08741-132">x</span><span class="sxs-lookup"><span data-stu-id="08741-132">x</span></span>      | <span data-ttu-id="08741-133">x</span><span class="sxs-lookup"><span data-stu-id="08741-133">x</span></span>        | <span data-ttu-id="08741-134">x</span><span class="sxs-lookup"><span data-stu-id="08741-134">x</span></span>     | <span data-ttu-id="08741-135">x</span><span class="sxs-lookup"><span data-stu-id="08741-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="08741-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08741-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08741-137">GatherRed 方法</span><span class="sxs-lookup"><span data-stu-id="08741-137">GatherRed methods</span></span>](texture2d-gatherred.md)
</dt> <dt>

[<span data-ttu-id="08741-138">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="08741-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




