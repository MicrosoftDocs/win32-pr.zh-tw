---
title: " (HLSL 參考) 飽和"
description: 將單一或雙精確度浮點算數運算的結果個至 \ 0.0 f .。。1.0 f-範圍。
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 25e771bd53dbb8a4b0d2eaf8162675cd556c071344b249562defe4a06e715f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790741"
---
# <a name="saturate-hlsl-reference"></a> (HLSL 參考) 飽和

個單或雙精確度浮點算數運算的結果為 \[ 0.0 f .。。1.0 f \] 範圍。



| \_坐 |
|-------|



 

[ **飽和** 指令結果] 修飾詞會針對結果值執行下列作業， (s 從已套用 sat 的浮點算數運算) \_ ：

`min(1.0f, max(0.0f, value))`

上述運算式中最小 () 和最大 () 的運作方式是 [最小值](min--sm4---asm-.md)、 [最大](max--sm4---asm-.md)值、最小值、 [dmin](dmin--sm5---asm-.md)或 [dmax](dmax--sm5---asm-.md) 的運作方式。

`_sat(NaN)` 依 min 和 max 的規則傳回0。

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

 

 




