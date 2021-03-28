---
title: Texture2D 的 SampleGrad：： SampleGrad (S、float、float、float、int、float) 函數
description: 範例 Texture2D，使用漸層來影響範例位置的計算方式，並使用選擇性的值來將範例詳細資料層級 (」 LOD) 值到。 適用于 Texture2D。
ms.assetid: 1216B02A-4F70-4804-9B04-37E83DFC1CE8
keywords:
- SampleGrad 函式 HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b309eb9bc0ce7cbd968be81fa05eee91ee577b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104992431"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture2d"></a><span data-ttu-id="5aca8-105">Texture2D 的 SampleGrad：： SampleGrad (S、float、float、float、int、float) 函數</span><span class="sxs-lookup"><span data-stu-id="5aca8-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture2D</span></span>

<span data-ttu-id="5aca8-106">範例 [**Texture2D**](sm5-object-texture2d.md)，使用漸層來影響範例位置的計算方式，並使用選擇性的值來將範例詳細資料層級 (」 lod) 值到。</span><span class="sxs-lookup"><span data-stu-id="5aca8-106">Samples a [**Texture2D**](sm5-object-texture2d.md), using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aca8-107">語法</span><span class="sxs-lookup"><span data-stu-id="5aca8-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="5aca8-108">參數</span><span class="sxs-lookup"><span data-stu-id="5aca8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aca8-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="5aca8-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aca8-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="5aca8-110">Type: **SamplerState**</span></span>

<span data-ttu-id="5aca8-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="5aca8-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="5aca8-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="5aca8-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="5aca8-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5aca8-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aca8-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="5aca8-114">Type: **float**</span></span>

<span data-ttu-id="5aca8-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="5aca8-115">The texture coordinates.</span></span> <span data-ttu-id="5aca8-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="5aca8-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5aca8-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="5aca8-117">Texture-Object Type</span></span>                    | <span data-ttu-id="5aca8-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="5aca8-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="5aca8-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5aca8-119">Texture1D</span></span>                              | <span data-ttu-id="5aca8-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5aca8-120">float</span></span>          |
| <span data-ttu-id="5aca8-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="5aca8-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="5aca8-122">float2</span><span class="sxs-lookup"><span data-stu-id="5aca8-122">float2</span></span>         |
| <span data-ttu-id="5aca8-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="5aca8-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="5aca8-124">float3</span><span class="sxs-lookup"><span data-stu-id="5aca8-124">float3</span></span>         |
| <span data-ttu-id="5aca8-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5aca8-125">TextureCubeArray</span></span>                       | <span data-ttu-id="5aca8-126">float4</span><span class="sxs-lookup"><span data-stu-id="5aca8-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="5aca8-127"> \[ 中的 DDX\]</span><span class="sxs-lookup"><span data-stu-id="5aca8-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aca8-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="5aca8-128">Type: **float**</span></span>

<span data-ttu-id="5aca8-129">以 x 方向呈現的表面幾何變化率。</span><span class="sxs-lookup"><span data-stu-id="5aca8-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="5aca8-130">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="5aca8-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5aca8-131">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="5aca8-131">Texture-Object Type</span></span>                      | <span data-ttu-id="5aca8-132">參數類型</span><span class="sxs-lookup"><span data-stu-id="5aca8-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="5aca8-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5aca8-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="5aca8-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5aca8-134">float</span></span>          |
| <span data-ttu-id="5aca8-135">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5aca8-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="5aca8-136">float2</span><span class="sxs-lookup"><span data-stu-id="5aca8-136">float2</span></span>         |
| <span data-ttu-id="5aca8-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5aca8-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="5aca8-138">float3</span><span class="sxs-lookup"><span data-stu-id="5aca8-138">float3</span></span>         |
| <span data-ttu-id="5aca8-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="5aca8-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="5aca8-140">不支援</span><span class="sxs-lookup"><span data-stu-id="5aca8-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="5aca8-141">*DDY* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5aca8-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aca8-142">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="5aca8-142">Type: **float**</span></span>

<span data-ttu-id="5aca8-143">介面幾何在 y 方向的變化率。</span><span class="sxs-lookup"><span data-stu-id="5aca8-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="5aca8-144">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="5aca8-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5aca8-145">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="5aca8-145">Texture-Object Type</span></span>                      | <span data-ttu-id="5aca8-146">參數類型</span><span class="sxs-lookup"><span data-stu-id="5aca8-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="5aca8-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5aca8-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="5aca8-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5aca8-148">float</span></span>          |
| <span data-ttu-id="5aca8-149">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5aca8-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="5aca8-150">float2</span><span class="sxs-lookup"><span data-stu-id="5aca8-150">float2</span></span>         |
| <span data-ttu-id="5aca8-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5aca8-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="5aca8-152">float3</span><span class="sxs-lookup"><span data-stu-id="5aca8-152">float3</span></span>         |
| <span data-ttu-id="5aca8-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="5aca8-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="5aca8-154">不支援</span><span class="sxs-lookup"><span data-stu-id="5aca8-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="5aca8-155">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5aca8-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aca8-156">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="5aca8-156">Type: **int**</span></span>

<span data-ttu-id="5aca8-157">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="5aca8-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="5aca8-158">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="5aca8-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="5aca8-159">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="5aca8-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="5aca8-160">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="5aca8-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="5aca8-161">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="5aca8-161">Texture-Object Type</span></span>           | <span data-ttu-id="5aca8-162">參數類型</span><span class="sxs-lookup"><span data-stu-id="5aca8-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="5aca8-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5aca8-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="5aca8-164">int</span><span class="sxs-lookup"><span data-stu-id="5aca8-164">int</span></span>            |
| <span data-ttu-id="5aca8-165">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5aca8-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="5aca8-166">int2</span><span class="sxs-lookup"><span data-stu-id="5aca8-166">int2</span></span>           |
| <span data-ttu-id="5aca8-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5aca8-167">Texture3D</span></span>                     | <span data-ttu-id="5aca8-168">int3</span><span class="sxs-lookup"><span data-stu-id="5aca8-168">int3</span></span>           |
| <span data-ttu-id="5aca8-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5aca8-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="5aca8-170">不支援</span><span class="sxs-lookup"><span data-stu-id="5aca8-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="5aca8-171">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5aca8-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aca8-172">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="5aca8-172">Type: **float**</span></span>

<span data-ttu-id="5aca8-173">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="5aca8-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="5aca8-174">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="5aca8-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aca8-175">傳回值</span><span class="sxs-lookup"><span data-stu-id="5aca8-175">Return value</span></span>

<span data-ttu-id="5aca8-176">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="5aca8-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="5aca8-177">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="5aca8-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="5aca8-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5aca8-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aca8-179">SampleGrad 方法</span><span class="sxs-lookup"><span data-stu-id="5aca8-179">SampleGrad methods</span></span>](texture2d-samplegrad.md)
</dt> </dl>

 

 
