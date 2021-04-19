---
description: Windows Installer 會將所有資料庫字串儲存在單一共用字串集區中，以減少資料庫的大小，並提升效能。 如需數值字碼頁的清單，請參閱當地語系化錯誤和 ActionText 資料表。
ms.assetid: 5d413fb7-99da-49f3-ace3-ec285df2e634
title: '程式字碼頁處理 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db2788a1bfc6bdb49ec1402d5bba8a1a2594b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972682"
---
# <a name="code-page-handling-windows-installer"></a>程式字碼頁處理 (Windows Installer) 

Windows Installer 會將所有資料庫字串儲存在單一共用字串集區中，以減少資料庫的大小，並提升效能。 如需數值字碼頁的清單，請參閱 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md)。

如需詳細資訊，請 [判斷安裝資料庫的字碼頁](determining-an-installation-database-s-code-page.md)。

Windows Installer 使用 [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) 來判斷字碼頁是否有效。

### <a name="localizing-a-windows-installer-package"></a>當地語系化 Windows Installer 套件

如果您將 Windows Installer 封裝當地語系化，它可能會涉及修改資料庫資料表中的資訊、將資料表匯出為 ANSI 文字封存檔案，然後將封存檔匯入正在當地語系化的資料庫中。 您也可以使用資料庫資料表編輯器或 [資料庫函數](database-functions.md)，將當地語系化變更加入至資料庫。 在對資料庫進行任何當地語系化變更之前，請務必先設定要當地語系化之資料庫的字碼頁。 將資料庫當地語系化之後，請不要設定資料庫的字碼頁，因為這樣可能會損毀擴充的字元。 如需詳細資訊，請參閱 [設定資料庫的字碼頁](setting-the-code-page-of-a-database.md)。

處理字碼頁的建議方法是撰寫一個中性資料庫，其中只包含可轉譯成任何字碼頁的字元。 如需詳細資訊，請參閱 [使用中性程式碼建立資料庫頁面](creating-a-database-with-a-neutral-code-page.md)。

如果您使用資料庫封存檔案加入當地語系化資訊，您可以使用 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) 將包含當地語系化變更的資料庫中的資料表匯出至 ANSI 文字封存檔案，然後將這些資料表匯入到以 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)當地語系化的資料庫中。 匯出封存檔案的字碼頁一律與其父資料庫相同。 匯入檔案的字碼頁和接收檔案的資料庫必須相同，或至少有兩個字碼頁必須是中立的。 如需詳細資訊，請參閱匯 [入和匯出資料表的字碼頁處理](code-page-handling-of-imported-and-exported-tables.md)。

如果您使用文字編輯器加入當地語系化資訊，或 [資料庫](database-functions.md) 函式小心只將字串參數傳遞至使用當地語系化資料庫之字碼頁的 Windows Installer API。 如果字串參數包含資料庫字碼頁未表示的字元，呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)時就會發生錯誤。 如需詳細資訊，請參閱 [參數字串的字碼頁處理](code-page-handling-of-parameter-strings.md)。

如果有一個封裝用來安裝產品的多個語言版本，則用來將字串當地語系化的轉換也可以變更資料庫的字碼頁。

 

 
