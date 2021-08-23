---
description: 深入瞭解：從資料庫讀取資料
title: 從資料庫讀取資料
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 7d33aa2640c07018186a5516d985fd4e46194d39cd4b12b7254f430f889e2484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780258"
---
# <a name="reading-data-from-the-database"></a>從資料庫讀取資料


_**適用于：** Windows |Windows伺服器_

## <a name="reading-data-from-the-database"></a>從資料庫讀取資料

從資料庫讀取資料時，應該在交易內執行。

下列程式說明如何在資料庫中執行簡單的讀取作業。

### <a name="to-read-data-from-a-database"></a>從資料庫讀取資料

1.  使用會話識別碼呼叫 [JetBeginTransaction](./jetbegintransaction-function.md) 或 [JetBeginTransaction2](./jetbegintransaction2-function.md) ，以啟動交易。

2.  藉由在 *魚尾紋* 參數中使用 JET_MoveFirst 呼叫 [JetMove](./jetmove-function.md) ，將游標移到所需的記錄。 如需如何移動游標的詳細資訊，請參閱 [資料表主題中的索引](./indexing-in-the-table.md) 。

3.  使用 *InfoLevel* 參數中指定的 JET_ColInfo，在目前記錄上呼叫 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) ，以抓取資料行的資料行識別碼。 [JET_COLUMNDEF](./jet-columndef-structure.md)結構中會傳回資料行識別碼。

4.  從資料行讀取資料，方法是呼叫 [JetRetrieveColumn](./jetretrievecolumn-function.md) ，並在 columnid 參數的步驟3中抓取資料行識別碼。 *PvData* 參數包含在步驟3中所抓取 [JET_COLUMNDEF](./jet-columndef-structure.md)結構中指定的資料類型。

5.  呼叫 [JetCommitTransaction](./jetcommittransaction-function.md) 將交易認可到資料庫。
