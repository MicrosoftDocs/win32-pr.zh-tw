---
title: 'dcl_input_sv (sm4-asm) '
description: 'dcl \_ 輸入 \_ sv (sm4-asm) '
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679191"
---
# <a name="dcl_input_sv-sm4---asm"></a>dcl \_ 輸入 \_ sv (sm4-asm) 

宣告需要從先前階段提供 [系統值](dx-graphics-hlsl-semantics.md) 的著色器輸入暫存器。



| dcl \_ 輸入 \_ sv v *N \[ . mask \]*、 *systemValueName \[ 、interpolationMode \]* |
|------------------------------------------------------------------------|



 



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
<td><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [mask]</em><br/></td>
<td>在頂點資料註冊。 <br/>
<ul>
<li><em>N</em> 是識別註冊編號的整數。</li>
<li><em>[mask]</em> 是選擇性的元件遮罩 ( xyzw) ，可指定要使用的註冊元件。</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em><br/></td>
<td>在系統值名稱，也就是字串 (請參閱 <a href="dx-graphics-hlsl-semantics.md">系統值語義</a>) ，而不使用 &quot; SV_ &quot; 前置詞。<br/></td>
</tr>
<tr class="odd">
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em><br/></td>
<td>[in] 選用。 插補模式，它會影響在點陣化期間計算值的方式;只有圖元著色器會使用此模式。 它可能是下列其中一個值： <br/>
<ul>
<li>常數-不在暫存器值之間插補。</li>
<li>線性-在註冊值之間以線性方式插補。</li>
<li>linearCentroid-與線性相同，但在取樣時距心壓制。</li>
<li>linearNoperspective-與線性相同，但沒有透視校正。</li>
<li>linearNoperspectiveCentroid-與線性相同，但在交叉取樣時沒有透視更正和距心壓制。</li>
</ul></td>
</tr>
</tbody>
</table>



 

系統值宣告的元件遮罩可以是任何適當的 xyzw 子集; 宣告 \[ \] 可能不會重迭 (每個宣告都必須遵循序列 xyzw) 。 宣告純量系統值 (剪切距離和剔除距離（例如) ）時，您可以在單一暫存器中宣告多個系統值。 如果您這樣做，請確定其他修飾詞（例如插補模式）相符。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

## <a name="example"></a>範例

以下是一些範例：


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
```



## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 是       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





