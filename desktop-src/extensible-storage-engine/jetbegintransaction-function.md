---
description: 深入瞭解： JetBeginTransaction 函數
title: JetBeginTransaction 函式
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd5986d2e9e8e3c65fa472f37e8d92c4afbb4803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318043"
---
# <a name="jetbegintransaction-function"></a><span data-ttu-id="d00fe-103">JetBeginTransaction 函式</span><span class="sxs-lookup"><span data-stu-id="d00fe-103">JetBeginTransaction Function</span></span>


<span data-ttu-id="d00fe-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d00fe-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction-function"></a><span data-ttu-id="d00fe-105">JetBeginTransaction 函式</span><span class="sxs-lookup"><span data-stu-id="d00fe-105">JetBeginTransaction Function</span></span>

<span data-ttu-id="d00fe-106">**JetBeginTransaction** 函式會讓會話進入交易並建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="d00fe-106">The **JetBeginTransaction** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="d00fe-107">您可以在單一會話上多次呼叫此函數，以建立額外的儲存點。</span><span class="sxs-lookup"><span data-stu-id="d00fe-107">This function can be called more than once on a single session to cause the creation of additional save points.</span></span> <span data-ttu-id="d00fe-108">您可以使用這些儲存點，選擇性地保留或捨棄資料庫狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="d00fe-108">These save points can be used to selectively keep or discard changes to the state of the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="d00fe-109">參數</span><span class="sxs-lookup"><span data-stu-id="d00fe-109">Parameters</span></span>

<span data-ttu-id="d00fe-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d00fe-110">*sesid*</span></span>

<span data-ttu-id="d00fe-111">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="d00fe-111">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="d00fe-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d00fe-112">Return Value</span></span>

<span data-ttu-id="d00fe-113">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="d00fe-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d00fe-114">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="d00fe-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d00fe-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d00fe-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="d00fe-116">Description</span><span class="sxs-lookup"><span data-stu-id="d00fe-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d00fe-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d00fe-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d00fe-118">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="d00fe-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d00fe-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d00fe-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d00fe-120">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="d00fe-120">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d00fe-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d00fe-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d00fe-122">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="d00fe-122">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d00fe-123">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="d00fe-123">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d00fe-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d00fe-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d00fe-125">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="d00fe-125">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d00fe-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d00fe-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d00fe-127">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="d00fe-127">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d00fe-128">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d00fe-128">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d00fe-129">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="d00fe-129">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="d00fe-130">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="d00fe-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d00fe-131">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d00fe-131">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d00fe-132">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="d00fe-132">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d00fe-133">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="d00fe-133">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="d00fe-134">無法啟動新的交易，因為會話已經是 database engine 允許的最大儲存點深度。</span><span class="sxs-lookup"><span data-stu-id="d00fe-134">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d00fe-135">成功時，所提供的會話將會在交易內。</span><span class="sxs-lookup"><span data-stu-id="d00fe-135">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="d00fe-136">如果會話先前是在交易內，則會建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="d00fe-136">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="d00fe-137">失敗時，會話的交易式狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="d00fe-137">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="d00fe-138">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="d00fe-138">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d00fe-139">備註</span><span class="sxs-lookup"><span data-stu-id="d00fe-139">Remarks</span></span>

<span data-ttu-id="d00fe-140">資料庫引擎會為其交易提供快照集隔離模型。</span><span class="sxs-lookup"><span data-stu-id="d00fe-140">The database engine provides a snapshot isolation model for its transactions.</span></span> <span data-ttu-id="d00fe-141">這表示，當會話第一次進入交易狀態時，會話會在交易開始時看到整個資料庫凍結。</span><span class="sxs-lookup"><span data-stu-id="d00fe-141">This means that, when a session first enters into a transactional state, the session will see the entire database frozen in time at the start of the transaction.</span></span> <span data-ttu-id="d00fe-142">會話不需要讀取任何資料，因為它一律可以存取該資料的適當版本。</span><span class="sxs-lookup"><span data-stu-id="d00fe-142">A session does not need to read lock any data because it can always access the appropriate version of that data.</span></span> <span data-ttu-id="d00fe-143">這表示正在更新資料的會話絕不會封鎖不同的會話讀取該資料。</span><span class="sxs-lookup"><span data-stu-id="d00fe-143">This means that a session that is updating data will never block a different session from reading that data.</span></span>

