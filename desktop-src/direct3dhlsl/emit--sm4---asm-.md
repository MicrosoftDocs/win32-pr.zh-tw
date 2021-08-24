---
title: '發出 (sm4-asm) '
description: 發出頂點。
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce90ed4ea87c74c09c6f45d590e8bc7a70bbb8178988b059c2b3a79726aabcb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673078"
---
# <a name="emit-sm4---asm"></a>發出 (sm4-asm) 

發出頂點。



| 發出 |
|------|



 

## <a name="remarks"></a>備註

**發出** 會導致 \# 從幾何著色器讀取所有宣告的 o 暫存器，以產生頂點。

發出多個 **發出** 呼叫時，會產生基本專案。

**發出** 可能會在幾何著色器中出現任何次數，包括 flow 控制項。

如果已宣告資料流程，您必須使用 [發出 \_ 資料流程](emit-stream--sm5---asm-.md)。

此指示適用于下列著色器階段：



| 頂點著色器 | 幾何著色器 | 像素著色器 |
|---------------|-----------------|--------------|
|               | x               |              |



 

### <a name="minimum-shader-model"></a>最小著色器模型

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

 

 




