---
title: rep-vs
description: 開始 a rep .。。endrep 組塊。
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5441d5d134ee2d60e14db9f273ec374323f93902
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373767"
---
# <a name="rep---vs"></a>rep-vs

開始 a rep .。。[endrep](endrep---vs.md) 組塊。

## <a name="syntax"></a>Syntax



| rep\# |
|---------|



 

其中 i \# 是指定. x 元件中重複計數的整數暫存器。 請參閱 [常數整數註冊](dx9-graphics-reference-asm-vs-registers-constant-integer.md)。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| 代表                    |      | x    | x    | x     | x    | x     |



 

-   \#x.x.x.x 會指定反復專案計數。 合法範圍是 \[ 0，255 \] 。 請注意，此指令不會遞增或遞減 i \# . x 的值。
-   \#yzw 不是由重複區塊使用。
-   重複區塊可能會進行嵌套。 請參閱 [流程式控制制的嵌套限制](dx9-graphics-reference-asm-vs-instructions-flow-control.md)。
-   重複區塊可以完全在 if \* 區塊內或完全圍繞它。 不允許任何 straddling。
-   針對不同或嵌套的 rep 表示，使用相同的 i， \# 每個迴圈都會根據指定的計數逐一進行反覆運算。

## <a name="example"></a>範例


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




