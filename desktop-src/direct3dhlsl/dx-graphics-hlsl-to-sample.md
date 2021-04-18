---
title: 範例 (DirectX HLSL 紋理物件)
description: 範例材質。 | (DirectX HLSL 材質物件) 範例
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ec80d296025684c1bb67642661a31d8cdc119a53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991871"
---
# <a name="sample-directx-hlsl-texture-object"></a><span data-ttu-id="ffb61-104">範例 (DirectX HLSL 紋理物件)</span><span class="sxs-lookup"><span data-stu-id="ffb61-104">Sample (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="ffb61-105">範例材質。</span><span class="sxs-lookup"><span data-stu-id="ffb61-105">Samples a texture.</span></span>

|                                                                                  |
|----------------------------------------------------------------------------------|
| <span data-ttu-id="ffb61-106">&lt;範本類型 &gt; 物件。範例 ( 取樣器 \_ 狀態 S、浮點位置 \[ 、整數位移 \] ) ;</span><span class="sxs-lookup"><span data-stu-id="ffb61-106">&lt;Template Type&gt; Object.Sample( sampler\_state S, float Location \[, int Offset\] );</span></span> |

## <a name="parameters"></a><span data-ttu-id="ffb61-107">參數</span><span class="sxs-lookup"><span data-stu-id="ffb61-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ffb61-108">項目</span><span class="sxs-lookup"><span data-stu-id="ffb61-108">Item</span></span></th>
<th><span data-ttu-id="ffb61-109">描述</span><span class="sxs-lookup"><span data-stu-id="ffb61-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ffb61-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>物件</em></span><span class="sxs-lookup"><span data-stu-id="ffb61-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="ffb61-111">任何 <a href="dx-graphics-hlsl-to-type.md">材質物件</a> 類型 (除了 Texture2DMS 和 Texture2DMSArray) 之外。</span><span class="sxs-lookup"><span data-stu-id="ffb61-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffb61-112"><span id="S"></span><span id="s"></span><em>！</em></span><span class="sxs-lookup"><span data-stu-id="ffb61-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="ffb61-113">在 <a href="dx-graphics-hlsl-sampler.md">取樣器狀態</a>。</span><span class="sxs-lookup"><span data-stu-id="ffb61-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="ffb61-114">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="ffb61-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffb61-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>位置</em></span><span class="sxs-lookup"><span data-stu-id="ffb61-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="ffb61-116">在材質座標。</span><span class="sxs-lookup"><span data-stu-id="ffb61-116">[in] The texture coordinates.</span></span> <span data-ttu-id="ffb61-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="ffb61-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ffb61-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="ffb61-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ffb61-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="ffb61-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ffb61-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ffb61-120">Texture1D</span></span></td>
<td><span data-ttu-id="ffb61-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ffb61-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffb61-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="ffb61-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="ffb61-123">float2</span><span class="sxs-lookup"><span data-stu-id="ffb61-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffb61-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="ffb61-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="ffb61-125">float3</span><span class="sxs-lookup"><span data-stu-id="ffb61-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffb61-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ffb61-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ffb61-127">float4</span><span class="sxs-lookup"><span data-stu-id="ffb61-127">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffb61-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>抵消</em></span><span class="sxs-lookup"><span data-stu-id="ffb61-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="ffb61-129">在選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="ffb61-129">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="ffb61-130">材質位移必須是靜態的。</span><span class="sxs-lookup"><span data-stu-id="ffb61-130">The texture offsets need to be static.</span></span> <span data-ttu-id="ffb61-131">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="ffb61-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ffb61-132">如需詳細資訊，請參閱套用 <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">材質座標位移</a>。</span><span class="sxs-lookup"><span data-stu-id="ffb61-132">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ffb61-133">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="ffb61-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ffb61-134">參數類型</span><span class="sxs-lookup"><span data-stu-id="ffb61-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ffb61-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ffb61-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="ffb61-136">int</span><span class="sxs-lookup"><span data-stu-id="ffb61-136">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffb61-137">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ffb61-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="ffb61-138">int2</span><span class="sxs-lookup"><span data-stu-id="ffb61-138">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffb61-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ffb61-139">Texture3D</span></span></td>
<td><span data-ttu-id="ffb61-140">int3</span><span class="sxs-lookup"><span data-stu-id="ffb61-140">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffb61-141">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="ffb61-141">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ffb61-142">不支援</span><span class="sxs-lookup"><span data-stu-id="ffb61-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>

## <a name="return-value"></a><span data-ttu-id="ffb61-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="ffb61-143">Return value</span></span>

<span data-ttu-id="ffb61-144">紋理的範本類型，可能是單一或多元件向量。</span><span class="sxs-lookup"><span data-stu-id="ffb61-144">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="ffb61-145">格式是以材質的 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)為基礎。</span><span class="sxs-lookup"><span data-stu-id="ffb61-145">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="ffb61-146">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="ffb61-146">Minimum Shader Model</span></span>

