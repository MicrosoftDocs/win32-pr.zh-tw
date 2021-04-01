---
title: Texture2DArray：： Sample (S，float，int，float) 函數
description: 使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值到。 |Texture2DArray：： Sample (S，float，int，float) 函數
ms.assetid: F6638224-0993-4F55-A8C0-7EC4140204D5
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
ms.openlocfilehash: 8d85e4d7e5662d76c011b1c5684f3fd36e4191ba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195932"
---
# <a name="texture2darraysamplesfloatintfloat-function"></a><span data-ttu-id="96ddd-105">Texture2DArray：： Sample (S，float，int，float) 函數</span><span class="sxs-lookup"><span data-stu-id="96ddd-105">Texture2DArray::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="96ddd-106">使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值到。</span><span class="sxs-lookup"><span data-stu-id="96ddd-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ddd-107">語法</span><span class="sxs-lookup"><span data-stu-id="96ddd-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="96ddd-108">參數</span><span class="sxs-lookup"><span data-stu-id="96ddd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ddd-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="96ddd-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96ddd-110">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="96ddd-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="96ddd-111">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="96ddd-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="96ddd-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96ddd-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96ddd-113">材質座標。</span><span class="sxs-lookup"><span data-stu-id="96ddd-113">The texture coordinates.</span></span> <span data-ttu-id="96ddd-114">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="96ddd-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="96ddd-115">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="96ddd-115">Texture-Object Type</span></span>                    | <span data-ttu-id="96ddd-116">參數類型</span><span class="sxs-lookup"><span data-stu-id="96ddd-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="96ddd-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="96ddd-117">Texture1D</span></span>                              | <span data-ttu-id="96ddd-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="96ddd-118">float</span></span>          |
| <span data-ttu-id="96ddd-119">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="96ddd-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="96ddd-120">float2</span><span class="sxs-lookup"><span data-stu-id="96ddd-120">float2</span></span>         |
| <span data-ttu-id="96ddd-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="96ddd-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="96ddd-122">float3</span><span class="sxs-lookup"><span data-stu-id="96ddd-122">float3</span></span>         |
| <span data-ttu-id="96ddd-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="96ddd-123">TextureCubeArray</span></span>                       | <span data-ttu-id="96ddd-124">float4</span><span class="sxs-lookup"><span data-stu-id="96ddd-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="96ddd-125">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96ddd-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96ddd-126">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="96ddd-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="96ddd-127">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="96ddd-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="96ddd-128">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="96ddd-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="96ddd-129">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="96ddd-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="96ddd-130">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="96ddd-130">Texture-Object Type</span></span>           | <span data-ttu-id="96ddd-131">參數類型</span><span class="sxs-lookup"><span data-stu-id="96ddd-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="96ddd-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="96ddd-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="96ddd-133">int</span><span class="sxs-lookup"><span data-stu-id="96ddd-133">int</span></span>            |
| <span data-ttu-id="96ddd-134">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="96ddd-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="96ddd-135">int2</span><span class="sxs-lookup"><span data-stu-id="96ddd-135">int2</span></span>           |
| <span data-ttu-id="96ddd-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="96ddd-136">Texture3D</span></span>                     | <span data-ttu-id="96ddd-137">int3</span><span class="sxs-lookup"><span data-stu-id="96ddd-137">int3</span></span>           |
| <span data-ttu-id="96ddd-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="96ddd-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="96ddd-139">不支援</span><span class="sxs-lookup"><span data-stu-id="96ddd-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="96ddd-140">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96ddd-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96ddd-141">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="96ddd-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="96ddd-142">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="96ddd-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96ddd-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="96ddd-143">Return value</span></span>

<span data-ttu-id="96ddd-144">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="96ddd-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="96ddd-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96ddd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ddd-146">範例方法</span><span class="sxs-lookup"><span data-stu-id="96ddd-146">Sample methods</span></span>](texture2darray-sample.md)
</dt> </dl>

 

 
