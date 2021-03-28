---
title: '範例 (S、float、int、float) 函數 (HLSL 參考) '
description: 使用選擇性值來取樣 Texture2D，以將範例層級 (」 LOD) 值設為。
ms.assetid: 899FACB6-40BB-471B-82A7-BDBBC63B206E
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
ms.openlocfilehash: e5c151c3d93f5e2fe374f0f60fd06798cf1ce52a
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/17/2020
ms.locfileid: "104093543"
---
# <a name="samplesfloatintfloat-function-hlsl-reference"></a><span data-ttu-id="e7c3c-104">範例 (S、float、int、float) 函數 (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="e7c3c-104">Sample(S,float,int,float) function (HLSL reference)</span></span>

<span data-ttu-id="e7c3c-105">使用選擇性值來取樣 [**Texture2D**](sm5-object-texture2d.md) ，以將範例層級 (」 lod) 值設為。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-105">Samples a [**Texture2D**](sm5-object-texture2d.md) with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

> [!Note]  
> <span data-ttu-id="e7c3c-106">需要 [著色器型號 5](d3d11-graphics-reference-sm5.md) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-106">Requires [shader model 5](d3d11-graphics-reference-sm5.md) or higher.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e7c3c-107">語法</span><span class="sxs-lookup"><span data-stu-id="e7c3c-107">Syntax</span></span>

``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float Location,
  in int Offset,
  in float Clamp
);
```

## <a name="parameters"></a><span data-ttu-id="e7c3c-108">參數</span><span class="sxs-lookup"><span data-stu-id="e7c3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7c3c-109"> \[ 中的 S\]</span><span class="sxs-lookup"><span data-stu-id="e7c3c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7c3c-110">[取樣器狀態](dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e7c3c-111">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e7c3c-112">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7c3c-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7c3c-113">材質座標。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-113">The texture coordinates.</span></span> <span data-ttu-id="e7c3c-114">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e7c3c-115">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="e7c3c-115">Texture-Object Type</span></span>                    | <span data-ttu-id="e7c3c-116">參數類型</span><span class="sxs-lookup"><span data-stu-id="e7c3c-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e7c3c-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e7c3c-117">Texture1D</span></span>                              | <span data-ttu-id="e7c3c-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e7c3c-118">float</span></span>          |
| <span data-ttu-id="e7c3c-119">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="e7c3c-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e7c3c-120">float2</span><span class="sxs-lookup"><span data-stu-id="e7c3c-120">float2</span></span>         |
| <span data-ttu-id="e7c3c-121">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="e7c3c-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e7c3c-122">float3</span><span class="sxs-lookup"><span data-stu-id="e7c3c-122">float3</span></span>         |
| <span data-ttu-id="e7c3c-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e7c3c-123">TextureCubeArray</span></span>                       | <span data-ttu-id="e7c3c-124">float4</span><span class="sxs-lookup"><span data-stu-id="e7c3c-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e7c3c-125">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7c3c-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7c3c-126">選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="e7c3c-127">材質位移必須是靜態的。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-127">The texture offsets need to be static.</span></span> <span data-ttu-id="e7c3c-128">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="e7c3c-129">如需詳細資訊，請參閱套用 [材質座標位移](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-129">For more info, see [Applying texture coordinate offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="e7c3c-130">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="e7c3c-130">Texture-Object Type</span></span>           | <span data-ttu-id="e7c3c-131">參數類型</span><span class="sxs-lookup"><span data-stu-id="e7c3c-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="e7c3c-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e7c3c-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="e7c3c-133">int</span><span class="sxs-lookup"><span data-stu-id="e7c3c-133">int</span></span>            |
| <span data-ttu-id="e7c3c-134">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e7c3c-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="e7c3c-135">int2</span><span class="sxs-lookup"><span data-stu-id="e7c3c-135">int2</span></span>           |
| <span data-ttu-id="e7c3c-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e7c3c-136">Texture3D</span></span>                     | <span data-ttu-id="e7c3c-137">int3</span><span class="sxs-lookup"><span data-stu-id="e7c3c-137">int3</span></span>           |
| <span data-ttu-id="e7c3c-138">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e7c3c-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e7c3c-139">不支援</span><span class="sxs-lookup"><span data-stu-id="e7c3c-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e7c3c-140">*夾具* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7c3c-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7c3c-141">用來將範例」 LOD 值設為的選擇性值。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e7c3c-142">例如，如果您傳遞 2.0 f 作為夾具值，您可以確保沒有任何個別的範例存取小於 2.0 f 的 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7c3c-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7c3c-143">Return value</span></span>

<span data-ttu-id="e7c3c-144">材質格式，這是以 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列出的其中一個具類型值。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7c3c-145">備註</span><span class="sxs-lookup"><span data-stu-id="e7c3c-145">Remarks</span></span>

<span data-ttu-id="e7c3c-146">紋理取樣會使用材質位置來查閱材質值。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-146">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="e7c3c-147">位移可以套用到查閱之前的位置。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-147">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="e7c3c-148">取樣器狀態包含取樣和篩選選項。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-148">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="e7c3c-149">這個方法可以在圖元著色器中叫用，但在頂點著色器或幾何著色器中不支援。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-149">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="e7c3c-150">只在整數 miplevel 使用位移;否則，您可能會根據硬體的執行或驅動程式設定取得不同的結果。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-150">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="e7c3c-151">計算材質位置</span><span class="sxs-lookup"><span data-stu-id="e7c3c-151">Calculating Texel Positions</span></span>

<span data-ttu-id="e7c3c-152">材質座標是參考紋理資料的浮點值，也稱為標準化材質空間。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-152">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="e7c3c-153">位址換行模式會依此順序套用 (材質座標 + 位移 + 換行模式) 來修改 \[ 0 ... 1 範圍以外的材質座標。 \]</span><span class="sxs-lookup"><span data-stu-id="e7c3c-153">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="e7c3c-154">針對材質陣列，location 參數中的額外值會指定紋理陣列中的索引。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-154">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="e7c3c-155">此索引會被視為調整的浮點值 (而不是標準材質座標) 的正規化空間。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-155">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="e7c3c-156">整數索引的轉換是以下列順序完成， (float + 四捨五入至最接近的陣列範圍) ，甚至是整數 + 夾具。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-156">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="e7c3c-157">套用材質座標位移</span><span class="sxs-lookup"><span data-stu-id="e7c3c-157">Applying Texture Coordinate Offsets</span></span>

<span data-ttu-id="e7c3c-158">Offset 參數會修改材質空間中的材質座標。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-158">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="e7c3c-159">雖然材質座標是正規化浮點數，但位移會套用整數位移。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-159">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="e7c3c-160">另請注意，材質位移必須是靜態的。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-160">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="e7c3c-161">傳回的資料格式取決於材質格式。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-161">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="e7c3c-162">例如，如果紋理資源是以 DXGI \_ 格式 \_ A8B8G8R8 \_ UNORM SRGB 格式所定義 \_ ，則取樣作業會將取樣的材質從 gamma 2.0 轉換為1.0、篩選，並將結果以浮點數形式寫入範圍 \[ 0 ..1 \] 。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-162">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

<span data-ttu-id="e7c3c-163">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="e7c3c-163">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7c3c-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7c3c-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c3c-165">範例方法</span><span class="sxs-lookup"><span data-stu-id="e7c3c-165">Sample methods</span></span>](texture-sample-overload.md)
</dt> <dt>

[<span data-ttu-id="e7c3c-166">材質物件</span><span class="sxs-lookup"><span data-stu-id="e7c3c-166">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
