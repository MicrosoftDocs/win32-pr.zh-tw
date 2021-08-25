---
description: 查詢中的 WHERE 子句會指定一組要與結果比對的專案。
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: ReuseWhere 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f073a7ac0d5faf5973d08ff53ccebdacf8bead080a53e2d9a4a6ae9ed5724db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944658"
---
# <a name="reusewhere-function"></a>ReuseWhere 函式

查詢中的 [WHERE](-search-sql-where.md) 子句會指定一組要與結果比對的專案。 後續查詢可以在新的查詢 WHERE 子句中使用 ReuseWhere 函式，來共用先前查詢所執行的工作。 利用此函式的查詢執行速度更快。

## <a name="examples"></a>範例

下列案例顯示如何使用 ReuseWhere 函數：

1.  您發出下列查詢：
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  從傳回的資料列集，您可以取得 [WHERE 識別碼](-search-sql-rowset-properties.md) *Query1WhereID*。

    Where ID 是具有 PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01}、PROPID 8 和 type UI4 的資料列集屬性。

3.  您可以使用 ReuseWhere 函式發出第二個查詢，並傳入步驟2的 *Query1WhereID* ：
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

第二個查詢相當於下列專案：


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



ReuseWhere 函數可以在 [WHERE](-search-sql-where.md) 子句中 anwhere 使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[WHERE 子句](-search-sql-where.md)
</dt> <dt>

[資料列集屬性](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



