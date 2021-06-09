---
title: 材質物件
description: 在 Direct3D 10 中，您可以單獨指定取樣器和紋理;紋理取樣是使用樣板化紋理物件來執行。 這個樣板化紋理物件有特定的格式，會傳回特定的類型，並實作為數種方法。
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- 材質物件 HLSL
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1881ba4a88e97e978e2646c92d276bb9763ffd
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825768"
---
# <a name="texture-object"></a><span data-ttu-id="67661-105">材質物件</span><span class="sxs-lookup"><span data-stu-id="67661-105">Texture Object</span></span>

<span data-ttu-id="67661-106">在 Direct3D 10 中，您可以單獨指定取樣器和紋理;紋理取樣是使用樣板化紋理物件來執行。</span><span class="sxs-lookup"><span data-stu-id="67661-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="67661-107">這個樣板化紋理物件有特定的格式，會傳回特定的類型，並實作為數種方法。</span><span class="sxs-lookup"><span data-stu-id="67661-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>

<span data-ttu-id="67661-108">Direct3D9 和 Direct3D10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="67661-108">Differences between Direct3D9 and Direct3D10:</span></span>

- <span data-ttu-id="67661-109">在 Direct3D 9 中，取樣器會系結至特定紋理。</span><span class="sxs-lookup"><span data-stu-id="67661-109">In Direct3D 9, samplers are bound to specific textures.</span></span>
- <span data-ttu-id="67661-110">在 Direct3D 10 中，紋理和取樣器是獨立的物件。</span><span class="sxs-lookup"><span data-stu-id="67661-110">In Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="67661-111">每個樣板化紋理物件都會實作為材質和取樣器的材質取樣方法，以做為輸入參數。</span><span class="sxs-lookup"><span data-stu-id="67661-111">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span>



 

