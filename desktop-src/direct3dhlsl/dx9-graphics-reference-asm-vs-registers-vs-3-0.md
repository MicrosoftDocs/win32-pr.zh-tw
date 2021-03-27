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
ms.openlocfilehash: 47353a3f312a2abbd6f4fe5ea1dcd1ed9495a9d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674716"
---
# <a name="registers---vs_3_0"></a>註冊-vs \_ 3 \_ 0

本章節包含頂點著色器第3版所實之輸入和輸出暫存器的參考資訊 \_ 。

## <a name="input-registers"></a>輸入暫存器



| 註冊 | Name                                                                                      | Count      | R/W | \# 讀取埠 | \# 讀取/inst | 維度 | RelAddr | Defaults     | 需要 DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| V\#      | [輸入暫存器](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | 無限制       | 4         | a0/aL   | 請參閱附注1   | Yes          |
| R\#      | [暫時註冊](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 32         | R/W | 3             | 無限制       | 4         | 否      | None         | No           |
| c\#      | [常數 Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | 請參閱附註 2 | R   | 1             | 無限制       | 4         | a0/aL   |  (0、0、0、0)  | No           |
| a0       | [位址註冊](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W | 1             | 無限制       | 4         | 否      | None         | No           |
| B\#      | [常數布林值暫存器](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | 否      | FALSE        | No           |
| 我\#      | [常數整數暫存器](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | 否      |  (0、0、0、0)  | No           |
| 鋁       | [迴圈計數器暫存器](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 無限制       | 1         | 否      | None         | No           |
| P       | [述詞註冊](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | R/W | 1             | 1               | 4         | 不可以      | 無         | 不可以           |
| s\#      | [ (Direct3D 9 asm 的取樣器-vs) ](dx9-graphics-reference-asm-vs-registers-sampler.md)        | 4          | R   | 1             | 1               | 4         | 否      | 請參閱附注3   | Yes          |



 

注意：

1.  部分 (0、0、0、1) -如果只有一部分的通道已更新，則其餘的通道會預設為 (0、0、0、1) 。
2.  等於 D3DCAPS9。Vs \_ 3 0) 的 MaxVertexShaderConst (至少 256 \_ 。
3.  取樣器查閱的預設值存在，但值相依于材質格式。

## <a name="output-registers"></a>輸出暫存器

輸出暫存器已折迭為 12 o \# (輸出) 註冊。 這些可用於使用者想要插入圖元著色器的任何內容：材質座標、色彩、霧化等等。



| 註冊 | Name            | Count | R/W | 維度 | RelAddr | Defaults | 需要 DCL |
|----------|-----------------|-------|-----|-----------|---------|----------|--------------|
| 輸出\#      | 輸出暫存器 | 12    | W   | 4         | 鋁      | 無     | Yes          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




