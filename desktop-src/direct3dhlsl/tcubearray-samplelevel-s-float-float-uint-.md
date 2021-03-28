---
title: SampleLevel：： SampleLevel (S，float，float，uint) 函數
description: 針對指定的 mipmap 層級進行紋理取樣，並傳回作業的狀態。 |SampleLevel：： SampleLevel (S，float，float，uint) 函數
ms.assetid: 3794D17F-BC70-4D3A-9F2C-ADF900983D2C
keywords:
- SampleLevel 函式 HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 356e2779d82e886946e93d2071ae693279c07eb8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196010"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function"></a><span data-ttu-id="40479-105">SampleLevel：： SampleLevel (S，float，float，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="40479-105">SampleLevel::SampleLevel(S,float,float,uint) function</span></span>

<span data-ttu-id="40479-106">針對指定的 mipmap 層級進行紋理取樣，並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="40479-106">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="40479-107">語法</span><span class="sxs-lookup"><span data-stu-id="40479-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="40479-108">參數</span><span class="sxs-lookup"><span data-stu-id="40479-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40479-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="40479-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40479-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="40479-110">Type: **SamplerState**</span></span>

<span data-ttu-id="40479-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="40479-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="40479-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="40479-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="40479-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40479-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40479-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="40479-114">Type: **float**</span></span>

<span data-ttu-id="40479-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="40479-115">The texture coordinates.</span></span> <span data-ttu-id="40479-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="40479-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="40479-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="40479-117">Texture-Object Type</span></span>                    | <span data-ttu-id="40479-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="40479-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="40479-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="40479-119">Texture1D</span></span>                              | <span data-ttu-id="40479-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="40479-120">float</span></span>          |
| <span data-ttu-id="40479-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="40479-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="40479-122">float2</span><span class="sxs-lookup"><span data-stu-id="40479-122">float2</span></span>         |
| <span data-ttu-id="40479-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="40479-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="40479-124">float3</span><span class="sxs-lookup"><span data-stu-id="40479-124">float3</span></span>         |
| <span data-ttu-id="40479-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="40479-125">TextureCubeArray</span></span>                       | <span data-ttu-id="40479-126">float4</span><span class="sxs-lookup"><span data-stu-id="40479-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="40479-127">*」 Lod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40479-127">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40479-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="40479-128">Type: **float**</span></span>

<span data-ttu-id="40479-129">\[在 \] 指定 mipmap 層級的數位中。</span><span class="sxs-lookup"><span data-stu-id="40479-129">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="40479-130">如果值為≤0，則會使用 mipmap 層級 0 (最大的對應) 。</span><span class="sxs-lookup"><span data-stu-id="40479-130">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="40479-131">小數值 (如果提供的) 用來在兩個 mipmap 層級之間插補。</span><span class="sxs-lookup"><span data-stu-id="40479-131">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="40479-132">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="40479-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40479-133">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="40479-133">Type: **uint**</span></span>

<span data-ttu-id="40479-134">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="40479-134">The status of the operation.</span></span> <span data-ttu-id="40479-135">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="40479-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="40479-136">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="40479-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="40479-137">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="40479-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40479-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="40479-138">Return value</span></span>

<span data-ttu-id="40479-139">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="40479-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="40479-140">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="40479-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="40479-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40479-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40479-142">SampleLevel 方法</span><span class="sxs-lookup"><span data-stu-id="40479-142">SampleLevel methods</span></span>](texturecubearray-samplelevel.md)
</dt> <dt>

[<span data-ttu-id="40479-143">**TextureCubeArray**</span><span class="sxs-lookup"><span data-stu-id="40479-143">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
