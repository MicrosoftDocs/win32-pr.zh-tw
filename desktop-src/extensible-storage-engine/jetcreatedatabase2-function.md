---
description: 深入瞭解： JetCreateDatabase2 函數
title: JetCreateDatabase2 函式
TOCTitle: JetCreateDatabase2 Function
ms:assetid: 267ac69f-49d3-4741-b324-d8510d7a36d3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269208(v=EXCHG.10)
ms:contentKeyID: 32765511
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase2A
- JetCreateDatabase2W
- JetCreateDatabase2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370f88f95a2eb8217dc06124b50c9ed165eb679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998322"
---
# <a name="jetcreatedatabase2-function"></a><span data-ttu-id="4ac89-103">JetCreateDatabase2 函式</span><span class="sxs-lookup"><span data-stu-id="4ac89-103">JetCreateDatabase2 Function</span></span>


<span data-ttu-id="4ac89-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4ac89-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase2-function"></a><span data-ttu-id="4ac89-105">JetCreateDatabase2 函式</span><span class="sxs-lookup"><span data-stu-id="4ac89-105">JetCreateDatabase2 Function</span></span>

<span data-ttu-id="4ac89-106">**JetCreateDatabase2** 函式會建立並附加資料庫檔案，以便與具有指定資料庫大小上限的 ESE 資料庫引擎一起使用。</span><span class="sxs-lookup"><span data-stu-id="4ac89-106">The **JetCreateDatabase2** function creates and attaches a database file to be used with the ESE database engine with a maximum database size specified.</span></span> <span data-ttu-id="4ac89-107">將 *cpgDatabaseSizeMax* 設定為零的呼叫 **JetCreateDatabase2** 等同于呼叫 [JetCreateDatabase](./jetcreatedatabase-function.md) ，並將 *szConnect* 設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="4ac89-107">Calling **JetCreateDatabase2** with *cpgDatabaseSizeMax* set to zero is identical to calling [JetCreateDatabase](./jetcreatedatabase-function.md) with *szConnect* set to NULL.</span></span> <span data-ttu-id="4ac89-108">目前最多可為每個實例建立7個資料庫。</span><span class="sxs-lookup"><span data-stu-id="4ac89-108">Currently up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="4ac89-109">參數</span><span class="sxs-lookup"><span data-stu-id="4ac89-109">Parameters</span></span>

<span data-ttu-id="4ac89-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="4ac89-110">*sesid*</span></span>

<span data-ttu-id="4ac89-111">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="4ac89-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="4ac89-112">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="4ac89-112">*szFilename*</span></span>

<span data-ttu-id="4ac89-113">要建立之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ac89-113">The name of the database to be created.</span></span>

<span data-ttu-id="4ac89-114">*cpgDatabaseSizeMax*</span><span class="sxs-lookup"><span data-stu-id="4ac89-114">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="4ac89-115">資料庫的大小上限（資料庫頁面）。</span><span class="sxs-lookup"><span data-stu-id="4ac89-115">The maximum size, in database pages, for the database.</span></span> <span data-ttu-id="4ac89-116">預設資料庫頁面大小為 4 kb，在建立資料庫之前，您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 加以變更。</span><span class="sxs-lookup"><span data-stu-id="4ac89-116">The default database page size is 4 kilobytes, and can be changed with [JetSetSystemParameter](./jetsetsystemparameter-function.md) prior to creating a database.</span></span>

<span data-ttu-id="4ac89-117">傳遞零表示資料庫引擎沒有強制執行的最大值。</span><span class="sxs-lookup"><span data-stu-id="4ac89-117">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="4ac89-118">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="4ac89-118">*pdbid*</span></span>

<span data-ttu-id="4ac89-119">在成功呼叫時，緩衝區的指標，其中包含資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ac89-119">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="4ac89-120">失敗時，值為未定義。</span><span class="sxs-lookup"><span data-stu-id="4ac89-120">On failure, the value is undefined.</span></span>

<span data-ttu-id="4ac89-121">*grbit*</span><span class="sxs-lookup"><span data-stu-id="4ac89-121">*grbit*</span></span>

