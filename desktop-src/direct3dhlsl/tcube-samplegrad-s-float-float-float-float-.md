---
title: SampleGrad：： SampleGrad (S，float，float，float，float) function for TextureCube
description: 使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。 針對 TextureCube
ms.assetid: C5BC71FA-63E3-4DE2-9202-B9C79789AE8E
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
ms.openlocfilehash: e4a51c49d9373dc210cbf216089e4c82835bf2c4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104514740"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="c2138-105">SampleGrad：： SampleGrad (S，float，float，float，float) function for TextureCube</span><span class="sxs-lookup"><span data-stu-id="c2138-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="c2138-106">使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="c2138-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2138-107">語法</span><span class="sxs-lookup"><span data-stu-id="c2138-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="c2138-108">參數</span><span class="sxs-lookup"><span data-stu-id="c2138-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2138-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="c2138-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2138-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="c2138-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c2138-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="c2138-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c2138-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="c2138-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c2138-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2138-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2138-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c2138-114">Type: **float**</span></span>

<span data-ttu-id="c2138-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="c2138-115">The texture coordinates.</span></span> <span data-ttu-id="c2138-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="c2138-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c2138-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="c2138-117">Texture-Object Type</span></span>                    | <span data-ttu-id="c2138-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="c2138-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c2138-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c2138-119">Texture1D</span></span>                              | <span data-ttu-id="c2138-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c2138-120">float</span></span>          |
| <span data-ttu-id="c2138-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="c2138-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c2138-122">float2</span><span class="sxs-lookup"><span data-stu-id="c2138-122">float2</span></span>         |
| <span data-ttu-id="c2138-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="c2138-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c2138-124">float3</span><span class="sxs-lookup"><span data-stu-id="c2138-124">float3</span></span>         |
| <span data-ttu-id="c2138-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c2138-125">TextureCubeArray</span></span>                       | <span data-ttu-id="c2138-126">float4</span><span class="sxs-lookup"><span data-stu-id="c2138-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c2138-127"> \[ 中的 DDX\]</span><span class="sxs-lookup"><span data-stu-id="c2138-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2138-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c2138-128">Type: **float**</span></span>

<span data-ttu-id="c2138-129">以 x 方向呈現的表面幾何變化率。</span><span class="sxs-lookup"><span data-stu-id="c2138-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="c2138-130">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="c2138-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c2138-131">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="c2138-131">Texture-Object Type</span></span>                      | <span data-ttu-id="c2138-132">參數類型</span><span class="sxs-lookup"><span data-stu-id="c2138-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="c2138-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c2138-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="c2138-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c2138-134">float</span></span>          |
| <span data-ttu-id="c2138-135">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c2138-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="c2138-136">float2</span><span class="sxs-lookup"><span data-stu-id="c2138-136">float2</span></span>         |
| <span data-ttu-id="c2138-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c2138-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c2138-138">float3</span><span class="sxs-lookup"><span data-stu-id="c2138-138">float3</span></span>         |
| <span data-ttu-id="c2138-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c2138-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="c2138-140">不支援</span><span class="sxs-lookup"><span data-stu-id="c2138-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c2138-141">*DDY* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2138-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2138-142">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c2138-142">Type: **float**</span></span>

<span data-ttu-id="c2138-143">介面幾何在 y 方向的變化率。</span><span class="sxs-lookup"><span data-stu-id="c2138-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="c2138-144">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="c2138-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c2138-145">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="c2138-145">Texture-Object Type</span></span>                      | <span data-ttu-id="c2138-146">參數類型</span><span class="sxs-lookup"><span data-stu-id="c2138-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="c2138-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="c2138-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="c2138-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c2138-148">float</span></span>          |
| <span data-ttu-id="c2138-149">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="c2138-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="c2138-150">float2</span><span class="sxs-lookup"><span data-stu-id="c2138-150">float2</span></span>         |
| <span data-ttu-id="c2138-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c2138-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="c2138-152">float3</span><span class="sxs-lookup"><span data-stu-id="c2138-152">float3</span></span>         |
| <span data-ttu-id="c2138-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="c2138-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="c2138-154">不支援</span><span class="sxs-lookup"><span data-stu-id="c2138-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="c2138-155">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2138-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2138-156">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c2138-156">Type: **float**</span></span>

<span data-ttu-id="c2138-157">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="c2138-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="c2138-158">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="c2138-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2138-159">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2138-159">Return value</span></span>

<span data-ttu-id="c2138-160">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="c2138-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="c2138-161">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="c2138-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="c2138-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2138-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2138-163">SampleGrad 方法</span><span class="sxs-lookup"><span data-stu-id="c2138-163">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="c2138-164">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="c2138-164">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
