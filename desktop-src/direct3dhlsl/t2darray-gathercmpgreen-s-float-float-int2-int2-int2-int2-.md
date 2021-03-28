---
title: Texture2DArray：： GatherCmpGreen (S、float、float、int2、int2、int2、int2) 函數
description: 針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。 |Texture2DArray：： GatherCmpGreen (S、float、float、int2、int2、int2、int2) 函數
ms.assetid: 5A4B8AEB-B278-4456-893A-CAE61BFD6CA5
keywords:
- GatherCmpGreen 函式 HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef5c22819e4c582fc354a9069036586e3b7fd028
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514532"
---
# <a name="texture2darraygathercmpgreensfloatfloatint2int2int2int2-function"></a><span data-ttu-id="d5dc0-105">Texture2DArray：： GatherCmpGreen (S、float、float、int2、int2、int2、int2) 函數</span><span class="sxs-lookup"><span data-stu-id="d5dc0-105">Texture2DArray::GatherCmpGreen(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="d5dc0-106">針對在雙線性篩選作業中使用的四個材質值，會傳回其綠色元件與比較值的比較。</span><span class="sxs-lookup"><span data-stu-id="d5dc0-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5dc0-107">語法</span><span class="sxs-lookup"><span data-stu-id="d5dc0-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpGreen(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="d5dc0-108">參數</span><span class="sxs-lookup"><span data-stu-id="d5dc0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5dc0-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="d5dc0-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5dc0-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="d5dc0-110">Type: **SamplerState**</span></span>

<span data-ttu-id="d5dc0-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="d5dc0-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="d5dc0-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5dc0-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5dc0-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="d5dc0-113">Type: **float**</span></span>

<span data-ttu-id="d5dc0-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="d5dc0-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="d5dc0-115">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5dc0-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5dc0-116">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="d5dc0-116">Type: **float**</span></span>

<span data-ttu-id="d5dc0-117">要針對每個取樣值進行比較的值。</span><span class="sxs-lookup"><span data-stu-id="d5dc0-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="d5dc0-118">*Offset1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5dc0-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5dc0-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="d5dc0-119">Type: **int2**</span></span>

<span data-ttu-id="d5dc0-120">第一個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="d5dc0-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="d5dc0-121">*Offset2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5dc0-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5dc0-122">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="d5dc0-122">Type: **int2**</span></span>

<span data-ttu-id="d5dc0-123">第二個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="d5dc0-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="d5dc0-124">*Offset3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5dc0-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5dc0-125">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="d5dc0-125">Type: **int2**</span></span>

<span data-ttu-id="d5dc0-126">第三個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="d5dc0-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="d5dc0-127">*Offset4* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5dc0-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5dc0-128">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="d5dc0-128">Type: **int2**</span></span>

<span data-ttu-id="d5dc0-129">第四個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="d5dc0-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5dc0-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5dc0-130">Return value</span></span>

<span data-ttu-id="d5dc0-131">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="d5dc0-131">Type: **TemplateType**</span></span>

<span data-ttu-id="d5dc0-132">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="d5dc0-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5dc0-133">備註</span><span class="sxs-lookup"><span data-stu-id="d5dc0-133">Remarks</span></span>

<span data-ttu-id="d5dc0-134">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="d5dc0-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="d5dc0-135">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="d5dc0-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d5dc0-136">頂點</span><span class="sxs-lookup"><span data-stu-id="d5dc0-136">Vertex</span></span> | <span data-ttu-id="d5dc0-137">船體</span><span class="sxs-lookup"><span data-stu-id="d5dc0-137">Hull</span></span> | <span data-ttu-id="d5dc0-138">網域</span><span class="sxs-lookup"><span data-stu-id="d5dc0-138">Domain</span></span> | <span data-ttu-id="d5dc0-139">幾何</span><span class="sxs-lookup"><span data-stu-id="d5dc0-139">Geometry</span></span> | <span data-ttu-id="d5dc0-140">像素</span><span class="sxs-lookup"><span data-stu-id="d5dc0-140">Pixel</span></span> | <span data-ttu-id="d5dc0-141">計算</span><span class="sxs-lookup"><span data-stu-id="d5dc0-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d5dc0-142">x</span><span class="sxs-lookup"><span data-stu-id="d5dc0-142">x</span></span>      | <span data-ttu-id="d5dc0-143">x</span><span class="sxs-lookup"><span data-stu-id="d5dc0-143">x</span></span>    | <span data-ttu-id="d5dc0-144">x</span><span class="sxs-lookup"><span data-stu-id="d5dc0-144">x</span></span>      | <span data-ttu-id="d5dc0-145">x</span><span class="sxs-lookup"><span data-stu-id="d5dc0-145">x</span></span>        | <span data-ttu-id="d5dc0-146">x</span><span class="sxs-lookup"><span data-stu-id="d5dc0-146">x</span></span>     | <span data-ttu-id="d5dc0-147">x</span><span class="sxs-lookup"><span data-stu-id="d5dc0-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d5dc0-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5dc0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5dc0-149">GatherCmpGreen 方法</span><span class="sxs-lookup"><span data-stu-id="d5dc0-149">GatherCmpGreen methods</span></span>](texture2darray-gathercmpgreen.md)
</dt> </dl>

 

 




