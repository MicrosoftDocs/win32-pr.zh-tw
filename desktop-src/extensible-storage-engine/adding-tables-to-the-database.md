---
description: 深入瞭解：將資料表加入至資料庫
title: 將資料表加入至資料庫
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 47cb3b87b96e8cb51f651bf7c069088df9d13f7502e24ed61d9d5c355bc6d827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117903534"
---
# <a name="adding-tables-to-the-database"></a>將資料表加入至資料庫


_**適用于：** Windows |Windows伺服器_

## <a name="adding-tables-to-the-database"></a>將資料表加入至資料庫

資料表是一組異類記錄，這些記錄會以實體和邏輯方式將資料庫中的資料分組。 資料表是由其名稱唯一識別。 資料表識別碼 ([JET_TABLEID](./jet-tableid.md)) 是資料指標的控制碼，可用來更新和流覽資料表。 您可以在相同的資料表上開啟多個 [JET_TABLEID](./jet-tableid.md) 。

現有的資料表會在 [JetOpenTable](./jetopentable-function.md)的呼叫中開啟，而且會建立新的資料表，而不會有 [JetCreateTable](./jetcreatetable-function.md)的資料列或資料行。 若要以自動方式建立一組初始的資料行和索引的資料表，請呼叫 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) 或 [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)。 資料表的初始大小是在 [JetCreateTable](./jetcreatetable-function.md)的 *lPages* 參數中指定，或是呼叫 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)中的 [JET_TABLECREATE](./jet-tablecreate-structure.md)結構的 **ulPages** 成員提供。 將資料加入資料表時，資料表會自動成長。 成長與資料表的初始大小成正比。 您可以使用 [JetAddColumn](./jetaddcolumn-function.md)隨時將資料行加入至資料表。 當應用程式不再需要存取資料表時，可以使用 [JetCloseTable](./jetclosetable-function.md)來關閉資料指標。 您可以透過呼叫 [JetDeleteTable](./jetdeletetable-function.md)來刪除資料表。

資料表作業應該在交易內容中執行。

## <a name="see-also"></a>另請參閱

[交易](./transactions.md)
