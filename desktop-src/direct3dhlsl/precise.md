---
title: 精確
description: 依指令停用算術重構。
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f288fb5dafee0e29c8c11cab72156f7ad3d569
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104507708"
---
# <a name="precise"></a>精確

依指令停用算術重構。



| 精確 (元件遮罩)  |
|--------------------------|



 

此修飾詞需要全域著色器旗標「允許重構」 \_ 。 當 \_ 有允許重構時，個別指令的個別元件結果可能會被強制由編譯器或驅動程式保持精確或不 refactorable。 如果將 [**mad**](mad--sm4---asm-.md) 指令的元件標記為 **精確**，則硬體必須執行 **mad** 指令或完全相同的對等指令，而且無法將它分割成乘上的乘號。 相反地，後面接著一個加上的乘法，其中任一或兩者都會標示為 **精確**，因此無法合併到融合的 **mad** 中。

如果尚未 \_ 指定允許的重構，則不允許 **精確** 的修飾詞。 這是不需要的，因為所有專案都是精確的。 **精確** 修飾詞會影響任何運算，而不只是算術。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此修飾詞。



| 著色器模型                                              | 支援 |
|-----------------------------------------------------------|-----------|
| [著色器模型5](d3d11-graphics-reference-sm5.md)        | 是       |
| [著色器模型4。1](dx-graphics-hlsl-sm4.md)              | 不可以        |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 不可以        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5指令修飾詞](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




