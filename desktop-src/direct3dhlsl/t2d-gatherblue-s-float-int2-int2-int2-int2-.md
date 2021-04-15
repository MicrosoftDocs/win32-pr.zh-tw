---
title: Texture2D：： GatherBlue (S、float、int2、int2、int2、int2) 函數
description: 傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業。 |Texture2D：： GatherBlue (S、float、int2、int2、int2、int2) 函數
ms.assetid: 0FFD3D82-E849-4C19-BEBC-85B9CCA40CA0
keywords:
- GatherBlue 函式 HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21f44482d82e8246391389289f0c90ea6c97de9a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974309"
---
# <a name="gatherbluesfloatint2int2int2int2-function"></a><span data-ttu-id="c8f64-105">GatherBlue (S、float、int2、int2、int2、int2) 函數</span><span class="sxs-lookup"><span data-stu-id="c8f64-105">GatherBlue(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="c8f64-106">傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業。</span><span class="sxs-lookup"><span data-stu-id="c8f64-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f64-107">語法</span><span class="sxs-lookup"><span data-stu-id="c8f64-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="c8f64-108">參數</span><span class="sxs-lookup"><span data-stu-id="c8f64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8f64-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="c8f64-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f64-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="c8f64-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c8f64-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="c8f64-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="c8f64-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8f64-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f64-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c8f64-113">Type: **float**</span></span>

<span data-ttu-id="c8f64-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="c8f64-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="c8f64-115">*Offset1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8f64-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f64-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="c8f64-116">Type: **int2**</span></span>

<span data-ttu-id="c8f64-117">第一個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="c8f64-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c8f64-118">*Offset2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8f64-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f64-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="c8f64-119">Type: **int2**</span></span>

<span data-ttu-id="c8f64-120">第二個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="c8f64-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c8f64-121">*Offset3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8f64-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f64-122">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="c8f64-122">Type: **int2**</span></span>

<span data-ttu-id="c8f64-123">第三個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="c8f64-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="c8f64-124">*Offset4* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8f64-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f64-125">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="c8f64-125">Type: **int2**</span></span>

<span data-ttu-id="c8f64-126">第四個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="c8f64-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8f64-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8f64-127">Return value</span></span>

<span data-ttu-id="c8f64-128">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="c8f64-128">Type: **TemplateType**</span></span>

<span data-ttu-id="c8f64-129">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="c8f64-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8f64-130">備註</span><span class="sxs-lookup"><span data-stu-id="c8f64-130">Remarks</span></span>

<span data-ttu-id="c8f64-131">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="c8f64-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="c8f64-132">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="c8f64-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c8f64-133">頂點</span><span class="sxs-lookup"><span data-stu-id="c8f64-133">Vertex</span></span> | <span data-ttu-id="c8f64-134">船體</span><span class="sxs-lookup"><span data-stu-id="c8f64-134">Hull</span></span> | <span data-ttu-id="c8f64-135">網域</span><span class="sxs-lookup"><span data-stu-id="c8f64-135">Domain</span></span> | <span data-ttu-id="c8f64-136">幾何</span><span class="sxs-lookup"><span data-stu-id="c8f64-136">Geometry</span></span> | <span data-ttu-id="c8f64-137">像素</span><span class="sxs-lookup"><span data-stu-id="c8f64-137">Pixel</span></span> | <span data-ttu-id="c8f64-138">計算</span><span class="sxs-lookup"><span data-stu-id="c8f64-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c8f64-139">x</span><span class="sxs-lookup"><span data-stu-id="c8f64-139">x</span></span>      | <span data-ttu-id="c8f64-140">x</span><span class="sxs-lookup"><span data-stu-id="c8f64-140">x</span></span>    | <span data-ttu-id="c8f64-141">x</span><span class="sxs-lookup"><span data-stu-id="c8f64-141">x</span></span>      | <span data-ttu-id="c8f64-142">x</span><span class="sxs-lookup"><span data-stu-id="c8f64-142">x</span></span>        | <span data-ttu-id="c8f64-143">x</span><span class="sxs-lookup"><span data-stu-id="c8f64-143">x</span></span>     | <span data-ttu-id="c8f64-144">x</span><span class="sxs-lookup"><span data-stu-id="c8f64-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c8f64-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8f64-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f64-146">GatherBlue 方法</span><span class="sxs-lookup"><span data-stu-id="c8f64-146">GatherBlue methods</span></span>](texture2d-gatherblue.md)
</dt> </dl>

 

 




