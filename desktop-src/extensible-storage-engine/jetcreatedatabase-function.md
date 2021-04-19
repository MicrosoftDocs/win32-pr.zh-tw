---
description: 深入瞭解： JetCreateDatabase 函數
title: JetCreateDatabase 函式
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8fbec76e3b38f9b42c36156b2312a8e77a6b43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974480"
---
# <a name="jetcreatedatabase-function"></a><span data-ttu-id="6154c-103">JetCreateDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="6154c-103">JetCreateDatabase Function</span></span>


<span data-ttu-id="6154c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6154c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatedatabase-function"></a><span data-ttu-id="6154c-105">JetCreateDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="6154c-105">JetCreateDatabase Function</span></span>

<span data-ttu-id="6154c-106">**JetCreateDatabase** 函式會建立和附加資料庫檔案，以搭配 ESE 資料庫引擎使用。</span><span class="sxs-lookup"><span data-stu-id="6154c-106">The **JetCreateDatabase** function creates and attaches a database file to be used with the ESE database engine.</span></span> <span data-ttu-id="6154c-107">將 *cpgDatabaseSizeMax* 設定為零的呼叫 [JetCreateDatabase2](./jetcreatedatabase2-function.md)等同于呼叫 **JetCreateDatabase** ，並將 *szConnect* 設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="6154c-107">Calling [JetCreateDatabase2](./jetcreatedatabase2-function.md) with *cpgDatabaseSizeMax* set to zero is identical to calling **JetCreateDatabase** with *szConnect* set to NULL.</span></span> <span data-ttu-id="6154c-108">目前，每個實例最多可以建立七個資料庫。</span><span class="sxs-lookup"><span data-stu-id="6154c-108">Currently, up to seven databases can be created per instance.</span></span>

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="6154c-109">參數</span><span class="sxs-lookup"><span data-stu-id="6154c-109">Parameters</span></span>

<span data-ttu-id="6154c-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6154c-110">*sesid*</span></span>

<span data-ttu-id="6154c-111">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="6154c-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="6154c-112">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="6154c-112">*szFilename*</span></span>

<span data-ttu-id="6154c-113">要建立之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6154c-113">The name of the database to be created.</span></span>

<span data-ttu-id="6154c-114">*szConnect*</span><span class="sxs-lookup"><span data-stu-id="6154c-114">*szConnect*</span></span>

<span data-ttu-id="6154c-115">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="6154c-115">Reserved for future use.</span></span> <span data-ttu-id="6154c-116">設定為 NULL。</span><span class="sxs-lookup"><span data-stu-id="6154c-116">Set to NULL.</span></span>

<span data-ttu-id="6154c-117">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="6154c-117">*pdbid*</span></span>

<span data-ttu-id="6154c-118">在成功呼叫時，緩衝區的指標，其中包含資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6154c-118">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="6154c-119">失敗時，值為未定義。</span><span class="sxs-lookup"><span data-stu-id="6154c-119">On failure, the value is undefined.</span></span>

<span data-ttu-id="6154c-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6154c-120">*grbit*</span></span>

<span data-ttu-id="6154c-121">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="6154c-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6154c-122">值</span><span class="sxs-lookup"><span data-stu-id="6154c-122">Value</span></span></p></th>
<th><p><span data-ttu-id="6154c-123">意義</span><span class="sxs-lookup"><span data-stu-id="6154c-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6154c-124">JET_bitDbOverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="6154c-124">JET_bitDbOverwriteExisting</span></span></p></td>
<td><p><span data-ttu-id="6154c-125">根據預設，如果呼叫 <strong>JetCreateDatabase</strong> ，而且資料庫已存在，則 API 呼叫將會失敗，而且不會覆寫原始資料庫。</span><span class="sxs-lookup"><span data-stu-id="6154c-125">By default, if <strong>JetCreateDatabase</strong> is called and the database already exists, the API call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="6154c-126">JET_bitDbOverwriteExisting 變更這種行為，舊資料庫將會以新的資料庫覆寫。</span><span class="sxs-lookup"><span data-stu-id="6154c-126">JET_bitDbOverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span> <span data-ttu-id="6154c-127">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="6154c-127">Windows XP and later.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6154c-128">JET_bitDbRecoveryOff</span><span class="sxs-lookup"><span data-stu-id="6154c-128">JET_bitDbRecoveryOff</span></span></p></td>
<td><p><span data-ttu-id="6154c-129">JET_bitDbRecoveryOff 關閉記錄功能。</span><span class="sxs-lookup"><span data-stu-id="6154c-129">JET_bitDbRecoveryOff turns off logging.</span></span> <span data-ttu-id="6154c-130">如此一來，在發生重大事件之後，就無法重新執行記錄檔並將資料庫復原到一致的可用狀態。</span><span class="sxs-lookup"><span data-stu-id="6154c-130">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a catastrophic event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6154c-131">JET_bitDbShadowingOff</span><span class="sxs-lookup"><span data-stu-id="6154c-131">JET_bitDbShadowingOff</span></span></p></td>
<td><p><span data-ttu-id="6154c-132">設定 JET_bitDbShadowingOff 將會停用部分內部資料庫結構 (遮蔽) 的複製。</span><span class="sxs-lookup"><span data-stu-id="6154c-132">Setting JET_bitDbShadowingOff will disable the duplication of some internal database structures (shadowing).</span></span> <span data-ttu-id="6154c-133">這些結構的複製是為了復原而完成，因此設定 JET_bitDbShadowingOff 將會移除該復原。</span><span class="sxs-lookup"><span data-stu-id="6154c-133">The duplication of these structures is done for resiliency, so setting JET_bitDbShadowingOff will remove that resiliency.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6154c-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="6154c-134">Return Value</span></span>

