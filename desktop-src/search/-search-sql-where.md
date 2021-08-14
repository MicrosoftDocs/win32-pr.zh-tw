---
description: 判斷檔是否包含在查詢所傳回之結果中的條件是由 WHERE 子句所指定。
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: 'WHERE 子句 (Windows Search) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e711219ff8eea81e8c4f8fd8145baccc35f49389d412f0e4ac088aa06666643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462400"
---
# <a name="where-clause-windows-search"></a>WHERE 子句 (Windows Search) 

判斷檔是否包含在查詢所傳回之結果中的條件是由 WHERE 子句所指定。 在最高層級，WHERE 子句語法有兩個部分：


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



選擇性的 <群組 \_ 別名> 部分子句會將別名指派給一或多個資料行的群組，以簡化複雜的查詢。 這可以改善在 Url 指定的多個資料行中搜尋相同資訊的複雜查詢可讀性。 如需群組別名的詳細資訊，請參閱 [WITH--AS Group Alias 述](-search-sql-with-as.md)詞。

<search condition>WHERE 子句的部分是一或多個搜尋述詞，可指定搜尋的相符準則。 搜尋述詞是判斷某個值某些事實的運算式。

搜尋條件的結果為布林值，如果檔符合指定的搜尋條件， **則為 TRUE** ; 如果不符合指定的搜尋條件，則為 **FALSE** 。 如果結果為 **TRUE**，則會傳回檔。 如果結果為 **FALSE**，則不會傳回檔。 Microsoft Windows Search 查詢中所傳回的檔，會根據符合搜尋條件的程度，指派等級值。 每個查詢搜尋條件都可以包含 [RANKBY](-search-sql-rankby.md) 子句，以支援修改傳回的排名值。

[ReuseWhere](-search-sql-reusewhere.md)函式會讓多個使用相同搜尋條件的查詢更有效率。 查詢中的 WHERE 子句會指定在查詢中相符的專案集合。 後續的查詢可以在新的查詢 WHERE 子句中使用 ReuseWhere 函數，以共用針對先前 evalution 執行的工作。

## <a name="search-predicates"></a>搜尋述詞

搜尋條件是由一或多個述詞或搜尋條件所組成，可描述使用者搜尋的內容 (例如，DateCreated > ' 2006-04-19 ' ) 。 您可以使用邏輯運算子 **AND**、 **or** 或 **NOT** 來合併搜尋述詞。 選擇性的一元運算子 **不** 可以搭配 **和** 使用，而且只能用來否定述詞或搜尋條件的邏輯值。 您可以使用括弧來分組及嵌套邏輯詞彙。

下表顯示邏輯運算子的優先順序順序。



| 順序 (優先順序)  | 邏輯運算子 |
|--------------------|------------------|
| 第一個 (最高)     | **NOT**          |
| Second             | **AND**          |
| 第三 (最低)      | **OR**           |



 

相同類型的邏輯運算子是關聯性，而且沒有指定的計算順序。 例如， (A **和** B) **，而且** (C **和** d) 可以計算 (A **和** d) **，** (B **和** C) ，但邏輯結果不會有任何變更。

> [!IMPORTANT]
>
> 不正確：其中 **不** 包含 ( ' computer ' ) 
>
> 正確：其中包含 ( ' software ' ) **且不** 包含 ( ' computer ' ) 

 

在複雜的查詢中，您可能會想要特別強調某些資料行中比其他資料行的相符專案。 例如，在搜尋討論「軟體設計」的檔時，尋找檔標題中的搜尋詞彙比在檔的文字中尋找個別單字更可能是很好的相符專案。 若要以這種方式影響檔的排名，Microsoft Windows Search 查詢語言支援搜尋條件的加權。 如需資料行加權的詳細資訊，請參閱 [CONTAINS](-search-sql-contains.md) 述詞和 [FREETEXT](-search-sql-freetext.md)述詞。

Windows Search 中有三個搜尋述詞群組：全文檢索、非全文檢索和資料夾深度搜尋。 全文檢索搜尋述詞通常符合內容、標題和其他資料行的意義，並支援語言比對 (例如，替代字組表單、片語和鄰近搜尋) 。 相反地，非全文檢索搜尋述詞會比對指定資料行的值，但不包含任何特殊的語言處理，但在許多情況下，會提供以字元為基礎的模式比對。 資料夾深度述詞會將搜尋範圍限制為指定的路徑。

> [!Note]  
> 如果查詢傳回檔，因為該檔的非全文檢索述詞評估為 **TRUE** ，則 rank 值會計算為1000。 使用 [rank 強制函數](-search-sql-rankby.md) 可以修改 rank 值。

 

下表說明全文檢索、非全文檢索和資料夾深度搜尋述詞。



| 全文檢索述詞                  | 描述                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CONTAINS](-search-sql-contains.md) | 支援檔文字資料行中詞彙的複雜搜尋 (例如，標題、內容) 。 可以搜尋搜尋詞彙的屈折變化形式、測試字詞的相近度，以及執行邏輯比較。 搜尋詞彙可以包含萬用字元。 |
| [FREETEXT](-search-sql-freetext.md) | 搜尋符合搜尋片語意義的檔。 相關的單字和類似的片語會相符，並根據檔與搜尋片語的緊密程度計算出排名資料行。 搜尋字詞不能包含萬用字元。  |



 



| 非全文檢索述詞                                                    | Description                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LIKE](-search-sql-like.md)                                               | 資料行值會使用簡單的模式比對與萬用字元進行比較。                                                                                                    |
| [常值比較](-search-sql-literalvaluecomparison.md)         | 資料行值會與字串、日期、時間戳記、數值和其他常值進行比較。 這個述詞支援相等和到差異，例如大於和小於。 |
| [多重值 (陣列) 比較](-search-sql-multivaluedcomparisons.md) | 多值資料行會與常值陣列的常值進行比較。                                                                                                             |
| [NULL](-search-sql-null.md)                                               | 您可以使用 **Null** 述詞來偵測為檔定義的資料行值。                                                                                    |



 



| 資料夾深度                             | Description                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [範圍](-search-sql-folderdepth.md)     | 執行指定路徑的深度遍歷，包括特定資料夾和所有子資料夾。 |
| [目錄](-search-sql-folderdepth.md) | 執行指定路徑的淺層遍歷，只搜尋特定資料夾。            |



 

## <a name="examples"></a>範例

如需 WHERE 子句的範例，請參閱上表中連結的個別述詞主題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[ReuseWhere 函式](-search-sql-reusewhere.md)
</dt> <dt>

[資料列集屬性](-search-sql-rowset-properties.md)
</dt> <dt>

[FROM 子句](-search-sql-from.md)
</dt> <dt>

[搜尋 SQL 語法的總覽](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[WITH--AS Group Alias 述詞](-search-sql-with-as.md)
</dt> <dt>

[範圍和目錄述詞](-search-sql-folderdepth.md)
</dt> <dt>

[RANK BY 子句](-search-sql-rankby.md)
</dt> <dt>

**概念**
</dt> <dt>

[全文檢索述詞](-search-sql-fulltextpredicates.md)
</dt> <dt>

[非全文檢索述詞](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



