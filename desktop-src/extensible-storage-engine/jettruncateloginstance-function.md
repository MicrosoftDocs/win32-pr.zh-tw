---
description: 深入瞭解： JetTruncateLogInstance 函數
title: JetTruncateLogInstance 函式
TOCTitle: JetTruncateLogInstance Function
ms:assetid: 9b6852c6-a991-4d7b-bc54-49092f788751
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269352(v=EXCHG.10)
ms:contentKeyID: 32765639
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLogInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7286b97b80c323eb6bba7b9d28057bf45eec3920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985613"
---
# <a name="jettruncateloginstance-function"></a><span data-ttu-id="437d6-103">JetTruncateLogInstance 函式</span><span class="sxs-lookup"><span data-stu-id="437d6-103">JetTruncateLogInstance Function</span></span>


<span data-ttu-id="437d6-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="437d6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncateloginstance-function"></a><span data-ttu-id="437d6-105">JetTruncateLogInstance 函式</span><span class="sxs-lookup"><span data-stu-id="437d6-105">JetTruncateLogInstance Function</span></span>

<span data-ttu-id="437d6-106">**JetTruncateLogInstance** 函式是在由 [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)所起始的備份期間，用來刪除目前的備份成功完成後，將不再需要的任何交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="437d6-106">The **JetTruncateLogInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="437d6-107">**Windows xp：**  **JetTruncateLogInstance** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="437d6-107">**Windows XP:**  **JetTruncateLogInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLogInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="437d6-108">參數</span><span class="sxs-lookup"><span data-stu-id="437d6-108">Parameters</span></span>

<span data-ttu-id="437d6-109">*實例*</span><span class="sxs-lookup"><span data-stu-id="437d6-109">*instance*</span></span>

<span data-ttu-id="437d6-110">此呼叫所要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="437d6-110">The instance to use for this call.</span></span>

<span data-ttu-id="437d6-111">針對 Windows 2000，無法使用接受此參數的 API 變體，因為只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="437d6-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="437d6-112">在此情況下，這種全域實例的使用是隱含的。</span><span class="sxs-lookup"><span data-stu-id="437d6-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="437d6-113">若為 Windows XP 和更新版本，則只有在引擎處於舊版模式時，才會呼叫不接受這個參數的 API 變數 (Windows 2000 相容性模式) 只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="437d6-113">For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="437d6-114">否則，作業將會失敗，並 JET_errRunningInMultiInstanceMode。</span><span class="sxs-lookup"><span data-stu-id="437d6-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="437d6-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="437d6-115">Return Value</span></span>

<span data-ttu-id="437d6-116">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="437d6-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="437d6-117">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="437d6-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="437d6-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="437d6-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="437d6-119">Description</span><span class="sxs-lookup"><span data-stu-id="437d6-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="437d6-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="437d6-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="437d6-121">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="437d6-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="437d6-122">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="437d6-122">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="437d6-123"><strong>Windows Server 2003：</strong>  此傳回值是在 Windows Server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="437d6-123"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="437d6-124">作業失敗，因為目前的外部備份已被 <a href="gg294067(v=exchg.10).md">JetStopBackup</a>的呼叫中止。</span><span class="sxs-lookup"><span data-stu-id="437d6-124">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="437d6-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="437d6-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="437d6-126">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="437d6-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="437d6-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="437d6-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="437d6-128">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="437d6-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="437d6-129">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="437d6-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="437d6-130">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="437d6-130">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="437d6-131">備份作業失敗，因為它的呼叫順序不是。</span><span class="sxs-lookup"><span data-stu-id="437d6-131">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="437d6-132">如果有任何未處理的檔案控制代碼是針對實例使用<a href="gg269249(v=exchg.10).md">JetOpenFile</a>所建立， <a href="gg269263(v=exchg.10).md">JetTruncateLog</a>就會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="437d6-132"><a href="gg269263(v=exchg.10).md">JetTruncateLog</a> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="437d6-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="437d6-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="437d6-134">提供的其中一個參數包含未預期的值，或數個參數的組合產生了非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="437d6-134">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="437d6-135">當指定的實例控制碼無效時， <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> 就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="437d6-135">This can happen for <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="437d6-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="437d6-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="437d6-137">作業失敗，因為沒有任何外部備份正在進行中。</span><span class="sxs-lookup"><span data-stu-id="437d6-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="437d6-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="437d6-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="437d6-139">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="437d6-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="437d6-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="437d6-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="437d6-141">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="437d6-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="437d6-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="437d6-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="437d6-143">作業失敗，因為嘗試使用舊版模式中的引擎 (Windows 2000 相容性模式) 在事實中，如果有多個實例存在，則只支援一個實例。</span><span class="sxs-lookup"><span data-stu-id="437d6-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="437d6-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="437d6-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="437d6-145">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="437d6-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="437d6-146">如果此函式成功，則會刪除目前的備份成功完成後，將不再需要的交易記錄檔集合。</span><span class="sxs-lookup"><span data-stu-id="437d6-146">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="437d6-147">備份狀態電腦將會是最先進的，因此不再允許資料庫檔案的備份。</span><span class="sxs-lookup"><span data-stu-id="437d6-147">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="437d6-148">現在只允許開啟資料庫修補檔和交易記錄檔進行備份。</span><span class="sxs-lookup"><span data-stu-id="437d6-148">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="437d6-149">如果此函式失敗，備份狀態電腦可以是 advanced，使資料庫檔案的備份不再被允許。</span><span class="sxs-lookup"><span data-stu-id="437d6-149">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="437d6-150">可能會刪除一些小於所需數目的交易記錄檔，但一律會從最舊到最年輕刪除。</span><span class="sxs-lookup"><span data-stu-id="437d6-150">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="437d6-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="437d6-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="437d6-152"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="437d6-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="437d6-153">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="437d6-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="437d6-154"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="437d6-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="437d6-155">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="437d6-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="437d6-156"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="437d6-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="437d6-157">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="437d6-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="437d6-158"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="437d6-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="437d6-159">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="437d6-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="437d6-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="437d6-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="437d6-161">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="437d6-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="437d6-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="437d6-162">See Also</span></span>

[<span data-ttu-id="437d6-163">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="437d6-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="437d6-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="437d6-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="437d6-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="437d6-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="437d6-166">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="437d6-166">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="437d6-167">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="437d6-167">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="437d6-168">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="437d6-168">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="437d6-169">JetStopService</span><span class="sxs-lookup"><span data-stu-id="437d6-169">JetStopService</span></span>](./jetstopservice-function.md)
