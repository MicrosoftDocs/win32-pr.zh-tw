---
description: 深入瞭解： JetOpenFile 函數
title: JetOpenFile 函式
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2996ffc46e2f6b37cdfec12cd4ee2fc62efa188a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972369"
---
# <a name="jetopenfile-function"></a><span data-ttu-id="8c338-103">JetOpenFile 函式</span><span class="sxs-lookup"><span data-stu-id="8c338-103">JetOpenFile Function</span></span>


<span data-ttu-id="8c338-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8c338-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfile-function"></a><span data-ttu-id="8c338-105">JetOpenFile 函式</span><span class="sxs-lookup"><span data-stu-id="8c338-105">JetOpenFile Function</span></span>

<span data-ttu-id="8c338-106">**JetOpenFile** 函式會開啟連接的資料庫、資料庫修補檔或作用中實例的交易記錄檔，以執行串流模糊備份。</span><span class="sxs-lookup"><span data-stu-id="8c338-106">The **JetOpenFile** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="8c338-107">之後可以使用 [JetReadFile](./jetreadfile-function.md)，透過傳回的控制碼讀取這些檔案中的資料。</span><span class="sxs-lookup"><span data-stu-id="8c338-107">The data from these files can subsequently be read through the returned handle using [JetReadFile](./jetreadfile-function.md).</span></span> <span data-ttu-id="8c338-108">傳回的控制碼必須使用 [JetCloseFile](./jetclosefile-function.md)來關閉。</span><span class="sxs-lookup"><span data-stu-id="8c338-108">The returned handle must be closed using [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="8c338-109">實例的外部備份必須先前已使用 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)起始。</span><span class="sxs-lookup"><span data-stu-id="8c338-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="8c338-110">參數</span><span class="sxs-lookup"><span data-stu-id="8c338-110">Parameters</span></span>

<span data-ttu-id="8c338-111">*szFileName*</span><span class="sxs-lookup"><span data-stu-id="8c338-111">*szFileName*</span></span>

<span data-ttu-id="8c338-112">附加的資料庫、資料庫修補檔或由將讀取以進行備份之實例管理的交易記錄檔的相對或絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="8c338-112">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that will be read for backup.</span></span>

<span data-ttu-id="8c338-113">*phfFile*</span><span class="sxs-lookup"><span data-stu-id="8c338-113">*phfFile*</span></span>

<span data-ttu-id="8c338-114">輸出緩衝區，接收要讀取之檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8c338-114">The output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="8c338-115">*pulFileSizeLow*</span><span class="sxs-lookup"><span data-stu-id="8c338-115">*pulFileSizeLow*</span></span>

<span data-ttu-id="8c338-116">輸出緩衝區，此緩衝區會接收最不重要的檔案大小32位。</span><span class="sxs-lookup"><span data-stu-id="8c338-116">The output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="8c338-117">*pulFileSizeHigh*</span><span class="sxs-lookup"><span data-stu-id="8c338-117">*pulFileSizeHigh*</span></span>

<span data-ttu-id="8c338-118">輸出緩衝區，可接收檔案大小最大的32位。</span><span class="sxs-lookup"><span data-stu-id="8c338-118">The output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="8c338-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c338-119">Return Value</span></span>