<span data-ttu-id="ffb61-147">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ffb61-147">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="ffb61-148">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ffb61-148">vs\_4\_0</span></span> | <span data-ttu-id="ffb61-149">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ffb61-149">vs\_4\_1</span></span>  | <span data-ttu-id="ffb61-150">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ffb61-150">ps\_4\_0</span></span> | <span data-ttu-id="ffb61-151">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ffb61-151">ps\_4\_1</span></span>  | <span data-ttu-id="ffb61-152">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ffb61-152">gs\_4\_0</span></span> | <span data-ttu-id="ffb61-153">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ffb61-153">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="ffb61-154">x</span><span class="sxs-lookup"><span data-stu-id="ffb61-154">x</span></span>        | <span data-ttu-id="ffb61-155">x</span><span class="sxs-lookup"><span data-stu-id="ffb61-155">x</span></span>         |          |           |

1.  <span data-ttu-id="ffb61-156">TextureCubeArray 適用于著色器模型4.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="ffb61-156">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="ffb61-157">在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="ffb61-157">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="ffb61-158">範例</span><span class="sxs-lookup"><span data-stu-id="ffb61-158">Example</span></span>

<span data-ttu-id="ffb61-159">這個部分程式碼範例是以 [BasicHLSL11 範例](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11)中的 BasicHLSL11 檔案為基礎。</span><span class="sxs-lookup"><span data-stu-id="ffb61-159">This partial code example is based on the BasicHLSL11.fx file in the [BasicHLSL11 Sample](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span></span>

```
// Object Declarations
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color (note that COLOR0 is clamped from 0..1)
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT In;

// Shader body calling the intrinsic function
   ...
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
```

## <a name="remarks"></a><span data-ttu-id="ffb61-160">備註</span><span class="sxs-lookup"><span data-stu-id="ffb61-160">Remarks</span></span>

<span data-ttu-id="ffb61-161">紋理取樣會使用材質位置來查閱材質值。</span><span class="sxs-lookup"><span data-stu-id="ffb61-161">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="ffb61-162">位移可以套用到查閱之前的位置。</span><span class="sxs-lookup"><span data-stu-id="ffb61-162">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="ffb61-163">取樣器狀態包含取樣和篩選選項。</span><span class="sxs-lookup"><span data-stu-id="ffb61-163">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="ffb61-164">這個方法可以在圖元著色器中叫用，但在頂點著色器或幾何著色器中不支援。</span><span class="sxs-lookup"><span data-stu-id="ffb61-164">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="ffb61-165">只在整數 miplevel 使用位移;否則，您可能會根據硬體的執行或驅動程式設定取得不同的結果。</span><span class="sxs-lookup"><span data-stu-id="ffb61-165">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="ffb61-166">計算材質位置</span><span class="sxs-lookup"><span data-stu-id="ffb61-166">Calculating texel positions</span></span>

<span data-ttu-id="ffb61-167">材質座標是參考紋理資料的浮點值，也稱為標準化材質空間。</span><span class="sxs-lookup"><span data-stu-id="ffb61-167">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="ffb61-168">位址換行模式會依此順序套用 (材質座標 + 位移 + 換行模式) 來修改 \[ 0 ... 1 範圍以外的材質座標。 \]</span><span class="sxs-lookup"><span data-stu-id="ffb61-168">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="ffb61-169">針對材質陣列，location 參數中的額外值會指定紋理陣列中的索引。</span><span class="sxs-lookup"><span data-stu-id="ffb61-169">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="ffb61-170">此索引會被視為調整的浮點值 (而不是標準材質座標) 的正規化空間。</span><span class="sxs-lookup"><span data-stu-id="ffb61-170">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="ffb61-171">整數索引的轉換是以下列順序完成， (float + 四捨五入至最接近的陣列範圍) ，甚至是整數 + 夾具。</span><span class="sxs-lookup"><span data-stu-id="ffb61-171">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="ffb61-172">套用材質座標位移</span><span class="sxs-lookup"><span data-stu-id="ffb61-172">Applying texture coordinate offsets</span></span>

<span data-ttu-id="ffb61-173">Offset 參數會修改材質空間中的材質座標。</span><span class="sxs-lookup"><span data-stu-id="ffb61-173">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="ffb61-174">雖然材質座標是正規化浮點數，但位移會套用整數位移。</span><span class="sxs-lookup"><span data-stu-id="ffb61-174">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="ffb61-175">另請注意，材質位移必須是靜態的。</span><span class="sxs-lookup"><span data-stu-id="ffb61-175">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="ffb61-176">傳回的資料格式取決於材質格式。</span><span class="sxs-lookup"><span data-stu-id="ffb61-176">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="ffb61-177">例如，如果紋理資源是以 DXGI \_ 格式 \_ A8B8G8R8 \_ UNORM SRGB 格式所定義 \_ ，則取樣作業會將取樣的材質從 gamma 2.0 轉換為1.0、篩選，並將結果以浮點數形式寫入範圍 \[ 0 ..1 \] 。</span><span class="sxs-lookup"><span data-stu-id="ffb61-177">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffb61-178">相關主題</span><span class="sxs-lookup"><span data-stu-id="ffb61-178">Related topics</span></span>

[<span data-ttu-id="ffb61-179">材質物件</span><span class="sxs-lookup"><span data-stu-id="ffb61-179">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
