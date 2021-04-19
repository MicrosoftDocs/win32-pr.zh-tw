---
description: 深入瞭解： JetEscrowUpdate 函數
title: JetEscrowUpdate 函式
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978306"
---
# <a name="jetescrowupdate-function"></a><span data-ttu-id="10800-103">JetEscrowUpdate 函式</span><span class="sxs-lookup"><span data-stu-id="10800-103">JetEscrowUpdate Function</span></span>


<span data-ttu-id="10800-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="10800-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetescrowupdate-function"></a><span data-ttu-id="10800-105">JetEscrowUpdate 函式</span><span class="sxs-lookup"><span data-stu-id="10800-105">JetEscrowUpdate Function</span></span>

<span data-ttu-id="10800-106">**JetEscrowUpdate** 函數會在一個資料行上執行不可部分完成的加法運算。</span><span class="sxs-lookup"><span data-stu-id="10800-106">The **JetEscrowUpdate** function performs an atomic addition operation on one column.</span></span> <span data-ttu-id="10800-107">此函數可讓多個會話同時更新相同的記錄，而不會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="10800-107">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="10800-108">參數</span><span class="sxs-lookup"><span data-stu-id="10800-108">Parameters</span></span>

<span data-ttu-id="10800-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="10800-109">*sesid*</span></span>

<span data-ttu-id="10800-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="10800-110">The session to use for this call.</span></span>

<span data-ttu-id="10800-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="10800-111">*tableid*</span></span>

<span data-ttu-id="10800-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="10800-112">The cursor to use for this call.</span></span>

<span data-ttu-id="10800-113">*columnid*</span><span class="sxs-lookup"><span data-stu-id="10800-113">*columnid*</span></span>

<span data-ttu-id="10800-114">要更新之資料行的 *columnid* 。</span><span class="sxs-lookup"><span data-stu-id="10800-114">The *columnid* of the column to be updated.</span></span>

<span data-ttu-id="10800-115">*光伏*</span><span class="sxs-lookup"><span data-stu-id="10800-115">*pv*</span></span>

<span data-ttu-id="10800-116">包含資料行之加數的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="10800-116">A pointer to a buffer containing the addend for the column.</span></span>

<span data-ttu-id="10800-117">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="10800-117">*cbMax*</span></span>

<span data-ttu-id="10800-118">包含加數的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="10800-118">The size of the buffer containing the addend.</span></span>

<span data-ttu-id="10800-119">*pvOld*</span><span class="sxs-lookup"><span data-stu-id="10800-119">*pvOld*</span></span>