<span data-ttu-id="8c338-120">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="8c338-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8c338-121">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="8c338-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c338-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8c338-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="8c338-123">Description</span><span class="sxs-lookup"><span data-stu-id="8c338-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c338-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8c338-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8c338-125">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="8c338-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c338-126">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="8c338-126">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="8c338-127">作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="8c338-127">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="8c338-128">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c338-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c338-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8c338-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8c338-130">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="8c338-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c338-131">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="8c338-131">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="8c338-132">作業失敗，因為它無法開啟要求的檔案，因為發生共用違規或許可權不足。</span><span class="sxs-lookup"><span data-stu-id="8c338-132">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c338-133">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="8c338-133">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="8c338-134">作業失敗，因為它無法開啟要求的檔案，因為在指定的路徑中找不到該檔案。</span><span class="sxs-lookup"><span data-stu-id="8c338-134">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="8c338-135">此錯誤只會由 Windows 2000 傳回。</span><span class="sxs-lookup"><span data-stu-id="8c338-135">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c338-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8c338-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8c338-137">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="8c338-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="8c338-138">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c338-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c338-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="8c338-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="8c338-140">備份作業失敗，因為它的呼叫順序不是。</span><span class="sxs-lookup"><span data-stu-id="8c338-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c338-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="8c338-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="8c338-142">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="8c338-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="8c338-143">在下列情況下， <strong>JetOpenFile</strong> 可能會發生：</span><span class="sxs-lookup"><span data-stu-id="8c338-143">This can happen for <strong>JetOpenFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="8c338-144">指定的實例控制碼 (Windows XP 和更新版本) 無效。</span><span class="sxs-lookup"><span data-stu-id="8c338-144">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="8c338-145">指定的 filename 參數為 Null 或 (Windows XP 和更新版本) 的長度為零的字串。</span><span class="sxs-lookup"><span data-stu-id="8c338-145">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c338-146">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="8c338-146">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="8c338-147">因為找不到指定的路徑，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="8c338-147">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c338-148">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="8c338-148">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="8c338-149">無法開啟要求的檔案進行備份，因為找不到該檔案。</span><span class="sxs-lookup"><span data-stu-id="8c338-149">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="8c338-150">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c338-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c338-151">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="8c338-151">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="8c338-152">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="8c338-152">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c338-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8c338-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8c338-154">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="8c338-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c338-155">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="8c338-155">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="8c338-156">作業失敗，因為無法配置足夠的記憶體來完成。</span><span class="sxs-lookup"><span data-stu-id="8c338-156">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="8c338-157">如果嘗試在先前使用<strong>JetOpenFile</strong>開啟的檔案已由<a href="gg294127(v=exchg.10).md">JetCloseFile</a>關閉之前開啟另一個檔案， <strong>JetOpenFile</strong>會傳回 JET_errOutOfMemory。</span><span class="sxs-lookup"><span data-stu-id="8c338-157"><strong>JetOpenFile</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFile</strong> has been closed by <a href="gg294127(v=exchg.10).md">JetCloseFile</a>.</span></span> <span data-ttu-id="8c338-158">目前只支援一個未處理的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="8c338-158">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c338-159">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="8c338-159">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="8c338-160">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="8c338-160">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c338-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8c338-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8c338-162">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="8c338-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span> <span data-ttu-id="8c338-163">JET_errRestoreInProgress 無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="8c338-163">JET_errRestoreInProgress It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8c338-164">成功時，將會傳回所要求檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8c338-164">On success, a handle to the requested file will be returned.</span></span> <span data-ttu-id="8c338-165">如果是資料庫檔案的控制碼，該資料庫檔案將會準備進行串流備份，這可能會導致在與資料庫檔案相同的位置中建立資料庫修補檔案。</span><span class="sxs-lookup"><span data-stu-id="8c338-165">If the handle is for a database file, that database file will be prepared for streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="8c338-166">資料庫修補檔案的路徑和檔案名與資料庫檔案完全相同，但具有。PAT 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="8c338-166">The database patch file has the exact same path and filename as the database file, but has a .PAT extension.</span></span> <span data-ttu-id="8c338-167">也會傳回檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="8c338-167">The size of the file will also be returned.</span></span>

