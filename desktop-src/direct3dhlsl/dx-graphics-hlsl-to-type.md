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
# <a name="texture-object"></a>材質物件

在 Direct3D 10 中，您可以單獨指定取樣器和紋理;紋理取樣是使用樣板化紋理物件來執行。 這個樣板化紋理物件有特定的格式，會傳回特定的類型，並實作為數種方法。




|                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D9 和 Direct3D10 之間的差異：在 Direct3D 9 中，取樣器會系結至特定紋理;在 Direct3D 10 中，紋理和取樣器是獨立的物件。 每個樣板化紋理物件都會實作為材質和取樣器的材質取樣方法，以做為輸入參數。<br/> |



 

以下是用來建立所有材質物件 (除了) 多重取樣物件以外的語法。



| Object1 \[ < *類型* > \] *名稱*; |
|------------------------------------|



 

多重取樣物件 (Texture2DMS 和 Texture2DMSArray) 需要明確陳述紋理大小，並以樣本數目表示。



| >object2 \[ < *類型，範例* > \] *名稱*; |
|---------------------------------------------|



 

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
<td>紋理物件。 必須是下列其中一種類型。 <br/> 
<table>
<thead>
<tr class="header">
<th>Object1 類型</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Buffer</td>
<td>Buffer </td>
</tr>
<tr class="even">
<td>Texture1D</td>
<td>1D 材質</td>
</tr>
<tr class="odd">
<td>Texture1DArray</td>
<td>1D 紋理的陣列</td>
</tr>
<tr class="even">
<td>Texture2D</td>
<td>2D 材質</td>
</tr>
<tr class="odd">
<td>Texture2DArray</td>
<td>2D 材質的陣列</td>
</tr>
<tr class="even">
<td>Texture3D</td>
<td>3D 材質</td>
</tr>
<tr class="odd">
<td>TextureCube</td>
<td>立方體材質</td>
</tr>
<tr class="even">
<td>TextureCubeArray  </td>
<td>Cube 紋理的陣列</td>
</tr>
<tr class="odd">
<td>>object2 類型</td>
<td>Description</td>
</tr>
<tr class="even">
<td>Texture2DMS</td>
<td>2D 多重取樣材質</td>
</tr>
<tr class="odd">
<td>Texture2DMSArray</td>
<td>2D 多重取樣材質的陣列</td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li>緩衝區類型支援大部分的材質物件方法，但 GetDimensions 除外。</li>
<li>TextureCubeArray 適用于著色器模型4.1 或更高版本。</li>
<li>在 Direct3D 10.1 或更高版本中可以使用著色器模型4.1。</li>
</ol></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>類型</em></p></td>
<td><p>選擇性。 任何純量 <a href="dx-graphics-hlsl-scalar.md">HLSL 類型</a> 或 <a href="dx-graphics-hlsl-vector.md"><strong>向量 HLSL 類型</strong></a>（以角括弧括住）。 預設類型為 <strong>float4</strong>。</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>名字</em></p></td>
<td><p>指定材質物件名稱的 ASCII 字串。</p></td>
</tr>
<tr class="even">
<td><p><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>樣品</em></p></td>
<td><p> (範圍介於1到 128) 之間的樣本數。</p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a>範例 1

以下是宣告材質物件的範例。


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a>材質物件方法

每個材質物件都會執行特定方法;以下是列出所有方法的表格。 請參閱每個方法的參考頁面，瞭解哪些物件可以使用該方法。



