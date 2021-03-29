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
ms.openlocfilehash: b075ddc1f659923efd03d9fe9d21ee3238e656e9
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104196155"
---
# <a name="texture-object"></a><span data-ttu-id="122c5-105">材質物件</span><span class="sxs-lookup"><span data-stu-id="122c5-105">Texture Object</span></span>

<span data-ttu-id="122c5-106">在 Direct3D 10 中，您可以單獨指定取樣器和紋理;紋理取樣是使用樣板化紋理物件來執行。</span><span class="sxs-lookup"><span data-stu-id="122c5-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="122c5-107">這個樣板化紋理物件有特定的格式，會傳回特定的類型，並實作為數種方法。</span><span class="sxs-lookup"><span data-stu-id="122c5-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>




|                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="122c5-108">Direct3D9 和 Direct3D10 之間的差異：在 Direct3D 9 中，取樣器會系結至特定紋理;在 Direct3D 10 中，紋理和取樣器是獨立的物件。</span><span class="sxs-lookup"><span data-stu-id="122c5-108">Differences between Direct3D9 and Direct3D10: In Direct3D 9, samplers are bound to specific textures; in Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="122c5-109">每個樣板化紋理物件都會實作為材質和取樣器的材質取樣方法，以做為輸入參數。</span><span class="sxs-lookup"><span data-stu-id="122c5-109">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span><br/> |



 

