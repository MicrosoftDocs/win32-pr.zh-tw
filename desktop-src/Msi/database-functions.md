---
description: 這份資料是針對正在撰寫自己的安裝程式，以及想要深入瞭解安裝程式資料庫資料表之開發人員的開發人員所設計。 如需安裝程式的一般資訊，請參閱關於 Windows Installer。
ms.assetid: 95516437-9708-4f4e-a5c2-7bcd4741c776
title: 資料庫函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a4233437d24944c8bb7fe5c7de6412e700022b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691076"
---
# <a name="database-functions"></a><span data-ttu-id="fbff4-104">資料庫函數</span><span class="sxs-lookup"><span data-stu-id="fbff4-104">Database Functions</span></span>

<span data-ttu-id="fbff4-105">這份資料是針對正在撰寫自己的安裝程式，以及想要深入瞭解安裝程式資料庫資料表之開發人員的開發人員所設計。</span><span class="sxs-lookup"><span data-stu-id="fbff4-105">This material is intended for developers who are writing their own setup programs and developers who want to learn more about the installer database tables.</span></span> <span data-ttu-id="fbff4-106">如需安裝程式的一般資訊，請參閱 [關於 Windows Installer](about-windows-installer.md)。</span><span class="sxs-lookup"><span data-stu-id="fbff4-106">For general information on the installer, see [About Windows Installer](about-windows-installer.md).</span></span>

