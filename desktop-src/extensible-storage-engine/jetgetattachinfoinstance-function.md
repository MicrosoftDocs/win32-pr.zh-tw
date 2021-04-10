---
description: 深入瞭解： JetGetAttachInfoInstance 函數
title: JetGetAttachInfoInstance 函式
TOCTitle: JetGetAttachInfoInstance Function
ms:assetid: 978e7817-0720-42fc-a5c1-46e4d44239f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269350(v=EXCHG.10)
ms:contentKeyID: 32765637
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfoInstanceW
- JetGetAttachInfoInstanceA
- JetGetAttachInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28abf76632f147b6e909c1b8fb036062d5d3af74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849545"
---
# <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="38b5e-103">JetGetAttachInfoInstance 函式</span><span class="sxs-lookup"><span data-stu-id="38b5e-103">JetGetAttachInfoInstance Function</span></span>


<span data-ttu-id="38b5e-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="38b5e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="38b5e-105">JetGetAttachInfoInstance 函式</span><span class="sxs-lookup"><span data-stu-id="38b5e-105">JetGetAttachInfoInstance Function</span></span>

<span data-ttu-id="38b5e-106">**JetGetAttachInfoInstance** 函式是在 [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md)所起始的備份期間，用來查詢實例，以取得應該成為備份檔案集一部分的資料庫檔案名。</span><span class="sxs-lookup"><span data-stu-id="38b5e-106">The **JetGetAttachInfoInstance** function is used during a backup initiated by [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="38b5e-107">只會考慮目前使用 [JetAttachDatabase](./jetattachdatabase-function.md) 連接到實例的資料庫。</span><span class="sxs-lookup"><span data-stu-id="38b5e-107">Only databases that are currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="38b5e-108">之後可能會使用 [JetOpenFileInstance](./jetopenfileinstance-function.md) 來開啟這些檔案，並使用 [JetReadFileInstance](./jetreadfileinstance-function.md)進行讀取。</span><span class="sxs-lookup"><span data-stu-id="38b5e-108">These files may subsequently be opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) and read using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="38b5e-109">**Windows xp： JetGetAttachInfoInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="38b5e-109">**Windows XP:  JetGetAttachInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="38b5e-110">參數</span><span class="sxs-lookup"><span data-stu-id="38b5e-110">Parameters</span></span>

<span data-ttu-id="38b5e-111">*實例*</span><span class="sxs-lookup"><span data-stu-id="38b5e-111">*instance*</span></span>

<span data-ttu-id="38b5e-112">此呼叫所要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="38b5e-112">The instance to use for this call.</span></span>

<span data-ttu-id="38b5e-113">針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="38b5e-113">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="38b5e-114">在此情況下，這種全域實例的使用是隱含的。</span><span class="sxs-lookup"><span data-stu-id="38b5e-114">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="38b5e-115">若為 Windows XP 和更新版本，則只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變體 (Windows 2000 相容性模式) 只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="38b5e-115">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="38b5e-116">否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。</span><span class="sxs-lookup"><span data-stu-id="38b5e-116">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="38b5e-117">*szz*</span><span class="sxs-lookup"><span data-stu-id="38b5e-117">*szz*</span></span>

<span data-ttu-id="38b5e-118">輸出緩衝區，此輸出緩衝區會接收以 null 結束字串的清單，這些字串會描述應該是備份檔案集一部分的資料庫檔案集。</span><span class="sxs-lookup"><span data-stu-id="38b5e-118">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="38b5e-119">此緩衝區中傳回的字串清單，與登錄所用的多重字串格式相同。</span><span class="sxs-lookup"><span data-stu-id="38b5e-119">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="38b5e-120">每個以 null 終止的字串會依序傳回，後面接著最後一個 null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="38b5e-120">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="38b5e-121">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="38b5e-121">*cbMax*</span></span>

<span data-ttu-id="38b5e-122">輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="38b5e-122">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="38b5e-123">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="38b5e-123">*pcbActual*</span></span>

<span data-ttu-id="38b5e-124">輸出緩衝區的指標，此輸出緩衝區會接收實際的字串資料量。</span><span class="sxs-lookup"><span data-stu-id="38b5e-124">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="38b5e-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="38b5e-125">Return Value</span></span>

