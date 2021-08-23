---
description: 您可以使用 MsiDatabaseExport 和 MsiDatabaseImport 匯入和匯出 ASCII 文字封存檔案，以將當地語系化資訊新增至安裝資料庫。
ms.assetid: dc52313b-38e7-43cc-abfd-86966c836fce
title: 匯入和匯出資料表的字碼頁處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f9a64617ccfda25380076d62e6dd4ad8c18c55f68afd0236b3258638c899f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065998"
---
# <a name="code-page-handling-of-imported-and-exported-tables"></a>匯入和匯出資料表的字碼頁處理

您可以使用 [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) 和 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)匯入和匯出 ASCII 文字封存檔案，以將當地語系化資訊新增至安裝資料庫。 因為資料庫字串集區使用 ANSI 字碼頁，所以資料庫和匯出的 [文字](text-archive-files.md) 封存檔都具有字碼頁。

從資料庫匯出 [文字保存](text-archive-files.md) 盤案時，封存檔案的字碼頁與父資料庫相同。 如需數值字碼頁的清單，請參閱 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md)。

> [!Note]  
> 將資料表匯出到文字封存檔案會轉譯控制字元，以避免與檔案分隔符號發生衝突。

 

## <a name="ascii-text-archive-files"></a>ASCII 壓縮檔案

[**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)匯出的 ASCII [文字](text-archive-files.md)封存檔案會以下列格式說明：

-   資料表資料行的名稱是寫入第一行。
-   資料行格式是在第二行寫入。
-   如果資料表只包含 ASCII 資料，則文字檔的第三行是資料表名稱，後面接著主鍵清單。
-   如果資料表包含非 ASCII 資料，而且資料庫是以數位字碼頁戳記，則字碼頁編號會出現在第三行的開頭。
-   如果資料庫包含非 ASCII 資料，但資料庫未加上數位字碼頁的戳記，則會在第三行的開頭寫入目前的系統字碼頁編號。
-   文字檔的其餘行是指定字碼頁中的資料。
-   如果資料表包含資料流程， [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) 會將資料表中的每個資料流程匯出至個別的檔案。

### <a name="neutral-and-non-neutral-code-pages"></a>中性和非中性字碼頁

您可以從具有中性字碼頁的資料庫開始，以促進當地語系化：

-   空白資料庫具有中性的字碼頁。
-   若資料庫不包含需要以 ASCII 表示之字碼頁的擴充字元，則會有中立的字碼頁。

如需詳細資訊，請參閱 [使用中性程式碼建立資料庫頁面](creating-a-database-with-a-neutral-code-page.md)。

中性和非中性的字碼頁具有下列特性：

-   如果將具有非中性字碼頁的 [文字](text-archive-files.md) 封存檔匯入至具有不同非特定字碼頁的資料庫，則在呼叫 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) 時，安裝程式會傳回錯誤。
-   具有中性字碼頁的 [文字保存](text-archive-files.md) 盤案，可以匯入具有任何字碼頁的資料庫中。
-   具有任何字碼頁的 [文字保存](text-archive-files.md) 盤案，可以匯入具有中性字碼頁的資料庫中。
-   使用中性字碼頁將 [文字](text-archive-files.md) 封存檔匯入資料庫中，會將資料庫的字碼頁設定為 [封存檔案代碼] 頁面。 後續匯入資料庫的所有封存檔案都必須有與第一個檔案相同的字碼頁。

如需詳細資訊，請參閱 [判斷安裝資料庫字碼頁](determining-an-installation-database-s-code-page.md) 和 [設定資料庫的字碼頁](setting-the-code-page-of-a-database.md)。

[**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)匯出的 [文字](text-archive-files.md)封存檔案可以與版本控制系統搭配使用。 使用 [資料庫函數](database-functions.md) 或資料庫資料表編輯器來編輯資料庫。

您可以使用資料庫資料表編輯器或 Windows Installer API，將當地語系化資訊加入至安裝資料庫。 如需詳細資訊，請參閱 [參數字串的字碼頁處理](code-page-handling-of-parameter-strings.md)。

 

 



