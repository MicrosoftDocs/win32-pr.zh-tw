---
title: Texture2DArray 的 SampleGrad：： SampleGrad (S、float、float、float、int、float、uint) 函數
description: 瞭解此函式如何使用漸層來取樣材質，以影響範例位置的計算方式。 適用于 Texture2DArray。
ms.assetid: 71CC8747-8684-4ABD-8B7A-E02889048261
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
ms.openlocfilehash: 3d6c46deb14c3a2c3554052ecc3e6625b13b2848
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104992422"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture2darray"></a><span data-ttu-id="3cdde-105">Texture2DArray 的 SampleGrad：： SampleGrad (S、float、float、float、int、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="3cdde-105">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture2DArray</span></span>

<span data-ttu-id="3cdde-106">使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="3cdde-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="3cdde-107">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="3cdde-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cdde-108">語法</span><span class="sxs-lookup"><span data-stu-id="3cdde-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3cdde-109">參數</span><span class="sxs-lookup"><span data-stu-id="3cdde-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cdde-110"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="3cdde-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdde-111">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="3cdde-111">Type: **SamplerState**</span></span>

<span data-ttu-id="3cdde-112">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="3cdde-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3cdde-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="3cdde-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3cdde-114">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cdde-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdde-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="3cdde-115">Type: **float**</span></span>

<span data-ttu-id="3cdde-116">材質座標。</span><span class="sxs-lookup"><span data-stu-id="3cdde-116">The texture coordinates.</span></span> <span data-ttu-id="3cdde-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="3cdde-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3cdde-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="3cdde-118">Texture-Object Type</span></span>                    | <span data-ttu-id="3cdde-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="3cdde-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3cdde-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3cdde-120">Texture1D</span></span>                              | <span data-ttu-id="3cdde-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3cdde-121">float</span></span>          |
| <span data-ttu-id="3cdde-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="3cdde-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3cdde-123">float2</span><span class="sxs-lookup"><span data-stu-id="3cdde-123">float2</span></span>         |
| <span data-ttu-id="3cdde-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="3cdde-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3cdde-125">float3</span><span class="sxs-lookup"><span data-stu-id="3cdde-125">float3</span></span>         |
| <span data-ttu-id="3cdde-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3cdde-126">TextureCubeArray</span></span>                       | <span data-ttu-id="3cdde-127">float4</span><span class="sxs-lookup"><span data-stu-id="3cdde-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3cdde-128"> \[ 中的 DDX\]</span><span class="sxs-lookup"><span data-stu-id="3cdde-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdde-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="3cdde-129">Type: **float**</span></span>

<span data-ttu-id="3cdde-130">以 x 方向呈現的表面幾何變化率。</span><span class="sxs-lookup"><span data-stu-id="3cdde-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="3cdde-131">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="3cdde-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3cdde-132">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="3cdde-132">Texture-Object Type</span></span>                      | <span data-ttu-id="3cdde-133">參數類型</span><span class="sxs-lookup"><span data-stu-id="3cdde-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="3cdde-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3cdde-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="3cdde-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3cdde-135">float</span></span>          |
| <span data-ttu-id="3cdde-136">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3cdde-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="3cdde-137">float2</span><span class="sxs-lookup"><span data-stu-id="3cdde-137">float2</span></span>         |
| <span data-ttu-id="3cdde-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3cdde-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3cdde-139">float3</span><span class="sxs-lookup"><span data-stu-id="3cdde-139">float3</span></span>         |
| <span data-ttu-id="3cdde-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3cdde-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="3cdde-141">不支援</span><span class="sxs-lookup"><span data-stu-id="3cdde-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3cdde-142">*DDY* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cdde-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdde-143">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="3cdde-143">Type: **float**</span></span>

<span data-ttu-id="3cdde-144">介面幾何在 y 方向的變化率。</span><span class="sxs-lookup"><span data-stu-id="3cdde-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="3cdde-145">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="3cdde-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3cdde-146">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="3cdde-146">Texture-Object Type</span></span>                      | <span data-ttu-id="3cdde-147">參數類型</span><span class="sxs-lookup"><span data-stu-id="3cdde-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="3cdde-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3cdde-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="3cdde-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3cdde-149">float</span></span>          |
| <span data-ttu-id="3cdde-150">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3cdde-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="3cdde-151">float2</span><span class="sxs-lookup"><span data-stu-id="3cdde-151">float2</span></span>         |
| <span data-ttu-id="3cdde-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3cdde-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3cdde-153">float3</span><span class="sxs-lookup"><span data-stu-id="3cdde-153">float3</span></span>         |
| <span data-ttu-id="3cdde-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="3cdde-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="3cdde-155">不支援</span><span class="sxs-lookup"><span data-stu-id="3cdde-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3cdde-156">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cdde-156">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdde-157">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="3cdde-157">Type: **int**</span></span>

<span data-ttu-id="3cdde-158">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="3cdde-158">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="3cdde-159">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="3cdde-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="3cdde-160">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="3cdde-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="3cdde-161">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="3cdde-161">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="3cdde-162">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="3cdde-162">Texture-Object Type</span></span>           | <span data-ttu-id="3cdde-163">參數類型</span><span class="sxs-lookup"><span data-stu-id="3cdde-163">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="3cdde-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3cdde-164">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="3cdde-165">int</span><span class="sxs-lookup"><span data-stu-id="3cdde-165">int</span></span>            |
| <span data-ttu-id="3cdde-166">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3cdde-166">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="3cdde-167">int2</span><span class="sxs-lookup"><span data-stu-id="3cdde-167">int2</span></span>           |
| <span data-ttu-id="3cdde-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3cdde-168">Texture3D</span></span>                     | <span data-ttu-id="3cdde-169">int3</span><span class="sxs-lookup"><span data-stu-id="3cdde-169">int3</span></span>           |
| <span data-ttu-id="3cdde-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3cdde-170">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3cdde-171">不支援</span><span class="sxs-lookup"><span data-stu-id="3cdde-171">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3cdde-172">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cdde-172">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdde-173">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="3cdde-173">Type: **float**</span></span>

<span data-ttu-id="3cdde-174">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="3cdde-174">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="3cdde-175">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="3cdde-175">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="3cdde-176">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3cdde-176">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdde-177">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="3cdde-177">Type: **uint**</span></span>

<span data-ttu-id="3cdde-178">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="3cdde-178">The status of the operation.</span></span> <span data-ttu-id="3cdde-179">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="3cdde-179">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3cdde-180">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="3cdde-180">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3cdde-181">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3cdde-181">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cdde-182">傳回值</span><span class="sxs-lookup"><span data-stu-id="3cdde-182">Return value</span></span>

<span data-ttu-id="3cdde-183">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3cdde-183">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3cdde-184">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="3cdde-184">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3cdde-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cdde-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cdde-186">SampleGrad 方法</span><span class="sxs-lookup"><span data-stu-id="3cdde-186">SampleGrad methods</span></span>](texture2darray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="3cdde-187">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="3cdde-187">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
