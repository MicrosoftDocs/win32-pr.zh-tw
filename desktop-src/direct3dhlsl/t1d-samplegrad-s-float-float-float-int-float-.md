---
title: Texture1D 的 SampleGrad：： SampleGrad (S、float、float、float、int、float) 函數
description: 此函式會取樣材質、使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料層級 (」 LOD) 值為。
ms.assetid: 34A79CB6-0C45-40ED-845C-77C08F1DEC57
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
ms.openlocfilehash: 8c6222d8fa9548e3154abf7605fc5032dd67235a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104974757"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="fcbc8-104">Texture1D 的 SampleGrad：： SampleGrad (S、float、float、float、int、float) 函數</span><span class="sxs-lookup"><span data-stu-id="fcbc8-104">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="fcbc8-105">使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-105">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcbc8-106">語法</span><span class="sxs-lookup"><span data-stu-id="fcbc8-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="fcbc8-107">參數</span><span class="sxs-lookup"><span data-stu-id="fcbc8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcbc8-108"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="fcbc8-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbc8-109">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="fcbc8-109">Type: **SamplerState**</span></span>

<span data-ttu-id="fcbc8-110">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="fcbc8-111">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="fcbc8-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fcbc8-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbc8-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="fcbc8-113">Type: **float**</span></span>

<span data-ttu-id="fcbc8-114">材質座標。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-114">The texture coordinates.</span></span> <span data-ttu-id="fcbc8-115">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="fcbc8-116">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="fcbc8-116">Texture-Object Type</span></span>                    | <span data-ttu-id="fcbc8-117">參數類型</span><span class="sxs-lookup"><span data-stu-id="fcbc8-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="fcbc8-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fcbc8-118">Texture1D</span></span>                              | <span data-ttu-id="fcbc8-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="fcbc8-119">float</span></span>          |
| <span data-ttu-id="fcbc8-120">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="fcbc8-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="fcbc8-121">float2</span><span class="sxs-lookup"><span data-stu-id="fcbc8-121">float2</span></span>         |
| <span data-ttu-id="fcbc8-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="fcbc8-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="fcbc8-123">float3</span><span class="sxs-lookup"><span data-stu-id="fcbc8-123">float3</span></span>         |
| <span data-ttu-id="fcbc8-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fcbc8-124">TextureCubeArray</span></span>                       | <span data-ttu-id="fcbc8-125">float4</span><span class="sxs-lookup"><span data-stu-id="fcbc8-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="fcbc8-126"> \[ 中的 DDX\]</span><span class="sxs-lookup"><span data-stu-id="fcbc8-126">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbc8-127">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="fcbc8-127">Type: **float**</span></span>

<span data-ttu-id="fcbc8-128">以 x 方向呈現的表面幾何變化率。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-128">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="fcbc8-129">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-129">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="fcbc8-130">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="fcbc8-130">Texture-Object Type</span></span>                      | <span data-ttu-id="fcbc8-131">參數類型</span><span class="sxs-lookup"><span data-stu-id="fcbc8-131">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="fcbc8-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="fcbc8-132">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="fcbc8-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="fcbc8-133">float</span></span>          |
| <span data-ttu-id="fcbc8-134">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="fcbc8-134">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="fcbc8-135">float2</span><span class="sxs-lookup"><span data-stu-id="fcbc8-135">float2</span></span>         |
| <span data-ttu-id="fcbc8-136">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fcbc8-136">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="fcbc8-137">float3</span><span class="sxs-lookup"><span data-stu-id="fcbc8-137">float3</span></span>         |
| <span data-ttu-id="fcbc8-138">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="fcbc8-138">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="fcbc8-139">不支援</span><span class="sxs-lookup"><span data-stu-id="fcbc8-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="fcbc8-140">*DDY* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fcbc8-140">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbc8-141">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="fcbc8-141">Type: **float**</span></span>

<span data-ttu-id="fcbc8-142">介面幾何在 y 方向的變化率。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-142">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="fcbc8-143">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-143">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="fcbc8-144">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="fcbc8-144">Texture-Object Type</span></span>                      | <span data-ttu-id="fcbc8-145">參數類型</span><span class="sxs-lookup"><span data-stu-id="fcbc8-145">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="fcbc8-146">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="fcbc8-146">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="fcbc8-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="fcbc8-147">float</span></span>          |
| <span data-ttu-id="fcbc8-148">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="fcbc8-148">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="fcbc8-149">float2</span><span class="sxs-lookup"><span data-stu-id="fcbc8-149">float2</span></span>         |
| <span data-ttu-id="fcbc8-150">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fcbc8-150">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="fcbc8-151">float3</span><span class="sxs-lookup"><span data-stu-id="fcbc8-151">float3</span></span>         |
| <span data-ttu-id="fcbc8-152">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="fcbc8-152">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="fcbc8-153">不支援</span><span class="sxs-lookup"><span data-stu-id="fcbc8-153">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="fcbc8-154">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fcbc8-154">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbc8-155">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="fcbc8-155">Type: **int**</span></span>

<span data-ttu-id="fcbc8-156">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-156">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="fcbc8-157">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-157">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="fcbc8-158">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-158">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="fcbc8-159">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-159">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="fcbc8-160">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="fcbc8-160">Texture-Object Type</span></span>           | <span data-ttu-id="fcbc8-161">參數類型</span><span class="sxs-lookup"><span data-stu-id="fcbc8-161">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="fcbc8-162">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="fcbc8-162">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="fcbc8-163">int</span><span class="sxs-lookup"><span data-stu-id="fcbc8-163">int</span></span>            |
| <span data-ttu-id="fcbc8-164">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="fcbc8-164">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="fcbc8-165">int2</span><span class="sxs-lookup"><span data-stu-id="fcbc8-165">int2</span></span>           |
| <span data-ttu-id="fcbc8-166">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fcbc8-166">Texture3D</span></span>                     | <span data-ttu-id="fcbc8-167">int3</span><span class="sxs-lookup"><span data-stu-id="fcbc8-167">int3</span></span>           |
| <span data-ttu-id="fcbc8-168">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fcbc8-168">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="fcbc8-169">不支援</span><span class="sxs-lookup"><span data-stu-id="fcbc8-169">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="fcbc8-170">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fcbc8-170">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbc8-171">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="fcbc8-171">Type: **float**</span></span>

<span data-ttu-id="fcbc8-172">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-172">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="fcbc8-173">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-173">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcbc8-174">傳回值</span><span class="sxs-lookup"><span data-stu-id="fcbc8-174">Return value</span></span>

<span data-ttu-id="fcbc8-175">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="fcbc8-175">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="fcbc8-176">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="fcbc8-176">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="fcbc8-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fcbc8-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcbc8-178">SampleGrad 方法</span><span class="sxs-lookup"><span data-stu-id="fcbc8-178">SampleGrad methods</span></span>](texture1d-samplegrad.md)
</dt> </dl>

 

 
