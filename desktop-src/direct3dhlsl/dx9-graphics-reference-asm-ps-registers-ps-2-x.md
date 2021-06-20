---
title: ps_2_x 註冊
description: 本文包含圖元著色器版本2_x 所執行之輸入和輸出暫存器的參考資訊。
ms.assetid: 52bb6290-46e2-4d7d-9b96-b4c3e2abfe43
keywords:
- 註冊-ps_2_x
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be0e7f282978ada28c2dd71dc7c16dd317ddce42
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406701"
---
# <a name="ps_2_x-registers"></a>ps \_ 2 \_ x 註冊

圖元著色器相依于註冊來取得頂點資料、輸出圖元資料、在計算期間保存暫存結果，以及識別紋理取樣階段。 有數種類型的暫存器，各有獨特的功能。 本章節包含圖元著色器第2版所執行之輸入和輸出暫存器的參考資訊 \_ 。

## <a name="input-register-types"></a>輸入暫存器類型



| 註冊 | Name                                                                                          | Count      | R/W        | \# 讀取埠 | \# 讀取/inst | 尺寸 | RelAddr | Defaults                  | 需要 DCL |
|----------|-----------------------------------------------------------------------------------------------|------------|------------|---------------|---------------|-----------|---------|---------------------------|--------------|
| v\#      | [輸入色彩暫存器](dx9-graphics-reference-asm-ps-registers-input-color.md)               | 2          | R          | 1             | 無限制     | 4         | N       | 部分 (0001) 。 請參閱附注4 | Y            |
| r\#      | [暫時註冊](dx9-graphics-reference-asm-ps-registers-temporary.md)                   | 請參閱附注1 | R/W        | 3             | 無限制     | 4         | N       | 無                      | N            |
| c\#      | [常數 Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)         | 32         | R          | 1             | 2             | 4         | N       | 0000                      | N            |
| 我\#      | [常數整數暫存器](dx9-graphics-reference-asm-ps-registers-constant-integer.md)     | 16         | 請參閱附註 2 | 1             | 1             | 4         | N       | 0000                      | N            |
| B\#      | [常數布林值暫存器](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)     | 16         | 請參閱附註 2 | 1             | 1             | 1         | N       | FALSE                     | N            |
| P       | [述詞註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)                   | 1          | 請參閱附註 2 | 1             | 1             | 1         | N       | 無                      | Y            |
| s\#      | [ (Direct3D 9 asm-ps) 的取樣器 ](dx9-graphics-reference-asm-ps-registers-sampler.md)            | 16         | 請參閱附注3 | 1             | 1             | 4         | N       | 請參閱附注5                | Y            |
| t\#      | [材質座標註冊](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) | 8          | R          | 1             | 1             | 4         | N       | 無                      | Y            |



 

注意：

1.  最多12分鐘/32 max： r 暫存器的數目 \# 取決於 D3DPSHADERCAPS2 \_ 0. NumTemps (，其範圍從12到 32) 。
2.  只能由流程式控制制指令使用。
3.  僅供紋理取樣指令使用。
4.  部分 (x、y、z、w) -如果登錄中只更新頻道的子集，則其餘的通道會預設為指定的值 (x、y、z、w) 。
5.  取樣器查閱的預設值存在，但值相依于材質格式。

Readports 數目是每個暫存器類型 (的不同暫存器數目，) 可在單一指令中讀取。

## <a name="output-register-types"></a>輸出暫存器類型



| 註冊 | Name                                                                              | Count                                                                             | R/W | 尺寸 | RelAddr | Defaults | 需要 DCL |
|----------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----|-----------|---------|----------|--------------|
| Oc#     | [輸出色彩暫存器](dx9-graphics-reference-asm-ps-registers-output-color.md) | 查看 [多元素紋理 (Direct3D 9) ](/windows/desktop/direct3d9/multiple-element-textures) | W   | 4         | N       | 無     | N            |
| oDepth   | [輸出深度註冊](dx9-graphics-reference-asm-ps-registers-output-depth.md) | 1                                                                                 | W   | 1         | N       | 無     | N            |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 