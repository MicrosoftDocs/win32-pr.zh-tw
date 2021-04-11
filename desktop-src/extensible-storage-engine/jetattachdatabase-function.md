---
description: 深入瞭解： JetAttachDatabase 函數
title: JetAttachDatabase 函式
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5968fe7906ace720dad3f94e278f37d992710d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191129"
---
# <a name="jetattachdatabase-function"></a><span data-ttu-id="4f3f2-103">JetAttachDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="4f3f2-103">JetAttachDatabase Function</span></span>


<span data-ttu-id="4f3f2-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4f3f2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase-function"></a><span data-ttu-id="4f3f2-105">JetAttachDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="4f3f2-105">JetAttachDatabase Function</span></span>

<span data-ttu-id="4f3f2-106">**JetAttachDatabase** 函數會附加資料庫檔案，以便與資料庫實例搭配使用。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-106">The **JetAttachDatabase** function attaches a database file for use with a database instance.</span></span> <span data-ttu-id="4f3f2-107">若要使用資料庫，就必須使用 [JetOpenDatabase](./jetopendatabase-function.md)來開啟它。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="4f3f2-108">參數</span><span class="sxs-lookup"><span data-stu-id="4f3f2-108">Parameters</span></span>

<span data-ttu-id="4f3f2-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="4f3f2-109">*sesid*</span></span>

<span data-ttu-id="4f3f2-110">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="4f3f2-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="4f3f2-111">*szFilename*</span></span>

<span data-ttu-id="4f3f2-112">要附加的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-112">The name of the database to attach.</span></span>

<span data-ttu-id="4f3f2-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="4f3f2-113">*grbit*</span></span>

<span data-ttu-id="4f3f2-114">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-114">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f3f2-115">值</span><span class="sxs-lookup"><span data-stu-id="4f3f2-115">Value</span></span></p></th>
<th><p><span data-ttu-id="4f3f2-116">意義</span><span class="sxs-lookup"><span data-stu-id="4f3f2-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f3f2-117">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="4f3f2-117">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-118">如果已設定 <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> ，將會刪除 Unicode 資料上的所有索引。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-118">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="4f3f2-119">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-119">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f3f2-120">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="4f3f2-120">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-121">無論 <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>的設定為何，都將刪除所有 Unicode 資料的索引。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-121">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="4f3f2-122">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-122">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f3f2-123">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="4f3f2-123">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-124">已過時。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-124">Obsolete.</span></span> <span data-ttu-id="4f3f2-125">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-125">Do not use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f3f2-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="4f3f2-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-127">防止修改資料庫。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="4f3f2-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f3f2-128">Return Value</span></span>

<span data-ttu-id="4f3f2-129">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4f3f2-130">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f3f2-131">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4f3f2-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="4f3f2-132">Description</span><span class="sxs-lookup"><span data-stu-id="4f3f2-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f3f2-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4f3f2-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-134">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f3f2-135">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="4f3f2-135">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-136">在備份期間，不允許附加資料庫。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-136">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f3f2-137">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="4f3f2-137">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-138"><em>SzFilename</em>所指定的資料庫檔案必須是可寫入的。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-138">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="4f3f2-139">不能設定 Read-Only 屬性，而且執行中的進程必須有足夠的許可權可寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-139">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f3f2-140">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="4f3f2-140">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-141">資料庫檔案已經由另一個進程開啟。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-141">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f3f2-142">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="4f3f2-142">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-143"><em>SzFilename</em>中提供了不正確路徑。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-143">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="4f3f2-144"><em>szFilename</em> 必須為非 Null，並參考有效的路徑。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-144"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f3f2-145">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4f3f2-145">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-146">已由不同的會話附加資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-146">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f3f2-147">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="4f3f2-147">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-148">資料庫引擎無法開啟資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-148">The database engine cannot open the database file.</span></span> <span data-ttu-id="4f3f2-149">檔案可能由另一個進程使用中，或呼叫者可能沒有足夠的許可權可以開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-149">The file may be in use by another process or the caller may not have sufficient privileges to open the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f3f2-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="4f3f2-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-151"><em>SzFilename</em>中提供的檔案不存在。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-151">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f3f2-152">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="4f3f2-152">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-153">主要索引發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-153">There is an error with the primary index.</span></span> <span data-ttu-id="4f3f2-154">這可能是因為物理損毀 (例如磁片或記憶體損毀) 。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-154">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="4f3f2-155">當附加資料庫上次修改較舊的作業系統，而且主要索引是在具有 Unicode 資料的資料行上時，也可能會傳回它。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-155">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="4f3f2-156">如需 Unicode 資料之索引的詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-156">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f3f2-157">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="4f3f2-157">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-158">次要索引發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-158">There is an error with a secondary index.</span></span> <span data-ttu-id="4f3f2-159">這可能是因為物理損毀 (例如磁片或記憶體損毀) 。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-159">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="4f3f2-160">當附加資料庫上次修改于較舊的作業系統上，而且次要索引是在具有 Unicode 資料的資料行上時，也可能會傳回它。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-160">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="4f3f2-161">如需 Unicode 資料之索引的詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-161">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="4f3f2-162">使用下列命令，以離線公用程式重新整理資料庫時，會完整重建次要索引： <strong>esentutl-d</strong>。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-162">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f3f2-163">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="4f3f2-163">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-164">每個實例只能附加有限數量的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-164">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="4f3f2-165">限制目前為每個實例七個資料庫。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-165">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f3f2-166">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="4f3f2-166">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="4f3f2-167">非嚴重警告，指出此會話已附加資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-167">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="4f3f2-168">備註</span><span class="sxs-lookup"><span data-stu-id="4f3f2-168">Remarks</span></span>

