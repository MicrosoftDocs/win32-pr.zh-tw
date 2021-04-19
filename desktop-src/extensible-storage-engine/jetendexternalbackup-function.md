---
description: 深入瞭解： JetEndExternalBackup 函數
title: JetEndExternalBackup 函式
TOCTitle: JetEndExternalBackup Function
ms:assetid: 058f903b-14b7-44b3-9ec7-7c05c9ec6363
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269176(v=EXCHG.10)
ms:contentKeyID: 32765479
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 91f3db40fef483114313bbaa5f01e592d860bde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992196"
---
# <a name="jetendexternalbackup-function"></a><span data-ttu-id="5cacc-103">JetEndExternalBackup 函式</span><span class="sxs-lookup"><span data-stu-id="5cacc-103">JetEndExternalBackup Function</span></span>


<span data-ttu-id="5cacc-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5cacc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackup-function"></a><span data-ttu-id="5cacc-105">JetEndExternalBackup 函式</span><span class="sxs-lookup"><span data-stu-id="5cacc-105">JetEndExternalBackup Function</span></span>

<span data-ttu-id="5cacc-106">**JetEndExternalBackup** 函數會結束外部備份會話。</span><span class="sxs-lookup"><span data-stu-id="5cacc-106">The **JetEndExternalBackup** function ends an external backup session.</span></span> <span data-ttu-id="5cacc-107">此函式是一系列 API 專案中的最後一個 API 元素，必須呼叫這些元素，才能執行成功的線上 (非 VSS 型) 備份。</span><span class="sxs-lookup"><span data-stu-id="5cacc-107">This function is the last API element in a series of API elements that must be called to execute a successful online (non-VSS based) backup.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="5cacc-108">參數</span><span class="sxs-lookup"><span data-stu-id="5cacc-108">Parameters</span></span>

<span data-ttu-id="5cacc-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="5cacc-109">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="5cacc-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="5cacc-110">Return Value</span></span>

