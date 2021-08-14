---
title: 'dcl_constantBuffer (sm4-asm) '
description: 'dcl \_ constantBuffer (sm4-asm) '
ms.assetid: 164fb2a4-8782-42f0-b4ba-1f87d9c7255d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 437266c5a37f266a4f8847f09719380f436b6d9d38e8dee21b3258c79adb32b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727262"
---
# <a name="dcl_constantbuffer-sm4---asm"></a>dcl \_ constantBuffer (sm4-asm) 

宣告著色器常數緩衝區。



| dcl \_ constantBuffer *cbN \[ size \]*， *AccessPattern* |
|----------------------------------------------------|



 



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
<td><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>cb<em>N [大小]</em><br/></td>
<td>在著色器常數緩衝區，其中 N 是表示常數緩衝區暫存器編號的整數，而 size 是表示緩衝區中專案數目的整數。<br/></td>
</tr>
<tr class="even">
<td><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em><br/></td>
<td>在著色器程式碼將存取緩衝區的方式，這是下列其中一項： <br/> 
<table>
<thead>
<tr class="header">
<th>Name</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>immediateIndexed</td>
<td>使用常值為緩衝區編制索引。</td>
</tr>
<tr class="even">
<td>dynamic_indexed</td>
<td>使用評估運算式的結果來編制緩衝區的索引。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

## <a name="example"></a>範例

此範例會為 register cb0 宣告常數緩衝區，其中有19個元素。 您可以使用常值索引來存取這些元素。


```
dcl_constantbuffer  cb0[19], immediateIndexed
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

 

 





