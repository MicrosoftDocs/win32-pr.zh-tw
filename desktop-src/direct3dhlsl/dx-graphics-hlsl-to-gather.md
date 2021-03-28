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
ms.openlocfilehash: 16c568afc3cfdc0d26472d50599abdf3dbd08301
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/17/2020
ms.locfileid: "104971836"
---
# <a name="gather-directx-hlsl-texture-object"></a>收集 (DirectX HLSL 材質物件) 

取得 (紅色元件的四個範例，只有在取樣材質時用於雙線性插補的) 。



|                                                                                                    |
|----------------------------------------------------------------------------------------------------|
| &lt;範本類型 &gt; 4 物件。收集 ( 取樣器 \_ 狀態 S、float2 \| 3 \| 4 位置 \[ 、int2 位移 \] ) ; |



 

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
<td>以下是支援的 <a href="dx-graphics-hlsl-to-type.md">材質物件</a> 類型： Texture2D、Texture2DArray、TextureCube、TextureCubeArray。<br/></td>
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
<td>Texture2D</td>
<td>float2</td>
</tr>
<tr class="even">
<td>Texture2DArray, TextureCube</td>
<td>float3</td>
</tr>
<tr class="odd">
<td>TextureCubeArray </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>抵消</em></p></td>
<td><p>在選擇性的材質座標位移，可用於任何材質物件類型;位移會套用至取樣之前的位置。 材質位移必須是靜態的。 引數類型相依于材質物件類型。 如需詳細資訊，請參閱套用 <a href="dx-graphics-hlsl-to-sample.md">材質座標位移</a>。</p>

<table>
<thead>
<tr class="header">
<th>Texture-Object 類型</th>
<th>參數類型</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture2D、Texture2DArray</td>
<td>int2</td>
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

四個元件的向量，具有四個紅色資料的元件，其類型與材質的範本類型相同。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

1.  TextureCubeArray 適用于著色器模型4.1 或更高版本。
2.  在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。

## <a name="example"></a>範例


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質物件](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





