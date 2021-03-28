---
title: endloop-vs
description: 迴圈結束 .。。endloop 組塊。
ms.assetid: fd7df120-a927-4a66-b152-6ce5247446e4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a9aec4d1b2c5237a87fae2c0beab4e8d995db97
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373691"
---
# <a name="endloop---vs"></a>endloop-vs

[迴圈](loop---vs.md)結束 .。。endloop 組塊。

## <a name="syntax"></a>Syntax



| endloop |
|---------|



 

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| endloop                |      | x    | x    | x     | x    | x     |



 

此指示的運作方式如下所示。


```
LoopCounter += LoopStep;
LoopInterationCount = LoopIterationCount - 1;
if (LoopIterationCount > 0)
    Continue execution at the StartLoopOffset
```



endloop 必須遵循 [迴圈-vs](loop---vs.md) 區塊的最後一個指令。

## <a name="example"></a>範例


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