<span data-ttu-id="4f3f2-169">呼叫 **JetAttachDatabase** 相當於呼叫 [JetAttachDatabase2](./jetattachdatabase2-function.md) 並傳遞零值，這表示 *cpgDatabaseSizeMax* 參數沒有限制。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-169">Calling **JetAttachDatabase** is equivalent to calling [JetAttachDatabase2](./jetattachdatabase2-function.md) and passing a value of zero, meaning there is no limit, for the *cpgDatabaseSizeMax* parameter.</span></span>

<span data-ttu-id="4f3f2-170">附加可寫入的資料庫 (也就是，如果未在 *grbit* 參數中指定 JET_bitDbReadOnly) 將會以獨佔方式在作業系統層級開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-170">Attaching a writable database (that is, if JET_bitDbReadOnly was not specified in the *grbit* parameter) will open the file exclusively at the operating system level.</span></span> <span data-ttu-id="4f3f2-171">沒有其他進程可以開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-171">No other process will be able open the file.</span></span> <span data-ttu-id="4f3f2-172">多個進程可以在唯讀模式中開啟單一資料庫，以附加單一資料庫。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-172">It is possible for multiple processes to attach a single database by opening them in read-only mode.</span></span>

<span data-ttu-id="4f3f2-173">使用 [JetDetachDatabase](./jetdetachdatabase-function.md) 或 [JetDetachDatabase2](./jetdetachdatabase2-function.md)卸離資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-173">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="4f3f2-174">索引檢查參數</span><span class="sxs-lookup"><span data-stu-id="4f3f2-174">Index-checking parameters</span></span>

<span data-ttu-id="4f3f2-175">不同版本的 Windows 會以不同的方式將 Unicode 文字標準化。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-175">Different versions of Windows normalize Unicode text in different ways.</span></span> <span data-ttu-id="4f3f2-176">這表示在某個 Windows 版本下建立的索引可能無法在其他版本上運作。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-176">That means indexes built under one version of Windows may not work on other versions.</span></span>

<span data-ttu-id="4f3f2-177">在 Windows Server 2003 之前，當作業系統版本變更 (包括) 安裝 Service Pack 時，每個 Unicode 資料的索引都處於可能已損毀的狀態。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-177">Prior to Windows Server 2003, when the operating system version changed (including installation of a Service Pack), every index over Unicode data was in a potentially corrupt state.</span></span>

<span data-ttu-id="4f3f2-178">在 Windows Server 2003 和更新版本中建立的索引會以建立它們的 Unicode 正規化版本標示。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-178">Indexes created in Windows Server 2003 and later are flagged with the version of Unicode normalization with which they were built.</span></span> <span data-ttu-id="4f3f2-179">較舊的索引不含任何版本資訊。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-179">Older indexes contain no version information.</span></span> <span data-ttu-id="4f3f2-180">大部分的 Unicode 正規化變更都包含新增字元，先前未定義的程式碼點現在已定義並以不同的方式進行標準化。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-180">Most Unicode normalization changes consist of adding new characters, code points which were previously undefined are now defined and normalize differently.</span></span> <span data-ttu-id="4f3f2-181">因此，如果二進位資料儲存在 Unicode 資料行中，則在定義新的程式碼點時，它會以不同的方式進行標準化。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-181">Thus, if binary data is stored in a Unicode column, it will normalize differently as new code points are defined.</span></span>

<span data-ttu-id="4f3f2-182">從 Windows Server 2003，ESE 資料庫引擎會追蹤包含未定義程式碼點的 Unicode 索引項目。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-182">As of Windows Server 2003, the ESE database engine tracks Unicode index entries that contain undefined code points.</span></span> <span data-ttu-id="4f3f2-183">當定義的 Unicode 字元集合變更時，可以使用這些方法來修正索引。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-183">These can be used to fix an index when the set of defined Unicode characters changes.</span></span>