<span data-ttu-id="5cacc-111">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="5cacc-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5cacc-112">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="5cacc-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cacc-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5cacc-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="5cacc-114">Description</span><span class="sxs-lookup"><span data-stu-id="5cacc-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cacc-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5cacc-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5cacc-116">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="5cacc-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cacc-117">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5cacc-117">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5cacc-118">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="5cacc-118">The operation cannot complete because the instance that is associated with the session has not been yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cacc-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5cacc-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5cacc-120">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="5cacc-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cacc-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5cacc-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5cacc-122"><strong>WINDOWS XP：  </strong>此傳回值是在 Windows XP 中引進</span><span class="sxs-lookup"><span data-stu-id="5cacc-122"><strong>Windows XP:  </strong>This return value is introduced in Windows XP</span></span></p>
<p><span data-ttu-id="5cacc-123">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="5cacc-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cacc-124">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5cacc-124">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5cacc-125">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="5cacc-125">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cacc-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5cacc-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5cacc-127">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="5cacc-127">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cacc-128">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="5cacc-128">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="5cacc-129">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="5cacc-129">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cacc-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="5cacc-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="5cacc-131"><strong>Windows Server 2003：  </strong>此傳回值是在 Windows Server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="5cacc-131"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="5cacc-132">作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="5cacc-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cacc-133">errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="5cacc-133">errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="5cacc-134"><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="5cacc-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="5cacc-135">呼叫端在備份順序中途終止備份，而不會向 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>發出任何信號。</span><span class="sxs-lookup"><span data-stu-id="5cacc-135">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="5cacc-136">此錯誤是 Windows Server 2003 和更新版本中備份用戶端的錯誤結果。</span><span class="sxs-lookup"><span data-stu-id="5cacc-136">This error is a result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="5cacc-137">在 Windows XP 上，會針對外部備份順序的刻意終止傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="5cacc-137">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cacc-138">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="5cacc-138">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="5cacc-139">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 只支援一個實例，而事實上有多個實例已經存在。</span><span class="sxs-lookup"><span data-stu-id="5cacc-139">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5cacc-140">如果此函式成功，則外部備份成功。</span><span class="sxs-lookup"><span data-stu-id="5cacc-140">If this function succeeds, the external backup was a success.</span></span> <span data-ttu-id="5cacc-141">[成功] 表示所有檔案 (例如，資料庫和記錄檔) ，適用于 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) 中指定的 (備份類型，可從備份引擎取出。</span><span class="sxs-lookup"><span data-stu-id="5cacc-141">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="5cacc-142">備份的檔案可以透過「硬復原」 ([JetExternalRestore](./jetexternalrestore-function.md)) 來復原。</span><span class="sxs-lookup"><span data-stu-id="5cacc-142">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="5cacc-143">如果此函式失敗，則外部備份通常會結束。</span><span class="sxs-lookup"><span data-stu-id="5cacc-143">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="5cacc-144">失敗表示因為用戶端或應用程式使用錯誤，所以備份無效。</span><span class="sxs-lookup"><span data-stu-id="5cacc-144">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="5cacc-145">檢查此 API 的傳回碼以確認備份順序是否成功，是很重要的。</span><span class="sxs-lookup"><span data-stu-id="5cacc-145">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5cacc-146">備註</span><span class="sxs-lookup"><span data-stu-id="5cacc-146">Remarks</span></span>

<span data-ttu-id="5cacc-147">如果引擎設定為記錄事件，則會記錄事件，以指出外部備份的解決方式。</span><span class="sxs-lookup"><span data-stu-id="5cacc-147">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="5cacc-148">如果備份順序未依順序完成，而且成功呼叫 **JetEndExternalBackup**，則後續的增量備份可能會包含比預期的應用程式更多的資料。</span><span class="sxs-lookup"><span data-stu-id="5cacc-148">If the backup sequence is not completed in order and with a successful call to **JetEndExternalBackup**, subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="5cacc-149">如需外部備份 API 序列的詳細資訊，請參閱 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)。</span><span class="sxs-lookup"><span data-stu-id="5cacc-149">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="5cacc-150">在 Windows Vista 之前，如果未執行記錄截斷，引擎會將備份視為複本備份。</span><span class="sxs-lookup"><span data-stu-id="5cacc-150">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="5cacc-151">不過，備份可能是未完成截斷的一般備份 (例如，如果有卸離的資料庫) 。</span><span class="sxs-lookup"><span data-stu-id="5cacc-151">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="5cacc-152">JET_bitBackupTruncateDone 選項可以用來通知引擎，並允許適當的資料庫標頭修改。</span><span class="sxs-lookup"><span data-stu-id="5cacc-152">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow appropriate database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5cacc-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cacc-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cacc-154"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="5cacc-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5cacc-155">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="5cacc-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cacc-156"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="5cacc-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5cacc-157">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="5cacc-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cacc-158"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="5cacc-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5cacc-159">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="5cacc-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cacc-160"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="5cacc-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5cacc-161">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="5cacc-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cacc-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5cacc-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5cacc-163">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="5cacc-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5cacc-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cacc-164">See Also</span></span>

[<span data-ttu-id="5cacc-165">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="5cacc-165">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="5cacc-166">可擴充儲存引擎錯誤</span><span class="sxs-lookup"><span data-stu-id="5cacc-166">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="5cacc-167">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="5cacc-167">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="5cacc-168">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="5cacc-168">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="5cacc-169">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="5cacc-169">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="5cacc-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5cacc-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5cacc-171">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="5cacc-171">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="5cacc-172">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="5cacc-172">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="5cacc-173">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="5cacc-173">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="5cacc-174">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="5cacc-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="5cacc-175">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="5cacc-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="5cacc-176">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="5cacc-176">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="5cacc-177">JetStopService</span><span class="sxs-lookup"><span data-stu-id="5cacc-177">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="5cacc-178">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="5cacc-178">JetTruncateLog</span></span>](./jettruncatelog-function.md)
