---
title: SampleBias：： SampleBias (S，float，float，int，float) 函數
description: 將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。 |SampleBias：： SampleBias (S，float，float，int，float) 函數
ms.assetid: C252F1D1-51F9-48E3-BD74-3B050E0E16E0
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
ms.openlocfilehash: 16cc939de3bffe32dd26380b05eb65afac05114d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973965"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function"></a><span data-ttu-id="df2bb-105">SampleBias：： SampleBias (S，float，float，int，float) 函數</span><span class="sxs-lookup"><span data-stu-id="df2bb-105">SampleBias::SampleBias(S,float,float,int,float) function</span></span>

<span data-ttu-id="df2bb-106">將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。</span><span class="sxs-lookup"><span data-stu-id="df2bb-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="df2bb-107">語法</span><span class="sxs-lookup"><span data-stu-id="df2bb-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="df2bb-108">參數</span><span class="sxs-lookup"><span data-stu-id="df2bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df2bb-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="df2bb-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df2bb-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="df2bb-110">Type: **SamplerState**</span></span>

<span data-ttu-id="df2bb-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="df2bb-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="df2bb-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="df2bb-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="df2bb-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df2bb-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df2bb-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="df2bb-114">Type: **float**</span></span>

<span data-ttu-id="df2bb-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="df2bb-115">The texture coordinates.</span></span> <span data-ttu-id="df2bb-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="df2bb-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="df2bb-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="df2bb-117">Texture-Object Type</span></span>                    | <span data-ttu-id="df2bb-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="df2bb-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="df2bb-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="df2bb-119">Texture1D</span></span>                              | <span data-ttu-id="df2bb-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="df2bb-120">float</span></span>          |
| <span data-ttu-id="df2bb-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="df2bb-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="df2bb-122">float2</span><span class="sxs-lookup"><span data-stu-id="df2bb-122">float2</span></span>         |
| <span data-ttu-id="df2bb-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="df2bb-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="df2bb-124">float3</span><span class="sxs-lookup"><span data-stu-id="df2bb-124">float3</span></span>         |
| <span data-ttu-id="df2bb-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="df2bb-125">TextureCubeArray</span></span>                       | <span data-ttu-id="df2bb-126">float4</span><span class="sxs-lookup"><span data-stu-id="df2bb-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="df2bb-127">*偏差* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df2bb-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df2bb-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="df2bb-128">Type: **float**</span></span>

<span data-ttu-id="df2bb-129">偏差值（介於0.0 到1.0 （含）之間的浮點數）會在取樣之前套用至 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="df2bb-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="df2bb-130">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df2bb-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df2bb-131">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="df2bb-131">Type: **int**</span></span>

<span data-ttu-id="df2bb-132">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="df2bb-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="df2bb-133">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="df2bb-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="df2bb-134">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="df2bb-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="df2bb-135">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="df2bb-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="df2bb-136">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="df2bb-136">Texture-Object Type</span></span>           | <span data-ttu-id="df2bb-137">參數類型</span><span class="sxs-lookup"><span data-stu-id="df2bb-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="df2bb-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="df2bb-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="df2bb-139">int</span><span class="sxs-lookup"><span data-stu-id="df2bb-139">int</span></span>            |
| <span data-ttu-id="df2bb-140">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="df2bb-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="df2bb-141">int2</span><span class="sxs-lookup"><span data-stu-id="df2bb-141">int2</span></span>           |
| <span data-ttu-id="df2bb-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="df2bb-142">Texture3D</span></span>                     | <span data-ttu-id="df2bb-143">int3</span><span class="sxs-lookup"><span data-stu-id="df2bb-143">int3</span></span>           |
| <span data-ttu-id="df2bb-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="df2bb-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="df2bb-145">不支援</span><span class="sxs-lookup"><span data-stu-id="df2bb-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="df2bb-146">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="df2bb-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df2bb-147">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="df2bb-147">Type: **float**</span></span>

<span data-ttu-id="df2bb-148">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="df2bb-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="df2bb-149">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="df2bb-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df2bb-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="df2bb-150">Return value</span></span>

<span data-ttu-id="df2bb-151">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="df2bb-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="df2bb-152">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="df2bb-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="df2bb-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df2bb-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df2bb-154">SampleBias 方法</span><span class="sxs-lookup"><span data-stu-id="df2bb-154">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="df2bb-155">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="df2bb-155">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
