---
title: Texture2DArray：： GatherAlpha (S、float、int2、int2、int2、int2) 函數
description: 傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。 |Texture2DArray：： GatherAlpha (S、float、int2、int2、int2、int2) 函數
ms.assetid: A7F96B45-A097-437B-A0D0-18555FF76544
keywords:
- GatherAlpha 函式 HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff6910152c9ac133c819456b9ec7aaeb2406b791
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945828"
---
# <a name="texture2darraygatheralphasfloatint2int2int2int2-function"></a><span data-ttu-id="69676-105">Texture2DArray：： GatherAlpha (S、float、int2、int2、int2、int2) 函數</span><span class="sxs-lookup"><span data-stu-id="69676-105">Texture2DArray::GatherAlpha(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="69676-106">傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。</span><span class="sxs-lookup"><span data-stu-id="69676-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="69676-107">語法</span><span class="sxs-lookup"><span data-stu-id="69676-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="69676-108">參數</span><span class="sxs-lookup"><span data-stu-id="69676-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69676-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="69676-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69676-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="69676-110">Type: **SamplerState**</span></span>

<span data-ttu-id="69676-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="69676-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="69676-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69676-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69676-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="69676-113">Type: **float**</span></span>

<span data-ttu-id="69676-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="69676-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="69676-115">*Offset1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69676-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69676-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="69676-116">Type: **int2**</span></span>

<span data-ttu-id="69676-117">第一個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="69676-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="69676-118">*Offset2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69676-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69676-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="69676-119">Type: **int2**</span></span>

<span data-ttu-id="69676-120">第二個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="69676-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="69676-121">*Offset3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69676-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69676-122">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="69676-122">Type: **int2**</span></span>

<span data-ttu-id="69676-123">第三個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="69676-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="69676-124">*Offset4* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69676-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69676-125">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="69676-125">Type: **int2**</span></span>

<span data-ttu-id="69676-126">第四個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="69676-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69676-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="69676-127">Return value</span></span>

<span data-ttu-id="69676-128">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="69676-128">Type: **TemplateType**</span></span>

<span data-ttu-id="69676-129">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="69676-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="69676-130">備註</span><span class="sxs-lookup"><span data-stu-id="69676-130">Remarks</span></span>

<span data-ttu-id="69676-131">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="69676-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="69676-132">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="69676-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="69676-133">頂點</span><span class="sxs-lookup"><span data-stu-id="69676-133">Vertex</span></span> | <span data-ttu-id="69676-134">船體</span><span class="sxs-lookup"><span data-stu-id="69676-134">Hull</span></span> | <span data-ttu-id="69676-135">網域</span><span class="sxs-lookup"><span data-stu-id="69676-135">Domain</span></span> | <span data-ttu-id="69676-136">幾何</span><span class="sxs-lookup"><span data-stu-id="69676-136">Geometry</span></span> | <span data-ttu-id="69676-137">像素</span><span class="sxs-lookup"><span data-stu-id="69676-137">Pixel</span></span> | <span data-ttu-id="69676-138">計算</span><span class="sxs-lookup"><span data-stu-id="69676-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="69676-139">x</span><span class="sxs-lookup"><span data-stu-id="69676-139">x</span></span>      | <span data-ttu-id="69676-140">x</span><span class="sxs-lookup"><span data-stu-id="69676-140">x</span></span>    | <span data-ttu-id="69676-141">x</span><span class="sxs-lookup"><span data-stu-id="69676-141">x</span></span>      | <span data-ttu-id="69676-142">x</span><span class="sxs-lookup"><span data-stu-id="69676-142">x</span></span>        | <span data-ttu-id="69676-143">x</span><span class="sxs-lookup"><span data-stu-id="69676-143">x</span></span>     | <span data-ttu-id="69676-144">x</span><span class="sxs-lookup"><span data-stu-id="69676-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="69676-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69676-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69676-146">GatherAlpha 方法</span><span class="sxs-lookup"><span data-stu-id="69676-146">GatherAlpha methods</span></span>](texture2darray-gatheralpha.md)
</dt> </dl>

 

 




