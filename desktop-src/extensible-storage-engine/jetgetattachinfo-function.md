---
description: 深入瞭解： JetGetAttachInfo 函數
title: JetGetAttachInfo 函式
TOCTitle: JetGetAttachInfo Function
ms:assetid: 6b1392f3-f40a-4eb0-aea8-1508b23ed649
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269286(v=EXCHG.10)
ms:contentKeyID: 32765578
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfo
- JetGetAttachInfoA
- JetGetAttachInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa1e51931c11e0fce0b18c0c102c4d54c0b47976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979340"
---
# <a name="jetgetattachinfo-function"></a><span data-ttu-id="856f3-103">JetGetAttachInfo 函式</span><span class="sxs-lookup"><span data-stu-id="856f3-103">JetGetAttachInfo Function</span></span>


<span data-ttu-id="856f3-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="856f3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfo-function"></a><span data-ttu-id="856f3-105">JetGetAttachInfo 函式</span><span class="sxs-lookup"><span data-stu-id="856f3-105">JetGetAttachInfo Function</span></span>

<span data-ttu-id="856f3-106">**JetGetAttachInfo** 函式是在 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)所起始的備份期間，用來查詢實例，以取得應該成為備份檔案集一部分的資料庫檔案名。</span><span class="sxs-lookup"><span data-stu-id="856f3-106">The **JetGetAttachInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="856f3-107">只會考慮目前使用 [JetAttachDatabase](./jetattachdatabase-function.md) 連接到實例的資料庫。</span><span class="sxs-lookup"><span data-stu-id="856f3-107">Only databases currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="856f3-108">之後可能會使用 [JetOpenFile](./jetopenfile-function.md) 來開啟這些檔案，並使用 [JetReadFile](./jetreadfile-function.md)進行讀取。</span><span class="sxs-lookup"><span data-stu-id="856f3-108">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="856f3-109">參數</span><span class="sxs-lookup"><span data-stu-id="856f3-109">Parameters</span></span>

<span data-ttu-id="856f3-110">*szz*</span><span class="sxs-lookup"><span data-stu-id="856f3-110">*szz*</span></span>

<span data-ttu-id="856f3-111">輸出緩衝區，此輸出緩衝區會接收以 null 結束字串的清單，這些字串會描述應該是備份檔案集一部分的資料庫檔案集。</span><span class="sxs-lookup"><span data-stu-id="856f3-111">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="856f3-112">此緩衝區中傳回的字串清單，與登錄所用的多重字串格式相同。</span><span class="sxs-lookup"><span data-stu-id="856f3-112">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="856f3-113">每個以 null 終止的字串會依序傳回，後面接著最後一個 null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="856f3-113">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="856f3-114">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="856f3-114">*cbMax*</span></span>

<span data-ttu-id="856f3-115">輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="856f3-115">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="856f3-116">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="856f3-116">*pcbActual*</span></span>

<span data-ttu-id="856f3-117">輸出緩衝區的指標，此緩衝區會接收實際的字串資料量。</span><span class="sxs-lookup"><span data-stu-id="856f3-117">Pointer to the output buffer that received the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="856f3-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="856f3-118">Return Value</span></span>

<span data-ttu-id="856f3-119">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="856f3-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="856f3-120">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="856f3-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="856f3-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="856f3-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="856f3-122">Description</span><span class="sxs-lookup"><span data-stu-id="856f3-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="856f3-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="856f3-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="856f3-124">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="856f3-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="856f3-125">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="856f3-125">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="856f3-126">作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="856f3-126">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="856f3-127">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="856f3-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="856f3-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="856f3-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="856f3-129">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="856f3-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="856f3-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="856f3-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="856f3-131">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="856f3-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="856f3-132">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="856f3-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="856f3-133">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="856f3-133">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="856f3-134">備份作業失敗，因為它的呼叫順序不是。</span><span class="sxs-lookup"><span data-stu-id="856f3-134">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="856f3-135">如果目前的備份不是完整備份， <strong>JetGetAttachInfo</strong>會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="856f3-135"><strong>JetGetAttachInfo</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="856f3-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="856f3-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="856f3-137">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="856f3-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="856f3-138">當指定的實例控制碼無效 (Windows XP 和更新版本) 時， <strong>JetGetAttachInfo</strong> 就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="856f3-138">This can happen for <strong>JetGetAttachInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="856f3-139">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="856f3-139">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="856f3-140">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="856f3-140">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="856f3-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="856f3-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="856f3-142">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="856f3-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="856f3-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="856f3-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="856f3-144">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="856f3-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="856f3-145">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="856f3-145">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="856f3-146">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="856f3-146">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="856f3-147">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="856f3-147">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="856f3-148">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="856f3-148">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="856f3-149">成功時，在所提供的輸出緩衝區中，會將所要求的資料庫檔案集合的資訊放入備份檔案集的一部分。</span><span class="sxs-lookup"><span data-stu-id="856f3-149">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="856f3-150">失敗時，輸出緩衝區的狀態是未定義的。</span><span class="sxs-lookup"><span data-stu-id="856f3-150">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="856f3-151">失敗會導致整個實例的整個備份進程取消。</span><span class="sxs-lookup"><span data-stu-id="856f3-151">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="856f3-152">備註</span><span class="sxs-lookup"><span data-stu-id="856f3-152">Remarks</span></span>

<span data-ttu-id="856f3-153">請務必注意，如果輸出緩衝區太小而無法接受備份檔案集中應包含的完整檔案清單，則此 API 不會傳回錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="856f3-153">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="856f3-154">應用程式應該一律提供緩衝區來接收此清單的實際大小，並使用該資訊來判斷清單是否已遭截斷。</span><span class="sxs-lookup"><span data-stu-id="856f3-154">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="856f3-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="856f3-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="856f3-156"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="856f3-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="856f3-157">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="856f3-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="856f3-158"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="856f3-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="856f3-159">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="856f3-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="856f3-160"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="856f3-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="856f3-161">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="856f3-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="856f3-162"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="856f3-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="856f3-163">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="856f3-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="856f3-164"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="856f3-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="856f3-165">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="856f3-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="856f3-166"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="856f3-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="856f3-167">實作為 <strong>JetGetAttachInfoW</strong> (Unicode) 和 <strong>JetGetAttachInfoA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="856f3-167">Implemented as <strong>JetGetAttachInfoW</strong> (Unicode) and <strong>JetGetAttachInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="856f3-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="856f3-168">See Also</span></span>

[<span data-ttu-id="856f3-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="856f3-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="856f3-170">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="856f3-170">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="856f3-171">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="856f3-171">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="856f3-172">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="856f3-172">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="856f3-173">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="856f3-173">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="856f3-174">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="856f3-174">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="856f3-175">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="856f3-175">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="856f3-176">JetStopService</span><span class="sxs-lookup"><span data-stu-id="856f3-176">JetStopService</span></span>](./jetstopservice-function.md)
