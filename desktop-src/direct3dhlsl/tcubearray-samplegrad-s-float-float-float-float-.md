---
title: SampleGrad：： SampleGrad (S，float，float，float，float) function for TextureCubeArray
description: 瞭解此函式如何使用漸層來取樣材質，以影響範例位置的計算方式。 適用于 TextureCubeArray。
ms.assetid: 0C7DC9AA-3F0A-47E4-852F-7AE25CF67EA3
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
ms.openlocfilehash: 5320f47a5ae4db5bd96232dfa0a1d55b54f29c25
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103696879"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="e6e6c-105">SampleGrad：： SampleGrad (S，float，float，float，float) function for TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e6e6c-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="e6e6c-106">使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="e6e6c-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e6c-107">語法</span><span class="sxs-lookup"><span data-stu-id="e6e6c-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="e6e6c-108">參數</span><span class="sxs-lookup"><span data-stu-id="e6e6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e6c-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="e6e6c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e6c-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="e6e6c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="e6e6c-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="e6e6c-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e6e6c-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="e6e6c-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e6e6c-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e6e6c-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e6c-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="e6e6c-114">Type: **float**</span></span>

<span data-ttu-id="e6e6c-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="e6e6c-115">The texture coordinates.</span></span> <span data-ttu-id="e6e6c-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="e6e6c-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e6e6c-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="e6e6c-117">Texture-Object Type</span></span>                    | <span data-ttu-id="e6e6c-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="e6e6c-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e6e6c-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e6e6c-119">Texture1D</span></span>                              | <span data-ttu-id="e6e6c-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e6e6c-120">float</span></span>          |
| <span data-ttu-id="e6e6c-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="e6e6c-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e6e6c-122">float2</span><span class="sxs-lookup"><span data-stu-id="e6e6c-122">float2</span></span>         |
| <span data-ttu-id="e6e6c-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e6e6c-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e6e6c-124">float3</span><span class="sxs-lookup"><span data-stu-id="e6e6c-124">float3</span></span>         |
| <span data-ttu-id="e6e6c-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e6e6c-125">TextureCubeArray</span></span>                       | <span data-ttu-id="e6e6c-126">float4</span><span class="sxs-lookup"><span data-stu-id="e6e6c-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e6e6c-127"> \[ 中的 DDX\]</span><span class="sxs-lookup"><span data-stu-id="e6e6c-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e6c-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="e6e6c-128">Type: **float**</span></span>

<span data-ttu-id="e6e6c-129">以 x 方向呈現的表面幾何變化率。</span><span class="sxs-lookup"><span data-stu-id="e6e6c-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="e6e6c-130">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="e6e6c-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e6e6c-131">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="e6e6c-131">Texture-Object Type</span></span>                      | <span data-ttu-id="e6e6c-132">參數類型</span><span class="sxs-lookup"><span data-stu-id="e6e6c-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="e6e6c-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e6e6c-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="e6e6c-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e6e6c-134">float</span></span>          |
| <span data-ttu-id="e6e6c-135">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e6e6c-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="e6e6c-136">float2</span><span class="sxs-lookup"><span data-stu-id="e6e6c-136">float2</span></span>         |
| <span data-ttu-id="e6e6c-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e6e6c-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e6e6c-138">float3</span><span class="sxs-lookup"><span data-stu-id="e6e6c-138">float3</span></span>         |
| <span data-ttu-id="e6e6c-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e6e6c-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="e6e6c-140">不支援</span><span class="sxs-lookup"><span data-stu-id="e6e6c-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e6e6c-141">*DDY* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e6e6c-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e6c-142">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="e6e6c-142">Type: **float**</span></span>

<span data-ttu-id="e6e6c-143">介面幾何在 y 方向的變化率。</span><span class="sxs-lookup"><span data-stu-id="e6e6c-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="e6e6c-144">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="e6e6c-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e6e6c-145">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="e6e6c-145">Texture-Object Type</span></span>                      | <span data-ttu-id="e6e6c-146">參數類型</span><span class="sxs-lookup"><span data-stu-id="e6e6c-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="e6e6c-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e6e6c-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="e6e6c-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e6e6c-148">float</span></span>          |
| <span data-ttu-id="e6e6c-149">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e6e6c-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="e6e6c-150">float2</span><span class="sxs-lookup"><span data-stu-id="e6e6c-150">float2</span></span>         |
| <span data-ttu-id="e6e6c-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e6e6c-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e6e6c-152">float3</span><span class="sxs-lookup"><span data-stu-id="e6e6c-152">float3</span></span>         |
| <span data-ttu-id="e6e6c-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e6e6c-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="e6e6c-154">不支援</span><span class="sxs-lookup"><span data-stu-id="e6e6c-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e6e6c-155">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e6e6c-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e6c-156">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="e6e6c-156">Type: **float**</span></span>

<span data-ttu-id="e6e6c-157">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="e6e6c-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e6e6c-158">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="e6e6c-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e6c-159">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6e6c-159">Return value</span></span>

<span data-ttu-id="e6e6c-160">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e6e6c-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e6e6c-161">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="e6e6c-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e6e6c-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6e6c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e6c-163">SampleGrad 方法</span><span class="sxs-lookup"><span data-stu-id="e6e6c-163">SampleGrad methods</span></span>](texturecubearray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="e6e6c-164">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="e6e6c-164">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
