---
description: Windows Installer 開發人員 Windows SDK 元件中提供了 VBScript 檔案 WiRunSQL.vbs。
ms.assetid: 1027b187-1237-43d1-9905-8fcdaec63903
title: 執行 SQL 語句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99da54f85b02ee867003b140d505f5754f58cc00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996692"
---
# <a name="execute-sql-statements"></a>執行 SQL 語句

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供了 VBScript 檔案 WiRunSQL.vbs。 此範例說明如何使用腳本來對 Windows Installer 資料庫執行 SQL 查詢和更新。 如需詳細資訊，請參閱 [Sql 語法](sql-syntax.md) 和 [使用 sql 和腳本的資料庫查詢範例](examples-of-database-queries-using-sql-and-script.md)。

範例腳本會示範：

-   [**OpenDatabase 方法 (安裝程式物件)**](installer-opendatabase.md)和 [**安裝程式物件**](installer-object.md)的 [**LastErrorRecord 方法**](installer-lasterrorrecord.md)
-   [**OpenView 方法**](database-openview.md)和 [**Database 物件**](database-object.md)的 [**Commit 方法**](database-commit.md)
-   [](view-execute.md) [ **View 物件** 的 Execute 方法](view-object.md)
-   [**至 convertfrom-stringdata 屬性**](record-stringdata.md) Propertyof [**記錄物件**](record-object.md)

使用此範例需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。 若要使用 CScript.exe 執行此範例，請使用下列語法在命令提示字元中輸入命令。 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。 若要將輸出重新導向至檔案，請以 VBS > 路徑結束命令列 \[  \] 。 此範例會傳回值0表示成功，如果叫用說明，則傳回 1; 如果腳本失敗，則傳回2。

**cscript WiRunSQL.vbs \[ 資料庫 \] \[ SQL 查詢的路徑\]**

指定 Windows Installer 資料庫的路徑。 指定要執行的 SQL 查詢。 請注意，SQL 查詢必須括在雙引號中。 選取 [查詢] 會顯示查詢中所指定之結果清單的資料列。 不會顯示查詢所選取的二進位資料行。

如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

如需詳細資訊，請參閱[使用 SQL 和腳本](examples-of-database-queries-using-sql-and-script.md)[處理查詢](working-with-queries.md)和資料庫查詢範例。 範例 [當地語系化範例](a-localization-example.md) 示範如何使用 SQL 來 [當地語系化資料庫資料行](localizing-database-columns.md) ，以及 [更新摘要資訊資料流程](updating-a-summary-information-stream.md)。

 

 



