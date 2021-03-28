---
title: 輸入色彩暫存器
description: 包含頂點色彩的圖元著色器輸入暫存器。
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372674"
---
# <a name="input-color-register"></a>輸入色彩暫存器

包含頂點色彩的圖元著色器輸入暫存器。

## <a name="syntax"></a>Syntax


```
dcl v#.writeMask
```



其中：

-   [ (sm2，sm3-ps asm) ](dcl---ps.md) 是暫存器宣告指令。
-   v 是輸入暫存器，而 \# 是註冊編號。 允許的暫存器數目取決於著色器版本。
-   writeMask 會判斷最多可 (四個) 寫入的元件。 有效的元件包括： (x、y、z、w) 或 (r、g、b、) 。

## <a name="remarks"></a>備註

色彩暫存器是唯讀的暫存器。 每個註冊包含四個元件的 RGBA 值，並從輸入頂點反復進行。 它們的精確度比大部分的暫存器低，保證在範圍 (0、+ 1) 中有8位不帶正負號的資料。 單一指令中不能使用一個以上的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[ps \_ 2 \_ 0 註冊](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[ps \_ 2 \_ x 註冊](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[ps \_ 3 \_ 0 註冊](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




