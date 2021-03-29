---
title: Texture1D 的 SampleCmp：： SampleCmp (S、float、float、int、float) 函數
description: 使用比較值來拒絕範例，並使用選擇性的值來將範例層級 (」 LOD) 值設為，以將材質取樣。 |Texture1D 的 SampleCmp：： SampleCmp (S、float、float、int、float) 函數
ms.assetid: 91AD0B59-D3F0-4A0D-8825-17282815D64B
keywords:
- SampleCmp 函式 HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 811636e7e7002afedf026d4e3955f08f647c2c5d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104992415"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="ae443-105">Texture1D 的 SampleCmp：： SampleCmp (S、float、float、int、float) 函數</span><span class="sxs-lookup"><span data-stu-id="ae443-105">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="ae443-106">使用比較值來拒絕範例，並使用選擇性的值來將範例層級 (」 LOD) 值設為，以將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="ae443-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae443-107">語法</span><span class="sxs-lookup"><span data-stu-id="ae443-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="ae443-108">參數</span><span class="sxs-lookup"><span data-stu-id="ae443-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae443-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="ae443-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae443-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="ae443-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ae443-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="ae443-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="ae443-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="ae443-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="ae443-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae443-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae443-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="ae443-114">Type: **float**</span></span>

<span data-ttu-id="ae443-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="ae443-115">The texture coordinates.</span></span> <span data-ttu-id="ae443-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="ae443-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="ae443-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="ae443-117">Texture-Object Type</span></span>                    | <span data-ttu-id="ae443-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="ae443-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="ae443-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ae443-119">Texture1D</span></span>                              | <span data-ttu-id="ae443-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ae443-120">float</span></span>          |
| <span data-ttu-id="ae443-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="ae443-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="ae443-122">float2</span><span class="sxs-lookup"><span data-stu-id="ae443-122">float2</span></span>         |
| <span data-ttu-id="ae443-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ae443-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="ae443-124">float3</span><span class="sxs-lookup"><span data-stu-id="ae443-124">float3</span></span>         |
| <span data-ttu-id="ae443-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ae443-125">TextureCubeArray</span></span>                       | <span data-ttu-id="ae443-126">float4</span><span class="sxs-lookup"><span data-stu-id="ae443-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="ae443-127">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae443-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae443-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="ae443-128">Type: **float**</span></span>

<span data-ttu-id="ae443-129">用來作為比較值的浮點值。</span><span class="sxs-lookup"><span data-stu-id="ae443-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="ae443-130">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae443-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae443-131">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="ae443-131">Type: **int**</span></span>

<span data-ttu-id="ae443-132">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="ae443-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="ae443-133">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="ae443-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="ae443-134">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="ae443-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ae443-135">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="ae443-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="ae443-136">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="ae443-136">Texture-Object Type</span></span>           | <span data-ttu-id="ae443-137">參數類型</span><span class="sxs-lookup"><span data-stu-id="ae443-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="ae443-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ae443-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="ae443-139">int</span><span class="sxs-lookup"><span data-stu-id="ae443-139">int</span></span>            |
| <span data-ttu-id="ae443-140">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ae443-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="ae443-141">int2</span><span class="sxs-lookup"><span data-stu-id="ae443-141">int2</span></span>           |
| <span data-ttu-id="ae443-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ae443-142">Texture3D</span></span>                     | <span data-ttu-id="ae443-143">int3</span><span class="sxs-lookup"><span data-stu-id="ae443-143">int3</span></span>           |
| <span data-ttu-id="ae443-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ae443-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="ae443-145">不支援</span><span class="sxs-lookup"><span data-stu-id="ae443-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="ae443-146">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae443-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae443-147">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="ae443-147">Type: **float**</span></span>

<span data-ttu-id="ae443-148">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="ae443-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="ae443-149">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="ae443-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae443-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae443-150">Return value</span></span>

<span data-ttu-id="ae443-151">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="ae443-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="ae443-152">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="ae443-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="ae443-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae443-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae443-154">SampleCmp 方法</span><span class="sxs-lookup"><span data-stu-id="ae443-154">SampleCmp methods</span></span>](texture1d-samplecmp.md)
</dt> </dl>

 

 
