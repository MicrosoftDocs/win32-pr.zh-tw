---
description: 深入瞭解： JetGetTruncateLogInfoInstance 函數
title: JetGetTruncateLogInfoInstance 函式
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d51243ff6ca4b2bbaec77233bbe00437f55e0f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979379"
---
# <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="e1467-103">JetGetTruncateLogInfoInstance 函式</span><span class="sxs-lookup"><span data-stu-id="e1467-103">JetGetTruncateLogInfoInstance Function</span></span>


<span data-ttu-id="e1467-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e1467-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="e1467-105">JetGetTruncateLogInfoInstance 函式</span><span class="sxs-lookup"><span data-stu-id="e1467-105">JetGetTruncateLogInfoInstance Function</span></span>

<span data-ttu-id="e1467-106">**JetGetTruncateLogInfoInstance** 函式會在由 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)起始的備份期間使用，以查詢實例是否有交易記錄檔的名稱，可在備份順利完成之後安全地刪除。</span><span class="sxs-lookup"><span data-stu-id="e1467-106">The **JetGetTruncateLogInfoInstance** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="e1467-107">**Windows xp：**  **JetGetTruncateLogInfoInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="e1467-107">**Windows XP:**  **JetGetTruncateLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="e1467-108">參數</span><span class="sxs-lookup"><span data-stu-id="e1467-108">Parameters</span></span>

<span data-ttu-id="e1467-109">*實例*</span><span class="sxs-lookup"><span data-stu-id="e1467-109">*instance*</span></span>

<span data-ttu-id="e1467-110">此呼叫所要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="e1467-110">The instance to use for this call.</span></span>

<span data-ttu-id="e1467-111">*szz*</span><span class="sxs-lookup"><span data-stu-id="e1467-111">*szz*</span></span>

<span data-ttu-id="e1467-112">輸出緩衝區，可接收以 null 終止字串的清單，這些字串描述可在成功完成備份之後安全刪除的交易記錄檔集合。</span><span class="sxs-lookup"><span data-stu-id="e1467-112">The output buffer that receives the list of null-terminated strings describing the set of transaction log files that can be safely deleted after the backup has been completed successfully.</span></span>

<span data-ttu-id="e1467-113">此緩衝區中傳回的字串清單，與登錄所使用的多字串格式相同。</span><span class="sxs-lookup"><span data-stu-id="e1467-113">The list of strings that are returned in this buffer is in the same format as a multi-string that is used by the registry.</span></span> <span data-ttu-id="e1467-114">每個以 null 終止的字串會依序傳回，後面接著最後一個 null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="e1467-114">Each null-terminated string is returned in sequence and followed by a final null terminator.</span></span>

<span data-ttu-id="e1467-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="e1467-115">*cbMax*</span></span>

<span data-ttu-id="e1467-116">輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e1467-116">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="e1467-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="e1467-117">*pcbActual*</span></span>

<span data-ttu-id="e1467-118">輸出緩衝區的指標，此輸出緩衝區會接收實際的字串資料量。</span><span class="sxs-lookup"><span data-stu-id="e1467-118">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="e1467-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1467-119">Return Value</span></span>

