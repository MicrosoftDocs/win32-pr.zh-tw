---
title: 'SampleLevel (DirectX HLSL 材質物件) '
description: 使用 mipmap 層級位移來取樣材質。
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bc3a074641ce5b15a3d837e8bd91dfdae09fe627
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826682"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a><span data-ttu-id="0234a-103">SampleLevel (DirectX HLSL 材質物件) </span><span class="sxs-lookup"><span data-stu-id="0234a-103">SampleLevel (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="0234a-104">使用 mipmap 層級位移來取樣材質。</span><span class="sxs-lookup"><span data-stu-id="0234a-104">Samples a texture using a mipmap-level offset.</span></span>

<span data-ttu-id="0234a-105">&lt;樣板類型 &gt; Object. SampleLevel ( 取樣器 \_ 狀態 S、float 位置、float」 lod \[ 、int Offset \] ) ;</span><span class="sxs-lookup"><span data-stu-id="0234a-105">&lt;Template Type&gt; Object.SampleLevel( sampler\_state S, float Location, float LOD \[, int Offset\] );</span></span>



 

<span data-ttu-id="0234a-106">此函式類似于 [範例](dx-graphics-hlsl-to-sample.md) ，不同之處在于它會使用 location 參數的最後一個元件中的」 lod 層級 () 來選擇 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="0234a-106">This function is similar to [Sample](dx-graphics-hlsl-to-sample.md) except that it uses the LOD level (in the last component of the location parameter) to choose the mipmap level.</span></span> <span data-ttu-id="0234a-107">例如，2D 材質針對 uv 座標使用前兩個元件，並使用 mipmap 層級的第三個元件。</span><span class="sxs-lookup"><span data-stu-id="0234a-107">For example, a 2D texture uses the first two components for uv coordinates and the third component for the mipmap level.</span></span>

## <a name="parameters"></a><span data-ttu-id="0234a-108">參數</span><span class="sxs-lookup"><span data-stu-id="0234a-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0234a-109">項目</span><span class="sxs-lookup"><span data-stu-id="0234a-109">Item</span></span></th>
<th><span data-ttu-id="0234a-110">描述</span><span class="sxs-lookup"><span data-stu-id="0234a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0234a-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>物件</em></span><span class="sxs-lookup"><span data-stu-id="0234a-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="0234a-112">任何 <a href="dx-graphics-hlsl-to-type.md">材質物件</a> 類型 (除了 Texture2DMS 和 Texture2DMSArray) 之外。</span><span class="sxs-lookup"><span data-stu-id="0234a-112">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0234a-113"><span id="S"></span><span id="s"></span><em>！</em></span><span class="sxs-lookup"><span data-stu-id="0234a-113"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="0234a-114">在 <a href="dx-graphics-hlsl-sampler.md">取樣器狀態</a>。</span><span class="sxs-lookup"><span data-stu-id="0234a-114">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="0234a-115">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="0234a-115">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0234a-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>位置</em></span><span class="sxs-lookup"><span data-stu-id="0234a-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="0234a-117">在材質座標。</span><span class="sxs-lookup"><span data-stu-id="0234a-117">[in] The texture coordinates.</span></span> <span data-ttu-id="0234a-118">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="0234a-118">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0234a-119">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="0234a-119">Texture-Object Type</span></span></th>
<th><span data-ttu-id="0234a-120">參數類型</span><span class="sxs-lookup"><span data-stu-id="0234a-120">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0234a-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="0234a-121">Texture1D</span></span></td>
<td><span data-ttu-id="0234a-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0234a-122">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0234a-123">Texture1DArray、Texture2D</span><span class="sxs-lookup"><span data-stu-id="0234a-123">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="0234a-124">float2</span><span class="sxs-lookup"><span data-stu-id="0234a-124">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0234a-125">Texture2DArray, Texture3D, TextureCube</span><span class="sxs-lookup"><span data-stu-id="0234a-125">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="0234a-126">float3</span><span class="sxs-lookup"><span data-stu-id="0234a-126">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0234a-127">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0234a-127">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="0234a-128">float4</span><span class="sxs-lookup"><span data-stu-id="0234a-128">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="0234a-129">如果材質物件是陣列，則最後一個元件是陣列索引。</span><span class="sxs-lookup"><span data-stu-id="0234a-129">If the texture object is an array, the last component is the array index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0234a-130"><span id="LOD"></span><span id="lod"></span><em>Lod</em></span><span class="sxs-lookup"><span data-stu-id="0234a-130"><span id="LOD"></span><span id="lod"></span><em>LOD</em></span></span></p></td>
<td><p><span data-ttu-id="0234a-131">在指定 mipmap 層級的數位。</span><span class="sxs-lookup"><span data-stu-id="0234a-131">[in] A number that specifies the mipmap level.</span></span> <span data-ttu-id="0234a-132">如果值為 = 0，則會使用 zero'th (最大的對應) 。</span><span class="sxs-lookup"><span data-stu-id="0234a-132">If the value is = 0, the zero'th (biggest map) is used.</span></span> <span data-ttu-id="0234a-133">小數值 (如果提供的) 用來在兩個 mipmap 層級之間插補。</span><span class="sxs-lookup"><span data-stu-id="0234a-133">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0234a-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>抵消</em></span><span class="sxs-lookup"><span data-stu-id="0234a-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="0234a-135">在選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="0234a-135">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="0234a-136">材質位移必須是靜態的。</span><span class="sxs-lookup"><span data-stu-id="0234a-136">The texture offsets need to be static.</span></span> <span data-ttu-id="0234a-137">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="0234a-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="0234a-138">如需詳細資訊，請參閱套用 <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">材質座標位移</a>。</span><span class="sxs-lookup"><span data-stu-id="0234a-138">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0234a-139">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="0234a-139">Texture-Object Type</span></span></th>
<th><span data-ttu-id="0234a-140">參數類型</span><span class="sxs-lookup"><span data-stu-id="0234a-140">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0234a-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="0234a-141">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="0234a-142">int</span><span class="sxs-lookup"><span data-stu-id="0234a-142">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0234a-143">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="0234a-143">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="0234a-144">int2</span><span class="sxs-lookup"><span data-stu-id="0234a-144">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0234a-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="0234a-145">Texture3D</span></span></td>
<td><span data-ttu-id="0234a-146">int3</span><span class="sxs-lookup"><span data-stu-id="0234a-146">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0234a-147">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="0234a-147">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="0234a-148">不支援</span><span class="sxs-lookup"><span data-stu-id="0234a-148">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="0234a-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="0234a-149">Return Value</span></span>

