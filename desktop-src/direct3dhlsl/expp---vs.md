---
title: expp-vs
description: 提供部分有效位數指數2x。
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0d57e2723c90eee8df728aa540baeab86932e773
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679136"
---
# <a name="expp---vs"></a>expp-vs

提供部分有效位數指數 2<sup>x</sup>。

## <a name="syntax"></a>Syntax



| expp dst、src。版|x|#a1|w |
|----------------------------|



 

其中：

-   dst 是目的地註冊。
-   src 是來源暫存器。 來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。
-   {x \| y \| z \| w} 是在來源註冊上所需的複寫 swizzle。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| expp                   | x    | x    | x    | x     | x    | x     |



 

### <a name="vs_1_1"></a>vs \_ 1 \_ 1

依據頂點著色器版本而 [定，exp vs](exp---vs.md) 指令的運作方式會有所不同。

在 vs \_ 1 \_ 1 中，expp 指令會提供下列結果：


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



在 vs \_ 2 \_ 0 和更新的中，expp 指令會提供下列結果：


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a>vs \_ 2 \_ 0

在 vs \_ 2 \_ 0 和更新的中，指令的運作方式如下：


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



指令至少提供10個位的精確度。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




