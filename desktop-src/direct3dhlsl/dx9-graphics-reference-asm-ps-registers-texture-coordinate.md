---
title: '材質座標註冊 (HLSL PS 參考) '
description: 包含材質座標的圖元著色器輸入暫存器。
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 456ea0da6c1c23f51dbdba357f18de747b318e6a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104971628"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a>材質座標註冊 (HLSL PS 參考) 

包含材質座標的圖元著色器輸入暫存器。



| 圖元著色器版本       | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| 材質座標註冊 |      |      |      |      | x    | x     | x    | x    | x     |



 

材質座標註冊包含材質座標資料。 使用紋理座標暫存器之前，必須先使用圖元著色器宣告來宣告。 For details about how to declare a texture register, see [dcl - (sm2, sm3 - ps asm)](dcl---ps.md).

此外，以下是材質座標註冊的一些其他屬性。

-   有八個圖元著色器紋理座標暫存器（t0 至 t7）。
-   這些是唯讀的暫存器。
-   它們包含從輸入頂點反覆運算的四個元件 RGBA 值。
-   它們包含從頂點資料中插入的高精確度、高動態範圍資料值。 系統會以觀點正確的插補來產生值。 資料是浮點精確度，並經過簽署。
-   單一指令中最多隻有一個。
-   著色器內的多個紋理座標暫存器讀取必須使用相同的 [目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)。
-   選擇性的局部有效位數修飾詞 \[ \_ pp \] 適用于相依讀取。 這是因為部分有效位數會影響涉及紋理座標註冊的算數運算。 它不會影響材質位址指示的精確度，因為它不會影響材質座標反覆運算器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




