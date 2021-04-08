---
description: CONTAINS 述詞支援使用星號 (\*) 作為萬用字元，以代表單字和片語。 您只能在單字或片語的結尾加上星號。 星號是否存在會啟用前置比對模式。
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: 在 CONTAINS 述詞中使用萬用字元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013e49f97cf23c7a00aca7bb287edd19951520f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112409"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a>在 CONTAINS 述詞中使用萬用字元

CONTAINS 述詞支援使用星號 (\*) 作為萬用字元，以代表單字和片語。 您只能在單字或片語的結尾加上星號。 星號是否存在會啟用前置比對模式。 在此模式中，如果資料行包含指定的搜尋字，後面接著零或多個其他字元，則會傳回相符專案。 如果提供了片語，則如果資料行包含所有指定的單字，且該單字後面有零或多個其他字元，則會偵測到相符專案。

## <a name="examples"></a>範例

第一個範例會比對檔案名欄中具有任何單字（開頭為 "serv"）的檔。 符合字組範例包括 "server"、"servers" 和 "service"。


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



第二個範例會比對檔中 FileName 資料行中的任何片語（開頭為 "comp"），並在下一個單字開頭為 "serv"。 符合字組範例包括「複合伺服器」、「複合伺服器」和「複合服務」。


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



星號只適用于前置詞比對，而且只能放在單字或片語的結尾。它不適用於尾碼比對。 下列語法無效，而且不符合檔案名資料行中任何單字結尾為 "服務" 的檔。


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[FREETEXT 述詞](-search-sql-freetext.md)
</dt> <dt>

[WHERE 子句](-search-sql-where.md)
</dt> </dl>

 

 



