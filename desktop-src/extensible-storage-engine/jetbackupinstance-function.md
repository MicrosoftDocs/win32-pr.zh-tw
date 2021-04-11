---
description: 深入瞭解： JetBackupInstance 函數
title: JetBackupInstance 函式
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fab20676267333ae8f60e4fe4f07d98a8b45e88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112060"
---
# <a name="jetbackupinstance-function"></a><span data-ttu-id="a9f47-103">JetBackupInstance 函式</span><span class="sxs-lookup"><span data-stu-id="a9f47-103">JetBackupInstance Function</span></span>


<span data-ttu-id="a9f47-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a9f47-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackupinstance-function"></a><span data-ttu-id="a9f47-105">JetBackupInstance 函式</span><span class="sxs-lookup"><span data-stu-id="a9f47-105">JetBackupInstance Function</span></span>

<span data-ttu-id="a9f47-106">**JetBackupInstance** 函式會執行實例（包括所有附加的資料庫）至目錄的資料流程備份。</span><span class="sxs-lookup"><span data-stu-id="a9f47-106">The **JetBackupInstance** function performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="a9f47-107">如果引擎支援多個備份方法，這是最簡單且最簡單的封裝函數。</span><span class="sxs-lookup"><span data-stu-id="a9f47-107">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="a9f47-108">**Windows xp： JetBackupInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="a9f47-108">**Windows XP:  JetBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="a9f47-109">參數</span><span class="sxs-lookup"><span data-stu-id="a9f47-109">Parameters</span></span>

<span data-ttu-id="a9f47-110">*實例*</span><span class="sxs-lookup"><span data-stu-id="a9f47-110">*instance*</span></span>

<span data-ttu-id="a9f47-111">要備份之資料庫的實例。</span><span class="sxs-lookup"><span data-stu-id="a9f47-111">The instance of the database to backup.</span></span>

<span data-ttu-id="a9f47-112">*szBackupPath*</span><span class="sxs-lookup"><span data-stu-id="a9f47-112">*szBackupPath*</span></span>

<span data-ttu-id="a9f47-113">儲存備份的目錄。</span><span class="sxs-lookup"><span data-stu-id="a9f47-113">The directory where the backup is stored.</span></span> <span data-ttu-id="a9f47-114">如果備份路徑為 Null，則使用函式會盡可能截斷記錄。</span><span class="sxs-lookup"><span data-stu-id="a9f47-114">If the backup path is NULL to use the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="a9f47-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a9f47-115">*grbit*</span></span>

<span data-ttu-id="a9f47-116">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="a9f47-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9f47-117">值</span><span class="sxs-lookup"><span data-stu-id="a9f47-117">Value</span></span></p></th>
<th><p><span data-ttu-id="a9f47-118">意義</span><span class="sxs-lookup"><span data-stu-id="a9f47-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="a9f47-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="a9f47-120">建立資料庫的完整備份。</span><span class="sxs-lookup"><span data-stu-id="a9f47-120">Creates a full backup of the database.</span></span> <span data-ttu-id="a9f47-121">這可在新備份失敗時，將現有的備份保留在相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="a9f47-121">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f47-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="a9f47-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="a9f47-123">建立增量備份，而不是完整備份。</span><span class="sxs-lookup"><span data-stu-id="a9f47-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="a9f47-124">這表示只會備份自上次完整或增量備份之後所建立的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="a9f47-124">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="a9f47-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="a9f47-126">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="a9f47-126">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9f47-127">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="a9f47-127">*pfnStatus*</span></span>

<span data-ttu-id="a9f47-128">[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)回呼函式的指標，它會提供有關備份作業進度的通知資訊。</span><span class="sxs-lookup"><span data-stu-id="a9f47-128">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="a9f47-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9f47-129">Return Value</span></span>