<span data-ttu-id="8c338-168">失敗時，輸出緩衝區的狀態將會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="8c338-168">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="8c338-169">可能會在磁片上暫時建立資料庫修補檔案，而且可能會刪除修補檔案位置上的任何現有檔案。</span><span class="sxs-lookup"><span data-stu-id="8c338-169">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="8c338-170">失敗會導致整個實例的整個備份進程取消。</span><span class="sxs-lookup"><span data-stu-id="8c338-170">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="8c338-171">在 Windows XP 和更新版本中，如果在呼叫時嘗試備份未附加至實例的資料庫，將不會取消備份。</span><span class="sxs-lookup"><span data-stu-id="8c338-171">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="8c338-172">**警告**  基於安全性理由，請務必注意， **JetOpenFile** 不會驗證所要求的檔案路徑是否與應該針對該實例備份的檔案集合相關聯。</span><span class="sxs-lookup"><span data-stu-id="8c338-172">**Warning**  For security reasons, it is important to note that **JetOpenFile** does not verify that the requested file path is associated with the set of files that should be backed up for the instance.</span></span> <span data-ttu-id="8c338-173">如此一來，您就可以使用此函式來存取任何可由目前線程的安全性內容開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="8c338-173">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="8c338-174">應用程式必須將傳遞給此函式的路徑限制為已知的良好檔案路徑集，否則可能會洩漏資訊攻擊。</span><span class="sxs-lookup"><span data-stu-id="8c338-174">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8c338-175">備註</span><span class="sxs-lookup"><span data-stu-id="8c338-175">Remarks</span></span>

<span data-ttu-id="8c338-176">必須要有控制碼和檔案大小輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8c338-176">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="8c338-177">如果不存在，引擎將會損毀，因為輸出緩衝區參數未經過驗證。</span><span class="sxs-lookup"><span data-stu-id="8c338-177">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="8c338-178">目前，每次只能開啟一個檔案進行備份。</span><span class="sxs-lookup"><span data-stu-id="8c338-178">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="8c338-179">**JetOpenFile** 不會在開啟要求的檔案之前判斷提示備份許可權。</span><span class="sxs-lookup"><span data-stu-id="8c338-179">**JetOpenFile** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="8c338-180">此函式所報告之檔案的大小，可能不符合磁片上的檔案大小。</span><span class="sxs-lookup"><span data-stu-id="8c338-180">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="8c338-181">在 Windows XP 和更新版本中，額外的資訊可能會附加到資料庫檔案，資料庫引擎會在還原作業期間使用該檔案。</span><span class="sxs-lookup"><span data-stu-id="8c338-181">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="8c338-182">因此，應用程式應該只依賴 **JetOpenFile** 傳回的檔案大小，或 [JetReadFile](./jetreadfile-function.md)所傳回之資料的實際位元組數目。</span><span class="sxs-lookup"><span data-stu-id="8c338-182">As such, the application should only rely on the file size returned by **JetOpenFile** or on the actual number of bytes of data returned by [JetReadFile](./jetreadfile-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="8c338-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c338-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c338-184"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="8c338-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8c338-185">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="8c338-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c338-186"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="8c338-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8c338-187">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="8c338-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c338-188"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="8c338-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8c338-189">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="8c338-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c338-190"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="8c338-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8c338-191">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="8c338-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c338-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8c338-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8c338-193">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="8c338-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c338-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8c338-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8c338-195">實作為 <strong>JetOpenFileW</strong> (Unicode) 和 <strong>JetOpenFileA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="8c338-195">Implemented as <strong>JetOpenFileW</strong> (Unicode) and <strong>JetOpenFileA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8c338-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c338-196">See Also</span></span>

[<span data-ttu-id="8c338-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8c338-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8c338-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="8c338-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="8c338-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="8c338-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="8c338-200">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="8c338-200">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="8c338-201">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="8c338-201">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="8c338-202">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="8c338-202">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="8c338-203">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="8c338-203">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="8c338-204">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="8c338-204">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="8c338-205">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="8c338-205">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="8c338-206">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="8c338-206">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="8c338-207">JetStopService</span><span class="sxs-lookup"><span data-stu-id="8c338-207">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="8c338-208">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="8c338-208">JetTruncateLog</span></span>](./jettruncatelog-function.md)
