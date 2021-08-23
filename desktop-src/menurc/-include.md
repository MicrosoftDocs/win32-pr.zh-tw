---
title: " include"
description: '\ Include 指示詞會導致資源編譯器處理 filename 參數中所指定的檔案。'
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bf5d6fa40e45073ca7ccb5f97dd3ddb0d13dfdfced965d5c83332183da421e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599717"
---
# <a name="-include"></a>包含

**\# Include** 指示詞會導致資源編譯器處理 *filename* 參數中所指定的檔案。 這個檔案應該是定義資源定義檔中所使用之常數的標頭檔。 檔案可以使用單一位元組、雙位元組或 Unicode 字元。

``` syntax
#include filename
```

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*檔案名*
</dt> <dd>

要包含的檔案名。 如果檔案在目前的目錄中，則字串必須用雙引號括住;如果檔案位於 INCLUDE 環境變數所指定的目錄中，則字串必須包含在 (<>) 的小於字元和大於字元。 如果檔案不在目前的目錄或 INCLUDE 環境變數所指定的目錄中，您必須提供以雙引號括住的完整路徑 ( ") 。

</dd> </dl>

## <a name="remarks"></a>備註

在標頭檔中使用下列語句，以圍住可由 C 編譯器編譯但不能由 RC 編譯的語句：

``` syntax
#ifndef RC_INVOKED
```

如此一來，您就可以在 .c 和 .rc 檔案中使用相同的 include 檔。

## <a name="example"></a>範例

此範例會在編譯資源定義檔時，處理 Windows .h 和 MyDefs 的標頭檔：

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預處理器指示詞](preprocessor-directives.md)
</dt> </dl>

 

 




