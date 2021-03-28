---
title: 'loop (sm4-asm) '
description: 指定迴圈，直到遇到 break 指令為止。
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 243bdf3b370d3505d787451162c22340acef3a45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990775"
---
# <a name="loop-sm4---asm"></a>loop (sm4-asm) 

指定迴圈，直到遇到 break 指令為止。



| loop |
|------|



 

## <a name="remarks"></a>備註

**迴圈** 可以無限期地逐一查看，不過在執行一些指令之後，可能會強制將著色器的整體執行終止。

流程式控制制區塊最多可在每個副程式和主要的64個深度上進行。 HLSL 編譯器將不會產生超過此限制的副程式。 除了64層級之外，每個副程式的控制流程指令行為未定義。

標記格式包含著色器中對應 [endloop](endloop--sm4---asm-.md) 指令的位移，以方便使用。

下列範例顯示如何使用迴圈指令。

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

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

 

 




