---
description: 查詢的結果包含查詢所傳回的資料列，以及每個資料列的次序值（如果 SELECT 子句中包含 rank 資料行的話）。
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: RANK BY 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33daf4865b0f7f08689802822d8c0d5b4d38702a1cb1f813563564e001811a6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462437"
---
# <a name="rank-by-clause"></a>RANK BY 子句

查詢的結果包含查詢所傳回的資料列，以及每個資料列的次序值（如果 SELECT 子句中包含 rank 資料行的話）。 排名值是由搜尋引擎計算，並傳回為0到1000範圍內的整數。 為了讓排名結果更有意義，查詢可以控制如何在 RANK BY 子句中計算原始排名值。

本主題的組織方式如下：

-   [RANK BY 子句](#rank-by-clause)
-   [權數函數](#weight-function)
-   [強制函式](#coercion-function)

## <a name="rank-by-clause"></a>RANK BY 子句

RANK BY 子句的語法如下所示：


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



RANK BY 子句會套用至 \_ 緊接在其前面的搜尋條件，有效地為該搜尋條件所傳回的資料列指定較低或更高的排名，而不是另一個搜尋條件所傳回的資料列。 搜尋條件周圍的括弧 \_ 是必要的。 排名規格周圍的括弧是選擇性的。

單一條件可以套用一個以上的 RANK BY 子句。 您可以使用括弧將其他順位 BY 子句加入至另一個。

> [!Note]  
> 全文檢索述詞會傳回範圍0到1000的排名值。 非全文檢索述詞所比對之所有檔的等級值為1000。 對排名值的修改應將此資訊納入考慮。

 

\_RANKBY 子句的排名規格部分會識別要套用至排名值的一或多個函數。 權數函數會針對傳回的資料列，將乘數套用至原始排名值。 乘數越小，所產生的排名值就越低。 強制函式可以用來將傳回的資料列相乘、加入或設定特定的等級值。 每個排名規格都可以包含零個或一個加權函數，以及零或多個強制函式。 如果加權和強制函式都包含在 RANK BY 子句中，加權函數必須是 first。

## <a name="weight-function"></a>權數函數

權數函數的語法為：


```
WEIGHT ( <weight_multipler> ) 
```



乘數必須是從0.001 到1.000 的十進位數。 搜尋條件述詞所傳回的原始排名值會乘以加權乘數來設定新的排名值。

在下列範例中，權數函數會在 System.Doc>ument 中提供 "Theresa" 一字的檔。LastAuthor 欄位在 [Author] 欄位中有 "Theresa" 的檔排名值一半：


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> CONTAINS 和 FREETEXT 述詞資料行加權功能支援使用在搜尋詞彙和乘數 ( "software"： 0.25) 之間的冒號格式的速記格式。 RANK BY 子句不支援縮寫形式。

 

使用依權數的等級時有限制：它無法搭配使用布林值條件的 CONTAINS 子句使用;例如，不允許下列範例：


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a>強制函式

Rank 強制函式可以用來變更傳回的等級值（藉由加法或乘法），或指派特定值給它。

強制函式的語法為：


```
COERCION ( <coercion_operation> , <coercion_value> )
```



強制值是整數值。

下表描述可用的強制操作設定。



| 強制操作 | Description                                                                                    | 數值範圍  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| ABSOLUTE           | 傳回的排名值是在強制值中指定的值。                          | 0到1000    |
| ADD                | 傳回的排名值是原始排名值和指定強制值的總和。     | 0.001 至1。0 |
| MULTIPLY           | 傳回的排名值是原始排名值和指定強制值的乘積。 | 0.001 至1。0 |



 

 

> [!IMPORTANT]
> 搜尋只能傳回0到1000範圍內的等級值。

 

 

下列範例會使用強制函式，將標題中有 "computer" 的所有檔設定為1000的順位，同時減少標題中包含 "computer" 和 "software" 的檔排名一季。


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



