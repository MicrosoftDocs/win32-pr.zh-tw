---
description: 深入瞭解： JetTruncateLog 函數
title: JetTruncateLog 函式
TOCTitle: JetTruncateLog Function
ms:assetid: 60cbf563-4228-452a-9b20-c7b1330c4514
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269263(v=EXCHG.10)
ms:contentKeyID: 32765565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e196a1570f769d8ae2619e962521bb181d506d63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689916"
---
# <a name="jettruncatelog-function"></a><span data-ttu-id="93ff1-103">JetTruncateLog 函式</span><span class="sxs-lookup"><span data-stu-id="93ff1-103">JetTruncateLog Function</span></span>


<span data-ttu-id="93ff1-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="93ff1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncatelog-function"></a><span data-ttu-id="93ff1-105">JetTruncateLog 函式</span><span class="sxs-lookup"><span data-stu-id="93ff1-105">JetTruncateLog Function</span></span>

<span data-ttu-id="93ff1-106">**JetTruncateLog** 函式會在由 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)起始的備份期間使用，以刪除目前的備份成功完成後，將不再需要的任何交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="93ff1-106">The **JetTruncateLog** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLog(void);
```

### <a name="parameters"></a><span data-ttu-id="93ff1-107">參數</span><span class="sxs-lookup"><span data-stu-id="93ff1-107">Parameters</span></span>

<span data-ttu-id="93ff1-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="93ff1-108">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="93ff1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="93ff1-109">Return Value</span></span>

<span data-ttu-id="93ff1-110">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="93ff1-110">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="93ff1-111">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="93ff1-111">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93ff1-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="93ff1-112">Return code</span></span></p></th>
<th><p><span data-ttu-id="93ff1-113">Description</span><span class="sxs-lookup"><span data-stu-id="93ff1-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93ff1-114">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="93ff1-114">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="93ff1-115">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="93ff1-115">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ff1-116">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="93ff1-116">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="93ff1-117">作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="93ff1-117">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="93ff1-118"><strong>Windows Server 2003：</strong>  此傳回值是在 Windows Server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="93ff1-118"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ff1-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="93ff1-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="93ff1-120">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="93ff1-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ff1-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="93ff1-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="93ff1-122">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="93ff1-122">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="93ff1-123"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="93ff1-123"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ff1-124">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="93ff1-124">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="93ff1-125">備份作業失敗，因為它的呼叫順序不是。</span><span class="sxs-lookup"><span data-stu-id="93ff1-125">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="93ff1-126">如果有任何未處理的檔案控制代碼是針對實例使用<a href="gg269249(v=exchg.10).md">JetOpenFile</a>所建立， <strong>JetTruncateLog</strong>就會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="93ff1-126"><strong>JetTruncateLog</strong> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ff1-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="93ff1-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="93ff1-128">提供的其中一個參數包含未預期的值，或數個參數的組合產生了非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="93ff1-128">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="93ff1-129">當指定的實例控制碼無效時， <strong>JetTruncateLog</strong> 就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="93ff1-129">This can happen for <strong>JetTruncateLog</strong> when the specified instance handle is invalid.</span></span></p>
<p><span data-ttu-id="93ff1-130"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="93ff1-130"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ff1-131">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="93ff1-131">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="93ff1-132">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="93ff1-132">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ff1-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="93ff1-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="93ff1-134">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="93ff1-134">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ff1-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="93ff1-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="93ff1-136">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="93ff1-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ff1-137">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="93ff1-137">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="93ff1-138">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 只支援一個實例，而事實上有多個實例已經存在。</span><span class="sxs-lookup"><span data-stu-id="93ff1-138">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ff1-139">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="93ff1-139">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="93ff1-140">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="93ff1-140">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93ff1-141">如果此函式成功，則會刪除目前的備份成功完成後，將不再需要的交易記錄檔集合。</span><span class="sxs-lookup"><span data-stu-id="93ff1-141">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="93ff1-142">備份狀態電腦將會是最先進的，因此不再允許資料庫檔案的備份。</span><span class="sxs-lookup"><span data-stu-id="93ff1-142">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="93ff1-143">現在只允許開啟資料庫修補檔和交易記錄檔進行備份。</span><span class="sxs-lookup"><span data-stu-id="93ff1-143">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="93ff1-144">如果此函式失敗，備份狀態電腦可以是 advanced，使資料庫檔案的備份不再被允許。</span><span class="sxs-lookup"><span data-stu-id="93ff1-144">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="93ff1-145">可能會刪除一些小於所需數目的交易記錄檔，但一律會從最舊到最年輕刪除。</span><span class="sxs-lookup"><span data-stu-id="93ff1-145">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="93ff1-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="93ff1-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93ff1-147"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="93ff1-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="93ff1-148">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="93ff1-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ff1-149"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="93ff1-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="93ff1-150">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="93ff1-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ff1-151"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="93ff1-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="93ff1-152">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="93ff1-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93ff1-153"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="93ff1-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="93ff1-154">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="93ff1-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93ff1-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="93ff1-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="93ff1-156">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="93ff1-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="93ff1-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93ff1-157">See Also</span></span>

[<span data-ttu-id="93ff1-158">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="93ff1-158">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="93ff1-159">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="93ff1-159">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="93ff1-160">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="93ff1-160">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="93ff1-161">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="93ff1-161">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="93ff1-162">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="93ff1-162">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="93ff1-163">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="93ff1-163">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="93ff1-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="93ff1-164">JetStopService</span></span>](./jetstopservice-function.md)
