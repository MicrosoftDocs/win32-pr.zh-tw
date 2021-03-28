---
title: EvaluateAttributeAtCentroid 函式
description: 在圖元距心進行評估。
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- EvaluateAttributeAtCentroid 函式 HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee95c7f2f202dfd0065e5e9c30003cc46fd29281
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373080"
---
# <a name="evaluateattributeatcentroid-function"></a><span data-ttu-id="3f8d5-104">EvaluateAttributeAtCentroid 函式</span><span class="sxs-lookup"><span data-stu-id="3f8d5-104">EvaluateAttributeAtCentroid function</span></span>

<span data-ttu-id="3f8d5-105">在圖元距心進行評估。</span><span class="sxs-lookup"><span data-stu-id="3f8d5-105">Evaluates at the pixel centroid.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f8d5-106">語法</span><span class="sxs-lookup"><span data-stu-id="3f8d5-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a><span data-ttu-id="3f8d5-107">參數</span><span class="sxs-lookup"><span data-stu-id="3f8d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f8d5-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3f8d5-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f8d5-109">類型： **attrib 數值**</span><span class="sxs-lookup"><span data-stu-id="3f8d5-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="3f8d5-110">輸入值。</span><span class="sxs-lookup"><span data-stu-id="3f8d5-110">The input value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f8d5-111">備註</span><span class="sxs-lookup"><span data-stu-id="3f8d5-111">Remarks</span></span>

<span data-ttu-id="3f8d5-112">插補模式可以是 **線性** 或線性，而不是在變數上的 **\_ \_ 觀點** 。</span><span class="sxs-lookup"><span data-stu-id="3f8d5-112">Interpolation mode can be **linear** or **linear\_no\_perspective** on the variable.</span></span> <span data-ttu-id="3f8d5-113">會忽略 **距心** 或 **sample** 的使用。</span><span class="sxs-lookup"><span data-stu-id="3f8d5-113">Use of **centroid** or **sample** is ignored.</span></span> <span data-ttu-id="3f8d5-114">也允許具有常數插補的屬性，在此情況下，會忽略範例索引。</span><span class="sxs-lookup"><span data-stu-id="3f8d5-114">Attributes with constant interpolation are also allowed, in which case the sample index is ignored.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="3f8d5-115">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="3f8d5-115">Minimum Shader Model</span></span>

<span data-ttu-id="3f8d5-116">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="3f8d5-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3f8d5-117">著色器模型</span><span class="sxs-lookup"><span data-stu-id="3f8d5-117">Shader Model</span></span>                                                                | <span data-ttu-id="3f8d5-118">支援</span><span class="sxs-lookup"><span data-stu-id="3f8d5-118">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3f8d5-119">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="3f8d5-119">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="3f8d5-120">是</span><span class="sxs-lookup"><span data-stu-id="3f8d5-120">yes</span></span>       |



 

<span data-ttu-id="3f8d5-121">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="3f8d5-121">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="3f8d5-122">頂點</span><span class="sxs-lookup"><span data-stu-id="3f8d5-122">Vertex</span></span> | <span data-ttu-id="3f8d5-123">船體</span><span class="sxs-lookup"><span data-stu-id="3f8d5-123">Hull</span></span> | <span data-ttu-id="3f8d5-124">網域</span><span class="sxs-lookup"><span data-stu-id="3f8d5-124">Domain</span></span> | <span data-ttu-id="3f8d5-125">幾何</span><span class="sxs-lookup"><span data-stu-id="3f8d5-125">Geometry</span></span> | <span data-ttu-id="3f8d5-126">像素</span><span class="sxs-lookup"><span data-stu-id="3f8d5-126">Pixel</span></span> | <span data-ttu-id="3f8d5-127">計算</span><span class="sxs-lookup"><span data-stu-id="3f8d5-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3f8d5-128">x</span><span class="sxs-lookup"><span data-stu-id="3f8d5-128">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="3f8d5-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f8d5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f8d5-130">內建函式</span><span class="sxs-lookup"><span data-stu-id="3f8d5-130">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="3f8d5-131">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="3f8d5-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




