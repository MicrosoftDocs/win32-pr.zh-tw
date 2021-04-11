---
description: 深入瞭解： ORDER BY 子句
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: ORDER BY 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eaa3c834ca2fe04222ef2ae452a0119bf391b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112420"
---
# <a name="order-by-clause"></a>ORDER BY 子句

ORDER BY 子句會根據您指定的一或多個資料行的值來排序結果。 以下是 ORDER BY 子句的語法：


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



資料行規范必須是有效的資料行。 您可以使用資料行規范，依照查詢中出現的順序來參考資料行。 查詢中的第一個資料行編號為1。 您可以在 ORDER BY 子句中包含一個以上的資料行，並以逗號分隔。

選擇性的方向規範可以是 "ASC" （表示遞增 (低至高) 或 "DESC"），以遞減 (高至低) 。 如果您未提供方向規範，則會使用預設值 [遞增]。 如果您指定一個以上的資料行，但未指定所有方向，則您指定的最後一個方向會套用至每個資料行，直到您明確變更方向為止。

例如，在下列 ORDER BY 子句中，A、B、C 和 G 資料行是以遞增順序排序，而資料行 D、E 和 F 則是以遞減順序排序。


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[FROM 子句](-search-sql-from.md)
</dt> <dt>

[RANK BY 子句](-search-sql-rankby.md)
</dt> <dt>

[SELECT 語句](-search-sql-select.md)
</dt> <dt>

**概念**
</dt> <dt>

[全文檢索述詞](-search-sql-fulltextpredicates.md)
</dt> <dt>

[非全文檢索述詞](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



