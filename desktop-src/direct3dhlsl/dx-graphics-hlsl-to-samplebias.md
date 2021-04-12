---
title: 'SampleBias (DirectX HLSL 材質物件) '
description: 將輸入偏差套用至 mipmap 層級之後，將材質取樣。
ms.assetid: 1bc03ad8-7b69-4001-81c7-64d8c631d68d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e710b8a6c7dd2983c6d0c635d16356f95d0b4fe7
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/17/2020
ms.locfileid: "104383401"
---
# <a name="samplebias-directx-hlsl-texture-object"></a><span data-ttu-id="d819d-103">SampleBias (DirectX HLSL 材質物件) </span><span class="sxs-lookup"><span data-stu-id="d819d-103">SampleBias (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="d819d-104">將輸入偏差套用至 mipmap 層級之後，將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="d819d-104">Samples a texture, after applying the input bias to the mipmap level.</span></span>



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d819d-105">&lt;樣板類型 &gt; Object. SampleBias ( 取樣器 \_ 狀態 S、浮點位置、浮點數偏差 \[ 、int 位移 \] ) ;</span><span class="sxs-lookup"><span data-stu-id="d819d-105">&lt;Template Type&gt; Object.SampleBias( sampler\_state S, float Location, float Bias \[, int Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="d819d-106">參數</span><span class="sxs-lookup"><span data-stu-id="d819d-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d819d-107">項目</span><span class="sxs-lookup"><span data-stu-id="d819d-107">Item</span></span></th>
<th><span data-ttu-id="d819d-108">描述</span><span class="sxs-lookup"><span data-stu-id="d819d-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d819d-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>物件</em></span><span class="sxs-lookup"><span data-stu-id="d819d-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="d819d-110">任何 <a href="dx-graphics-hlsl-to-type.md">材質物件</a> 類型 (除了 Texture2DMS 和 Texture2DMSArray) 之外。</span><span class="sxs-lookup"><span data-stu-id="d819d-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d819d-111"><span id="S"></span><span id="s"></span><em>！</em></span><span class="sxs-lookup"><span data-stu-id="d819d-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="d819d-112">在 <a href="dx-graphics-hlsl-sampler.md">取樣器狀態</a>。</span><span class="sxs-lookup"><span data-stu-id="d819d-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="d819d-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="d819d-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d819d-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>位置</em></span><span class="sxs-lookup"><span data-stu-id="d819d-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="d819d-115">在材質座標。</span><span class="sxs-lookup"><span data-stu-id="d819d-115">[in] The texture coordinates.</span></span> <span data-ttu-id="d819d-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="d819d-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d819d-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="d819d-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="d819d-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="d819d-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d819d-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d819d-119">Texture1D</span></span></td>
<td><span data-ttu-id="d819d-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d819d-120">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d819d-121">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="d819d-121">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="d819d-122">float2</span><span class="sxs-lookup"><span data-stu-id="d819d-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d819d-123">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="d819d-123">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="d819d-124">float3</span><span class="sxs-lookup"><span data-stu-id="d819d-124">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d819d-125">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d819d-125">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="d819d-126">float4</span><span class="sxs-lookup"><span data-stu-id="d819d-126">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d819d-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>偏見</em></span><span class="sxs-lookup"><span data-stu-id="d819d-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Bias</em></span></span></p></td>
<td><p><span data-ttu-id="d819d-128">在偏差值（介於-16.0 和15.99 之間的浮點數）會在取樣之前套用至 mip 層級。</span><span class="sxs-lookup"><span data-stu-id="d819d-128">[in] The bias value, which is a floating-point number between -16.0 and 15.99, is applied to a mip level before sampling.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d819d-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>抵消</em></span><span class="sxs-lookup"><span data-stu-id="d819d-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="d819d-130">在選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="d819d-130">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="d819d-131">材質位移必須是靜態的。</span><span class="sxs-lookup"><span data-stu-id="d819d-131">The texture offsets need to be static.</span></span> <span data-ttu-id="d819d-132">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="d819d-132">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="d819d-133">如需詳細資訊，請參閱套用 <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">材質座標位移</a>。</span><span class="sxs-lookup"><span data-stu-id="d819d-133">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d819d-134">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="d819d-134">Texture-Object Type</span></span></th>
<th><span data-ttu-id="d819d-135">參數類型</span><span class="sxs-lookup"><span data-stu-id="d819d-135">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d819d-136">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d819d-136">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="d819d-137">int</span><span class="sxs-lookup"><span data-stu-id="d819d-137">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d819d-138">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d819d-138">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="d819d-139">int2</span><span class="sxs-lookup"><span data-stu-id="d819d-139">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d819d-140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d819d-140">Texture3D</span></span></td>
<td><span data-ttu-id="d819d-141">int3</span><span class="sxs-lookup"><span data-stu-id="d819d-141">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d819d-142">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="d819d-142">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="d819d-143">不支援</span><span class="sxs-lookup"><span data-stu-id="d819d-143">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="d819d-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="d819d-144">Return Value</span></span>

<span data-ttu-id="d819d-145">紋理的範本類型，可能是單一或多元件向量。</span><span class="sxs-lookup"><span data-stu-id="d819d-145">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="d819d-146">格式是以材質的 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)為基礎。</span><span class="sxs-lookup"><span data-stu-id="d819d-146">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="d819d-147">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d819d-147">Minimum Shader Model</span></span>

<span data-ttu-id="d819d-148">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="d819d-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d819d-149">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d819d-149">vs\_4\_0</span></span> | <span data-ttu-id="d819d-150">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d819d-150">vs\_4\_1</span></span>  | <span data-ttu-id="d819d-151">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d819d-151">ps\_4\_0</span></span> | <span data-ttu-id="d819d-152">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d819d-152">ps\_4\_1</span></span>  | <span data-ttu-id="d819d-153">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d819d-153">gs\_4\_0</span></span> | <span data-ttu-id="d819d-154">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d819d-154">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="d819d-155">x</span><span class="sxs-lookup"><span data-stu-id="d819d-155">x</span></span>        | <span data-ttu-id="d819d-156">x</span><span class="sxs-lookup"><span data-stu-id="d819d-156">x</span></span>         |          |           |



 

1.  <span data-ttu-id="d819d-157">TextureCubeArray 適用于著色器模型4.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="d819d-157">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="d819d-158">在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="d819d-158">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d819d-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="d819d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d819d-160">材質物件</span><span class="sxs-lookup"><span data-stu-id="d819d-160">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

