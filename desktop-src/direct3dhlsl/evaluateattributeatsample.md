---
title: EvaluateAttributeAtSample 函式
description: 在索引範例位置評估。
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- EvaluateAttributeAtSample 函式 HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b183f86599d08a6892e33c169b938dc09a2b55de
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678295"
---
# <a name="evaluateattributeatsample-function"></a><span data-ttu-id="e727d-104">EvaluateAttributeAtSample 函式</span><span class="sxs-lookup"><span data-stu-id="e727d-104">EvaluateAttributeAtSample function</span></span>

<span data-ttu-id="e727d-105">在索引範例位置評估。</span><span class="sxs-lookup"><span data-stu-id="e727d-105">Evaluates at the indexed sample location.</span></span>

## <a name="syntax"></a><span data-ttu-id="e727d-106">語法</span><span class="sxs-lookup"><span data-stu-id="e727d-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="e727d-107">參數</span><span class="sxs-lookup"><span data-stu-id="e727d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e727d-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e727d-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e727d-109">類型： **attrib 數值**</span><span class="sxs-lookup"><span data-stu-id="e727d-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="e727d-110">輸入值。</span><span class="sxs-lookup"><span data-stu-id="e727d-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="e727d-111">*sampleindex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e727d-111">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e727d-112">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="e727d-112">Type: **uint**</span></span>

<span data-ttu-id="e727d-113">範例位置。</span><span class="sxs-lookup"><span data-stu-id="e727d-113">The sample location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e727d-114">備註</span><span class="sxs-lookup"><span data-stu-id="e727d-114">Remarks</span></span>

<span data-ttu-id="e727d-115">插補模式可以是 **線性** 或線性，而不是在變數上的 **\_ \_ 觀點** 。</span><span class="sxs-lookup"><span data-stu-id="e727d-115">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="e727d-116">會忽略 **距心** 或 **sample** 的使用。</span><span class="sxs-lookup"><span data-stu-id="e727d-116">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="e727d-117">也允許具有常數插補的屬性，在此情況下，會忽略範例索引。</span><span class="sxs-lookup"><span data-stu-id="e727d-117">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="e727d-118">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="e727d-118">Minimum Shader Model</span></span>

<span data-ttu-id="e727d-119">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="e727d-119">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e727d-120">著色器模型</span><span class="sxs-lookup"><span data-stu-id="e727d-120">Shader Model</span></span>                                                                | <span data-ttu-id="e727d-121">支援</span><span class="sxs-lookup"><span data-stu-id="e727d-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e727d-122">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="e727d-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e727d-123">是</span><span class="sxs-lookup"><span data-stu-id="e727d-123">yes</span></span>       |



 

<span data-ttu-id="e727d-124">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="e727d-124">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e727d-125">頂點</span><span class="sxs-lookup"><span data-stu-id="e727d-125">Vertex</span></span> | <span data-ttu-id="e727d-126">船體</span><span class="sxs-lookup"><span data-stu-id="e727d-126">Hull</span></span> | <span data-ttu-id="e727d-127">網域</span><span class="sxs-lookup"><span data-stu-id="e727d-127">Domain</span></span> | <span data-ttu-id="e727d-128">幾何</span><span class="sxs-lookup"><span data-stu-id="e727d-128">Geometry</span></span> | <span data-ttu-id="e727d-129">像素</span><span class="sxs-lookup"><span data-stu-id="e727d-129">Pixel</span></span> | <span data-ttu-id="e727d-130">計算</span><span class="sxs-lookup"><span data-stu-id="e727d-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e727d-131">x</span><span class="sxs-lookup"><span data-stu-id="e727d-131">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="e727d-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e727d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e727d-133">內建函式</span><span class="sxs-lookup"><span data-stu-id="e727d-133">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="e727d-134">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="e727d-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




