---
title: 'SampleGrad (DirectX HLSL 材質物件) '
description: '使用漸層來取樣材質，以影響範例位置的計算方式。 |SampleGrad (DirectX HLSL 材質物件) '
ms.assetid: f3d73296-23c4-4178-b89e-6f84cfcb48a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 959304d36da2b95bdf6289fba1b8c75d6ecfa314
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825735"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a><span data-ttu-id="73798-104">SampleGrad (DirectX HLSL 材質物件) </span><span class="sxs-lookup"><span data-stu-id="73798-104">SampleGrad (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="73798-105">使用漸層來取樣材質，以影響範例位置的計算方式。</span><span class="sxs-lookup"><span data-stu-id="73798-105">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>

<span data-ttu-id="73798-106">&lt;樣板類型 &gt; Object. SampleGrad ( 取樣器 \_ 狀態 S、float 位置、float DDX、float DDY \[ 、int Offset \] ) ;</span><span class="sxs-lookup"><span data-stu-id="73798-106">&lt;Template Type&gt; Object.SampleGrad( sampler\_state S, float Location, float DDX, float DDY \[, int Offset\] );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="73798-107">參數</span><span class="sxs-lookup"><span data-stu-id="73798-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73798-108">項目</span><span class="sxs-lookup"><span data-stu-id="73798-108">Item</span></span></th>
<th><span data-ttu-id="73798-109">描述</span><span class="sxs-lookup"><span data-stu-id="73798-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73798-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>物件</em></span><span class="sxs-lookup"><span data-stu-id="73798-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="73798-111">任何 <a href="dx-graphics-hlsl-to-type.md">材質物件</a> 類型 (除了 Texture2DMS 和 Texture2DMSArray) 之外。</span><span class="sxs-lookup"><span data-stu-id="73798-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73798-112"><span id="S"></span><span id="s"></span><em>！</em></span><span class="sxs-lookup"><span data-stu-id="73798-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="73798-113">在 <a href="dx-graphics-hlsl-sampler.md">取樣器狀態</a>。</span><span class="sxs-lookup"><span data-stu-id="73798-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="73798-114">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="73798-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73798-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>位置</em></span><span class="sxs-lookup"><span data-stu-id="73798-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="73798-116">在材質座標。</span><span class="sxs-lookup"><span data-stu-id="73798-116">[in] The Texture coordinates.</span></span> <span data-ttu-id="73798-117">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="73798-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="73798-118">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="73798-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="73798-119">參數類型</span><span class="sxs-lookup"><span data-stu-id="73798-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73798-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="73798-120">Texture1D</span></span></td>
<td><span data-ttu-id="73798-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="73798-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73798-122">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="73798-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="73798-123">float2</span><span class="sxs-lookup"><span data-stu-id="73798-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73798-124">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="73798-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="73798-125">float3</span><span class="sxs-lookup"><span data-stu-id="73798-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73798-126">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="73798-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="73798-127">float4</span><span class="sxs-lookup"><span data-stu-id="73798-127">float4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73798-128">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="73798-128">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="73798-129">不支援</span><span class="sxs-lookup"><span data-stu-id="73798-129">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73798-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span><span class="sxs-lookup"><span data-stu-id="73798-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span></span></p></td>
<td><p><span data-ttu-id="73798-131">在以 x 方向呈現的表面幾何變化率。</span><span class="sxs-lookup"><span data-stu-id="73798-131">[in] The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="73798-132">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="73798-132">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="73798-133">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="73798-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="73798-134">參數類型</span><span class="sxs-lookup"><span data-stu-id="73798-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73798-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="73798-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="73798-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="73798-136">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73798-137">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="73798-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="73798-138">float2</span><span class="sxs-lookup"><span data-stu-id="73798-138">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73798-139">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="73798-139">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="73798-140">float3</span><span class="sxs-lookup"><span data-stu-id="73798-140">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73798-141">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="73798-141">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="73798-142">不支援</span><span class="sxs-lookup"><span data-stu-id="73798-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73798-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span><span class="sxs-lookup"><span data-stu-id="73798-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span></span></p></td>
<td><p><span data-ttu-id="73798-144">在介面幾何在 y 方向的變化率。</span><span class="sxs-lookup"><span data-stu-id="73798-144">[in] The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="73798-145">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="73798-145">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="73798-146">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="73798-146">Texture-Object Type</span></span></th>
<th><span data-ttu-id="73798-147">參數類型</span><span class="sxs-lookup"><span data-stu-id="73798-147">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73798-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="73798-148">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="73798-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="73798-149">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73798-150">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="73798-150">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="73798-151">float2</span><span class="sxs-lookup"><span data-stu-id="73798-151">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73798-152">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="73798-152">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="73798-153">float3</span><span class="sxs-lookup"><span data-stu-id="73798-153">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73798-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="73798-154">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="73798-155">不支援</span><span class="sxs-lookup"><span data-stu-id="73798-155">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73798-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>抵消</em></span><span class="sxs-lookup"><span data-stu-id="73798-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="73798-157">在選擇性的材質座標位移，可用於任何材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="73798-157">[in] An optional texture coordinate offset, which can be used for any texture-object types.</span></span> <span data-ttu-id="73798-158">位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="73798-158">The offset is applied to the location before sampling.</span></span> <span data-ttu-id="73798-159">只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。</span><span class="sxs-lookup"><span data-stu-id="73798-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="73798-160">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="73798-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="73798-161">如需詳細資訊，請參閱套用<a href="dx-graphics-hlsl-to-sample.md">整數位移</a>。</span><span class="sxs-lookup"><span data-stu-id="73798-161">For more info, see<a href="dx-graphics-hlsl-to-sample.md">Applying Integer Offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="73798-162">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="73798-162">Texture-Object Type</span></span></th>
<th><span data-ttu-id="73798-163">參數類型</span><span class="sxs-lookup"><span data-stu-id="73798-163">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73798-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="73798-164">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="73798-165">int</span><span class="sxs-lookup"><span data-stu-id="73798-165">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73798-166">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="73798-166">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="73798-167">int2</span><span class="sxs-lookup"><span data-stu-id="73798-167">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73798-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="73798-168">Texture3D</span></span></td>
<td><span data-ttu-id="73798-169">int3</span><span class="sxs-lookup"><span data-stu-id="73798-169">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73798-170">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="73798-170">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="73798-171">不支援</span><span class="sxs-lookup"><span data-stu-id="73798-171">not supported</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73798-172">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="73798-172">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="73798-173">不支援</span><span class="sxs-lookup"><span data-stu-id="73798-173">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="73798-174">傳回值</span><span class="sxs-lookup"><span data-stu-id="73798-174">Return Value</span></span>