<span data-ttu-id="4ac89-122">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="4ac89-122">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ac89-123">值</span><span class="sxs-lookup"><span data-stu-id="4ac89-123">Value</span></span></p></th>
<th><p><span data-ttu-id="4ac89-124">意義</span><span class="sxs-lookup"><span data-stu-id="4ac89-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-125">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="4ac89-125">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="4ac89-126">根據預設，如果呼叫 <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> 或 <strong>JetCreateDatabase2</strong> ，而且資料庫已存在，則 API 呼叫將會失敗，而且不會覆寫原始資料庫。</span><span class="sxs-lookup"><span data-stu-id="4ac89-126">By default, if <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> or <strong>JetCreateDatabase2</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="4ac89-127">JET_bitDbOverwriteExisting 變更這種行為，舊資料庫將會以新的資料庫覆寫。</span><span class="sxs-lookup"><span data-stu-id="4ac89-127">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="4ac89-128">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="4ac89-128">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ac89-129">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="4ac89-129">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="4ac89-130">JET_bitDbRecoveryOff 關閉記錄功能。</span><span class="sxs-lookup"><span data-stu-id="4ac89-130">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="4ac89-131">如此一來，在發生重大事件之後，就無法重新執行記錄檔並將資料庫復原到一致的可用狀態。</span><span class="sxs-lookup"><span data-stu-id="4ac89-131">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-132">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="4ac89-132">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="4ac89-133">設定 JET_bitDbShadowingOff 將會停用部分內部資料庫結構 (遮蔽) 的複製。</span><span class="sxs-lookup"><span data-stu-id="4ac89-133">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="4ac89-134">這些結構的複製是為了復原而完成，因此設定 JET_bitDbShadowingOff 將會移除該復原。</span><span class="sxs-lookup"><span data-stu-id="4ac89-134">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="4ac89-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ac89-135">Return Value</span></span>

<span data-ttu-id="4ac89-136">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="4ac89-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4ac89-137">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="4ac89-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ac89-138">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4ac89-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="4ac89-139">Description</span><span class="sxs-lookup"><span data-stu-id="4ac89-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4ac89-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4ac89-141">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="4ac89-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ac89-142">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="4ac89-142">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="4ac89-143"><em>SzFilename</em>中名為的資料庫已經存在。</span><span class="sxs-lookup"><span data-stu-id="4ac89-143">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="4ac89-144">傳回此錯誤時，就不會附加資料庫。</span><span class="sxs-lookup"><span data-stu-id="4ac89-144">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-145">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="4ac89-145">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="4ac89-146">如果要求獨佔存取權，但無法授與，或是其他會話已獨佔開啟資料庫，則可以傳回。</span><span class="sxs-lookup"><span data-stu-id="4ac89-146">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ac89-147">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="4ac89-147">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="4ac89-148">當 <em>cpgDatabaseSizeMax</em> 大於資料庫中允許的最大頁面數目時傳回。</span><span class="sxs-lookup"><span data-stu-id="4ac89-148">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="4ac89-149">目前的最大值為 2147483646 (0x7ffffffe) 。</span><span class="sxs-lookup"><span data-stu-id="4ac89-149">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-150">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="4ac89-150">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="4ac89-151"><em>SzFilename</em>中提供了不正確路徑。</span><span class="sxs-lookup"><span data-stu-id="4ac89-151">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="4ac89-152"><em>szFilename</em> 必須為非 Null。</span><span class="sxs-lookup"><span data-stu-id="4ac89-152"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="4ac89-153">根據預設， <em>szFilename</em> 必須指向存在的目錄。</span><span class="sxs-lookup"><span data-stu-id="4ac89-153">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="4ac89-154">如果設定 <em>JET_paramCreatePathIfNotExist</em> ，則會建立路徑 (請參閱 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>) 。</span><span class="sxs-lookup"><span data-stu-id="4ac89-154">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ac89-155">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="4ac89-155">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="4ac89-156">指出另一個會話已 (使用 JET_bitDbExclusive) ，以獨佔方式開啟資料庫。</span><span class="sxs-lookup"><span data-stu-id="4ac89-156">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-157">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="4ac89-157">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="4ac89-158">先前尚未附加資料庫 (請參閱 <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>) 。</span><span class="sxs-lookup"><span data-stu-id="4ac89-158">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ac89-159">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4ac89-159">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4ac89-160">已由不同的會話附加資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4ac89-160">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-161">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="4ac89-161">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="4ac89-162">嘗試在交易中建立資料庫。</span><span class="sxs-lookup"><span data-stu-id="4ac89-162">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ac89-163">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="4ac89-163">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="4ac89-164">嘗試開啟的檔案不是有效的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4ac89-164">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-165">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="4ac89-165">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="4ac89-166">嘗試開啟一個以上的資料庫，並已設定 JET_paramOneDatabasePerSession。</span><span class="sxs-lookup"><span data-stu-id="4ac89-166">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="4ac89-167">請參閱 <a href="gg294139(v=exchg.10).md">系統參數</a>。</span><span class="sxs-lookup"><span data-stu-id="4ac89-167">See <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ac89-168">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="4ac89-168">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="4ac89-169">系統資源不足。</span><span class="sxs-lookup"><span data-stu-id="4ac89-169">The system ran low on resources.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-170">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="4ac89-170">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="4ac89-171">每個實例只能附加有限數量的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4ac89-171">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="4ac89-172">限制目前為每個實例七個資料庫。</span><span class="sxs-lookup"><span data-stu-id="4ac89-172">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ac89-173">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="4ac89-173">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="4ac89-174">非嚴重警告，指出此會話已附加資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4ac89-174">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-175">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="4ac89-175">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="4ac89-176">JET_wrnFileOpenReadOnly 指出檔案已附加唯讀，但 <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> 未傳遞 JET_bitDbReadOnly。</span><span class="sxs-lookup"><span data-stu-id="4ac89-176">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="4ac89-177">資料庫仍會以唯讀存取權開啟。</span><span class="sxs-lookup"><span data-stu-id="4ac89-177">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="4ac89-178">備註</span><span class="sxs-lookup"><span data-stu-id="4ac89-178">Remarks</span></span>

