---
title: Texture2D：： GatherCmpRed (S、float、float、int2、int2、int2、int2) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較。 |Texture2D：： GatherCmpRed (S、float、float、int2、int2、int2、int2) 函數
ms.assetid: B20A766E-0B4F-4FBA-A691-70ACE7BECF33
keywords:
- GatherCmpRed 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f84467c798337ac2cc81283637636900933c9e41
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945865"
---
# <a name="texture2dgathercmpredsfloatfloatint2int2int2int2-function"></a><span data-ttu-id="3101c-105">Texture2D：： GatherCmpRed (S、float、float、int2、int2、int2、int2) 函數</span><span class="sxs-lookup"><span data-stu-id="3101c-105">Texture2D::GatherCmpRed(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="3101c-106">針對在雙線性篩選作業中使用的四個材質值，會傳回其紅色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="3101c-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3101c-107">語法</span><span class="sxs-lookup"><span data-stu-id="3101c-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpRed(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="3101c-108">參數</span><span class="sxs-lookup"><span data-stu-id="3101c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3101c-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="3101c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3101c-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="3101c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="3101c-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="3101c-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="3101c-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3101c-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3101c-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="3101c-113">Type: **float**</span></span>

<span data-ttu-id="3101c-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="3101c-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="3101c-115">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3101c-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3101c-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="3101c-116">Type: **float**</span></span>

<span data-ttu-id="3101c-117">要針對每個取樣值進行比較的值。</span><span class="sxs-lookup"><span data-stu-id="3101c-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="3101c-118">*Offset1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3101c-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3101c-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="3101c-119">Type: **int2**</span></span>

<span data-ttu-id="3101c-120">第一個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="3101c-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3101c-121">*Offset2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3101c-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3101c-122">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="3101c-122">Type: **int2**</span></span>

<span data-ttu-id="3101c-123">第二個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="3101c-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3101c-124">*Offset3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3101c-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3101c-125">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="3101c-125">Type: **int2**</span></span>

<span data-ttu-id="3101c-126">第三個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="3101c-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3101c-127">*Offset4* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3101c-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3101c-128">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="3101c-128">Type: **int2**</span></span>

<span data-ttu-id="3101c-129">第四個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="3101c-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3101c-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="3101c-130">Return value</span></span>

<span data-ttu-id="3101c-131">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="3101c-131">Type: **TemplateType**</span></span>

<span data-ttu-id="3101c-132">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="3101c-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="3101c-133">備註</span><span class="sxs-lookup"><span data-stu-id="3101c-133">Remarks</span></span>

<span data-ttu-id="3101c-134">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="3101c-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="3101c-135">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="3101c-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3101c-136">頂點</span><span class="sxs-lookup"><span data-stu-id="3101c-136">Vertex</span></span> | <span data-ttu-id="3101c-137">船體</span><span class="sxs-lookup"><span data-stu-id="3101c-137">Hull</span></span> | <span data-ttu-id="3101c-138">網域</span><span class="sxs-lookup"><span data-stu-id="3101c-138">Domain</span></span> | <span data-ttu-id="3101c-139">幾何</span><span class="sxs-lookup"><span data-stu-id="3101c-139">Geometry</span></span> | <span data-ttu-id="3101c-140">像素</span><span class="sxs-lookup"><span data-stu-id="3101c-140">Pixel</span></span> | <span data-ttu-id="3101c-141">計算</span><span class="sxs-lookup"><span data-stu-id="3101c-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3101c-142">x</span><span class="sxs-lookup"><span data-stu-id="3101c-142">x</span></span>      | <span data-ttu-id="3101c-143">x</span><span class="sxs-lookup"><span data-stu-id="3101c-143">x</span></span>    | <span data-ttu-id="3101c-144">x</span><span class="sxs-lookup"><span data-stu-id="3101c-144">x</span></span>      | <span data-ttu-id="3101c-145">x</span><span class="sxs-lookup"><span data-stu-id="3101c-145">x</span></span>        | <span data-ttu-id="3101c-146">x</span><span class="sxs-lookup"><span data-stu-id="3101c-146">x</span></span>     | <span data-ttu-id="3101c-147">x</span><span class="sxs-lookup"><span data-stu-id="3101c-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3101c-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3101c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3101c-149">GatherCmpRed 方法</span><span class="sxs-lookup"><span data-stu-id="3101c-149">GatherCmpRed methods</span></span>](texture2d-gathercmpred.md)
</dt> </dl>

 

 




