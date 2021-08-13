---
title: callnz bool-ps
description: 如果不是零，則呼叫。 對標籤索引所標記的指令執行條件式呼叫。 |callnz bool-ps
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 793feb1934b86b46f26050a67b5f26d94b9f277e31735c4d1912805374bab903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516623"
---
# <a name="callnz-bool---ps"></a>callnz bool-ps

如果不是零，則呼叫。 對標籤索引所標記的指令執行條件式呼叫。

## <a name="syntax"></a>Syntax



| callnz l \# 、 \[ ！ \]B\# |
|----------------------|



 

其中：

-   l \# 是標示要呼叫的副程式開頭的 [標籤（ps）](label---ps.md) 。
-   \[!\] 這是選擇性的否定修飾詞。
-   b \# 識別 [常數布林值](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz bool           |      |      |      |      |      | x    | x     | x    | x     |



 

此指令會執行下列動作：


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




