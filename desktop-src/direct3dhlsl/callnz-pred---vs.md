---
title: callnz pred-vs
description: 如果不是零，則使用述詞來呼叫。 對標籤索引所標記的指令執行條件式呼叫。 Predication 會使用布林值來判斷是否要執行指令。
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1449ed9fb061ea2d5a83d37cb7c0d744a4c7e8b6517d49c0d2e32a10f7f5ed9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287022"
---
# <a name="callnz-pred---vs"></a>callnz pred-vs

如果不是零，則使用述詞來呼叫。 對標籤索引所標記的指令執行條件式呼叫。 Predication 會使用布林值來判斷是否要執行指令。

## <a name="syntax"></a>Syntax



| callnz l \# 、 \[ ！ \]P。版|x|#a1|w |
|----------------------------------|



 

其中：

-   l \# 是 [標籤-vs](label---vs.md) 標示要呼叫的副程式開頭。
-   \[!\] 這是選擇性的否定修飾詞。
-   p0 是述詞 [註冊](dx9-graphics-reference-asm-vs-registers-predicate.md)。
-   {x \| y \| z \| w} 是 p0 上所需的複寫 swizzle。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| callnz pred            |      |      | x    | x     | x    | x     |



 

此指令會執行下列動作：


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



此指令會使用一個頂點著色器指令位置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




