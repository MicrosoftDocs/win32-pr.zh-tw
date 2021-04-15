---
title: Texture2DArray 的 SampleCmpLevelZero：： SampleCmpLevelZero (S、float、float、int、uint) 函數
description: 只對 mipmap 層級0上的材質進行取樣，並比較結果與比較值，然後傳回作業的相關狀態。 適用于 Texture2DArray。
ms.assetid: 2F5669A6-D506-4096-A37E-421E5A16545F
keywords:
- SampleCmpLevelZero 函式 HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f105e4eb1cfecbf56cde7c62b903ef10b5fa476b
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104974737"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatintuint-function-for-texture2darray"></a><span data-ttu-id="5a037-105">Texture2DArray 的 SampleCmpLevelZero：： SampleCmpLevelZero (S、float、float、int、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="5a037-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) function for Texture2DArray</span></span>

<span data-ttu-id="5a037-106">只對 mipmap 層級0進行紋理取樣，並將結果與比較值進行比較。</span><span class="sxs-lookup"><span data-stu-id="5a037-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="5a037-107">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="5a037-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a037-108">語法</span><span class="sxs-lookup"><span data-stu-id="5a037-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="5a037-109">參數</span><span class="sxs-lookup"><span data-stu-id="5a037-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a037-110"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="5a037-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a037-111">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="5a037-111">Type: **SamplerState**</span></span>

<span data-ttu-id="5a037-112">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="5a037-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="5a037-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="5a037-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="5a037-114">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a037-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a037-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="5a037-115">Type: **float**</span></span>

<span data-ttu-id="5a037-116">材質座標。</span><span class="sxs-lookup"><span data-stu-id="5a037-116">The texture coordinates.</span></span> <span data-ttu-id="5a037-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="5a037-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5a037-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="5a037-118">Texture-Object Type</span></span>                    | <span data-ttu-id="5a037-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="5a037-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="5a037-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5a037-120">Texture1D</span></span>                              | <span data-ttu-id="5a037-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5a037-121">float</span></span>          |
| <span data-ttu-id="5a037-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="5a037-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="5a037-123">float2</span><span class="sxs-lookup"><span data-stu-id="5a037-123">float2</span></span>         |
| <span data-ttu-id="5a037-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="5a037-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="5a037-125">float3</span><span class="sxs-lookup"><span data-stu-id="5a037-125">float3</span></span>         |
| <span data-ttu-id="5a037-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5a037-126">TextureCubeArray</span></span>                       | <span data-ttu-id="5a037-127">float4</span><span class="sxs-lookup"><span data-stu-id="5a037-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="5a037-128">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a037-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a037-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="5a037-129">Type: **float**</span></span>

<span data-ttu-id="5a037-130">用來作為比較值的浮點值。</span><span class="sxs-lookup"><span data-stu-id="5a037-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="5a037-131">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a037-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a037-132">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="5a037-132">Type: **int**</span></span>

<span data-ttu-id="5a037-133">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="5a037-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="5a037-134">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="5a037-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="5a037-135">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="5a037-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="5a037-136">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="5a037-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="5a037-137">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="5a037-137">Texture-Object Type</span></span>           | <span data-ttu-id="5a037-138">參數類型</span><span class="sxs-lookup"><span data-stu-id="5a037-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="5a037-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5a037-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="5a037-140">int</span><span class="sxs-lookup"><span data-stu-id="5a037-140">int</span></span>            |
| <span data-ttu-id="5a037-141">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5a037-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="5a037-142">int2</span><span class="sxs-lookup"><span data-stu-id="5a037-142">int2</span></span>           |
| <span data-ttu-id="5a037-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5a037-143">Texture3D</span></span>                     | <span data-ttu-id="5a037-144">int3</span><span class="sxs-lookup"><span data-stu-id="5a037-144">int3</span></span>           |
| <span data-ttu-id="5a037-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5a037-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="5a037-146">不支援</span><span class="sxs-lookup"><span data-stu-id="5a037-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="5a037-147">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5a037-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a037-148">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="5a037-148">Type: **uint**</span></span>

<span data-ttu-id="5a037-149">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="5a037-149">The status of the operation.</span></span> <span data-ttu-id="5a037-150">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="5a037-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5a037-151">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="5a037-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5a037-152">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5a037-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a037-153">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a037-153">Return value</span></span>

<span data-ttu-id="5a037-154">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="5a037-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="5a037-155">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="5a037-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="5a037-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a037-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a037-157">SampleCmpLevelZero 方法</span><span class="sxs-lookup"><span data-stu-id="5a037-157">SampleCmpLevelZero methods</span></span>](texture2darray-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="5a037-158">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="5a037-158">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
