---
title: pow-vs
description: 完整有效位數 abs (src0) src1。 |pow-vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3263fa19015bc32c94ae714891c3bbb2128c9463
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195918"
---
# <a name="pow---vs"></a>pow-vs

完整有效位數 abs (src0) <sup>src1</sup>。

## <a name="syntax"></a>Syntax



| pow dst、src0、src1 |
|---------------------|



 

其中

-   dst 是目的地註冊。
-   src0 是輸入來源註冊。 來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。
-   src1 是輸入來源註冊。 來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。

## <a name="remarks"></a>備註



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| pow                    |      | x    | x    | x     | x    | x     |



 

此指示的運作方式如下所示。


```
dest = pow(abs(src0), src1);
```



這是純量指令，因此來源暫存器應該具有複寫 swizzles，以指出要使用的通道。

純量結果會複寫到所有的四個輸出通道。

此指令可以擴充為 exp (src1 \* 記錄 (src0) ) 。

有效位數不是低於15個位。

目的地暫存器應該是臨時暫存器，而且不應該與 src1 是相同的註冊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器指示](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




