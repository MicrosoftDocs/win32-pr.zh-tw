---
title: 註冊-vs_1_1
description: 本章節包含頂點著色器第1版所實之輸入和輸出暫存器的參考資訊 \_ 。
ms.assetid: 8b19a0da-1561-450f-a36a-35ac7ea6e17a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4bcfadae2b1dca70298ffed188de2e6075892563b27bf6f624f2139e441600cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908002"
---
# <a name="registers---vs_1_1"></a>註冊-vs \_ 1 \_ 1

本章節包含頂點著色器第1版所實之輸入和輸出暫存器的參考資訊 \_ 。

## <a name="input-registers"></a>輸入暫存器



| 註冊 | 名稱                                                                                  | 計數      | R/W | \# 讀取埠 | \# 讀取/inst | 尺寸  | RelAddr | Defaults     | 需要 DCL |
|----------|---------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|------------|---------|--------------|--------------|
| a0       | [位址註冊](dx9-graphics-reference-asm-vs-registers-address.md)               | 1          | R/W | 1             | 無限制       | 請參閱附注3 | 否      | 無         | No           |
| c\#      | [常數 Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md) | 請參閱附註 2 | R   | 1             | 無限制       | 4          | a0. x    |  (0、0、0、0)  | No           |
| V\#      | [輸入暫存器](dx9-graphics-reference-asm-vs-registers-input.md)                   | 16         | R   | 1             | 無限制       | 4          | 否      | 請參閱附注1   | Yes          |
| R\#      | [暫時註冊](dx9-graphics-reference-asm-vs-registers-temporary.md)           | 12         | R/W | 3             | 無限制       | 4          | 否      | 無         | No           |



 

注意：

1.  部分 (0、0、0、1) -如果只有一部分的通道已更新，則其餘的通道會預設為 (0、0、0、1) 。
2.  等於 D3DCAPS9。Vs \_ 1 1) 的 MaxVertexShaderConst (至少 96 \_ 。
3.  只有. x 通道可供使用。

## <a name="output-registers"></a>輸出暫存器



| 註冊 | 名稱                        | 計數 | R/W | 尺寸 | RelAddr | Defaults | 需要 DCL |
|----------|-----------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | 位置註冊           | 1     | W   | 4         | 否      | 無     | No           |
| oFog     | 霧化暫存器                | 1     | W   | 1         | 否      | 無     | No           |
| 選擇     | 點大小暫存器         | 1     | W   | 1         | 否      | 無     | No           |
| Od\#     | 色彩註冊;請參閱附注1  | 2     | W   | 4         | 否      | 無     | No           |
| oT\#     | 材質座標註冊 | 8     | W   | 4         | 否      | 無     | No           |



 

注意：

-   oD0 是擴散色彩輸出;oD1 是反射色彩輸出。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




