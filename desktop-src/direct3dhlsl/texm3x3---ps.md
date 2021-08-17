---
title: texm3x3-ps
description: 當與兩個 texm3x3pad ps 指令搭配使用時，會執行3x3 矩陣乘法。
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 17030bb99eb472b5cffe53474eb04c30159e5e30ffb2d219f1ac47dfce9da205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787731"
---
# <a name="texm3x3---ps"></a>texm3x3-ps

當與兩個 [texm3x3pad ps](texm3x3pad---ps.md) 指令搭配使用時，會執行3x3 矩陣乘法。

## <a name="syntax"></a>Syntax



| texm3x3 dst、src |
|------------------|



 

其中

-   dst 是目的地註冊。
-   src 是來源暫存器。

## <a name="remarks"></a>備註



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3               |      | x    | x    |      |      |      |       |      |       |



 

此指示與 [texm3x3tex ps](texm3x3tex---ps.md) 指令相同，不需要材質查閱。

此指令會當做三個指示的最後三個指示使用，表示3x3 矩陣乘法運算。 3x3 矩陣是由第三個材質階段的材質座標，以及兩個先前的材質階段所組成。 任何指派給三個材質階段的材質都會被忽略。

此指令必須搭配兩個 texm3x3pad 指令使用。 材質暫存器必須遵循下列順序。


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



以下是有關3x3 乘法如何完成的更多詳細資料。

第一個 texm3x3pad 指令會執行乘法的第一個資料列來尋找 u<sup>'</sup>。

u<sup>'</sup> = TextureCoordinates (階段 m) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

第二個 texm3x3pad 指令會執行乘法的第二個數據列，以找出 v<sup>'</sup>。

v<sup>'</sup> = TextureCoordinates (階段 m + 1) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

Texm3x3tex 指令會執行乘法的第三個數據列，以找出 w<sup>'</sup>。

w<sup>'</sup> = TextureCoordinates (階段 m + 2) <sub>UVW</sub> \* t (n) <sub>RGB</sub>

將矩陣相乘的結果放在目的地暫存器中。

t (m + 2) <sub>RGBA</sub> = (u<sup>'</sup> 、v<sup>'</sup> 、w<sup>'</sup> 、1) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器指示](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




