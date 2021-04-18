---
title: callnz bool-vs
description: 如果不是零，則呼叫。 對標籤索引所標記的指令執行條件式呼叫。 |callnz bool-vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3932f4c5d50445b3220a0460a5c434a1ff8aae4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992114"
---
# <a name="callnz-bool---vs"></a>callnz bool-vs

如果不是零，則呼叫。 對標籤索引所標記的指令執行條件式呼叫。

## <a name="syntax"></a>Syntax



| callnz l \# 、 \[ ！ \]B\# |
|----------------------|



 

其中：

-   其中 l \# 是 [標籤-vs](label---vs.md) 標示要呼叫的副程式開頭。
-   \[!\] 這是選擇性的布林值 NOT 修飾詞。
-   b \# 識別 [常數布林值](dx9-graphics-reference-asm-vs-registers-constant-boolean.md)暫存器。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| callnz bool            |      | x    | x    | x     | x    | x     |



 

此指令會執行下列動作：


```
if (specified boolean register is not zero)
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

 

 




