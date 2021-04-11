---
description: 深入瞭解： JetGetLock 函數
title: JetGetLock 函式
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5757616214336de25ce30ca49755ac229b10afbe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104116317"
---
# <a name="jetgetlock-function"></a><span data-ttu-id="f5af2-103">JetGetLock 函式</span><span class="sxs-lookup"><span data-stu-id="f5af2-103">JetGetLock Function</span></span>


<span data-ttu-id="f5af2-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f5af2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetlock-function"></a><span data-ttu-id="f5af2-105">JetGetLock 函式</span><span class="sxs-lookup"><span data-stu-id="f5af2-105">JetGetLock Function</span></span>

<span data-ttu-id="f5af2-106">**JetGetLock** 函式會提供一種方法來明確保留更新資料列、寫入鎖定的能力，或是明確防止任何其他會話、讀取鎖定更新資料列。</span><span class="sxs-lookup"><span data-stu-id="f5af2-106">The **JetGetLock** function provides a means to explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="f5af2-107">一般來說，資料列寫入鎖定是以隱含方式取得，因為更新資料列的結果。</span><span class="sxs-lookup"><span data-stu-id="f5af2-107">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="f5af2-108">由於記錄版本控制，通常不需要讀取鎖定。</span><span class="sxs-lookup"><span data-stu-id="f5af2-108">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="f5af2-109">不過，在某些情況下，交易可能會想要明確地鎖定資料列以強制執行序列化，或確保後續的作業會成功，因為已採取必要的鎖定。</span><span class="sxs-lookup"><span data-stu-id="f5af2-109">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed by virtue that required locks have already been taken.</span></span>

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="f5af2-110">參數</span><span class="sxs-lookup"><span data-stu-id="f5af2-110">Parameters</span></span>

<span data-ttu-id="f5af2-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f5af2-111">*sesid*</span></span>

<span data-ttu-id="f5af2-112">此呼叫將使用的會話。</span><span class="sxs-lookup"><span data-stu-id="f5af2-112">The session that will be used for this call.</span></span>

<span data-ttu-id="f5af2-113">*tableid*</span><span class="sxs-lookup"><span data-stu-id="f5af2-113">*tableid*</span></span>

<span data-ttu-id="f5af2-114">將用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="f5af2-114">The cursor that will be used for this call.</span></span>

<span data-ttu-id="f5af2-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f5af2-115">*grbit*</span></span>

<span data-ttu-id="f5af2-116">位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列各項：</span><span class="sxs-lookup"><span data-stu-id="f5af2-116">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f5af2-117">值</span><span class="sxs-lookup"><span data-stu-id="f5af2-117">Value</span></span></p></th>
<th><p><span data-ttu-id="f5af2-118">意義</span><span class="sxs-lookup"><span data-stu-id="f5af2-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5af2-119">JET_bitReadLock</span><span class="sxs-lookup"><span data-stu-id="f5af2-119">JET_bitReadLock</span></span></p></td>
<td><p><span data-ttu-id="f5af2-120">此旗標會在目前的記錄上取得讀取鎖定。</span><span class="sxs-lookup"><span data-stu-id="f5af2-120">This flag causes a read lock to be acquired on the current record.</span></span> <span data-ttu-id="f5af2-121">讀取鎖定與其他會話已保留的寫入鎖定不相容，但與其他會話所持有的讀取鎖定相容。</span><span class="sxs-lookup"><span data-stu-id="f5af2-121">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5af2-122">JET_bitWriteLock</span><span class="sxs-lookup"><span data-stu-id="f5af2-122">JET_bitWriteLock</span></span></p></td>
<td><p><span data-ttu-id="f5af2-123">此旗標會在目前的記錄上取得寫入鎖定。</span><span class="sxs-lookup"><span data-stu-id="f5af2-123">This flag causes a write lock to be acquired on the current record.</span></span> <span data-ttu-id="f5af2-124">寫入鎖定與其他會話所持有的寫入或讀取鎖定不相容，但與相同會話所持有的讀取鎖定相容。</span><span class="sxs-lookup"><span data-stu-id="f5af2-124">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f5af2-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5af2-125">Return Value</span></span>

<span data-ttu-id="f5af2-126">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="f5af2-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f5af2-127">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="f5af2-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f5af2-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f5af2-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="f5af2-129">Description</span><span class="sxs-lookup"><span data-stu-id="f5af2-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5af2-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f5af2-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f5af2-131">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f5af2-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5af2-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f5af2-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f5af2-133">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="f5af2-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5af2-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f5af2-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f5af2-135">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="f5af2-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="f5af2-136">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5af2-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5af2-137">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="f5af2-137">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="f5af2-138">指定的 <em>grbit</em> 不是 JET_bitReadLock 或 JET_bitWriteLock。</span><span class="sxs-lookup"><span data-stu-id="f5af2-138">The given <em>grbit</em> is neither JET_bitReadLock or JET_bitWriteLock.</span></span> <span data-ttu-id="f5af2-139">它必須是這兩個旗標的其中一個。</span><span class="sxs-lookup"><span data-stu-id="f5af2-139">It must be one of these two flags.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5af2-140">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="f5af2-140">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="f5af2-141">資料指標必須在記錄上，才能取得鎖定。</span><span class="sxs-lookup"><span data-stu-id="f5af2-141">Cursor must be on a record in order to acquire a lock.</span></span> <span data-ttu-id="f5af2-142">鎖定一律為 on 記錄。</span><span class="sxs-lookup"><span data-stu-id="f5af2-142">Locks are always on records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5af2-143">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f5af2-143">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f5af2-144">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="f5af2-144">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5af2-145">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="f5af2-145">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="f5af2-146">鎖定只能由交易中的會話取得。</span><span class="sxs-lookup"><span data-stu-id="f5af2-146">Locks can only be acquired by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5af2-147">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="f5af2-147">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="f5af2-148">資料指標不可以是唯讀的，而是取得寫入鎖定。</span><span class="sxs-lookup"><span data-stu-id="f5af2-148">Cursor cannot be read only and acquire a write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5af2-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f5af2-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f5af2-150">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="f5af2-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5af2-151">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f5af2-151">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="f5af2-152">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="f5af2-152">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="f5af2-153">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5af2-153">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5af2-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f5af2-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f5af2-155">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="f5af2-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5af2-156">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="f5af2-156">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="f5af2-157">會話必須有寫入權限，才能取得寫入鎖定。</span><span class="sxs-lookup"><span data-stu-id="f5af2-157">Session must have write permissions to acquire write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5af2-158">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="f5af2-158">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="f5af2-159">要求衝突鎖定時傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5af2-159">The error returned when a conflicting lock is requested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f5af2-160">成功時，會話已取得要求的鎖定。</span><span class="sxs-lookup"><span data-stu-id="f5af2-160">On success, session has acquired requested lock.</span></span>

