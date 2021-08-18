---
title: HLSL 與參考) 的指令修飾詞 (
description: 指令修飾詞
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2bdad90d13fe960c0d7a5cabfbb508d8abba890e8114c6d4ae1e47d1977e7d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119692"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a>HLSL 與參考) 的指令修飾詞 (

指令修飾詞會在將指令寫入目的地登錄之前，先影響指令的結果。

## <a name="_sat"></a>\_坐

在寫入目的地登錄之前， (或個將指令結果) 至 \[ 0，1個 \] 範圍內。

例如：


```
add_sat dst, src0, src1
```



其中：

dst = \_ 介於 \_ 0 \_ 和1之間的夾具 \_ (src0 + src1) 

\_Sat 指令修飾詞的成本沒有額外的指示位置。

如果支援，則 \_ 除了： [frc-vs](frc---vs.md)、 [sincos-vs](sincos---vs.md)和 [texldl-vs](texldl---vs.md)，sat 指令修飾詞可以搭配任何指令使用。



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| \_坐                  |      |      |      |       | x    | x     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




