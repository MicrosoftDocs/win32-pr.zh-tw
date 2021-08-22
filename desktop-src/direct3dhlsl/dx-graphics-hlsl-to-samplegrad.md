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
ms.openlocfilehash: a22ca88937b1c285c88edcc2fa1e9edaf1498a5473c8459f744f752cd1fbc7df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562868"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a>SampleGrad (DirectX HLSL 材質物件) 

使用漸層來取樣材質，以影響範例位置的計算方式。

&lt;樣板類型 &gt; Object. SampleGrad ( 取樣器 \_ 狀態 S、float 位置、float DDX、float DDY \[ 、int Offset \] ) ;



 

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
<tr class="odd">
<td>Texture2DMS, Texture2DMSArray</td>
<td>不支援</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="DDX"></span><span id="ddx"></span><em>DDX</em></p></td>
<td><p>在以 x 方向呈現的表面幾何變化率。 引數類型相依于材質物件類型。</p>

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
<td>FLOAT</td>
</tr>
<tr class="even">
<td>Texture2D、Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, TextureCube, TextureCubeArray </td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texture2DMS, Texture2DMSArray</td>
<td>不支援</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span id="DDY"></span><span id="ddy"></span><em>DDY</em></p></td>
<td><p>在介面幾何在 y 方向的變化率。 引數類型相依于材質物件類型。</p>

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
<td>FLOAT</td>
</tr>
<tr class="even">
<td>Texture2D、Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, TextureCube, TextureCubeArray </td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texture2DMS, Texture2DMSArray</td>
<td>不支援</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>抵消</em></p></td>
<td><p>在選擇性的材質座標位移，可用於任何材質物件類型。 位移會套用至取樣之前的位置。 只在整數 miplevel 使用位移;否則，您可能會得到無法妥善轉譯至硬體的結果。 引數類型相依于材質物件類型。 如需詳細資訊，請參閱套用<a href="dx-graphics-hlsl-to-sample.md">整數位移</a>。</p>

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
<tr class="odd">
<td>Texture2DMS, Texture2DMSArray</td>
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
| x        | x         | x        | x         | x        | x         |



 

1.  TextureCubeArray 適用于著色器模型4.1 或更高版本。
2.  在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。

## <a name="example"></a>範例

這個部分程式碼範例是來自 [MotionBlur10 範例](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx)中的 MotionBlur 檔案。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質物件](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

