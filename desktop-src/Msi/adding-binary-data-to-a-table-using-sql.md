---
description: 二進位資料無法使用 INSERT INTO 或 UPDATE SQL 查詢直接插入資料表中。
ms.assetid: cc055de8-eaba-48eb-a982-4d584ac7a881
title: 使用 SQL 將二進位資料新增至資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491bfe57354b4faf9f7c385bc4e14c64ad366f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848994"
---
# <a name="adding-binary-data-to-a-table-using-sql"></a>使用 SQL 將二進位資料新增至資料表

二進位資料無法使用 INSERT INTO 或 UPDATE SQL 查詢直接插入資料表中。 若要將二進位資料加入至資料表，您必須先在查詢中使用參數標記 (？ ) 作為二進位值的預留位置。 查詢的執行應該包含一筆記錄，其中包含其中一個欄位中的二進位資料。

標記是由查詢所提交之記錄所提供值的參數參考。 它是在 SQL 語句中，以問號 (？ ) 來表示。

下列範例程式碼會將二進位資料加入至資料表。


```C++
#include <windows.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")


int main()  
{ 

PMSIHANDLE hDatabase = 0;
PMSIHANDLE hView = 0;
PMSIHANDLE hRec = 0;

if (ERROR_SUCCESS == MsiOpenDatabase(_T("c:\\temp\\testdb.msi"), MSIDBOPEN_TRANSACT, &hDatabase))
{
    //
    // Open view on Binary table so that we can add a new row, must use '?' to represent Binary data
    //

    if (ERROR_SUCCESS == MsiDatabaseOpenView(hDatabase, _T("INSERT INTO `Binary` (`Name`, `Data`) VALUES ('NewBlob', ?)"), &hView))
    {

        //
        // Create record with binary data in 1st field (must match up with '?' in query)
        //

        hRec = MsiCreateRecord(1);
        if (ERROR_SUCCESS == MsiRecordSetStream(hRec, 1, _T("c:\\temp\\data.bin")))
        {

            //
            // Execute view with record containing binary data value; commit database to save changes
            //

            if (ERROR_SUCCESS == MsiViewExecute(hView, hRec)
              && ERROR_SUCCESS == MsiViewClose(hView)
              && ERROR_SUCCESS == MsiDatabaseCommit(hDatabase))
            {
                //
                // New binary data successfully committed to the database
                //
            }
        }
    }
}

return 0;  
}
```



下列範例腳本會將二進位資料加入至資料表。


```VB
Dim Installer
Dim Database
Dim View
Dim Record

Set Installer = CreateObject("WindowsInstaller.Installer")

Set Record = Installer.CreateRecord(1)
Record.SetStream 1, "c:\temp\data.bin"

Set Database = Installer.OpenDatabase("c:\temp\testdb.msi", msiOpenDatabaseModeTransact)
Set View = Database.OpenView("INSERT INTO `Binary` (`Name`, `Data`) VALUES ('NewBlob', ?)")
View.Execute Record
Database.Commit ' save changes
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用查詢](working-with-queries.md)
</dt> <dt>

[SQL 語法](sql-syntax.md)
</dt> <dt>

[使用 SQL 和腳本的資料庫查詢範例](examples-of-database-queries-using-sql-and-script.md)
</dt> </dl>

 

 



