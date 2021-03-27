---
title: Texture2D：：搜集 (S、float、int) 函數
description: 傳回要在雙線性篩選作業中使用的四個材質值。 |Texture2D：：搜集 (S、float、int) 函數
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
keywords:
- 收集函數 HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d0a58be0580572441f91a3b3f637601d70cd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696457"
---
# <a name="texture2dgathersfloatint-function"></a><span data-ttu-id="19dcd-105">Texture2D：：搜集 (S、float、int) 函數</span><span class="sxs-lookup"><span data-stu-id="19dcd-105">Texture2D::Gather(S,float,int) function</span></span>

<span data-ttu-id="19dcd-106">傳回要在雙線性篩選作業中使用的四個材質值。</span><span class="sxs-lookup"><span data-stu-id="19dcd-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="19dcd-107">語法</span><span class="sxs-lookup"><span data-stu-id="19dcd-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="19dcd-108">參數</span><span class="sxs-lookup"><span data-stu-id="19dcd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19dcd-109"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="19dcd-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19dcd-110">類型：**取樣** 器</span><span class="sxs-lookup"><span data-stu-id="19dcd-110">Type: **sampler**</span></span>

<span data-ttu-id="19dcd-111">以零為基底的取樣器索引。</span><span class="sxs-lookup"><span data-stu-id="19dcd-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="19dcd-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19dcd-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19dcd-113">類型： **float2**</span><span class="sxs-lookup"><span data-stu-id="19dcd-113">Type: **float2**</span></span>

<span data-ttu-id="19dcd-114">此範例會協調 (u，v) 。</span><span class="sxs-lookup"><span data-stu-id="19dcd-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="19dcd-115">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19dcd-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19dcd-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="19dcd-116">Type: **int2**</span></span>

<span data-ttu-id="19dcd-117">取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="19dcd-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19dcd-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="19dcd-118">Return value</span></span>

<span data-ttu-id="19dcd-119">類型： **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="19dcd-119">Type: **TemplateType**</span></span>

<span data-ttu-id="19dcd-120">四個元件的值，其類型與範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="19dcd-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="19dcd-121">備註</span><span class="sxs-lookup"><span data-stu-id="19dcd-121">Remarks</span></span>

<span data-ttu-id="19dcd-122">紋理範例可用於雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="19dcd-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="19dcd-123">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="19dcd-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="19dcd-124">頂點</span><span class="sxs-lookup"><span data-stu-id="19dcd-124">Vertex</span></span> | <span data-ttu-id="19dcd-125">船體</span><span class="sxs-lookup"><span data-stu-id="19dcd-125">Hull</span></span> | <span data-ttu-id="19dcd-126">網域</span><span class="sxs-lookup"><span data-stu-id="19dcd-126">Domain</span></span> | <span data-ttu-id="19dcd-127">幾何</span><span class="sxs-lookup"><span data-stu-id="19dcd-127">Geometry</span></span> | <span data-ttu-id="19dcd-128">像素</span><span class="sxs-lookup"><span data-stu-id="19dcd-128">Pixel</span></span> | <span data-ttu-id="19dcd-129">計算</span><span class="sxs-lookup"><span data-stu-id="19dcd-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="19dcd-130">x</span><span class="sxs-lookup"><span data-stu-id="19dcd-130">x</span></span>      | <span data-ttu-id="19dcd-131">x</span><span class="sxs-lookup"><span data-stu-id="19dcd-131">x</span></span>    | <span data-ttu-id="19dcd-132">x</span><span class="sxs-lookup"><span data-stu-id="19dcd-132">x</span></span>      | <span data-ttu-id="19dcd-133">x</span><span class="sxs-lookup"><span data-stu-id="19dcd-133">x</span></span>        | <span data-ttu-id="19dcd-134">x</span><span class="sxs-lookup"><span data-stu-id="19dcd-134">x</span></span>     | <span data-ttu-id="19dcd-135">x</span><span class="sxs-lookup"><span data-stu-id="19dcd-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="19dcd-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19dcd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19dcd-137">收集方法</span><span class="sxs-lookup"><span data-stu-id="19dcd-137">Gather methods</span></span>](texture2d-gather.md)
</dt> <dt>

[<span data-ttu-id="19dcd-138">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="19dcd-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