<span data-ttu-id="67661-112">以下是用來建立所有材質物件 (除了) 多重取樣物件以外的語法。</span><span class="sxs-lookup"><span data-stu-id="67661-112">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="67661-113">Object1 \[ < *類型* > \] *名稱*;</span><span class="sxs-lookup"><span data-stu-id="67661-113">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="67661-114">多重取樣物件 (Texture2DMS 和 Texture2DMSArray) 需要明確陳述紋理大小，並以樣本數目表示。</span><span class="sxs-lookup"><span data-stu-id="67661-114">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="67661-115">>Object2 \[ < *類型，範例* > \] *名稱*;</span><span class="sxs-lookup"><span data-stu-id="67661-115">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="67661-116">參數</span><span class="sxs-lookup"><span data-stu-id="67661-116">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67661-117">項目</span><span class="sxs-lookup"><span data-stu-id="67661-117">Item</span></span></th>
<th><span data-ttu-id="67661-118">描述</span><span class="sxs-lookup"><span data-stu-id="67661-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67661-119"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>物件</em></span><span class="sxs-lookup"><span data-stu-id="67661-119"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="67661-120">紋理物件。</span><span class="sxs-lookup"><span data-stu-id="67661-120">A texture object.</span></span> <span data-ttu-id="67661-121">必須是下列其中一種類型。</span><span class="sxs-lookup"><span data-stu-id="67661-121">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="67661-122">Object1 類型</span><span class="sxs-lookup"><span data-stu-id="67661-122">Object1 Type</span></span></th>
<th><span data-ttu-id="67661-123">描述</span><span class="sxs-lookup"><span data-stu-id="67661-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67661-124">Buffer</span><span class="sxs-lookup"><span data-stu-id="67661-124">Buffer</span></span></td>
<td><span data-ttu-id="67661-125">Buffer</span><span class="sxs-lookup"><span data-stu-id="67661-125">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="67661-126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="67661-126">Texture1D</span></span></td>
<td><span data-ttu-id="67661-127">1D 材質</span><span class="sxs-lookup"><span data-stu-id="67661-127">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67661-128">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="67661-128">Texture1DArray</span></span></td>
<td><span data-ttu-id="67661-129">1D 紋理的陣列</span><span class="sxs-lookup"><span data-stu-id="67661-129">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67661-130">Texture2D</span><span class="sxs-lookup"><span data-stu-id="67661-130">Texture2D</span></span></td>
<td><span data-ttu-id="67661-131">2D 材質</span><span class="sxs-lookup"><span data-stu-id="67661-131">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67661-132">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="67661-132">Texture2DArray</span></span></td>
<td><span data-ttu-id="67661-133">2D 材質的陣列</span><span class="sxs-lookup"><span data-stu-id="67661-133">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67661-134">Texture3D</span><span class="sxs-lookup"><span data-stu-id="67661-134">Texture3D</span></span></td>
<td><span data-ttu-id="67661-135">3D 材質</span><span class="sxs-lookup"><span data-stu-id="67661-135">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67661-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="67661-136">TextureCube</span></span></td>
<td><span data-ttu-id="67661-137">立方體材質</span><span class="sxs-lookup"><span data-stu-id="67661-137">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67661-138">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="67661-138">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="67661-139">Cube 紋理的陣列</span><span class="sxs-lookup"><span data-stu-id="67661-139">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67661-140">>Object2 類型</span><span class="sxs-lookup"><span data-stu-id="67661-140">Object2 Type</span></span></td>
<td><span data-ttu-id="67661-141">描述</span><span class="sxs-lookup"><span data-stu-id="67661-141">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67661-142">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="67661-142">Texture2DMS</span></span></td>
<td><span data-ttu-id="67661-143">2D 多重取樣材質</span><span class="sxs-lookup"><span data-stu-id="67661-143">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67661-144">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="67661-144">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="67661-145">2D 多重取樣材質的陣列</span><span class="sxs-lookup"><span data-stu-id="67661-145">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="67661-146">緩衝區類型支援大部分的材質物件方法，但 GetDimensions 除外。</span><span class="sxs-lookup"><span data-stu-id="67661-146">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="67661-147">TextureCubeArray 適用于著色器模型4.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="67661-147">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="67661-148">在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="67661-148">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67661-149"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>類型</em></span><span class="sxs-lookup"><span data-stu-id="67661-149"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="67661-150">選擇性。</span><span class="sxs-lookup"><span data-stu-id="67661-150">Optional.</span></span> <span data-ttu-id="67661-151">任何純量 <a href="dx-graphics-hlsl-scalar.md">HLSL 類型</a> 或 <a href="dx-graphics-hlsl-vector.md"><strong>向量 HLSL 類型</strong></a>（以角括弧括住）。</span><span class="sxs-lookup"><span data-stu-id="67661-151">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="67661-152">預設類型為 <strong>float4</strong>。</span><span class="sxs-lookup"><span data-stu-id="67661-152">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67661-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>名字</em></span><span class="sxs-lookup"><span data-stu-id="67661-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="67661-154">指定材質物件名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="67661-154">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67661-155"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>樣品</em></span><span class="sxs-lookup"><span data-stu-id="67661-155"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="67661-156"> (範圍介於1到 128) 之間的樣本數。</span><span class="sxs-lookup"><span data-stu-id="67661-156">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="67661-157">範例 1</span><span class="sxs-lookup"><span data-stu-id="67661-157">Example 1</span></span>

<span data-ttu-id="67661-158">以下是宣告材質物件的範例。</span><span class="sxs-lookup"><span data-stu-id="67661-158">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="67661-159">材質物件方法</span><span class="sxs-lookup"><span data-stu-id="67661-159">Texture Object Methods</span></span>

