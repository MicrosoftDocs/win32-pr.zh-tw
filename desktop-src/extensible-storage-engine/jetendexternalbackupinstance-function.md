---
description: 深入瞭解： JetEndExternalBackupInstance 函數
title: JetEndExternalBackupInstance 函式
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a017a0dbb4fa2f92c3e43a9dd2ff5649b65ee375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027142"
---
# <a name="jetendexternalbackupinstance-function"></a><span data-ttu-id="9660f-103">JetEndExternalBackupInstance 函式</span><span class="sxs-lookup"><span data-stu-id="9660f-103">JetEndExternalBackupInstance Function</span></span>


<span data-ttu-id="9660f-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9660f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackupinstance-function"></a><span data-ttu-id="9660f-105">JetEndExternalBackupInstance 函式</span><span class="sxs-lookup"><span data-stu-id="9660f-105">JetEndExternalBackupInstance Function</span></span>

<span data-ttu-id="9660f-106">**JetEndExternalBackupInstance** 函數會結束外部備份會話。</span><span class="sxs-lookup"><span data-stu-id="9660f-106">The **JetEndExternalBackupInstance** function ends an external backup session.</span></span> <span data-ttu-id="9660f-107">此 API 是一系列 Api 中的最後一個 API，必須呼叫這些 api，以執行線上 (非 VSS 型) 備份成功。</span><span class="sxs-lookup"><span data-stu-id="9660f-107">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="9660f-108">**Windows xp： JetEndExternalBackupInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="9660f-108">**Windows XP:  JetEndExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="9660f-109">參數</span><span class="sxs-lookup"><span data-stu-id="9660f-109">Parameters</span></span>

<span data-ttu-id="9660f-110">*實例*</span><span class="sxs-lookup"><span data-stu-id="9660f-110">*instance*</span></span>

<span data-ttu-id="9660f-111">此呼叫所要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="9660f-111">The instance to use for this call.</span></span>

<span data-ttu-id="9660f-112">**Windows 2000：** 針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="9660f-112">**Windows 2000:** For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="9660f-113">在此情況下，這種全域實例的使用是隱含的。</span><span class="sxs-lookup"><span data-stu-id="9660f-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="9660f-114">**WINDOWS XP：** 若為 Windows XP 和更新版本，則只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變數 (Windows 2000 相容性模式) 只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="9660f-114">**Windows XP:** For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="9660f-115">否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。</span><span class="sxs-lookup"><span data-stu-id="9660f-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="9660f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9660f-116">Return Value</span></span>

<span data-ttu-id="9660f-117">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="9660f-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9660f-118">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="9660f-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9660f-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9660f-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="9660f-120">Description</span><span class="sxs-lookup"><span data-stu-id="9660f-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9660f-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9660f-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9660f-122">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="9660f-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9660f-123">JET_errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="9660f-123">JET_errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="9660f-124"><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="9660f-124"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="9660f-125">呼叫端在備份順序中途終止備份，而不會向 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>發出任何信號。</span><span class="sxs-lookup"><span data-stu-id="9660f-125">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="9660f-126">此錯誤是 Windows Server 2003 和更新版本中的備份用戶端發生錯誤的結果。</span><span class="sxs-lookup"><span data-stu-id="9660f-126">This error is the result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="9660f-127">在 Windows XP 上，會針對外部備份順序的刻意終止傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="9660f-127">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9660f-128">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="9660f-128">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="9660f-129"><strong>Windows Server 2003：  </strong>此傳回值是在 Windows Server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="9660f-129"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="9660f-130">作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="9660f-130">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9660f-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9660f-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9660f-132">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="9660f-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9660f-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9660f-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9660f-134"><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="9660f-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="9660f-135">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="9660f-135">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9660f-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="9660f-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="9660f-137">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="9660f-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9660f-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9660f-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9660f-139">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="9660f-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9660f-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9660f-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9660f-141">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="9660f-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9660f-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="9660f-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="9660f-143">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 只支援一個實例，而事實上有多個實例已經存在。</span><span class="sxs-lookup"><span data-stu-id="9660f-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9660f-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9660f-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9660f-145">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="9660f-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9660f-146">如果函式成功，則外部備份成功。</span><span class="sxs-lookup"><span data-stu-id="9660f-146">If the function succeeds, the external backup was a success.</span></span> <span data-ttu-id="9660f-147">[成功] 表示所有檔案 (例如，資料庫和記錄檔) ，適用于 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) 中指定的 (備份類型，可從備份引擎取出。</span><span class="sxs-lookup"><span data-stu-id="9660f-147">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="9660f-148">備份的檔案可以透過「硬復原」 ([JetExternalRestore](./jetexternalrestore-function.md)) 來復原。</span><span class="sxs-lookup"><span data-stu-id="9660f-148">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="9660f-149">如果此函式失敗，則外部備份通常會結束。</span><span class="sxs-lookup"><span data-stu-id="9660f-149">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="9660f-150">失敗表示因為用戶端或應用程式使用錯誤，所以備份無效。</span><span class="sxs-lookup"><span data-stu-id="9660f-150">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="9660f-151">檢查此 API 的傳回碼以確認備份順序是否成功，是很重要的。</span><span class="sxs-lookup"><span data-stu-id="9660f-151">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9660f-152">備註</span><span class="sxs-lookup"><span data-stu-id="9660f-152">Remarks</span></span>

