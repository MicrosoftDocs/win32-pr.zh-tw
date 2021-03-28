---
title: '切換 (sm4-asm) '
description: 將控制權傳輸至切換主體內的不同語句區塊，取決於選取器的值。
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022822"
---
# <a name="switch-sm4---asm"></a>切換 (sm4-asm) 

將控制權傳輸至切換主體內的不同語句區塊，取決於選取器的值。



| 切換 src0 選取的 \_ 元件 |
|---------------------------------|



 



| 項目                                                            | 描述                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[在 \] switch 語句的選取器中。<br/> |



 

## <a name="remarks"></a>備註

**Switch** / [endswitch](endswitch--sm4---asm-.md)結構的運作方式與 C 語言中的 **switch** 結構完全相同，但有下列例外狀況：若為 D3D11 [案例](case--sm4---asm-.md) / ，而不使用 break 的 [預設](default--sm4---asm-.md)語句，則 / 不能有任何程式碼。 [](break--sm4---asm-.md) 允許多個 **case** 語句（包括 **預設值**）依序出現，並共用相同的程式碼區塊。

條件必須是32位的註冊元件或立即數量。 相等比較是位 (整數) 。

如同 D3D11 中的任何著色器指令，硬體可能會或可能不會直接執行 **switch** 結構。

**Switch** 語句可以嵌套。 每個 **switch** 區塊都會針對每個副程式和 main 的流程式控制制對應深度64限制為1個層級，而不受 **case** 語句的數目影響。 HLSL 編譯器將不會產生超過此限制的副程式。 除了64層級之外，每個副程式的控制流程指令行為未定義。

下列範例示範如何使用此指令。

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
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

 

 





