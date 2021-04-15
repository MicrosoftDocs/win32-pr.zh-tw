---
title: Texture3D 的 SampleGrad：： SampleGrad (S、float、float、float、int、float、uint) 函數
description: 瞭解此函式如何取樣材質、使用漸層來影響範例位置的計算方式，以及選擇性的值來將範例詳細資料層級 (」 LOD) 值為。 適用于 Texture3D。
ms.assetid: 4B02A3B8-8179-497D-BF87-489BF0B9ECC2
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
ms.openlocfilehash: b80b6ddcc2eebecf02416b09256d714bd2b8772f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104974736"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture3d"></a><span data-ttu-id="e1aa6-105">Texture3D 的 SampleGrad：： SampleGrad (S、float、float、float、int、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="e1aa6-105">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture3D</span></span>

<span data-ttu-id="e1aa6-106">使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="e1aa6-107">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1aa6-108">語法</span><span class="sxs-lookup"><span data-stu-id="e1aa6-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="e1aa6-109">參數</span><span class="sxs-lookup"><span data-stu-id="e1aa6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1aa6-110"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="e1aa6-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1aa6-111">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="e1aa6-111">Type: **SamplerState**</span></span>

<span data-ttu-id="e1aa6-112">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e1aa6-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e1aa6-114">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e1aa6-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1aa6-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="e1aa6-115">Type: **float**</span></span>

<span data-ttu-id="e1aa6-116">材質座標。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-116">The texture coordinates.</span></span> <span data-ttu-id="e1aa6-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e1aa6-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="e1aa6-118">Texture-Object Type</span></span>                    | <span data-ttu-id="e1aa6-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="e1aa6-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e1aa6-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e1aa6-120">Texture1D</span></span>                              | <span data-ttu-id="e1aa6-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e1aa6-121">float</span></span>          |
| <span data-ttu-id="e1aa6-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="e1aa6-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e1aa6-123">float2</span><span class="sxs-lookup"><span data-stu-id="e1aa6-123">float2</span></span>         |
| <span data-ttu-id="e1aa6-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e1aa6-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e1aa6-125">float3</span><span class="sxs-lookup"><span data-stu-id="e1aa6-125">float3</span></span>         |
| <span data-ttu-id="e1aa6-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e1aa6-126">TextureCubeArray</span></span>                       | <span data-ttu-id="e1aa6-127">float4</span><span class="sxs-lookup"><span data-stu-id="e1aa6-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e1aa6-128"> \[ 中的 DDX\]</span><span class="sxs-lookup"><span data-stu-id="e1aa6-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1aa6-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="e1aa6-129">Type: **float**</span></span>

<span data-ttu-id="e1aa6-130">以 x 方向呈現的表面幾何變化率。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="e1aa6-131">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e1aa6-132">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="e1aa6-132">Texture-Object Type</span></span>                      | <span data-ttu-id="e1aa6-133">參數類型</span><span class="sxs-lookup"><span data-stu-id="e1aa6-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="e1aa6-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e1aa6-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="e1aa6-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e1aa6-135">float</span></span>          |
| <span data-ttu-id="e1aa6-136">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e1aa6-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="e1aa6-137">float2</span><span class="sxs-lookup"><span data-stu-id="e1aa6-137">float2</span></span>         |
| <span data-ttu-id="e1aa6-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e1aa6-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e1aa6-139">float3</span><span class="sxs-lookup"><span data-stu-id="e1aa6-139">float3</span></span>         |
| <span data-ttu-id="e1aa6-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e1aa6-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="e1aa6-141">不支援</span><span class="sxs-lookup"><span data-stu-id="e1aa6-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e1aa6-142">*DDY* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e1aa6-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1aa6-143">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="e1aa6-143">Type: **float**</span></span>

<span data-ttu-id="e1aa6-144">介面幾何在 y 方向的變化率。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="e1aa6-145">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e1aa6-146">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="e1aa6-146">Texture-Object Type</span></span>                      | <span data-ttu-id="e1aa6-147">參數類型</span><span class="sxs-lookup"><span data-stu-id="e1aa6-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="e1aa6-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e1aa6-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="e1aa6-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e1aa6-149">float</span></span>          |
| <span data-ttu-id="e1aa6-150">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e1aa6-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="e1aa6-151">float2</span><span class="sxs-lookup"><span data-stu-id="e1aa6-151">float2</span></span>         |
| <span data-ttu-id="e1aa6-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e1aa6-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e1aa6-153">float3</span><span class="sxs-lookup"><span data-stu-id="e1aa6-153">float3</span></span>         |
| <span data-ttu-id="e1aa6-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e1aa6-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="e1aa6-155">不支援</span><span class="sxs-lookup"><span data-stu-id="e1aa6-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e1aa6-156">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e1aa6-156">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1aa6-157">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="e1aa6-157">Type: **int**</span></span>

<span data-ttu-id="e1aa6-158">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-158">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="e1aa6-159">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="e1aa6-160">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="e1aa6-161">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-161">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="e1aa6-162">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="e1aa6-162">Texture-Object Type</span></span>           | <span data-ttu-id="e1aa6-163">參數類型</span><span class="sxs-lookup"><span data-stu-id="e1aa6-163">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="e1aa6-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e1aa6-164">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="e1aa6-165">int</span><span class="sxs-lookup"><span data-stu-id="e1aa6-165">int</span></span>            |
| <span data-ttu-id="e1aa6-166">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e1aa6-166">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="e1aa6-167">int2</span><span class="sxs-lookup"><span data-stu-id="e1aa6-167">int2</span></span>           |
| <span data-ttu-id="e1aa6-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e1aa6-168">Texture3D</span></span>                     | <span data-ttu-id="e1aa6-169">int3</span><span class="sxs-lookup"><span data-stu-id="e1aa6-169">int3</span></span>           |
| <span data-ttu-id="e1aa6-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e1aa6-170">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e1aa6-171">不支援</span><span class="sxs-lookup"><span data-stu-id="e1aa6-171">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e1aa6-172">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e1aa6-172">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1aa6-173">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="e1aa6-173">Type: **float**</span></span>

<span data-ttu-id="e1aa6-174">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-174">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e1aa6-175">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-175">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="e1aa6-176">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e1aa6-176">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1aa6-177">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="e1aa6-177">Type: **uint**</span></span>

<span data-ttu-id="e1aa6-178">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-178">The status of the operation.</span></span> <span data-ttu-id="e1aa6-179">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-179">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e1aa6-180">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-180">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e1aa6-181">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-181">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1aa6-182">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1aa6-182">Return value</span></span>

<span data-ttu-id="e1aa6-183">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e1aa6-183">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e1aa6-184">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="e1aa6-184">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e1aa6-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1aa6-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1aa6-186">SampleGrad 方法</span><span class="sxs-lookup"><span data-stu-id="e1aa6-186">SampleGrad methods</span></span>](texture3d-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="e1aa6-187">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="e1aa6-187">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
