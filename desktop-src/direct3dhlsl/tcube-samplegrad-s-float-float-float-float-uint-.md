---
title: TextureCube 的 SampleGrad：： SampleGrad (S、float、float、float、float、uint) 函數
description: 使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。 適用于 TextureCube。
ms.assetid: 36DF7846-416A-4F2F-A7F8-44EE768CDEE1
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
ms.openlocfilehash: 3e75bccaeac28aefc50620a5dea31fa62b880332
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104514721"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="14222-105">TextureCube 的 SampleGrad：： SampleGrad (S、float、float、float、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="14222-105">SampleGrad::SampleGrad(S,float,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="14222-106">使用漸層來影響範例位置的計算方式，並使用選擇性值來將範例詳細資料 (」 LOD) 值到，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="14222-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="14222-107">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="14222-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="14222-108">語法</span><span class="sxs-lookup"><span data-stu-id="14222-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="14222-109">參數</span><span class="sxs-lookup"><span data-stu-id="14222-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14222-110"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="14222-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14222-111">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="14222-111">Type: **SamplerState**</span></span>

<span data-ttu-id="14222-112">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="14222-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="14222-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="14222-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="14222-114">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14222-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14222-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="14222-115">Type: **float**</span></span>

<span data-ttu-id="14222-116">材質座標。</span><span class="sxs-lookup"><span data-stu-id="14222-116">The texture coordinates.</span></span> <span data-ttu-id="14222-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="14222-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="14222-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="14222-118">Texture-Object Type</span></span>                    | <span data-ttu-id="14222-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="14222-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="14222-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="14222-120">Texture1D</span></span>                              | <span data-ttu-id="14222-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="14222-121">float</span></span>          |
| <span data-ttu-id="14222-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="14222-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="14222-123">float2</span><span class="sxs-lookup"><span data-stu-id="14222-123">float2</span></span>         |
| <span data-ttu-id="14222-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="14222-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="14222-125">float3</span><span class="sxs-lookup"><span data-stu-id="14222-125">float3</span></span>         |
| <span data-ttu-id="14222-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="14222-126">TextureCubeArray</span></span>                       | <span data-ttu-id="14222-127">float4</span><span class="sxs-lookup"><span data-stu-id="14222-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="14222-128"> \[ 中的 DDX\]</span><span class="sxs-lookup"><span data-stu-id="14222-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14222-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="14222-129">Type: **float**</span></span>

<span data-ttu-id="14222-130">以 x 方向呈現的表面幾何變化率。</span><span class="sxs-lookup"><span data-stu-id="14222-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="14222-131">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="14222-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="14222-132">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="14222-132">Texture-Object Type</span></span>                      | <span data-ttu-id="14222-133">參數類型</span><span class="sxs-lookup"><span data-stu-id="14222-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="14222-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="14222-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="14222-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="14222-135">float</span></span>          |
| <span data-ttu-id="14222-136">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="14222-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="14222-137">float2</span><span class="sxs-lookup"><span data-stu-id="14222-137">float2</span></span>         |
| <span data-ttu-id="14222-138">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="14222-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="14222-139">float3</span><span class="sxs-lookup"><span data-stu-id="14222-139">float3</span></span>         |
| <span data-ttu-id="14222-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="14222-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="14222-141">不支援</span><span class="sxs-lookup"><span data-stu-id="14222-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="14222-142">*DDY* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14222-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14222-143">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="14222-143">Type: **float**</span></span>

<span data-ttu-id="14222-144">介面幾何在 y 方向的變化率。</span><span class="sxs-lookup"><span data-stu-id="14222-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="14222-145">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="14222-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="14222-146">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="14222-146">Texture-Object Type</span></span>                      | <span data-ttu-id="14222-147">參數類型</span><span class="sxs-lookup"><span data-stu-id="14222-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="14222-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="14222-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="14222-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="14222-149">float</span></span>          |
| <span data-ttu-id="14222-150">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="14222-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="14222-151">float2</span><span class="sxs-lookup"><span data-stu-id="14222-151">float2</span></span>         |
| <span data-ttu-id="14222-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="14222-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="14222-153">float3</span><span class="sxs-lookup"><span data-stu-id="14222-153">float3</span></span>         |
| <span data-ttu-id="14222-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="14222-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="14222-155">不支援</span><span class="sxs-lookup"><span data-stu-id="14222-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="14222-156">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14222-156">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14222-157">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="14222-157">Type: **float**</span></span>

<span data-ttu-id="14222-158">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="14222-158">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="14222-159">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="14222-159">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="14222-160">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="14222-160">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14222-161">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="14222-161">Type: **uint**</span></span>

<span data-ttu-id="14222-162">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="14222-162">The status of the operation.</span></span> <span data-ttu-id="14222-163">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="14222-163">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="14222-164">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="14222-164">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="14222-165">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="14222-165">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14222-166">傳回值</span><span class="sxs-lookup"><span data-stu-id="14222-166">Return value</span></span>

<span data-ttu-id="14222-167">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="14222-167">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="14222-168">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="14222-168">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="14222-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14222-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14222-170">SampleGrad 方法</span><span class="sxs-lookup"><span data-stu-id="14222-170">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="14222-171">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="14222-171">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