<span data-ttu-id="122c5-110">以下是用來建立所有材質物件 (除了) 多重取樣物件以外的語法。</span><span class="sxs-lookup"><span data-stu-id="122c5-110">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="122c5-111">Object1 \[ < *類型* > \] *名稱*;</span><span class="sxs-lookup"><span data-stu-id="122c5-111">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="122c5-112">多重取樣物件 (Texture2DMS 和 Texture2DMSArray) 需要明確陳述紋理大小，並以樣本數目表示。</span><span class="sxs-lookup"><span data-stu-id="122c5-112">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="122c5-113">>object2 \[ < *類型，範例* > \] *名稱*;</span><span class="sxs-lookup"><span data-stu-id="122c5-113">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="122c5-114">參數</span><span class="sxs-lookup"><span data-stu-id="122c5-114">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="122c5-115">項目</span><span class="sxs-lookup"><span data-stu-id="122c5-115">Item</span></span></th>
<th><span data-ttu-id="122c5-116">描述</span><span class="sxs-lookup"><span data-stu-id="122c5-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="122c5-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>物件</em></span><span class="sxs-lookup"><span data-stu-id="122c5-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="122c5-118">紋理物件。</span><span class="sxs-lookup"><span data-stu-id="122c5-118">A texture object.</span></span> <span data-ttu-id="122c5-119">必須是下列其中一種類型。</span><span class="sxs-lookup"><span data-stu-id="122c5-119">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="122c5-120">Object1 類型</span><span class="sxs-lookup"><span data-stu-id="122c5-120">Object1 Type</span></span></th>
<th><span data-ttu-id="122c5-121">Description</span><span class="sxs-lookup"><span data-stu-id="122c5-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="122c5-122">Buffer</span><span class="sxs-lookup"><span data-stu-id="122c5-122">Buffer</span></span></td>
<td><span data-ttu-id="122c5-123">Buffer</span><span class="sxs-lookup"><span data-stu-id="122c5-123">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="122c5-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="122c5-124">Texture1D</span></span></td>
<td><span data-ttu-id="122c5-125">1D 材質</span><span class="sxs-lookup"><span data-stu-id="122c5-125">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="122c5-126">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="122c5-126">Texture1DArray</span></span></td>
<td><span data-ttu-id="122c5-127">1D 紋理的陣列</span><span class="sxs-lookup"><span data-stu-id="122c5-127">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="122c5-128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="122c5-128">Texture2D</span></span></td>
<td><span data-ttu-id="122c5-129">2D 材質</span><span class="sxs-lookup"><span data-stu-id="122c5-129">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="122c5-130">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="122c5-130">Texture2DArray</span></span></td>
<td><span data-ttu-id="122c5-131">2D 材質的陣列</span><span class="sxs-lookup"><span data-stu-id="122c5-131">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="122c5-132">Texture3D</span><span class="sxs-lookup"><span data-stu-id="122c5-132">Texture3D</span></span></td>
<td><span data-ttu-id="122c5-133">3D 材質</span><span class="sxs-lookup"><span data-stu-id="122c5-133">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="122c5-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="122c5-134">TextureCube</span></span></td>
<td><span data-ttu-id="122c5-135">立方體材質</span><span class="sxs-lookup"><span data-stu-id="122c5-135">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="122c5-136">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="122c5-136">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="122c5-137">Cube 紋理的陣列</span><span class="sxs-lookup"><span data-stu-id="122c5-137">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="122c5-138">>object2 類型</span><span class="sxs-lookup"><span data-stu-id="122c5-138">Object2 Type</span></span></td>
<td><span data-ttu-id="122c5-139">Description</span><span class="sxs-lookup"><span data-stu-id="122c5-139">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="122c5-140">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="122c5-140">Texture2DMS</span></span></td>
<td><span data-ttu-id="122c5-141">2D 多重取樣材質</span><span class="sxs-lookup"><span data-stu-id="122c5-141">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="122c5-142">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="122c5-142">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="122c5-143">2D 多重取樣材質的陣列</span><span class="sxs-lookup"><span data-stu-id="122c5-143">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="122c5-144">緩衝區類型支援大部分的材質物件方法，但 GetDimensions 除外。</span><span class="sxs-lookup"><span data-stu-id="122c5-144">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="122c5-145">TextureCubeArray 適用于著色器模型4.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="122c5-145">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="122c5-146">在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="122c5-146">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="122c5-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>類型</em></span><span class="sxs-lookup"><span data-stu-id="122c5-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="122c5-148">選擇性。</span><span class="sxs-lookup"><span data-stu-id="122c5-148">Optional.</span></span> <span data-ttu-id="122c5-149">任何純量 <a href="dx-graphics-hlsl-scalar.md">HLSL 類型</a> 或 <a href="dx-graphics-hlsl-vector.md"><strong>向量 HLSL 類型</strong></a>（以角括弧括住）。</span><span class="sxs-lookup"><span data-stu-id="122c5-149">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="122c5-150">預設類型為 <strong>float4</strong>。</span><span class="sxs-lookup"><span data-stu-id="122c5-150">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="122c5-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>名字</em></span><span class="sxs-lookup"><span data-stu-id="122c5-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="122c5-152">指定材質物件名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="122c5-152">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="122c5-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>樣品</em></span><span class="sxs-lookup"><span data-stu-id="122c5-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="122c5-154"> (範圍介於1到 128) 之間的樣本數。</span><span class="sxs-lookup"><span data-stu-id="122c5-154">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="122c5-155">範例 1</span><span class="sxs-lookup"><span data-stu-id="122c5-155">Example 1</span></span>

<span data-ttu-id="122c5-156">以下是宣告材質物件的範例。</span><span class="sxs-lookup"><span data-stu-id="122c5-156">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="122c5-157">材質物件方法</span><span class="sxs-lookup"><span data-stu-id="122c5-157">Texture Object Methods</span></span>

