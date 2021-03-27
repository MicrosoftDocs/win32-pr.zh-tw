---
title: '常數整數 Register (HLSL 與參考) '
description: 常數整數暫存器只會用於迴圈-vs 和 rep-vs。
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4cf2612eccb891ce0cffd04955e4997173e84007
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971760"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a>常數整數 Register (HLSL 與參考) 

常數整數暫存器只會用於 [迴圈-vs](loop---vs.md) 和 [rep-vs](rep---vs.md)。

您可以使用 [defi-vs](defi---vs.md) 或 [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)來設定它們。

當做迴圈的引數使用時 [（vs](loop---vs.md) 指令）：

-   . x 是反復專案計數。  ([rep-vs](rep---vs.md) 只會) 使用此元件。
-   . y 是迴圈計數器的起始值。
-   . z 是迴圈計數器的遞增步驟。

在 Direct3D 8 和 Direct3D 9 之間變更著色器常數的行為。

-   針對 Direct3D 9，使用 defx 設定的常數會將值指派給著色器常數空間。 使用 defx 宣告之常數的存留期只限于該著色器的執行。 相反地，使用 Api 設定的常數 SetXXXShaderConstantX 會初始化全域空間中的常數。 在呼叫 SetxxxShaderConstants 之前，不會將全域空間中的常數複製到 (著色器) 可見的本機空間。
-   針對 Direct3D 8，使用 defx 或 Api 設定的常數都會將值指派給著色器常數空間。 每次執行著色器時，目前的著色器都會使用常數，而不考慮用來設定它們的技巧。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 