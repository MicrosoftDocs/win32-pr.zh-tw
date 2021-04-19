---
title: SampleBias：： SampleBias (S，float，float，float) function for TextureCube
description: 將偏差值套用至 mipmap 層級之後，TextureCube 範例的 SampleBias：： SampleBias (S、float、float、float) 函數會進行紋理取樣。
ms.assetid: BCDDADD9-D8B0-47C9-A312-5E6AF9C3C07B
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
ms.openlocfilehash: 55404f2e32f45e5b19e7b0cd4c109a6d5a8bcc13
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106993702"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="189a7-104">SampleBias：： SampleBias (S，float，float，float) function for TextureCube</span><span class="sxs-lookup"><span data-stu-id="189a7-104">SampleBias::SampleBias(S,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="189a7-105">將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。</span><span class="sxs-lookup"><span data-stu-id="189a7-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="189a7-106">語法</span><span class="sxs-lookup"><span data-stu-id="189a7-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="189a7-107">參數</span><span class="sxs-lookup"><span data-stu-id="189a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="189a7-108"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="189a7-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="189a7-109">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="189a7-109">Type: **SamplerState**</span></span>

<span data-ttu-id="189a7-110">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="189a7-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="189a7-111">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="189a7-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="189a7-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="189a7-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="189a7-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="189a7-113">Type: **float**</span></span>

<span data-ttu-id="189a7-114">材質座標。</span><span class="sxs-lookup"><span data-stu-id="189a7-114">The texture coordinates.</span></span> <span data-ttu-id="189a7-115">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="189a7-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="189a7-116">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="189a7-116">Texture-Object Type</span></span>                    | <span data-ttu-id="189a7-117">參數類型</span><span class="sxs-lookup"><span data-stu-id="189a7-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="189a7-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="189a7-118">Texture1D</span></span>                              | <span data-ttu-id="189a7-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="189a7-119">float</span></span>          |
| <span data-ttu-id="189a7-120">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="189a7-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="189a7-121">float2</span><span class="sxs-lookup"><span data-stu-id="189a7-121">float2</span></span>         |
| <span data-ttu-id="189a7-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="189a7-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="189a7-123">float3</span><span class="sxs-lookup"><span data-stu-id="189a7-123">float3</span></span>         |
| <span data-ttu-id="189a7-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="189a7-124">TextureCubeArray</span></span>                       | <span data-ttu-id="189a7-125">float4</span><span class="sxs-lookup"><span data-stu-id="189a7-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="189a7-126">*偏差* \[在\]</span><span class="sxs-lookup"><span data-stu-id="189a7-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="189a7-127">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="189a7-127">Type: **float**</span></span>

<span data-ttu-id="189a7-128">偏差值（介於0.0 到1.0 （含）之間的浮點數）會在取樣之前套用至 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="189a7-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="189a7-129">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="189a7-129">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="189a7-130">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="189a7-130">Type: **float**</span></span>

<span data-ttu-id="189a7-131">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="189a7-131">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="189a7-132">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="189a7-132">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="189a7-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="189a7-133">Return value</span></span>

<span data-ttu-id="189a7-134">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="189a7-134">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="189a7-135">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="189a7-135">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="189a7-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="189a7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="189a7-137">SampleBias 方法</span><span class="sxs-lookup"><span data-stu-id="189a7-137">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="189a7-138">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="189a7-138">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
