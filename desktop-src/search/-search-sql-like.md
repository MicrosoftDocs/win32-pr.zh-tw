---
description: LIKE 述詞會針對指定的資料行執行模式比對比較。
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: LIKE 述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970144"
---
# <a name="like-predicate"></a>LIKE 述詞

LIKE 述詞會針對指定的資料行執行模式比對比較。 其使用下列語法：


```
...WHERE <column> LIKE '<wildcard_literal>'
```



<column>可以是一般或分隔的[識別碼](-search-sql-identifiers.md)。 此資料行受限於屬性存放區中的屬性。

<萬用字元 \_ 常值> 是字串常值。 它會以引號括住，並且可以選擇性地包含萬用字元。 如有需要，相符字串可以包含多個萬用字元。 下表描述 LIKE 述詞可辨識的萬用字元。



| 萬用字元                | 描述                                                                                                                                                                                     | 範例                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| % (百分比)              | 符合零或多個字元。                                                                                                                                                         | ' comp% r ' 符合 ' comp '，後面接著零或多個字元，以 r 結尾。                                                                                                                                  |
| \_ (底線)          | 符合任何單一字元。                                                                                                                                                                   | ' comp \_ 終端 ' 會比對 ' comp '，後面接著剛好一個字元，後面接著 ' 終端 '。                                                                                                                              |
| \[\] (方括弧)  | 符合指定範圍或集合內的任何單一字元。 例如， \[ -z \] 指定範圍; \[aeiou \] 指定一組母音。                                                  | ' comp \[ a-z \] re ' 會比對 ' comp '，後面接著範圍 a 至 z 的單一字元，後面接著是 '。 ' comp \[ ao \] ' 符合 ' comp '，後面接著一個必須是或 o 的單一字元。<br/> |
| \[^ \] (插入號)           | 符合不在指定範圍或集合內的任何單一字元。 例如， \[ ^ a-z \] 會指定排除 a 到 z 的範圍; \[^ aeiou \] 指定排除母音的集合。 | ' comp \[ ^ u \] ' 符合 ' comp '，後面接著任何不是 u 的單一字元。                                                                                                                                        |



 

如果您建立具有多個範圍的述詞，則範圍必須是順序。

> [!Note]  
> 若要比對萬用字元做為比對的常值字元，而不是萬用字元，請將字元放在方括弧內。 例如，若要與百分比符號相符，請使用 ' \[ % \] '

 

## <a name="examples"></a>範例


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[常值比較](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[多重值 (陣列) 比較](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[Null 述詞](-search-sql-null.md)
</dt> <dt>

**概念**
</dt> <dt>

[全文檢索述詞](-search-sql-fulltextpredicates.md)
</dt> <dt>

[非全文檢索述詞](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




