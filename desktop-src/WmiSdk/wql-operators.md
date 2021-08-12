---
description: 描述 WHERE 子句或 SELECT 語句中使用的 WQL 運算子。
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: WQL 運算子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a441afb661e4f8d92e21d944462dddd6d7390fd2dbe871512342f7c9251d6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553085"
---
# <a name="wql-operators"></a>WQL 運算子

Windows Management Instrumentation Query Language (WQL) 支援在 SELECT 語句的[WHERE 子句](where-clause.md)中使用的一組標準運算子，如下所示。



| 運算子       | 描述              |
|----------------|--------------------------|
| =              | 等於                 |
| <           | 小於                |
| >           | 大於             |
| <=          | 小於或等於    |
| >=          | 大於或等於 |
| ！ = 或 <> | 不等於             |



 

有幾個額外的 WQL 特定運算子：是、不是、ISA 和 LIKE。 只有當常數是 **Null** 時，才會在 WHERE 子句中有效，而不是運算子。 例如，下列查詢是有效的：


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



下列查詢顯示的無效用法為，而且不是：


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



ISA 運算子用於資料和事件查詢的 WHERE 子句中，用來測試類別階層的内嵌物件。 ISA 運算子在要求類別階層時，不需要追蹤新衍生的類別。 當您使用 ISA 時，所要求類別的新建立和現有子類別會自動包含在結果集中。

如需此運算子的語法和用法的詳細資訊，請參閱下列主題：

-   [資料查詢的 ISA 運算子](isa-operator-for-data-queries.md)
-   [事件查詢的 ISA 運算子](isa-operator-for-event-queries.md)
-   [適用于架構查詢的 ISA 運算子](isa-operator-for-schema-queries.md)

LIKE 運算子在 WHERE 子句中是有效的，用來判斷指定的字元字串是否符合指定的模式。 例如，下列查詢會傳回 Win32 類別的所有實例 \_ 。


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



如需這個運算子的語法和用法的詳細資訊，請參閱 [LIKE 運算子](like-operator.md)。

 

 



