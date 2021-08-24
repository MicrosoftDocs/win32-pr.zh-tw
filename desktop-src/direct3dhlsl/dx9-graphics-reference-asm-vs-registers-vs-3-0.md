---
title: 註冊-vs_3_0
description: 本章節包含頂點著色器第3版所實之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: af81f1c4-9c11-455e-a565-1b80f1ee8683
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d658d2d14d149d5d83d673269f2a414d7feaa22f13f1b32f57c4b80500fb1398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673098"
---
# <a name="registers---vs_3_0"></a>註冊-vs \_ 3 \_ 0

本章節包含頂點著色器第3版所實之輸入和輸出暫存器的參考資訊 \_ 。

## <a name="input-registers"></a>輸入暫存器



| 註冊 | 名稱                                                                                      | 計數      | R/W | \# 讀取埠 | \# 讀取/inst | 尺寸 | RelAddr | Defaults     | 需要 DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| v\#      | [輸入暫存器](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | 無限制       | 4         | a0/aL   | 請參閱附注1   | Yes          |
| R\#      | [暫時註冊](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 32         | R/W | 3             | 無限制       | 4         | 否      | 無         | No           |
| c\#      | [常數 Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | 請參閱附註 2 | R   | 1             | 無限制       | 4         | a0/aL   |  (0、0、0、0)  | No           |
| a0       | [位址註冊](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W | 1             | 無限制       | 4         | 否      | 無         | No           |
| B\#      | [常數布林值暫存器](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | 否      | FALSE        | No           |
| i\#      | [常數整數暫存器](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | 否      |  (0、0、0、0)  | No           |
| 鋁       | [迴圈計數器暫存器](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 無限制       | 1         | 否      | 無         | No           |
| P       | [述詞註冊](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | R/W | 1             | 1               | 4         | 否      | 無         | 否           |
| s\#      | [ (Direct3D 9 asm 的取樣器-vs) ](dx9-graphics-reference-asm-vs-registers-sampler.md)        | 4          | R   | 1             | 1               | 4         | 否      | 請參閱附注3   | Yes          |



 

注意：

1.  部分 (0、0、0、1) -如果只有一部分的通道已更新，則其餘的通道會預設為 (0、0、0、1) 。
2.  等於 D3DCAPS9。Vs \_ 3 0) 的 MaxVertexShaderConst (至少 256 \_ 。
3.  取樣器查閱的預設值存在，但值相依于材質格式。

## <a name="output-registers"></a>輸出暫存器

輸出暫存器已折迭為 12 o \# (輸出) 註冊。 這些可用於使用者想要插入圖元著色器的任何內容：材質座標、色彩、霧化等等。



| 註冊 | 名稱            | 計數 | R/W | 尺寸 | RelAddr | Defaults | 需要 DCL |
|----------|-----------------|-------|-----|-----------|---------|----------|--------------|
| 輸出\#      | 輸出暫存器 | 12    | W   | 4         | 鋁      | 無     | Yes          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




