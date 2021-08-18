---
description: 深入瞭解：資料行
title: 資料行
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 8cc7e3921c1904cdae3a09432d6a17eae3953251d3bd39c288cb6d6ffe184ffc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982698"
---
# <a name="columns"></a>資料行


_**適用于：** Windows |Windows伺服器_

## <a name="columns"></a>資料行

您可以藉由呼叫 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) 或不使用一組初始的資料行來建立資料表，方法是呼叫 [JetCreateTable](./jetcreatetable-function.md)。 ESE 中的資料表最多可以包含127個固定長度的資料行、128個可變長度的資料行，以及64993標記的資料行。 資料行是由其名稱和識別碼所識別，並可透過 [JetAddColumn](./jetaddcolumn-function.md)以動態方式新增至資料表。 建立資料行時，會使用特定的資料類型和一組選擇性的屬性，例如資料行是否為固定長度或是否可以是 Null。

資料行的型別決定了可能儲存在資料行中的資料，以及資料行的許多屬性，包括其編制索引的順序。 ESE 支援各式各樣的資料行類型，範圍從1位到 2 GB (2146483647 ASCII 字元或 1073741823 Unicode 字元) 。 如需 ESE 所支援之資料行資料類型的完整清單，請參閱 [JET_COLTYP](./jet-coltyp.md) 主題。 下列主題將討論 ESE 所支援的一些資料行類型：

  - [標記、固定和變數資料行](./tagged-fixed-and-variable-columns.md)

  - [版本、自動遞增和託管資料行](./version-auto-increment-and-escrow-columns.md)

  - [Long 值資料行](./long-value-columns.md)

  - [多重值的稀疏資料行](./multi-valued-sparse-columns.md)

  - [使用者定義資料行](./user-defined-columns.md)

  - [使用資料表中的資料行](./using-columns-in-a-table.md)
