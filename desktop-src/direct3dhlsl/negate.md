---
title: Negate
description: 翻轉算數運算中所使用之來源運算元值的正負號。
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104022806"
---
# <a name="negate"></a>Negate

翻轉算數運算中所使用之來源運算元值的正負號。



| \-  |
|-----|



 

若為單精確度和雙精度浮點數和指示，否定修飾詞會翻轉來源運算元中)  (s 的正負號，包括 IN光圈值在內。 在 NaN 上套用 **否定** 會保留 nan，雖然未定義結果的特定 NaN 位模式。

若為整數指示， **否定** 修飾詞會採用來源運算元中)  (s 的2補數。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此修飾詞。



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

[指令修飾詞](instruction-modifiers.md)
</dt> </dl>

 

 




