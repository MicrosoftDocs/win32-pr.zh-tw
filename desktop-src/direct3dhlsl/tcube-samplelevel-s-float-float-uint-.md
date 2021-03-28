---
title: TextureCube 的 SampleLevel：： SampleLevel (S、float、float、uint) 函數
description: 針對指定的 mipmap 層級進行紋理取樣，並傳回作業的狀態。 |SampleLevel：： SampleLevel (S，float，float，uint) 函數
ms.assetid: DB27D8B9-11AB-4F0C-947A-9469BA565F41
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
ms.openlocfilehash: a31eaa2351b4758c29327aaa08ccee5ed0c3056c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104386539"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="98e55-105">TextureCube 的 SampleLevel：： SampleLevel (S、float、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="98e55-105">SampleLevel::SampleLevel(S,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="98e55-106">針對指定的 mipmap 層級進行紋理取樣，並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="98e55-106">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e55-107">語法</span><span class="sxs-lookup"><span data-stu-id="98e55-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="98e55-108">參數</span><span class="sxs-lookup"><span data-stu-id="98e55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e55-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="98e55-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98e55-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="98e55-110">Type: **SamplerState**</span></span>

<span data-ttu-id="98e55-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="98e55-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="98e55-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="98e55-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="98e55-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98e55-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98e55-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="98e55-114">Type: **float**</span></span>

<span data-ttu-id="98e55-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="98e55-115">The texture coordinates.</span></span> <span data-ttu-id="98e55-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="98e55-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="98e55-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="98e55-117">Texture-Object Type</span></span>                    | <span data-ttu-id="98e55-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="98e55-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="98e55-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="98e55-119">Texture1D</span></span>                              | <span data-ttu-id="98e55-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="98e55-120">float</span></span>          |
| <span data-ttu-id="98e55-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="98e55-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="98e55-122">float2</span><span class="sxs-lookup"><span data-stu-id="98e55-122">float2</span></span>         |
| <span data-ttu-id="98e55-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="98e55-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="98e55-124">float3</span><span class="sxs-lookup"><span data-stu-id="98e55-124">float3</span></span>         |
| <span data-ttu-id="98e55-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="98e55-125">TextureCubeArray</span></span>                       | <span data-ttu-id="98e55-126">float4</span><span class="sxs-lookup"><span data-stu-id="98e55-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="98e55-127">*」 Lod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98e55-127">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98e55-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="98e55-128">Type: **float**</span></span>

<span data-ttu-id="98e55-129">\[在 \] 指定 mipmap 層級的數位中。</span><span class="sxs-lookup"><span data-stu-id="98e55-129">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="98e55-130">如果值為≤0，則會使用 mipmap 層級 0 (最大的對應) 。</span><span class="sxs-lookup"><span data-stu-id="98e55-130">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="98e55-131">小數值 (如果提供的) 用來在兩個 mipmap 層級之間插補。</span><span class="sxs-lookup"><span data-stu-id="98e55-131">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="98e55-132">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="98e55-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98e55-133">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="98e55-133">Type: **uint**</span></span>

<span data-ttu-id="98e55-134">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="98e55-134">The status of the operation.</span></span> <span data-ttu-id="98e55-135">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="98e55-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="98e55-136">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="98e55-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="98e55-137">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="98e55-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e55-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="98e55-138">Return value</span></span>

<span data-ttu-id="98e55-139">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="98e55-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="98e55-140">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="98e55-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="98e55-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98e55-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e55-142">SampleLevel 方法</span><span class="sxs-lookup"><span data-stu-id="98e55-142">SampleLevel methods</span></span>](texturecube-samplelevel.md)
</dt> <dt>

[<span data-ttu-id="98e55-143">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="98e55-143">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
