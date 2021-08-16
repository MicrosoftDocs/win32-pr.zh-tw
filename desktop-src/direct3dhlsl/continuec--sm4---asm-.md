---
title: 'continuec (sm4-asm) '
description: 在目前迴圈的開頭有條件地繼續執行。
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d909c199dc0ceaa4e5498429f1ac3a136d3fb75d930e392d7f6fd8230e5b49b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117909055"
---
# <a name="continuec-sm4---asm"></a>continuec (sm4-asm) 

在目前迴圈的開頭有條件地繼續執行。



| continuec { \_ z \|\_nz} src0. 選取 \_ 元件 |
|---------------------------------------------|



 



| 詞彙                                                            | 描述                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[用 \] 來測試條件的元件。<br/> |



 

## <a name="remarks"></a>備註

**continuec** 只能在 [迴圈](loop--sm4---asm-.md) 或 [endloop](endloop--sm4---asm-.md)內使用。

下列範例顯示如何使用 **continuec** 指令。


```
                loop
                    if_na r0.x
                        break
                    endif
                    continuec_z r1.x  // if all bits of r1.x are zero then
                                      // continue at beginning of loop.
                    ...
                    continuec_nz r3.y // if any bit in r3.y is set then
                                      // continue at beginning of loop.

                    ...
                endloop

```



Token 格式包含著色器中對應迴圈指令的位移，以方便使用。

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

 

 