<span data-ttu-id="fbff4-107">您可以使用安裝程式存取功能來存取資料庫和安裝程式。</span><span class="sxs-lookup"><span data-stu-id="fbff4-107">You can use the installer access functions to access the database and the installation process.</span></span> <span data-ttu-id="fbff4-108">這些函式只能由自訂安裝動作和 authoring tools 使用。</span><span class="sxs-lookup"><span data-stu-id="fbff4-108">These functions should only be used by custom installation actions and authoring tools.</span></span> <span data-ttu-id="fbff4-109">部分安裝程式存取函式需要 SQL 查詢字串來查詢資料庫。</span><span class="sxs-lookup"><span data-stu-id="fbff4-109">Some of the installer access functions require SQL query strings for querying the database.</span></span> <span data-ttu-id="fbff4-110">查詢必須遵守安裝程式 [SQL 語法](sql-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="fbff4-110">Queries must adhere to the installer [SQL syntax](sql-syntax.md).</span></span>

<span data-ttu-id="fbff4-111">本主題依類別列出安裝程式資料庫存取功能。</span><span class="sxs-lookup"><span data-stu-id="fbff4-111">This topic lists the installer database access functions by category.</span></span>

## <a name="general-database-access-functions"></a><span data-ttu-id="fbff4-112">一般資料庫存取函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-112">General Database Access Functions</span></span>



| <span data-ttu-id="fbff4-113">函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-113">Function</span></span>                                                             | <span data-ttu-id="fbff4-114">描述</span><span class="sxs-lookup"><span data-stu-id="fbff4-114">Description</span></span>                                                                             |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="fbff4-115">**MsiDatabaseCommit**</span><span class="sxs-lookup"><span data-stu-id="fbff4-115">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)                       | <span data-ttu-id="fbff4-116">認可對資料庫所做的變更。</span><span class="sxs-lookup"><span data-stu-id="fbff4-116">Commits changes to a database.</span></span>                                                          |
| [<span data-ttu-id="fbff4-117">**MsiDatabaseGetPrimaryKeys**</span><span class="sxs-lookup"><span data-stu-id="fbff4-117">**MsiDatabaseGetPrimaryKeys**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa)       | <span data-ttu-id="fbff4-118">傳回所有主鍵資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbff4-118">Returns the names of all the primary key columns.</span></span>                                       |
| [<span data-ttu-id="fbff4-119">**MsiDatabaseIsTablePersistent**</span><span class="sxs-lookup"><span data-stu-id="fbff4-119">**MsiDatabaseIsTablePersistent**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta) | <span data-ttu-id="fbff4-120">傳回描述資料表狀態的列舉。</span><span class="sxs-lookup"><span data-stu-id="fbff4-120">Returns an enumeration describing the state of a table.</span></span>                                 |
| [<span data-ttu-id="fbff4-121">**MsiDatabaseOpenView**</span><span class="sxs-lookup"><span data-stu-id="fbff4-121">**MsiDatabaseOpenView**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)                   | <span data-ttu-id="fbff4-122">準備資料庫查詢並建立 view 物件。</span><span class="sxs-lookup"><span data-stu-id="fbff4-122">Prepares a database query and creates a view object.</span></span>                                    |
| [<span data-ttu-id="fbff4-123">**MsiGetActiveDatabase**</span><span class="sxs-lookup"><span data-stu-id="fbff4-123">**MsiGetActiveDatabase**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)                 | <span data-ttu-id="fbff4-124">傳回安裝的使用中資料庫。</span><span class="sxs-lookup"><span data-stu-id="fbff4-124">Returns the active database for the installation.</span></span>                                       |
| [<span data-ttu-id="fbff4-125">**MsiViewGetColumnInfo**</span><span class="sxs-lookup"><span data-stu-id="fbff4-125">**MsiViewGetColumnInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)                 | <span data-ttu-id="fbff4-126">傳回資料行名稱或定義。</span><span class="sxs-lookup"><span data-stu-id="fbff4-126">Returns column names or definitions.</span></span>                                                    |
| [<span data-ttu-id="fbff4-127">**MsiOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="fbff4-127">**MsiOpenDatabase**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)                           | <span data-ttu-id="fbff4-128">開啟資料庫檔案以進行資料存取。</span><span class="sxs-lookup"><span data-stu-id="fbff4-128">Opens a database file for data access.</span></span>                                                  |
| [<span data-ttu-id="fbff4-129">**MsiViewClose**</span><span class="sxs-lookup"><span data-stu-id="fbff4-129">**MsiViewClose**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)                                 | <span data-ttu-id="fbff4-130">釋放已執行之視圖的結果集。</span><span class="sxs-lookup"><span data-stu-id="fbff4-130">Releases the result set for an executed view.</span></span>                                           |
| [<span data-ttu-id="fbff4-131">**MsiViewExecute**</span><span class="sxs-lookup"><span data-stu-id="fbff4-131">**MsiViewExecute**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)                             | <span data-ttu-id="fbff4-132">執行 view 查詢並提供所需的參數。</span><span class="sxs-lookup"><span data-stu-id="fbff4-132">Executes the view query and supplies required parameters.</span></span>                               |
| [<span data-ttu-id="fbff4-133">**MsiViewFetch**</span><span class="sxs-lookup"><span data-stu-id="fbff4-133">**MsiViewFetch**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)                                 | <span data-ttu-id="fbff4-134">從 view 中提取下一個順序記錄。</span><span class="sxs-lookup"><span data-stu-id="fbff4-134">Fetches the next sequential record from the view.</span></span>                                       |
| [<span data-ttu-id="fbff4-135">**MsiViewGetError**</span><span class="sxs-lookup"><span data-stu-id="fbff4-135">**MsiViewGetError**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)                           | <span data-ttu-id="fbff4-136">傳回在 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 函式中發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="fbff4-136">Returns the error that occurred in the [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) function.</span></span> |
| [<span data-ttu-id="fbff4-137">**MsiViewModify**</span><span class="sxs-lookup"><span data-stu-id="fbff4-137">**MsiViewModify**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)                               | <span data-ttu-id="fbff4-138">更新提取的記錄。</span><span class="sxs-lookup"><span data-stu-id="fbff4-138">Updates a fetched record.</span></span>                                                               |



 

## <a name="database-management-functions"></a><span data-ttu-id="fbff4-139">資料庫管理函數</span><span class="sxs-lookup"><span data-stu-id="fbff4-139">Database Management Functions</span></span>



| <span data-ttu-id="fbff4-140">函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-140">Function</span></span>                                                               | <span data-ttu-id="fbff4-141">描述</span><span class="sxs-lookup"><span data-stu-id="fbff4-141">Description</span></span>                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="fbff4-142">**MsiCreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="fbff4-142">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) | <span data-ttu-id="fbff4-143">建立現有轉換的摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="fbff4-143">Creates summary information for an existing transform.</span></span>           |
| [<span data-ttu-id="fbff4-144">**MsiDatabaseApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="fbff4-144">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)         | <span data-ttu-id="fbff4-145">將轉換套用至資料庫。</span><span class="sxs-lookup"><span data-stu-id="fbff4-145">Applies a transform to a database.</span></span>                               |
| [<span data-ttu-id="fbff4-146">**MsiDatabaseExport**</span><span class="sxs-lookup"><span data-stu-id="fbff4-146">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)                         | <span data-ttu-id="fbff4-147">從開啟的資料庫將資料表匯出到文字封存檔案。</span><span class="sxs-lookup"><span data-stu-id="fbff4-147">Exports a table from an open database to a text archive file.</span></span>    |
| [<span data-ttu-id="fbff4-148">**MsiDatabaseGenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="fbff4-148">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)   | <span data-ttu-id="fbff4-149">產生兩個資料庫之間差異的轉換檔案。</span><span class="sxs-lookup"><span data-stu-id="fbff4-149">Generates a transform file of differences between two databases.</span></span> |
| [<span data-ttu-id="fbff4-150">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="fbff4-150">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)                         | <span data-ttu-id="fbff4-151">將安裝程式的文字封存資料表匯入至開啟的資料庫。</span><span class="sxs-lookup"><span data-stu-id="fbff4-151">Imports an installer text archive table into an open database.</span></span>   |
| [<span data-ttu-id="fbff4-152">**MsiDatabaseMerge**</span><span class="sxs-lookup"><span data-stu-id="fbff4-152">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)                           | <span data-ttu-id="fbff4-153">將兩個資料庫合併在一起。</span><span class="sxs-lookup"><span data-stu-id="fbff4-153">Merges two databases together.</span></span>                                   |
| [<span data-ttu-id="fbff4-154">**MsiGetDatabaseState**</span><span class="sxs-lookup"><span data-stu-id="fbff4-154">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)                     | <span data-ttu-id="fbff4-155">傳回資料庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="fbff4-155">Returns the state of the database.</span></span>                               |



 

## <a name="record-processing-functions"></a><span data-ttu-id="fbff4-156">記錄處理函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-156">Record Processing Functions</span></span>



| <span data-ttu-id="fbff4-157">函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-157">Function</span></span>                                                 | <span data-ttu-id="fbff4-158">描述</span><span class="sxs-lookup"><span data-stu-id="fbff4-158">Description</span></span>                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="fbff4-159">**MsiCreateRecord**</span><span class="sxs-lookup"><span data-stu-id="fbff4-159">**MsiCreateRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)               | <span data-ttu-id="fbff4-160">使用指定的欄位數目來建立新的記錄物件。</span><span class="sxs-lookup"><span data-stu-id="fbff4-160">Creates new record object with specified number of fields.</span></span>      |
| [<span data-ttu-id="fbff4-161">**MsiFormatRecord**</span><span class="sxs-lookup"><span data-stu-id="fbff4-161">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)               | <span data-ttu-id="fbff4-162">使用格式字串來格式化記錄欄位資料和屬性。</span><span class="sxs-lookup"><span data-stu-id="fbff4-162">Formats record field data and properties using a format string.</span></span> |
| [<span data-ttu-id="fbff4-163">**MsiRecordClearData**</span><span class="sxs-lookup"><span data-stu-id="fbff4-163">**MsiRecordClearData**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)         | <span data-ttu-id="fbff4-164">將記錄中的所有欄位設定為 null。</span><span class="sxs-lookup"><span data-stu-id="fbff4-164">Sets all fields in a record to null.</span></span>                            |
| [<span data-ttu-id="fbff4-165">**MsiRecordDataSize**</span><span class="sxs-lookup"><span data-stu-id="fbff4-165">**MsiRecordDataSize**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize)           | <span data-ttu-id="fbff4-166">傳回記錄欄位的長度。</span><span class="sxs-lookup"><span data-stu-id="fbff4-166">Returns the length of a record field.</span></span>                           |
| [<span data-ttu-id="fbff4-167">**MsiRecordGetFieldCount**</span><span class="sxs-lookup"><span data-stu-id="fbff4-167">**MsiRecordGetFieldCount**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) | <span data-ttu-id="fbff4-168">傳回記錄中的欄位數。</span><span class="sxs-lookup"><span data-stu-id="fbff4-168">Returns the number of fields in a record.</span></span>                       |
| [<span data-ttu-id="fbff4-169">**MsiRecordGetInteger**</span><span class="sxs-lookup"><span data-stu-id="fbff4-169">**MsiRecordGetInteger**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)       | <span data-ttu-id="fbff4-170">從記錄欄位傳回整數值。</span><span class="sxs-lookup"><span data-stu-id="fbff4-170">Returns the integer value from a record field.</span></span>                  |
| [<span data-ttu-id="fbff4-171">**MsiRecordGetString**</span><span class="sxs-lookup"><span data-stu-id="fbff4-171">**MsiRecordGetString**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)         | <span data-ttu-id="fbff4-172">傳回記錄欄位的字串值。</span><span class="sxs-lookup"><span data-stu-id="fbff4-172">Returns the string value of a record field.</span></span>                     |
| [<span data-ttu-id="fbff4-173">**MsiRecordIsNull**</span><span class="sxs-lookup"><span data-stu-id="fbff4-173">**MsiRecordIsNull**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)               | <span data-ttu-id="fbff4-174">報告記錄欄位是否為 null。</span><span class="sxs-lookup"><span data-stu-id="fbff4-174">Reports whether a record field is null.</span></span>                         |
| [<span data-ttu-id="fbff4-175">**MsiRecordReadStream**</span><span class="sxs-lookup"><span data-stu-id="fbff4-175">**MsiRecordReadStream**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)       | <span data-ttu-id="fbff4-176">從記錄資料流程欄位將位元組讀入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fbff4-176">Reads bytes from a record stream field into a buffer.</span></span>           |
| [<span data-ttu-id="fbff4-177">**MsiRecordSetInteger**</span><span class="sxs-lookup"><span data-stu-id="fbff4-177">**MsiRecordSetInteger**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)       | <span data-ttu-id="fbff4-178">將記錄欄位設定為整數位段。</span><span class="sxs-lookup"><span data-stu-id="fbff4-178">Sets a record field to an integer field.</span></span>                        |
| [<span data-ttu-id="fbff4-179">**MsiRecordSetStream**</span><span class="sxs-lookup"><span data-stu-id="fbff4-179">**MsiRecordSetStream**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)         | <span data-ttu-id="fbff4-180">從檔案設定記錄資料流程欄位。</span><span class="sxs-lookup"><span data-stu-id="fbff4-180">Sets a record stream field from a file.</span></span>                         |
| [<span data-ttu-id="fbff4-181">**MsiRecordSetString**</span><span class="sxs-lookup"><span data-stu-id="fbff4-181">**MsiRecordSetString**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)         | <span data-ttu-id="fbff4-182">將字串複製到指定的欄位。</span><span class="sxs-lookup"><span data-stu-id="fbff4-182">Copies a string into the designated field.</span></span>                      |



 

## <a name="summary-information-property-functions"></a><span data-ttu-id="fbff4-183">摘要資訊屬性函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-183">Summary Information Property Functions</span></span>



| <span data-ttu-id="fbff4-184">函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-184">Function</span></span>                                                                 | <span data-ttu-id="fbff4-185">描述</span><span class="sxs-lookup"><span data-stu-id="fbff4-185">Description</span></span>                                                            |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="fbff4-186">**MsiGetSummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="fbff4-186">**MsiGetSummaryInformation**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)             | <span data-ttu-id="fbff4-187">取得安裝程式資料庫之摘要資訊資料流程的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fbff4-187">Obtains handle to summary information stream of installer database.</span></span>    |
| [<span data-ttu-id="fbff4-188">**MsiSummaryInfoGetProperty**</span><span class="sxs-lookup"><span data-stu-id="fbff4-188">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)           | <span data-ttu-id="fbff4-189">從摘要資訊取得單一屬性。</span><span class="sxs-lookup"><span data-stu-id="fbff4-189">Gets a single property from the summary information.</span></span>                   |
| [<span data-ttu-id="fbff4-190">**MsiSummaryInfoGetPropertyCount**</span><span class="sxs-lookup"><span data-stu-id="fbff4-190">**MsiSummaryInfoGetPropertyCount**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) | <span data-ttu-id="fbff4-191">傳回摘要資訊資料流程中的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="fbff4-191">Returns number of properties in the summary information stream.</span></span>        |
| [<span data-ttu-id="fbff4-192">**MsiSummaryInfoPersist**</span><span class="sxs-lookup"><span data-stu-id="fbff4-192">**MsiSummaryInfoPersist**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist)                   | <span data-ttu-id="fbff4-193">將已變更的摘要資訊寫回摘要資訊串流。</span><span class="sxs-lookup"><span data-stu-id="fbff4-193">Writes changed summary information back to summary information stream.</span></span> |
| [<span data-ttu-id="fbff4-194">**MsiSummaryInfoSetProperty**</span><span class="sxs-lookup"><span data-stu-id="fbff4-194">**MsiSummaryInfoSetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)           | <span data-ttu-id="fbff4-195">設定單一摘要資訊屬性。</span><span class="sxs-lookup"><span data-stu-id="fbff4-195">Sets a single summary information property.</span></span>                            |



 

## <a name="installer-state-access-functions"></a><span data-ttu-id="fbff4-196">安裝程式狀態存取函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-196">Installer State Access Functions</span></span>



| <span data-ttu-id="fbff4-197">函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-197">Function</span></span>                                               | <span data-ttu-id="fbff4-198">描述</span><span class="sxs-lookup"><span data-stu-id="fbff4-198">Description</span></span>                                                 |
|--------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="fbff4-199">**MsiGetLanguage**</span><span class="sxs-lookup"><span data-stu-id="fbff4-199">**MsiGetLanguage**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)               | <span data-ttu-id="fbff4-200">傳回目前安裝的數位語言。</span><span class="sxs-lookup"><span data-stu-id="fbff4-200">Returns the numeric language of the current installation.</span></span>   |
| [<span data-ttu-id="fbff4-201">**MsiGetLastErrorRecord**</span><span class="sxs-lookup"><span data-stu-id="fbff4-201">**MsiGetLastErrorRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetlasterrorrecord) | <span data-ttu-id="fbff4-202">傳回上次傳回給呼叫進程的錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="fbff4-202">Returns error record last returned for the calling process.</span></span> |
| [<span data-ttu-id="fbff4-203">**MsiGetMode**</span><span class="sxs-lookup"><span data-stu-id="fbff4-203">**MsiGetMode**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)                       | <span data-ttu-id="fbff4-204">傳回其中一個布林值內部安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="fbff4-204">Returns one of the Boolean internal installation states.</span></span>    |
| [<span data-ttu-id="fbff4-205">**MsiGetProperty**</span><span class="sxs-lookup"><span data-stu-id="fbff4-205">**MsiGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)               | <span data-ttu-id="fbff4-206">取得安裝程式屬性的值。</span><span class="sxs-lookup"><span data-stu-id="fbff4-206">Gets the value of an installer property.</span></span>                    |
| [<span data-ttu-id="fbff4-207">**MsiSetProperty**</span><span class="sxs-lookup"><span data-stu-id="fbff4-207">**MsiSetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)               | <span data-ttu-id="fbff4-208">設定安裝屬性的值。</span><span class="sxs-lookup"><span data-stu-id="fbff4-208">Sets the value of an installation property.</span></span>                 |
| [<span data-ttu-id="fbff4-209">**MsiSetMode**</span><span class="sxs-lookup"><span data-stu-id="fbff4-209">**MsiSetMode**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)                       | <span data-ttu-id="fbff4-210">設定內部引擎布林狀態。</span><span class="sxs-lookup"><span data-stu-id="fbff4-210">Sets an internal engine Boolean state.</span></span>                      |



 