<span data-ttu-id="4f3f2-184">這些參數可控制當 ESE 資料庫引擎連接到最後在不同的作業系統組建下使用的資料庫時，會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-184">These parameters control what happens when the ESE database engine attaches to a database that was last used under a different build of the operating system.</span></span> <span data-ttu-id="4f3f2-185">系統會在資料庫標頭中將作業系統版本加上戳記。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-185">The operating system version is stamped in the database header.</span></span>

<span data-ttu-id="4f3f2-186">如果 [JET_paramEnableIndexChecking](./database-parameters.md) 設定為 **TRUE**，且資料庫包含可能已損毀的索引：</span><span class="sxs-lookup"><span data-stu-id="4f3f2-186">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **TRUE**, and the database contains potentially corrupt indexes:</span></span>

  - <span data-ttu-id="4f3f2-187">如果 *grbit* 包含 JET_bitDbDeleteCorruptIndexes， **JetAttachDatabase** 會刪除可能損毀的索引</span><span class="sxs-lookup"><span data-stu-id="4f3f2-187">**JetAttachDatabase** will delete the potentially corrupt indexes if *grbit* contains JET_bitDbDeleteCorruptIndexes</span></span>

  - <span data-ttu-id="4f3f2-188">如果 *grbit* 不包含 JET_bitDbDeleteCorruptIndexes，且有需要刪除的索引， **JetAttachDatabase** 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-188">**JetAttachDatabase** will return an error if *grbit* does not contain JET_bitDbDeleteCorruptIndexes and there are indexes which need deletion.</span></span>

<span data-ttu-id="4f3f2-189">如果 [JET_paramEnableIndexChecking](./database-parameters.md) 設定為 **FALSE**：</span><span class="sxs-lookup"><span data-stu-id="4f3f2-189">If [JET_paramEnableIndexChecking](./database-parameters.md) is set to **FALSE**:</span></span>

  - <span data-ttu-id="4f3f2-190">**JetAttachDatabase** 會忽略可能損毀的索引，並傳回 JET_errSuccess (假設沒有其他錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-190">**JetAttachDatabase** will ignore potentially corrupt indexes, and return JET_errSuccess (assuming there were no other errors).</span></span>

<span data-ttu-id="4f3f2-191">Windows Server 2003 和更新版本：如果 [JET_paramEnableIndexChecking](./database-parameters.md) 尚未重設，則會使用內部修復表格來修復索引項目。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-191">Windows Server 2003 and later: If [JET_paramEnableIndexChecking](./database-parameters.md) has not been reset, the internal fixup table will be used to fixup index entries.</span></span> <span data-ttu-id="4f3f2-192">這可能無法修正所有索引損毀，但對應用程式而言會是透明的。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-192">This may not fix all index corruptions but will be transparent to the application.</span></span>

<span data-ttu-id="4f3f2-193">如果資料庫附加為唯讀，則無法修正或刪除索引。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-193">If the database was attached as read-only the index cannot be fixed or deleted.</span></span> <span data-ttu-id="4f3f2-194">在此情況下，API 會改為傳回錯誤，例如 JET_errSecondaryIndexCorrupted 或 JET_errPrimaryIndexCorrupted。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-194">In this case, the API will instead return an error, such as JET_errSecondaryIndexCorrupted or JET_errPrimaryIndexCorrupted.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4f3f2-195">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f3f2-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f3f2-196"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="4f3f2-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4f3f2-197">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-197">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f3f2-198"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="4f3f2-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4f3f2-199">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-199">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f3f2-200"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="4f3f2-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4f3f2-201">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f3f2-202"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="4f3f2-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4f3f2-203">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f3f2-204"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4f3f2-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4f3f2-205">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-205">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f3f2-206"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4f3f2-206"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4f3f2-207">實作為 <strong>JetAddColumnW</strong> (Unicode) 和 <strong>JetAddColumnA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="4f3f2-207">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4f3f2-208">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f3f2-208">See Also</span></span>

[<span data-ttu-id="4f3f2-209">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="4f3f2-209">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="4f3f2-210">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4f3f2-210">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4f3f2-211">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4f3f2-211">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4f3f2-212">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4f3f2-212">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4f3f2-213">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4f3f2-213">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4f3f2-214">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="4f3f2-214">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="4f3f2-215">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="4f3f2-215">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="4f3f2-216">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="4f3f2-216">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="4f3f2-217">JetDetachDatabase2</span><span class="sxs-lookup"><span data-stu-id="4f3f2-217">JetDetachDatabase2</span></span>](./jetdetachdatabase2-function.md)  
[<span data-ttu-id="4f3f2-218">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="4f3f2-218">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="4f3f2-219">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="4f3f2-219">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
