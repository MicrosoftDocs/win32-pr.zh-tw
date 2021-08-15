---
title: 迴圈-ps
description: 開始迴圈 .。。endloop-ps block。
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a08d2954b478bd6afd0c52d517e07a82ba3ee148dd07f839ec7d8787d93c2134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510981"
---
# <a name="loop---ps"></a>迴圈-ps

開始迴圈 .。。[endloop-ps](endloop---ps.md) block。

## <a name="syntax"></a>Syntax



| 迴圈 aL、i\# |
|--------------|



 

其中：

-   aL 是包含目前迴圈計數的 [迴圈計數器](dx9-graphics-reference-asm-ps-registers-loop-counter.md) 暫存器。
-   我 \# 是 [常數整數註冊](dx9-graphics-reference-asm-ps-registers-constant-integer.md)。 請參閱＜備註＞。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| loop                  |      |      |      |      |      |      |       | x    | x     |



 

-   [迴圈計數器](dx9-graphics-reference-asm-ps-registers-loop-counter.md)暫存器 (aL) 保存目前的迴圈計數，並且可用於在迴圈區塊內 (v) 的[輸入色彩](dx9-graphics-reference-asm-ps-registers-input-color.md)暫存器中的相對定址 \# 。
-   \#x.x.x.x 會指定反復專案計數。 合法範圍是 \[ 0，255 \] 。 請注意，此指令不會遞增或遞減 i \# . x 的值。
-   i. \# 指定 [迴圈計數器 Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) Register 的初始值。 合法範圍是 \[ 0，255 \] 。 請注意，此指令不會遞增或遞減 i \# . y 的值。
-   i \# . z 指定步驟/stride 的大小。 合法範圍為 \[ -128、127 \] 。
-   \#在迴圈區塊中不會使用 w，而且必須是0。
-   迴圈區塊可能會進行嵌套。 請參閱[Flow 控制限制](dx9-graphics-reference-asm-ps-instructions-flow-control.md)。
-   當進行嵌套時， [迴圈計數器 Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) 是指立即封閉迴圈區塊。
-   迴圈區塊可以完全在 if \* 區塊內或完全圍繞它。 不允許任何 straddling。

## <a name="example"></a>範例


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