<span data-ttu-id="10800-120">將會忽略) 中儲存之資料行的目前值的輸出緩衝區， (版本控制。</span><span class="sxs-lookup"><span data-stu-id="10800-120">The output buffer that will receive the current value of the column as stored in the database (versioning is ignored).</span></span>

<span data-ttu-id="10800-121">*cbOldMax*</span><span class="sxs-lookup"><span data-stu-id="10800-121">*cbOldMax*</span></span>

<span data-ttu-id="10800-122">將接收資料行目前值的輸出緩衝區大小上限。</span><span class="sxs-lookup"><span data-stu-id="10800-122">The maximum size of the output buffer that will receive the current value of the column.</span></span> <span data-ttu-id="10800-123">目前只支援 JET_coltypLong，因此緩衝區的長度必須是4個位元組或0個位元組。</span><span class="sxs-lookup"><span data-stu-id="10800-123">Currently only JET_coltypLong is supported, so the buffer must either be 4 bytes or 0 bytes in length.</span></span> <span data-ttu-id="10800-124">如果 *pvOld* 為 Null，則 *cbOldMax* 應為0。</span><span class="sxs-lookup"><span data-stu-id="10800-124">If *pvOld* is NULL then *cbOldMax* should be 0.</span></span>

<span data-ttu-id="10800-125">*pcbOldActual*</span><span class="sxs-lookup"><span data-stu-id="10800-125">*pcbOldActual*</span></span>

<span data-ttu-id="10800-126">接收輸出緩衝區中所接收的實際原始值資料量。</span><span class="sxs-lookup"><span data-stu-id="10800-126">Receives the actual amount of raw value data received in the output buffer.</span></span>

<span data-ttu-id="10800-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="10800-127">*grbit*</span></span>

<span data-ttu-id="10800-128">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="10800-128">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10800-129">值</span><span class="sxs-lookup"><span data-stu-id="10800-129">Value</span></span></p></th>
<th><p><span data-ttu-id="10800-130">意義</span><span class="sxs-lookup"><span data-stu-id="10800-130">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10800-131">JET_bitEscrowNoRollback</span><span class="sxs-lookup"><span data-stu-id="10800-131">JET_bitEscrowNoRollback</span></span></p></td>
<td><p><span data-ttu-id="10800-132">即使執行保管更新的會話具有其交易回復，但這種更新將不會復原。</span><span class="sxs-lookup"><span data-stu-id="10800-132">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="10800-133">請注意，因為記錄檔記錄可能不會排清到磁片，所以使用此旗標完成的最新的證書處理更新可能會在發生損毀時遺失。</span><span class="sxs-lookup"><span data-stu-id="10800-133">Note that as the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="10800-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="10800-134">Return Value</span></span>

<span data-ttu-id="10800-135">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="10800-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="10800-136">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="10800-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10800-137">傳回碼</span><span class="sxs-lookup"><span data-stu-id="10800-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="10800-138">Description</span><span class="sxs-lookup"><span data-stu-id="10800-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10800-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="10800-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="10800-140">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="10800-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-141">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="10800-141">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="10800-142">資料指標具有以 <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>準備的更新。</span><span class="sxs-lookup"><span data-stu-id="10800-142">The cursor has an update prepared with <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="10800-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="10800-144">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="10800-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-145">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="10800-145">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="10800-146">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="10800-146">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="10800-147">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="10800-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-148">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="10800-148">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="10800-149">傳入了不正確緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="10800-149">An invalid buffer size has been passed in.</span></span> <span data-ttu-id="10800-150">目前只支援 JET_coltypLong，因此緩衝區必須是4個位元組。</span><span class="sxs-lookup"><span data-stu-id="10800-150">Currently only JET_coltypLong is supported, so the buffer must be 4 bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="10800-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="10800-152">指定了不正確資料行。</span><span class="sxs-lookup"><span data-stu-id="10800-152">An invalid column has been specified.</span></span> <span data-ttu-id="10800-153">必須使用指定的 JET_bitColumnEscrowUpdate 來建立資料行。</span><span class="sxs-lookup"><span data-stu-id="10800-153">The column must be created with JET_bitColumnEscrowUpdate specified.</span></span> <span data-ttu-id="10800-154">只有 JET_coltypLong 的固定資料行可以指定為可更新的可更新資料行。</span><span class="sxs-lookup"><span data-stu-id="10800-154">Only fixed columns of JET_coltypLong can be specified as escrow updateable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="10800-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="10800-156">資料指標必須在記錄上，才能更新資料行。</span><span class="sxs-lookup"><span data-stu-id="10800-156">Cursor must be on a record in order to update a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-157">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="10800-157">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="10800-158">交易更新只能由交易中的會話執行。</span><span class="sxs-lookup"><span data-stu-id="10800-158">Escrow updates can only be performed by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="10800-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="10800-160">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="10800-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-161">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="10800-161">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="10800-162">資料指標不能是唯讀的，而是更新記錄。</span><span class="sxs-lookup"><span data-stu-id="10800-162">Cursor cannot be read only and update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-163">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="10800-163">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="10800-164">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="10800-164">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-165">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="10800-165">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="10800-166">相同的會話無法同時從一個以上的執行緒使用。</span><span class="sxs-lookup"><span data-stu-id="10800-166">The same session cannot be used from more than one thread at the same time.</span></span> <span data-ttu-id="10800-167">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="10800-167">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-168">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="10800-168">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="10800-169">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="10800-169">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-170">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="10800-170">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="10800-171">會話必須有寫入權限，才能更新記錄。</span><span class="sxs-lookup"><span data-stu-id="10800-171">Session must have write permissions to update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-172">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="10800-172">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="10800-173">要求衝突更新時傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="10800-173">The error returned when a conflicting update is requested.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="10800-174">備註</span><span class="sxs-lookup"><span data-stu-id="10800-174">Remarks</span></span>

<span data-ttu-id="10800-175">一般來說，如果兩個會話嘗試同時更新記錄，除非會話已完全序列化，否則第二個會話會收到 JET_errWriteConflict 錯誤。</span><span class="sxs-lookup"><span data-stu-id="10800-175">Normally, if two sessions attempt to update a record simultaneously, the second session will receive a JET_errWriteConflict error unless the sessions are completely serialized.</span></span> <span data-ttu-id="10800-176">若要將兩個更新相同記錄的會話序列化，第二個會話必須在第一次交易認可交易之後啟動其交易。</span><span class="sxs-lookup"><span data-stu-id="10800-176">To serialize two sessions that update the same record, the second session must start its transaction after the first transaction commits its transaction.</span></span> <span data-ttu-id="10800-177">如需詳細資訊，請參閱 [JetBeginTransaction](./jetbegintransaction-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="10800-177">See [JetBeginTransaction](./jetbegintransaction-function.md) for more information.</span></span>

<span data-ttu-id="10800-178">相同記錄中的多個資料行可以進行證書更新。</span><span class="sxs-lookup"><span data-stu-id="10800-178">Multiple columns in the same record can be escrow updated.</span></span> <span data-ttu-id="10800-179">這些更新不會影響彼此。</span><span class="sxs-lookup"><span data-stu-id="10800-179">The updates do not affect each other.</span></span>

<span data-ttu-id="10800-180">只有 **JetEscrowUpdate** 作業會彼此相容。</span><span class="sxs-lookup"><span data-stu-id="10800-180">Only **JetEscrowUpdate** operations are compatible with each other.</span></span> <span data-ttu-id="10800-181">如果有兩個不同的會話嘗試準備更新或刪除相同的記錄，則會產生寫入衝突。</span><span class="sxs-lookup"><span data-stu-id="10800-181">If two different sessions try to prepare updates or delete the same record, a write conflict will be generated.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p><span data-ttu-id="10800-182">會話 B</span><span class="sxs-lookup"><span data-stu-id="10800-182">Session B</span></span><br /><span data-ttu-id="10800-183">
<strong>JetEscrowUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="10800-183">
<strong>JetEscrowUpdate</strong></span></span></p></th>
<th><p><span data-ttu-id="10800-184"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></span><span class="sxs-lookup"><span data-stu-id="10800-184"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></span></span></p></th>
<th><p><span data-ttu-id="10800-185"><a href="gg269315(v=exchg.10).md">JetDelete</a></span><span class="sxs-lookup"><span data-stu-id="10800-185"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="10800-186"><strong>JetEscrowUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="10800-186"><strong>JetEscrowUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="10800-187">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="10800-187">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="10800-188">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="10800-188">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="10800-189">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="10800-189">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="10800-190"><a href="gg269288(v=exchg.10).md">JetUpdate</a></span><span class="sxs-lookup"><span data-stu-id="10800-190"><a href="gg269288(v=exchg.10).md">JetUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="10800-191">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="10800-191">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="10800-192">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="10800-192">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="10800-193">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="10800-193">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-194">會話 A</span><span class="sxs-lookup"><span data-stu-id="10800-194">Session A</span></span></p></td>
<td><p><span data-ttu-id="10800-195"><a href="gg269315(v=exchg.10).md">JetDelete</a></span><span class="sxs-lookup"><span data-stu-id="10800-195"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></td>
<td><p><span data-ttu-id="10800-196">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="10800-196">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="10800-197">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="10800-197">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="10800-198">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="10800-198">JET_errWriteConflict</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10800-199">除非 JET_bitEscrowNoRollback 是) 指定的，否則會使用 [JetRollback](./jetrollback-function.md) (來建立版本的託管作業。</span><span class="sxs-lookup"><span data-stu-id="10800-199">Escrow operations are versioned and are undone using [JetRollback](./jetrollback-function.md) (unless JET_bitEscrowNoRollback was specified).</span></span> <span data-ttu-id="10800-200">**JetEscrowUpdate** 會傳回儲存在資料庫中之資料行的原始值，因為應用程式可能會想要在叫用 sentinel 值時執行特殊動作。</span><span class="sxs-lookup"><span data-stu-id="10800-200">**JetEscrowUpdate** returns the raw value of the column stored in the database, because an application may want to perform a special action when a sentinel value is hit.</span></span> <span data-ttu-id="10800-201">[JetRetrieveColumn](./jetretrievecolumn-function.md) 會傳回正確設定資料行版本的視圖，並忽略並行會話所做的更新。</span><span class="sxs-lookup"><span data-stu-id="10800-201">[JetRetrieveColumn](./jetretrievecolumn-function.md) returns the correctly versioned view of the column, ignoring updates made by concurrent sessions.</span></span>

<span data-ttu-id="10800-202">假設有兩個會話在相同記錄的相同資料行上運作，我們可以查看其運作方式。</span><span class="sxs-lookup"><span data-stu-id="10800-202">Given two sessions operating on the same column of the same record, we can see how this works.</span></span> <span data-ttu-id="10800-203">假設資料行的開頭值為0。</span><span class="sxs-lookup"><span data-stu-id="10800-203">Assume the column starts with a value of 0.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10800-204">工作階段</span><span class="sxs-lookup"><span data-stu-id="10800-204">Session</span></span></p></th>
<th><p><span data-ttu-id="10800-205">作業</span><span class="sxs-lookup"><span data-stu-id="10800-205">Operation</span></span></p></th>
<th><p><span data-ttu-id="10800-206">儲存的值</span><span class="sxs-lookup"><span data-stu-id="10800-206">Stored value</span></span></p></th>
<th><p><span data-ttu-id="10800-207">傳回值</span><span class="sxs-lookup"><span data-stu-id="10800-207">Returned value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10800-208">A</span><span class="sxs-lookup"><span data-stu-id="10800-208">A</span></span></p></td>
<td><p><span data-ttu-id="10800-209"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span><span class="sxs-lookup"><span data-stu-id="10800-209"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-210">A</span><span class="sxs-lookup"><span data-stu-id="10800-210">A</span></span></p></td>
<td><p><span data-ttu-id="10800-211"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span><span class="sxs-lookup"><span data-stu-id="10800-211"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="10800-212">0</span><span class="sxs-lookup"><span data-stu-id="10800-212">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-213">A</span><span class="sxs-lookup"><span data-stu-id="10800-213">A</span></span></p></td>
<td><p><span data-ttu-id="10800-214"><strong>JetEscrowUpdate</strong> (4) </span><span class="sxs-lookup"><span data-stu-id="10800-214"><strong>JetEscrowUpdate</strong> (4)</span></span></p></td>
<td><p><span data-ttu-id="10800-215">4</span><span class="sxs-lookup"><span data-stu-id="10800-215">4</span></span></p></td>
<td><p><span data-ttu-id="10800-216">0</span><span class="sxs-lookup"><span data-stu-id="10800-216">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-217">A</span><span class="sxs-lookup"><span data-stu-id="10800-217">A</span></span></p></td>
<td><p><span data-ttu-id="10800-218"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="10800-218"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="10800-219">4</span><span class="sxs-lookup"><span data-stu-id="10800-219">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-220">B</span><span class="sxs-lookup"><span data-stu-id="10800-220">B</span></span></p></td>
<td><p><span data-ttu-id="10800-221"><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></span><span class="sxs-lookup"><span data-stu-id="10800-221"><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-222">B</span><span class="sxs-lookup"><span data-stu-id="10800-222">B</span></span></p></td>
<td><p><span data-ttu-id="10800-223"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="10800-223"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="10800-224">0</span><span class="sxs-lookup"><span data-stu-id="10800-224">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-225">B</span><span class="sxs-lookup"><span data-stu-id="10800-225">B</span></span></p></td>
<td><p><span data-ttu-id="10800-226"><strong>JetEscrowUpdate</strong> (3) </span><span class="sxs-lookup"><span data-stu-id="10800-226"><strong>JetEscrowUpdate</strong> (3)</span></span></p></td>
<td><p><span data-ttu-id="10800-227">7</span><span class="sxs-lookup"><span data-stu-id="10800-227">7</span></span></p></td>
<td><p><span data-ttu-id="10800-228">4</span><span class="sxs-lookup"><span data-stu-id="10800-228">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-229">B</span><span class="sxs-lookup"><span data-stu-id="10800-229">B</span></span></p></td>
<td><p><span data-ttu-id="10800-230"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="10800-230"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="10800-231">3</span><span class="sxs-lookup"><span data-stu-id="10800-231">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-232">A</span><span class="sxs-lookup"><span data-stu-id="10800-232">A</span></span></p></td>
<td><p><span data-ttu-id="10800-233"><strong>JetEscrowUpdate</strong> (2) </span><span class="sxs-lookup"><span data-stu-id="10800-233"><strong>JetEscrowUpdate</strong> (2)</span></span></p></td>
<td><p><span data-ttu-id="10800-234">9</span><span class="sxs-lookup"><span data-stu-id="10800-234">9</span></span></p></td>
<td><p><span data-ttu-id="10800-235">7</span><span class="sxs-lookup"><span data-stu-id="10800-235">7</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-236">A</span><span class="sxs-lookup"><span data-stu-id="10800-236">A</span></span></p></td>
<td><p><span data-ttu-id="10800-237"><strong>JetEscrowUpdate</strong> (-7) </span><span class="sxs-lookup"><span data-stu-id="10800-237"><strong>JetEscrowUpdate</strong> (-7)</span></span></p></td>
<td><p><span data-ttu-id="10800-238">2</span><span class="sxs-lookup"><span data-stu-id="10800-238">2</span></span></p></td>
<td><p><span data-ttu-id="10800-239">9</span><span class="sxs-lookup"><span data-stu-id="10800-239">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-240">B</span><span class="sxs-lookup"><span data-stu-id="10800-240">B</span></span></p></td>
<td><p><span data-ttu-id="10800-241"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="10800-241"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="10800-242">3</span><span class="sxs-lookup"><span data-stu-id="10800-242">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-243">A</span><span class="sxs-lookup"><span data-stu-id="10800-243">A</span></span></p></td>
<td><p><span data-ttu-id="10800-244"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="10800-244"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="10800-245">-1</span><span class="sxs-lookup"><span data-stu-id="10800-245">-1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-246">B</span><span class="sxs-lookup"><span data-stu-id="10800-246">B</span></span></p></td>
<td><p><span data-ttu-id="10800-247"><a href="gg269273(v=exchg.10).md">JetRollback</a></span><span class="sxs-lookup"><span data-stu-id="10800-247"><a href="gg269273(v=exchg.10).md">JetRollback</a></span></span></p></td>
<td><p><span data-ttu-id="10800-248">-1</span><span class="sxs-lookup"><span data-stu-id="10800-248">-1</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-249">A</span><span class="sxs-lookup"><span data-stu-id="10800-249">A</span></span></p></td>
<td><p><span data-ttu-id="10800-250"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="10800-250"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="10800-251">-1</span><span class="sxs-lookup"><span data-stu-id="10800-251">-1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10800-252">不建議將執行交易更新的相同交易中的記錄取代為記錄。</span><span class="sxs-lookup"><span data-stu-id="10800-252">Replacing a record in the same transaction that performs escrow updates to a record is not recommended.</span></span> <span data-ttu-id="10800-253">尤其是，如果記錄上的更新是以一個 [JET_TABLEID](./jet-tableid.md) 準備，而另一個 [JET_TABLEID](./jet-tableid.md) 用來將更新記錄，則在呼叫 [JetUpdate](./jetupdate-function.md) 時，將會遺失已更新的保管。</span><span class="sxs-lookup"><span data-stu-id="10800-253">In particular, if an update on a record is prepared with one [JET_TABLEID](./jet-tableid.md) and a different [JET_TABLEID](./jet-tableid.md) is used to escrow update the record then the escrow updated will be lost when [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="10800-254">即使在更新期間未設定「託管」資料行，也會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="10800-254">This happens even if the escrow column was not set during the update.</span></span>

<span data-ttu-id="10800-255">當可更新的可更新資料行值為零時，就可以觸發特殊的行為。</span><span class="sxs-lookup"><span data-stu-id="10800-255">When an escrow updateable column has a value of zero, special behavior can be triggered.</span></span> <span data-ttu-id="10800-256">只有當 **JetEscrowUpdate** 作業導致資料行的值為零時，才會發生這種行為。</span><span class="sxs-lookup"><span data-stu-id="10800-256">This behavior only happens if a **JetEscrowUpdate** operation causes the column to have a value of zero.</span></span> <span data-ttu-id="10800-257">動作不會立即發生，但會在造成資料行值為零之交易之後的某段時間發生。</span><span class="sxs-lookup"><span data-stu-id="10800-257">The action does not happen immediately, but occurs sometime after the transaction which caused the column to have a value of zero commits.</span></span> <span data-ttu-id="10800-258">資料行的值仍然必須為零 (也就是，如果沒有任何其他會話修改了資料行) 。</span><span class="sxs-lookup"><span data-stu-id="10800-258">The column must still have a value of zero (that is, if no other sessions have modified the column).</span></span> <span data-ttu-id="10800-259">如果資料行是使用 JET_bitColumnDeleteOnZero 建立的，將會刪除包含此資料行的記錄。</span><span class="sxs-lookup"><span data-stu-id="10800-259">If the column was created with JET_bitColumnDeleteOnZero, the record containing the column will be deleted.</span></span> <span data-ttu-id="10800-260">如果資料行是使用 JET_bitColumnFinalize 所建立，則會發出回呼。</span><span class="sxs-lookup"><span data-stu-id="10800-260">If the column was created with JET_bitColumnFinalize then a callback will be issued.</span></span> <span data-ttu-id="10800-261">損毀可能會導致這些動作不會發生，但是 (使用 [JetDefragment](./jetdefragment-function.md) 函式的線上維護) 將會正確地重做動作。</span><span class="sxs-lookup"><span data-stu-id="10800-261">A crash may cause these actions not to happen, but online maintenance (using the [JetDefragment](./jetdefragment-function.md) function) will correctly redo the actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="10800-262">規格需求</span><span class="sxs-lookup"><span data-stu-id="10800-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10800-263"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="10800-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="10800-264">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="10800-264">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-265"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="10800-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="10800-266">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="10800-266">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-267"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="10800-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="10800-268">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="10800-268">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10800-269"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="10800-269"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="10800-270">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="10800-270">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10800-271"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="10800-271"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="10800-272">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="10800-272">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="10800-273">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10800-273">See Also</span></span>

[<span data-ttu-id="10800-274">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="10800-274">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="10800-275">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="10800-275">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="10800-276">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="10800-276">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="10800-277">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="10800-277">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="10800-278">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="10800-278">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="10800-279">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="10800-279">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="10800-280">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="10800-280">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="10800-281">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="10800-281">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="10800-282">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="10800-282">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="10800-283">JetRollback</span><span class="sxs-lookup"><span data-stu-id="10800-283">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="10800-284">JetStopService</span><span class="sxs-lookup"><span data-stu-id="10800-284">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="10800-285">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="10800-285">JetUpdate</span></span>](./jetupdate-function.md)
