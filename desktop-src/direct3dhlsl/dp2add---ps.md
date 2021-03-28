---
title: dp2add-ps
description: 執行2D 點乘積和純量加法。
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88d3d28cc64bdb7caa1b7456e87711c3dbee2b13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104092447"
---
# <a name="dp2add---ps"></a>dp2add-ps

執行2D 點乘積和純量加法。

## <a name="syntax"></a>Syntax


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



其中：

-   dst 是目的地註冊。
-   src0、src1 和 src2 收取都是三個來源暫存器。
-   {x \| y \| z \| w} 是 src2 收取上所需的複寫 swizzle。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp2add                |      |      |      |      | x    | x    | x     | x    | x     |



 

Add 的純量值是由 src2 收取上的複寫 swizzle 所選擇。

下列程式碼片段會顯示已執行的作業。


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




