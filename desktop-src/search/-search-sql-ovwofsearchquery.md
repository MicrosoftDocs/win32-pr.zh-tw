---
description: Windows Search 結構化查詢語言 (SQL)  (SQL) 類似于標準的 SQL 查詢。
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: SQL 語法 Windows Search 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff6a755312e4358dc2eaa9ea7ae97f22ef783f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026117"
---
# <a name="overview-of-windows-search-sql-syntax"></a>SQL 語法 Windows Search 總覽

Windows Search 結構化查詢語言 (SQL)  (SQL) 類似于標準的 SQL 查詢。 它會顯示在下列兩個語法中：


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

在下列查詢範例中，會針對擁有50個以上頁面的所有檔傳回頁面計數和日期的值，並以頁面計數的遞增順序排序。

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

Windows Search 查詢語法支援許多選項，可啟用更複雜的查詢。

下表描述 SELECT 或 GROUP ON 語句中的每個子句，以及支援的功能。

| 子句                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [分組依據 .。。OVER .。。](-search-sql-group-on-over.md) | 指定如何將查詢所傳回的結果群組。 您可以指定要用來分組的範圍，並指定一個以上的資料行進行分組。 例如，您可以將檔案大小範圍的結果群組 (大小 < 100、100 <= 大小 < 1000;1000 <= 大小) 和嵌套群組。                                                                                                       |
| [SELECT](-search-sql-select.md)                    | 指定查詢所傳回的資料行。                                                                                                                                                                                                                                                                                                                                                         |
| [FROM](-search-sql-from.md)                        | 指定要搜尋的電腦和目錄。                                                                                                                                                                                                                                                                                                                                                         |
| [WHERE](-search-sql-where.md)                      | 指定構成相符檔的內容。 這個子句有許多選項，可以讓您在搜尋條件中提供豐富的控制權。 例如，您可以比對單字、片語、字形變化 word 表單、字串、數值和位值，以及多重值陣列。 您也可以將統計權數套用至比對條件，並結合符合條件與布林運算子。 |
| [ORDER BY](-search-sql-orderby.md)                 | 指定查詢所傳回之結果的排序次序。 您可以指定一個以上的欄位來排序結果，而且可以使用遞增或遞減順序。                                                                                                                                                                                                               |

### <a name="code-samples"></a>程式碼範例

WSSQL 程式碼範例會示範如何透過 SQL 在 Microsoft OLE DB 和 Windows Search 之間進行通訊。 WSOleDB 程式碼範例說明 Active Template Library (ATL) OLE DB Windows Search 應用程式的存取權，以及兩種從 Windows Search 抓取結果的額外方法。 這兩個範例都可在 [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)上取得。

## <a name="related-topics"></a>相關主題

### <a name="reference"></a>參考

[常值](-search-sql-literals.md)

[使用當地語系化的搜尋](-search-sql-usinglocsearches.md)

[瞭解相關性值](-search-sql-understandingrelevancevalues.md)

[屬性對應](-search-3x-wds-propertymappings.md)

[進階查詢語法](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a>概念

[Microsoft Windows Search 中的 SQL 擴充功能](-search-sql-extensions-sps.md)

[Microsoft Windows Search 中無法使用 SQL 功能](-search-sql-featuresunavailableinspssearch.md)

[識別碼](-search-sql-identifiers.md)

[搜尋中的區分大小寫](-search-sql-casesensitivityinsearches.md)

[搜尋中的變音符號敏感度](-search-sql-accentinsensitivitysearches.md)

[轉換資料行的資料類型](-search-sql-castingdatacolumntype.md)

[資料類型對應](-search-sql-datatypemappings.md)
