---
description: 深入瞭解： JetGetLogInfoInstance 函數
title: JetGetLogInfoInstance 函式
TOCTitle: JetGetLogInfoInstance Function
ms:assetid: 505500b1-2827-43f1-a0fe-5e84e00b0260
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269246(v=EXCHG.10)
ms:contentKeyID: 32765548
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance
- JetGetLogInfoInstanceW
- JetGetLogInfoInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2056859bdce13dfdc28d4cbbf8716925d5bc1cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978151"
---
# <a name="jetgetloginfoinstance-function"></a><span data-ttu-id="cc252-103">JetGetLogInfoInstance 函式</span><span class="sxs-lookup"><span data-stu-id="cc252-103">JetGetLogInfoInstance Function</span></span>


<span data-ttu-id="cc252-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cc252-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfoinstance-function"></a><span data-ttu-id="cc252-105">JetGetLogInfoInstance 函式</span><span class="sxs-lookup"><span data-stu-id="cc252-105">JetGetLogInfoInstance Function</span></span>

<span data-ttu-id="cc252-106">**JetGetLogInfoInstance** 函式會在 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)所起始的備份期間使用，以查詢資料庫修補檔的名稱和交易記錄檔的名稱，這些檔案應該會成為備份檔案集的一部分。</span><span class="sxs-lookup"><span data-stu-id="cc252-106">The **JetGetLogInfoInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="cc252-107">之後可能會使用 [JetOpenFile](./jetopenfile-function.md) 來開啟這些檔案，並使用 [JetReadFile](./jetreadfile-function.md)進行讀取。</span><span class="sxs-lookup"><span data-stu-id="cc252-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

<span data-ttu-id="cc252-108">**Windows xp： JetGetLogInfoInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="cc252-108">**Windows XP:  JetGetLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="cc252-109">參數</span><span class="sxs-lookup"><span data-stu-id="cc252-109">Parameters</span></span>

<span data-ttu-id="cc252-110">*實例*</span><span class="sxs-lookup"><span data-stu-id="cc252-110">*instance*</span></span>

<span data-ttu-id="cc252-111">此呼叫所要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="cc252-111">The instance to use for this call.</span></span>

<span data-ttu-id="cc252-112">針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="cc252-112">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="cc252-113">在此情況下，這種全域實例的使用是隱含的。</span><span class="sxs-lookup"><span data-stu-id="cc252-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="cc252-114">若為 Windows XP 和更新版本，則只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變體 (Windows 2000 相容性模式) 只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="cc252-114">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="cc252-115">否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。</span><span class="sxs-lookup"><span data-stu-id="cc252-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="cc252-116">*szz*</span><span class="sxs-lookup"><span data-stu-id="cc252-116">*szz*</span></span>

<span data-ttu-id="cc252-117">輸出緩衝區會接收 null 結束字串的清單，這些字串會描述資料庫修補檔和交易記錄檔的集合，而這些檔案應該是備份檔案集的一部分。</span><span class="sxs-lookup"><span data-stu-id="cc252-117">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="cc252-118">此緩衝區中傳回的字串清單，與登錄所用的多重字串格式相同。</span><span class="sxs-lookup"><span data-stu-id="cc252-118">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="cc252-119">每個以 null 終止的字串會依序傳回，後面接著最後一個 null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="cc252-119">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="cc252-120">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="cc252-120">*cbMax*</span></span>

<span data-ttu-id="cc252-121">輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cc252-121">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="cc252-122">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="cc252-122">*pcbActual*</span></span>

<span data-ttu-id="cc252-123">接收輸出緩衝區中收到的實際字串資料量。</span><span class="sxs-lookup"><span data-stu-id="cc252-123">Receives the actual amount of string data received in the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="cc252-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc252-124">Return Value</span></span>

