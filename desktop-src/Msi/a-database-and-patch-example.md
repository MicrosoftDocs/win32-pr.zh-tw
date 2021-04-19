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
# <a name="a-database-and-patch-example"></a><span data-ttu-id="82b90-103">資料庫和修補範例</span><span class="sxs-lookup"><span data-stu-id="82b90-103">A Database and Patch Example</span></span>

<span data-ttu-id="82b90-104">應用程式可以使用 [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) 函式來開啟新的或現有的安裝資料庫 ( .msi 檔案) 或修補封裝 ( .msp 檔案。 ) 應用程式會先檢查 **MsiOpenDatabase** 的傳回值，再使用資料庫控制碼。</span><span class="sxs-lookup"><span data-stu-id="82b90-104">An application can use the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function to open a new or existing installation database (.msi file) or patch package (.msp file.) The application checks the return value of **MsiOpenDatabase** before using the database handle.</span></span>

<span data-ttu-id="82b90-105">下列範例會使用在 msi 中定義的 **PMSIHANDLE** 類型變數。</span><span class="sxs-lookup"><span data-stu-id="82b90-105">The following examples use the **PMSIHANDLE** type variables defined in msi.h.</span></span> <span data-ttu-id="82b90-106">建議使用 **PMSIHANDLE** 類型，因為安裝程式會在超出範圍時關閉 **PMSIHANDLE** 物件，而您的應用程式必須藉由呼叫 [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle)來關閉 **MSIHANDLE** 物件。</span><span class="sxs-lookup"><span data-stu-id="82b90-106">It is recommended to use the **PMSIHANDLE** type because the installer closes **PMSIHANDLE** objects as they go out of scope, whereas your application must close **MSIHANDLE** objects by calling [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).</span></span> <span data-ttu-id="82b90-107">如需詳細資訊，請參閱[Windows Installer 最佳做法](windows-installer-best-practices.md)中的[使用 PMSIHANDLE 而非控制碼](windows-installer-best-practices.md)一節。</span><span class="sxs-lookup"><span data-stu-id="82b90-107">For more information see [Use PMSIHANDLE instead of HANDLE](windows-installer-best-practices.md) section in the [Windows Installer Best Practices](windows-installer-best-practices.md).</span></span>

<span data-ttu-id="82b90-108">下列範例會開啟資料庫，sample.msi，僅供讀取。</span><span class="sxs-lookup"><span data-stu-id="82b90-108">The following example opens a database, sample.msi, for reading only.</span></span> <span data-ttu-id="82b90-109">只有當 sample.msi 存在於 c： test 目錄中時， [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)才會成功 \\ 。</span><span class="sxs-lookup"><span data-stu-id="82b90-109">[**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) succeeds only if sample.msi exists in the c:\\test directory.</span></span> <span data-ttu-id="82b90-110">成功時，會使用 [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) 和 [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)，在安裝套件中使用傳回的資料庫控制碼來查詢資料。</span><span class="sxs-lookup"><span data-stu-id="82b90-110">Upon success, the returned database handle can be used to query the data in the installation package using [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) and [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).</span></span>


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



<span data-ttu-id="82b90-111">下列範例會開啟資料庫以供讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="82b90-111">The following example opens the database for reading and writing.</span></span> <span data-ttu-id="82b90-112">如果應用程式呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)，就會儲存對資料庫所做的所有變更。</span><span class="sxs-lookup"><span data-stu-id="82b90-112">If the application calls [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), all changes made to the database are saved.</span></span> <span data-ttu-id="82b90-113">如果應用程式未呼叫 **MsiDatabaseCommit**，就不會對資料庫進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="82b90-113">If the application does not call **MsiDatabaseCommit**, no changes are made to the database.</span></span>


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



<span data-ttu-id="82b90-114">下列範例會使用現有的資料庫 text.msi，並建立新的資料庫 newtest.msi。</span><span class="sxs-lookup"><span data-stu-id="82b90-114">The following example takes an existing database, text.msi, and creates a new database, newtest.msi.</span></span> <span data-ttu-id="82b90-115">您可以藉由呼叫 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)，將所做的任何變更儲存在新的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="82b90-115">Any changes that are made can be saved in the new database by calling [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="82b90-116">*SzDatabasePath* 參數中指定的現有資料庫未變更。</span><span class="sxs-lookup"><span data-stu-id="82b90-116">The existing database specified in the *szDatabasePath* parameter is unchanged.</span></span>


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



<span data-ttu-id="82b90-117">下列範例會開啟 Windows Installer 修補套件 ( .msp 檔) 僅供讀取。</span><span class="sxs-lookup"><span data-stu-id="82b90-117">The following example opens a Windows Installer patch package (.msp file) for reading only.</span></span> <span data-ttu-id="82b90-118">傳回的 patch 控制碼可以用來判斷 patch 封裝中的封包和轉換 substorages，方法是針對[ \_ 資料流程](-streams-table.md)和[ \_ 儲存體](-storages-table.md)資料表進行查詢。</span><span class="sxs-lookup"><span data-stu-id="82b90-118">The returned patch handle can be used to determine the cabinets and transform substorages included in the patch package by queries on the [\_Streams](-streams-table.md) and [\_Storages](-storages-table.md) tables.</span></span>

<span data-ttu-id="82b90-119">**Windows Installer 2.0：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="82b90-119">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="82b90-120">從 Windows Installer 3.0 開始，應用程式可以查詢修補套件中的 [MsiPatchSequence 資料表](msipatchsequence-table.md) ，該封裝會使用新的修補程式排序資訊。</span><span class="sxs-lookup"><span data-stu-id="82b90-120">Beginning with Windows Installer 3.0, the application can query the [MsiPatchSequence table](msipatchsequence-table.md) present in a patch package that uses the new patch sequencing information.</span></span>


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



 

 



