---
description: 應用程式可以使用 MsiOpenDatabase 函式來開啟新的或現有的安裝資料庫 ( .msi 檔案) 或修補封裝 ( .msp 檔案。 ) 應用程式會先檢查 MsiOpenDatabase 的傳回值，再使用資料庫控制碼。
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: 資料庫和修補範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ff5925fc409352b4c9ed8c1762ba1ad17b261f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985438"
---
# <a name="a-database-and-patch-example"></a>資料庫和修補範例

應用程式可以使用 [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) 函式來開啟新的或現有的安裝資料庫 ( .msi 檔案) 或修補封裝 ( .msp 檔案。 ) 應用程式會先檢查 **MsiOpenDatabase** 的傳回值，再使用資料庫控制碼。

下列範例會使用在 msi 中定義的 **PMSIHANDLE** 類型變數。 建議使用 **PMSIHANDLE** 類型，因為安裝程式會在超出範圍時關閉 **PMSIHANDLE** 物件，而您的應用程式必須藉由呼叫 [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)來關閉 **MSIHANDLE** 物件。 如需詳細資訊，請參閱[Windows Installer 最佳做法](windows-installer-best-practices.md)中的[使用 PMSIHANDLE 而非控制碼](windows-installer-best-practices.md)一節。

下列範例會開啟資料庫，sample.msi，僅供讀取。 只有當 sample.msi 存在於 c： test 目錄中時， [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)才會成功 \\ 。 成功時，會使用 [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) 和 [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)，在安裝套件中使用傳回的資料庫控制碼來查詢資料。


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



下列範例會開啟資料庫以供讀取和寫入。 如果應用程式呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)，就會儲存對資料庫所做的所有變更。 如果應用程式未呼叫 **MsiDatabaseCommit**，就不會對資料庫進行任何變更。


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



下列範例會使用現有的資料庫 text.msi，並建立新的資料庫 newtest.msi。 您可以藉由呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)，將所做的任何變更儲存在新的資料庫中。 *SzDatabasePath* 參數中指定的現有資料庫未變更。


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



下列範例會開啟 Windows Installer 修補套件 ( .msp 檔) 僅供讀取。 傳回的 patch 控制碼可以用來判斷 patch 封裝中的封包和轉換 substorages，方法是針對[ \_ 資料流程](-streams-table.md)和[ \_ 儲存體](-storages-table.md)資料表進行查詢。

**Windows Installer 2.0：** 不支援。 從 Windows Installer 3.0 開始，應用程式可以查詢修補套件中的 [MsiPatchSequence 資料表](msipatchsequence-table.md) ，該封裝會使用新的修補程式排序資訊。


```C++
PMSIHANDLE hDbPatch = 0;
LPCTSTR szPersistMode = MSIDBOPEN_READONLY + MSIDBOPEN_PATCHFILE;
UINT uiStatus4 = MsiOpenDatabase(TEXT("c:\\test\\sample.msp"), szPersistMode, &hDbPatch);
if (ERROR_SUCCESS != uiStatus4)
{
    // process error
    return uiStatus4;
}
```



 

 



