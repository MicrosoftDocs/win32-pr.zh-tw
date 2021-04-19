---
title: " ifndef"
description: '\ Ifndef 指示詞會檢查指定的名稱，以控制資源檔的條件式編譯。'
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984a969123ea68fd68b14c1b98354b8bc5205aba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967822"
---
# <a name="ifndef"></a>\#ifndef

**\# Ifndef** 指示詞會檢查指定的名稱，以控制資源檔的條件式編譯。 如果未定義名稱，或已使用 **\# undef** 指示詞移除其定義， **\# ifndef** 會指示編譯器繼續處理語句，直到下一個 **\# endif**、 **\# else** 或 **\# elif** 指示詞，然後跳至 **\# endif** 指示詞之後的語句。 如果定義的名稱， **\# ifndef** 會指示編譯器跳到下一個 **\# endif**、 **\# else** 或 **\# elif** 指示詞。

``` syntax
#ifndef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*名字*
</dt> <dd>

指示詞要檢查的名稱。

</dd> </dl>

## <a name="example"></a>範例

這個範例只有在未定義 Optimize 時，才會編譯 [**BITMAP**](bitmap-resource.md) 語句：

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預處理器指示詞](preprocessor-directives.md)
</dt> </dl>

 

 




