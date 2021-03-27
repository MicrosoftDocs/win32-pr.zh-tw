---
title: '常數 Boolean register (HLSL PS 參考) '
description: 此暫存器是靜態流程式控制制 (指令中使用的位集合，例如，如果 bool-ps---------ps) 。
ms.assetid: fb4abe19-d0cf-48ac-866e-4be60cc86bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4868be7c22ce5a6a1881ad7db8acf0af65330c04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682820"
---
# <a name="constant-boolean-register-hlsl-ps-reference"></a>常數 Boolean register (HLSL PS 參考) 

此暫存器是靜態流程式控制制指示中使用的位集合 (例如，[如果 bool-ps](if-bool---ps.md)（ps）-ps  -  [](else---ps.md)  -  [](endif---ps.md)) 。 其中有16個，因此著色器可以有16個獨立的分支條件。 您可以使用 [defb-ps](defb---ps.md) 或 [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)來設定它們。

在 Direct3D 8 和 Direct3D 9 之間變更著色器常數的行為。

-   針對 Direct3D 9，使用 defx 設定的常數會將值指派給著色器常數空間。 使用 defx 宣告之常數的存留期只限于該著色器的執行。 相反地，使用 Api 設定的常數 SetXXXShaderConstantX 會初始化全域空間中的常數。 在呼叫 SetxxxShaderConstants 之前，不會將全域空間中的常數複製到 (著色器) 可見的本機空間。
-   針對 Direct3D 8，使用 defx 或 Api 設定的常數都會將值指派給著色器常數空間。 每次執行著色器時，目前的著色器都會使用常數，而不考慮用來設定它們的技巧。



| 圖元著色器版本     | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| 常數布林值暫存器 |      |      |      |      |      |       | x    | x    | x     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 