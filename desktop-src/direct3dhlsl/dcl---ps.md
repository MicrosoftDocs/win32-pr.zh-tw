---
title: 'dcl- (sm2、sm3-ps asm) '
description: 宣告圖元著色器輸入暫存器。
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad61ea8d733ed01fcd2e57ba06c38e0b3efac682
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2019
ms.locfileid: "104373851"
---
# <a name="dcl---sm2-sm3---ps-asm"></a>dcl- (sm2、sm3-ps asm) 

宣告圖元著色器輸入暫存器。

## <a name="syntax"></a>Syntax



|                           |
|---------------------------|
| dcl \[ \_ pp \] 目標 \[ . 遮罩\] |



 

其中：

-   \[\_pp \] 是選擇性的局部有效位數。 請參閱 [部分有效位數](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)。
-   dest 是目的地註冊。 它必須是 [輸入色彩](dx9-graphics-reference-asm-ps-registers-input-color.md) 暫存器 (vn) 或 [紋理座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) 。
-   \[mask \] 是選擇性的寫入遮罩，可控制可寫入目的地登錄的哪些元件。 請參閱 [目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dcl                   |      |      |      |      | x    | x    | x     | x    | x     |



 

所有的 dcl 指令都必須出現在第一個可執行指令之前。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




