---
title: 'movc (sm4-asm) '
description: '以元件為條件的移動。 |movc (sm4-asm) '
ms.assetid: B7F19DF5-282F-41D4-AE2D-6ACF61A42088
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81da36b39f60929bdfbac3b4a37c379189cf358ed4844e1a4cc899f867970065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095358"
---
# <a name="movc-sm4---asm"></a>movc (sm4-asm) 

以元件為條件的移動。



| movc \[ \_ sat \] dest \[ . mask \] 、src0 \[ . swizzle \] 、 \[ - \] src1 \[ \_ abs \] \[ . swizzle \] 、 \[ - \] src2 收取 \[ \_ abs \] \[ . swizzle \] 、 |
|----------------------------------------------------------------------------------------------------------------|



 



| 項目                                                            | 描述                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*目標*<br/> | \[在 \] 操作結果的位址中。 <br/> 如果是 *src0*，則 *dest*  =  *src1* else *dest*  =  *src2 收取*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 測試條件的元件中。<br/>                                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[在 \] 要移動的元件中。 <br/>                                                                                     |
| <span id="src2"></span><span id="SRC2"></span>*src2 收取*<br/> | \[在 \] 要移動的元件中。<br/>                                                                                      |



 

## <a name="remarks"></a>備註

下列範例示範如何使用此指令。

``` syntax
                for each component in dest[.mask]
                    if the corresponding component in src0 (POS-swizzle)
                       has any bit set
                    {
                        copy this component (POS-swizzle) from src1 into dest
                    }
                    else
                    {
                        copy this component (POS-swizzle) from src2 into dest
                    }
                endfor
```

*Src1* 和 *src2 收取* 上的修飾詞（除了 swizzle 以外）會假設資料是浮點數。 缺少修飾詞只會在不改變位的情況下移動資料。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

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

 

 





