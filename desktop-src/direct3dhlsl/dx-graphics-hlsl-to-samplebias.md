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
# <a name="samplebias-directx-hlsl-texture-object"></a>SampleBias (DirectX HLSL 材質物件) 

將輸入偏差套用至 mipmap 層級之後，將材質取樣。



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| &lt;樣板類型 &gt; Object. SampleBias ( 取樣器 \_ 狀態 S、浮點位置、浮點數偏差 \[ 、int 位移 \] ) ; |



 

## <a name="parameters"></a>參數



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>項目</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>物件</em><br/></td>
<td>任何 <a href="dx-graphics-hlsl-to-type.md">材質物件</a> 類型 (除了 Texture2DMS 和 Texture2DMSArray) 之外。<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>！</em><br/></td>
<td>在 <a href="dx-graphics-hlsl-sampler.md">取樣器狀態</a>。 這是在包含狀態指派的效果檔案中宣告的物件。<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>位置</em><br/></td>
<td>在材質座標。 引數類型相依于材質物件類型。 <br/> 
<table>
<thead>
<tr class="header">
<th>Texture-Object 類型</th>
<th>參數類型</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D</td>
<td>FLOAT</td>
</tr>
<tr class="even">
<td>Texture1DArray、Texture2D</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture2DArray, Texture3D, TextureCube</td>
<td>float3</td>
</tr>
<tr class="even">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>偏見</em></p></td>
<td><p>在偏差值（介於-16.0 和15.99 之間的浮點數）會在取樣之前套用至 mip 層級。</p></td>
</tr>
<tr class="odd">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>抵消</em></p></td>
<td><p>在選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。 材質位移必須是靜態的。 引數類型相依于材質物件類型。 如需詳細資訊，請參閱套用 <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">材質座標位移</a>。</p>

<table>
<thead>
<tr class="header">
<th>Texture-Object 類型</th>
<th>參數類型</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>int</td>
</tr>
<tr class="even">
<td>Texture2D、Texture2DArray</td>
<td>int2</td>
</tr>
<tr class="odd">
<td>Texture3D</td>
<td>int3</td>
</tr>
<tr class="even">
<td>TextureCube, TextureCubeArray </td>
<td>不支援</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>傳回值

紋理的範本類型，可能是單一或多元件向量。 格式是以材質的 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)為基礎。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x        | x         |          |           |



 

1.  TextureCubeArray 適用于著色器模型4.1 或更高版本。
2.  在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質物件](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

