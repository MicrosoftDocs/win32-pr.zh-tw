---
title: Texture2DArray 的 SampleLevel：： SampleLevel (S、float、float、int、uint) 函數
description: 針對指定的 mipmap 層級進行紋理取樣，並傳回作業的狀態。 適用于 Texture2DArray。 |SampleLevel：： SampleLevel (S、float、float、int、uint) 函數
ms.assetid: 2A561EE4-D7CF-44D4-AC93-F6841770B868
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
ms.openlocfilehash: 60e9f1df1a68d0971ac9d0ddf6be39eca03dd6ae
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104992419"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2darray"></a><span data-ttu-id="d71e0-106">Texture2DArray 的 SampleLevel：： SampleLevel (S、float、float、int、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="d71e0-106">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture2DArray</span></span>

<span data-ttu-id="d71e0-107">針對指定的 mipmap 層級進行紋理取樣，並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="d71e0-107">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d71e0-108">語法</span><span class="sxs-lookup"><span data-stu-id="d71e0-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="d71e0-109">參數</span><span class="sxs-lookup"><span data-stu-id="d71e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d71e0-110"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="d71e0-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d71e0-111">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="d71e0-111">Type: **SamplerState**</span></span>

<span data-ttu-id="d71e0-112">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="d71e0-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="d71e0-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="d71e0-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="d71e0-114">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d71e0-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d71e0-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="d71e0-115">Type: **float**</span></span>

<span data-ttu-id="d71e0-116">材質座標。</span><span class="sxs-lookup"><span data-stu-id="d71e0-116">The texture coordinates.</span></span> <span data-ttu-id="d71e0-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="d71e0-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d71e0-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="d71e0-118">Texture-Object Type</span></span>                    | <span data-ttu-id="d71e0-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="d71e0-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="d71e0-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d71e0-120">Texture1D</span></span>                              | <span data-ttu-id="d71e0-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d71e0-121">float</span></span>          |
| <span data-ttu-id="d71e0-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="d71e0-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="d71e0-123">float2</span><span class="sxs-lookup"><span data-stu-id="d71e0-123">float2</span></span>         |
| <span data-ttu-id="d71e0-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="d71e0-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="d71e0-125">float3</span><span class="sxs-lookup"><span data-stu-id="d71e0-125">float3</span></span>         |
| <span data-ttu-id="d71e0-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d71e0-126">TextureCubeArray</span></span>                       | <span data-ttu-id="d71e0-127">float4</span><span class="sxs-lookup"><span data-stu-id="d71e0-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="d71e0-128">*」 Lod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d71e0-128">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d71e0-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="d71e0-129">Type: **float**</span></span>

<span data-ttu-id="d71e0-130">\[在 \] 指定 mipmap 層級的數位中。</span><span class="sxs-lookup"><span data-stu-id="d71e0-130">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="d71e0-131">如果值為≤0，則會使用 mipmap 層級 0 (最大的對應) 。</span><span class="sxs-lookup"><span data-stu-id="d71e0-131">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="d71e0-132">小數值 (如果提供的) 用來在兩個 mipmap 層級之間插補。</span><span class="sxs-lookup"><span data-stu-id="d71e0-132">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="d71e0-133">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d71e0-133">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d71e0-134">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="d71e0-134">Type: **int**</span></span>

<span data-ttu-id="d71e0-135">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="d71e0-135">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="d71e0-136">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="d71e0-136">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="d71e0-137">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="d71e0-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="d71e0-138">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="d71e0-138">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="d71e0-139">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="d71e0-139">Texture-Object Type</span></span>           | <span data-ttu-id="d71e0-140">參數類型</span><span class="sxs-lookup"><span data-stu-id="d71e0-140">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="d71e0-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d71e0-141">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="d71e0-142">int</span><span class="sxs-lookup"><span data-stu-id="d71e0-142">int</span></span>            |
| <span data-ttu-id="d71e0-143">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d71e0-143">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="d71e0-144">int2</span><span class="sxs-lookup"><span data-stu-id="d71e0-144">int2</span></span>           |
| <span data-ttu-id="d71e0-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d71e0-145">Texture3D</span></span>                     | <span data-ttu-id="d71e0-146">int3</span><span class="sxs-lookup"><span data-stu-id="d71e0-146">int3</span></span>           |
| <span data-ttu-id="d71e0-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d71e0-147">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="d71e0-148">不支援</span><span class="sxs-lookup"><span data-stu-id="d71e0-148">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d71e0-149">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d71e0-149">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d71e0-150">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="d71e0-150">Type: **uint**</span></span>

<span data-ttu-id="d71e0-151">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="d71e0-151">The status of the operation.</span></span> <span data-ttu-id="d71e0-152">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="d71e0-152">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="d71e0-153">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="d71e0-153">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="d71e0-154">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d71e0-154">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d71e0-155">傳回值</span><span class="sxs-lookup"><span data-stu-id="d71e0-155">Return value</span></span>

<span data-ttu-id="d71e0-156">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="d71e0-156">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="d71e0-157">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="d71e0-157">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="d71e0-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d71e0-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d71e0-159">SampleLevel 方法</span><span class="sxs-lookup"><span data-stu-id="d71e0-159">SampleLevel methods</span></span>](texture2darray-samplelevel.md)
</dt> <dt>

[<span data-ttu-id="d71e0-160">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="d71e0-160">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
