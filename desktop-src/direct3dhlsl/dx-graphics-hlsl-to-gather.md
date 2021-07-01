---
title: '收集 (DirectX HLSL 材質物件) '
description: 取得 (紅色元件的四個範例，只有在取樣材質時用於雙線性插補的) 。
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4659ba19e9fa950a659969f2491533858f4658fb
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120543"
---
# <a name="gather-directx-hlsl-texture-object"></a><span data-ttu-id="10d33-103">收集 (DirectX HLSL 材質物件) </span><span class="sxs-lookup"><span data-stu-id="10d33-103">Gather (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="10d33-104">取得 (紅色元件的四個範例，只有在取樣材質時用於雙線性插補的) 。</span><span class="sxs-lookup"><span data-stu-id="10d33-104">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span>

<span data-ttu-id="10d33-105">&lt;範本類型 &gt; 4 物件。收集 ( 取樣器 \_ 狀態 S、float2 \| 3 \| 4 位置 \[ 、int2 位移 \] ) ;</span><span class="sxs-lookup"><span data-stu-id="10d33-105">&lt;Template Type&gt;4 Object.Gather( sampler\_state S, float2\|3\|4 Location \[, int2 Offset\] );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="10d33-106">參數</span><span class="sxs-lookup"><span data-stu-id="10d33-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10d33-107">項目</span><span class="sxs-lookup"><span data-stu-id="10d33-107">Item</span></span></th>
<th><span data-ttu-id="10d33-108">描述</span><span class="sxs-lookup"><span data-stu-id="10d33-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10d33-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>物件</em></span><span class="sxs-lookup"><span data-stu-id="10d33-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="10d33-110">以下是支援的 <a href="dx-graphics-hlsl-to-type.md">材質物件</a> 類型： Texture2D、Texture2DArray、TextureCube、TextureCubeArray。</span><span class="sxs-lookup"><span data-stu-id="10d33-110">The following <a href="dx-graphics-hlsl-to-type.md">texture-object</a> types are supported: Texture2D, Texture2DArray, TextureCube, TextureCubeArray.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10d33-111"><span id="S"></span><span id="s"></span><em>！</em></span><span class="sxs-lookup"><span data-stu-id="10d33-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="10d33-112">在 <a href="dx-graphics-hlsl-sampler.md">取樣器狀態</a>。</span><span class="sxs-lookup"><span data-stu-id="10d33-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="10d33-113">這是在包含狀態指派的效果檔案中宣告的物件。</span><span class="sxs-lookup"><span data-stu-id="10d33-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10d33-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>位置</em></span><span class="sxs-lookup"><span data-stu-id="10d33-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="10d33-115">在材質座標。</span><span class="sxs-lookup"><span data-stu-id="10d33-115">[in] The texture coordinates.</span></span> <span data-ttu-id="10d33-116">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="10d33-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10d33-117">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="10d33-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="10d33-118">參數類型</span><span class="sxs-lookup"><span data-stu-id="10d33-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10d33-119">Texture2D</span><span class="sxs-lookup"><span data-stu-id="10d33-119">Texture2D</span></span></td>
<td><span data-ttu-id="10d33-120">float2</span><span class="sxs-lookup"><span data-stu-id="10d33-120">float2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10d33-121">Texture2DArray, TextureCube</span><span class="sxs-lookup"><span data-stu-id="10d33-121">Texture2DArray, TextureCube</span></span></td>
<td><span data-ttu-id="10d33-122">float3</span><span class="sxs-lookup"><span data-stu-id="10d33-122">float3</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10d33-123">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="10d33-123">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="10d33-124">float4</span><span class="sxs-lookup"><span data-stu-id="10d33-124">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10d33-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>抵消</em></span><span class="sxs-lookup"><span data-stu-id="10d33-125"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="10d33-126">在選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。</span><span class="sxs-lookup"><span data-stu-id="10d33-126">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="10d33-127">引數類型相依于材質物件類型。</span><span class="sxs-lookup"><span data-stu-id="10d33-127">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="10d33-128">針對以著色器模型5.0 和更新版本為目標的著色器，每個位移值的6個最低有效位會視為帶正負號的值，並產生 [-32.. 31] 範圍。</span><span class="sxs-lookup"><span data-stu-id="10d33-128">For shaders targeting Shader Model 5.0 and above, the 6 least significant bits of each offset value is honored as a signed value, yielding [-32..31] range.</span></span> <span data-ttu-id="10d33-129">針對先前的著色器模型著色器，位移必須是-8 到7之間的立即整數。</span><span class="sxs-lookup"><span data-stu-id="10d33-129">For previous shader model shaders, offsets need to be immediate integers between -8 and 7.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="10d33-130">Texture-Object 類型</span><span class="sxs-lookup"><span data-stu-id="10d33-130">Texture-Object Type</span></span></th>
<th><span data-ttu-id="10d33-131">參數類型</span><span class="sxs-lookup"><span data-stu-id="10d33-131">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10d33-132">Texture2D、Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="10d33-132">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="10d33-133">int2</span><span class="sxs-lookup"><span data-stu-id="10d33-133">int2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10d33-134">TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="10d33-134">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="10d33-135">不支援</span><span class="sxs-lookup"><span data-stu-id="10d33-135">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="10d33-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="10d33-136">Return Value</span></span>

