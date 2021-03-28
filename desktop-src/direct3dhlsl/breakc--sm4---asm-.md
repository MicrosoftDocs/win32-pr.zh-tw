---
title: 'breakc (sm4-asm) '
description: 有條件地將執行點移到下一個 endloop 或 endswitch 之後的指令。
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373819"
---
# <a name="breakc-sm4---asm"></a>breakc (sm4-asm) 

有條件地將執行點移到下一個 [endloop](endloop--sm4---asm-.md) 或 [endswitch](endswitch--sm4---asm-.md)之後的指令。



| breakc { \_ z \|\_nz} src0. 選取 \_ 元件 |
|------------------------------------------|



 



| 項目                                                            | 描述                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] 測試條件的元件中。<br/> |



 

## <a name="remarks"></a>備註

標記格式包含著色器中對應 **endloop** 指令的位移，以方便使用。

下列範例顯示 **breakc** 指令。


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



這個指令必須出現在 **迴圈** / **endloop** 或 **switch** / **endswitch** 內。

*Src0* 提供的32位暫存器會在位層級進行測試。 如果有任何位為非零值， **breakc \_ nz** 將會執行中斷。 如果所有位都是零， **breakc \_ z** 將會執行中斷。

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

 

 