## <a name="installer-action-functions"></a><span data-ttu-id="fbff4-211">安裝程式動作函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-211">Installer Action Functions</span></span>



| <span data-ttu-id="fbff4-212">函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-212">Function</span></span>                                             | <span data-ttu-id="fbff4-213">描述</span><span class="sxs-lookup"><span data-stu-id="fbff4-213">Description</span></span>                                                               |
|------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="fbff4-214">**MsiDoAction**</span><span class="sxs-lookup"><span data-stu-id="fbff4-214">**MsiDoAction**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)                   | <span data-ttu-id="fbff4-215">執行內建動作、自訂動作或使用者介面 wizard 動作。</span><span class="sxs-lookup"><span data-stu-id="fbff4-215">Executes built-in action, custom action, or user-interface wizard action.</span></span> |
| [<span data-ttu-id="fbff4-216">**MsiEvaluateCondition**</span><span class="sxs-lookup"><span data-stu-id="fbff4-216">**MsiEvaluateCondition**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) | <span data-ttu-id="fbff4-217">評估包含屬性名稱和值的條件運算式。</span><span class="sxs-lookup"><span data-stu-id="fbff4-217">Evaluates a conditional expression containing property names and values.</span></span>  |
| [<span data-ttu-id="fbff4-218">**MsiProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="fbff4-218">**MsiProcessMessage**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)       | <span data-ttu-id="fbff4-219">將錯誤記錄傳送至安裝程式進行處理。</span><span class="sxs-lookup"><span data-stu-id="fbff4-219">Sends an error record to the installer for processing.</span></span>                    |
| [<span data-ttu-id="fbff4-220">**MsiSequence**</span><span class="sxs-lookup"><span data-stu-id="fbff4-220">**MsiSequence**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)                   | <span data-ttu-id="fbff4-221">執行動作順序。</span><span class="sxs-lookup"><span data-stu-id="fbff4-221">Executes an action sequence.</span></span>                                              |



 

