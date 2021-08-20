---
title: '繼續 (sm4-asm) '
description: 在目前迴圈的開頭繼續執行。
ms.assetid: 3F0021B2-50D1-407C-9EE4-1CB679E184BF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abe95c445c6b339e950e051368bb6a80e6604df59e09934ecfff3b1e00a7830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117909153"
---
# <a name="continue-sm4---asm"></a>繼續 (sm4-asm) 

在目前迴圈的開頭繼續執行。



| continue |
|----------|



 

## <a name="remarks"></a>備註

**continue** 只能用在 [迴圈](loop--sm4---asm-.md) 或 [endloop](endloop--sm4---asm-.md)中。

下列範例顯示如何使用 **continue** 指令。


```
                loop
                    if_na r0.x
                        break
                    endif
                    if_z r1.x
                        ...
                        continue
                    endif
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

 

 




