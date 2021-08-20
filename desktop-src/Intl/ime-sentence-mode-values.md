---
description: 查看輸入法編輯器 (IME) 句子模式值的清單。 這些值會搭配 ImmGetConversionStatus 和 ImmSetConversionStatus 函數使用。
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: IME 句子模式值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c471282ebf50657b45f7c1c22938b27fff5a62c08c48ab4191dd84048a4b6b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146127"
---
# <a name="ime-sentence-mode-values"></a>IME 句子模式值

這些值會搭配 [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) 和 [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) 函數使用。



| 常數                  | 定義                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| 自動輸入法 \_ SMODE \_     | IME 會在自動模式中執行轉換處理。               |
| IME \_ SMODE \_ 無          | 沒有句子的資訊。                                               |
| IME \_ SMODE \_ PHRASEPREDICT | IME 會使用片語資訊來預測下一個字元。             |
| IME \_ SMODE \_ PLURALCLAUSE  | IME 使用複數子句資訊來執行轉換處理。 |
| IME \_ SMODE \_ SINGLECONVERT | IME 會以單一字元模式執行轉換處理。        |
| IME \_ SMODE \_ 對話  | IME 使用交談模式。 這對聊天應用程式很有用。      |



 

Bits 16 到31會保留給 IME 使用。

 

 