<span data-ttu-id="10d33-137">四個元件的向量，具有四個紅色資料的元件，其類型與材質的範本類型相同。</span><span class="sxs-lookup"><span data-stu-id="10d33-137">A four-component vector, with four components of red data, whose type is the same as the texture's template type.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="10d33-138">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="10d33-138">Minimum Shader Model</span></span>

<span data-ttu-id="10d33-139">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="10d33-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="10d33-140">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10d33-140">vs\_4\_0</span></span> | <span data-ttu-id="10d33-141">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="10d33-141">vs\_4\_1</span></span>  | <span data-ttu-id="10d33-142">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10d33-142">ps\_4\_0</span></span> | <span data-ttu-id="10d33-143">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="10d33-143">ps\_4\_1</span></span>  | <span data-ttu-id="10d33-144">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="10d33-144">gs\_4\_0</span></span> | <span data-ttu-id="10d33-145">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="10d33-145">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="10d33-146">x</span><span class="sxs-lookup"><span data-stu-id="10d33-146">x</span></span>         |          | <span data-ttu-id="10d33-147">x</span><span class="sxs-lookup"><span data-stu-id="10d33-147">x</span></span>         |          | <span data-ttu-id="10d33-148">x</span><span class="sxs-lookup"><span data-stu-id="10d33-148">x</span></span>         |



 

1.  <span data-ttu-id="10d33-149">TextureCubeArray 適用于著色器模型4.1 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="10d33-149">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="10d33-150">在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</span><span class="sxs-lookup"><span data-stu-id="10d33-150">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="10d33-151">範例</span><span class="sxs-lookup"><span data-stu-id="10d33-151">Example</span></span>


```
Texture2D<int1> Tex2d;
Texture2DArray<int2> Tex2dArray;
TextureCube<int3> TexCube;
TextureCubeArray<float2> TexCubeArray;

SamplerState s;

int4 main (float4 f : SV_Position) : SV_Target
{
    int2 iOffset = int2(2,3);

    int4 i1 = Tex2d.Gather(s, f.xy);
    int4 i2 = Tex2d.Gather(s, f.xy, iOffset);

    int4 i3 = Tex2dArray.Gather(s, f.xyz);
    int4 i4 = Tex2dArray.Gather(s, f.xyz, iOffset);

    int4 i5 = TexCube.Gather(s, f.xyzw);

    float4 f6 = TexCubeArray.Gather(s, f.xyzw);

    return i1+i2+i3+i4+i5+int4(i6);
}
  
```



## <a name="related-topics"></a><span data-ttu-id="10d33-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="10d33-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10d33-153">材質物件</span><span class="sxs-lookup"><span data-stu-id="10d33-153">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





