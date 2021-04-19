---
description: 深入瞭解： JetBackup 函數
title: JetBackup 函式
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f225053df36ebe98bc890a8e036d84ee31b6b154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975526"
---
# <a name="jetbackup-function"></a><span data-ttu-id="5a2d6-103">JetBackup 函式</span><span class="sxs-lookup"><span data-stu-id="5a2d6-103">JetBackup Function</span></span>


<span data-ttu-id="5a2d6-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5a2d6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackup-function"></a><span data-ttu-id="5a2d6-105">JetBackup 函式</span><span class="sxs-lookup"><span data-stu-id="5a2d6-105">JetBackup Function</span></span>

<span data-ttu-id="5a2d6-106">當資料庫在線上時， **JetBackup** 函數會建立資料庫的備份。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-106">The **JetBackup** function creates a backup of the database while the database is online.</span></span> <span data-ttu-id="5a2d6-107">這項功能主要是為了與 Windows 2000 及舊版的資料庫引擎回溯相容，其中只允許一個資料庫的實例。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="5a2d6-108">在此情況下，作用中的實例是已備份的實例。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-108">In this case, the active instance is the instance that is backed up.</span></span>

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="5a2d6-109">參數</span><span class="sxs-lookup"><span data-stu-id="5a2d6-109">Parameters</span></span>

<span data-ttu-id="5a2d6-110">*szBackupPath*</span><span class="sxs-lookup"><span data-stu-id="5a2d6-110">*szBackupPath*</span></span>

<span data-ttu-id="5a2d6-111">儲存備份的目錄。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-111">The directory where the backup is stored.</span></span> <span data-ttu-id="5a2d6-112">如果備份路徑為 Null，則函式會盡可能截斷記錄。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-112">If the backup path is NULL, the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="5a2d6-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5a2d6-113">*grbit*</span></span>

<span data-ttu-id="5a2d6-114">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-114">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a2d6-115">值</span><span class="sxs-lookup"><span data-stu-id="5a2d6-115">Value</span></span></p></th>
<th><p><span data-ttu-id="5a2d6-116">意義</span><span class="sxs-lookup"><span data-stu-id="5a2d6-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-117">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="5a2d6-117">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-118">建立資料庫的完整備份。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-118">Creates a full backup of the database.</span></span> <span data-ttu-id="5a2d6-119">這可在新備份失敗時，將現有的備份保留在相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a2d6-120">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="5a2d6-120">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-121">建立增量備份，而不是完整備份。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-121">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="5a2d6-122">這表示只會備份自上次完整或增量備份之後的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-122">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5a2d6-123">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="5a2d6-123">*pfnStatus*</span></span>

<span data-ttu-id="5a2d6-124">[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)回呼函式的指標，它會提供有關備份作業進度的通知資訊。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-124">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="5a2d6-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a2d6-125">Return Value</span></span>

