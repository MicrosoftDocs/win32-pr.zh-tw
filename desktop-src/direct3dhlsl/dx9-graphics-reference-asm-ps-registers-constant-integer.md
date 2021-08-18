---
title: '常數整數 register (HLSL PS 參考) '
description: 常數整數暫存器只能由迴圈-ps 和 rep-ps 使用。
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce2d9ba19f97439da098563639bc8940cdae2f202a6f24cdd1940e25cfc14e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489379"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a>常數整數 register (HLSL PS 參考) 

常數整數暫存器只能由 [迴圈-ps](loop---ps.md) 和 [rep-ps](rep---ps.md)使用。

您可以使用 [defi-ps](defi---ps.md) 或 [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)來設定它們。

當做 [迴圈 ps](loop---ps.md) 指令的引數使用時：

-   . x 是反復專案計數。  ([代表-ps](rep---ps.md) 只會使用此元件) 。
-   . y 是迴圈計數器的起始值。
-   . z 是迴圈計數器的遞增步驟。



| 圖元著色器版本     | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| 常數整數暫存器 |      |      |      |      |      |       | x    | x    | x     |



 

在 Direct3D 8 和 Direct3D 9 之間變更著色器常數的行為。

-   針對 Direct3D 9，使用 defx 設定的常數會將值指派給著色器常數空間。 使用 defx 宣告之常數的存留期只限于該著色器的執行。 相反地，使用 Api 設定的常數 SetXXXShaderConstantX 會初始化全域空間中的常數。 在呼叫 SetxxxShaderConstants 之前，不會將全域空間中的常數複製到 (著色器) 可見的本機空間。
-   針對 Direct3D 8，使用 defx 或 Api 設定的常數都會將值指派給著色器常數空間。 每次執行著色器時，目前的著色器都會使用常數，而不考慮用來設定它們的技巧。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 