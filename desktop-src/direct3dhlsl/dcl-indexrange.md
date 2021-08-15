---
title: 'dcl_indexRange (sm4-asm) '
description: 'dcl \_ indexRange (sm4-asm) '
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a652d200a211eb5528f6e7ecdedf2cc20579817d1f0148d59855d1e864de55de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727188"
---
# <a name="dcl_indexrange-sm4---asm"></a>dcl \_ indexRange (sm4-asm) 

宣告將由索引存取的暫存器範圍 (在著色器) 中計算的整數。



| dcl \_ IndexRange *minRegisterM*， *maxRegisterN* |
|------------------------------------------------|



 



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
<td><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em><br/></td>
<td>在要依索引存取的第一個註冊。 <br/>
<ul>
<li>針對頂點或圖元著色器輸入暫存器， <em>minRegister</em>是<strong>v</strong> ，或頂點著色器輸出暫存器的<strong>o</strong> 。</li>
<li><em>M</em> 是表示註冊編號的整數。</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em><br/></td>
<td>在要依索引存取的最後一個暫存器。 與 <em>minRegister</em> 相同的表單，但 <em>N</em> 是註冊編號。<br/></td>
</tr>
</tbody>
</table>



 

下列限制適用于所有註冊：

-   最小和最大暫存器必須是相同的類型，而且如果遮罩宣告) ，則相同的元件遮罩 (。
-   註冊可以有多個索引範圍，只要它們不會重迭。
-   最小注冊號碼必須小於最大註冊編號。
-   索引暫存器不能包含 [系統值](dx-graphics-hlsl-semantics.md)。
-   在 max index 宣告之外索引暫存器會產生未定義的結果。

圖元著色器輸入暫存器必須使用相同的插補模式;圖元著色器輸出暫存器無法編制索引。

幾何著色器輸入暫存器有兩個維度 (頂點軸、屬性軸) ;索引範圍只適用于屬性軸，因為頂點軸永遠是可完全索引的。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

## <a name="example"></a>範例

範例如下。


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
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

 

 





