---
description: 彈性頂點格式常數（或 FVF 代碼）是用來描述在單一資料流程中交錯的頂點內容，此資料流程會由固定函式管線處理。
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4351e622ec54acae2ebe560813c6bdc2bc1d49e9df3b991591b7fdfd1eeef2c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911129"
---
# <a name="d3dfvf"></a>D3DFVF

彈性頂點格式常數（或 FVF 代碼）是用來描述在單一資料流程中交錯的頂點內容，此資料流程會由固定函式管線處理。

## <a name="vertex-data-flags"></a>頂點資料旗標

下列旗標描述頂點格式。 如需有關頂點格式的詳細資訊，請參閱 [ (Direct3D 9) 的固定函式 FVF 碼 ](fixed-function-fvf-codes.md)。



| \#定義                            | 描述                                                                                                                                                                                                                                                                                                                                                             | 資料順序和類型                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D3DFVF \_ 擴散                     | 頂點格式包含擴散色彩元件。                                                                                                                                                                                                                                                                                                                       | 依 ARGB 順序的 DWORD。 請參閱 [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)。                                         |
| D3DFVF \_ 正常                      | 頂點格式包含頂點一般向量。 此旗標不可與 D3DFVF XYZRHW 旗標一起使用 \_ 。                                                                                                                                                                                                                                                                   | float、float、float                                                                                       |
| D3DFVF \_ PSIZE                       | 以點大小指定的頂點格式。 這種大小是以相機空間單位來表示，而這些頂點未轉換和亮，而裝置空間單位適用于已轉換和亮頂點。                                                                                                                                                                          | FLOAT                                                                                                     |
| D3DFVF \_ 反光                    | 頂點格式包含反射色彩元件。                                                                                                                                                                                                                                                                                                                      | 依 ARGB 順序的 DWORD。 請參閱 [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)。                                         |
| D3DFVF \_ XYZ                         | 頂點格式包含未轉換頂點的位置。 此旗標不可與 D3DFVF XYZRHW 旗標一起使用 \_ 。                                                                                                                                                                                                                                                  | 浮點數、浮點數、浮點數。                                                                                      |
| D3DFVF \_ XYZRHW                      | 頂點格式包含已轉換頂點的位置。 此旗標不可與 D3DFVF \_ XYZ 或 D3DFVF \_ NORMAL 旗標一起使用。                                                                                                                                                                                                                                     | 浮點數、浮點數、浮點數、浮點數。                                                                               |
| D3DFVF \_ XYZB1 到 D3DFVF \_ XYZB5 | 頂點格式包含位置資料，以及對應的加權數目 (Beta) 值，用於 multimatrix 頂點混合作業。 目前，Direct3D 最多可以 blend 三個加權值和四個混合矩陣。 如需使用混色矩陣的詳細資訊，請參閱 [ (Direct3D 9) 的索引頂點混色 ](indexed-vertex-blending.md)。 | 1、2或3浮點數。 使用 D3DFVF \_ LASTBETA \_ UBYTE4 時，會將最後一個混合權數視為 DWORD。 |
| D3DFVF \_ XYZW                        | 頂點格式包含已轉換和裁剪的 (x、y、z、w) 資料。 ProcessVertices 不會叫用 clipper，而是以裁剪座標輸出資料。 這個常數是針對所設計，而且只能與可程式化的頂點管線搭配使用。                                                                                                                 | float、float、float、float                                                                                |



 

## <a name="texture-flags"></a>材質旗標

下列旗標描述固定函式管線所使用的材質旗標。



| \#定義                          | 描述                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFVF \_ TEX0-D3DFVF \_ TEX8       | 這個頂點的材質座標集數目。 這些旗標的實際值不是連續的。                                                                                                                                                                           |
| D3DFVF \_ TEXCOORDSIZEN (coordIndex)  | 定義材質座標資料集。 n 表示紋理座標的維度。 coordIndex 表示紋理座標索引編號。 請參閱 [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) 和 [材質座標和材質階段](texture-coordinates.md)。 |



 

