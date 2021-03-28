---
title: ProcessTriTessFactorsMax 函式
description: 產生三個修補程式的已更正鑲嵌因數。 |ProcessTriTessFactorsMax 函式
ms.assetid: a24cc1a8-5e6e-4963-b36b-e2265475580e
keywords:
- ProcessTriTessFactorsMax 函式 HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b5c17fe1dd9f3457a4104178e61af3589ba9f72d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514428"
---
# <a name="processtritessfactorsmax-function"></a><span data-ttu-id="c9066-105">ProcessTriTessFactorsMax 函式</span><span class="sxs-lookup"><span data-stu-id="c9066-105">ProcessTriTessFactorsMax function</span></span>

<span data-ttu-id="c9066-106">產生三個修補程式的已更正鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="c9066-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9066-107">語法</span><span class="sxs-lookup"><span data-stu-id="c9066-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsMax(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a><span data-ttu-id="c9066-108">參數</span><span class="sxs-lookup"><span data-stu-id="c9066-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9066-109">*RawEdgeFactors* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9066-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9066-110">類型： **float3**</span><span class="sxs-lookup"><span data-stu-id="c9066-110">Type: **float3**</span></span>

<span data-ttu-id="c9066-111">傳遞至鑲嵌階段的邊緣鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="c9066-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="c9066-112">*InsideScale* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9066-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9066-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c9066-113">Type: **float**</span></span>

<span data-ttu-id="c9066-114">調整因數會套用至鑲嵌式階段所計算的 UV 鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="c9066-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="c9066-115">InsideScale 的允許範圍是0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="c9066-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="c9066-116">*RoundedEdgeTessFactors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c9066-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9066-117">類型： **float3**</span><span class="sxs-lookup"><span data-stu-id="c9066-117">Type: **float3**</span></span>

<span data-ttu-id="c9066-118">鑲嵌階段所計算的圓角邊緣鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="c9066-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="c9066-119">*RoundedInsideTessFactor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c9066-119">*RoundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9066-120">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c9066-120">Type: **float**</span></span>

<span data-ttu-id="c9066-121">鑲嵌階段所計算的鑲嵌因數，並且舍入。</span><span class="sxs-lookup"><span data-stu-id="c9066-121">The tessellation factors calculated by the tessellator stage, and rounded.</span></span>

</dd> <dt>

<span data-ttu-id="c9066-122">*UnroundedInsideTessFactor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c9066-122">*UnroundedInsideTessFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9066-123">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c9066-123">Type: **float**</span></span>

<span data-ttu-id="c9066-124">鑲嵌階段所計算的原始、unrounded、UV 鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="c9066-124">The original, unrounded, UV tessellation factors computed by the tessellation stage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9066-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9066-125">Return value</span></span>

<span data-ttu-id="c9066-126">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c9066-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9066-127">備註</span><span class="sxs-lookup"><span data-stu-id="c9066-127">Remarks</span></span>

<span data-ttu-id="c9066-128">會產生三個修補程式的已更正鑲嵌式因素，將內鑲嵌因數計算為邊緣鑲嵌因數的最大值，然後以 InsideScale 進行調整。</span><span class="sxs-lookup"><span data-stu-id="c9066-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the maximum of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="c9066-129">結果接著會根據資料分割模式舍入，但使用 UnroundedInsideTessFactor 參數可使用 unrounded 結果。</span><span class="sxs-lookup"><span data-stu-id="c9066-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="c9066-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="c9066-130">Minimum Shader Model</span></span>

<span data-ttu-id="c9066-131">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="c9066-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c9066-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="c9066-132">Shader Model</span></span>                                                                | <span data-ttu-id="c9066-133">支援</span><span class="sxs-lookup"><span data-stu-id="c9066-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c9066-134">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="c9066-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="c9066-135">是</span><span class="sxs-lookup"><span data-stu-id="c9066-135">yes</span></span>       |



 

<span data-ttu-id="c9066-136">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="c9066-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="c9066-137">頂點</span><span class="sxs-lookup"><span data-stu-id="c9066-137">Vertex</span></span> | <span data-ttu-id="c9066-138">船體</span><span class="sxs-lookup"><span data-stu-id="c9066-138">Hull</span></span> | <span data-ttu-id="c9066-139">網域</span><span class="sxs-lookup"><span data-stu-id="c9066-139">Domain</span></span> | <span data-ttu-id="c9066-140">幾何</span><span class="sxs-lookup"><span data-stu-id="c9066-140">Geometry</span></span> | <span data-ttu-id="c9066-141">像素</span><span class="sxs-lookup"><span data-stu-id="c9066-141">Pixel</span></span> | <span data-ttu-id="c9066-142">計算</span><span class="sxs-lookup"><span data-stu-id="c9066-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="c9066-143">x</span><span class="sxs-lookup"><span data-stu-id="c9066-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="c9066-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9066-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9066-145">內建函式</span><span class="sxs-lookup"><span data-stu-id="c9066-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="c9066-146">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="c9066-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