<span data-ttu-id="d00fe-144">使用快照集隔離的另一種含意是用於更新的鎖定模型。</span><span class="sxs-lookup"><span data-stu-id="d00fe-144">Another implication of the use of snapshot isolation is the locking model used for updates.</span></span> <span data-ttu-id="d00fe-145">資料庫引擎會將指定資料片段的寫入鎖定，獎勵給要求它的第一個會話。</span><span class="sxs-lookup"><span data-stu-id="d00fe-145">The database engine will award a write lock on a given piece of data to the first session that requests it.</span></span> <span data-ttu-id="d00fe-146">當交易已完全認可或中止，讓會話不再存在於交易中時，就會釋放此寫入鎖定。</span><span class="sxs-lookup"><span data-stu-id="d00fe-146">This write lock is released when the transaction is either committed or aborted completely such that the session is no longer in a transaction.</span></span> <span data-ttu-id="d00fe-147">當會話保留寫入鎖定時，任何其他要求相同寫入鎖定的會話都不會封鎖，直到有寫入鎖定為止。</span><span class="sxs-lookup"><span data-stu-id="d00fe-147">While a session holds a write lock, any other session that requests the same write lock will not block until the write lock is available.</span></span> <span data-ttu-id="d00fe-148">相反地，第二個會話將會在 JET_errWriteConflict 時立即失敗。</span><span class="sxs-lookup"><span data-stu-id="d00fe-148">Rather, that second session will immediately fail with JET_errWriteConflict.</span></span> <span data-ttu-id="d00fe-149">若要解決此衝突，第二個會話必須完全中止 (或認可) 其交易，請等候一小段時間讓第一個會話認可或中止交易，然後再重新開機所有。</span><span class="sxs-lookup"><span data-stu-id="d00fe-149">To resolve this conflict, the second session must abort (or commit) its transaction completely, wait some small period of time for the first session to commit or abort its transaction, and then start all over again.</span></span>

<span data-ttu-id="d00fe-150">為了支援快照集隔離，資料庫引擎會將所有修改過之資料的所有版本儲存在記憶體中，因為在第一次啟動任何會話的最舊使用中交易時。</span><span class="sxs-lookup"><span data-stu-id="d00fe-150">In support of snapshot isolation, the database engine stores all versions of all modified data in memory since the time when the oldest active transaction on any session was first started.</span></span> <span data-ttu-id="d00fe-151">這對您的應用程式有重要的影響。</span><span class="sxs-lookup"><span data-stu-id="d00fe-151">This has important implications for your application.</span></span> <span data-ttu-id="d00fe-152">造成大量版本在記憶體中建立的任何行為，可能會導致實例耗盡其最大版本存放區大小 (如需詳細資訊) ，請參閱[系統參數](./extensible-storage-engine-system-parameters.md) [JET_paramMaxVerPages](./resource-parameters.md) 。</span><span class="sxs-lookup"><span data-stu-id="d00fe-152">Any behavior that causes a large number of versions to build up in memory may cause the instance to exhaust its maximum version store size (see [JET_paramMaxVerPages](./resource-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md) for more information).</span></span> <span data-ttu-id="d00fe-153">這類行為包括（但不限於）單一交易中的大量更新和執行中的交易。</span><span class="sxs-lookup"><span data-stu-id="d00fe-153">Such behavior includes, but is not limited to very large updates in a single transaction and very long running transactions.</span></span> <span data-ttu-id="d00fe-154">因此，請務必正確地為應用程式的預期交易載入設定版本存放區大小。</span><span class="sxs-lookup"><span data-stu-id="d00fe-154">As a result, it is very important to properly configure the version store size for the expected transactional load of the application.</span></span> <span data-ttu-id="d00fe-155">也請務必小心限制在單一交易中執行的更新數目。</span><span class="sxs-lookup"><span data-stu-id="d00fe-155">It is also important to take great care to limit the number of updates performed in a single transaction.</span></span> <span data-ttu-id="d00fe-156">此外，在高負載案例下，盡可能將交易的時間縮短得很短。</span><span class="sxs-lookup"><span data-stu-id="d00fe-156">Furthermore, it is important to make transactions as short in duration as possible under high load scenarios.</span></span>

