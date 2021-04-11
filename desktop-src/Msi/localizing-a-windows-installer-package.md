---
description: 如需當地語系化的一般資訊，請參閱全球化服務。
ms.assetid: 734961f6-de0a-4c54-9866-ade994c41c7e
title: 當地語系化 Windows Installer 套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b325b211302fba632f454f30eefbcb688f30d819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113565"
---
# <a name="localizing-a-windows-installer-package"></a>當地語系化 Windows Installer 套件

如需當地語系化的一般資訊，請參閱 [全球化服務](../intl/globalization-services.md)。 當地語系化 Windows Installer 套件需要修改使用者介面所顯示的字串，也可能需要新增或修改產品資源。 例如，當地語系化可能包括將國際 Dll 和當地語系化檔案新增至產品。

**當地語系化 Windows Installer 套件**

1.  撰寫原始安裝套件時，準備進行當地語系化。 設計當地語系化檔案的版面配置，讓不同的語言版本在使用者的電腦上安裝時可以安全並存。 將需要當地語系化的檔案組織成個別的元件，並將這些檔案安裝在不同的目錄中。 撰寫具有中立控制頁面的基礎安裝資料庫。 請參閱 [準備 Windows Installer 套件以進行當地語系化](preparing-a-windows-installer-package-for-localization.md)。
2.  請一律先設定要當地語系化之資料庫的字碼頁，再加入任何當地語系化的資料。 如果要當地語系化之資料庫的字碼頁是中性的，請參閱 [設定資料庫的字碼頁](setting-the-code-page-of-a-database.md)。 若要判斷字碼頁，請參閱 [判斷安裝資料庫的字碼頁](determining-an-installation-database-s-code-page.md)。
3.  將當地語系化的 [錯誤資料表](error-table.md) 和 [ActionText 資料表](actiontext-table.md) 匯入資料庫中。 如需詳細資訊，請參閱 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md) ，以取得 Microsoft WINDOWS 軟體開發套件 (SDK) 所支援的語言清單。 您可以使用 Msidb.exe 或 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)來匯入這些資料表。
4.  使用資料表編輯器或 SQL 查詢，修改資料庫中任何其他可當地語系化的資料行。 如需 SQL access 函數，請參閱 [使用查詢](working-with-queries.md)。 資料庫資料表的主題會識別可以當地語系化的資料庫資料行。 如需詳細資訊，請參閱 [資料庫資料表](database-tables.md)中的資料表清單。
5.  將 [屬性工作表](property-table.md)中的 [**ProductLanguage**](productlanguage.md)屬性設定為資料庫的 LANGID。 將封裝編寫為非語言相關時，請將 ProductLanguage 屬性設定為0，並使用 MS Shell Dlg 字型作為所有撰寫之對話方塊的文字樣式。 因為某些字型不支援所有字元集，所以您可以使用這個字型來確保文字在所有當地語系化版本的作業系統上都已正確顯示。
6.  設定 [ [**範本摘要**](template-summary.md) ] 屬性的 [語言] 欄位，以反映資料庫的 LANGID。
7.  如果 [摘要資訊資料流程](summary-information-stream.md) 中的文字字串已當地語系化，請將 [字碼頁 [**摘要**](codepage-summary.md) ] 屬性設定為 [字碼頁]。
8.  設定 [屬性工作表](property-table.md)中的 [ [**ProductCode**](productcode.md) ] 屬性，並將 [[**修訂編號摘要**](revision-number-summary.md)] 屬性中的封裝程式碼設定為新的封裝程式碼。 當地語系化的產品會視為不同的產品。 例如，應用程式的德文和英文版會視為兩個不同的產品，而且必須具有不同的產品代碼。
9.  當地語系化可能需要修改已經存在的資源，或是新增資源（例如檔案或登錄機碼）。 檢查並確定已新增新資源的每個現有元件的元件程式碼已變更。 其他修改可能也需要變更元件的程式碼。 如需詳細資訊，請參閱 [變更元件代碼](changing-the-component-code.md)。
10. 藉由使用編輯工具或呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)儲存封裝，請務必儲存資料庫的當地語系化和其他變更。

如需詳細資訊，請參閱 [當地語系化範例](a-localization-example.md)。

 

 