<span data-ttu-id="6154c-135">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="6154c-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6154c-136">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="6154c-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6154c-137">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6154c-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="6154c-138">Description</span><span class="sxs-lookup"><span data-stu-id="6154c-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6154c-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6154c-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6154c-140">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="6154c-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6154c-141">JET_errDatabaseDuplicate</span><span class="sxs-lookup"><span data-stu-id="6154c-141">JET_errDatabaseDuplicate</span></span></p></td>
<td><p><span data-ttu-id="6154c-142"><em>SzFilename</em>中名為的資料庫已經存在。</span><span class="sxs-lookup"><span data-stu-id="6154c-142">The database named in <em>szFilename</em> already exists.</span></span> <span data-ttu-id="6154c-143">傳回此錯誤時，就不會附加資料庫。</span><span class="sxs-lookup"><span data-stu-id="6154c-143">When this error is returned, the database does not get attached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6154c-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="6154c-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="6154c-145">如果要求獨佔存取權，但無法授與，或是其他會話已獨佔開啟資料庫，則可以傳回。</span><span class="sxs-lookup"><span data-stu-id="6154c-145">Can be returned if exclusive access was requested, but could not be granted, or if another session has already opened the database exclusively.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6154c-146">JET_errDatabaseInvalidPages</span><span class="sxs-lookup"><span data-stu-id="6154c-146">JET_errDatabaseInvalidPages</span></span></p></td>
<td><p><span data-ttu-id="6154c-147">當 <em>cpgDatabaseSizeMax</em> 大於資料庫中允許的最大頁面數目時傳回。</span><span class="sxs-lookup"><span data-stu-id="6154c-147">Returned when <em>cpgDatabaseSizeMax</em> is larger than the maximum number of pages allowed in a database.</span></span> <span data-ttu-id="6154c-148">目前的最大值為 2147483646 (0x7ffffffe) 。</span><span class="sxs-lookup"><span data-stu-id="6154c-148">The current maximum is 2147483646 (0x7ffffffe).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6154c-149">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="6154c-149">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="6154c-150"><em>SzFilename</em>中提供了不正確路徑。</span><span class="sxs-lookup"><span data-stu-id="6154c-150">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="6154c-151"><em>szFilename</em> 必須為非 Null。</span><span class="sxs-lookup"><span data-stu-id="6154c-151"><em>szFilename</em> must be non-NULL.</span></span> <span data-ttu-id="6154c-152">根據預設， <em>szFilename</em> 必須指向存在的目錄。</span><span class="sxs-lookup"><span data-stu-id="6154c-152">By default, <em>szFilename</em> must point to a directory that exists.</span></span> <span data-ttu-id="6154c-153">如果設定 <em>JET_paramCreatePathIfNotExist</em> ，則會建立路徑 (請參閱 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>) 。</span><span class="sxs-lookup"><span data-stu-id="6154c-153">The path will be created if <em>JET_paramCreatePathIfNotExist</em> is set (See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6154c-154">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="6154c-154">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="6154c-155">指出另一個會話已 (使用 JET_bitDbExclusive) ，以獨佔方式開啟資料庫。</span><span class="sxs-lookup"><span data-stu-id="6154c-155">Indicates that another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6154c-156">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="6154c-156">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="6154c-157">先前尚未附加資料庫 (請參閱 <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>) 。</span><span class="sxs-lookup"><span data-stu-id="6154c-157">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6154c-158">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6154c-158">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="6154c-159">已由不同的會話附加資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="6154c-159">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6154c-160">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="6154c-160">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="6154c-161">嘗試在交易中建立資料庫。</span><span class="sxs-lookup"><span data-stu-id="6154c-161">An attempt was made to create a database while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6154c-162">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="6154c-162">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="6154c-163">嘗試開啟的檔案不是有效的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="6154c-163">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6154c-164">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="6154c-164">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="6154c-165">嘗試開啟一個以上的資料庫，並已設定 JET_paramOneDatabasePerSession。</span><span class="sxs-lookup"><span data-stu-id="6154c-165">An attempt was made to open more than one database, and JET_paramOneDatabasePerSession was set.</span></span> <span data-ttu-id="6154c-166">請參閱 <a href="gg269337(v=exchg.10).md">資料庫參數</a>。</span><span class="sxs-lookup"><span data-stu-id="6154c-166">See <a href="gg269337(v=exchg.10).md">Database Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6154c-167">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="6154c-167">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="6154c-168">因為無法配置記憶體，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="6154c-168">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6154c-169">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="6154c-169">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="6154c-170">每個實例只能附加有限數量的資料庫。</span><span class="sxs-lookup"><span data-stu-id="6154c-170">Only a finite number of database can be attached per instance.</span></span> <span data-ttu-id="6154c-171">限制目前為每個實例七個資料庫。</span><span class="sxs-lookup"><span data-stu-id="6154c-171">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6154c-172">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="6154c-172">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="6154c-173">非嚴重警告，指出此會話已附加資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="6154c-173">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6154c-174">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="6154c-174">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="6154c-175">JET_wrnFileOpenReadOnly 指出檔案已附加唯讀，但 <strong>JetCreateDatabase</strong> 未傳遞 JET_bitDbReadOnly。</span><span class="sxs-lookup"><span data-stu-id="6154c-175">JET_wrnFileOpenReadOnly indicates that the file was attached read-only, but <strong>JetCreateDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="6154c-176">資料庫仍會以唯讀存取權開啟。</span><span class="sxs-lookup"><span data-stu-id="6154c-176">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="6154c-177">備註</span><span class="sxs-lookup"><span data-stu-id="6154c-177">Remarks</span></span>

