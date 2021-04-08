---
title: Pragma 指示詞
description: RC 不支援 C/c + + 編譯器所支援的 pragma 指示詞。
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0c92136ba5e00d5b821d35ea05a337e7d6abe7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023453"
---
# <a name="pragma-directives"></a>Pragma 指示詞

RC 不支援 C/c + + 編譯器所支援的 pragma 指示詞。 不過，RC 支援下列 pragma 指示詞來變更字碼頁：

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

 ( .rc) 包含的資源檔中不支援這個 pragma。 因此，如果您有一個上層 .rc 檔案，且其中包含適用于多種語言的 .rc 檔，請在包含另一個 .rc 檔之前使用此 pragma，而不是在包含的 .rc 檔本身中使用它。 下列範例就將此進行示範。

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

如需 CodePageNum 的值清單，請參閱 [字碼頁識別碼](../intl/code-page-identifiers.md)。

 

 