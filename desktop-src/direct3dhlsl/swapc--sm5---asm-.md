---
title: 'swapc (sm5-asm) '
description: 執行兩個輸入暫存器之間值的元件條件式交換。
ms.assetid: 3DFCEB82-076E-4AFA-915F-47390A355B7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d09d52bd497c7819500c11c4464907e4a7854bb305ed0e31d53b897ba4cf7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486258"
---
# <a name="swapc-sm5---asm"></a>swapc (sm5-asm) 

執行兩個輸入暫存器之間值的元件條件式交換。



| swapc dest0 \[ mask \] 、dest1 \[ mask \] 、src0 \[ . swizzle \] 、src1. swizzle \[ \] 、src2 收取 \[ . swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| 項目                                                               | 描述                                                                                     |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[以 \] 任意非空白寫入遮罩進行註冊。 必須不同于 *dest1*。<br/> |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[以 \] 任意非空白寫入遮罩進行註冊。 必須不同于 *dest0*。<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[中 \] 提供4個條件。 非零整數值表示 **true**。 <br/>               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[\]其中一個要交換的值。<br/>                                              |
| <span id="src2"></span><span id="SRC2"></span>*src2 收取*<br/>    | \[\]其中一個要交換的值。<br/>                                              |



 

## <a name="remarks"></a>備註

此指示的編碼方式會嘗試在 2 4 元件暫存器中簡潔地多個純量的多重平行條件式交換，而且在結算所涉及的數位配對中，有些許的彈性。

針對 *src0*、 *src1* 和 *src2 收取* 所選擇的 register 和 value，會以任何方式（例如 [movc](movc--sm4---asm-.md)）進行限制。

您可以使用 **movc** 指令，以對等的作業描述此指令的語法。 最糟的情況會顯示在下列範例中，以確保目的地暫存器不會在結束之前更新。

``` syntax
                swapc dest0[.mask], 
                      dest1[.mask],
                      src0[.swizzle],
                      src1[.swizzle],
                      src2[.swizzle]

                expands to:

                movc temp[dest0 s mask], 
                     src0[.swizzle], 
                     src2[.swizzle], src1[.swizzle]

                movc dest1[.mask], 
                     src0[.swizzle], 
                     src1[.swizzle], src2[.swizzle]

                mov  dest0.mask, temp
```

您可以選擇處理工作的方式（如果不是直接）。 例如，相同的效果可以透過一連串最多4個簡單純量條件交換的順序來達成，也可以在上述的兩個向量 **movc** 指令中完成，再加上任何額外負荷，以確保在展開的早期作業中不會事情來源值。

使用此指令進行排序。

此指示適用于下列著色器階段：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





