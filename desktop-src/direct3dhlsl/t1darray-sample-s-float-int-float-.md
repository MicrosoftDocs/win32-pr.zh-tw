---
title: Texture1DArray：： Sample (S，float，int，float) 函數
description: 使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值到。 |Texture1DArray：： Sample (S，float，int，float) 函數
ms.assetid: 3A965EEE-FCA3-4DD8-87D2-56679DFF5D3A
keywords:
- 範例函式 HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16d0a651d70aa618b9791fb760c51dfa05945752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992054"
---
# <a name="texture1darraysamplesfloatintfloat-function"></a><span data-ttu-id="f2fc2-105">Texture1DArray：： Sample (S，float，int，float) 函數</span><span class="sxs-lookup"><span data-stu-id="f2fc2-105">Texture1DArray::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="f2fc2-106">使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值到。</span><span class="sxs-lookup"><span data-stu-id="f2fc2-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2fc2-107">語法</span><span class="sxs-lookup"><span data-stu-id="f2fc2-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="f2fc2-108">參數</span><span class="sxs-lookup"><span data-stu-id="f2fc2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2fc2-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="f2fc2-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fc2-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="f2fc2-110">Type: **SamplerState**</span></span>

<span data-ttu-id="f2fc2-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="f2fc2-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f2fc2-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="f2fc2-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f2fc2-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2fc2-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fc2-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="f2fc2-114">Type: **float**</span></span>

<span data-ttu-id="f2fc2-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="f2fc2-115">The texture coordinates.</span></span> <span data-ttu-id="f2fc2-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="f2fc2-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f2fc2-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="f2fc2-117">Texture-Object Type</span></span>                    | <span data-ttu-id="f2fc2-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="f2fc2-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f2fc2-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f2fc2-119">Texture1D</span></span>                              | <span data-ttu-id="f2fc2-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f2fc2-120">float</span></span>          |
| <span data-ttu-id="f2fc2-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="f2fc2-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f2fc2-122">float2</span><span class="sxs-lookup"><span data-stu-id="f2fc2-122">float2</span></span>         |
| <span data-ttu-id="f2fc2-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="f2fc2-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f2fc2-124">float3</span><span class="sxs-lookup"><span data-stu-id="f2fc2-124">float3</span></span>         |
| <span data-ttu-id="f2fc2-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f2fc2-125">TextureCubeArray</span></span>                       | <span data-ttu-id="f2fc2-126">float4</span><span class="sxs-lookup"><span data-stu-id="f2fc2-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f2fc2-127">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2fc2-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fc2-128">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="f2fc2-128">Type: **int**</span></span>

<span data-ttu-id="f2fc2-129">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="f2fc2-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="f2fc2-130">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="f2fc2-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="f2fc2-131">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="f2fc2-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="f2fc2-132">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="f2fc2-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="f2fc2-133">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="f2fc2-133">Texture-Object Type</span></span>           | <span data-ttu-id="f2fc2-134">參數類型</span><span class="sxs-lookup"><span data-stu-id="f2fc2-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="f2fc2-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f2fc2-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="f2fc2-136">int</span><span class="sxs-lookup"><span data-stu-id="f2fc2-136">int</span></span>            |
| <span data-ttu-id="f2fc2-137">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f2fc2-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="f2fc2-138">int2</span><span class="sxs-lookup"><span data-stu-id="f2fc2-138">int2</span></span>           |
| <span data-ttu-id="f2fc2-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f2fc2-139">Texture3D</span></span>                     | <span data-ttu-id="f2fc2-140">int3</span><span class="sxs-lookup"><span data-stu-id="f2fc2-140">int3</span></span>           |
| <span data-ttu-id="f2fc2-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="f2fc2-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f2fc2-142">不支援</span><span class="sxs-lookup"><span data-stu-id="f2fc2-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f2fc2-143">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2fc2-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2fc2-144">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="f2fc2-144">Type: **float**</span></span>

<span data-ttu-id="f2fc2-145">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="f2fc2-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f2fc2-146">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="f2fc2-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2fc2-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2fc2-147">Return value</span></span>

<span data-ttu-id="f2fc2-148">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f2fc2-148">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f2fc2-149">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="f2fc2-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f2fc2-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2fc2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2fc2-151">範例方法</span><span class="sxs-lookup"><span data-stu-id="f2fc2-151">Sample methods</span></span>](texture1darray-sample.md)
</dt> </dl>

 

 