<span data-ttu-id="4ac89-179">如果 *szFilename* 中指定的資料庫存在，而且未傳入 JET_BITDBOVERWRITEEXISTING，API 呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="4ac89-179">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="4ac89-180">如果傳入了 JET_bitDbOverwriteExisting，將會先刪除舊的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="4ac89-180">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="4ac89-181">如果 API 建立資料庫檔案，然後遇到另一個錯誤，則會清除並刪除該檔案。</span><span class="sxs-lookup"><span data-stu-id="4ac89-181">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="4ac89-182">**JetCreateDatabase2** 會以隱含方式開啟資料庫。</span><span class="sxs-lookup"><span data-stu-id="4ac89-182">**JetCreateDatabase2** will implicitly open the database.</span></span> <span data-ttu-id="4ac89-183">然後不需要呼叫 [JetOpenDatabase](./jetopendatabase-function.md)。</span><span class="sxs-lookup"><span data-stu-id="4ac89-183">It is not necessary to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="4ac89-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ac89-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-185"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="4ac89-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4ac89-186">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="4ac89-186">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ac89-187"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="4ac89-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4ac89-188">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="4ac89-188">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-189"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="4ac89-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4ac89-190">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="4ac89-190">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ac89-191"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="4ac89-191"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4ac89-192">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="4ac89-192">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ac89-193"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4ac89-193"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4ac89-194">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="4ac89-194">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ac89-195"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4ac89-195"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4ac89-196">實作為 <strong>JetCreateDatabase2W</strong> (Unicode) 和 <strong>JetCreateDatabase2A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="4ac89-196">Implemented as <strong>JetCreateDatabase2W</strong> (Unicode) and <strong>JetCreateDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4ac89-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ac89-197">See Also</span></span>

[<span data-ttu-id="4ac89-198">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="4ac89-198">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="4ac89-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4ac89-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4ac89-200">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="4ac89-200">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="4ac89-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4ac89-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4ac89-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4ac89-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4ac89-203">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="4ac89-203">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="4ac89-204">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="4ac89-204">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="4ac89-205">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="4ac89-205">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="4ac89-206">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="4ac89-206">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="4ac89-207">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="4ac89-207">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="4ac89-208">系統參數</span><span class="sxs-lookup"><span data-stu-id="4ac89-208">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
