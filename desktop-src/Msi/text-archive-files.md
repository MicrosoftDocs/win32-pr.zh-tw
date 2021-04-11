---
description: 您可以使用 MsiDatabaseExport 或 Database 物件的 Export 方法，將 Windows Installer 資料庫資料表匯出到 ASCII 文字檔。
ms.assetid: 49210242-bd32-4e5c-b782-a132d670fdfe
title: 壓縮檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baba814fd182a7da5e13fbb26eec257be96ab1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849628"
---
# <a name="text-archive-files"></a>壓縮檔案

您可以使用 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)或 [**Database**](database-object.md)物件的 [**Export**](database-export.md)方法，將 Windows Installer 資料庫資料表匯出到 ASCII 文字檔。 然後，您可以使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)或 **Database** 物件的 [Import](database-import.md)方法，將這些文字封存檔案中的資訊匯入回 Windows Installer 資料庫。

[msidb.exe](msidb-exe.md)之類的工具都可以匯出和匯入文字保存檔案。 如需可從資料庫匯出及匯入文字封存檔案的[Windows Installer 腳本範例](windows-installer-scripting-examples.md)，請參閱[匯出](export-files.md)檔案和匯[入](import-files.md)檔案。

> [!Note]  
> 文字封存檔案並非用來做為編輯安裝資料庫的方式。 您應該使用 Windows Installer 表編輯工具（例如 [Orca](orca-exe.md) 或協力廠商工具）來建立和修改安裝套件。

 

文字封存檔案可用於下列用途。

-   文字封存檔案可以與版本控制系統搭配使用。
-   移除浪費的儲存空間，並減少 .msi 檔案的最終大小。 請參閱 [減少 .msi 檔案的大小](reducing-the-size-of-an--msi-file.md)。
-   將當地語系化資訊新增至安裝資料庫。 如需詳細資訊，請參閱匯 [入和匯出資料表的字碼頁處理](code-page-handling-of-imported-and-exported-tables.md)。

-   判斷資料庫的字碼頁。 請參閱 [判斷安裝資料庫的字碼頁](determining-an-installation-database-s-code-page.md)。
-   若要設定資料庫的字碼頁。 請參閱 [設定資料庫的字碼頁](setting-the-code-page-of-a-database.md)。
-   提高資料庫資料行的限制。 使用 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)匯出資料表、編輯匯出的 idt 檔案，然後使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)匯入資料表。 作者無法變更標準資料表中任何資料行的資料行資料類型、null 屬性或當地語系化屬性。 另請參閱 [撰寫大型套件](authoring-a-large-package.md)。

下列頁面會解說文字保存頁面及其格式。

-   [封存檔案格式](archive-file-format.md)
-   [壓縮檔案中的 ASCII 資料](ascii-data-in-text-archive-files.md)
-   [\_ForceCodepage](-forcecodepage.md)
-   [\_SummaryInformation](-summaryinformation.md)

 

 



