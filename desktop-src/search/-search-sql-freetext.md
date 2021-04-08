---
description: FREETEXT 述詞是 WHERE 子句的一部分，而且支援在文字資料行中搜尋單字和片語。
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: FREETEXT 述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc78be4d5ac75f892c82c6dad390e4583876856f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689871"
---
# <a name="freetext-predicate"></a>FREETEXT 述詞

FREETEXT 述詞是 [WHERE](-search-sql-where.md) 子句的一部分，而且支援在文字資料行中搜尋單字和片語。 使用 FREETEXT 述詞來尋找檔，其中包含在指定的內容或資料行中散佈之搜尋文字的組合。 若要取得等級值，請將相關的排名視為 SELECT 語句中的資料行。

FREETEXT 述詞具有下列語法：


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



全文檢索資料行參考是選擇性的。 您可以使用它來指定單一資料行，或針對 FREETEXT 述詞進行測試的資料 [行群組別名](-search-sql-with-as.md) 。 當全文檢索資料行指定為 "ALL" 或 " \* " 時，就會搜尋所有已編制索引的 text 屬性。 雖然資料行不需要是文字屬性，但如果資料行是其他資料類型，則結果可能沒有意義。 資料行名稱可以是一般或分隔的 [識別碼](-search-sql-identifiers.md)，而且您必須將它與條件分隔（以逗號分隔）。 如果未提供任何全文檢索條件，則會使用 [內容] 資料行，也就是檔的主體。

您可以指定搜尋地區設定，以識別搜尋查詢的適當斷詞工具和字形變化表單。 有效的地區設定值是 (LCID) 的 Windows standard 語言代碼識別碼。 例如，1033是美國的 LCID （英文）。 將 LCID 放在 FREETEXT 子句括弧內的最後一個專案。 如需搜尋和語言的重要資訊，請參閱 [使用當地語系化的搜尋](-search-sql-usinglocsearches.md)。

> [!Note]  
> 預設搜尋地區設定是系統預設的地區設定。

 

您必須將 freetext 條件部分以單引號括住，而且必須由一或多個搜尋詞彙組成。 FREETEXT 述詞不支援邏輯運算。 若要搜尋片語，就像是單一單字一樣，請用雙引號括住該片語。

當您使用 FREETEXT 述詞時，搜尋查詢結果會傳回包含所有搜尋字詞的檔。 這些條款不需要以任何特定順序顯示。 包含更多搜尋詞彙的檔具有較高等級的資料行值。

## <a name="examples"></a>範例

下列範例會搜尋包含「電腦」、「軟體」、「硬體」或這些字組組合的檔：


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> 您無法在相同的 FREETEXT 述詞中同時使用單字相符和片語比對。

 

使用縮寫執行查詢時，您必須在使用 FREETEXT 時，在縮減中將引號換用，但在使用 CONTAINS 時則否。

例如，下列語法會失敗：


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



正確的語法包括兩個單引號，而不是雙引號。

下列語法會成功：


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[CONTAINS 述詞](-search-sql-contains.md)
</dt> <dt>

[WHERE 子句](-search-sql-where.md)
</dt> <dt>

**概念**
</dt> <dt>

[非全文檢索述詞](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