<span data-ttu-id="e1467-120">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="e1467-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e1467-121">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="e1467-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1467-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e1467-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="e1467-123">Description</span><span class="sxs-lookup"><span data-stu-id="e1467-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1467-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e1467-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e1467-125">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="e1467-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1467-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e1467-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e1467-127">其中一個提供的參數包含未預期的值，或數個參數值的組合導致非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="e1467-127">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="e1467-128"><strong>WINDOWS XP 和更新版本：</strong>  當指定的實例控制碼無效時， <strong>JetGetTruncateLogInfoInstance</strong> 就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="e1467-128"><strong>Windows XP and later:</strong>  This can happen for <strong>JetGetTruncateLogInfoInstance</strong> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1467-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e1467-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e1467-130">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="e1467-130">The operation cannot complete because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1467-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e1467-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e1467-132">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="e1467-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1467-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e1467-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e1467-134">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="e1467-134">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="e1467-135"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="e1467-135"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1467-136">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="e1467-136">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="e1467-137">作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="e1467-137">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="e1467-138"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="e1467-138"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1467-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="e1467-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="e1467-140">備份作業失敗，因為它的呼叫順序不是。</span><span class="sxs-lookup"><span data-stu-id="e1467-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1467-141">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="e1467-141">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="e1467-142">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="e1467-142">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1467-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e1467-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e1467-144">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="e1467-144">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1467-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e1467-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e1467-146">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="e1467-146">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1467-147"><strong>JetGetTruncateLogInfoInstance</strong></span><span class="sxs-lookup"><span data-stu-id="e1467-147"><strong>JetGetTruncateLogInfoInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="e1467-148">有未處理的檔案控制代碼，該控制碼是使用實例的 <a href="gg269249(v=exchg.10).md">JetOpenFile</a> 所建立。</span><span class="sxs-lookup"><span data-stu-id="e1467-148">There are outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e1467-149">如果此函式成功，則在已成功完成備份之後，可以安全地刪除的一組交易記錄檔所要求的相關資訊，將會放在提供這些記錄的輸出緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="e1467-149">If this function succeeds, the requested information about the set of transaction log files that can be safely deleted after the backup has been completed successfully will be placed in the output buffers where they are provided.</span></span> <span data-ttu-id="e1467-150">備份狀態電腦將會是最先進的，因此不再允許資料庫檔案的備份。</span><span class="sxs-lookup"><span data-stu-id="e1467-150">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="e1467-151">您只可以開啟資料庫修補檔和交易記錄檔，以進行備份。</span><span class="sxs-lookup"><span data-stu-id="e1467-151">Only database patch files and transaction log files can be opened for backup beyond this point.</span></span>

<span data-ttu-id="e1467-152">如果此函式失敗，輸出緩衝區的狀態就會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="e1467-152">If this function fails, the state of the output buffers is undefined.</span></span> <span data-ttu-id="e1467-153">失敗會導致整個實例的整個備份進程取消。</span><span class="sxs-lookup"><span data-stu-id="e1467-153">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e1467-154">備註</span><span class="sxs-lookup"><span data-stu-id="e1467-154">Remarks</span></span>

<span data-ttu-id="e1467-155">如果輸出緩衝區太小，無法接受備份檔案集中應包含的完整檔案清單，則此 API 不會傳回錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="e1467-155">This API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="e1467-156">應用程式應該一律提供緩衝區來接收此清單的實際大小，並使用該資訊來判斷清單是否已遭截斷。</span><span class="sxs-lookup"><span data-stu-id="e1467-156">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e1467-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1467-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1467-158"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="e1467-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e1467-159">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e1467-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1467-160"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="e1467-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e1467-161">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="e1467-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1467-162"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="e1467-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e1467-163">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="e1467-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1467-164"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="e1467-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e1467-165">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="e1467-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1467-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e1467-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e1467-167">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="e1467-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1467-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e1467-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e1467-169">實作為 <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) 和 <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="e1467-169">Implemented as <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) and <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e1467-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1467-170">See Also</span></span>

[<span data-ttu-id="e1467-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e1467-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e1467-172">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e1467-172">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="e1467-173">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="e1467-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="e1467-174">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="e1467-174">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="e1467-175">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="e1467-175">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="e1467-176">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="e1467-176">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="e1467-177">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="e1467-177">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="e1467-178">JetResetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="e1467-178">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="e1467-179">JetRollback</span><span class="sxs-lookup"><span data-stu-id="e1467-179">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="e1467-180">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="e1467-180">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="e1467-181">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e1467-181">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="e1467-182">JetTerm</span><span class="sxs-lookup"><span data-stu-id="e1467-182">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="e1467-183">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="e1467-183">JetTerm2</span></span>](./jetterm2-function.md)