<span data-ttu-id="a9f47-130">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="a9f47-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a9f47-131">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="a9f47-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9f47-132">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a9f47-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="a9f47-133">Description</span><span class="sxs-lookup"><span data-stu-id="a9f47-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a9f47-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a9f47-135">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="a9f47-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f47-136">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="a9f47-136">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="a9f47-137">相同實例的備份已經在進行中。</span><span class="sxs-lookup"><span data-stu-id="a9f47-137">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="a9f47-138">不允許多個備份。</span><span class="sxs-lookup"><span data-stu-id="a9f47-138">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-139">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="a9f47-139">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="a9f47-140">實例在初始化時尚未準備好進行備份。</span><span class="sxs-lookup"><span data-stu-id="a9f47-140">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f47-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a9f47-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a9f47-142">作業無法完成，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>。</span><span class="sxs-lookup"><span data-stu-id="a9f47-142">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a9f47-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a9f47-144">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="a9f47-144">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a9f47-145"><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="a9f47-145"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f47-146">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="a9f47-146">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="a9f47-147">如果迴圈記錄開啟，則不允許增量備份。</span><span class="sxs-lookup"><span data-stu-id="a9f47-147">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-148">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="a9f47-148">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="a9f47-149">指定的選項無效。</span><span class="sxs-lookup"><span data-stu-id="a9f47-149">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f47-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a9f47-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a9f47-151">傳遞至 API 的參數無效。</span><span class="sxs-lookup"><span data-stu-id="a9f47-151">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="a9f47-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="a9f47-153">目的地路徑不存在。</span><span class="sxs-lookup"><span data-stu-id="a9f47-153">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f47-154">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="a9f47-154">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="a9f47-155">實例正在執行，但未記錄。</span><span class="sxs-lookup"><span data-stu-id="a9f47-155">The instance is running without logging.</span></span> <span data-ttu-id="a9f47-156">不允許備份。</span><span class="sxs-lookup"><span data-stu-id="a9f47-156">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-157">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="a9f47-157">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="a9f47-158">記錄檔發生總和檢查碼驗證錯誤。</span><span class="sxs-lookup"><span data-stu-id="a9f47-158">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f47-159">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="a9f47-159">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="a9f47-160">因為發生未預期的錯誤，所以實例的記錄是暫時性的或永久停用。</span><span class="sxs-lookup"><span data-stu-id="a9f47-160">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-161">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a9f47-161">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a9f47-162">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="a9f47-162">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f47-163">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="a9f47-163">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="a9f47-164">資料庫頁面上發生總和檢查碼驗證錯誤。</span><span class="sxs-lookup"><span data-stu-id="a9f47-164">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a9f47-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a9f47-166">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="a9f47-166">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f47-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a9f47-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a9f47-168">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="a9f47-168">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="a9f47-169"><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="a9f47-169"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a9f47-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a9f47-171">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="a9f47-171">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9f47-172">在函式傳回成功之後，備份目錄中的所有還原備份所需的檔案都會出現在備份目錄中。</span><span class="sxs-lookup"><span data-stu-id="a9f47-172">After the function returns success, in the backup directory all the files needed for a restore up to the moment of the backup will be present.</span></span> <span data-ttu-id="a9f47-173">如果這是完整備份，檔案將會是資料庫檔案，以及將資料庫帶入一致狀態所需的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="a9f47-173">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="a9f47-174">如果這是增量備份，則只會將記錄檔新增至目錄，但現有的檔案 (資料庫和記錄檔，) 連同新的記錄檔將可以還原，並使資料庫回到備份當時的狀態。</span><span class="sxs-lookup"><span data-stu-id="a9f47-174">If this is an incremental backup, only log files will be added to the directories but the already existing files (databases and log files) together with the new log files will be able to be restored and bring the database back to the state at the moment of the backup.</span></span>

<span data-ttu-id="a9f47-175">備份的副作用是，不再需要的記錄檔將會被截斷。</span><span class="sxs-lookup"><span data-stu-id="a9f47-175">As a side effect of the backup, the log files which are not longer needed will be truncated.</span></span>

<span data-ttu-id="a9f47-176">在相同的時間內，資料庫標頭會在最後一次備份時，以資訊更新。</span><span class="sxs-lookup"><span data-stu-id="a9f47-176">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="a9f47-177">失敗時，備份目錄目的地中將不會有任何檔案，因此不會有任何還原。</span><span class="sxs-lookup"><span data-stu-id="a9f47-177">On failure, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="a9f47-178">在相同的時間內，目前的記錄檔不會被截斷。</span><span class="sxs-lookup"><span data-stu-id="a9f47-178">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a9f47-179">備註</span><span class="sxs-lookup"><span data-stu-id="a9f47-179">Remarks</span></span>