<span data-ttu-id="122c5-158">每個材質物件都會執行特定方法;以下是列出所有方法的表格。</span><span class="sxs-lookup"><span data-stu-id="122c5-158">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="122c5-159">請參閱每個方法的參考頁面，瞭解哪些物件可以使用該方法。</span><span class="sxs-lookup"><span data-stu-id="122c5-159">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="122c5-160">材質方法</span><span class="sxs-lookup"><span data-stu-id="122c5-160">Texture Method</span></span>                                                                     | <span data-ttu-id="122c5-161">Description</span><span class="sxs-lookup"><span data-stu-id="122c5-161">Description</span></span>                                                                                                       | <span data-ttu-id="122c5-162">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="122c5-162">vs\_4\_0</span></span> | <span data-ttu-id="122c5-163">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="122c5-163">vs\_4\_1</span></span>  | <span data-ttu-id="122c5-164">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="122c5-164">ps\_4\_0</span></span> | <span data-ttu-id="122c5-165">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="122c5-165">ps\_4\_1</span></span>  | <span data-ttu-id="122c5-166">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="122c5-166">gs\_4\_0</span></span> | <span data-ttu-id="122c5-167">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="122c5-167">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="122c5-168">CalculateLevelOfDetail</span><span class="sxs-lookup"><span data-stu-id="122c5-168">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="122c5-169">計算」 LOD，傳回壓制結果。</span><span class="sxs-lookup"><span data-stu-id="122c5-169">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="122c5-170">x</span><span class="sxs-lookup"><span data-stu-id="122c5-170">x</span></span>         |          |           |
| [<span data-ttu-id="122c5-171">CalculateLevelOfDetailUnclamped</span><span class="sxs-lookup"><span data-stu-id="122c5-171">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="122c5-172">計算」 LOD，傳回 unclamped 結果。</span><span class="sxs-lookup"><span data-stu-id="122c5-172">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="122c5-173">x</span><span class="sxs-lookup"><span data-stu-id="122c5-173">x</span></span>         |          |           |
| [<span data-ttu-id="122c5-174">收集</span><span class="sxs-lookup"><span data-stu-id="122c5-174">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="122c5-175">取得 (紅色元件的四個範例，只有在取樣材質時用於雙線性插補的) 。</span><span class="sxs-lookup"><span data-stu-id="122c5-175">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="122c5-176">x</span><span class="sxs-lookup"><span data-stu-id="122c5-176">x</span></span>         |          | <span data-ttu-id="122c5-177">x</span><span class="sxs-lookup"><span data-stu-id="122c5-177">x</span></span>         |          | <span data-ttu-id="122c5-178">x</span><span class="sxs-lookup"><span data-stu-id="122c5-178">x</span></span>         |
| [<span data-ttu-id="122c5-179">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="122c5-179">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="122c5-180">取得指定之 mipmap 層級的材質維度。</span><span class="sxs-lookup"><span data-stu-id="122c5-180">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="122c5-181">x</span><span class="sxs-lookup"><span data-stu-id="122c5-181">x</span></span>        | <span data-ttu-id="122c5-182">x</span><span class="sxs-lookup"><span data-stu-id="122c5-182">x</span></span>         | <span data-ttu-id="122c5-183">x</span><span class="sxs-lookup"><span data-stu-id="122c5-183">x</span></span>        | <span data-ttu-id="122c5-184">x</span><span class="sxs-lookup"><span data-stu-id="122c5-184">x</span></span>         | <span data-ttu-id="122c5-185">x</span><span class="sxs-lookup"><span data-stu-id="122c5-185">x</span></span>        | <span data-ttu-id="122c5-186">x</span><span class="sxs-lookup"><span data-stu-id="122c5-186">x</span></span>         |
| [<span data-ttu-id="122c5-187">GetDimensions (的多級取樣) </span><span class="sxs-lookup"><span data-stu-id="122c5-187">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="122c5-188">取得指定之 mipmap 層級的材質維度。</span><span class="sxs-lookup"><span data-stu-id="122c5-188">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="122c5-189">x</span><span class="sxs-lookup"><span data-stu-id="122c5-189">x</span></span>         |          | <span data-ttu-id="122c5-190">x</span><span class="sxs-lookup"><span data-stu-id="122c5-190">x</span></span>         |          | <span data-ttu-id="122c5-191">x</span><span class="sxs-lookup"><span data-stu-id="122c5-191">x</span></span>         |
| [<span data-ttu-id="122c5-192">GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="122c5-192">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="122c5-193">取得指定範例的位置。</span><span class="sxs-lookup"><span data-stu-id="122c5-193">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="122c5-194">x</span><span class="sxs-lookup"><span data-stu-id="122c5-194">x</span></span>         |          | <span data-ttu-id="122c5-195">x</span><span class="sxs-lookup"><span data-stu-id="122c5-195">x</span></span>         |          | <span data-ttu-id="122c5-196">x</span><span class="sxs-lookup"><span data-stu-id="122c5-196">x</span></span>         |
| [<span data-ttu-id="122c5-197">載入</span><span class="sxs-lookup"><span data-stu-id="122c5-197">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="122c5-198">載入資料，而不進行任何篩選或取樣。</span><span class="sxs-lookup"><span data-stu-id="122c5-198">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="122c5-199">x</span><span class="sxs-lookup"><span data-stu-id="122c5-199">x</span></span>        | <span data-ttu-id="122c5-200">x</span><span class="sxs-lookup"><span data-stu-id="122c5-200">x</span></span>         | <span data-ttu-id="122c5-201">x</span><span class="sxs-lookup"><span data-stu-id="122c5-201">x</span></span>        | <span data-ttu-id="122c5-202">x</span><span class="sxs-lookup"><span data-stu-id="122c5-202">x</span></span>         | <span data-ttu-id="122c5-203">x</span><span class="sxs-lookup"><span data-stu-id="122c5-203">x</span></span>        | <span data-ttu-id="122c5-204">x</span><span class="sxs-lookup"><span data-stu-id="122c5-204">x</span></span>         |
| [<span data-ttu-id="122c5-205">載入 (的多重採樣) </span><span class="sxs-lookup"><span data-stu-id="122c5-205">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="122c5-206">載入資料，而不進行任何篩選或取樣。</span><span class="sxs-lookup"><span data-stu-id="122c5-206">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="122c5-207">x</span><span class="sxs-lookup"><span data-stu-id="122c5-207">x</span></span>         | <span data-ttu-id="122c5-208">x</span><span class="sxs-lookup"><span data-stu-id="122c5-208">x</span></span>        | <span data-ttu-id="122c5-209">x</span><span class="sxs-lookup"><span data-stu-id="122c5-209">x</span></span>         |          | <span data-ttu-id="122c5-210">x</span><span class="sxs-lookup"><span data-stu-id="122c5-210">x</span></span>         |
| [<span data-ttu-id="122c5-211">範例</span><span class="sxs-lookup"><span data-stu-id="122c5-211">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="122c5-212">範例紋理。</span><span class="sxs-lookup"><span data-stu-id="122c5-212">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="122c5-213">x</span><span class="sxs-lookup"><span data-stu-id="122c5-213">x</span></span>        | <span data-ttu-id="122c5-214">x</span><span class="sxs-lookup"><span data-stu-id="122c5-214">x</span></span>         |          |           |
| [<span data-ttu-id="122c5-215">SampleBias</span><span class="sxs-lookup"><span data-stu-id="122c5-215">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="122c5-216">將偏差值套用至 mipmap 層級之後，將材質取樣。</span><span class="sxs-lookup"><span data-stu-id="122c5-216">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="122c5-217">x</span><span class="sxs-lookup"><span data-stu-id="122c5-217">x</span></span>        | <span data-ttu-id="122c5-218">x</span><span class="sxs-lookup"><span data-stu-id="122c5-218">x</span></span>         |          |           |
| [<span data-ttu-id="122c5-219">SampleCmp</span><span class="sxs-lookup"><span data-stu-id="122c5-219">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="122c5-220">使用比較值來拒絕範例，以取樣材質。</span><span class="sxs-lookup"><span data-stu-id="122c5-220">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="122c5-221">x</span><span class="sxs-lookup"><span data-stu-id="122c5-221">x</span></span>        | <span data-ttu-id="122c5-222">x</span><span class="sxs-lookup"><span data-stu-id="122c5-222">x</span></span>         |          |           |
| [<span data-ttu-id="122c5-223">SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="122c5-223">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="122c5-224"> (只) 使用比較值來拒絕範例的材質樣本的材質。</span><span class="sxs-lookup"><span data-stu-id="122c5-224">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="122c5-225">x</span><span class="sxs-lookup"><span data-stu-id="122c5-225">x</span></span>        | <span data-ttu-id="122c5-226">x</span><span class="sxs-lookup"><span data-stu-id="122c5-226">x</span></span>         | <span data-ttu-id="122c5-227">x</span><span class="sxs-lookup"><span data-stu-id="122c5-227">x</span></span>        | <span data-ttu-id="122c5-228">x</span><span class="sxs-lookup"><span data-stu-id="122c5-228">x</span></span>         | <span data-ttu-id="122c5-229">x</span><span class="sxs-lookup"><span data-stu-id="122c5-229">x</span></span>        | <span data-ttu-id="122c5-230">x</span><span class="sxs-lookup"><span data-stu-id="122c5-230">x</span></span>         |
| [<span data-ttu-id="122c5-231">SampleGrad</span><span class="sxs-lookup"><span data-stu-id="122c5-231">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="122c5-232">使用漸層來取樣材質，以影響範例位置的計算方式。</span><span class="sxs-lookup"><span data-stu-id="122c5-232">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="122c5-233">x</span><span class="sxs-lookup"><span data-stu-id="122c5-233">x</span></span>        | <span data-ttu-id="122c5-234">x</span><span class="sxs-lookup"><span data-stu-id="122c5-234">x</span></span>         | <span data-ttu-id="122c5-235">x</span><span class="sxs-lookup"><span data-stu-id="122c5-235">x</span></span>        | <span data-ttu-id="122c5-236">x</span><span class="sxs-lookup"><span data-stu-id="122c5-236">x</span></span>         | <span data-ttu-id="122c5-237">x</span><span class="sxs-lookup"><span data-stu-id="122c5-237">x</span></span>        | <span data-ttu-id="122c5-238">x</span><span class="sxs-lookup"><span data-stu-id="122c5-238">x</span></span>         |
| [<span data-ttu-id="122c5-239">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="122c5-239">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="122c5-240">範例指定的 mipmap 層級上的材質。</span><span class="sxs-lookup"><span data-stu-id="122c5-240">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="122c5-241">x</span><span class="sxs-lookup"><span data-stu-id="122c5-241">x</span></span>        | <span data-ttu-id="122c5-242">x</span><span class="sxs-lookup"><span data-stu-id="122c5-242">x</span></span>         | <span data-ttu-id="122c5-243">x</span><span class="sxs-lookup"><span data-stu-id="122c5-243">x</span></span>        | <span data-ttu-id="122c5-244">x</span><span class="sxs-lookup"><span data-stu-id="122c5-244">x</span></span>         | <span data-ttu-id="122c5-245">x</span><span class="sxs-lookup"><span data-stu-id="122c5-245">x</span></span>        | <span data-ttu-id="122c5-246">x</span><span class="sxs-lookup"><span data-stu-id="122c5-246">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="122c5-247">傳回類型</span><span class="sxs-lookup"><span data-stu-id="122c5-247">Return Type</span></span>

<span data-ttu-id="122c5-248">除非另有指定，否則材質物件方法的傳回型別為 float4，但多重取樣消除鋸齒紋理物件（一律需要指定類型和樣本計數）除外。</span><span class="sxs-lookup"><span data-stu-id="122c5-248">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="122c5-249">傳回型別與材質資源類型相同 ([**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。</span><span class="sxs-lookup"><span data-stu-id="122c5-249">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="122c5-250">換句話說，它可以是下列任何一種類型。</span><span class="sxs-lookup"><span data-stu-id="122c5-250">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="122c5-251">類型</span><span class="sxs-lookup"><span data-stu-id="122c5-251">Type</span></span>                       | <span data-ttu-id="122c5-252">Description</span><span class="sxs-lookup"><span data-stu-id="122c5-252">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="122c5-253">FLOAT</span><span class="sxs-lookup"><span data-stu-id="122c5-253">float</span></span>                      | <span data-ttu-id="122c5-254">32-bit float (查看與 IEEE float) 差異的[浮點規則](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules)</span><span class="sxs-lookup"><span data-stu-id="122c5-254">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="122c5-255">int</span><span class="sxs-lookup"><span data-stu-id="122c5-255">int</span></span>                        | <span data-ttu-id="122c5-256">32 位元帶正負號的整數</span><span class="sxs-lookup"><span data-stu-id="122c5-256">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="122c5-257">不帶正負號的整數</span><span class="sxs-lookup"><span data-stu-id="122c5-257">unsigned int</span></span>               | <span data-ttu-id="122c5-258">32 位元不帶正負號的整數</span><span class="sxs-lookup"><span data-stu-id="122c5-258">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="122c5-259">snorm</span><span class="sxs-lookup"><span data-stu-id="122c5-259">snorm</span></span>                      | <span data-ttu-id="122c5-260">32位浮點數，範圍介於-1 到1（含） (查看與 IEEE float 之間差異的 [浮點規則](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules)) </span><span class="sxs-lookup"><span data-stu-id="122c5-260">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="122c5-261">unorm</span><span class="sxs-lookup"><span data-stu-id="122c5-261">unorm</span></span>                      | <span data-ttu-id="122c5-262">32位浮點數，範圍介於0到1（含） (查看與 IEEE float 之間差異的 [浮點規則](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules)) </span><span class="sxs-lookup"><span data-stu-id="122c5-262">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="122c5-263">任何材質類型或結構</span><span class="sxs-lookup"><span data-stu-id="122c5-263">any texture type or struct</span></span> | <span data-ttu-id="122c5-264">傳回的元件數目必須介於1到3（含）之間。</span><span class="sxs-lookup"><span data-stu-id="122c5-264">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="122c5-265">此外，傳回類型可以是任何材質類型（包括結構），但必須小於4個元件（例如傳回一個元件的 float1 類型）。</span><span class="sxs-lookup"><span data-stu-id="122c5-265">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="122c5-266">材質中遺漏元件的預設值</span><span class="sxs-lookup"><span data-stu-id="122c5-266">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="122c5-267">除了 Alpha 元件 () 之外，材質資源類型中遺漏元件的預設值為零。遺漏 A 的預設值是1。</span><span class="sxs-lookup"><span data-stu-id="122c5-267">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="122c5-268">這一種對著色器的顯示方式取決於材質資源類型。</span><span class="sxs-lookup"><span data-stu-id="122c5-268">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="122c5-269">它會採用實際出現在材質資源類型中的第一個具類型元件的形式 (從 RGBA 順序的左邊開始) 。</span><span class="sxs-lookup"><span data-stu-id="122c5-269">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="122c5-270">如果這個表單是 UNORM 或 FLOAT，則遺漏 A 的預設值為 1.0 f。</span><span class="sxs-lookup"><span data-stu-id="122c5-270">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="122c5-271">如果表單為聖或 UINT，則遺漏的預設值為0x1。</span><span class="sxs-lookup"><span data-stu-id="122c5-271">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="122c5-272">例如，當著色器讀取 [**DXGI \_ 格式 \_ R24 \_ UNORM \_ X8 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 無類型紋理資源類型時，G 和 B 的預設值為零，而 a 的預設值為 1.0 f; 當著色器讀取 [**dxgi \_ 格式 \_ R16G16 \_ UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 材質資源類型時，B 的預設值為零，而 a 的預設值為 0x00000001; 當著色器讀取 [**DXGI \_ 格式 \_ R16 \_ 聖**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 材質資源類型時，G 和 B 的預設值為零，而的預設值為0x00000001。</span><span class="sxs-lookup"><span data-stu-id="122c5-272">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="122c5-273">範例 2</span><span class="sxs-lookup"><span data-stu-id="122c5-273">Example 2</span></span>

<span data-ttu-id="122c5-274">以下是使用材質方法的材質取樣範例。</span><span class="sxs-lookup"><span data-stu-id="122c5-274">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="122c5-275">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="122c5-275">Minimum Shader Model</span></span>

<span data-ttu-id="122c5-276">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="122c5-276">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="122c5-277">著色器模型</span><span class="sxs-lookup"><span data-stu-id="122c5-277">Shader Model</span></span>                                                        | <span data-ttu-id="122c5-278">支援</span><span class="sxs-lookup"><span data-stu-id="122c5-278">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="122c5-279">[著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型</span><span class="sxs-lookup"><span data-stu-id="122c5-279">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="122c5-280">是</span><span class="sxs-lookup"><span data-stu-id="122c5-280">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="122c5-281">另請參閱</span><span class="sxs-lookup"><span data-stu-id="122c5-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="122c5-282">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="122c5-282">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

