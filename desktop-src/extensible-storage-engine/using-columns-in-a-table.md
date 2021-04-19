---
description: 深入瞭解：在資料表中使用資料行
title: 使用資料表中的資料行
TOCTitle: Using Columns in a Table
ms:assetid: 064ac59e-d306-4335-a623-754a003f5ebc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269178(v=EXCHG.10)
ms:contentKeyID: 32765481
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: cd715b171162f63aaf0772ff6ec2e4a6d057a0d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973298"
---
# <a name="using-columns-in-a-table"></a>使用資料表中的資料行


_**適用于：** Windows |Windows Server_

## <a name="using-columns-in-a-table"></a>使用資料表中的資料行

您可以藉由呼叫[JetCreateTable](./jetcreatetable-function.md)來呼叫[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)或沒有資料行，以建立一組初始的資料行來建立資料表。 當使用 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) 或 [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)呼叫中的一組初始資料行來建立資料表時，它會包含 [JET_TABLECREATE](./jet-tablecreate-structure.md) (或 [JET_TABLECREATE2](./jet-tablecreate2-structure.md)) 結構。 這些結構包含 [JET_COLUMNCREATE](./jet-columncreate-structure.md) 結構的陣列，可定義資料表中的資料行集合。 **Grbit** 成員會設定資料行上的選項，而 **coltyp** 成員會設定可在資料行中設定的資料類型。

如果建立的資料表沒有資料行，就必須使用[JET_COLUMNDEF](./jet-columndef-structure.md)結構來呼叫[JetAddColumn](./jetaddcolumn-function.md) ，以加入資料表。 [JET_COLUMNDEF](./jet-columndef-structure.md)結構的 **grbit** 成員會設定資料行上的選項，而 **coltyp** 成員會設定可在資料行中設定的資料類型。 預設資料行值是在呼叫 [JetAddColumn](./jetaddcolumn-function.md) 時設定，方法是在 *pvDefault* 參數中指定值，並在 *cbDefault* 參數中指定大小。 沒有預設值的資料行有效的預設值是 Null。

資料表中的值只能在交易的內容中設定。 交易開始于呼叫 [JetBeginTransaction](./jetbegintransaction-function.md) ，結束于 [JetCommitTransaction](./jetcommittransaction-function.md)的呼叫中。 在交易中，您可以藉由呼叫 [JetSetColumn](./jetsetcolumn-function.md)來設定單一資料行值，或是藉由呼叫 [JetSetColumns](./jetsetcolumns-function.md)來設定多個資料行值。 [JetSetColumns](./jetsetcolumns-function.md) 使用 [JET_SETCOLUMN](./jet-setcolumn-structure.md) 結構的陣列來設定資料表中的多個資料行。 資料會包含在 [JetSetColumn](./jetsetcolumn-function.md)的 *pvData* 參數或 [JET_SETCOLUMN](./jet-setcolumn-structure.md)結構中的 **pvData** 成員。

在[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)的呼叫中會傳回[JET_COLUMNBASE](./jet-columnbase-structure.md)、 [JET_COLUMNLIST](./jet-columnlist-structure.md)和[JET_COLUMNDEF](./jet-columndef-structure.md)結構，而且會根據抓取的資料行類型而[JetGetColumnInfo](./jetgetcolumninfo-function.md) 。 [JET_COLUMNBASE](./jet-columnbase-structure.md)結構描述了基底資料行的參數，而[JET_COLUMNLIST](./jet-columnlist-structure.md)包含了[JetGetColumnInfo](./jetgetcolumninfo-function.md)和[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)函數所建立之臨時表的遍歷所需的資訊。