<span data-ttu-id="5a2d6-126">函數會傳回其中一個 [JET_ERR](./jet-err.md) 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-126">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="5a2d6-127">以下是最常傳回的。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-127">The following are the most commonly returned.</span></span> <span data-ttu-id="5a2d6-128"> (如需此 API 的完整錯誤清單，請參閱可延伸的 [儲存引擎錯誤碼](./extensible-storage-engine-error-codes.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="5a2d6-128">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5a2d6-129">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5a2d6-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="5a2d6-130">Description</span><span class="sxs-lookup"><span data-stu-id="5a2d6-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5a2d6-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-132">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a2d6-133">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="5a2d6-133">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-134">相同實例的備份已經在進行中。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-134">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="5a2d6-135">不允許多個備份。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-135">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-136">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="5a2d6-136">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-137">實例在初始化時尚未準備好進行備份。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-137">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a2d6-138">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5a2d6-138">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-139">作業無法完成，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-139">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5a2d6-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-141">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-141">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5a2d6-142"><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-142"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a2d6-143">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="5a2d6-143">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-144">如果迴圈記錄開啟，則不允許增量備份。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-144">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-145">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="5a2d6-145">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-146">指定的選項無效。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-146">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a2d6-147">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="5a2d6-147">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-148">傳遞至 API 的參數無效。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-148">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-149">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="5a2d6-149">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-150">目的地路徑不存在。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-150">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a2d6-151">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="5a2d6-151">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-152">實例正在執行，但未記錄。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-152">The instance is running without logging.</span></span> <span data-ttu-id="5a2d6-153">不允許備份。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-153">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-154">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="5a2d6-154">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-155">記錄檔發生總和檢查碼驗證錯誤。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-155">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a2d6-156">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="5a2d6-156">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-157">因為發生未預期的錯誤，所以實例的記錄是暫時性的或永久停用。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-157">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5a2d6-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-159">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-159">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a2d6-160">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="5a2d6-160">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-161">資料庫頁面上發生總和檢查碼驗證錯誤。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-161">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5a2d6-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-163">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a2d6-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="5a2d6-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-165">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="5a2d6-166"><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-166"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5a2d6-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5a2d6-168">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-168">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5a2d6-169">如果函式成功，則還原到備份時所需的所有檔案都會包含在備份目錄中。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-169">If the function succeeds, all the files needed for a restore up to the moment of the backup will be contained in the backup directory.</span></span> <span data-ttu-id="5a2d6-170">如果這是完整備份，檔案將會是資料庫檔案，以及將資料庫帶入一致狀態所需的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-170">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="5a2d6-171">如果這是增量備份，則只會將記錄檔新增至目錄，但 (資料庫和) 記錄檔的現有檔案，以及新的記錄檔，將可進行還原，讓資料庫回到備份開始時的狀態。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-171">If this is an incremental backup, only log files will be added to the directories, but the already existing files (databases and log files), together with the new log files, will be able to be restored to bring the database back to the state it was in at the moment that the backup began.</span></span>

<span data-ttu-id="5a2d6-172">備份的副作用是，不再需要的記錄檔將會被截斷。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-172">As a side effect of the backup, the log files which are no longer needed will be truncated.</span></span>

<span data-ttu-id="5a2d6-173">在相同的時間內，資料庫標頭會在最後一次備份時，以資訊更新。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-173">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="5a2d6-174">如果函式失敗，就不會有備份目錄目的地中的任何檔案，因此不會有任何還原功能。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-174">If the function fails, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="5a2d6-175">在相同的時間內，目前的記錄檔不會被截斷。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-175">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5a2d6-176">備註</span><span class="sxs-lookup"><span data-stu-id="5a2d6-176">Remarks</span></span>

<span data-ttu-id="5a2d6-177">備份的不同步驟將會產生事件記錄檔專案，包括檔案名、記錄截斷，以及備份的最終結果。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-177">The different steps of the backup will have Event Log entries generated, including the file names, the log truncation, and the final result of the backup.</span></span>

<span data-ttu-id="5a2d6-178">只有在執行完整備份之後，才可能進行增量備份。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-178">Incremental backups are possible only after a full backup was taken.</span></span> <span data-ttu-id="5a2d6-179">此外，只有在迴圈記錄關閉時，才可能進行增量備份。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-179">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="5a2d6-180">建議備份目錄不應包含備份中所使用的任何檔案，或先前成功備份所新增的檔案。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-180">It is recommended that the backup directory should not contain any files other than the one used in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="5a2d6-181">除非針對實例設定了參數 *JET_paramCreatePathIfNotExist* ，否則備份目錄應該會存在。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-181">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="5a2d6-182">如需詳細資訊，請參閱 [系統參數](./extensible-storage-engine-system-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-182">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="5a2d6-183">備份也會在記錄檔上，對所有已使用的資料庫頁面進行總和檢查碼驗證，並從 Windows Server 2003 開始。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-183">The backup will do a checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="5a2d6-184">這讓您有機會評估資料庫的健全狀況，即使是在正常作業期間未讀取的頁面也是如此。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-184">This gives an opportunity to estimate the health of the database, even for pages which are not read during normal operations.</span></span> <span data-ttu-id="5a2d6-185">如果遇到任何這類損毀，備份將會失敗。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-185">If any such corruption is encountered, the backup will fail.</span></span>

<span data-ttu-id="5a2d6-186">在備份期間，目前的記錄檔將會完成，並產生新的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-186">During the backup, the current log file will be finished and a new log will be generated.</span></span> <span data-ttu-id="5a2d6-187">如此一來，所有必要的記錄檔都可以複製，因為目前的記錄檔將不會再使用。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-187">This way, all of the necessary log files can be copies, because the current log will not be in use anymore.</span></span>

<span data-ttu-id="5a2d6-188">強烈建議您不要將備份用於引擎層級的備份和還原以外的任何目的。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-188">It is strongly recommended that the backup not be used for any purpose other than the backup and restore at the engine level.</span></span> <span data-ttu-id="5a2d6-189">這可將在備份和還原作業期間發生錯誤的機會降到最低。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-189">This will minimize the chance of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5a2d6-190">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a2d6-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-191"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="5a2d6-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5a2d6-192">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a2d6-193"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="5a2d6-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5a2d6-194">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-195"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="5a2d6-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5a2d6-196">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a2d6-197"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="5a2d6-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5a2d6-198">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a2d6-199"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5a2d6-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5a2d6-200">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-200">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a2d6-201"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5a2d6-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5a2d6-202">實作為 <strong>JetBackupW</strong> (Unicode) 和 <strong>JetBackupA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="5a2d6-202">Implemented as <strong>JetBackupW</strong> (Unicode) and <strong>JetBackupA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5a2d6-203">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a2d6-203">See Also</span></span>

[<span data-ttu-id="5a2d6-204">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="5a2d6-204">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="5a2d6-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5a2d6-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5a2d6-206">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5a2d6-206">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5a2d6-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="5a2d6-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="5a2d6-208">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="5a2d6-208">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="5a2d6-209">JetRestore</span><span class="sxs-lookup"><span data-stu-id="5a2d6-209">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="5a2d6-210">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="5a2d6-210">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="5a2d6-211">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="5a2d6-211">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="5a2d6-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="5a2d6-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="5a2d6-213">系統參數</span><span class="sxs-lookup"><span data-stu-id="5a2d6-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