| 材質方法                                                                     | Description                                                                                                       | vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [CalculateLevelOfDetail](dx-graphics-hlsl-to-calculate-lod.md)                    | 計算」 LOD，傳回壓制結果。                                                                       |          |           |          | x         |          |           |
| [CalculateLevelOfDetailUnclamped](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | 計算」 LOD，傳回 unclamped 結果。                                                                    |          |           |          | x         |          |           |
| [收集](dx-graphics-hlsl-to-gather.md)                                           | 取得 (紅色元件的四個範例，只有在取樣材質時用於雙線性插補的) 。 |          | x         |          | x         |          | x         |
| [GetDimensions](dx-graphics-hlsl-to-getdimensions.md)                             | 取得指定之 mipmap 層級的材質維度。                                                           | x        | x         | x        | x         | x        | x         |
| [GetDimensions (的多級取樣) ](dx-graphics-hlsl-to-getdimensions.md)               | 取得指定之 mipmap 層級的材質維度。                                                           |          | x         |          | x         |          | x         |
| [GetSamplePosition](dx-graphics-hlsl-to-get-sample-position.md)                   | 取得指定範例的位置。                                                                         |          | x         |          | x         |          | x         |
| [載入](dx-graphics-hlsl-to-load.md)                                               | 載入資料，而不進行任何篩選或取樣。                                                                      | x        | x         | x        | x         | x        | x         |
| [載入 (的多重採樣) ](dx-graphics-hlsl-to-load.md)                                 | 載入資料，而不進行任何篩選或取樣。                                                                      |          | x         | x        | x         |          | x         |
| [範例](dx-graphics-hlsl-to-sample.md)                                           | 範例紋理。                                                                                                 |          |           | x        | x         |          |           |
| [SampleBias](dx-graphics-hlsl-to-samplebias.md)                                   | 將偏差值套用至 mipmap 層級之後，將材質取樣。                                              |          |           | x        | x         |          |           |
| [SampleCmp](dx-graphics-hlsl-to-samplecmp.md)                                     | 使用比較值來拒絕範例，以取樣材質。                                                     |          |           | x        | x         |          |           |
| [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                   |  (只) 使用比較值來拒絕範例的材質樣本的材質。                               | x        | x         | x        | x         | x        | x         |
| [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)                                   | 使用漸層來取樣材質，以影響範例位置的計算方式。                         | x        | x         | x        | x         | x        | x         |
| [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                 | 範例指定的 mipmap 層級上的材質。                                                                   | x        | x         | x        | x         | x        | x         |



 

### <a name="return-type"></a>傳回類型

除非另有指定，否則材質物件方法的傳回型別為 float4，但多重取樣消除鋸齒紋理物件（一律需要指定類型和樣本計數）除外。 傳回型別與材質資源類型相同 ([**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。 換句話說，它可以是下列任何一種類型。



| 類型                       | Description                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FLOAT                      | 32-bit float (查看與 IEEE float) 差異的[浮點規則](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules)                            |
| int                        | 32 位元帶正負號的整數                                                                                                                                                   |
| 不帶正負號的整數               | 32 位元不帶正負號的整數                                                                                                                                                 |
| snorm                      | 32位浮點數，範圍介於-1 到1（含） (查看與 IEEE float 之間差異的 [浮點規則](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules))  |
| unorm                      | 32位浮點數，範圍介於0到1（含） (查看與 IEEE float 之間差異的 [浮點規則](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules))   |
| 任何材質類型或結構 | 傳回的元件數目必須介於1到3（含）之間。                                                                                                    |



 

此外，傳回類型可以是任何材質類型（包括結構），但必須小於4個元件（例如傳回一個元件的 float1 類型）。

## <a name="default-values-for-missing-components-in-a-texture"></a>材質中遺漏元件的預設值

除了 Alpha 元件 () 之外，材質資源類型中遺漏元件的預設值為零。遺漏 A 的預設值是1。 這一種對著色器的顯示方式取決於材質資源類型。 它會採用實際出現在材質資源類型中的第一個具類型元件的形式 (從 RGBA 順序的左邊開始) 。 如果這個表單是 UNORM 或 FLOAT，則遺漏 A 的預設值為 1.0 f。 如果表單為聖或 UINT，則遺漏的預設值為0x1。

例如，當著色器讀取 [**DXGI \_ 格式 \_ R24 \_ UNORM \_ X8 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 無類型紋理資源類型時，G 和 B 的預設值為零，而 a 的預設值為 1.0 f; 當著色器讀取 [**dxgi \_ 格式 \_ R16G16 \_ UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 材質資源類型時，B 的預設值為零，而 a 的預設值為 0x00000001; 當著色器讀取 [**DXGI \_ 格式 \_ R16 \_ 聖**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 材質資源類型時，G 和 B 的預設值為零，而的預設值為0x00000001。

## <a name="example-2"></a>範例 2

以下是使用材質方法的材質取樣範例。


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                        | 支援 |
|---------------------------------------------------------------------|-----------|
| [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型 | 是       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

