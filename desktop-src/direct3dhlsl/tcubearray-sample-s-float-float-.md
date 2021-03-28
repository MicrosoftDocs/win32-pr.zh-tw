---
title: TextureCubeArray：： Sample (S，float，float) 函數
description: 使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值到。 |TextureCubeArray：： Sample (S，float，float) 函數
ms.assetid: E3BACA5E-18FC-4BD7-A8D8-C2808BDF1517
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
ms.openlocfilehash: 0f3f822ee334262dc50950064c6b4257aca3dd1f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974113"
---
# <a name="texturecubearraysamplesfloatfloat-function"></a><span data-ttu-id="c7b6b-105">TextureCubeArray：： Sample (S，float，float) 函數</span><span class="sxs-lookup"><span data-stu-id="c7b6b-105">TextureCubeArray::Sample(S,float,float) function</span></span>

<span data-ttu-id="c7b6b-106">使用選擇性值來取樣材質，以將範例詳細資料 (」 LOD) 值到。</span><span class="sxs-lookup"><span data-stu-id="c7b6b-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7b6b-107">語法</span><span class="sxs-lookup"><span data-stu-id="c7b6b-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="c7b6b-108">參數</span><span class="sxs-lookup"><span data-stu-id="c7b6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7b6b-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="c7b6b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b6b-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="c7b6b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="c7b6b-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="c7b6b-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="c7b6b-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="c7b6b-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="c7b6b-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7b6b-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b6b-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c7b6b-114">Type: **float**</span></span>

<span data-ttu-id="c7b6b-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="c7b6b-115">The texture coordinates.</span></span> <span data-ttu-id="c7b6b-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="c7b6b-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="c7b6b-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="c7b6b-117">Texture-Object Type</span></span>                    | <span data-ttu-id="c7b6b-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="c7b6b-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="c7b6b-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c7b6b-119">Texture1D</span></span>                              | <span data-ttu-id="c7b6b-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c7b6b-120">float</span></span>          |
| <span data-ttu-id="c7b6b-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="c7b6b-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="c7b6b-122">float2</span><span class="sxs-lookup"><span data-stu-id="c7b6b-122">float2</span></span>         |
| <span data-ttu-id="c7b6b-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="c7b6b-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="c7b6b-124">float3</span><span class="sxs-lookup"><span data-stu-id="c7b6b-124">float3</span></span>         |
| <span data-ttu-id="c7b6b-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="c7b6b-125">TextureCubeArray</span></span>                       | <span data-ttu-id="c7b6b-126">float4</span><span class="sxs-lookup"><span data-stu-id="c7b6b-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="c7b6b-127">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7b6b-127">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b6b-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="c7b6b-128">Type: **float**</span></span>

<span data-ttu-id="c7b6b-129">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="c7b6b-129">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="c7b6b-130">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="c7b6b-130">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7b6b-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7b6b-131">Return value</span></span>

<span data-ttu-id="c7b6b-132">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="c7b6b-132">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="c7b6b-133">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="c7b6b-133">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="c7b6b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7b6b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7b6b-135">範例方法</span><span class="sxs-lookup"><span data-stu-id="c7b6b-135">Sample methods</span></span>](texturecubearray-sample.md)
</dt> <dt>

[<span data-ttu-id="c7b6b-136">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="c7b6b-136">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
