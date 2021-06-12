---
title: ps_2_0
description: 瞭解 ps_2_0，這是一個可程式化的圖元著色器，由一組操作圖元資料的指令所組成。
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2433c8490af06d23d8dccef676ec206fdbb88c0
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010981"
---
# <a name="ps_2_0"></a>ps \_ 2 \_ 0

可程式化的圖元著色器是由一組操作圖元資料的指令所組成。 註冊將資料傳入和傳出 ALU。 您可以套用其他控制項來修改指令、結果，或寫出哪些資料。

-   [ps \_ 2 \_ 0 指示](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) 包含可用指令的清單。
-   [ps \_ 2 \_ 0 註冊](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) 會列出頂點著色器 ALU 所使用的不同類型的暫存器。
-   [](dx9-graphics-reference-asm-ps-registers-modifiers.md)修飾詞用來修改指令的運作方式。
-   [目的地註冊寫入遮罩](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) 會決定要寫入的目的地登錄元件。
-   [圖元著色器來源暫存器](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) 修飾詞在執行指令之前，會改變來源暫存器資料。
-   [[來源登錄 Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) ] 可讓您進一步控制要讀取、複製或寫入哪些註冊元件。

## <a name="instruction-count"></a>指令計數

著色器具有最大指令計數的限制。 指令插槽總數： 96 (64 算術和32材質) 。

## <a name="sampler-count"></a>取樣器計數

可用的紋理取樣器數目是16。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