<span data-ttu-id="6154c-178">如果 *szFilename* 中指定的資料庫存在，而且未傳入 JET_BITDBOVERWRITEEXISTING，API 呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="6154c-178">If the database specified in *szFilename* exists and JET_bitDbOverwriteExisting was not passed in, the API call will fail.</span></span> <span data-ttu-id="6154c-179">如果傳入了 JET_bitDbOverwriteExisting，將會先刪除舊的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="6154c-179">If JET_bitDbOverwriteExisting was passed in, the old database file will be deleted first.</span></span>

<span data-ttu-id="6154c-180">如果 API 建立資料庫檔案，然後遇到另一個錯誤，則會清除並刪除該檔案。</span><span class="sxs-lookup"><span data-stu-id="6154c-180">If the API creates a database file and then hits another error, it will clean up and delete the file.</span></span>

<span data-ttu-id="6154c-181">**JetCreateDatabase** 會以隱含方式開啟資料庫。</span><span class="sxs-lookup"><span data-stu-id="6154c-181">**JetCreateDatabase** will implicitly open the database.</span></span> <span data-ttu-id="6154c-182">這不一定會再呼叫 [JetOpenDatabase](./jetopendatabase-function.md)。</span><span class="sxs-lookup"><span data-stu-id="6154c-182">It is not necessarily to subsequently call [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="6154c-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="6154c-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6154c-184"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="6154c-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6154c-185">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="6154c-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6154c-186"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="6154c-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6154c-187">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="6154c-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6154c-188"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="6154c-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6154c-189">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="6154c-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6154c-190"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="6154c-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6154c-191">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="6154c-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6154c-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6154c-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6154c-193">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="6154c-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6154c-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="6154c-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="6154c-195">實作為 <strong>JetCreateDatabaseW</strong> (Unicode) 和 <strong>JetCreateDatabaseA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="6154c-195">Implemented as <strong>JetCreateDatabaseW</strong> (Unicode) and <strong>JetCreateDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6154c-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6154c-196">See Also</span></span>

[<span data-ttu-id="6154c-197">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="6154c-197">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="6154c-198">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6154c-198">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6154c-199">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="6154c-199">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="6154c-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="6154c-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="6154c-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6154c-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6154c-202">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="6154c-202">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="6154c-203">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="6154c-203">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="6154c-204">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="6154c-204">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="6154c-205">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="6154c-205">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="6154c-206">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="6154c-206">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="6154c-207">系統參數</span><span class="sxs-lookup"><span data-stu-id="6154c-207">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
