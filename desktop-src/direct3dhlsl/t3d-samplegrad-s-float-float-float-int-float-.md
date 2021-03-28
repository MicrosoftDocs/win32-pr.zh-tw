---
title: Texture3D 的 SampleGrad：： SampleGrad (S、float、float、float、int、float) 函數函數
description: 使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。 適用于 Texture3D。
ms.assetid: F59D54F8-CC9E-47F8-97DD-735C70939C07
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
ms.openlocfilehash: 6d0bd1c47a82784b2b96a93a7f43ecd158e4782a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104974751"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture3d"></a><span data-ttu-id="c174c-105">Texture3D 的 SampleGrad：： SampleGrad (S、float、float、float、int、float) 函數</span><span class="sxs-lookup"><span data-stu-id="c174c-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture3D</span></span>

<span data-ttu-id="c174c-106">使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="c174c-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="c174c-107">語法</span><span class="sxs-lookup"><span data-stu-id="c174c-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c174c-108">參數</span><span class="sxs-lookup"><span data-stu-id="c174c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c174c-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="c174c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c174c-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="c174c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c174c-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="c174c-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c174c-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="c174c-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c174c-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c174c-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c174c-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c174c-114">Type: **float**</span></span>

<span data-ttu-id="c174c-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="c174c-115">The texture coordinates.</span></span> <span data-ttu-id="c174c-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="c174c-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c174c-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="c174c-117">Texture-Object Type</span></span>                    | <span data-ttu-id="c174c-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="c174c-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c174c-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c174c-119">Texture1D</span></span>                              | <span data-ttu-id="c174c-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c174c-120">float</span></span>          |
| <span data-ttu-id="c174c-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="c174c-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c174c-122">float2</span><span class="sxs-lookup"><span data-stu-id="c174c-122">float2</span></span>         |
| <span data-ttu-id="c174c-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="c174c-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c174c-124">float3</span><span class="sxs-lookup"><span data-stu-id="c174c-124">float3</span></span>         |
| <span data-ttu-id="c174c-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c174c-125">TextureCubeArray</span></span>                       | <span data-ttu-id="c174c-126">float4</span><span class="sxs-lookup"><span data-stu-id="c174c-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c174c-127"> \[ 中的 DDX\]</span><span class="sxs-lookup"><span data-stu-id="c174c-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c174c-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c174c-128">Type: **float**</span></span>

<span data-ttu-id="c174c-129">以 x 方向呈現的表面幾何變化率。</span><span class="sxs-lookup"><span data-stu-id="c174c-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="c174c-130">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="c174c-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c174c-131">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="c174c-131">Texture-Object Type</span></span>                      | <span data-ttu-id="c174c-132">參數類型</span><span class="sxs-lookup"><span data-stu-id="c174c-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="c174c-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c174c-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="c174c-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c174c-134">float</span></span>          |
| <span data-ttu-id="c174c-135">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c174c-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="c174c-136">float2</span><span class="sxs-lookup"><span data-stu-id="c174c-136">float2</span></span>         |
| <span data-ttu-id="c174c-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c174c-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c174c-138">float3</span><span class="sxs-lookup"><span data-stu-id="c174c-138">float3</span></span>         |
| <span data-ttu-id="c174c-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c174c-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="c174c-140">不支援</span><span class="sxs-lookup"><span data-stu-id="c174c-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c174c-141">*DDY* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c174c-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c174c-142">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c174c-142">Type: **float**</span></span>

<span data-ttu-id="c174c-143">介面幾何在 y 方向的變化率。</span><span class="sxs-lookup"><span data-stu-id="c174c-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="c174c-144">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="c174c-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c174c-145">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="c174c-145">Texture-Object Type</span></span>                      | <span data-ttu-id="c174c-146">參數類型</span><span class="sxs-lookup"><span data-stu-id="c174c-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="c174c-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c174c-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="c174c-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c174c-148">float</span></span>          |
| <span data-ttu-id="c174c-149">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c174c-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="c174c-150">float2</span><span class="sxs-lookup"><span data-stu-id="c174c-150">float2</span></span>         |
| <span data-ttu-id="c174c-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c174c-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c174c-152">float3</span><span class="sxs-lookup"><span data-stu-id="c174c-152">float3</span></span>         |
| <span data-ttu-id="c174c-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c174c-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="c174c-154">不支援</span><span class="sxs-lookup"><span data-stu-id="c174c-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c174c-155">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c174c-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c174c-156">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="c174c-156">Type: **int**</span></span>

<span data-ttu-id="c174c-157">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="c174c-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="c174c-158">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="c174c-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="c174c-159">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="c174c-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="c174c-160">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="c174c-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="c174c-161">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="c174c-161">Texture-Object Type</span></span>           | <span data-ttu-id="c174c-162">參數類型</span><span class="sxs-lookup"><span data-stu-id="c174c-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="c174c-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c174c-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="c174c-164">int</span><span class="sxs-lookup"><span data-stu-id="c174c-164">int</span></span>            |
| <span data-ttu-id="c174c-165">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c174c-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="c174c-166">int2</span><span class="sxs-lookup"><span data-stu-id="c174c-166">int2</span></span>           |
| <span data-ttu-id="c174c-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="c174c-167">Texture3D</span></span>                     | <span data-ttu-id="c174c-168">int3</span><span class="sxs-lookup"><span data-stu-id="c174c-168">int3</span></span>           |
| <span data-ttu-id="c174c-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c174c-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c174c-170">不支援</span><span class="sxs-lookup"><span data-stu-id="c174c-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c174c-171">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c174c-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c174c-172">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c174c-172">Type: **float**</span></span>

<span data-ttu-id="c174c-173">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="c174c-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="c174c-174">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="c174c-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c174c-175">傳回值</span><span class="sxs-lookup"><span data-stu-id="c174c-175">Return value</span></span>

<span data-ttu-id="c174c-176">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="c174c-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="c174c-177">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="c174c-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="c174c-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c174c-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c174c-179">SampleGrad 方法</span><span class="sxs-lookup"><span data-stu-id="c174c-179">SampleGrad methods</span></span>](texture3d-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="c174c-180">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="c174c-180">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
