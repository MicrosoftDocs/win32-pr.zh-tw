---
title: SampleBias：： SampleBias (S，float，float，float) function for TextureCubeArray
description: 將偏差值套用至 mipmap 層級之後，TextureCubeArray 範例的 SampleBias：： SampleBias (S、float、float、float) 函數會進行紋理取樣。
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
ms.openlocfilehash: 0c57eec224ca92b2584ba7262488530ea7080939
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106988006"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="1a5a9-104">SampleBias：： SampleBias (S，float，float，float) function for TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1a5a9-104">SampleBias::SampleBias(S,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="1a5a9-105">將偏差值套用至 mipmap 層級之後，將材質取樣，並使用選擇性的值來壓 (」 LOD) 值到的範例詳細層級。</span><span class="sxs-lookup"><span data-stu-id="1a5a9-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a5a9-106">語法</span><span class="sxs-lookup"><span data-stu-id="1a5a9-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="1a5a9-107">參數</span><span class="sxs-lookup"><span data-stu-id="1a5a9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a5a9-108"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="1a5a9-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5a9-109">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="1a5a9-109">Type: **SamplerState**</span></span>

<span data-ttu-id="1a5a9-110">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="1a5a9-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="1a5a9-111">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="1a5a9-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="1a5a9-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1a5a9-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5a9-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="1a5a9-113">Type: **float**</span></span>

<span data-ttu-id="1a5a9-114">材質座標。</span><span class="sxs-lookup"><span data-stu-id="1a5a9-114">The texture coordinates.</span></span> <span data-ttu-id="1a5a9-115">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="1a5a9-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="1a5a9-116">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="1a5a9-116">Texture-Object Type</span></span>                    | <span data-ttu-id="1a5a9-117">參數類型</span><span class="sxs-lookup"><span data-stu-id="1a5a9-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="1a5a9-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1a5a9-118">Texture1D</span></span>                              | <span data-ttu-id="1a5a9-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1a5a9-119">float</span></span>          |
| <span data-ttu-id="1a5a9-120">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="1a5a9-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="1a5a9-121">float2</span><span class="sxs-lookup"><span data-stu-id="1a5a9-121">float2</span></span>         |
| <span data-ttu-id="1a5a9-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="1a5a9-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="1a5a9-123">float3</span><span class="sxs-lookup"><span data-stu-id="1a5a9-123">float3</span></span>         |
| <span data-ttu-id="1a5a9-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="1a5a9-124">TextureCubeArray</span></span>                       | <span data-ttu-id="1a5a9-125">float4</span><span class="sxs-lookup"><span data-stu-id="1a5a9-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="1a5a9-126">*偏差* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1a5a9-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5a9-127">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="1a5a9-127">Type: **float**</span></span>

<span data-ttu-id="1a5a9-128">偏差值（介於0.0 到1.0 （含）之間的浮點數）會在取樣之前套用至 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="1a5a9-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1a5a9-129">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1a5a9-129">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5a9-130">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="1a5a9-130">Type: **float**</span></span>

<span data-ttu-id="1a5a9-131">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="1a5a9-131">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="1a5a9-132">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="1a5a9-132">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a5a9-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a5a9-133">Return value</span></span>

<span data-ttu-id="1a5a9-134">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="1a5a9-134">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="1a5a9-135">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="1a5a9-135">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="1a5a9-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a5a9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a5a9-137">SampleBias 方法</span><span class="sxs-lookup"><span data-stu-id="1a5a9-137">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="1a5a9-138">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="1a5a9-138">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