## <a name="installer-location-functions"></a><span data-ttu-id="fbff4-222">安裝程式位置函數</span><span class="sxs-lookup"><span data-stu-id="fbff4-222">Installer Location Functions</span></span>



| <span data-ttu-id="fbff4-223">函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-223">Function</span></span>                                     | <span data-ttu-id="fbff4-224">描述</span><span class="sxs-lookup"><span data-stu-id="fbff4-224">Description</span></span>                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="fbff4-225">**MsiGetSourcePath**</span><span class="sxs-lookup"><span data-stu-id="fbff4-225">**MsiGetSourcePath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha) | <span data-ttu-id="fbff4-226">傳回目錄資料表中資料夾的完整來源路徑。</span><span class="sxs-lookup"><span data-stu-id="fbff4-226">Returns the full source path for a folder in the Directory table.</span></span> |
| [<span data-ttu-id="fbff4-227">**MsiGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="fbff4-227">**MsiGetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) | <span data-ttu-id="fbff4-228">傳回目錄資料表中資料夾的完整目標路徑。</span><span class="sxs-lookup"><span data-stu-id="fbff4-228">Returns the full target path for a folder in the Directory table.</span></span> |
| [<span data-ttu-id="fbff4-229">**MsiSetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="fbff4-229">**MsiSetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) | <span data-ttu-id="fbff4-230">設定目錄資料表中資料夾的完整目標路徑。</span><span class="sxs-lookup"><span data-stu-id="fbff4-230">Sets the full target path for a folder in the Directory table.</span></span>    |



 

