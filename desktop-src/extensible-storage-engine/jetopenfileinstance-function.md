---
description: 深入瞭解： JetOpenFileInstance 函數
title: JetOpenFileInstance 函式
TOCTitle: JetOpenFileInstance Function
ms:assetid: 44af9549-77ef-48f4-8580-507f7199f281
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269238(v=EXCHG.10)
ms:contentKeyID: 32765540
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileInstanceA
- JetOpenFileInstanceW
- JetOpenFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6065914fcd5b03d8c8b05996d57331a474ad7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998004"
---
# <a name="jetopenfileinstance-function"></a><span data-ttu-id="2bb74-103">JetOpenFileInstance 函式</span><span class="sxs-lookup"><span data-stu-id="2bb74-103">JetOpenFileInstance Function</span></span>


<span data-ttu-id="2bb74-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2bb74-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfileinstance-function"></a><span data-ttu-id="2bb74-105">JetOpenFileInstance 函式</span><span class="sxs-lookup"><span data-stu-id="2bb74-105">JetOpenFileInstance Function</span></span>

<span data-ttu-id="2bb74-106">**JetOpenFileInstance** 函式會開啟連接的資料庫、資料庫修補檔或作用中實例的交易記錄檔，以執行串流模糊備份。</span><span class="sxs-lookup"><span data-stu-id="2bb74-106">The **JetOpenFileInstance** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="2bb74-107">之後可以使用 [JetReadFileInstance](./jetreadfileinstance-function.md)，透過傳回的控制碼讀取這些檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="2bb74-107">The data from these files can subsequently be read through the returned handle using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span> <span data-ttu-id="2bb74-108">傳回的控制碼必須使用 [JetCloseFileInstance](./jetclosefileinstance-function.md)來關閉。</span><span class="sxs-lookup"><span data-stu-id="2bb74-108">The returned handle must be closed using [JetCloseFileInstance](./jetclosefileinstance-function.md).</span></span> <span data-ttu-id="2bb74-109">實例的外部備份必須先前已使用 [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)起始。</span><span class="sxs-lookup"><span data-stu-id="2bb74-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).</span></span>

<span data-ttu-id="2bb74-110">**Windows xp：**  **JetOpenFileInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="2bb74-110">**Windows XP:**  **JetOpenFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOpenFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="2bb74-111">參數</span><span class="sxs-lookup"><span data-stu-id="2bb74-111">Parameters</span></span>

<span data-ttu-id="2bb74-112">*實例*</span><span class="sxs-lookup"><span data-stu-id="2bb74-112">*instance*</span></span>

<span data-ttu-id="2bb74-113">此呼叫所要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="2bb74-113">The instance to use for this call.</span></span>

<span data-ttu-id="2bb74-114">針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="2bb74-114">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="2bb74-115">在此情況下，這種全域實例的使用是隱含的。</span><span class="sxs-lookup"><span data-stu-id="2bb74-115">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="2bb74-116">若為 Windows XP 和更新版本，則只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變體 (Windows 2000 相容性模式) 只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="2bb74-116">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="2bb74-117">否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。</span><span class="sxs-lookup"><span data-stu-id="2bb74-117">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="2bb74-118">*szFileName*</span><span class="sxs-lookup"><span data-stu-id="2bb74-118">*szFileName*</span></span>

<span data-ttu-id="2bb74-119">連接的資料庫、資料庫修補檔或由讀取以進行備份之實例所管理的交易記錄檔的相對或絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="2bb74-119">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that is read for backup.</span></span>

<span data-ttu-id="2bb74-120">*phfFile*</span><span class="sxs-lookup"><span data-stu-id="2bb74-120">*phfFile*</span></span>

<span data-ttu-id="2bb74-121">輸出緩衝區的指標，此緩衝區會接收要讀取之檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2bb74-121">Pointer to the output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="2bb74-122">*pulFileSizeLow*</span><span class="sxs-lookup"><span data-stu-id="2bb74-122">*pulFileSizeLow*</span></span>

<span data-ttu-id="2bb74-123">輸出緩衝區的指標，此緩衝區會接收最不重要的檔案大小32位。</span><span class="sxs-lookup"><span data-stu-id="2bb74-123">Pointer to the output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="2bb74-124">*pulFileSizeHigh*</span><span class="sxs-lookup"><span data-stu-id="2bb74-124">*pulFileSizeHigh*</span></span>

<span data-ttu-id="2bb74-125">輸出緩衝區的指標，此緩衝區會接收檔案大小最大的32位。</span><span class="sxs-lookup"><span data-stu-id="2bb74-125">Pointer to the output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="2bb74-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="2bb74-126">Return Value</span></span>

