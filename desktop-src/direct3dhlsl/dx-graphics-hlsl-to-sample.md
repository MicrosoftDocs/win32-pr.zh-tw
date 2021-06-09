---
title: 範例 (DirectX HLSL 紋理物件)
description: 範例材質。 | (DirectX HLSL 材質物件) 範例
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2374063d222d06576f720fed2aa7fb714bcccf04
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825745"
---
# <a name="sample-directx-hlsl-texture-object"></a>範例 (DirectX HLSL 紋理物件)

範例材質。

&lt;範本類型 &gt; 物件。範例 ( 取樣器 \_ 狀態 S、浮點位置 \[ 、整數位移 \] ) ;

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

## <a name="example"></a>範例

這個部分程式碼範例是以 [BasicHLSL11 範例](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11)中的 BasicHLSL11 檔案為基礎。

```
// Object Declarations
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color (note that COLOR0 is clamped from 0..1)
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT In;

// Shader body calling the intrinsic function
   ...
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
```

## <a name="remarks"></a>備註

紋理取樣會使用材質位置來查閱材質值。 位移可以套用到查閱之前的位置。 取樣器狀態包含取樣和篩選選項。 這個方法可以在圖元著色器中叫用，但在頂點著色器或幾何著色器中不支援。

只在整數 miplevel 使用位移;否則，您可能會根據硬體的執行或驅動程式設定取得不同的結果。

### <a name="calculating-texel-positions"></a>計算材質位置

材質座標是參考紋理資料的浮點值，也稱為標準化材質空間。 位址換行模式會依此順序套用 (材質座標 + 位移 + 換行模式) 來修改 \[ 0 ... 1 範圍以外的材質座標。 \]

針對材質陣列，location 參數中的額外值會指定紋理陣列中的索引。 此索引會被視為調整的浮點值 (而不是標準材質座標) 的正規化空間。 整數索引的轉換是以下列順序完成， (float + 四捨五入至最接近的陣列範圍) ，甚至是整數 + 夾具。

### <a name="applying-texture-coordinate-offsets"></a>套用材質座標位移

Offset 參數會修改材質空間中的材質座標。 雖然材質座標是正規化浮點數，但位移會套用整數位移。 另請注意，材質位移必須是靜態的。

傳回的資料格式取決於材質格式。 例如，如果紋理資源是以 DXGI \_ 格式 \_ A8B8G8R8 \_ UNORM SRGB 格式所定義 \_ ，則取樣作業會將取樣的材質從 gamma 2.0 轉換為1.0、篩選，並將結果以浮點數形式寫入範圍 \[ 0 ..1 \] 。

## <a name="related-topics"></a>相關主題

[材質物件](dx-graphics-hlsl-to-type.md)
