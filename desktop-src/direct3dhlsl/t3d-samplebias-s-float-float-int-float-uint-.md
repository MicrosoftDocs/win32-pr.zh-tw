---
title: Texture3D 的 SampleBias：： SampleBias (S、float、float、int、float、uint) 函數
description: 將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。 |Texture3D 的 SampleBias：： SampleBias (S、float、float、int、float、uint) 函數
ms.assetid: 87B06414-F1A3-4BC8-B7DE-137B2156CFA7
keywords:
- SampleBias 函式 HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6155bbd4a3b21b86add57d13bc14a1185c76b73
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104974738"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture3d"></a><span data-ttu-id="48c3f-105">Texture3D 的 SampleBias：： SampleBias (S、float、float、int、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="48c3f-105">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture3D</span></span>

<span data-ttu-id="48c3f-106">將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。</span><span class="sxs-lookup"><span data-stu-id="48c3f-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="48c3f-107">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="48c3f-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="48c3f-108">語法</span><span class="sxs-lookup"><span data-stu-id="48c3f-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="48c3f-109">參數</span><span class="sxs-lookup"><span data-stu-id="48c3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48c3f-110"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="48c3f-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c3f-111">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="48c3f-111">Type: **SamplerState**</span></span>

<span data-ttu-id="48c3f-112">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="48c3f-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="48c3f-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="48c3f-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="48c3f-114">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48c3f-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c3f-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="48c3f-115">Type: **float**</span></span>

<span data-ttu-id="48c3f-116">材質座標。</span><span class="sxs-lookup"><span data-stu-id="48c3f-116">The texture coordinates.</span></span> <span data-ttu-id="48c3f-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="48c3f-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="48c3f-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="48c3f-118">Texture-Object Type</span></span>                    | <span data-ttu-id="48c3f-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="48c3f-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="48c3f-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="48c3f-120">Texture1D</span></span>                              | <span data-ttu-id="48c3f-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="48c3f-121">float</span></span>          |
| <span data-ttu-id="48c3f-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="48c3f-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="48c3f-123">float2</span><span class="sxs-lookup"><span data-stu-id="48c3f-123">float2</span></span>         |
| <span data-ttu-id="48c3f-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="48c3f-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="48c3f-125">float3</span><span class="sxs-lookup"><span data-stu-id="48c3f-125">float3</span></span>         |
| <span data-ttu-id="48c3f-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="48c3f-126">TextureCubeArray</span></span>                       | <span data-ttu-id="48c3f-127">float4</span><span class="sxs-lookup"><span data-stu-id="48c3f-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="48c3f-128">*偏差* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48c3f-128">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c3f-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="48c3f-129">Type: **float**</span></span>

<span data-ttu-id="48c3f-130">偏差值（介於0.0 到1.0 （含）之間的浮點數）會在取樣之前套用至 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="48c3f-130">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="48c3f-131">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48c3f-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c3f-132">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="48c3f-132">Type: **int**</span></span>

<span data-ttu-id="48c3f-133">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="48c3f-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="48c3f-134">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="48c3f-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="48c3f-135">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="48c3f-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="48c3f-136">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="48c3f-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="48c3f-137">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="48c3f-137">Texture-Object Type</span></span>           | <span data-ttu-id="48c3f-138">參數類型</span><span class="sxs-lookup"><span data-stu-id="48c3f-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="48c3f-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="48c3f-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="48c3f-140">int</span><span class="sxs-lookup"><span data-stu-id="48c3f-140">int</span></span>            |
| <span data-ttu-id="48c3f-141">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="48c3f-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="48c3f-142">int2</span><span class="sxs-lookup"><span data-stu-id="48c3f-142">int2</span></span>           |
| <span data-ttu-id="48c3f-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="48c3f-143">Texture3D</span></span>                     | <span data-ttu-id="48c3f-144">int3</span><span class="sxs-lookup"><span data-stu-id="48c3f-144">int3</span></span>           |
| <span data-ttu-id="48c3f-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="48c3f-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="48c3f-146">不支援</span><span class="sxs-lookup"><span data-stu-id="48c3f-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="48c3f-147">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48c3f-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c3f-148">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="48c3f-148">Type: **float**</span></span>

<span data-ttu-id="48c3f-149">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="48c3f-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="48c3f-150">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="48c3f-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="48c3f-151">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="48c3f-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48c3f-152">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="48c3f-152">Type: **uint**</span></span>

<span data-ttu-id="48c3f-153">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="48c3f-153">The status of the operation.</span></span> <span data-ttu-id="48c3f-154">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="48c3f-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="48c3f-155">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="48c3f-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="48c3f-156">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="48c3f-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48c3f-157">傳回值</span><span class="sxs-lookup"><span data-stu-id="48c3f-157">Return value</span></span>

<span data-ttu-id="48c3f-158">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="48c3f-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="48c3f-159">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="48c3f-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="48c3f-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48c3f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c3f-161">SampleBias 方法</span><span class="sxs-lookup"><span data-stu-id="48c3f-161">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="48c3f-162">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="48c3f-162">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
