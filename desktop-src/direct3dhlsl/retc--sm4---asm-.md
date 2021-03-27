---
title: 'retc (sm4-asm) '
description: 條件式傳回。
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e394bc6b947d91fafb09dbfdc075b0c60be2cf8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971593"
---
# <a name="retc-sm4---asm"></a>retc (sm4-asm) 

條件式傳回。



| retc { \_ z \|\_nz} src0. 選取 \_ 元件 |
|----------------------------------------|



 



| 項目                                                            | 描述                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[用 \] 來測試條件的註冊。<br/> |



 

## <a name="remarks"></a>備註

如果在副程式中，此指令會有條件地傳回呼叫之後的指令。 如果不在副程式內，此指令會終止程式執行。

下列範例示範如何使用此指令。

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a>限制

-   **retc** 可以出現在程式中的任何位置，不限次數。
-   Main 程式或副程式中的最後一個指令不能是 **retc \_ z** 或 **retc \_ nz**。 相反地，可以使用無條件的 [ret](ret--sm4---asm-.md) 。
-   *Src0* 提供的32位暫存器會在位層級進行測試。 如果有任何位為非零值，則會傳回 **ret \_ nz** 。 如果所有位都是零， **retc \_ z** 將會傳回。

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
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型4元件 (DirectX HLSL) ](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