## <a name="installer-selection-functions"></a><span data-ttu-id="fbff4-231">安裝程式選取功能</span><span class="sxs-lookup"><span data-stu-id="fbff4-231">Installer Selection Functions</span></span>



| <span data-ttu-id="fbff4-232">函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-232">Function</span></span>                                                     | <span data-ttu-id="fbff4-233">描述</span><span class="sxs-lookup"><span data-stu-id="fbff4-233">Description</span></span>                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="fbff4-234">**MsiEnumComponentCosts**</span><span class="sxs-lookup"><span data-stu-id="fbff4-234">**MsiEnumComponentCosts**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienumcomponentcostsa)       | <span data-ttu-id="fbff4-235">列舉安裝元件所需的磁碟空間（每個磁片磁碟機）。</span><span class="sxs-lookup"><span data-stu-id="fbff4-235">Enumerates the disk-space per drive required to install a component.</span></span> |
| [<span data-ttu-id="fbff4-236">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="fbff4-236">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)         | <span data-ttu-id="fbff4-237">取得元件的狀態。</span><span class="sxs-lookup"><span data-stu-id="fbff4-237">Obtains the state of a component.</span></span>                                    |
| [<span data-ttu-id="fbff4-238">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="fbff4-238">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)               | <span data-ttu-id="fbff4-239">傳回功能所需的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="fbff4-239">Returns the disk space required by a feature.</span></span>                        |
| [<span data-ttu-id="fbff4-240">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="fbff4-240">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)             | <span data-ttu-id="fbff4-241">取得功能的狀態。</span><span class="sxs-lookup"><span data-stu-id="fbff4-241">Gets the state of a feature.</span></span>                                         |
| [<span data-ttu-id="fbff4-242">**MsiGetFeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="fbff4-242">**MsiGetFeatureValidStates**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) | <span data-ttu-id="fbff4-243">傳回有效的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="fbff4-243">Returns a valid installation state.</span></span>                                  |
| [<span data-ttu-id="fbff4-244">**MsiSetComponentState**</span><span class="sxs-lookup"><span data-stu-id="fbff4-244">**MsiSetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)         | <span data-ttu-id="fbff4-245">將元件設定為指定的狀態。</span><span class="sxs-lookup"><span data-stu-id="fbff4-245">Sets a component to the specified state.</span></span>                             |
| [<span data-ttu-id="fbff4-246">**MsiSetFeatureAttributes**</span><span class="sxs-lookup"><span data-stu-id="fbff4-246">**MsiSetFeatureAttributes**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa)   | <span data-ttu-id="fbff4-247">在執行時間修改功能的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="fbff4-247">Modifies the default attributes of a feature at run time.</span></span>            |
| [<span data-ttu-id="fbff4-248">**MsiSetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="fbff4-248">**MsiSetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)             | <span data-ttu-id="fbff4-249">將功能設定為指定的狀態。</span><span class="sxs-lookup"><span data-stu-id="fbff4-249">Sets a feature to a specified state.</span></span>                                 |
| [<span data-ttu-id="fbff4-250">**MsiSetInstallLevel**</span><span class="sxs-lookup"><span data-stu-id="fbff4-250">**MsiSetInstallLevel**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)             | <span data-ttu-id="fbff4-251">設定完整產品安裝的安裝層級。</span><span class="sxs-lookup"><span data-stu-id="fbff4-251">Sets the installation level of a full product installation.</span></span>          |
| [<span data-ttu-id="fbff4-252">**MsiVerifyDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="fbff4-252">**MsiVerifyDiskSpace**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)             | <span data-ttu-id="fbff4-253">檢查是否有足夠的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="fbff4-253">Checks for sufficient disk space.</span></span>                                    |



 

