---
title: Texture1D 的 SampleLevel：： SampleLevel (S、float、float、int、uint) 函數
description: 針對指定的 mipmap 層級進行紋理取樣，並傳回作業的狀態。 適用于 Texture1D。 |SampleLevel：： SampleLevel (S、float、float、int、uint) 函數
ms.assetid: B797C7F9-7436-4DD5-9CAB-EFF81D410174
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
ms.openlocfilehash: 6d0c74bd59c8e693b009e9d53a766f339a20a2d6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104992443"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture1d"></a><span data-ttu-id="3a8ca-106">Texture1D 的 SampleLevel：： SampleLevel (S、float、float、int、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="3a8ca-106">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture1D</span></span>

<span data-ttu-id="3a8ca-107">針對指定的 mipmap 層級進行紋理取樣，並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-107">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a8ca-108">語法</span><span class="sxs-lookup"><span data-stu-id="3a8ca-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="3a8ca-109">參數</span><span class="sxs-lookup"><span data-stu-id="3a8ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a8ca-110"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="3a8ca-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a8ca-111">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="3a8ca-111">Type: **SamplerState**</span></span>

<span data-ttu-id="3a8ca-112">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3a8ca-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3a8ca-114">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a8ca-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a8ca-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="3a8ca-115">Type: **float**</span></span>

<span data-ttu-id="3a8ca-116">材質座標。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-116">The texture coordinates.</span></span> <span data-ttu-id="3a8ca-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3a8ca-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="3a8ca-118">Texture-Object Type</span></span>                    | <span data-ttu-id="3a8ca-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="3a8ca-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3a8ca-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3a8ca-120">Texture1D</span></span>                              | <span data-ttu-id="3a8ca-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3a8ca-121">float</span></span>          |
| <span data-ttu-id="3a8ca-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="3a8ca-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3a8ca-123">float2</span><span class="sxs-lookup"><span data-stu-id="3a8ca-123">float2</span></span>         |
| <span data-ttu-id="3a8ca-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="3a8ca-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3a8ca-125">float3</span><span class="sxs-lookup"><span data-stu-id="3a8ca-125">float3</span></span>         |
| <span data-ttu-id="3a8ca-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3a8ca-126">TextureCubeArray</span></span>                       | <span data-ttu-id="3a8ca-127">float4</span><span class="sxs-lookup"><span data-stu-id="3a8ca-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3a8ca-128">*」 Lod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a8ca-128">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a8ca-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="3a8ca-129">Type: **float**</span></span>

<span data-ttu-id="3a8ca-130">\[在 \] 指定 mipmap 層級的數位中。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-130">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="3a8ca-131">如果值為≤0，則會使用 mipmap 層級 0 (最大的對應) 。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-131">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="3a8ca-132">小數值 (如果提供的) 用來在兩個 mipmap 層級之間插補。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-132">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="3a8ca-133">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a8ca-133">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a8ca-134">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="3a8ca-134">Type: **int**</span></span>

<span data-ttu-id="3a8ca-135">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-135">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="3a8ca-136">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-136">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="3a8ca-137">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="3a8ca-138">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-138">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="3a8ca-139">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="3a8ca-139">Texture-Object Type</span></span>           | <span data-ttu-id="3a8ca-140">參數類型</span><span class="sxs-lookup"><span data-stu-id="3a8ca-140">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="3a8ca-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3a8ca-141">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="3a8ca-142">int</span><span class="sxs-lookup"><span data-stu-id="3a8ca-142">int</span></span>            |
| <span data-ttu-id="3a8ca-143">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3a8ca-143">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="3a8ca-144">int2</span><span class="sxs-lookup"><span data-stu-id="3a8ca-144">int2</span></span>           |
| <span data-ttu-id="3a8ca-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3a8ca-145">Texture3D</span></span>                     | <span data-ttu-id="3a8ca-146">int3</span><span class="sxs-lookup"><span data-stu-id="3a8ca-146">int3</span></span>           |
| <span data-ttu-id="3a8ca-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="3a8ca-147">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3a8ca-148">不支援</span><span class="sxs-lookup"><span data-stu-id="3a8ca-148">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3a8ca-149">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3a8ca-149">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a8ca-150">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="3a8ca-150">Type: **uint**</span></span>

<span data-ttu-id="3a8ca-151">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-151">The status of the operation.</span></span> <span data-ttu-id="3a8ca-152">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-152">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3a8ca-153">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-153">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3a8ca-154">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-154">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a8ca-155">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a8ca-155">Return value</span></span>

<span data-ttu-id="3a8ca-156">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3a8ca-156">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3a8ca-157">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="3a8ca-157">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3a8ca-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a8ca-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a8ca-159">SampleLevel 方法</span><span class="sxs-lookup"><span data-stu-id="3a8ca-159">SampleLevel methods</span></span>](texture1d-samplelevel.md)
</dt> </dl>

 

 
