---
title: Texture2D 的 SampleCmp：： SampleCmp (S、float、float、int、float) function) 函數
description: 此函式會使用比較值來拒絕範例，並使用選擇性的值來將範例層級 (」 LOD) 值設為，以進行 Texture2D 的取樣。
ms.assetid: 1B5E6559-2524-4557-8F43-7AF258C39FB2
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
ms.openlocfilehash: 9df6a84fff7c6988ed9333584a7196fa06ad30ec
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104974766"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2d"></a><span data-ttu-id="feac9-104">Texture2D 的 SampleCmp：： SampleCmp (S、float、float、int、float) 函數</span><span class="sxs-lookup"><span data-stu-id="feac9-104">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture2D</span></span>

<span data-ttu-id="feac9-105">使用比較值來拒絕範例以 [**Texture2D**](sm5-object-texture2d.md)範例，並使用選擇性的值來將範例詳細資料層級 (」 lod) 值到。</span><span class="sxs-lookup"><span data-stu-id="feac9-105">Samples a [**Texture2D**](sm5-object-texture2d.md), using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="feac9-106">語法</span><span class="sxs-lookup"><span data-stu-id="feac9-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="feac9-107">參數</span><span class="sxs-lookup"><span data-stu-id="feac9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feac9-108"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="feac9-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feac9-109">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="feac9-109">Type: **SamplerState**</span></span>

<span data-ttu-id="feac9-110">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="feac9-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="feac9-111">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="feac9-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="feac9-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="feac9-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feac9-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="feac9-113">Type: **float**</span></span>

<span data-ttu-id="feac9-114">材質座標。</span><span class="sxs-lookup"><span data-stu-id="feac9-114">The texture coordinates.</span></span> <span data-ttu-id="feac9-115">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="feac9-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="feac9-116">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="feac9-116">Texture-Object Type</span></span>                    | <span data-ttu-id="feac9-117">參數類型</span><span class="sxs-lookup"><span data-stu-id="feac9-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="feac9-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="feac9-118">Texture1D</span></span>                              | <span data-ttu-id="feac9-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="feac9-119">float</span></span>          |
| <span data-ttu-id="feac9-120">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="feac9-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="feac9-121">float2</span><span class="sxs-lookup"><span data-stu-id="feac9-121">float2</span></span>         |
| <span data-ttu-id="feac9-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="feac9-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="feac9-123">float3</span><span class="sxs-lookup"><span data-stu-id="feac9-123">float3</span></span>         |
| <span data-ttu-id="feac9-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="feac9-124">TextureCubeArray</span></span>                       | <span data-ttu-id="feac9-125">float4</span><span class="sxs-lookup"><span data-stu-id="feac9-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="feac9-126">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="feac9-126">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feac9-127">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="feac9-127">Type: **float**</span></span>

<span data-ttu-id="feac9-128">用來作為比較值的浮點值。</span><span class="sxs-lookup"><span data-stu-id="feac9-128">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="feac9-129">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="feac9-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feac9-130">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="feac9-130">Type: **int**</span></span>

<span data-ttu-id="feac9-131">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="feac9-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="feac9-132">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="feac9-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="feac9-133">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="feac9-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="feac9-134">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="feac9-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="feac9-135">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="feac9-135">Texture-Object Type</span></span>           | <span data-ttu-id="feac9-136">參數類型</span><span class="sxs-lookup"><span data-stu-id="feac9-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="feac9-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="feac9-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="feac9-138">int</span><span class="sxs-lookup"><span data-stu-id="feac9-138">int</span></span>            |
| <span data-ttu-id="feac9-139">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="feac9-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="feac9-140">int2</span><span class="sxs-lookup"><span data-stu-id="feac9-140">int2</span></span>           |
| <span data-ttu-id="feac9-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="feac9-141">Texture3D</span></span>                     | <span data-ttu-id="feac9-142">int3</span><span class="sxs-lookup"><span data-stu-id="feac9-142">int3</span></span>           |
| <span data-ttu-id="feac9-143">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="feac9-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="feac9-144">不支援</span><span class="sxs-lookup"><span data-stu-id="feac9-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="feac9-145">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="feac9-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feac9-146">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="feac9-146">Type: **float**</span></span>

<span data-ttu-id="feac9-147">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="feac9-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="feac9-148">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="feac9-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feac9-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="feac9-149">Return value</span></span>

<span data-ttu-id="feac9-150">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="feac9-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="feac9-151">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="feac9-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="feac9-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="feac9-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feac9-153">SampleCmp 方法</span><span class="sxs-lookup"><span data-stu-id="feac9-153">SampleCmp methods</span></span>](texture2d-samplecmp.md)
</dt> </dl>

 

 
