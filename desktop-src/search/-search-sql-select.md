---
description: 以下顯示本機查詢之 SELECT 語句的基本語法：
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: SELECT 陳述式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df8cc5f4b6bab673d20c981e44386d3fdbd651b5a2753d8c965ee55023a6562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227193"
---
# <a name="select-statement"></a>SELECT 陳述式

以下顯示本機查詢之 SELECT 語句的基本語法：


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



以下顯示 SELECT 語句語法的資料行部分：


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



 (s) 的資料行規范必須是有效的屬性名稱資料行，並以逗號分隔。 有效的資料行名稱是已註冊的屬性描述，或是由 Shell 的屬性系統架構定義。 您只能選取在屬性系統架構中標示為可抓取的資料行。 如果您使用混合大小寫來識別不是系統定義屬性的屬性，則必須將資料行規范括在雙引號中。 系統定義的屬性名稱包括以 "System" 開頭的所有屬性 (例如，) ，而且不需要引號。

> [!Note]  
> 您也可以用雙引號括住系統定義的屬性名稱，以方便閱讀。 這不會影響相容性。

 

當查詢傳回的檔沒有所要求的資料行時，該檔的該資料行值就是 **Null**。

您必須在 SELECT 語句中至少提供一個資料行名稱。 在 [結構化查詢語言 (SQL)  (SQL) 查詢] 中，您可以使用星號 (\*) 來指定要傳回資料表中的所有資料行。 不過，沒有任何已定義且固定的屬性集會套用至所有檔。 基於這個理由，SELECT 語句的規範中不允許 SQL 星號 <columns> 。

## <a name="getting-the-top-n-results"></a>取得前 n 個結果

您可以使用 TOP 語法來指定要傳回的結果數目上限：


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a>轉換資料行資料類型

有時，您可能需要將從檔中解壓縮的字串資料轉換成另一種資料類型，才能進行適當的比較。 如需詳細資訊，請參閱 [轉換資料行的資料類型](-search-sql-castingdatacolumntype.md)。

## <a name="examples"></a>範例

下列範例會傳回相符檔的名稱和 URL。


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[轉換資料行的資料類型](-search-sql-castingdatacolumntype.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[系統屬性](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 



