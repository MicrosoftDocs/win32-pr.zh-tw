---
title: " if"
description: '\ If 指示詞會藉由檢查指定的常數運算式來控制資源檔的條件式編譯。'
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d898d0089ab6abeefb8c11e3a781446e498ed7c0f490545189987ec4857f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599709"
---
# <a name="if"></a>\#如果

**\# If** 指示詞會藉由檢查指定的常數運算式來控制資源檔的條件式編譯。 如果常數運算式不是零，則會指示編譯器繼續處理語句，直到下一個 **\# endif**、 **\# else** 或 **\# elif** 指示詞，然後跳至 **\# endif** 指示詞之後的語句。 **\#** 如果常數運算式為零，則 **\#** 會指示編譯器跳到下一個 **\# endif**、 **\# else** 或 **\# elif** 指示詞。

``` syntax
#if constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*常數運算式*
</dt> <dd>

要檢查的運算式。 此值是已定義的名稱、整數常數，或由名稱、整數和算術和關聯式運算子組成的運算式。

</dd> </dl>

## <a name="example"></a>範例

這個範例只有在指派的值版本小於3時，才會編譯 [**BITMAP**](bitmap-resource.md) 語句：

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預處理器指示詞](preprocessor-directives.md)
</dt> </dl>

 

 




