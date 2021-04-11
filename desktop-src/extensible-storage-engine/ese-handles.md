---
description: 深入瞭解： ESE 控制碼
title: ESE 控制碼
TOCTitle: ESE Handles
ms:assetid: 969ae14f-3548-431d-a19d-5df92891441d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269349(v=EXCHG.10)
ms:contentKeyID: 32765636
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: cc91a4586fc1619c55b5f45afbca39ce04c0c6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194476"
---
# <a name="ese-handles"></a>ESE 控制碼


_**適用于：** Windows |Windows Server_

## <a name="ese-handles"></a>ESE 控制碼

ESE 控制碼可用來建立會話和 access 資料庫。 它們會在階層中維護，這表示某層級的輸出會用來存取下一個層級的資源。

這裡的圖顯示建立控制碼的控制碼階層和對應函數。 此外，也指出函式是在呼叫中用來建立新控制碼的控制碼。

![ESE_Documentation_handles2](images/Gg269349.ESE_Documentation_handles2(EXCHG.10).gif "ESE_Documentation_handles2")

如圖所示，實例是根控制碼，以及資料庫在發生非預期的進程終止或系統關機時復原的層級。 實例控制碼（JET_INSTANCE）是由 [JetCreateInstance](./jetcreateinstance-function.md) 和 [JetCreateInstance2](./jetcreateinstance2-function.md)所建立。 下一個層級（工作階段層級）是 database engine 的交易內容，以及執行所有資料庫作業的層級。 在 [JetBeginSession](./jetbeginsession-function.md)的呼叫中，會在實例的內容中建立會話控制碼（JET_SESID）。 會話識別碼會用於所有後續呼叫，以存取資料表和資料庫。 如果一次有一個以上的執行緒正在使用實例，則每個執行緒都必須使用自己的會話控制碼。 資料庫控制碼是使用會話控制碼所建立，主要是用來管理資料庫的架構，但是也可以用來管理資料庫內的資料表。 資料庫控制碼只能用在建立它們的會話中。 在呼叫 [JetCreateDatabase](./jetcreatedatabase-function.md) 或 [JetOpenDatabase](./jetopendatabase-function.md)時，會建立資料庫的控制碼。 資料表會與建立它們的資料庫識別碼相關聯。

JET_TABLEID 資料類型包含資料庫資料指標的控制碼。 它是用來掃描記錄、搜尋記錄，或建立更新和刪除記錄。 資料表控制碼是在 [JetOpenTable](./jetopentable-function.md)或 [JetCreateTable](./jetcreatetable-function.md)的呼叫中建立的。 [JetOpenTempTable](./jetopentemptable-function.md)、 [JetOpenTempTable2](./jetopentemptable2-function.md)和 [JetOpenTempTable3](./jetopentemptable3-function.md) 也會建立臨時表的資料表識別碼，而 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) 和 [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) 會傳回 out 結構中的資料表識別碼。 資料表內建立的每個資料行都有唯一的資料行識別碼或 COLUMN_ID。 在 [JetAddColumn](./jetaddcolumn-function.md)的呼叫中，或在對臨時表的 [JetOpenTempTable](./jetopentemptable-function.md)、 [JetOpenTempTable2](./jetopentemptable2-function.md)或 [JetOpenTempTable3](./jetopentemptable3-function.md) 呼叫中建立資料行識別碼。 您也可以使用 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)之類的 api，依名稱針對指定的資料行取得資料行識別碼。
