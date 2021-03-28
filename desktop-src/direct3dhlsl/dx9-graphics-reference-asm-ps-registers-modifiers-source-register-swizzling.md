---
title: '來源註冊 swizzling (HLSL PS 參考) '
description: Swizzling 是指將任何來源暫存器元件複製到任何暫存登錄元件的能力。 Swizzling 不會影響來源註冊資料。 在執行指令之前，會將來源暫存器中的資料複製到臨時暫存器。
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313791"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a>來源註冊 swizzling (HLSL PS 參考) 

Swizzling 是指將任何來源暫存器元件複製到任何暫存登錄元件的能力。 Swizzling 不會影響來源註冊資料。 在執行指令之前，會將來源暫存器中的資料複製到臨時暫存器。

## <a name="source-swizzling"></a>來源 Swizzling

來源 swizzle 可讓來源暫存器的個別元件採用相同來源暫存器中任何四個元件的值，然後再讀取註冊來進行計算。

例如，zxxy swizzle 表示：

-   . x 元件會取得. z 元件的值
-   . y 元件會取得. x 元件的值
-   . z 元件會取得. x 元件的值
-   。 w 元件會採用. y 元件的值

元件可以依任何順序顯示。 如果指定的元件少於四個，則會重複最後一個元件。 例如：


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



如果未指定任何元件，則不會套用任何 swizzling。

某些指示對於來源 swizzle 有一些限制。 它們列在 [遵守的指令參考] 頁面中。



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2個 \_ sw | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| .x                    |      |      |      | x    | x    | x    | x     | x    | x     |
| . y                    |      |      |      | x    | x    | x    | x     | x    | x     |
| . z                    | X\*  | X\*  | x\*  | x    | x    | x    | x     | x    | x     |
| w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| xyzw (預設)        | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .yzxw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .zxyw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .wzyx                 |      |      |      |      | x    | x    | x     | x    | x     |
| 任意 swizzle     |      |      |      |      |      | x    | x     | x    | x     |



 

\* 只有當目的地寫入遮罩是. w ( 時，才可使用。) 。

## <a name="arbitrary-swizzle"></a>任意 Swizzle

Swizzles 可依任意順序套用至來源暫存器;也就是說，任何來源暫存器都可以採用任何順序的元件遮罩。

## <a name="replicate-swizzle"></a>複寫 Swizzle

複寫 swizzle 會將一個元件複製到另一個元件。 這就是其中一個. x、. y、z、w swizzle 元件 (或 r、g.、b.。必須指定對應的) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖元著色器來源登錄修飾詞](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 註冊](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[ps \_ 2 \_ 0 註冊](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[ps \_ 2 \_ x 註冊](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[ps \_ 3 \_ 0 註冊](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




