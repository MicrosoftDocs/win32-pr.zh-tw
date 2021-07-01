---
title: 'dcl_semantics (sm3-ps asm) '
description: 宣告頂點著色器輸出和圖元著色器輸入之間的關聯。
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c506d2ad23003f93bbaea409cacc60b18c86534
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129705"
---
# <a name="dcl_semantics-sm3---ps-asm"></a>dcl \_ 語義 (sm3-ps asm) 

宣告頂點著色器輸出和圖元著色器輸入之間的關聯。

## <a name="syntax"></a>Syntax

\_ \[ \_ 距心 \] dst 的 dcl 語義 \[ 。寫入 \_ 遮罩\]



 

其中：

-   \_語義：識別預期的資料使用方式，而且可以是 [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (中沒有 D3DDECLUSAGE 前置詞) 的任何值 \_ 。 此外，您可以將整數索引附加至語義，以區分使用類似語義的參數。
-   \[\_[距心](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \]這是選擇性的指令修飾詞。 在宣告輸入暫存器 \_ 和紋理查閱指示的 dcl 使用指示上支援此功能。 距心會附加沒有空格的位置。
-   dst：目的地註冊。 請參閱 [ps \_ 3 \_ 0 註冊](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)。
-   寫入 \_ 遮罩：相同的輸出暫存器可以多次宣告，每次都有唯一的寫入遮罩 (如此一來，就可以將不同的語義套用至) 的個別元件。 不過，在宣告中不能多次使用相同的語義。 這表示向量必須是四個或更少的元件，而且無法跨四個元件的暫存器界限 (個別的輸出暫存器) 。 \_使用 psize 語義時，它應該有完整的寫入遮罩，因為它會被視為純量。 \_使用位置語義時，它應該有完整的寫入遮罩，因為必須寫入全部四個元件。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dcl \_ 使用方式            |      |      |      |      |      |      |       | x    | x     |



 

所有 \_ 的 dcl 使用方式指令都必須出現在第一個可執行指令之前。

## <a name="declaration-examples"></a>宣告範例


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[消除鋸齒範例](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)
</dt> </dl>

 

 
