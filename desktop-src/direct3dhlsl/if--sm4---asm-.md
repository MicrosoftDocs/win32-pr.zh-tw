---
title: '如果 (sm4-asm) '
description: 以邏輯 OR 結果為基礎的分支。
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 653c84be0d30a036bf93d852268e44bcca08bbcb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990706"
---
# <a name="if-sm4---asm"></a>如果 (sm4-asm) 

以邏輯 OR 結果為基礎的分支。



| if { \_ z \|\_nz} src0. 選取 \_ 元件 |
|--------------------------------------|



 



| 項目                                                            | 描述                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[中的 \] 包含要測試條件的元件。<br/> |



 

## <a name="remarks"></a>備註

Token 格式會在著色器中包含對應的 endif 指令位移，以方便使用。

下列範例示範如何使用此指令。

``` syntax
                if_z r0.x // if all bits in r0.x are zero
                   ...
                else // (optional)
                   ...
                endif
                if_nz r1.x // if any bit in r0.x is nonzero
                   ...
                else // (optional)
                   ...
                endif
```

### <a name="restrictions"></a>限制

-   如果4個元件向量) 必須使用單一元件選取器，則來源運算元 (。
-   *Src0* 提供的32位暫存器會在位層級進行測試。 如果有任何位為非零值，則 **\_ z** 為 true。 如果所有位為零， **則為，如果 \_ nz** 為 true。
-   在每個副程式 (和主要) 的流程式控制制區塊最多可有64個深度。 HLSL 編譯器將不會產生超過此限制的副程式。 除了64層級外的控制流程指令行為之外，每個副程式的 (深度) 未定義。

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

 

 





