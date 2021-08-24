---
title: 'dcl_input (sm4-asm) '
description: 'dcl \_ 輸入 (sm4-asm) '
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8214287a4afb4c683a94e213cdfed133c03219e2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467005"
---
# <a name="dcl_input-sm4---asm"></a>dcl \_ 輸入 (sm4-asm) 

宣告著色器輸入暫存器。



| dcl \_ 輸入 v *N \[ . mask \] \[ ，interpolationMode \]* |
|-------------------------------------------------|



 




| 項目 | 描述 | 
|------|-------------|
| <span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [mask]</em><br /> | 在頂點資料註冊。 <br /><ul><li><em>N</em> 是識別註冊編號的整數。</li><li><em>[mask]</em> 是選擇性的元件遮罩 ( xyzw) ，可指定要使用的註冊元件。</li></ul> | 
| <span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em><br /> | [in] 選用。 插補模式，僅適用于圖元著色器輸入暫存器。 它可能是下列其中一個值： <br /><ul><li>常數-不在暫存器值之間插補。</li><li>線性-在註冊值之間以線性方式插補。</li><li>linearCentroid-與線性相同，但在取樣時距心壓制。</li><li>linearNoperspective-與線性相同，但沒有透視校正。</li><li>linearNoperspectiveCentroid-與線性相同，距心壓制，在取樣時，不會進行透視校正。</li></ul> | 




 

### <a name="interpolation-notes"></a>插補附注

依預設，在執行效能高效能消除鋸齒時，會從圖元中心內插上頂點屬性。 如果未涵蓋圖元中心，則會在插補之前將屬性推斷到圖元中心。

針對未完全涵蓋的圖元或未涵蓋圖元中心的屬性，您可以指定距心取樣，以強制取樣在圖元涵蓋區域內的某處發生。 因為範例遮罩 (如果在計算距心之前套用了使用的) ，所以不能將範例遮罩所遮罩的任何範例位置選擇為距心位置。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

若要將輸入識別為系統值，請使用 [dcl \_ 輸入 \_ sv (sm4-asm) ](dcl-input-sv.md)。

包含此指令的目的是協助您在元件中進行著色器的偵錯工具。您無法使用著色器模型4來撰寫元件語言中的著色器。

## <a name="example"></a>範例

以下是一些範例。


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
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

 

 





