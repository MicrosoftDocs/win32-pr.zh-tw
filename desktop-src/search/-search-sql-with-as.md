---
description: 資料行群組別名提供一種方式，可讓您使用較短的名稱來取代資料行或資料行群組的名稱。 選擇性群組別名述詞是 WHERE 子句的一部分。
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: WITH--AS Group Alias 述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed77072c83d1c28dcc3ec63396b46a21a57c4a97d9c6dcd70259bd861d19762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226731"
---
# <a name="with----as-group-alias-predicate"></a>WITH--AS Group Alias 述詞

資料行群組別名提供一種方式，可讓您使用較短的名稱來取代資料行或資料行群組的名稱。 選擇性群組別名述詞是 WHERE 子句的一部分。 其語法如下：


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



您可以指定一個以上的群組別名，並以 .。。做為逗號的述詞。

在 WHERE 子句述詞中參考群組別名時，此條件會套用至群組中的每個資料行。 使用邏輯 **OR** 運算子結合每個資料行所產生的邏輯值。

必須先定義別名，才能使用它，而且只能在 WHERE 子句中使用。 別名名稱必須是一般識別碼，前面加上必要的井字型大小 (\#) 。

資料行規范可包含一或多個以逗號分隔的資料行指定名稱。 資料行清單必須以括弧括住，而且可以將加權指派給每個資料行。 每個資料行都有下列語法：


```
<column_identifier> [<weight_assignment>]
```



如需指定資料行加權的詳細資訊，請參閱 [FREETEXT](-search-sql-freetext.md) 述詞和 [CONTAINS](-search-sql-contains.md)述詞。

資料行識別碼可以是一般或分隔的。

## <a name="examples"></a>範例

下列 WHERE 子句範例會示範何時以及如何使用群組別名述詞。 第一個範例顯示更重複的 WHERE 子句，而不使用群組別名。


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



您可以使用群組別名來簡化上述範例，如下列範例所示。


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



以下是正數加權的範例，其中 **Title** 屬性會在決定相對排名時獲得更多加權。


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



以下是負加權的範例，其中不會考慮權數為0的 **標題** 屬性。


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[FREETEXT 述詞](-search-sql-freetext.md)
</dt> <dt>

**概念**
</dt> <dt>

[全文檢索述詞](-search-sql-fulltextpredicates.md)
</dt> <dt>

[非全文檢索述詞](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