<span data-ttu-id="a9f47-180">備份的不同步驟將會產生事件記錄檔專案，包括檔案名、記錄截斷，以及備份的最終結果。</span><span class="sxs-lookup"><span data-stu-id="a9f47-180">The different steps of the backup will have Event Log entries generated including the file names, the log truncation and the final result of the backup.</span></span>

<span data-ttu-id="a9f47-181">只有在執行完整備份之後，才可能進行增量備份。</span><span class="sxs-lookup"><span data-stu-id="a9f47-181">Incremental backup are possible only after a full backup was taken.</span></span> <span data-ttu-id="a9f47-182">此外，只有在迴圈記錄關閉時，才可能進行增量備份。</span><span class="sxs-lookup"><span data-stu-id="a9f47-182">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="a9f47-183">建議備份目錄不應該包含其他檔案，然後是備份所牽涉的檔案，或是先前成功備份所新增的檔案。</span><span class="sxs-lookup"><span data-stu-id="a9f47-183">It is recommended that the backup directory should not contain other files then the one involved in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="a9f47-184">除非針對實例設定了參數 *JET_paramCreatePathIfNotExist* ，否則備份目錄應該會存在。</span><span class="sxs-lookup"><span data-stu-id="a9f47-184">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="a9f47-185">如需詳細資訊，請參閱 [系統參數](./extensible-storage-engine-system-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="a9f47-185">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="a9f47-186">備份也會在記錄檔上，對所有已使用的資料庫頁面進行總和檢查碼驗證，並從 Windows Server 2003 開始。</span><span class="sxs-lookup"><span data-stu-id="a9f47-186">The backup will do checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="a9f47-187">這讓您有機會評估資料庫的健全狀況，即使是在正常作業期間未讀取的頁面也是一樣。</span><span class="sxs-lookup"><span data-stu-id="a9f47-187">This gives an opportunity to estimate the health of the database even for pages which are not read during normal operations.</span></span> <span data-ttu-id="a9f47-188">如果發生任何這類損毀，備份將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a9f47-188">If any such corruption will be encountered, the backup will fail.</span></span>

<span data-ttu-id="a9f47-189">在備份期間，目前的記錄檔將會完成，而且我們會開始新的記錄產生。</span><span class="sxs-lookup"><span data-stu-id="a9f47-189">During the backup, the current log file will be finished and we will start a new log generation.</span></span> <span data-ttu-id="a9f47-190">這將允許複製所需的記錄檔，因為最後一個必要的記錄檔將不再使用。</span><span class="sxs-lookup"><span data-stu-id="a9f47-190">This will allow copying the needed log files because the last needed one will not be in use anymore.</span></span>

<span data-ttu-id="a9f47-191">強烈建議您不要將備份用於其他設定，然後備份並在引擎層級還原。</span><span class="sxs-lookup"><span data-stu-id="a9f47-191">It is strongly recommended that the backup should not be used for other purposed other then the backup and restored at the engine level.</span></span> <span data-ttu-id="a9f47-192">這可將在備份和還原作業期間取得錯誤的變更降至最低。</span><span class="sxs-lookup"><span data-stu-id="a9f47-192">This will minimize the change of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a9f47-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9f47-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-194"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="a9f47-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a9f47-195">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="a9f47-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f47-196"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="a9f47-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a9f47-197">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="a9f47-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-198"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="a9f47-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a9f47-199">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="a9f47-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f47-200"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="a9f47-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a9f47-201">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="a9f47-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9f47-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a9f47-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a9f47-203">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="a9f47-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9f47-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a9f47-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a9f47-205">實作為 <strong>JetBackupInstanceW</strong> (Unicode) 和 <strong>JetBackupInstanceA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="a9f47-205">Implemented as <strong>JetBackupInstanceW</strong> (Unicode) and <strong>JetBackupInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a9f47-206">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9f47-206">See Also</span></span>

[<span data-ttu-id="a9f47-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a9f47-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a9f47-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a9f47-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a9f47-209">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a9f47-209">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a9f47-210">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="a9f47-210">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="a9f47-211">JetRestore</span><span class="sxs-lookup"><span data-stu-id="a9f47-211">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="a9f47-212">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="a9f47-212">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="a9f47-213">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="a9f47-213">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="a9f47-214">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="a9f47-214">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)  
[<span data-ttu-id="a9f47-215">系統參數</span><span class="sxs-lookup"><span data-stu-id="a9f47-215">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
