---
description: 深入瞭解： JetEndExternalBackupInstance2 函數
title: JetEndExternalBackupInstance2 函式
TOCTitle: JetEndExternalBackupInstance2 Function
ms:assetid: a30961f7-a1fb-44fe-881a-d46bf8f743b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294047(v=EXCHG.10)
ms:contentKeyID: 32765646
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e719885cc61ff3f3193046b632e9969b8d660f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977076"
---
# <a name="jetendexternalbackupinstance2-function"></a><span data-ttu-id="f1140-103">JetEndExternalBackupInstance2 函式</span><span class="sxs-lookup"><span data-stu-id="f1140-103">JetEndExternalBackupInstance2 Function</span></span>


<span data-ttu-id="f1140-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f1140-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackupinstance2-function"></a><span data-ttu-id="f1140-105">JetEndExternalBackupInstance2 函式</span><span class="sxs-lookup"><span data-stu-id="f1140-105">JetEndExternalBackupInstance2 Function</span></span>

<span data-ttu-id="f1140-106">**JetEndExternalBackupInstance2** 函數會結束外部備份會話。</span><span class="sxs-lookup"><span data-stu-id="f1140-106">The **JetEndExternalBackupInstance2** function ends an external backup session.</span></span> <span data-ttu-id="f1140-107">此 API 是一系列 Api 中的最後一個 API，必須呼叫這些 api，以執行線上 (非 VSS 型) 備份成功。</span><span class="sxs-lookup"><span data-stu-id="f1140-107">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="f1140-108">**Windows xp： JetEndExternalBackupInstance2** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="f1140-108">**Windows XP:  JetEndExternalBackupInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f1140-109">參數</span><span class="sxs-lookup"><span data-stu-id="f1140-109">Parameters</span></span>

<span data-ttu-id="f1140-110">*實例*</span><span class="sxs-lookup"><span data-stu-id="f1140-110">*instance*</span></span>

<span data-ttu-id="f1140-111">此呼叫所要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="f1140-111">The instance to use for this call.</span></span>

<span data-ttu-id="f1140-112">**Windows 2000：** 針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="f1140-112">**Windows 2000:** For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="f1140-113">在此情況下，這種全域實例的使用是隱含的。</span><span class="sxs-lookup"><span data-stu-id="f1140-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="f1140-114">**WINDOWS XP：** 若為 Windows XP 和更新版本，則只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變數 (Windows 2000 相容性模式) 只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="f1140-114">**Windows XP:** For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="f1140-115">否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。</span><span class="sxs-lookup"><span data-stu-id="f1140-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="f1140-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f1140-116">*grbit*</span></span>

<span data-ttu-id="f1140-117">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="f1140-117">A group of bits that specifies zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1140-118">值</span><span class="sxs-lookup"><span data-stu-id="f1140-118">Value</span></span></p></th>
<th><p><span data-ttu-id="f1140-119">意義</span><span class="sxs-lookup"><span data-stu-id="f1140-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1140-120">JET_bitBackupEndAbort</span><span class="sxs-lookup"><span data-stu-id="f1140-120">JET_bitBackupEndAbort</span></span><br />
<span data-ttu-id="f1140-121">0x0002</span><span class="sxs-lookup"><span data-stu-id="f1140-121">0x0002</span></span></p></td>
<td><p><span data-ttu-id="f1140-122">用戶端應用程式正在中止備份。</span><span class="sxs-lookup"><span data-stu-id="f1140-122">The client application is aborting the backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1140-123">JET_bitBackupEndNormal</span><span class="sxs-lookup"><span data-stu-id="f1140-123">JET_bitBackupEndNormal</span></span><br />
<span data-ttu-id="f1140-124">0x0001</span><span class="sxs-lookup"><span data-stu-id="f1140-124">0x0001</span></span></p></td>
<td><p><span data-ttu-id="f1140-125">用戶端應用程式已完全完成備份，且正常結束。</span><span class="sxs-lookup"><span data-stu-id="f1140-125">The client application finished the backup completely, and is ending normally.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1140-126">JET_bitBackupTruncateDone</span><span class="sxs-lookup"><span data-stu-id="f1140-126">JET_bitBackupTruncateDone</span></span><br />
<span data-ttu-id="f1140-127">0x0100</span><span class="sxs-lookup"><span data-stu-id="f1140-127">0x0100</span></span></p></td>
<td><p><span data-ttu-id="f1140-128"><strong>Windows Vista：  </strong>JET_bitBackupTruncateDone 是在 Windows Vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="f1140-128"><strong>Windows Vista:  </strong>JET_bitBackupTruncateDone is introduced in Windows Vista.</span></span></p>
<p><span data-ttu-id="f1140-129">引擎可以在適當的情況下標記資料庫標頭 (例如，完整備份已完成) ，即使未完成截斷的呼叫也是一樣。</span><span class="sxs-lookup"><span data-stu-id="f1140-129">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f1140-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1140-130">Return Value</span></span>