## <a name="user-interface-functions"></a><span data-ttu-id="fbff4-254">消費者介面函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-254">User Interface Functions</span></span>



| <span data-ttu-id="fbff4-255">函式</span><span class="sxs-lookup"><span data-stu-id="fbff4-255">Function</span></span>                                           | <span data-ttu-id="fbff4-256">描述</span><span class="sxs-lookup"><span data-stu-id="fbff4-256">Description</span></span>                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="fbff4-257">**MsiEnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="fbff4-257">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)   | <span data-ttu-id="fbff4-258">啟用使用者介面的預覽模式。</span><span class="sxs-lookup"><span data-stu-id="fbff4-258">Enables preview mode of the user interface.</span></span>                             |
| [<span data-ttu-id="fbff4-259">**MsiPreviewBillboard**</span><span class="sxs-lookup"><span data-stu-id="fbff4-259">**MsiPreviewBillboard**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) | <span data-ttu-id="fbff4-260">在顯示的對話方塊中顯示具有主控制項的佈告欄。</span><span class="sxs-lookup"><span data-stu-id="fbff4-260">Displays a billboard with the host control in the displayed dialog box.</span></span> |
| [<span data-ttu-id="fbff4-261">**MsiPreviewDialog**</span><span class="sxs-lookup"><span data-stu-id="fbff4-261">**MsiPreviewDialog**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)       | <span data-ttu-id="fbff4-262">將對話方塊顯示為非模式和非使用中。</span><span class="sxs-lookup"><span data-stu-id="fbff4-262">Displays a dialog box as modeless and inactive.</span></span>                         |



 

<span data-ttu-id="fbff4-263">所有函數都支援 ANSI 和 Unicode 呼叫。</span><span class="sxs-lookup"><span data-stu-id="fbff4-263">All functions support both ANSI and Unicode calls.</span></span> <span data-ttu-id="fbff4-264">若要使用這些函式，請包含 MsiQuery，並連結至 .Msi。</span><span class="sxs-lookup"><span data-stu-id="fbff4-264">To use these functions, include MsiQuery.h and link with Msi.lib.</span></span>

## <a name="installation-functions"></a><span data-ttu-id="fbff4-265">安裝功能</span><span class="sxs-lookup"><span data-stu-id="fbff4-265">Installation Functions</span></span>

<span data-ttu-id="fbff4-266">除了上面所列的資料庫存取函式之外，您還可以使用 [安裝程式函數參考](installer-function-reference.md) 一節中所列的安裝程式函數，來建立應用程式的安裝封裝。</span><span class="sxs-lookup"><span data-stu-id="fbff4-266">In addition to the database access functions listed above, you create an installation package for an application by using the installer functions listed in the [Installer Function Reference](installer-function-reference.md) section.</span></span>

 

 



