---
description: 請一律先設定資料庫的字碼頁，再加入任何當地語系化資訊。
ms.assetid: 0d8aee30-989a-4093-8718-1bb90029c0fb
title: 設定資料庫的字碼頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c9ac1840b624b821dff6a85bee94607cd9568dcd6bb9b01025cb02f87c5c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628538"
---
# <a name="setting-the-code-page-of-a-database"></a>設定資料庫的字碼頁

請一律先設定資料庫的字碼頁，再加入任何當地語系化資訊。 因為這可能會損毀擴充字元，所以不建議在將資料輸入至資料庫之後嘗試設定字碼頁。 從以字碼頁中立的資料庫開始，可以大幅地促進當地語系化。 如需詳細資訊，請參閱 [使用中性程式碼建立資料庫頁面](creating-a-database-with-a-neutral-code-page.md)。 您可以依照 [判斷安裝資料庫的字碼頁](determining-an-installation-database-s-code-page.md)所述，判斷資料庫目前的字碼頁。 請參閱 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md) ，以取得數值字碼頁的清單。

您可以藉由匯入具有非中性字碼頁與 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)的文字保存檔案，來設定空白資料庫的字碼頁，或具有中性字碼頁的資料庫。 這會將資料庫的字碼頁設定為匯入檔案的字碼頁。 之後匯入資料庫的所有封存檔案，都必須與第一個檔案具有相同的字碼頁。 如果是從資料庫匯出文字保存檔案，則封存檔案的字碼頁與父資料庫相同。 請參閱匯 [入和匯出資料表的字碼頁處理](code-page-handling-of-imported-and-exported-tables.md)。

任何資料庫的字碼頁都可以設定為指定的數值字碼頁，方法是使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) 匯入具有下列格式的文字封存檔案：兩行空白;後面接著包含數值字碼頁的行、索引標籤分隔符號，以及確切的字串： \_ ForceCodepage。 請注意，在 Windows 2000 中，這會將資料庫中的所有字串轉譯為 ForceCodepage 的字碼頁 \_ 。 這可能是在當地語系化現有的資料庫，並將所有非中性的字串轉譯成新字碼頁時所設計。 但是，如果資料庫包含不會轉譯的非中性字元串，這會導致錯誤。

公用程式 WiLangId.vbs 提供如何使用匯 [**入方法**](database-import.md)來設定封裝字碼頁的範例。 Windows Installer SDK 中提供了 WiLangId.vbs 的複本。 您可以使用這個公用程式來判斷資料庫 (封裝) 所支援的語言版本、安裝程式用於使用者介面中未撰寫至資料庫 (產品) 之任何字串的語言版本，或字串集區的單一 ANSI 字碼頁 (程式碼片段) 。 如需使用 WiLangId.vbs 的詳細資訊，請參閱說明頁面： [管理語言和字碼頁](manage-language-and-codepage.md)。

若要判斷 Product、Package 和字碼頁的值，請執行 WiLangId.vbs，如下所示。

**cscript wilangid.vbs** *\[ 資料庫 \] 路徑*

若要設定封裝的字碼頁，請執行下列命令列。

**cscript wilangid.vbs** *\[ 資料庫 \]* **字碼頁** 的路徑 *\[ 值 \]*

例如，若要將 test.msi 的字碼頁設定為數值 ANSI 字碼頁值1252，請執行下列命令列。

**cscript wilangid.vbs c： \\ temp \\test.msi 字碼頁1252**

 

 