<span data-ttu-id="f1140-131">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="f1140-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f1140-132">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="f1140-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1140-133">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f1140-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="f1140-134">Description</span><span class="sxs-lookup"><span data-stu-id="f1140-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1140-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f1140-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f1140-136">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f1140-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1140-137">JET_errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="f1140-137">JET_errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="f1140-138"><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="f1140-138"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="f1140-139">呼叫端在備份順序中途終止備份，而不會向 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>發出任何信號。</span><span class="sxs-lookup"><span data-stu-id="f1140-139">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="f1140-140">此錯誤是 Windows Server 2003 和更新版本中備份用戶端的錯誤所導致。</span><span class="sxs-lookup"><span data-stu-id="f1140-140">This error is result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="f1140-141">在 Windows XP 中，系統會針對外部備份順序的蓄意終止傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f1140-141">In Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1140-142">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="f1140-142">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="f1140-143"><strong>Windows Server 2003：  </strong>此傳回值是在 Windows Server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="f1140-143"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="f1140-144">作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="f1140-144">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1140-145">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f1140-145">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f1140-146">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="f1140-146">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1140-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f1140-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f1140-148"><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="f1140-148"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="f1140-149">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="f1140-149">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1140-150">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="f1140-150">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="f1140-151">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="f1140-151">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1140-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f1140-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f1140-153">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="f1140-153">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1140-154">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f1140-154">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f1140-155">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="f1140-155">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1140-156">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="f1140-156">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="f1140-157">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 只支援一個實例，而事實上有多個實例已經存在。</span><span class="sxs-lookup"><span data-stu-id="f1140-157">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1140-158">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f1140-158">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f1140-159">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="f1140-159">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1140-160">如果函式成功，則外部備份成功。</span><span class="sxs-lookup"><span data-stu-id="f1140-160">If the function succeeds, the external backup was a success.</span></span> <span data-ttu-id="f1140-161">[成功] 表示所有檔案 (例如，資料庫和記錄檔) ，適用于 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) 中指定的 (備份類型，可從備份引擎取出。</span><span class="sxs-lookup"><span data-stu-id="f1140-161">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="f1140-162">備份的檔案可以透過「硬復原」 ([JetExternalRestore](./jetexternalrestore-function.md)) 來復原。</span><span class="sxs-lookup"><span data-stu-id="f1140-162">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="f1140-163">如果此函式失敗，則外部備份通常會結束。</span><span class="sxs-lookup"><span data-stu-id="f1140-163">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="f1140-164">失敗表示因為用戶端或應用程式使用錯誤，所以備份無效。</span><span class="sxs-lookup"><span data-stu-id="f1140-164">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="f1140-165">檢查此 API 的傳回碼以確認備份順序是否成功，是很重要的。</span><span class="sxs-lookup"><span data-stu-id="f1140-165">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f1140-166">備註</span><span class="sxs-lookup"><span data-stu-id="f1140-166">Remarks</span></span>

<span data-ttu-id="f1140-167">如果引擎設定為記錄事件，則會記錄事件，以指出外部備份的解決方式。</span><span class="sxs-lookup"><span data-stu-id="f1140-167">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="f1140-168">如果備份順序未依順序完成，而且成功呼叫 [JetEndExternalBackup](./jetendexternalbackup-function.md)，則後續的增量備份可能會包含比預期的應用程式更多的資料。</span><span class="sxs-lookup"><span data-stu-id="f1140-168">If the backup sequence is not completed in order and with a successful call to [JetEndExternalBackup](./jetendexternalbackup-function.md), subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="f1140-169">如需外部備份 API 序列的詳細資訊，請參閱 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)。</span><span class="sxs-lookup"><span data-stu-id="f1140-169">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="f1140-170">在 Windows Vista 之前，如果未執行記錄截斷，引擎會將備份視為複本備份。</span><span class="sxs-lookup"><span data-stu-id="f1140-170">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="f1140-171">不過，備份可能是未完成截斷的一般備份 (例如，如果有卸離的資料庫) 。</span><span class="sxs-lookup"><span data-stu-id="f1140-171">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="f1140-172">JET_bitBackupTruncateDone 選項可以用來通知引擎，並允許適當的資料庫標頭修改。</span><span class="sxs-lookup"><span data-stu-id="f1140-172">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow appropriate database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f1140-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1140-173">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1140-174"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="f1140-174"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f1140-175">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="f1140-175">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1140-176"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="f1140-176"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f1140-177">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="f1140-177">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1140-178"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="f1140-178"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f1140-179">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="f1140-179">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1140-180"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="f1140-180"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f1140-181">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="f1140-181">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1140-182"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f1140-182"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f1140-183">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="f1140-183">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f1140-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1140-184">See Also</span></span>

[<span data-ttu-id="f1140-185">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="f1140-185">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="f1140-186">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="f1140-186">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="f1140-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f1140-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f1140-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f1140-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f1140-189">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="f1140-189">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="f1140-190">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="f1140-190">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="f1140-191">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="f1140-191">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="f1140-192">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="f1140-192">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="f1140-193">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="f1140-193">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="f1140-194">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="f1140-194">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="f1140-195">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="f1140-195">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="f1140-196">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f1140-196">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f1140-197">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="f1140-197">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="f1140-198">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="f1140-198">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="f1140-199">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="f1140-199">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="f1140-200">JetStopService</span><span class="sxs-lookup"><span data-stu-id="f1140-200">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="f1140-201">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="f1140-201">JetTruncateLog</span></span>](./jettruncatelog-function.md)
