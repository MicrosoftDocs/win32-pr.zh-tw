---
description: 常值比較會使用標準比較運算子來比對單一值資料行與常值。
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: 常值比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1e311c6f98c1114b63a1bf650d6e7be004e1e8e4cf5848b962a7cbf8049bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227173"
---
# <a name="literal-value-comparison"></a>常值比較

常值比較會使用標準比較運算子來比對單一值資料行與 [常](-search-sql-literals.md) 值。 如需有關比較多值資料行的詳細資訊，請參閱 [多重值 (陣列) 比較](-search-sql-multivaluedcomparisons.md)。

常值比較述詞具有下列語法：


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> 比較的右側必須是常值。 您無法將資料行與計算的值相比較，也無法將資料行與另一個資料行進行比較。

 

資料行部分是任何有效的屬性資料行，如有必要，可以轉換成另一種類型。 （選擇性）您可以用雙引號括住資料行名稱，以利可讀性，而不會影響功能。 如需詳細資訊，請參閱 [轉換資料行的資料類型](-search-sql-castingdatacolumntype.md)。

常值可以是任何字串、數值、十六進位、布林值或日期常值（以單引號括住）。 只會辨識完全相符的專案，而且會忽略萬用字元。 常值也可以轉換成另一種類型。

## <a name="comparison-operators"></a>比較運算子

下表描述支援的比較運算子。



| 比較運算子 | 描述              |
|---------------------|--------------------------|
| =                   | 等於                 |
| ！ = 或 <>      | 不等於             |
| >                | 大於             |
| >=               | 大於或等於 |
| <                | 小於                |
| <=               | 小於或等於    |



 

 

使用 "=" 運算子時，Windows Search 結構化查詢語言 (SQL)  (SQL) 支援使用 BEFORE 和 after 關鍵字，以指定查詢是否應該在字典排序次序中，比較指定值之前或之後的資料行值。


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a>範例

以下是常值比較述詞的範例。


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[LIKE 述詞](-search-sql-like.md)
</dt> <dt>

[DATEADD 函數](-search-sql-dateadd.md)
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

 

 



