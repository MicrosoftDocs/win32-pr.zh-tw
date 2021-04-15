---
title: Texture2D 的 SampleLevel：： SampleLevel (S、float、float、int、uint) 函數
description: 在指定的 mipmap 層級上取樣 Texture2D，並傳回作業的狀態。
ms.assetid: B021D42E-9F63-4CCE-939B-F93D91F7CB80
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
ms.openlocfilehash: 1455454649e24bd984948a81837181a7bcdba11a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104992427"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2d"></a><span data-ttu-id="bb5d1-104">Texture2D 的 SampleLevel：： SampleLevel (S、float、float、int、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="bb5d1-104">SampleLevel::SampleLevel(S,float,float,int,uint) function for Texture2D</span></span>

<span data-ttu-id="bb5d1-105">在指定的 mipmap 層級上取樣 [**Texture2D**](sm5-object-texture2d.md) ，並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-105">Samples a [**Texture2D**](sm5-object-texture2d.md) on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb5d1-106">語法</span><span class="sxs-lookup"><span data-stu-id="bb5d1-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="bb5d1-107">參數</span><span class="sxs-lookup"><span data-stu-id="bb5d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb5d1-108"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="bb5d1-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5d1-109">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="bb5d1-109">Type: **SamplerState**</span></span>

<span data-ttu-id="bb5d1-110">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="bb5d1-111">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="bb5d1-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb5d1-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5d1-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="bb5d1-113">Type: **float**</span></span>

<span data-ttu-id="bb5d1-114">材質座標。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-114">The texture coordinates.</span></span> <span data-ttu-id="bb5d1-115">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="bb5d1-116">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="bb5d1-116">Texture-Object Type</span></span>                    | <span data-ttu-id="bb5d1-117">參數類型</span><span class="sxs-lookup"><span data-stu-id="bb5d1-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="bb5d1-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bb5d1-118">Texture1D</span></span>                              | <span data-ttu-id="bb5d1-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bb5d1-119">float</span></span>          |
| <span data-ttu-id="bb5d1-120">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="bb5d1-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="bb5d1-121">float2</span><span class="sxs-lookup"><span data-stu-id="bb5d1-121">float2</span></span>         |
| <span data-ttu-id="bb5d1-122">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="bb5d1-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="bb5d1-123">float3</span><span class="sxs-lookup"><span data-stu-id="bb5d1-123">float3</span></span>         |
| <span data-ttu-id="bb5d1-124">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bb5d1-124">TextureCubeArray</span></span>                       | <span data-ttu-id="bb5d1-125">float4</span><span class="sxs-lookup"><span data-stu-id="bb5d1-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="bb5d1-126">*」 Lod* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb5d1-126">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5d1-127">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="bb5d1-127">Type: **float**</span></span>

<span data-ttu-id="bb5d1-128">\[在 \] 指定 mipmap 層級的數位中。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-128">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="bb5d1-129">如果值為≤0，則會使用 mipmap 層級 0 (最大的對應) 。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-129">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="bb5d1-130">小數值 (如果提供的) 用來在兩個 mipmap 層級之間插補。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-130">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="bb5d1-131">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb5d1-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5d1-132">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="bb5d1-132">Type: **int**</span></span>

<span data-ttu-id="bb5d1-133">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="bb5d1-134">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="bb5d1-135">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="bb5d1-136">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="bb5d1-137">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="bb5d1-137">Texture-Object Type</span></span>           | <span data-ttu-id="bb5d1-138">參數類型</span><span class="sxs-lookup"><span data-stu-id="bb5d1-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="bb5d1-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bb5d1-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="bb5d1-140">int</span><span class="sxs-lookup"><span data-stu-id="bb5d1-140">int</span></span>            |
| <span data-ttu-id="bb5d1-141">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bb5d1-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="bb5d1-142">int2</span><span class="sxs-lookup"><span data-stu-id="bb5d1-142">int2</span></span>           |
| <span data-ttu-id="bb5d1-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bb5d1-143">Texture3D</span></span>                     | <span data-ttu-id="bb5d1-144">int3</span><span class="sxs-lookup"><span data-stu-id="bb5d1-144">int3</span></span>           |
| <span data-ttu-id="bb5d1-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="bb5d1-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="bb5d1-146">不支援</span><span class="sxs-lookup"><span data-stu-id="bb5d1-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="bb5d1-147">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bb5d1-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb5d1-148">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="bb5d1-148">Type: **uint**</span></span>

<span data-ttu-id="bb5d1-149">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-149">The status of the operation.</span></span> <span data-ttu-id="bb5d1-150">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="bb5d1-151">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="bb5d1-152">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb5d1-153">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb5d1-153">Return value</span></span>

<span data-ttu-id="bb5d1-154">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="bb5d1-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="bb5d1-155">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="bb5d1-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="bb5d1-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb5d1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb5d1-157">SampleLevel 方法</span><span class="sxs-lookup"><span data-stu-id="bb5d1-157">SampleLevel methods</span></span>](texture2d-samplelevel.md)
</dt> </dl>

 

 
