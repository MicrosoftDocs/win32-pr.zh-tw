---
title: ProcessQuadTessFactorsMin 函式
description: 產生四個修補程式的已更正鑲嵌因數。 |ProcessQuadTessFactorsMin 函式
ms.assetid: 19cbd807-e379-4ee3-beba-55e35e4bcbcf
keywords:
- ProcessQuadTessFactorsMin 函式 HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 57eff10af1bf53b2a659cde6b7e036b5391c3ea6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973949"
---
# <a name="processquadtessfactorsmin-function"></a><span data-ttu-id="2520d-105">ProcessQuadTessFactorsMin 函式</span><span class="sxs-lookup"><span data-stu-id="2520d-105">ProcessQuadTessFactorsMin function</span></span>

<span data-ttu-id="2520d-106">產生四個修補程式的已更正鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="2520d-106">Generates the corrected tessellation factors for a quad patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="2520d-107">語法</span><span class="sxs-lookup"><span data-stu-id="2520d-107">Syntax</span></span>

``` syntax
void ProcessQuadTessFactorsMin(
  in  float4 RawEdgeFactors,
  in  float InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="2520d-108">參數</span><span class="sxs-lookup"><span data-stu-id="2520d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2520d-109">*RawEdgeFactors* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2520d-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2520d-110">類型： **float4**</span><span class="sxs-lookup"><span data-stu-id="2520d-110">Type: **float4**</span></span>

<span data-ttu-id="2520d-111">傳遞至鑲嵌階段的邊緣鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="2520d-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="2520d-112">*InsideScale* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2520d-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2520d-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="2520d-113">Type: **float**</span></span>

<span data-ttu-id="2520d-114">調整因數會套用至鑲嵌式階段所計算的 UV 鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="2520d-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="2520d-115">InsideScale 的允許範圍是0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="2520d-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="2520d-116">*RoundedEdgeTessFactors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2520d-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2520d-117">類型： **float4**</span><span class="sxs-lookup"><span data-stu-id="2520d-117">Type: **float4**</span></span>

<span data-ttu-id="2520d-118">鑲嵌階段所計算的圓角邊緣鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="2520d-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="2520d-119">*RoundedInsideTessFactors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2520d-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2520d-120">類型： **float2**</span><span class="sxs-lookup"><span data-stu-id="2520d-120">Type: **float2**</span></span>

<span data-ttu-id="2520d-121">鑲嵌階段針對內部邊緣計算的圓角鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="2520d-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="2520d-122">*UnroundedInsideTessFactors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2520d-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2520d-123">類型： **float2**</span><span class="sxs-lookup"><span data-stu-id="2520d-123">Type: **float2**</span></span>

<span data-ttu-id="2520d-124">鑲嵌階段針對內部邊緣所計算的鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="2520d-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2520d-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="2520d-125">Return value</span></span>

<span data-ttu-id="2520d-126">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2520d-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2520d-127">備註</span><span class="sxs-lookup"><span data-stu-id="2520d-127">Remarks</span></span>

<span data-ttu-id="2520d-128">產生四個修補程式的已更正鑲嵌因數，以最小的邊緣鑲嵌因數來計算內鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="2520d-128">Generates the corrected tessellation factors for a quad patch, computing the inside tessellation factors as the minimum of the edge tessellation factors.</span></span> <span data-ttu-id="2520d-129">內部 tess 因數將會是相同的值，由 InsideScale 所調整的四個邊緣的最小值所決定。</span><span class="sxs-lookup"><span data-stu-id="2520d-129">The inside tess factors will be identical values determined by the minimum of all four edges scaled by InsideScale.</span></span> <span data-ttu-id="2520d-130">結果接著會根據資料分割模式舍入，但使用 UnroundedInsideTessFactors 參數可使用 unrounded 結果。</span><span class="sxs-lookup"><span data-stu-id="2520d-130">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactors parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="2520d-131">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="2520d-131">Minimum Shader Model</span></span>

<span data-ttu-id="2520d-132">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="2520d-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2520d-133">著色器模型</span><span class="sxs-lookup"><span data-stu-id="2520d-133">Shader Model</span></span>                                                                | <span data-ttu-id="2520d-134">支援</span><span class="sxs-lookup"><span data-stu-id="2520d-134">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2520d-135">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="2520d-135">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="2520d-136">是</span><span class="sxs-lookup"><span data-stu-id="2520d-136">yes</span></span>       |



 

<span data-ttu-id="2520d-137">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="2520d-137">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2520d-138">頂點</span><span class="sxs-lookup"><span data-stu-id="2520d-138">Vertex</span></span> | <span data-ttu-id="2520d-139">船體</span><span class="sxs-lookup"><span data-stu-id="2520d-139">Hull</span></span> | <span data-ttu-id="2520d-140">網域</span><span class="sxs-lookup"><span data-stu-id="2520d-140">Domain</span></span> | <span data-ttu-id="2520d-141">幾何</span><span class="sxs-lookup"><span data-stu-id="2520d-141">Geometry</span></span> | <span data-ttu-id="2520d-142">像素</span><span class="sxs-lookup"><span data-stu-id="2520d-142">Pixel</span></span> | <span data-ttu-id="2520d-143">計算</span><span class="sxs-lookup"><span data-stu-id="2520d-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="2520d-144">x</span><span class="sxs-lookup"><span data-stu-id="2520d-144">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="2520d-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2520d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2520d-146">內建函式</span><span class="sxs-lookup"><span data-stu-id="2520d-146">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="2520d-147">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="2520d-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




