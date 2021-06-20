---
title: ps_3_0 註冊
description: 本文包含圖元著色器版本3_0 所執行之輸入和輸出暫存器的參考資訊。
ms.assetid: 01bee50a-c1b7-4b15-9df8-1dd52d9ff163
keywords:
- vPos
- 位置暫存器，圖元著色器
- 註冊-ps_3_0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1cd0173beabc8fbe21ad15e88e23fc1b6e84892
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405491"
---
# <a name="ps_3_0-registers"></a>ps \_ 3 \_ 0 註冊

圖元著色器相依于註冊來取得頂點資料、輸出圖元資料、在計算期間保存暫存結果，以及識別紋理取樣階段。 有數種類型的暫存器，各有獨特的功能。 本章節包含圖元著色器第3版所執行之輸入和輸出暫存器的參考資訊 \_ 。

## <a name="new-registers"></a>新的暫存器

### <a name="input-register"></a>輸入暫存器

輸入暫存器 (v \#) 現已完全浮點數，而且 [紋理座標](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)登錄 s (t \#) 已合併至其中。 在著色器頂端 [ \_ (sm3-ps asm) 的 dcl 語義 ](dcl-usage---ps.md) 是用來描述特定輸入暫存器中的穩 \_ 。 圖元型別的語義是 (類似于此模型的頂點端) 所引進。 當輸入暫存器定義為色彩 (例如紋理座標) 時，不會執行任何固定。 當取樣時，定義為色彩的暫存器評估與材質座標不同。

### <a name="face-register"></a>臉部登記

臉部暫存器 (vFace) 是此模型的新功能。 這是浮點純量暫存器，最後會包含基本區域。 不過，在 ps \_ 3 0 中， \_ 只有這個註冊的正負號有效。 因此，如果值小於零 (則會將正負號位設為負值) 而 (區域是負數，則會逆時針) 。 因此，在 ps \_ 3 0 中，將此暫存器與 \_ 0 (> 0 或 < 0) 比較是合理的。 在圖元著色器中，應用程式可以決定要使用的光源技術。 您可以透過這種方式來達成雙面光源。 此暫存器需要宣告，因此未宣告的使用方式將會標示為錯誤。 對於線條和點基本類型，此暫存器是未定義的。 臉部暫存器只能用來做為具有下列指示的條件： [setp \_ -ps](setp-comp---ps.md)、（ [如果 \_ ](if-comp---ps.md)是）或 [中斷 \_ 複合 ps](break-comp---ps.md)。

### <a name="loop-counter-register"></a>迴圈計數器暫存器

[迴圈計數器 Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) 是此模型的新功能。 它會在每次執行[迴圈 ps](loop---ps.md) / [endloop-ps](endloop---ps.md)區塊時自動遞增。 如有需要，可在區塊中用來進行相對定址。 在迴圈外使用迴圈計數器暫存器是不正確。

### <a name="position-register"></a>位置註冊

此模型的新位置註冊 (vPos) 。 它包含目前的圖元 (x，y) 在對應的通道中。  (z、w) 頻道未定義。 此暫存器需要宣告，因此未宣告的使用方式將會標示為錯誤。 宣告時，此暫存器必須正好具有下列其中一個遮罩：. x、. y、xy。

## <a name="input-register-types"></a>輸入暫存器類型



| 註冊 | Name                                                                                      | Count | R/W | \# 讀取埠 | \# 讀取/inst | 尺寸 | RelAddr | Defaults   | 需要 DCL |
|----------|-------------------------------------------------------------------------------------------|-------|-----|---------------|---------------|-----------|---------|------------|--------------|
| v\#      | [輸入暫存器](dx9-graphics-reference-asm-ps-registers-input-color.md)                 | 10    | R   | 1             | 無限制     | 4         | 鋁      | 無       | 是          |
| r\#      | [暫時註冊](dx9-graphics-reference-asm-ps-registers-temporary.md)               | 32    | R/W | 3             | 無限制     | 4         | 否      | None       | 否           |
| c\#      | [常數 Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)     | 224   | R   | 1             | 無限制     | 4         | 否      | 0000       | 否           |
| 我\#      | [常數整數暫存器](dx9-graphics-reference-asm-ps-registers-constant-integer.md) | 16    | R   | 1             | 1             | 4         | 否      | 0000       | 否           |
| B\#      | [常數布林值暫存器](dx9-graphics-reference-asm-ps-registers-constant-boolean.md) | 16    | R   | 1             | 1             | 1         | 否      | FALSE      | 否           |
| P       | [述詞註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)               | 1     | R   | 1             | 1             | 1         | 否      | None       | 否           |
| s\#      | [ (Direct3D 9 asm-ps) 的取樣器 ](dx9-graphics-reference-asm-ps-registers-sampler.md)        | 16    | R   | 1             | 1             | 4         | 否      | 請參閱附注1 | 是          |
| vFace    | 臉部 \_ 登記                                                                            | 1     | R   | 1             | 無限制     | 1         | 否      | None       | 是          |
| vPos     | 位置 \_ 註冊                                                                        | 1     | R   | 1             | 無限制     | 4         | 否      | None       | 是          |
| 鋁       | 迴圈 \_ 計數器暫存器 \_                                                                   | 1     | R   | 1             | 無限制     | 1         | n/a     | 無       | 否           |



 

注意：

-   取樣器查閱的預設值存在，但值相依于材質格式。

Readports 數目是每個暫存器類型 (的不同暫存器數目，) 可在單一指令中讀取。

## <a name="output-register-types"></a>輸出暫存器類型



| 註冊 | Name                                                                              | Count                                                                             | R/W | 尺寸 | RelAddr | Defaults | 需要 DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| Oc#     | [輸出色彩暫存器](dx9-graphics-reference-asm-ps-registers-output-color.md) | 查看 [多元素紋理 (Direct3D 9) ](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | 否      | None     | 否           |
| oDepth   | [輸出深度註冊](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | 否      | None     | 否           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 