---
title: vs_2_0
description: 可程式化頂點著色器是由一組在頂點資料上操作的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce4e986e610ff95716cd6899d6167e4f69efe042
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971445"
---
# <a name="vs_2_0"></a>vs \_ 2 \_ 0

可程式化頂點著色器是由一組在頂點資料上操作的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。

-   [指示-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) 包含可用指令的清單。
-   暫存器[-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md)會列出頂點著色器 ALU 所使用的不同類型的暫存器。
-   [頂點著色器](dx9-graphics-reference-asm-vs-registers-modifiers.md) 暫存器修飾詞可用來修改指令的運作方式。
-   [頂點著色器來源](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) 暫存器修飾詞在執行指令之前，會改變來源暫存器資料。
-   [[來源登錄 Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) ] 可讓您進一步控制要讀取、複製或寫入哪些註冊元件。
-   [目的地註冊遮罩](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) 會決定要寫入的目的地登錄元件。

## <a name="instruction-count"></a>指令計數

每個頂點著色器最多可以儲存256指令。 執行的指令數目可能會更高 (因為迴圈/代表支援) ，且受 D3DCAPS9 限制。MaxVShaderInstructionsExecuted，至少應該是0xFFFF。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