<span data-ttu-id="0234a-150">紋理的範本類型，可能是單一或多元件向量。</span><span class="sxs-lookup"><span data-stu-id="0234a-150">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="0234a-151">格式是以材質的 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)為基礎。</span><span class="sxs-lookup"><span data-stu-id="0234a-151">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="0234a-152">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="0234a-152">Minimum Shader Model</span></span>

<span data-ttu-id="0234a-153">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="0234a-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0234a-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0234a-154">vs\_4\_0</span></span> | <span data-ttu-id="0234a-155">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0234a-155">vs\_4\_1</span></span>  | <span data-ttu-id="0234a-156">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0234a-156">ps\_4\_0</span></span> | <span data-ttu-id="0234a-157">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0234a-157">ps\_4\_1</span></span>  | <span data-ttu-id="0234a-158">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0234a-158">gs\_4\_0</span></span> | <span data-ttu-id="0234a-159">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="0234a-159">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="0234a-160">x</span><span class="sxs-lookup"><span data-stu-id="0234a-160">x</span></span>        | <span data-ttu-id="0234a-161">x</span><span class="sxs-lookup"><span data-stu-id="0234a-161">x</span></span>         | <span data-ttu-id="0234a-162">x</span><span class="sxs-lookup"><span data-stu-id="0234a-162">x</span></span>        | <span data-ttu-id="0234a-163">x</span><span class="sxs-lookup"><span data-stu-id="0234a-163">x</span></span>         | <span data-ttu-id="0234a-164">x</span><span class="sxs-lookup"><span data-stu-id="0234a-164">x</span></span>        | <span data-ttu-id="0234a-165">x</span><span class="sxs-lookup"><span data-stu-id="0234a-165">x</span></span>         |



 

1.  <span data-ttu-id="0234a-166">TextureCubeArray 適用于著色器模型4.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="0234a-166">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="0234a-167">在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="0234a-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="0234a-168">範例</span><span class="sxs-lookup"><span data-stu-id="0234a-168">Example</span></span>

<span data-ttu-id="0234a-169">這個部分程式碼範例是來自 [Instancing10 範例](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx)中的實例 fx 檔案。</span><span class="sxs-lookup"><span data-stu-id="0234a-169">This partial code example is from the Instancing.fx file in the [Instancing10 Sample](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span></span>


```
// Object Declarations
Texture1D g_txRandom;

SamplerState g_samPoint
{
    Filter = MIN_MAG_MIP_POINT;
    AddressU = Wrap;
    AddressV = Wrap;
};

    
// Shader body calling the intrinsic function
float3 RandomDir(float fOffset)
{   
    float tCoord = (fOffset) / 300.0;
    return g_txRandom.SampleLevel( g_samPoint, tCoord, 0 );
   ...

```



## <a name="related-topics"></a><span data-ttu-id="0234a-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="0234a-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0234a-171">材質物件</span><span class="sxs-lookup"><span data-stu-id="0234a-171">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

