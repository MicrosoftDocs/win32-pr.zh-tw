---
title: Texture1DArray 的 SampleCmpLevelZero：： SampleCmpLevelZero (S、float、float、int、uint) 函數
description: 瞭解此函式如何只對 mipmap 層級0進行紋理取樣，並將結果與比較值進行比較。 適用于 Texture1DArray。
ms.assetid: DBC06FEF-DA64-4210-A47C-81EB0F1F9D5A
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
ms.openlocfilehash: 854dc20d732813623ba637ce53029d8098c90908
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104992405"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatintuint-function-for-texture1darray"></a><span data-ttu-id="37b18-105">Texture1DArray 的 SampleCmpLevelZero：： SampleCmpLevelZero (S、float、float、int、uint) 函數</span><span class="sxs-lookup"><span data-stu-id="37b18-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,int,uint) function for Texture1DArray</span></span>

<span data-ttu-id="37b18-106">只對 mipmap 層級0進行紋理取樣，並將結果與比較值進行比較。</span><span class="sxs-lookup"><span data-stu-id="37b18-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="37b18-107">傳回操作的相關狀態。</span><span class="sxs-lookup"><span data-stu-id="37b18-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="37b18-108">語法</span><span class="sxs-lookup"><span data-stu-id="37b18-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="37b18-109">參數</span><span class="sxs-lookup"><span data-stu-id="37b18-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b18-110"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="37b18-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37b18-111">類型： **SamplerState**</span><span class="sxs-lookup"><span data-stu-id="37b18-111">Type: **SamplerState**</span></span>

<span data-ttu-id="37b18-112">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="37b18-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="37b18-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="37b18-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="37b18-114">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37b18-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37b18-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="37b18-115">Type: **float**</span></span>

<span data-ttu-id="37b18-116">材質座標。</span><span class="sxs-lookup"><span data-stu-id="37b18-116">The texture coordinates.</span></span> <span data-ttu-id="37b18-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="37b18-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="37b18-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="37b18-118">Texture-Object Type</span></span>                    | <span data-ttu-id="37b18-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="37b18-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="37b18-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="37b18-120">Texture1D</span></span>                              | <span data-ttu-id="37b18-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="37b18-121">float</span></span>          |
| <span data-ttu-id="37b18-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="37b18-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="37b18-123">float2</span><span class="sxs-lookup"><span data-stu-id="37b18-123">float2</span></span>         |
| <span data-ttu-id="37b18-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="37b18-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="37b18-125">float3</span><span class="sxs-lookup"><span data-stu-id="37b18-125">float3</span></span>         |
| <span data-ttu-id="37b18-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="37b18-126">TextureCubeArray</span></span>                       | <span data-ttu-id="37b18-127">float4</span><span class="sxs-lookup"><span data-stu-id="37b18-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="37b18-128">*CompareValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37b18-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37b18-129">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="37b18-129">Type: **float**</span></span>

<span data-ttu-id="37b18-130">用來作為比較值的浮點值。</span><span class="sxs-lookup"><span data-stu-id="37b18-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="37b18-131">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37b18-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37b18-132">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="37b18-132">Type: **int**</span></span>

<span data-ttu-id="37b18-133">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="37b18-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="37b18-134">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="37b18-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="37b18-135">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="37b18-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="37b18-136">如需詳細資訊，請參閱套用 [整數位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="37b18-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="37b18-137">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="37b18-137">Texture-Object Type</span></span>           | <span data-ttu-id="37b18-138">參數類型</span><span class="sxs-lookup"><span data-stu-id="37b18-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="37b18-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="37b18-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="37b18-140">int</span><span class="sxs-lookup"><span data-stu-id="37b18-140">int</span></span>            |
| <span data-ttu-id="37b18-141">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="37b18-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="37b18-142">int2</span><span class="sxs-lookup"><span data-stu-id="37b18-142">int2</span></span>           |
| <span data-ttu-id="37b18-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="37b18-143">Texture3D</span></span>                     | <span data-ttu-id="37b18-144">int3</span><span class="sxs-lookup"><span data-stu-id="37b18-144">int3</span></span>           |
| <span data-ttu-id="37b18-145">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="37b18-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="37b18-146">不支援</span><span class="sxs-lookup"><span data-stu-id="37b18-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="37b18-147">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="37b18-147">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37b18-148">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="37b18-148">Type: **uint**</span></span>

<span data-ttu-id="37b18-149">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="37b18-149">The status of the operation.</span></span> <span data-ttu-id="37b18-150">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="37b18-150">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="37b18-151">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="37b18-151">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="37b18-152">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="37b18-152">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b18-153">傳回值</span><span class="sxs-lookup"><span data-stu-id="37b18-153">Return value</span></span>

<span data-ttu-id="37b18-154">類型： **[ **DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="37b18-154">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="37b18-155">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="37b18-155">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="37b18-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37b18-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b18-157">SampleCmpLevelZero 方法</span><span class="sxs-lookup"><span data-stu-id="37b18-157">SampleCmpLevelZero methods</span></span>](texture1darray-samplecmplevelzero.md)
</dt> </dl>

 

 
