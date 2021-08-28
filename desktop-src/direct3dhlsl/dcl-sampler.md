---
title: 'dcl_sampler (sm4-asm) '
description: 'dcl \_ 取樣器 (sm4-asm) '
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cb3835e1c0e2cfb5ffbb49523617b9d233810494
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627094"
---
# <a name="dcl_sampler-sm4---asm"></a>dcl \_ 取樣器 (sm4-asm) 

宣告取樣器暫存器。



| dcl \_ 取樣器 sN，模式 |
|-----------------------|



 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em><br/></td>
<td>在取樣器暫存器，其中 <em>N</em> 是表示註冊編號的整數。<br/></td>
</tr>
<tr class="even">
<td><span id="mode"></span><span id="MODE"></span><em>模式</em><br/></td>
<td>在取樣器模式，限制 <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) 的成員中所列的取樣器狀態 (。 下表列出模式和狀態。<br/> 
<table>
<thead>
<tr class="header">
<th>[模式]</th>
<th>已接受取樣器狀態</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>預設</td>
<td><em>篩選</em> (可能不會使用 _COMPARISON 或 _TEXT 值) 、 <em>AddressU/V/W</em>、 <em>MinLOD/MaxLOD</em>、 <em>MipLODBias</em>、 <em>MaxAnisotropy</em>、加 <em>邊框 [4]</em></td>
</tr>
<tr class="even">
<td>比較</td>
<td><em>Filter</em>、 <em>ComparisonFunction</em>、 <em>AddressU/V/W</em>、 <em>MinLOD、MaxLOD</em>、 <em>MipLODBias</em>、 <em>MaxAnisotropy</em>、加 <em>邊框 [4]</em></td>
</tr>
<tr class="odd">
<td>單</td>
<td><em>篩選</em> (必須是其中一個 _TEXT 值) 、 <em>MonoFilterWidth</em>、 <em>MonoFilterHeight</em> (這兩個狀態為全域裝置狀態) 、 <em>MinLOD</em>、 <em>MipLODBias</em>、 <em>MaxAnisotropy</em></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

此模式會限制可使用的範例指令;下表列出每個模式都支援的材質物件方法。



| 在此模式中操作的取樣器 | 可以使用這些 Texture-Object 方法                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| 預設                          | [Sample](dx-graphics-hlsl-to-sample.md)、 [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)、 [SampleGrad](dx-graphics-hlsl-to-samplegrad.md) |
| 比較                       | [SampleCmp](dx-graphics-hlsl-to-samplecmp.md)、 [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)                               |
| 單                             | [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x\*          |



 

\* -只有在圖元著色器中才支援使用 mono 模式的取樣器。

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

## <a name="example"></a>範例

範例如下。


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 是       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