<span data-ttu-id="67661-160">每個材質物件都會執行特定方法;以下是列出所有方法的表格。</span><span class="sxs-lookup"><span data-stu-id="67661-160">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="67661-161">請參閱每個方法的參考頁面，瞭解哪些物件可以使用該方法。</span><span class="sxs-lookup"><span data-stu-id="67661-161">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="67661-162">材質方法</span><span class="sxs-lookup"><span data-stu-id="67661-162">Texture Method</span></span>                                                                     | <span data-ttu-id="67661-163">描述</span><span class="sxs-lookup"><span data-stu-id="67661-163">Description</span></span>                                                                                                       | <span data-ttu-id="67661-164">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="67661-164">vs\_4\_0</span></span> | <span data-ttu-id="67661-165">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="67661-165">vs\_4\_1</span></span>  | <span data-ttu-id="67661-166">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="67661-166">ps\_4\_0</span></span> | <span data-ttu-id="67661-167">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="67661-167">ps\_4\_1</span></span>  | <span data-ttu-id="67661-168">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="67661-168">gs\_4\_0</span></span> | <span data-ttu-id="67661-169">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="67661-169">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="67661-170">CalculateLevelOfDetail</span><span class="sxs-lookup"><span data-stu-id="67661-170">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="67661-171">計算」 LOD，傳回壓制結果。</span><span class="sxs-lookup"><span data-stu-id="67661-171">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="67661-172">x</span><span class="sxs-lookup"><span data-stu-id="67661-172">x</span></span>         |          |           |
| [<span data-ttu-id="67661-173">CalculateLevelOfDetailUnclamped</span><span class="sxs-lookup"><span data-stu-id="67661-173">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="67661-174">計算」 LOD，傳回 unclamped 結果。</span><span class="sxs-lookup"><span data-stu-id="67661-174">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="67661-175">x</span><span class="sxs-lookup"><span data-stu-id="67661-175">x</span></span>         |          |           |
| [<span data-ttu-id="67661-176">收集</span><span class="sxs-lookup"><span data-stu-id="67661-176">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="67661-177">取得 (紅色元件的四個範例，只有在取樣材質時用於雙線性插補的) 。</span><span class="sxs-lookup"><span data-stu-id="67661-177">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="67661-178">x</span><span class="sxs-lookup"><span data-stu-id="67661-178">x</span></span>         |          | <span data-ttu-id="67661-179">x</span><span class="sxs-lookup"><span data-stu-id="67661-179">x</span></span>         |          | <span data-ttu-id="67661-180">x</span><span class="sxs-lookup"><span data-stu-id="67661-180">x</span></span>         |
| [<span data-ttu-id="67661-181">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="67661-181">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="67661-182">取得指定之 mipmap 層級的材質維度。</span><span class="sxs-lookup"><span data-stu-id="67661-182">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="67661-183">x</span><span class="sxs-lookup"><span data-stu-id="67661-183">x</span></span>        | <span data-ttu-id="67661-184">x</span><span class="sxs-lookup"><span data-stu-id="67661-184">x</span></span>         | <span data-ttu-id="67661-185">x</span><span class="sxs-lookup"><span data-stu-id="67661-185">x</span></span>        | <span data-ttu-id="67661-186">x</span><span class="sxs-lookup"><span data-stu-id="67661-186">x</span></span>         | <span data-ttu-id="67661-187">x</span><span class="sxs-lookup"><span data-stu-id="67661-187">x</span></span>        | <span data-ttu-id="67661-188">x</span><span class="sxs-lookup"><span data-stu-id="67661-188">x</span></span>         |
| [<span data-ttu-id="67661-189">GetDimensions (的多級取樣) </span><span class="sxs-lookup"><span data-stu-id="67661-189">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="67661-190">取得指定之 mipmap 層級的材質維度。</span><span class="sxs-lookup"><span data-stu-id="67661-190">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="67661-191">x</span><span class="sxs-lookup"><span data-stu-id="67661-191">x</span></span>         |          | <span data-ttu-id="67661-192">x</span><span class="sxs-lookup"><span data-stu-id="67661-192">x</span></span>         |          | <span data-ttu-id="67661-193">x</span><span class="sxs-lookup"><span data-stu-id="67661-193">x</span></span>         |
| [<span data-ttu-id="67661-194">GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="67661-194">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="67661-195">取得指定範例的位置。</span><span class="sxs-lookup"><span data-stu-id="67661-195">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="67661-196">x</span><span class="sxs-lookup"><span data-stu-id="67661-196">x</span></span>         |          | <span data-ttu-id="67661-197">x</span><span class="sxs-lookup"><span data-stu-id="67661-197">x</span></span>         |          | <span data-ttu-id="67661-198">x</span><span class="sxs-lookup"><span data-stu-id="67661-198">x</span></span>         |
| [<span data-ttu-id="67661-199">載入</span><span class="sxs-lookup"><span data-stu-id="67661-199">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="67661-200">載入資料，而不進行任何篩選或取樣。</span><span class="sxs-lookup"><span data-stu-id="67661-200">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="67661-201">x</span><span class="sxs-lookup"><span data-stu-id="67661-201">x</span></span>        | <span data-ttu-id="67661-202">x</span><span class="sxs-lookup"><span data-stu-id="67661-202">x</span></span>         | <span data-ttu-id="67661-203">x</span><span class="sxs-lookup"><span data-stu-id="67661-203">x</span></span>        | <span data-ttu-id="67661-204">x</span><span class="sxs-lookup"><span data-stu-id="67661-204">x</span></span>         | <span data-ttu-id="67661-205">x</span><span class="sxs-lookup"><span data-stu-id="67661-205">x</span></span>        | <span data-ttu-id="67661-206">x</span><span class="sxs-lookup"><span data-stu-id="67661-206">x</span></span>         |
| [<span data-ttu-id="67661-207">載入 (的多重採樣) </span><span class="sxs-lookup"><span data-stu-id="67661-207">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="67661-208">載入資料，而不進行任何篩選或取樣。</span><span class="sxs-lookup"><span data-stu-id="67661-208">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="67661-209">x</span><span class="sxs-lookup"><span data-stu-id="67661-209">x</span></span>         | <span data-ttu-id="67661-210">x</span><span class="sxs-lookup"><span data-stu-id="67661-210">x</span></span>        | <span data-ttu-id="67661-211">x</span><span class="sxs-lookup"><span data-stu-id="67661-211">x</span></span>         |          | <span data-ttu-id="67661-212">x</span><span class="sxs-lookup"><span data-stu-id="67661-212">x</span></span>         |
| [<span data-ttu-id="67661-213">範例</span><span class="sxs-lookup"><span data-stu-id="67661-213">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="67661-214">範例紋理。</span><span class="sxs-lookup"><span data-stu-id="67661-214">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="67661-215">x</span><span class="sxs-lookup"><span data-stu-id="67661-215">x</span></span>        | <span data-ttu-id="67661-216">x</span><span class="sxs-lookup"><span data-stu-id="67661-216">x</span></span>         |          |           |
| [<span data-ttu-id="67661-217">SampleBias</span><span class="sxs-lookup"><span data-stu-id="67661-217">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="67661-218">將偏差值套用至 mipmap 層級之後，將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="67661-218">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="67661-219">x</span><span class="sxs-lookup"><span data-stu-id="67661-219">x</span></span>        | <span data-ttu-id="67661-220">x</span><span class="sxs-lookup"><span data-stu-id="67661-220">x</span></span>         |          |           |
| [<span data-ttu-id="67661-221">SampleCmp</span><span class="sxs-lookup"><span data-stu-id="67661-221">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="67661-222">使用比較值來拒絕範例，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="67661-222">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="67661-223">x</span><span class="sxs-lookup"><span data-stu-id="67661-223">x</span></span>        | <span data-ttu-id="67661-224">x</span><span class="sxs-lookup"><span data-stu-id="67661-224">x</span></span>         |          |           |
| [<span data-ttu-id="67661-225">SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="67661-225">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="67661-226"> (只) 使用比較值來拒絕範例的材質樣本的材質。</span><span class="sxs-lookup"><span data-stu-id="67661-226">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="67661-227">x</span><span class="sxs-lookup"><span data-stu-id="67661-227">x</span></span>        | <span data-ttu-id="67661-228">x</span><span class="sxs-lookup"><span data-stu-id="67661-228">x</span></span>         | <span data-ttu-id="67661-229">x</span><span class="sxs-lookup"><span data-stu-id="67661-229">x</span></span>        | <span data-ttu-id="67661-230">x</span><span class="sxs-lookup"><span data-stu-id="67661-230">x</span></span>         | <span data-ttu-id="67661-231">x</span><span class="sxs-lookup"><span data-stu-id="67661-231">x</span></span>        | <span data-ttu-id="67661-232">x</span><span class="sxs-lookup"><span data-stu-id="67661-232">x</span></span>         |
| [<span data-ttu-id="67661-233">SampleGrad</span><span class="sxs-lookup"><span data-stu-id="67661-233">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="67661-234">使用漸層來取樣材質，以影響範例位置的計算方式。</span><span class="sxs-lookup"><span data-stu-id="67661-234">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="67661-235">x</span><span class="sxs-lookup"><span data-stu-id="67661-235">x</span></span>        | <span data-ttu-id="67661-236">x</span><span class="sxs-lookup"><span data-stu-id="67661-236">x</span></span>         | <span data-ttu-id="67661-237">x</span><span class="sxs-lookup"><span data-stu-id="67661-237">x</span></span>        | <span data-ttu-id="67661-238">x</span><span class="sxs-lookup"><span data-stu-id="67661-238">x</span></span>         | <span data-ttu-id="67661-239">x</span><span class="sxs-lookup"><span data-stu-id="67661-239">x</span></span>        | <span data-ttu-id="67661-240">x</span><span class="sxs-lookup"><span data-stu-id="67661-240">x</span></span>         |
| [<span data-ttu-id="67661-241">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="67661-241">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="67661-242">範例指定的 mipmap 層級上的材質。</span><span class="sxs-lookup"><span data-stu-id="67661-242">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="67661-243">x</span><span class="sxs-lookup"><span data-stu-id="67661-243">x</span></span>        | <span data-ttu-id="67661-244">x</span><span class="sxs-lookup"><span data-stu-id="67661-244">x</span></span>         | <span data-ttu-id="67661-245">x</span><span class="sxs-lookup"><span data-stu-id="67661-245">x</span></span>        | <span data-ttu-id="67661-246">x</span><span class="sxs-lookup"><span data-stu-id="67661-246">x</span></span>         | <span data-ttu-id="67661-247">x</span><span class="sxs-lookup"><span data-stu-id="67661-247">x</span></span>        | <span data-ttu-id="67661-248">x</span><span class="sxs-lookup"><span data-stu-id="67661-248">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="67661-249">傳回類型</span><span class="sxs-lookup"><span data-stu-id="67661-249">Return Type</span></span>

<span data-ttu-id="67661-250">除非另有指定，否則材質物件方法的傳回型別為 float4，但多重取樣消除鋸齒紋理物件（一律需要指定類型和樣本計數）除外。</span><span class="sxs-lookup"><span data-stu-id="67661-250">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="67661-251">傳回型別與材質資源類型相同 ([**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。</span><span class="sxs-lookup"><span data-stu-id="67661-251">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="67661-252">換句話說，它可以是下列任何一種類型。</span><span class="sxs-lookup"><span data-stu-id="67661-252">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="67661-253">類型</span><span class="sxs-lookup"><span data-stu-id="67661-253">Type</span></span>                       | <span data-ttu-id="67661-254">描述</span><span class="sxs-lookup"><span data-stu-id="67661-254">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67661-255">FLOAT</span><span class="sxs-lookup"><span data-stu-id="67661-255">float</span></span>                      | <span data-ttu-id="67661-256">32-bit float (查看與 IEEE float) 差異的[浮點規則](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules)</span><span class="sxs-lookup"><span data-stu-id="67661-256">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="67661-257">int</span><span class="sxs-lookup"><span data-stu-id="67661-257">int</span></span>                        | <span data-ttu-id="67661-258">32 位元帶正負號的整數</span><span class="sxs-lookup"><span data-stu-id="67661-258">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="67661-259">不帶正負號的整數</span><span class="sxs-lookup"><span data-stu-id="67661-259">unsigned int</span></span>               | <span data-ttu-id="67661-260">32 位元不帶正負號的整數</span><span class="sxs-lookup"><span data-stu-id="67661-260">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="67661-261">snorm</span><span class="sxs-lookup"><span data-stu-id="67661-261">snorm</span></span>                      | <span data-ttu-id="67661-262">32位浮點數，範圍介於-1 到1（含） (查看與 IEEE float 之間差異的 [浮點規則](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules)) </span><span class="sxs-lookup"><span data-stu-id="67661-262">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="67661-263">unorm</span><span class="sxs-lookup"><span data-stu-id="67661-263">unorm</span></span>                      | <span data-ttu-id="67661-264">32位浮點數，範圍介於0到1（含） (查看與 IEEE float 之間差異的 [浮點規則](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules)) </span><span class="sxs-lookup"><span data-stu-id="67661-264">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="67661-265">任何材質類型或結構</span><span class="sxs-lookup"><span data-stu-id="67661-265">any texture type or struct</span></span> | <span data-ttu-id="67661-266">傳回的元件數目必須介於1到3（含）之間。</span><span class="sxs-lookup"><span data-stu-id="67661-266">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="67661-267">此外，傳回類型可以是任何材質類型（包括結構），但必須小於4個元件（例如傳回一個元件的 float1 類型）。</span><span class="sxs-lookup"><span data-stu-id="67661-267">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="67661-268">材質中遺漏元件的預設值</span><span class="sxs-lookup"><span data-stu-id="67661-268">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="67661-269">除了 Alpha 元件 () 之外，材質資源類型中遺漏元件的預設值為零。遺漏 A 的預設值是1。</span><span class="sxs-lookup"><span data-stu-id="67661-269">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="67661-270">這一種對著色器的顯示方式取決於材質資源類型。</span><span class="sxs-lookup"><span data-stu-id="67661-270">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="67661-271">它會採用實際出現在材質資源類型中的第一個具類型元件的形式 (從 RGBA 順序的左邊開始) 。</span><span class="sxs-lookup"><span data-stu-id="67661-271">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="67661-272">如果這個表單是 UNORM 或 FLOAT，則遺漏 A 的預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="67661-272">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="67661-273">如果表單為聖或 UINT，則遺漏的預設值為0x1。</span><span class="sxs-lookup"><span data-stu-id="67661-273">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="67661-274">例如，當著色器讀取 [**DXGI \_ 格式 \_ R24 \_ UNORM \_ X8 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 無類型紋理資源類型時，G 和 B 的預設值為零，而 a 的預設值為 1.0 f; 當著色器讀取 [**dxgi \_ 格式 \_ R16G16 \_ UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 材質資源類型時，B 的預設值為零，而 a 的預設值為 0x00000001; 當著色器讀取 [**DXGI \_ 格式 \_ R16 \_ 聖**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 材質資源類型時，G 和 B 的預設值為零，而的預設值為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="67661-274">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="67661-275">範例 2</span><span class="sxs-lookup"><span data-stu-id="67661-275">Example 2</span></span>

<span data-ttu-id="67661-276">以下是使用材質方法的材質取樣範例。</span><span class="sxs-lookup"><span data-stu-id="67661-276">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="67661-277">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="67661-277">Minimum Shader Model</span></span>

<span data-ttu-id="67661-278">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="67661-278">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="67661-279">著色器模型</span><span class="sxs-lookup"><span data-stu-id="67661-279">Shader Model</span></span>                                                        | <span data-ttu-id="67661-280">支援</span><span class="sxs-lookup"><span data-stu-id="67661-280">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="67661-281">[著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="67661-281">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="67661-282">是</span><span class="sxs-lookup"><span data-stu-id="67661-282">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="67661-283">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67661-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67661-284">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="67661-284">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

