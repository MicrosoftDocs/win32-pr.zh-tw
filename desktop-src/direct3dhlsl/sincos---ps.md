---
title: sincos-ps
description: 計算正弦和余弦值（以弧度為單位）。 |sincos-ps
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e7ccdca91af206862384ae14cf25a85d0817814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991994"
---
# <a name="sincos---ps"></a>sincos-ps

計算正弦和余弦值（以弧度為單位）。

## <a name="syntax"></a>Syntax

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 和 ps \_ 2 \_ x



| sincos dst。版|x|xy}、src0。版|x|#a1|w}、src1、src2 收取 |
|------------------------------------------------------|



 

其中：

-   dst 是目的地註冊，而且必須是 (r) 的 [暫時性註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) \# 。 目的地暫存器必須剛好有下列三個遮罩中的其中一個：. x. x. x. x. \| y \| 。
-   src0 是提供輸入角度的來源暫存器，其必須在 \[ -pi、+ pi 內 \] 。 {x \| y \| z \| w} 是必要的複製 swizzle。
-   src1 和 src2 收取是來源暫存器，必須是兩個不同的 [常數 Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c \#) 。 Src1 和 src2 收取的值必須分別是宏 [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) 和 [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) 的值。

### <a name="ps_3_0"></a>ps \_ 3 \_ 0



| sincos dst。版|x|xy}、src0。版|x|#a1|w |
|------------------------------------------|



 

其中：

-   dst 是目的地註冊，必須是 [暫時的註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) 。 目的地暫存器必須剛好有下列三個遮罩中的其中一個：. x. x. x. x. \| y \| 。
-   src0 是提供輸入角度的來源暫存器，其必須在 \[ -pi、+ pi 內 \] 。 {x \| y \| z \| w} 是必要的複製 swizzle。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| sincos                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 和 ps \_ 2 \_ x

針對 ps \_ 2 \_ 0 和 ps \_ 2 \_ x，sincos 可以搭配 predication 使用，但 [對述](dx9-graphics-reference-asm-ps-registers-predicate.md) 詞登錄的 swizzle 有一項限制 (p0) ：只允許複寫 swizzle (. \| y. \| z \| . w) 。

針對 ps \_ 2 \_ 0 和 ps \_ 2 \_ x，指令的運作方式如下 (V = src0 與複寫 swizzle) 的純量值：

-   如果寫入遮罩是. x：
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   如果寫入遮罩為. y：
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   如果寫入遮罩是 xy：
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

針對 ps \_ 3 \_ 0，sincos 可以搭配 predication 使用，而不受任何限制。 請參閱述詞 [註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)。

針對 ps \_ 3 \_ 0，指令的運作方式如下 (V = src0 與複寫 swizzle) 的純量值：

-   如果寫入遮罩是. x：
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   如果寫入遮罩為. y：
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   如果寫入遮罩是 xy：
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

應用程式可以使用下列著色器的虛擬程式碼，將任意角度 (弧度) 至範圍 \[ -pi、+ pi \] ：


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
