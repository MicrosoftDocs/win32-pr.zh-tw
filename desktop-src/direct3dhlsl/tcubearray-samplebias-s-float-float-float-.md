---
title: SampleBias：： SampleBias (S，float，float，float) 函數
description: 將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。 |SampleBias：： SampleBias (S，float，float，float) 函數
ms.assetid: 6683F115-4F81-4C24-B735-67DB4B52455B
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
ms.openlocfilehash: 8d95a1b0341e61853a20d313a04d1cde64dde66d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104116113"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function"></a><span data-ttu-id="b41d0-105">SampleBias：： SampleBias (S，float，float，float) 函數</span><span class="sxs-lookup"><span data-stu-id="b41d0-105">SampleBias::SampleBias(S,float,float,float) function</span></span>

<span data-ttu-id="b41d0-106">將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。</span><span class="sxs-lookup"><span data-stu-id="b41d0-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="b41d0-107">語法</span><span class="sxs-lookup"><span data-stu-id="b41d0-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="b41d0-108">參數</span><span class="sxs-lookup"><span data-stu-id="b41d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b41d0-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="b41d0-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b41d0-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="b41d0-110">Type: **SamplerState**</span></span>

<span data-ttu-id="b41d0-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="b41d0-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="b41d0-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="b41d0-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="b41d0-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b41d0-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b41d0-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="b41d0-114">Type: **float**</span></span>

<span data-ttu-id="b41d0-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="b41d0-115">The texture coordinates.</span></span> <span data-ttu-id="b41d0-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="b41d0-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="b41d0-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="b41d0-117">Texture-Object Type</span></span>                    | <span data-ttu-id="b41d0-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="b41d0-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="b41d0-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b41d0-119">Texture1D</span></span>                              | <span data-ttu-id="b41d0-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b41d0-120">float</span></span>          |
| <span data-ttu-id="b41d0-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="b41d0-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="b41d0-122">float2</span><span class="sxs-lookup"><span data-stu-id="b41d0-122">float2</span></span>         |
| <span data-ttu-id="b41d0-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="b41d0-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="b41d0-124">float3</span><span class="sxs-lookup"><span data-stu-id="b41d0-124">float3</span></span>         |
| <span data-ttu-id="b41d0-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="b41d0-125">TextureCubeArray</span></span>                       | <span data-ttu-id="b41d0-126">float4</span><span class="sxs-lookup"><span data-stu-id="b41d0-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="b41d0-127">*偏差* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b41d0-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b41d0-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="b41d0-128">Type: **float**</span></span>

<span data-ttu-id="b41d0-129">偏差值（介於0.0 到1.0 （含）之間的浮點數）會在取樣之前套用至 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="b41d0-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="b41d0-130">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b41d0-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b41d0-131">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="b41d0-131">Type: **float**</span></span>

<span data-ttu-id="b41d0-132">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="b41d0-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="b41d0-133">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="b41d0-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b41d0-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="b41d0-134">Return value</span></span>

<span data-ttu-id="b41d0-135">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="b41d0-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="b41d0-136">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="b41d0-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="b41d0-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b41d0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b41d0-138">SampleBias 方法</span><span class="sxs-lookup"><span data-stu-id="b41d0-138">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="b41d0-139">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="b41d0-139">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