## <a name="mask-flags"></a>遮罩旗標

下列旗標描述固定函式管線所使用的遮罩旗標。



| \#定義                             | 描述                                           |
|--------------------------------------|-------------------------------------------------------|
| D3DFVF \_ 位置 \_ 遮罩               | 位置位的遮罩。                               |
| D3DFVF \_ RESERVED0、D3DFVF \_ RESERVED2 | 遮罩 FVF 中保留位的值。 請勿使用。 |
| D3DFVF \_ TEXCOUNT \_ MASK               | 材質旗標位的遮罩值。                     |



 

## <a name="miscellaneous-flags"></a>其他旗標

下列旗標描述固定函式管線所使用的各種旗標。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#定義</td>
<td>描述</td>
</tr>
<tr class="even">
<td>D3DFVF_LASTBETA_D3DCOLOR</td>
<td>頂點位置資料中的最後一個搶鮮版（Beta）欄位將會是 D3DCOLOR 類型。 搶鮮版（Beta）欄位中的資料會搭配矩陣調色板的外觀使用，以指定矩陣索引。</td>
</tr>
<tr class="odd">
<td>D3DFVF_LASTBETA_UBYTE4</td>
<td>頂點位置資料中的最後一個搶鮮版（Beta）欄位將會是 UBYTE4 類型。 搶鮮版（Beta）欄位中的資料會搭配矩陣調色板的外觀使用，以指定矩陣索引。 <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>// Given the following vertex data definition: 
struct VERTEXPOSITION
{
   float pos[3];
   union 
   {
      float beta[5];
      struct
      {
         float weights[4];
         DWORD MatrixIndices;  // Used as UBYTEs
      }
   }
};</code></pre></td>
</tr>
</tbody>
</table>

<p>假設 FVF 宣告為： D3DFVF_XYZB5 |D3DFVF_LASTBETA_UBYTE4。 權數和 MatrixIndices 包含在 Beta [5] 中，D3DFVF_LASTBETA_UBYTE4 表示要將 Beta [5] 中的最後一個 DWORD 解讀為類型 UBYTE4。</p></td>
</tr>
<tr class="even">
<td>D3DFVF_TEXCOUNT_SHIFT</td>
<td>用來將識別頂點材質座標數目的整數值移位的位數。 您可以使用此值，如下所示。
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>DWORD dwNumTextures = 1;  // Vertex has only one set of coordinates.

// Shift the value for use when creating a 
//   flexible vertex format (FVF) combination.
dwFVF = dwNumTextures << D3DFVF_TEXCOUNT_SHIFT;

// Now, create an FVF combination using the shifted value.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

### <a name="examples"></a>範例

下列範例顯示其他常見的旗標組合。


```
// Untransformed vertex for lit, untextured, Gouraud-shaded content.
dwFVF = ( D3DFVF_XYZ | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for unlit, untextured, Gouraud-shaded 
//   content with diffuse material color specified per vertex.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for light-map-based lighting.
dwFVF = ( D3DFVF_XYZ | D3DFVF_TEX2 );
```




```
// Transformed vertex for light-map-based lighting with shared rhw.
dwFVF = ( D3DFVF_XYZRHW | D3DFVF_TEX2 );
```




```
// Heavyweight vertex for unlit, colored content with two 
//   sets of texture coordinates.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE | 
          D3DFVF_SPECULAR | D3DFVF_TEX2 );
```



## <a name="constant-information"></a>常數資訊



| 需求                         | 值            |
|--------------------------|-------------|
| 標頭                   | d3d9types。h |
| 最低作業系統 | Windows 98  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[修正 (Direct3D 9) 的函式 FVF 碼 ](fixed-function-fvf-codes.md)
</dt> <dt>

[ (Direct3D 9) 的幾何混合 ](geometry-blending.md)
</dt> </dl>

 

 