<span data-ttu-id="73798-175">紋理的範本類型，可能是單一或多元件向量。</span><span class="sxs-lookup"><span data-stu-id="73798-175">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="73798-176">格式是以材質的 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)為基礎。</span><span class="sxs-lookup"><span data-stu-id="73798-176">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="73798-177">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="73798-177">Minimum Shader Model</span></span>

<span data-ttu-id="73798-178">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="73798-178">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="73798-179">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="73798-179">vs\_4\_0</span></span> | <span data-ttu-id="73798-180">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="73798-180">vs\_4\_1</span></span>  | <span data-ttu-id="73798-181">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="73798-181">ps\_4\_0</span></span> | <span data-ttu-id="73798-182">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="73798-182">ps\_4\_1</span></span>  | <span data-ttu-id="73798-183">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="73798-183">gs\_4\_0</span></span> | <span data-ttu-id="73798-184">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="73798-184">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="73798-185">x</span><span class="sxs-lookup"><span data-stu-id="73798-185">x</span></span>        | <span data-ttu-id="73798-186">x</span><span class="sxs-lookup"><span data-stu-id="73798-186">x</span></span>         | <span data-ttu-id="73798-187">x</span><span class="sxs-lookup"><span data-stu-id="73798-187">x</span></span>        | <span data-ttu-id="73798-188">x</span><span class="sxs-lookup"><span data-stu-id="73798-188">x</span></span>         | <span data-ttu-id="73798-189">x</span><span class="sxs-lookup"><span data-stu-id="73798-189">x</span></span>        | <span data-ttu-id="73798-190">x</span><span class="sxs-lookup"><span data-stu-id="73798-190">x</span></span>         |



 

1.  <span data-ttu-id="73798-191">TextureCubeArray 適用于著色器模型4.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="73798-191">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="73798-192">在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="73798-192">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="73798-193">範例</span><span class="sxs-lookup"><span data-stu-id="73798-193">Example</span></span>

<span data-ttu-id="73798-194">這個部分程式碼範例是來自 [MotionBlur10 範例](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx)中的 MotionBlur 檔案。</span><span class="sxs-lookup"><span data-stu-id="73798-194">This partial code example is from the MotionBlur.fx file in the [MotionBlur10 Sample](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span></span>


```
// Object Declarations
Texture2D g_txDiffuse;

SamplerState g_samLinear
{
    Filter = ANISOTROPIC;
    MaxAnisotropy = 8;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VSSceneOut
{
    float4 Pos : SV_POSITION;
    float4 Color : COLOR0;
    float2 Tex : TEXCOORD;
    float2 Aniso : ANISOTROPY;
};

float4 PSSceneMain( VSSceneOut Input ) : SV_TARGET
{
    float2 ddx = Input.Aniso;
    float2 ddy = Input.Aniso;
    
    // Shader body calling the intrinsic function
    float4 diff = g_txDiffuse.SampleGrad( g_samLinear, Input.Tex, ddx, ddy);
    
    ...
}
```



## <a name="related-topics"></a><span data-ttu-id="73798-195">相關主題</span><span class="sxs-lookup"><span data-stu-id="73798-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73798-196">材質物件</span><span class="sxs-lookup"><span data-stu-id="73798-196">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

