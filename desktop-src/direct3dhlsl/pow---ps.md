---
title: pow-ps
description: 完整有效位數 abs (src0) src1。 |pow-ps
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974008"
---
# <a name="pow---ps"></a>pow-ps

完整有效位數 abs (src0) <sup>src1</sup>。

## <a name="syntax"></a>Syntax



| pow dst、src0、src1 |
|---------------------|



 

其中

-   dst 是目的地註冊。
-   src0 是輸入來源註冊。 來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。
-   src1 是輸入來源註冊。 來源暫存器需要明確使用複寫 swizzle，也就是，只有其中一個. x、. y、a-z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| pow                   |      |      |      |      | x    | x    | x     | x    | x     |



 

此指示的運作方式如下：

dest. x = dest. y = dest. z = dest. w = \[ abs (src0) \] <sup>src1</sup>;

這是純量指令，因此來源暫存器應該具有複寫 swizzles，以指出要使用的通道。

輸入 power (src1) 必須是純量。

純量結果會複寫到所有的四個輸出通道。

此指令可以擴充為 exp (src1 \* 記錄 (src0) ) 。

Dst 暫存器應該是暫時的註冊，而且不應該與 src1 相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




