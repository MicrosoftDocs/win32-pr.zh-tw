---
title: Texture2D：： GatherAlpha (S、float、int2、int2、int2、int2) 函數
description: 傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。 |Texture2D：： GatherAlpha (S、float、int2、int2、int2、int2) 函數
ms.assetid: 925A5085-33CB-4DFC-B4E3-1ADA5892C13A
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
ms.openlocfilehash: 4dc2077c8c10d9a7caba1c9d7a3999ffd522b5ab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992058"
---
# <a name="texture2dgatheralphasfloatint2int2int2int2-function"></a><span data-ttu-id="fd330-105">Texture2D：： GatherAlpha (S、float、int2、int2、int2、int2) 函數</span><span class="sxs-lookup"><span data-stu-id="fd330-105">Texture2D::GatherAlpha(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="fd330-106">傳回四個材質值的 Alpha 元件，這些值會在雙線性篩選作業中使用。</span><span class="sxs-lookup"><span data-stu-id="fd330-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd330-107">語法</span><span class="sxs-lookup"><span data-stu-id="fd330-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="fd330-108">參數</span><span class="sxs-lookup"><span data-stu-id="fd330-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd330-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="fd330-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd330-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="fd330-110">Type: **SamplerState**</span></span>

<span data-ttu-id="fd330-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="fd330-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="fd330-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd330-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd330-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="fd330-113">Type: **float**</span></span>

<span data-ttu-id="fd330-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="fd330-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="fd330-115">*Offset1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd330-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd330-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="fd330-116">Type: **int2**</span></span>

<span data-ttu-id="fd330-117">第一個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="fd330-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fd330-118">*Offset2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd330-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd330-119">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="fd330-119">Type: **int2**</span></span>

<span data-ttu-id="fd330-120">第二個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="fd330-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fd330-121">*Offset3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd330-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd330-122">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="fd330-122">Type: **int2**</span></span>

<span data-ttu-id="fd330-123">第三個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="fd330-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fd330-124">*Offset4* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd330-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd330-125">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="fd330-125">Type: **int2**</span></span>

<span data-ttu-id="fd330-126">第四個位移元件會在取樣之前套用至材質座標。</span><span class="sxs-lookup"><span data-stu-id="fd330-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd330-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd330-127">Return value</span></span>

<span data-ttu-id="fd330-128">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="fd330-128">Type: **TemplateType**</span></span>

<span data-ttu-id="fd330-129">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="fd330-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd330-130">備註</span><span class="sxs-lookup"><span data-stu-id="fd330-130">Remarks</span></span>

<span data-ttu-id="fd330-131">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="fd330-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="fd330-132">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="fd330-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fd330-133">頂點</span><span class="sxs-lookup"><span data-stu-id="fd330-133">Vertex</span></span> | <span data-ttu-id="fd330-134">船體</span><span class="sxs-lookup"><span data-stu-id="fd330-134">Hull</span></span> | <span data-ttu-id="fd330-135">網域</span><span class="sxs-lookup"><span data-stu-id="fd330-135">Domain</span></span> | <span data-ttu-id="fd330-136">幾何</span><span class="sxs-lookup"><span data-stu-id="fd330-136">Geometry</span></span> | <span data-ttu-id="fd330-137">像素</span><span class="sxs-lookup"><span data-stu-id="fd330-137">Pixel</span></span> | <span data-ttu-id="fd330-138">計算</span><span class="sxs-lookup"><span data-stu-id="fd330-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fd330-139">x</span><span class="sxs-lookup"><span data-stu-id="fd330-139">x</span></span>      | <span data-ttu-id="fd330-140">x</span><span class="sxs-lookup"><span data-stu-id="fd330-140">x</span></span>    | <span data-ttu-id="fd330-141">x</span><span class="sxs-lookup"><span data-stu-id="fd330-141">x</span></span>      | <span data-ttu-id="fd330-142">x</span><span class="sxs-lookup"><span data-stu-id="fd330-142">x</span></span>        | <span data-ttu-id="fd330-143">x</span><span class="sxs-lookup"><span data-stu-id="fd330-143">x</span></span>     | <span data-ttu-id="fd330-144">x</span><span class="sxs-lookup"><span data-stu-id="fd330-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fd330-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd330-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd330-146">GatherAlpha 方法</span><span class="sxs-lookup"><span data-stu-id="fd330-146">GatherAlpha methods</span></span>](texture2d-gatheralpha.md)
</dt> </dl>

 

 




