---
title: '剪下 (sm4-asm) '
description: 幾何著色器指令會完成目前的基本拓撲 (如果已發出) 的任何頂點，並啟動幾何著色器所宣告之類型的新拓撲。
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34357c05cdd9506ec480d5021db5b330971de9fce7fd70ce9909658be9bb8c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908822"
---
# <a name="cut-sm4---asm"></a>剪下 (sm4-asm) 

幾何著色器指令會完成目前的基本拓撲 (如果已發出) 的任何頂點，並啟動幾何著色器所宣告之類型的新拓撲。



| 剪下 |
|-----|



 

## <a name="remarks"></a>備註

當執行 **剪** 下時，第一件事就是已完成幾何著色器調用的任何先前發出的拓撲。 如果未針對先前的基本拓撲發出足夠的頂點，則會捨棄這些頂點。 因為幾何著色器的唯一可用輸出拓撲是 pointlist、linestrip 和 trianglestrip，所以 **剪** 下時永遠不會有任何剩餘的頂點。

在先前的拓撲（如果有的話）完成之後， **剪** 下會使用宣告為幾何著色器輸出的拓撲來開始新的拓撲。

## <a name="restrictions"></a>限制

-   **剪** 下的指令只適用于幾何著色器。
-   **剪** 下可以在幾何著色器中出現任何次數，包括 flow 控制項內。
-   如果幾何著色器結束且頂點已發出，則會完成其所建立的拓撲，就像是執行 **剪** 下做為最後一個指令一樣。
-   如果已宣告資料流程，就必須使用 [剪下 \_ 資料流程](cut-stream---sm5---asm-.md) ，而不是 **剪** 下。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
|               | x               |              |



 

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

 

 