<span data-ttu-id="d00fe-157">強烈建議應用程式在呼叫可捕獲或更新資料的 ESE Api 時，一律在交易內容中。</span><span class="sxs-lookup"><span data-stu-id="d00fe-157">It is highly recommended that the application always be in the context of a transaction when calling ESE APIs that retrieve or update data.</span></span> <span data-ttu-id="d00fe-158">如果未這麼做，database engine 就會將此類型的每個 ESE API 呼叫自動包裝在交易中，以代表應用程式。</span><span class="sxs-lookup"><span data-stu-id="d00fe-158">If this is not done, the database engine will automatically wrap each ESE API call of this type in a transaction on behalf of the application.</span></span> <span data-ttu-id="d00fe-159">在某些情況下，這些非常簡短的交易成本可以快速增加。</span><span class="sxs-lookup"><span data-stu-id="d00fe-159">The cost of these very short transactions can add up quickly in some cases.</span></span>

<span data-ttu-id="d00fe-160">引擎的預設行為是在呼叫 **JetBeginTransaction** 的第一次呼叫時，將會話限制在相同的執行緒上，直到發出 [JetCommitTransaction](./jetcommittransaction-function.md) 或 [JetRollback](./jetrollback-function.md) 的相符呼叫為止。</span><span class="sxs-lookup"><span data-stu-id="d00fe-160">The default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to **JetBeginTransaction** is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="d00fe-161">您可以使用 [JetSetSessionCoNtext](./jetsetsessioncontext-function.md) 和 [JetResetSessionCoNtext](./jetresetsessioncontext-function.md)設定自訂會話內容，來變更此行為以移除這項限制。</span><span class="sxs-lookup"><span data-stu-id="d00fe-161">This behavior can be changed to remove this restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

<span data-ttu-id="d00fe-162">資料庫引擎也支援交易式架構修改。</span><span class="sxs-lookup"><span data-stu-id="d00fe-162">The database engine also supports transactional schema modifications.</span></span> <span data-ttu-id="d00fe-163">例如，您可以開始新的交易、建立資料表、新增幾個資料行、建立一個或兩個索引，然後中止交易。</span><span class="sxs-lookup"><span data-stu-id="d00fe-163">For example, it is possible to begin a new transaction, create a table, add a few columns, create an index or two, and then abort the transaction.</span></span> <span data-ttu-id="d00fe-164">剛才加入的架構元素將會從資料庫中移除。</span><span class="sxs-lookup"><span data-stu-id="d00fe-164">The schema elements that were just added will be removed from the database.</span></span> <span data-ttu-id="d00fe-165">您也可以在相同的交易中混用架構修改和一般資料庫更新。</span><span class="sxs-lookup"><span data-stu-id="d00fe-165">It is also possible to mix schema modifications and ordinary database updates in the same transaction.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d00fe-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="d00fe-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d00fe-167"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="d00fe-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d00fe-168">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="d00fe-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d00fe-169"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="d00fe-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d00fe-170">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="d00fe-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d00fe-171"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="d00fe-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d00fe-172">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="d00fe-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d00fe-173"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="d00fe-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d00fe-174">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="d00fe-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d00fe-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d00fe-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d00fe-176">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="d00fe-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d00fe-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d00fe-177">See Also</span></span>

[<span data-ttu-id="d00fe-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d00fe-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d00fe-179">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d00fe-179">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d00fe-180">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d00fe-180">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d00fe-181">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="d00fe-181">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="d00fe-182">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="d00fe-182">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="d00fe-183">JetResetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="d00fe-183">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="d00fe-184">JetRollback</span><span class="sxs-lookup"><span data-stu-id="d00fe-184">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="d00fe-185">JetSetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="d00fe-185">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="d00fe-186">JetStopService</span><span class="sxs-lookup"><span data-stu-id="d00fe-186">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="d00fe-187">系統參數</span><span class="sxs-lookup"><span data-stu-id="d00fe-187">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
