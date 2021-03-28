---
title: 迴圈-vs
description: 開始迴圈 .。。endloop 組塊。
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6a96a1ce53b850ec8feeba282055e8111b275bfd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990778"
---
# <a name="loop---vs"></a>迴圈-vs

開始迴圈 .。。[endloop](endloop---vs.md) 組塊。

## <a name="syntax"></a>Syntax



| 迴圈 aL、i\# |
|--------------|



 

其中：

-   aL 是包含目前迴圈計數的 [迴圈計數器](dx9-graphics-reference-asm-vs-registers-loop-counter.md) 暫存器。
-   我 \# 是 [常數整數註冊](dx9-graphics-reference-asm-vs-registers-constant-integer.md)。 請參閱＜備註＞。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| loop                   |      | x    | x    | x     | x    | x     |



 

-   [迴圈計數器](dx9-graphics-reference-asm-vs-registers-loop-counter.md)暫存器 (aL) 保留目前的迴圈計數，並且可用於在迴圈區塊內 (o) 中的「[常數整數](dx9-graphics-reference-asm-vs-registers-constant-integer.md)暫存器」 (c \#) 或[輸出](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)暫存器的相對定址 \# 。
-   \#x.x.x.x 會指定反復專案計數。 合法範圍是 \[ 0，255 \] 。 請注意，此指令不會遞增或遞減 i \# . x 的值。
-   i. \# 指定 [迴圈計數器 Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) Register 的初始值。 合法範圍是 \[ 0，255 \] 。 請注意，此指令不會遞增或遞減 i \# . y 的值。
-   i \# . z 指定步驟/stride 的大小。 合法範圍為 \[ -128、127 \] 。
-   i. \# 未使用，且必須設定為0。
-   迴圈區塊可能會進行嵌套。 請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md)。
-   當進行嵌套時， [迴圈計數器 Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) 是指立即封閉迴圈區塊。
-   迴圈區塊可以完全在 if \* 區塊內或完全圍繞它。 不允許任何 straddling。

## <a name="example"></a>範例


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




