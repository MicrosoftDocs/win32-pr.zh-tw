---
title: Texture3D 的 SampleBias：： SampleBias (S、float、float、int、float) 函數
description: 將偏差值套用至 mipmap 層級之後，Texture3D 範例的 SampleBias：： SampleBias (S、float、float、int、float) 函數。
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
ms.openlocfilehash: c7ef038a3faa4cb0a208e9a9d05de230d2b87231
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "107001639"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function-for-texture3d"></a><span data-ttu-id="fb3e0-104">Texture3D 的 SampleBias：： SampleBias (S、float、float、int、float) 函數</span><span class="sxs-lookup"><span data-stu-id="fb3e0-104">SampleBias::SampleBias(S,float,float,int,float) function for Texture3D</span></span>

<span data-ttu-id="fb3e0-105">將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3e0-106">語法</span><span class="sxs-lookup"><span data-stu-id="fb3e0-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="fb3e0-107">參數</span><span class="sxs-lookup"><span data-stu-id="fb3e0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb3e0-108"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="fb3e0-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3e0-109">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="fb3e0-109">Type: **SamplerState**</span></span>

<span data-ttu-id="fb3e0-110">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="fb3e0-111">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="fb3e0-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb3e0-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3e0-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="fb3e0-113">Type: **float**</span></span>

<span data-ttu-id="fb3e0-114">材質座標。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-114">The texture coordinates.</span></span> <span data-ttu-id="fb3e0-115">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="fb3e0-116">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="fb3e0-116">Texture-Object Type</span></span>                    | <span data-ttu-id="fb3e0-117">參數類型</span><span class="sxs-lookup"><span data-stu-id="fb3e0-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="fb3e0-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="fb3e0-118">Texture1D</span></span>                              | <span data-ttu-id="fb3e0-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="fb3e0-119">float</span></span>          |
| <span data-ttu-id="fb3e0-120">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="fb3e0-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="fb3e0-121">float2</span><span class="sxs-lookup"><span data-stu-id="fb3e0-121">float2</span></span>         |
| <span data-ttu-id="fb3e0-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="fb3e0-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="fb3e0-123">float3</span><span class="sxs-lookup"><span data-stu-id="fb3e0-123">float3</span></span>         |
| <span data-ttu-id="fb3e0-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fb3e0-124">TextureCubeArray</span></span>                       | <span data-ttu-id="fb3e0-125">float4</span><span class="sxs-lookup"><span data-stu-id="fb3e0-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="fb3e0-126">*偏差* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb3e0-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3e0-127">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="fb3e0-127">Type: **float**</span></span>

<span data-ttu-id="fb3e0-128">偏差值（介於0.0 到1.0 （含）之間的浮點數）會在取樣之前套用至 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fb3e0-129">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb3e0-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3e0-130">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="fb3e0-130">Type: **int**</span></span>

<span data-ttu-id="fb3e0-131">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="fb3e0-132">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="fb3e0-133">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="fb3e0-134">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="fb3e0-135">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="fb3e0-135">Texture-Object Type</span></span>           | <span data-ttu-id="fb3e0-136">參數類型</span><span class="sxs-lookup"><span data-stu-id="fb3e0-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="fb3e0-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="fb3e0-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="fb3e0-138">int</span><span class="sxs-lookup"><span data-stu-id="fb3e0-138">int</span></span>            |
| <span data-ttu-id="fb3e0-139">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="fb3e0-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="fb3e0-140">int2</span><span class="sxs-lookup"><span data-stu-id="fb3e0-140">int2</span></span>           |
| <span data-ttu-id="fb3e0-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="fb3e0-141">Texture3D</span></span>                     | <span data-ttu-id="fb3e0-142">int3</span><span class="sxs-lookup"><span data-stu-id="fb3e0-142">int3</span></span>           |
| <span data-ttu-id="fb3e0-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="fb3e0-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="fb3e0-144">不支援</span><span class="sxs-lookup"><span data-stu-id="fb3e0-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="fb3e0-145">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb3e0-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3e0-146">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="fb3e0-146">Type: **float**</span></span>

<span data-ttu-id="fb3e0-147">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="fb3e0-148">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb3e0-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb3e0-149">Return value</span></span>

<span data-ttu-id="fb3e0-150">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="fb3e0-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="fb3e0-151">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="fb3e0-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="fb3e0-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb3e0-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3e0-153">SampleBias 方法</span><span class="sxs-lookup"><span data-stu-id="fb3e0-153">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="fb3e0-154">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="fb3e0-154">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
