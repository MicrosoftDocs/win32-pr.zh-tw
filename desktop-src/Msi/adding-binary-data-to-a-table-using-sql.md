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
# <a name="adding-binary-data-to-a-table-using-sql"></a><span data-ttu-id="af88a-103">使用 SQL 將二進位資料新增至資料表</span><span class="sxs-lookup"><span data-stu-id="af88a-103">Adding Binary Data to a Table Using SQL</span></span>

<span data-ttu-id="af88a-104">二進位資料無法使用 INSERT INTO 或 UPDATE SQL 查詢直接插入資料表中。</span><span class="sxs-lookup"><span data-stu-id="af88a-104">Binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL queries.</span></span> <span data-ttu-id="af88a-105">若要將二進位資料加入至資料表，您必須先在查詢中使用參數標記 (？ ) 作為二進位值的預留位置。</span><span class="sxs-lookup"><span data-stu-id="af88a-105">In order to add binary data to a table, you must first use the parameter marker (?) in the query as a placeholder for the binary value.</span></span> <span data-ttu-id="af88a-106">查詢的執行應該包含一筆記錄，其中包含其中一個欄位中的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="af88a-106">The execution of the query should include a record that contains the binary data in one of its fields.</span></span>

<span data-ttu-id="af88a-107">標記是由查詢所提交之記錄所提供值的參數參考。</span><span class="sxs-lookup"><span data-stu-id="af88a-107">A marker is a parameter reference to a value supplied by a record submitted with the query.</span></span> <span data-ttu-id="af88a-108">它是在 SQL 語句中，以問號 (？ ) 來表示。</span><span class="sxs-lookup"><span data-stu-id="af88a-108">It is represented in the SQL statement by a question mark (?).</span></span>

<span data-ttu-id="af88a-109">下列範例程式碼會將二進位資料加入至資料表。</span><span class="sxs-lookup"><span data-stu-id="af88a-109">The following sample code adds binary data to a table.</span></span>


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



<span data-ttu-id="af88a-110">下列範例腳本會將二進位資料加入至資料表。</span><span class="sxs-lookup"><span data-stu-id="af88a-110">The following sample script adds binary data to a table.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="af88a-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="af88a-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af88a-112">使用查詢</span><span class="sxs-lookup"><span data-stu-id="af88a-112">Working with Queries</span></span>](working-with-queries.md)
</dt> <dt>

[<span data-ttu-id="af88a-113">SQL 語法</span><span class="sxs-lookup"><span data-stu-id="af88a-113">SQL Syntax</span></span>](sql-syntax.md)
</dt> <dt>

[<span data-ttu-id="af88a-114">使用 SQL 和腳本的資料庫查詢範例</span><span class="sxs-lookup"><span data-stu-id="af88a-114">Examples of Database Queries Using SQL and Script</span></span>](examples-of-database-queries-using-sql-and-script.md)
</dt> </dl>

 

 



