---
title: " elif"
description: '\ Elif 指示詞會標記由 \ ifdef、\ ifndef 或 \ if 指示詞所定義之條件式編譯區塊的選擇性子句。'
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a548cff74151dadf4a83a1e7d91ceedeafe07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021583"
---
# <a name="elif"></a>\#elif

**\# Elif** 指示詞會標記由 **\# ifdef**、 **\# ifndef** 或 **\# if** 指示詞所定義之條件式編譯區塊的選擇性子句。 指示詞會檢查指定的常數運算式，以控制資源檔的條件式編譯。 如果常數運算式為非零值， **\# elif** 會指示編譯器繼續處理語句，直到下一個 **\# endif**、 **\# else** 或 **\# elif** 指示詞，然後跳至 **\# endif** 之後的語句。 如果常數運算式為零， **\# elif** 會指示編譯器跳到下一個 **\# endif**、 **\# else** 或 **\# elif** 指示詞。 您可以在條件式區塊中使用任何數目的 **\# elif** 指示詞。

``` syntax
#elif constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*常數運算式*
</dt> <dd>

要檢查的運算式。 此值是已定義的名稱、整數常數，或由名稱、整數和算術和關聯式運算子組成的運算式。

</dd> </dl>

## <a name="example"></a>範例

在此範例中，只有當指派給名稱版本的值小於7時， **\# elif** 才會指示編譯器處理第二個 [**BITMAP**](bitmap-resource.md)語句。 只有當版本大於或等於3時，才會處理 **\# elif** 指示詞本身。

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預處理器指示詞](preprocessor-directives.md)
</dt> </dl>

 

 




