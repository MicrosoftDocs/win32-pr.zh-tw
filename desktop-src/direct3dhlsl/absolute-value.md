---
title: 絕對值
description: 取得算數運算中所使用之來源運算元的絕對值。
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 904ff3bb89e71a95a1c88851426ba283987ba6b96f336c91dd443794ee5e143d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795407"
---
# <a name="absolute-value"></a>絕對值

取得算數運算中所使用之來源運算元的絕對值。



| \_Abs |
|-------|



 

此修飾詞僅適用于單一和雙精確度浮點數和指示。 **\_ Abs** 修飾詞會強制在來源運算元的 (s) 的正負號，包括 IN光圈值在內。

在 NaN 上套用 **\_ abs** 會保留 nan，雖然未定義結果的特定 NaN 位模式。

當 \_ abs 與 [否定](negate.md)修飾詞結合時，此組合會強制正負號為負數，如同先套用 **\_ abs** 修飾詞，然後是 **否定** 的。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此修飾詞。



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

[指令修飾詞](instruction-modifiers.md)
</dt> </dl>

 

 