<span data-ttu-id="f5af2-161">失敗時，會話尚未取得要求的鎖定。</span><span class="sxs-lookup"><span data-stu-id="f5af2-161">On failure, session has not acquired requested lock.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f5af2-162">備註</span><span class="sxs-lookup"><span data-stu-id="f5af2-162">Remarks</span></span>

<span data-ttu-id="f5af2-163">無法使用具有唯讀許可權的會話或資料指標取得寫入鎖定，即使會話和資料指標最終不會執行更新作業。</span><span class="sxs-lookup"><span data-stu-id="f5af2-163">Write locks cannot be acquired with sessions or cursors that have read-only permissions, even if the session and cursor ultimately do not perform an update operation.</span></span> <span data-ttu-id="f5af2-164">會話和資料指標都必須有寫入權限，才能取得寫入鎖定。</span><span class="sxs-lookup"><span data-stu-id="f5af2-164">Both the session and the cursor must have write privileges in order to acquire a write lock.</span></span>

<span data-ttu-id="f5af2-165">讀取和寫入鎖定是一種封閉式鎖定的方式。</span><span class="sxs-lookup"><span data-stu-id="f5af2-165">Read and write locks are a means of pessimistic locking.</span></span> <span data-ttu-id="f5af2-166">封閉式鎖定預期會有多個並行會話衝突並事先取得鎖定，以確保其作業成功。</span><span class="sxs-lookup"><span data-stu-id="f5af2-166">Pessimistic locking expects multiple concurrent sessions to conflict and acquire locks in advance to ensure that their operations succeed.</span></span>

<span data-ttu-id="f5af2-167">大部分的作業都可透過隱含採用鎖定的方式進行序列化。</span><span class="sxs-lookup"><span data-stu-id="f5af2-167">Most operations will be serializable by virtue of locks implicitly taken.</span></span> <span data-ttu-id="f5af2-168">不過，某些作業將不會。</span><span class="sxs-lookup"><span data-stu-id="f5af2-168">However, some operations will not.</span></span> <span data-ttu-id="f5af2-169">為了說明這一點，請考慮兩個交易：</span><span class="sxs-lookup"><span data-stu-id="f5af2-169">To illustrate this, consider the two transactions,</span></span>

<span data-ttu-id="f5af2-170">T1： R () 、U (B) </span><span class="sxs-lookup"><span data-stu-id="f5af2-170">T1 : R(A), U(B)</span></span>

<span data-ttu-id="f5af2-171">T2： R (B) ，U (A) </span><span class="sxs-lookup"><span data-stu-id="f5af2-171">T2 : R(B), U(A)</span></span>

<span data-ttu-id="f5af2-172">記錄層級版本控制會確保同時執行的每個交易都會看到 A 和 B 的原始值。在結果相依于讀取資料的情況下，不會執行任何序列順序來產生 A 和 B 的相同結果。</span><span class="sxs-lookup"><span data-stu-id="f5af2-172">Record level versioning will ensure that each transaction when executed concurrently will see the original values for A and B. There is no serial order of execution that could produce the same results for A and B in the case that the results are dependent upon the data read.</span></span> <span data-ttu-id="f5af2-173">為了讓應用程式能夠序列化此交易，在讀取值時，應該會在每個交易中取得 A 和 B 的明確讀取鎖定。</span><span class="sxs-lookup"><span data-stu-id="f5af2-173">In order for the application to make this transaction serializable, it should acquire an explicit read lock on A and B in each transaction when the value is read.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f5af2-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5af2-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f5af2-175"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="f5af2-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f5af2-176">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="f5af2-176">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5af2-177"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="f5af2-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f5af2-178">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="f5af2-178">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5af2-179"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="f5af2-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f5af2-180">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="f5af2-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f5af2-181"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="f5af2-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f5af2-182">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="f5af2-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f5af2-183"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f5af2-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f5af2-184">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="f5af2-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f5af2-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5af2-185">See Also</span></span>

[<span data-ttu-id="f5af2-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f5af2-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f5af2-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f5af2-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f5af2-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f5af2-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f5af2-189">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="f5af2-189">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="f5af2-190">JetStopService</span><span class="sxs-lookup"><span data-stu-id="f5af2-190">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="f5af2-191">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="f5af2-191">JetUpdate</span></span>](./jetupdate-function.md)
