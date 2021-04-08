---
title: " else"
description: Else 指示詞會標記由 \ ifdef、\ ifndef 或 \ if 指示詞所定義之條件式編譯區塊的選擇性子句。 Else 指示詞必須是在 \ endif 指示詞之前的最後一個指示詞。
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673475"
---
# <a name="else"></a>\#else

**\# Else** 指示詞會標示由 **\# ifdef**、 **\# ifndef** 或 **\# if** 指示詞所定義之條件式編譯區塊的選擇性子句。 **\# Else** 指示詞必須是 **\# endif** 指示詞前面的最後一個指示詞。

``` syntax
#else
```

這個指示詞沒有任何參數。

## <a name="example"></a>範例

這個範例只有在未定義 DEBUG 時，才會編譯第二個 [**BITMAP**](bitmap-resource.md) 語句：

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預處理器指示詞](preprocessor-directives.md)
</dt> </dl>

 

 




