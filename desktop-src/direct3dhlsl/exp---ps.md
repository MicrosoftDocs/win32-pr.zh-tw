---
title: exp-ps
description: 提供完整的精確度指數2x。 |exp-ps
ms.assetid: 09e4446f-4149-4ec8-b3e3-2045b55bd591
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acd7c50c1f0d6ff08ee5d66e50fdd3e56939f0d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104035252"
---
# <a name="exp---ps"></a>exp-ps

提供完整的精確度指數 2<sup>x</sup>。

## <a name="syntax"></a>Syntax



| exp dst、src |
|--------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。 來源註冊需要明確使用複寫 swizzle;也就是，您必須指定一個. x、. y、z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。 請參閱 [來源註冊 Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| exp                   |      |      |      |      | x    | x    | x     | x    | x     |



 

下列程式碼片段會顯示執行的作業：


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




