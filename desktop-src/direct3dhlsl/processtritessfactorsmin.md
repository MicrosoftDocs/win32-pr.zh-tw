---
title: ProcessTriTessFactorsMin 函式
description: 產生三個修補程式的已更正鑲嵌因數。 |ProcessTriTessFactorsMin 函式
ms.assetid: fa1e19c2-fadf-42d4-9574-834eaf871393
keywords:
- ProcessTriTessFactorsMin 函式 HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f82c7935d47813d833ccc21a7ec0134adee1cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514425"
---
# <a name="processtritessfactorsmin-function"></a><span data-ttu-id="8f60d-105">ProcessTriTessFactorsMin 函式</span><span class="sxs-lookup"><span data-stu-id="8f60d-105">ProcessTriTessFactorsMin function</span></span>

<span data-ttu-id="8f60d-106">產生三個修補程式的已更正鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="8f60d-106">Generates the corrected tessellation factors for a tri patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f60d-107">語法</span><span class="sxs-lookup"><span data-stu-id="8f60d-107">Syntax</span></span>

``` syntax
void ProcessTriTessFactorsMin(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactors,
  out float UnroundedInsideTessFactors
);
```

## <a name="parameters"></a><span data-ttu-id="8f60d-108">參數</span><span class="sxs-lookup"><span data-stu-id="8f60d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f60d-109">*RawEdgeFactors* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f60d-109">*RawEdgeFactors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f60d-110">類型： **float3**</span><span class="sxs-lookup"><span data-stu-id="8f60d-110">Type: **float3**</span></span>

<span data-ttu-id="8f60d-111">傳遞至鑲嵌階段的邊緣鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="8f60d-111">The edge tessellation factors, passed into the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="8f60d-112">*InsideScale* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f60d-112">*InsideScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f60d-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="8f60d-113">Type: **float**</span></span>

<span data-ttu-id="8f60d-114">調整因數會套用至鑲嵌式階段所計算的 UV 鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="8f60d-114">The scale factor applied to the UV tessellation factors computed by the tessellation stage.</span></span> <span data-ttu-id="8f60d-115">InsideScale 的允許範圍是0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="8f60d-115">The allowable range for InsideScale is 0.0 to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="8f60d-116">*RoundedEdgeTessFactors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f60d-116">*RoundedEdgeTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f60d-117">類型： **float3**</span><span class="sxs-lookup"><span data-stu-id="8f60d-117">Type: **float3**</span></span>

<span data-ttu-id="8f60d-118">鑲嵌階段所計算的圓角邊緣鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="8f60d-118">The rounded edge-tessellation factors calculated by the tessellator stage.</span></span>

</dd> <dt>

<span data-ttu-id="8f60d-119">*RoundedInsideTessFactors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f60d-119">*RoundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f60d-120">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="8f60d-120">Type: **float**</span></span>

<span data-ttu-id="8f60d-121">鑲嵌階段針對內部邊緣計算的圓角鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="8f60d-121">The rounded tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> <dt>

<span data-ttu-id="8f60d-122">*UnroundedInsideTessFactors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f60d-122">*UnroundedInsideTessFactors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f60d-123">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="8f60d-123">Type: **float**</span></span>

<span data-ttu-id="8f60d-124">鑲嵌階段針對內部邊緣所計算的鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="8f60d-124">The tessellation factors calculated by the tessellator stage for inside edges.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f60d-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f60d-125">Return value</span></span>

<span data-ttu-id="8f60d-126">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8f60d-126">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f60d-127">備註</span><span class="sxs-lookup"><span data-stu-id="8f60d-127">Remarks</span></span>

<span data-ttu-id="8f60d-128">會產生三個修補程式的已更正鑲嵌因數，以最小的邊緣鑲嵌因數來計算內鑲嵌因數，然後以 InsideScale 進行調整。</span><span class="sxs-lookup"><span data-stu-id="8f60d-128">Generates the corrected tessellation factors for a tri patch, computing the inside tessellation factor as the minimum of the edge tessellation factors, which is then scaled by InsideScale.</span></span> <span data-ttu-id="8f60d-129">結果接著會根據資料分割模式舍入，但使用 UnroundedInsideTessFactor 參數可使用 unrounded 結果。</span><span class="sxs-lookup"><span data-stu-id="8f60d-129">The result is then rounded based on the partitioning mode, but the unrounded results are available using the UnroundedInsideTessFactor parameter.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="8f60d-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="8f60d-130">Minimum Shader Model</span></span>

<span data-ttu-id="8f60d-131">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="8f60d-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8f60d-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="8f60d-132">Shader Model</span></span>                                                                | <span data-ttu-id="8f60d-133">支援</span><span class="sxs-lookup"><span data-stu-id="8f60d-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8f60d-134">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="8f60d-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="8f60d-135">是</span><span class="sxs-lookup"><span data-stu-id="8f60d-135">yes</span></span>       |



 

<span data-ttu-id="8f60d-136">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="8f60d-136">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="8f60d-137">頂點</span><span class="sxs-lookup"><span data-stu-id="8f60d-137">Vertex</span></span> | <span data-ttu-id="8f60d-138">船體</span><span class="sxs-lookup"><span data-stu-id="8f60d-138">Hull</span></span> | <span data-ttu-id="8f60d-139">網域</span><span class="sxs-lookup"><span data-stu-id="8f60d-139">Domain</span></span> | <span data-ttu-id="8f60d-140">幾何</span><span class="sxs-lookup"><span data-stu-id="8f60d-140">Geometry</span></span> | <span data-ttu-id="8f60d-141">像素</span><span class="sxs-lookup"><span data-stu-id="8f60d-141">Pixel</span></span> | <span data-ttu-id="8f60d-142">計算</span><span class="sxs-lookup"><span data-stu-id="8f60d-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="8f60d-143">x</span><span class="sxs-lookup"><span data-stu-id="8f60d-143">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="8f60d-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f60d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f60d-145">內建函式</span><span class="sxs-lookup"><span data-stu-id="8f60d-145">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="8f60d-146">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="8f60d-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




