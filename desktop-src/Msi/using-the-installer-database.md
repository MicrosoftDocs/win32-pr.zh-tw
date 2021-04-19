---
description: 安裝程式資料庫可讓安裝封裝的開發人員控制將應用程式從來源傳送到目標映射的程式。
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: 使用安裝程式資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb22b9c66547c849b4c9cbd012e78b22d9301756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976909"
---
# <a name="using-the-installer-database"></a>使用安裝程式資料庫

安裝 [程式資料庫](installer-database.md) 可讓安裝封裝的開發人員控制將應用程式從來源傳送到目標映射的程式。 應用程式的來源和目標影像的版面配置都是在 [目錄](directory-table.md) 資料表中指定的，而安裝應用程式的動作則是以六個順序表格來指定：

-   [InstallUISequence](installuisequence-table.md) 資料表
-   [InstallExecuteSequence](installexecutesequence-table.md) 資料表
-   [AdminUISequence](adminuisequence-table.md) 資料表
-   [AdminExecuteSequence](adminexecutesequence-table.md) 資料表
-   [AdvtUISequence](advtuisequence-table.md) 資料表
-   [AdvtExecuteSequence](advtexecutesequence-table.md) 資料表

下列各節說明如何使用 [安裝程式資料庫](installer-database.md)：

-   [使用目錄資料表](using-the-directory-table.md)
-   [使用順序資料表](using-a-sequence-table.md)
-   [取得資料庫控制碼](obtaining-a-database-handle.md)
-   [認可資料庫](committing-databases.md)
-   [匯入和匯出](importing-and-exporting.md)
-   [合併資料庫](merging-databases.md)
-   [命名自訂資料表、屬性和動作](naming-custom-tables-properties-and-actions.md)
-   [資料流程的 OLE 限制](ole-limitations-on-streams.md)
-   [使用查詢](working-with-queries.md)
-   [使用 SQL 將二進位資料新增至資料表](adding-binary-data-to-a-table-using-sql.md)
-   [使用記錄](working-with-records.md)
-   [使用資料夾位置](working-with-folder-locations.md)
-   [指定自我註冊的順序](specifying-the-order-of-self-registration.md)
-   [要在移除期間執行的調節動作](conditioning-actions-to-run-during-removal.md)
-   [從程式呼叫資料庫函式](calling-database-functions-from-programs.md)
-   [條件陳述式語法](conditional-statement-syntax.md)
-   [資料行定義格式](column-definition-format.md)
-   [判斷資料行是否為主要或外部索引鍵](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



