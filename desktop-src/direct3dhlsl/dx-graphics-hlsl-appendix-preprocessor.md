---
title: '預處理器指示詞 (HLSL) '
description: 預處理器指示詞（例如 \ 定義和 \ ifdef）通常用來讓來來源程式在不同的執行環境中變得更容易變更和編譯。
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8efdd996ddeb58c09d1c8250f174c21bb939f082
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386827"
---
# <a name="preprocessor-directives-hlsl"></a>預處理器指示詞 (HLSL) 

預處理器指示詞（例如[ \# define](dx-graphics-hlsl-appendix-pre-define.md)和[ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)）通常用來讓來來源程式在不同的執行環境中變得更容易變更和編譯。 原始程式檔中的指示詞會指示前置處理器執行特定動作。 例如，前置處理器可以取代文字中的語彙基元、將其他檔案的內容插入原始程式檔，或是透過移除文字區段來隱藏編譯檔案的一部分。 在巨集展開之前，會辨識並執行前置處理器程式行。 因此，如果巨集展開成類似前置處理器命令的程式碼，前置處理器就無法辨識該命令。

除了不支援逸出序列以外，前置處理器陳述式使用的字元集與原始程式檔陳述式使用的相同。 前置處理器陳述式中使用的字元集與執行字元集相同。 前置處理器也會辨識負數字元值。

HLSL 預處理器會辨識下列指示詞：

-   [\#定義](dx-graphics-hlsl-appendix-pre-define.md)
-   [\#elif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#else](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#endif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#錯誤](dx-graphics-hlsl-appendix-pre-error.md)
-   [\#如果](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#ifndef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#包括](dx-graphics-hlsl-appendix-pre-include.md)
-   [\#線](dx-graphics-hlsl-appendix-pre-line.md)
-   [\#pragma](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [\#undef](dx-graphics-hlsl-appendix-pre-undef.md)

數位記號 (\#) 必須是包含指示詞的行上的第一個非空白字元空白字元; 在數位記號與指示詞的第一個字母之間可以出現空白字元。 某些指示詞會包含引數或值。 指示詞後面的任何文字 (除了屬於指示詞一部分的引數或值以外，) 前面必須加上單行批註分隔符號 (//) 或以批註分隔符號括住 (/ \* \* /) 。 包含預處理器指示詞的行，可以透過反斜線 () 來繼續 \\ 。

前置處理器指示詞可以出現在原始程式檔的任何位置，但是這只會套用至原始程式檔的其餘部分。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[附錄 (DirectX HLSL) ](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




