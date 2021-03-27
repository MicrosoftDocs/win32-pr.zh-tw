---
title: 註冊-vs_2_x
description: 本章節包含頂點著色器第2版所實之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: 35dfa3c8-be8e-4b2b-84c4-766850cf146c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6aebd9095e18abd5ac76988e46c2e061e30209c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674468"
---
# <a name="registers---vs_2_x"></a>暫存器-vs \_ 2 \_ x

本章節包含頂點著色器第2版所實之輸入和輸出暫存器的參考資訊 \_ 。

## <a name="input-registers"></a>輸入暫存器



| 註冊 | 名稱                                                                                      | Count      | R/W | \# 讀取埠 | \# 讀取/inst | 維度 | RelAddr | Defaults     | 需要 DCL |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| V\#      | [輸入暫存器](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | 無限制       | 4         | 否      | 請參閱附注1   | Yes          |
| R\#      | [暫時註冊](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 請參閱附註 2 | R/W | 3             | 無限制       | 4         | 否      | None         | No           |
| c\#      | [常數 Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | 請參閱附注3 | R   | 1             | 2               | 4         | a0/aL |  (0、0、0、0)  | No           |
| a0       | [位址註冊](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | R/W | 1             | 2               | 4         | 否      | None         | No           |
| B\#      | [常數布林值暫存器](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | 否      | FALSE        | No           |
| 我\#      | [常數整數暫存器](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | 否      |  (0、0、0、0)  | No           |
| 鋁       | [迴圈計數器暫存器](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 2               | 1         | 否      | None         | No           |
| P       | [述詞註冊](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | R/W | 1             | 1               | 4         | 否      | None         | No           |



 

注意：

1.  部分 (0、0、0、1) -如果只有一部分的通道已更新，則其餘的通道會預設為 (0、0、0、1) 。
2.  等於 D3DCAPS9。VS20Caps. NumTemps (vs \_ 2 x) 的最少12個 \_ 。
3.  等於 D3DCAPS9。Vs \_ 2 x) 的 MaxVertexShaderConst (至少為 256 \_ 。

## <a name="output-registers"></a>輸出暫存器



| 註冊 | 名稱                                                                                          | Count | R/W | 維度 | RelAddr | Defaults | 需要 DCL |
|----------|-----------------------------------------------------------------------------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | [位置註冊](dx9-graphics-reference-asm-vs-registers-position.md)                     | 1     | W   | 4         | 否      | None     | No           |
| oFog     | [霧化暫存器](dx9-graphics-reference-asm-vs-registers-fog.md)                               | 1     | W   | 1         | 否      | None     | No           |
| 選擇     | [點大小暫存器](dx9-graphics-reference-asm-vs-registers-point-size.md)                 | 1     | W   | 1         | 否      | None     | No           |
| Od\#     | [色彩註冊](dx9-graphics-reference-asm-vs-registers-color.md);請參閱附注1               | 2     | W   | 4         | 否      | None     | No           |
| oT\#     | [材質座標註冊](dx9-graphics-reference-asm-vs-registers-texture-coordinate.md) | 8     | W   | 4         | 否      | None     | No           |



 

注意：

-   oD0 是擴散色彩輸出;oD1 是反射色彩輸出。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




