---
title: 'dcl_inputPrimitive (sm4-asm) '
description: 'dcl \_ inputPrimitive (sm4-asm) '
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7f266bc7cf4d697f457ef51a9021709c55ca6e1d1add88dd5dbf0491ddc469a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986718"
---
# <a name="dcl_inputprimitive-sm4---asm"></a>dcl \_ inputPrimitive (sm4-asm) 

宣告幾何著色器輸入的基本類型。



| dcl \_ inputPrimitive *類型* |
|----------------------------|



 



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
<td><span id="type"></span><span id="TYPE"></span><em>類型</em><br/></td>
<td>在輸入-資料基本類型，這是下列其中一項： <br/>
<ul>
<li><em>點</em> - 點清單</li>
<li><em>行</em> - 行清單</li>
<li><em>三角形</em> - 三角形清單</li>
<li><em>line_adj</em> - 具有相鄰資料的行清單</li>
<li><em>triangle_adj</em> - 具有相鄰資料的三角形清單</li>
</ul></td>
</tr>
</tbody>
</table>



 

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
|               | x               |              |



 

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

## <a name="example"></a>範例

範例如下。


```
dcl_inputPrimitive triangle
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

 

 