<span data-ttu-id="cc252-125">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="cc252-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cc252-126">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="cc252-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc252-127">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cc252-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="cc252-128">Description</span><span class="sxs-lookup"><span data-stu-id="cc252-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc252-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cc252-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cc252-130">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="cc252-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc252-131">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="cc252-131">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="cc252-132">作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="cc252-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="cc252-133">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cc252-133">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc252-134">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="cc252-134">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="cc252-135">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="cc252-135">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc252-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="cc252-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="cc252-137">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="cc252-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="cc252-138">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cc252-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc252-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="cc252-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="cc252-140">備份作業失敗，因為它的呼叫順序不是。</span><span class="sxs-lookup"><span data-stu-id="cc252-140">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="cc252-141">如果有任何未完成的檔案控制代碼使用<a href="gg269249(v=exchg.10).md">JetOpenFile</a>建立實例， <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a>將會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="cc252-141"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc252-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="cc252-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="cc252-143">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="cc252-143">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="cc252-144">當指定的實例控制碼無效 (Windows XP 和更新版本) 時， <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> 就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="cc252-144">This can happen for <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc252-145">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="cc252-145">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="cc252-146">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="cc252-146">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc252-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="cc252-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="cc252-148">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cc252-148">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc252-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="cc252-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="cc252-150">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="cc252-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc252-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="cc252-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="cc252-152">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="cc252-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc252-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="cc252-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="cc252-154">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="cc252-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cc252-155">成功時，在提供的輸出緩衝區中，會將資料庫修補檔和交易記錄檔集上所要求的資訊放入備份檔案集的一部分。</span><span class="sxs-lookup"><span data-stu-id="cc252-155">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="cc252-156">備份狀態電腦將會是最先進的，因此不再允許資料庫檔案的備份。</span><span class="sxs-lookup"><span data-stu-id="cc252-156">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="cc252-157">現在只允許開啟資料庫修補檔和交易記錄檔進行備份。</span><span class="sxs-lookup"><span data-stu-id="cc252-157">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="cc252-158">失敗時，輸出緩衝區的狀態是未定義的。</span><span class="sxs-lookup"><span data-stu-id="cc252-158">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="cc252-159">失敗會導致整個實例的整個備份進程取消。</span><span class="sxs-lookup"><span data-stu-id="cc252-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc252-160">備註</span><span class="sxs-lookup"><span data-stu-id="cc252-160">Remarks</span></span>

<span data-ttu-id="cc252-161">請務必注意，如果輸出緩衝區太小而無法接受備份檔案集中應包含的完整檔案清單，則此 API 不會傳回錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="cc252-161">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="cc252-162">應用程式應該一律提供緩衝區來接收此清單的實際大小，並使用該資訊來判斷清單是否已遭截斷。</span><span class="sxs-lookup"><span data-stu-id="cc252-162">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="cc252-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc252-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc252-164"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="cc252-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cc252-165">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="cc252-165">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc252-166"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="cc252-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cc252-167">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="cc252-167">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc252-168"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="cc252-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cc252-169">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="cc252-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc252-170"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="cc252-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cc252-171">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="cc252-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc252-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cc252-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cc252-173">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="cc252-173">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc252-174"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="cc252-174"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="cc252-175">實作為 <strong>JetGetLogInfoInstanceW</strong> (Unicode) 和 <strong>JetGetLogInfoInstanceA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="cc252-175">Implemented as <strong>JetGetLogInfoInstanceW</strong> (Unicode) and <strong>JetGetLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cc252-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc252-176">See Also</span></span>

[<span data-ttu-id="cc252-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cc252-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cc252-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="cc252-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="cc252-179">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="cc252-179">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="cc252-180">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="cc252-180">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="cc252-181">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="cc252-181">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="cc252-182">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="cc252-182">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="cc252-183">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="cc252-183">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="cc252-184">JetStopService</span><span class="sxs-lookup"><span data-stu-id="cc252-184">JetStopService</span></span>](./jetstopservice-function.md)