<span data-ttu-id="38b5e-126">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="38b5e-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="38b5e-127">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="38b5e-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38b5e-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="38b5e-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="38b5e-129">Description</span><span class="sxs-lookup"><span data-stu-id="38b5e-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38b5e-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="38b5e-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="38b5e-131">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="38b5e-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b5e-132">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="38b5e-132">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="38b5e-133">作業失敗，因為目前的外部備份已被 <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="38b5e-133">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="38b5e-134">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="38b5e-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b5e-135">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="38b5e-135">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="38b5e-136">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="38b5e-136">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b5e-137">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="38b5e-137">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="38b5e-138">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="38b5e-138">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="38b5e-139">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="38b5e-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b5e-140">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="38b5e-140">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="38b5e-141">備份作業失敗，因為它的呼叫順序不是。</span><span class="sxs-lookup"><span data-stu-id="38b5e-141">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="38b5e-142">如果目前的備份不是完整備份， <strong>JetGetAttachInfoInstance</strong>會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="38b5e-142"><strong>JetGetAttachInfoInstance</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b5e-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="38b5e-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="38b5e-144">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="38b5e-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="38b5e-145">當指定的實例控制碼無效 (Windows XP 和更新版本) 時， <strong>JetGetAttachInfoInstance</strong> 就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="38b5e-145">This can happen for <strong>JetGetAttachInfoInstance</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b5e-146">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="38b5e-146">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="38b5e-147">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="38b5e-147">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b5e-148">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="38b5e-148">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="38b5e-149">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="38b5e-149">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b5e-150">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="38b5e-150">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="38b5e-151">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="38b5e-151">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b5e-152">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="38b5e-152">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="38b5e-153">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="38b5e-153">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b5e-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="38b5e-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="38b5e-155">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="38b5e-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="38b5e-156">成功時，在所提供的輸出緩衝區中，會將所要求的資料庫檔案集合的資訊放入備份檔案集的一部分。</span><span class="sxs-lookup"><span data-stu-id="38b5e-156">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="38b5e-157">失敗時，輸出緩衝區的狀態是未定義的。</span><span class="sxs-lookup"><span data-stu-id="38b5e-157">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="38b5e-158">失敗會導致整個實例的整個備份進程取消。</span><span class="sxs-lookup"><span data-stu-id="38b5e-158">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="38b5e-159">備註</span><span class="sxs-lookup"><span data-stu-id="38b5e-159">Remarks</span></span>

<span data-ttu-id="38b5e-160">請務必注意，如果輸出緩衝區太小而無法接受備份檔案集中應包含的完整檔案清單，則此 API 不會傳回錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="38b5e-160">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="38b5e-161">應用程式應該一律提供緩衝區來接收此清單的實際大小，並使用該資訊來判斷清單是否已遭截斷。</span><span class="sxs-lookup"><span data-stu-id="38b5e-161">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="38b5e-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="38b5e-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38b5e-163"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="38b5e-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="38b5e-164">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="38b5e-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b5e-165"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="38b5e-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="38b5e-166">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="38b5e-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b5e-167"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="38b5e-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="38b5e-168">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="38b5e-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b5e-169"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="38b5e-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="38b5e-170">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="38b5e-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38b5e-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="38b5e-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="38b5e-172">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="38b5e-172">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38b5e-173"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="38b5e-173"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="38b5e-174">實作為 <strong>JetGetAttachInfoInstanceW</strong> (Unicode) 和 <strong>JetGetAttachInfoInstanceA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="38b5e-174">Implemented as <strong>JetGetAttachInfoInstanceW</strong> (Unicode) and <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="38b5e-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38b5e-175">See Also</span></span>

[<span data-ttu-id="38b5e-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="38b5e-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="38b5e-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="38b5e-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="38b5e-178">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="38b5e-178">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="38b5e-179">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="38b5e-179">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="38b5e-180">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="38b5e-180">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="38b5e-181">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="38b5e-181">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="38b5e-182">JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="38b5e-182">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="38b5e-183">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="38b5e-183">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
