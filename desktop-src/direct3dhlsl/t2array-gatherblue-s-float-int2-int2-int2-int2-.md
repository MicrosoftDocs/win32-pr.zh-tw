---
title: 'GatherBlue (S、float、int2、int2、int2、int2) function (HLSL reference) '
description: '傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業。 |GatherBlue (S、float、int2、int2、int2、int2) function (HLSL reference) '
ms.assetid: 0DDD3235-4F12-4D74-975A-F70A271C1FC0
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
ms.openlocfilehash: a5676d9d6b25c6e67123c59dac14efa234386d4e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322392"
---
# <a name="gatherbluesfloatint2int2int2int2-function-hlsl-reference"></a><span data-ttu-id="283a3-105">GatherBlue (S、float、int2、int2、int2、int2) function (HLSL reference) </span><span class="sxs-lookup"><span data-stu-id="283a3-105">GatherBlue(S,float,int2,int2,int2,int2) function (HLSL reference)</span></span>

<span data-ttu-id="283a3-106">傳回四個材質值的藍色元件，這些值會用於雙線性篩選作業。</span><span class="sxs-lookup"><span data-stu-id="283a3-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="283a3-107">語法</span><span class="sxs-lookup"><span data-stu-id="283a3-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="283a3-108">參數</span><span class="sxs-lookup"><span data-stu-id="283a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="283a3-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="283a3-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="283a3-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="283a3-110">Type: **SamplerState**</span></span>

<span data-ttu-id="283a3-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="283a3-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="283a3-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="283a3-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="283a3-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="283a3-113">Type: **float**</span></span>

<span data-ttu-id="283a3-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="283a3-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="283a3-115">*Offset1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="283a3-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="283a3-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="283a3-116">Type: **int2**</span></span>

<span data-ttu-id="283a3-117">第一個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="283a3-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="283a3-118">*Offset2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="283a3-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="283a3-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="283a3-119">Type: **int2**</span></span>

<span data-ttu-id="283a3-120">第二個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="283a3-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="283a3-121">*Offset3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="283a3-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="283a3-122">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="283a3-122">Type: **int2**</span></span>

<span data-ttu-id="283a3-123">第三個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="283a3-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="283a3-124">*Offset4* \[在\]</span><span class="sxs-lookup"><span data-stu-id="283a3-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="283a3-125">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="283a3-125">Type: **int2**</span></span>

<span data-ttu-id="283a3-126">第四個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="283a3-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="283a3-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="283a3-127">Return value</span></span>

<span data-ttu-id="283a3-128">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="283a3-128">Type: **TemplateType**</span></span>

<span data-ttu-id="283a3-129">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="283a3-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="283a3-130">備註</span><span class="sxs-lookup"><span data-stu-id="283a3-130">Remarks</span></span>

<span data-ttu-id="283a3-131">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="283a3-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="283a3-132">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="283a3-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="283a3-133">頂點</span><span class="sxs-lookup"><span data-stu-id="283a3-133">Vertex</span></span> | <span data-ttu-id="283a3-134">船體</span><span class="sxs-lookup"><span data-stu-id="283a3-134">Hull</span></span> | <span data-ttu-id="283a3-135">網域</span><span class="sxs-lookup"><span data-stu-id="283a3-135">Domain</span></span> | <span data-ttu-id="283a3-136">幾何</span><span class="sxs-lookup"><span data-stu-id="283a3-136">Geometry</span></span> | <span data-ttu-id="283a3-137">像素</span><span class="sxs-lookup"><span data-stu-id="283a3-137">Pixel</span></span> | <span data-ttu-id="283a3-138">計算</span><span class="sxs-lookup"><span data-stu-id="283a3-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="283a3-139">x</span><span class="sxs-lookup"><span data-stu-id="283a3-139">x</span></span>      | <span data-ttu-id="283a3-140">x</span><span class="sxs-lookup"><span data-stu-id="283a3-140">x</span></span>    | <span data-ttu-id="283a3-141">x</span><span class="sxs-lookup"><span data-stu-id="283a3-141">x</span></span>      | <span data-ttu-id="283a3-142">x</span><span class="sxs-lookup"><span data-stu-id="283a3-142">x</span></span>        | <span data-ttu-id="283a3-143">x</span><span class="sxs-lookup"><span data-stu-id="283a3-143">x</span></span>     | <span data-ttu-id="283a3-144">x</span><span class="sxs-lookup"><span data-stu-id="283a3-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="283a3-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="283a3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="283a3-146">GatherBlue 方法</span><span class="sxs-lookup"><span data-stu-id="283a3-146">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> </dl>

 

 