<span data-ttu-id="2bb74-127">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="2bb74-127">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2bb74-128">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="2bb74-128">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2bb74-129">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2bb74-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="2bb74-130">Description</span><span class="sxs-lookup"><span data-stu-id="2bb74-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bb74-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2bb74-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2bb74-132">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="2bb74-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb74-133">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="2bb74-133">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="2bb74-134">作業失敗，因為目前的外部備份已被 <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="2bb74-134">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="2bb74-135">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2bb74-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb74-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="2bb74-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="2bb74-137">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="2bb74-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb74-138">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="2bb74-138">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="2bb74-139">作業失敗，因為它無法開啟要求的檔案，因為發生共用違規或許可權不足。</span><span class="sxs-lookup"><span data-stu-id="2bb74-139">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb74-140">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="2bb74-140">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="2bb74-141">作業失敗，因為它無法開啟要求的檔案，因為在指定的路徑中找不到該檔案。</span><span class="sxs-lookup"><span data-stu-id="2bb74-141">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="2bb74-142">此錯誤只會由 Windows 2000 傳回。</span><span class="sxs-lookup"><span data-stu-id="2bb74-142">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb74-143">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="2bb74-143">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="2bb74-144">備份作業失敗，因為它的呼叫順序不是。</span><span class="sxs-lookup"><span data-stu-id="2bb74-144">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb74-145">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="2bb74-145">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="2bb74-146">因為找不到指定的路徑，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="2bb74-146">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb74-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="2bb74-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="2bb74-148">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="2bb74-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="2bb74-149">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2bb74-149">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb74-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2bb74-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2bb74-151">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="2bb74-151">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="2bb74-152">在下列情況下， <strong>JetOpenFileInstance</strong> 可能會發生：</span><span class="sxs-lookup"><span data-stu-id="2bb74-152">This can happen for <strong>JetOpenFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="2bb74-153">指定的實例控制碼 (Windows XP 和更新版本) 無效。</span><span class="sxs-lookup"><span data-stu-id="2bb74-153">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="2bb74-154">指定的 filename 參數為 Null 或 (Windows XP 和更新版本) 的長度為零的字串。</span><span class="sxs-lookup"><span data-stu-id="2bb74-154">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb74-155">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="2bb74-155">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="2bb74-156">無法開啟要求的檔案進行備份，因為找不到該檔案。</span><span class="sxs-lookup"><span data-stu-id="2bb74-156">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="2bb74-157">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2bb74-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb74-158">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="2bb74-158">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="2bb74-159">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="2bb74-159">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb74-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="2bb74-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="2bb74-161">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="2bb74-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb74-162">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="2bb74-162">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="2bb74-163">作業失敗，因為無法配置足夠的記憶體來完成。</span><span class="sxs-lookup"><span data-stu-id="2bb74-163">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="2bb74-164">如果嘗試在先前使用<strong>JetOpenFileInstance</strong>開啟的檔案已由<a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>關閉之前開啟另一個檔案， <strong>JetOpenFileInstance</strong>會傳回 JET_errOutOfMemory。</span><span class="sxs-lookup"><span data-stu-id="2bb74-164"><strong>JetOpenFileInstance</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFileInstance</strong> has been closed by <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>.</span></span> <span data-ttu-id="2bb74-165">目前只支援一個未處理的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="2bb74-165">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb74-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="2bb74-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="2bb74-167">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="2bb74-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb74-168">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="2bb74-168">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="2bb74-169">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="2bb74-169">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb74-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="2bb74-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="2bb74-171">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="2bb74-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2bb74-172">成功時，會傳回所要求檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2bb74-172">On success, a handle to the requested file is returned.</span></span> <span data-ttu-id="2bb74-173">如果是資料庫檔案的控制碼，則會為該資料庫檔案準備好進行串流備份，這可能會在與資料庫檔案相同的位置中建立資料庫修補檔案。</span><span class="sxs-lookup"><span data-stu-id="2bb74-173">If the handle is for a database file, that database file will be prepared for a streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="2bb74-174">資料庫修補檔案與資料庫檔案的路徑和檔案名完全相同，但有。PAT 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="2bb74-174">The database patch file has the exact same path and filename as the database file but with a .PAT extension.</span></span> <span data-ttu-id="2bb74-175">也會傳回檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="2bb74-175">The size of the file will also be returned.</span></span>

