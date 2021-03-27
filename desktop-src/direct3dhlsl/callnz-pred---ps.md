---
title: callnz pred-ps
description: 使用述詞來呼叫，如果不是零，則為。 對標籤索引所標記的指令執行條件式呼叫。 Predication 會使用布林值來判斷是否要執行指令。
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a04bd4b1bfa16d965a90b66e3956674ecb112590
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "103932815"
---
# <a name="callnz-pred---ps"></a>callnz pred-ps

使用述詞來呼叫，如果不是零，則為。 對標籤索引所標記的指令執行條件式呼叫。 Predication 會使用布林值來判斷是否要執行指令。

## <a name="syntax"></a>Syntax



| callnz l \# 、 \[ ！ \]P。版|x|#a1|w |
|----------------------------------|



 

其中：

-   其中 l \# 是 [標籤-ps](label---ps.md) ，標示要呼叫的副程式開頭。
-   \[!\] 這是選擇性的否定修飾詞。
-   p0 是述詞註冊。 請參閱述詞 [註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)。
-   {x \| y \| z \| w} 是 p0 上所需的複寫 swizzle。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz pred           |      |      |      |      |      | x    | x     | x    | x     |



 

此指令會執行下列動作：


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




