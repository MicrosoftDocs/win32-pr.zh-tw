---
title: Texture2DArray：： GatherGreen (S，float，int) 函數
description: 傳回雙線性篩選作業中所使用之四個材質值的綠色元件。 |Texture2DArray：： GatherGreen (S，float，int) 函數
ms.assetid: bfe9ab9f-64f7-4a50-aa46-2ec6effebce2
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
ms.openlocfilehash: 48a5d968ffe5eeb12fdb0240d1823a9b1834ae19
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195878"
---
# <a name="texture2darraygathergreensfloatint-function"></a><span data-ttu-id="7c6b8-105">Texture2DArray：： GatherGreen (S，float，int) 函數</span><span class="sxs-lookup"><span data-stu-id="7c6b8-105">Texture2DArray::GatherGreen(S,float,int) function</span></span>

<span data-ttu-id="7c6b8-106">傳回雙線性篩選作業中所使用之四個材質值的綠色元件。</span><span class="sxs-lookup"><span data-stu-id="7c6b8-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c6b8-107">語法</span><span class="sxs-lookup"><span data-stu-id="7c6b8-107">Syntax</span></span>

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="7c6b8-108">參數</span><span class="sxs-lookup"><span data-stu-id="7c6b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c6b8-109"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="7c6b8-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c6b8-110">類型：**取樣** 器</span><span class="sxs-lookup"><span data-stu-id="7c6b8-110">Type: **sampler**</span></span>

<span data-ttu-id="7c6b8-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="7c6b8-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="7c6b8-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c6b8-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c6b8-113">類型： **float3**</span><span class="sxs-lookup"><span data-stu-id="7c6b8-113">Type: **float3**</span></span>

<span data-ttu-id="7c6b8-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="7c6b8-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="7c6b8-115">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c6b8-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c6b8-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="7c6b8-116">Type: **int2**</span></span>

<span data-ttu-id="7c6b8-117">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="7c6b8-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c6b8-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c6b8-118">Return value</span></span>

<span data-ttu-id="7c6b8-119">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="7c6b8-119">Type: **TemplateType**</span></span>

<span data-ttu-id="7c6b8-120">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="7c6b8-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c6b8-121">備註</span><span class="sxs-lookup"><span data-stu-id="7c6b8-121">Remarks</span></span>

<span data-ttu-id="7c6b8-122">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="7c6b8-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="7c6b8-123">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="7c6b8-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7c6b8-124">頂點</span><span class="sxs-lookup"><span data-stu-id="7c6b8-124">Vertex</span></span> | <span data-ttu-id="7c6b8-125">船體</span><span class="sxs-lookup"><span data-stu-id="7c6b8-125">Hull</span></span> | <span data-ttu-id="7c6b8-126">網域</span><span class="sxs-lookup"><span data-stu-id="7c6b8-126">Domain</span></span> | <span data-ttu-id="7c6b8-127">幾何</span><span class="sxs-lookup"><span data-stu-id="7c6b8-127">Geometry</span></span> | <span data-ttu-id="7c6b8-128">像素</span><span class="sxs-lookup"><span data-stu-id="7c6b8-128">Pixel</span></span> | <span data-ttu-id="7c6b8-129">計算</span><span class="sxs-lookup"><span data-stu-id="7c6b8-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7c6b8-130">x</span><span class="sxs-lookup"><span data-stu-id="7c6b8-130">x</span></span>      | <span data-ttu-id="7c6b8-131">x</span><span class="sxs-lookup"><span data-stu-id="7c6b8-131">x</span></span>    | <span data-ttu-id="7c6b8-132">x</span><span class="sxs-lookup"><span data-stu-id="7c6b8-132">x</span></span>      | <span data-ttu-id="7c6b8-133">x</span><span class="sxs-lookup"><span data-stu-id="7c6b8-133">x</span></span>        | <span data-ttu-id="7c6b8-134">x</span><span class="sxs-lookup"><span data-stu-id="7c6b8-134">x</span></span>     | <span data-ttu-id="7c6b8-135">x</span><span class="sxs-lookup"><span data-stu-id="7c6b8-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7c6b8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c6b8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c6b8-137">GatherGreen 方法</span><span class="sxs-lookup"><span data-stu-id="7c6b8-137">GatherGreen methods</span></span>](texture2darray-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="7c6b8-138">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="7c6b8-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




