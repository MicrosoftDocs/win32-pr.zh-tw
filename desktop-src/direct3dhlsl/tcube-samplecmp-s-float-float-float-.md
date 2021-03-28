---
title: SampleCmp：： SampleCmp (S，float，float，float) function for TextureCube
description: 使用比較值來拒絕範例，並使用選擇性的值來將範例層級 (」 LOD) 值設為，以將材質取樣。 |SampleCmp：： SampleCmp (S，float，float，float) function for TextureCube
ms.assetid: FCCF12CF-3F0A-4468-9FC4-27CAAF0BEEE3
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
ms.openlocfilehash: e8a326101df26ab7f4925c9c6cce3673385309fd
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104974752"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="37529-105">SampleCmp：： SampleCmp (S，float，float，float) function for TextureCube</span><span class="sxs-lookup"><span data-stu-id="37529-105">SampleCmp::SampleCmp(S,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="37529-106">使用比較值來拒絕範例，並使用選擇性的值來將範例層級 (」 LOD) 值設為，以將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="37529-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="37529-107">語法</span><span class="sxs-lookup"><span data-stu-id="37529-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="37529-108">參數</span><span class="sxs-lookup"><span data-stu-id="37529-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37529-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="37529-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37529-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="37529-110">Type: **SamplerState**</span></span>

<span data-ttu-id="37529-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="37529-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="37529-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="37529-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="37529-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37529-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37529-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="37529-114">Type: **float**</span></span>

<span data-ttu-id="37529-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="37529-115">The texture coordinates.</span></span> <span data-ttu-id="37529-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="37529-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="37529-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="37529-117">Texture-Object Type</span></span>                    | <span data-ttu-id="37529-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="37529-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="37529-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="37529-119">Texture1D</span></span>                              | <span data-ttu-id="37529-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="37529-120">float</span></span>          |
| <span data-ttu-id="37529-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="37529-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="37529-122">float2</span><span class="sxs-lookup"><span data-stu-id="37529-122">float2</span></span>         |
| <span data-ttu-id="37529-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="37529-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="37529-124">float3</span><span class="sxs-lookup"><span data-stu-id="37529-124">float3</span></span>         |
| <span data-ttu-id="37529-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="37529-125">TextureCubeArray</span></span>                       | <span data-ttu-id="37529-126">float4</span><span class="sxs-lookup"><span data-stu-id="37529-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="37529-127">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37529-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37529-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="37529-128">Type: **float**</span></span>

<span data-ttu-id="37529-129">用來作為比較值的浮點值。</span><span class="sxs-lookup"><span data-stu-id="37529-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="37529-130">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37529-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37529-131">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="37529-131">Type: **float**</span></span>

<span data-ttu-id="37529-132">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="37529-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="37529-133">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="37529-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37529-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="37529-134">Return value</span></span>

<span data-ttu-id="37529-135">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="37529-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="37529-136">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="37529-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="37529-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37529-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37529-138">SampleCmp 方法</span><span class="sxs-lookup"><span data-stu-id="37529-138">SampleCmp methods</span></span>](texturecube-samplecmp.md)
</dt> <dt>

[<span data-ttu-id="37529-139">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="37529-139">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