<span data-ttu-id="9660f-153">如果引擎設定為記錄事件，則會記錄事件，以指出外部備份的解決方式。</span><span class="sxs-lookup"><span data-stu-id="9660f-153">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="9660f-154">如果備份順序未依順序完成，而且成功呼叫 [JetEndExternalBackup](./jetendexternalbackup-function.md)，則後續的增量備份可能會包含比預期的應用程式更多的資料。</span><span class="sxs-lookup"><span data-stu-id="9660f-154">If the backup sequence is not completed in order and with a successful call to [JetEndExternalBackup](./jetendexternalbackup-function.md), subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="9660f-155">如需外部備份 API 序列的詳細資訊，請參閱 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)。</span><span class="sxs-lookup"><span data-stu-id="9660f-155">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="9660f-156">在 Windows Vista 之前，如果未執行記錄截斷，引擎會將備份視為複本備份。</span><span class="sxs-lookup"><span data-stu-id="9660f-156">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="9660f-157">不過，備份可能是未完成截斷的一般備份 (例如，如果有卸離的資料庫) 。</span><span class="sxs-lookup"><span data-stu-id="9660f-157">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="9660f-158">JET_bitBackupTruncateDone 選項可以用來通知引擎這項資訊，並允許適當的資料庫標頭修改。</span><span class="sxs-lookup"><span data-stu-id="9660f-158">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow proper database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9660f-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="9660f-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9660f-160"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="9660f-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9660f-161">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="9660f-161">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9660f-162"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="9660f-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9660f-163">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="9660f-163">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9660f-164"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="9660f-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9660f-165">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="9660f-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9660f-166"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="9660f-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9660f-167">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="9660f-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9660f-168"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9660f-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9660f-169">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="9660f-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9660f-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9660f-170">See Also</span></span>

[<span data-ttu-id="9660f-171">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="9660f-171">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="9660f-172">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="9660f-172">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="9660f-173">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="9660f-173">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="9660f-174">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="9660f-174">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="9660f-175">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="9660f-175">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="9660f-176">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="9660f-176">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="9660f-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9660f-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9660f-178">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="9660f-178">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="9660f-179">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="9660f-179">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="9660f-180">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="9660f-180">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="9660f-181">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="9660f-181">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="9660f-182">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="9660f-182">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="9660f-183">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="9660f-183">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="9660f-184">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="9660f-184">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="9660f-185">JetStopService</span><span class="sxs-lookup"><span data-stu-id="9660f-185">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="9660f-186">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="9660f-186">JetTruncateLog</span></span>](./jettruncatelog-function.md)
