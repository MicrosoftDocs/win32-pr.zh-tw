---
title: 'dcl_output oMask (sm5-asm) '
description: 宣告要由著色器寫入的輸出暫存器。
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a6860904b557bc21a5202bbfd60105852adc260580457afb02b4fe6d92352b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068508"
---
# <a name="dcl_output-omask-sm5---asm"></a>dcl \_ 輸出 oMask (sm5-asm) 

宣告要由著色器寫入的輸出暫存器。



| dcl \_ 輸出 o \# \[ . mask\] |
|--------------------------|



 



| 項目                                                   | 描述                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="o"></span><span id="O"></span>*輸出*<br/> | \[在輸出暫存器中 \] 。<br/> |



 

## <a name="remarks"></a>備註


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a>限制

-   元件遮罩可以是 xyzw 的任何子集 \[ \] 。 不過，保留元件之間的間距會浪費空間。
-   宣告針對下一個階段所宣告的元件遮罩的超集合，是合法的。 但是，不允許互斥的遮罩。 頂點著色器輸出 o3，表示圖元著色器輸入 v3. z 無效，但輸入 v3. x 或 v3. y 或 v3。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     |         |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此指令：



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 否        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 否        |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 否        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5元件 (DirectX HLSL) ](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





