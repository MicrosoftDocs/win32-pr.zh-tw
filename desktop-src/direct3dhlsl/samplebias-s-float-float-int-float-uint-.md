---
title: Texture2D 的 SampleBias：： SampleBias (S、float、float、int、float、uint) 函數
description: 將偏差值套用至 mipmap 層級之後，SampleBias：： SampleBias (S、float、float、int、float、uint) 函數會取樣 Texture2D。
ms.assetid: ACABF551-1DBF-4979-B0B1-D025E04EC08C
keywords:
- SampleBias 函式 HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86840748d12a92eca24b8d0d2bfba26eee69cff5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104974767"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture2d"></a><span data-ttu-id="4d63b-104">Texture2D 的 SampleBias：： SampleBias (S、float、float、int、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="4d63b-104">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture2D</span></span>

<span data-ttu-id="4d63b-105">在將偏差值套用至 mipmap 層級之後，針對 [**Texture2D**](sm5-object-texture2d.md)進行取樣，並使用選擇性的值來壓入範例詳細資料層級 (」 lod) 值為。</span><span class="sxs-lookup"><span data-stu-id="4d63b-105">Samples a [**Texture2D**](sm5-object-texture2d.md), after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="4d63b-106">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="4d63b-106">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d63b-107">語法</span><span class="sxs-lookup"><span data-stu-id="4d63b-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="4d63b-108">參數</span><span class="sxs-lookup"><span data-stu-id="4d63b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d63b-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="4d63b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d63b-110">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="4d63b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="4d63b-111">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="4d63b-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="4d63b-112">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="4d63b-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="4d63b-113">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d63b-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d63b-114">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="4d63b-114">Type: **float**</span></span>

<span data-ttu-id="4d63b-115">材質座標。</span><span class="sxs-lookup"><span data-stu-id="4d63b-115">The texture coordinates.</span></span> <span data-ttu-id="4d63b-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="4d63b-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4d63b-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="4d63b-117">Texture-Object Type</span></span>                    | <span data-ttu-id="4d63b-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="4d63b-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="4d63b-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4d63b-119">Texture1D</span></span>                              | <span data-ttu-id="4d63b-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d63b-120">float</span></span>          |
| <span data-ttu-id="4d63b-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="4d63b-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="4d63b-122">float2</span><span class="sxs-lookup"><span data-stu-id="4d63b-122">float2</span></span>         |
| <span data-ttu-id="4d63b-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="4d63b-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="4d63b-124">float3</span><span class="sxs-lookup"><span data-stu-id="4d63b-124">float3</span></span>         |
| <span data-ttu-id="4d63b-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4d63b-125">TextureCubeArray</span></span>                       | <span data-ttu-id="4d63b-126">float4</span><span class="sxs-lookup"><span data-stu-id="4d63b-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="4d63b-127">*偏差* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d63b-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d63b-128">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="4d63b-128">Type: **float**</span></span>

<span data-ttu-id="4d63b-129">偏差值（介於0.0 到1.0 （含）之間的浮點數）會在取樣之前套用至 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="4d63b-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="4d63b-130">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d63b-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d63b-131">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="4d63b-131">Type: **int**</span></span>

<span data-ttu-id="4d63b-132">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="4d63b-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="4d63b-133">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="4d63b-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="4d63b-134">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="4d63b-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="4d63b-135">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="4d63b-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="4d63b-136">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="4d63b-136">Texture-Object Type</span></span>           | <span data-ttu-id="4d63b-137">參數類型</span><span class="sxs-lookup"><span data-stu-id="4d63b-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="4d63b-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4d63b-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="4d63b-139">int</span><span class="sxs-lookup"><span data-stu-id="4d63b-139">int</span></span>            |
| <span data-ttu-id="4d63b-140">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4d63b-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="4d63b-141">int2</span><span class="sxs-lookup"><span data-stu-id="4d63b-141">int2</span></span>           |
| <span data-ttu-id="4d63b-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4d63b-142">Texture3D</span></span>                     | <span data-ttu-id="4d63b-143">int3</span><span class="sxs-lookup"><span data-stu-id="4d63b-143">int3</span></span>           |
| <span data-ttu-id="4d63b-144">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="4d63b-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="4d63b-145">不支援</span><span class="sxs-lookup"><span data-stu-id="4d63b-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4d63b-146">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d63b-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d63b-147">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="4d63b-147">Type: **float**</span></span>

<span data-ttu-id="4d63b-148">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="4d63b-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="4d63b-149">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="4d63b-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="4d63b-150">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d63b-150">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d63b-151">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="4d63b-151">Type: **uint**</span></span>

<span data-ttu-id="4d63b-152">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="4d63b-152">The status of the operation.</span></span> <span data-ttu-id="4d63b-153">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="4d63b-153">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4d63b-154">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="4d63b-154">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4d63b-155">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="4d63b-155">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d63b-156">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d63b-156">Return value</span></span>

<span data-ttu-id="4d63b-157">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="4d63b-157">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="4d63b-158">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="4d63b-158">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="4d63b-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d63b-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d63b-160">SampleBias 方法</span><span class="sxs-lookup"><span data-stu-id="4d63b-160">SampleBias methods</span></span>](texture2d-samplebias.md)
</dt> </dl>

 

 
