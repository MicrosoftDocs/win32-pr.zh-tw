---
title: Texture3D：： Sample (S，float，int，float) 函數
description: 使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值到。 |Texture3D：： Sample (S，float，int，float) 函數
ms.assetid: A1114A4A-16B9-4A5D-9A9D-262D6BAA9F2E
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
ms.openlocfilehash: 11577e6151d2353477a70e6ef2873d287eb71a87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991895"
---
# <a name="texture3dsamplesfloatintfloat-function"></a><span data-ttu-id="8ea7a-105">Texture3D：： Sample (S，float，int，float) 函數</span><span class="sxs-lookup"><span data-stu-id="8ea7a-105">Texture3D::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="8ea7a-106">使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值到。</span><span class="sxs-lookup"><span data-stu-id="8ea7a-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea7a-107">語法</span><span class="sxs-lookup"><span data-stu-id="8ea7a-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="8ea7a-108">參數</span><span class="sxs-lookup"><span data-stu-id="8ea7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea7a-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="8ea7a-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea7a-110">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="8ea7a-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="8ea7a-111">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="8ea7a-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="8ea7a-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ea7a-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea7a-113">材質座標。</span><span class="sxs-lookup"><span data-stu-id="8ea7a-113">The texture coordinates.</span></span> <span data-ttu-id="8ea7a-114">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="8ea7a-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="8ea7a-115">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="8ea7a-115">Texture-Object Type</span></span>                    | <span data-ttu-id="8ea7a-116">參數類型</span><span class="sxs-lookup"><span data-stu-id="8ea7a-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="8ea7a-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="8ea7a-117">Texture1D</span></span>                              | <span data-ttu-id="8ea7a-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="8ea7a-118">float</span></span>          |
| <span data-ttu-id="8ea7a-119">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="8ea7a-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="8ea7a-120">float2</span><span class="sxs-lookup"><span data-stu-id="8ea7a-120">float2</span></span>         |
| <span data-ttu-id="8ea7a-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="8ea7a-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="8ea7a-122">float3</span><span class="sxs-lookup"><span data-stu-id="8ea7a-122">float3</span></span>         |
| <span data-ttu-id="8ea7a-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8ea7a-123">TextureCubeArray</span></span>                       | <span data-ttu-id="8ea7a-124">float4</span><span class="sxs-lookup"><span data-stu-id="8ea7a-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="8ea7a-125">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ea7a-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea7a-126">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="8ea7a-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="8ea7a-127">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="8ea7a-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="8ea7a-128">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="8ea7a-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="8ea7a-129">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="8ea7a-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="8ea7a-130">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="8ea7a-130">Texture-Object Type</span></span>           | <span data-ttu-id="8ea7a-131">參數類型</span><span class="sxs-lookup"><span data-stu-id="8ea7a-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="8ea7a-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="8ea7a-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="8ea7a-133">int</span><span class="sxs-lookup"><span data-stu-id="8ea7a-133">int</span></span>            |
| <span data-ttu-id="8ea7a-134">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="8ea7a-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="8ea7a-135">int2</span><span class="sxs-lookup"><span data-stu-id="8ea7a-135">int2</span></span>           |
| <span data-ttu-id="8ea7a-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="8ea7a-136">Texture3D</span></span>                     | <span data-ttu-id="8ea7a-137">int3</span><span class="sxs-lookup"><span data-stu-id="8ea7a-137">int3</span></span>           |
| <span data-ttu-id="8ea7a-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="8ea7a-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="8ea7a-139">不支援</span><span class="sxs-lookup"><span data-stu-id="8ea7a-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="8ea7a-140">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ea7a-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea7a-141">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="8ea7a-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="8ea7a-142">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="8ea7a-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea7a-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ea7a-143">Return value</span></span>

<span data-ttu-id="8ea7a-144">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="8ea7a-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="8ea7a-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ea7a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea7a-146">範例方法</span><span class="sxs-lookup"><span data-stu-id="8ea7a-146">Sample methods</span></span>](texture3d-sample.md)
</dt> <dt>

[<span data-ttu-id="8ea7a-147">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="8ea7a-147">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
