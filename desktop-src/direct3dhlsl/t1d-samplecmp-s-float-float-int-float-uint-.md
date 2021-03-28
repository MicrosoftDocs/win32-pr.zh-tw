---
title: Texture1D 的 SampleCmp：： SampleCmp (S、float、float、int、float、uint) 函數
description: 此函式會使用比較值來拒絕範例，並使用選擇性的值來將範例層級 (」 LOD) 值到，來取樣材質。 適用于 Texture1D。
ms.assetid: D2320225-4BC6-4229-A624-6D0F105DD788
keywords:
- SampleCmp 函式 HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 690ede3cac45d05a3000fe60654255daef5202f7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104974758"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture1d"></a><span data-ttu-id="e664f-105">Texture1D 的 SampleCmp：： SampleCmp (S、float、float、int、float、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="e664f-105">SampleCmp::SampleCmp(S,float,float,int,float,uint) function for Texture1D</span></span>

<span data-ttu-id="e664f-106">使用比較值來拒絕範例，並使用選擇性的值來將範例層級 (」 LOD) 值設為，以將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="e664f-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="e664f-107">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="e664f-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e664f-108">語法</span><span class="sxs-lookup"><span data-stu-id="e664f-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="e664f-109">參數</span><span class="sxs-lookup"><span data-stu-id="e664f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e664f-110"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="e664f-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e664f-111">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="e664f-111">Type: **SamplerState**</span></span>

<span data-ttu-id="e664f-112">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="e664f-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e664f-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="e664f-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e664f-114">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e664f-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e664f-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="e664f-115">Type: **float**</span></span>

<span data-ttu-id="e664f-116">材質座標。</span><span class="sxs-lookup"><span data-stu-id="e664f-116">The texture coordinates.</span></span> <span data-ttu-id="e664f-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="e664f-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e664f-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="e664f-118">Texture-Object Type</span></span>                    | <span data-ttu-id="e664f-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="e664f-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e664f-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e664f-120">Texture1D</span></span>                              | <span data-ttu-id="e664f-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e664f-121">float</span></span>          |
| <span data-ttu-id="e664f-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="e664f-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e664f-123">float2</span><span class="sxs-lookup"><span data-stu-id="e664f-123">float2</span></span>         |
| <span data-ttu-id="e664f-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e664f-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e664f-125">float3</span><span class="sxs-lookup"><span data-stu-id="e664f-125">float3</span></span>         |
| <span data-ttu-id="e664f-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e664f-126">TextureCubeArray</span></span>                       | <span data-ttu-id="e664f-127">float4</span><span class="sxs-lookup"><span data-stu-id="e664f-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e664f-128">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e664f-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e664f-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="e664f-129">Type: **float**</span></span>

<span data-ttu-id="e664f-130">用來作為比較值的浮點值。</span><span class="sxs-lookup"><span data-stu-id="e664f-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="e664f-131">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e664f-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e664f-132">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="e664f-132">Type: **int**</span></span>

<span data-ttu-id="e664f-133">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="e664f-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="e664f-134">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="e664f-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="e664f-135">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="e664f-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="e664f-136">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="e664f-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="e664f-137">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="e664f-137">Texture-Object Type</span></span>           | <span data-ttu-id="e664f-138">參數類型</span><span class="sxs-lookup"><span data-stu-id="e664f-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="e664f-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e664f-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="e664f-140">int</span><span class="sxs-lookup"><span data-stu-id="e664f-140">int</span></span>            |
| <span data-ttu-id="e664f-141">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e664f-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="e664f-142">int2</span><span class="sxs-lookup"><span data-stu-id="e664f-142">int2</span></span>           |
| <span data-ttu-id="e664f-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e664f-143">Texture3D</span></span>                     | <span data-ttu-id="e664f-144">int3</span><span class="sxs-lookup"><span data-stu-id="e664f-144">int3</span></span>           |
| <span data-ttu-id="e664f-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e664f-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e664f-146">不支援</span><span class="sxs-lookup"><span data-stu-id="e664f-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e664f-147">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e664f-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e664f-148">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="e664f-148">Type: **float**</span></span>

<span data-ttu-id="e664f-149">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="e664f-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e664f-150">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="e664f-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="e664f-151">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e664f-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e664f-152">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="e664f-152">Type: **uint**</span></span>

<span data-ttu-id="e664f-153">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="e664f-153">The status of the operation.</span></span> <span data-ttu-id="e664f-154">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="e664f-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="e664f-155">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="e664f-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="e664f-156">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e664f-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e664f-157">傳回值</span><span class="sxs-lookup"><span data-stu-id="e664f-157">Return value</span></span>

<span data-ttu-id="e664f-158">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e664f-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e664f-159">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="e664f-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e664f-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e664f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e664f-161">SampleCmp 方法</span><span class="sxs-lookup"><span data-stu-id="e664f-161">SampleCmp methods</span></span>](texture1d-samplecmp.md)
</dt> </dl>

 

 
