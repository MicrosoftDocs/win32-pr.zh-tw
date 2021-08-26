---
description: Null 述詞指出檔是否有指定之資料行的值。
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Null 述詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd80ea6cba2009b398c8cdd0a2926240e3ce78309ca3f8511fb6ba286f44a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058118"
---
# <a name="null-predicate"></a>Null 述詞

**Null** 述詞指出檔是否有指定之資料行的值。

**Null** 述詞具有下列語法：


```
...WHERE <column> IS [NOT] NULL
```



選擇性的 NOT 關鍵字會否定結果。 此資料行可以是一般或分隔的 [識別碼](-search-sql-identifiers.md)。

> [!IMPORTANT]
> 若要測試資料行是否有 **null** 值，您必須使用 **null** 述詞。 在比較述詞中使用 **Null** 值是不正確。 「WHERE 資料行是 **Null**」是正確的。 "WHERE column = **Null**" 無效。

 

## <a name="example"></a>範例

下列範例會傳回沒有 System.object 值的檔。


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[LIKE 述詞](-search-sql-like.md)
</dt> <dt>

[常值比較](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[多重值 (陣列) 比較](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**概念**
</dt> <dt>

[全文檢索述詞](-search-sql-fulltextpredicates.md)
</dt> <dt>

[非全文檢索述詞](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



