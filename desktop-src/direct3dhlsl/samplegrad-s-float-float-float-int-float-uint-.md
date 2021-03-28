---
title: Texture2D 的 SampleGrad：： SampleGrad (S、float、float、float、int、float、uint) 函數
description: 範例 Texture2D，使用漸層來影響範例位置的計算方式，並使用選擇性的值來將範例詳細資料層級 (」 LOD) 值到。
ms.assetid: 896497E1-A795-4674-AB41-2440A7D0CC76
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
ms.openlocfilehash: 9f1909c792863a3b480b6bdec553db58f7ff8492
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104992430"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture2d"></a><span data-ttu-id="b23cd-104">Texture2D 的 SampleGrad：： SampleGrad (S、float、float、float、int、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="b23cd-104">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture2D</span></span>

<span data-ttu-id="b23cd-105">範例 [**Texture2D**](sm5-object-texture2d.md)，使用漸層來影響範例位置的計算方式，並使用選擇性的值來將範例詳細資料層級 (」 lod) 值到。</span><span class="sxs-lookup"><span data-stu-id="b23cd-105">Samples a [**Texture2D**](sm5-object-texture2d.md), using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="b23cd-106">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="b23cd-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b23cd-107">語法</span><span class="sxs-lookup"><span data-stu-id="b23cd-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b23cd-108">參數</span><span class="sxs-lookup"><span data-stu-id="b23cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b23cd-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="b23cd-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cd-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="b23cd-110">Type: **SamplerState**</span></span>

<span data-ttu-id="b23cd-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="b23cd-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="b23cd-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="b23cd-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="b23cd-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b23cd-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cd-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="b23cd-114">Type: **float**</span></span>

<span data-ttu-id="b23cd-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="b23cd-115">The texture coordinates.</span></span> <span data-ttu-id="b23cd-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="b23cd-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b23cd-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="b23cd-117">Texture-Object Type</span></span>                    | <span data-ttu-id="b23cd-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="b23cd-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="b23cd-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b23cd-119">Texture1D</span></span>                              | <span data-ttu-id="b23cd-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b23cd-120">float</span></span>          |
| <span data-ttu-id="b23cd-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="b23cd-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="b23cd-122">float2</span><span class="sxs-lookup"><span data-stu-id="b23cd-122">float2</span></span>         |
| <span data-ttu-id="b23cd-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="b23cd-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="b23cd-124">float3</span><span class="sxs-lookup"><span data-stu-id="b23cd-124">float3</span></span>         |
| <span data-ttu-id="b23cd-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b23cd-125">TextureCubeArray</span></span>                       | <span data-ttu-id="b23cd-126">float4</span><span class="sxs-lookup"><span data-stu-id="b23cd-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="b23cd-127"> \[ 中的 DDX\]</span><span class="sxs-lookup"><span data-stu-id="b23cd-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cd-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="b23cd-128">Type: **float**</span></span>

<span data-ttu-id="b23cd-129">以 x 方向呈現的表面幾何變化率。</span><span class="sxs-lookup"><span data-stu-id="b23cd-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="b23cd-130">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="b23cd-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b23cd-131">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="b23cd-131">Texture-Object Type</span></span>                      | <span data-ttu-id="b23cd-132">參數類型</span><span class="sxs-lookup"><span data-stu-id="b23cd-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="b23cd-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b23cd-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="b23cd-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b23cd-134">float</span></span>          |
| <span data-ttu-id="b23cd-135">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b23cd-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="b23cd-136">float2</span><span class="sxs-lookup"><span data-stu-id="b23cd-136">float2</span></span>         |
| <span data-ttu-id="b23cd-137">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b23cd-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="b23cd-138">float3</span><span class="sxs-lookup"><span data-stu-id="b23cd-138">float3</span></span>         |
| <span data-ttu-id="b23cd-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="b23cd-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="b23cd-140">不支援</span><span class="sxs-lookup"><span data-stu-id="b23cd-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b23cd-141">*DDY* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b23cd-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cd-142">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="b23cd-142">Type: **float**</span></span>

<span data-ttu-id="b23cd-143">介面幾何在 y 方向的變化率。</span><span class="sxs-lookup"><span data-stu-id="b23cd-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="b23cd-144">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="b23cd-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b23cd-145">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="b23cd-145">Texture-Object Type</span></span>                      | <span data-ttu-id="b23cd-146">參數類型</span><span class="sxs-lookup"><span data-stu-id="b23cd-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="b23cd-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b23cd-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="b23cd-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b23cd-148">float</span></span>          |
| <span data-ttu-id="b23cd-149">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b23cd-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="b23cd-150">float2</span><span class="sxs-lookup"><span data-stu-id="b23cd-150">float2</span></span>         |
| <span data-ttu-id="b23cd-151">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b23cd-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="b23cd-152">float3</span><span class="sxs-lookup"><span data-stu-id="b23cd-152">float3</span></span>         |
| <span data-ttu-id="b23cd-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="b23cd-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="b23cd-154">不支援</span><span class="sxs-lookup"><span data-stu-id="b23cd-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b23cd-155">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b23cd-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cd-156">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="b23cd-156">Type: **int**</span></span>

<span data-ttu-id="b23cd-157">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="b23cd-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="b23cd-158">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="b23cd-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="b23cd-159">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="b23cd-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="b23cd-160">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="b23cd-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="b23cd-161">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="b23cd-161">Texture-Object Type</span></span>           | <span data-ttu-id="b23cd-162">參數類型</span><span class="sxs-lookup"><span data-stu-id="b23cd-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="b23cd-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b23cd-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="b23cd-164">int</span><span class="sxs-lookup"><span data-stu-id="b23cd-164">int</span></span>            |
| <span data-ttu-id="b23cd-165">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b23cd-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="b23cd-166">int2</span><span class="sxs-lookup"><span data-stu-id="b23cd-166">int2</span></span>           |
| <span data-ttu-id="b23cd-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b23cd-167">Texture3D</span></span>                     | <span data-ttu-id="b23cd-168">int3</span><span class="sxs-lookup"><span data-stu-id="b23cd-168">int3</span></span>           |
| <span data-ttu-id="b23cd-169">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b23cd-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="b23cd-170">不支援</span><span class="sxs-lookup"><span data-stu-id="b23cd-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="b23cd-171">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b23cd-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cd-172">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="b23cd-172">Type: **float**</span></span>

<span data-ttu-id="b23cd-173">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="b23cd-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="b23cd-174">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="b23cd-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="b23cd-175">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b23cd-175">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cd-176">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="b23cd-176">Type: **uint**</span></span>

<span data-ttu-id="b23cd-177">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="b23cd-177">The status of the operation.</span></span> <span data-ttu-id="b23cd-178">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="b23cd-178">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="b23cd-179">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="b23cd-179">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="b23cd-180">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b23cd-180">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b23cd-181">傳回值</span><span class="sxs-lookup"><span data-stu-id="b23cd-181">Return value</span></span>

<span data-ttu-id="b23cd-182">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="b23cd-182">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="b23cd-183">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="b23cd-183">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="b23cd-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b23cd-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b23cd-185">SampleGrad 方法</span><span class="sxs-lookup"><span data-stu-id="b23cd-185">SampleGrad methods</span></span>](texture2d-samplegrad.md)
</dt> </dl>

 

 