<span data-ttu-id="2bb74-176">失敗時，輸出緩衝區的狀態將會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="2bb74-176">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="2bb74-177">可能會在磁片上暫時建立資料庫修補檔案，而且可能會刪除修補檔案位置上的任何現有檔案。</span><span class="sxs-lookup"><span data-stu-id="2bb74-177">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="2bb74-178">失敗會導致整個實例的整個備份進程取消。</span><span class="sxs-lookup"><span data-stu-id="2bb74-178">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="2bb74-179">在 Windows XP 和更新版本中，如果在呼叫時嘗試備份未附加至實例的資料庫，將不會取消備份。</span><span class="sxs-lookup"><span data-stu-id="2bb74-179">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="2bb74-180">**警告**  基於安全性理由，請務必注意， **JetOpenFileInstance** 不會驗證所要求的檔案路徑是否與針對該實例所備份的檔案集合相關聯。</span><span class="sxs-lookup"><span data-stu-id="2bb74-180">**Warning**  For security reasons, it is important to note that **JetOpenFileInstance** does not verify that the requested file path is associated with the set of files that are backed up for the instance.</span></span> <span data-ttu-id="2bb74-181">如此一來，您就可以使用此函式來存取任何可由目前線程的安全性內容開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="2bb74-181">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="2bb74-182">應用程式必須將傳遞給此函式的路徑限制為已知的良好檔案路徑集，否則可能會洩漏資訊攻擊。</span><span class="sxs-lookup"><span data-stu-id="2bb74-182">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2bb74-183">備註</span><span class="sxs-lookup"><span data-stu-id="2bb74-183">Remarks</span></span>

<span data-ttu-id="2bb74-184">必須要有控制碼和檔案大小輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2bb74-184">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="2bb74-185">如果不存在，引擎將會損毀，因為輸出緩衝區參數未經過驗證。</span><span class="sxs-lookup"><span data-stu-id="2bb74-185">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="2bb74-186">目前，每次只能開啟一個檔案進行備份。</span><span class="sxs-lookup"><span data-stu-id="2bb74-186">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="2bb74-187">**JetOpenFileInstance** 不會在開啟要求的檔案之前判斷提示備份許可權。</span><span class="sxs-lookup"><span data-stu-id="2bb74-187">**JetOpenFileInstance** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="2bb74-188">此函式所報告之檔案的大小，可能不符合磁片上的檔案大小。</span><span class="sxs-lookup"><span data-stu-id="2bb74-188">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="2bb74-189">在 Windows XP 和更新版本中，額外的資訊可能會附加到資料庫檔案，資料庫引擎會在還原作業期間使用該檔案。</span><span class="sxs-lookup"><span data-stu-id="2bb74-189">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="2bb74-190">因此，應用程式應該只依賴 **JetOpenFileInstance** 傳回的檔案大小，或 [JetReadFileInstance](./jetreadfileinstance-function.md)所傳回之資料的實際位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2bb74-190">As such, the application should only rely on the file size returned by **JetOpenFileInstance** or on the actual number of bytes of data returned by [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="2bb74-191">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bb74-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bb74-192"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="2bb74-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb74-193">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="2bb74-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb74-194"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="2bb74-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb74-195">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="2bb74-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb74-196"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="2bb74-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb74-197">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="2bb74-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb74-198"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="2bb74-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb74-199">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="2bb74-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bb74-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2bb74-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb74-201">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="2bb74-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bb74-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2bb74-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2bb74-203">實作為 <strong>JetOpenFileInstanceW</strong> (Unicode) 和 <strong>JetOpenFileInstanceA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="2bb74-203">Implemented as <strong>JetOpenFileInstanceW</strong> (Unicode) and <strong>JetOpenFileInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2bb74-204">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bb74-204">See Also</span></span>

[<span data-ttu-id="2bb74-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2bb74-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2bb74-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="2bb74-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="2bb74-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="2bb74-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="2bb74-208">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="2bb74-208">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="2bb74-209">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="2bb74-209">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="2bb74-210">JetCloseFileInstance</span><span class="sxs-lookup"><span data-stu-id="2bb74-210">JetCloseFileInstance</span></span>](./jetclosefileinstance-function.md)  
[<span data-ttu-id="2bb74-211">JetGetAttachInfoInstance</span><span class="sxs-lookup"><span data-stu-id="2bb74-211">JetGetAttachInfoInstance</span></span>](./jetgetattachinfoinstance-function.md)  
[<span data-ttu-id="2bb74-212">JetGetLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="2bb74-212">JetGetLogInfoInstance</span></span>](./jetgetloginfoinstance-function.md)  
[<span data-ttu-id="2bb74-213">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="2bb74-213">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="2bb74-214">JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="2bb74-214">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="2bb74-215">JetTruncateLogInstance</span><span class="sxs-lookup"><span data-stu-id="2bb74-215">JetTruncateLogInstance</span></span>](./jettruncateloginstance-function.md)
