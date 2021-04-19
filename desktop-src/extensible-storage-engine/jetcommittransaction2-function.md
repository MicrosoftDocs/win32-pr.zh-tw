---
description: 深入瞭解： JetCommitTransaction2 函數
title: JetCommitTransaction2 函式
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24dfecd091de027f51ed8f69c0441fbc7cbd57af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997955"
---
# <a name="jetcommittransaction2-function"></a><span data-ttu-id="739be-103">JetCommitTransaction2 函式</span><span class="sxs-lookup"><span data-stu-id="739be-103">JetCommitTransaction2 Function</span></span>


<span data-ttu-id="739be-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="739be-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="739be-105">**JetCommitTransaction2** 函式會在目前的儲存點期間認可對資料庫狀態所做的變更，並將其遷移至先前的儲存點。</span><span class="sxs-lookup"><span data-stu-id="739be-105">The **JetCommitTransaction2** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="739be-106">如果已認可最外層的儲存點，則在該儲存點期間所做的變更將會認可至資料庫的狀態，而會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="739be-106">If the outermost save point is committed, the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="739be-107">**JetCommitTransaction2** 函式是在 Windows 8 作業系統中引進的。</span><span class="sxs-lookup"><span data-stu-id="739be-107">The **JetCommitTransaction2** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a><span data-ttu-id="739be-108">參數</span><span class="sxs-lookup"><span data-stu-id="739be-108">Parameters</span></span>

<span data-ttu-id="739be-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="739be-109">*sesid*</span></span>

<span data-ttu-id="739be-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="739be-110">The session to use for this call.</span></span>

<span data-ttu-id="739be-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="739be-111">*grbit*</span></span>

<span data-ttu-id="739be-112">一組位，指定下表所列的零或多個值。</span><span class="sxs-lookup"><span data-stu-id="739be-112">A group of bits that specify zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="739be-113">值</span><span class="sxs-lookup"><span data-stu-id="739be-113">Value</span></span></p></th>
<th><p><span data-ttu-id="739be-114">意義</span><span class="sxs-lookup"><span data-stu-id="739be-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="739be-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="739be-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="739be-116">交易會正常認可，但此 API 不會等到交易被排清到交易記錄檔，然後再傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="739be-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="739be-117">這可大幅減少認可作業的持續時間，代價是持久性。</span><span class="sxs-lookup"><span data-stu-id="739be-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="739be-118">在下一次呼叫 <a href="gg294068(v=exchg.10).md">JetInit</a> 函式期間，任何未在損毀之前排清到記錄檔的交易都會自動中止。</span><span class="sxs-lookup"><span data-stu-id="739be-118">Any transaction that is not flushed to the log before a crash will automatically be aborted during crash recovery during the next call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function.</span></span></p>
<p><span data-ttu-id="739be-119">如果指定 JET_bitWaitLastLevel0Commit 或 JET_bitWaitAllLevel0Commit，則會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="739be-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="739be-120">如果這個 <strong>JetCommitTransaction2</strong> 呼叫不符合此會話的第一次呼叫 <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> 函數，則會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="739be-120">If this call to <strong>JetCommitTransaction2</strong> does not match the first call to the <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> function for this session, this option is ignored.</span></span> <span data-ttu-id="739be-121">這是因為在最外層儲存點上發生的最後一個動作，就是整個交易實際上是否認可到磁片的決定因素。</span><span class="sxs-lookup"><span data-stu-id="739be-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="739be-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="739be-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="739be-123">所有先前由尚未排清至交易記錄檔的會話所認可的交易，都會立即進行清除。</span><span class="sxs-lookup"><span data-stu-id="739be-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="739be-124">此 API 會等到交易已排清之後，再返回呼叫端。</span><span class="sxs-lookup"><span data-stu-id="739be-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="739be-125">即使會話目前不在交易中，也可以使用此選項。</span><span class="sxs-lookup"><span data-stu-id="739be-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="739be-126">此選項不能與任何其他選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="739be-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="739be-127">從 Windows Server 2003 開始，此選項適用于 Windows Server 作業系統的版本。</span><span class="sxs-lookup"><span data-stu-id="739be-127">This option is available in versions of the Windows Server operating system starting with Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="739be-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="739be-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="739be-129">如果會話先前已認可任何交易，而且它們尚未排清到交易記錄檔，則應該立即排清它們。</span><span class="sxs-lookup"><span data-stu-id="739be-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="739be-130">此 API 會等到交易已排清之後，再返回呼叫端。</span><span class="sxs-lookup"><span data-stu-id="739be-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="739be-131">如果應用程式先前已使用 JET_bitCommitLazyFlush 認可數筆交易，而現在想要將所有交易排清到磁片上，這項功能就很有用。</span><span class="sxs-lookup"><span data-stu-id="739be-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="739be-132">即使會話目前不在交易中，也可以使用此選項。</span><span class="sxs-lookup"><span data-stu-id="739be-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="739be-133">此選項不能與任何其他選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="739be-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="739be-134">*cmsecDurableCommit*</span><span class="sxs-lookup"><span data-stu-id="739be-134">*cmsecDurableCommit*</span></span>

<span data-ttu-id="739be-135">認可延遲交易的持續時間。</span><span class="sxs-lookup"><span data-stu-id="739be-135">The duration to commit a lazy transaction.</span></span>

<span data-ttu-id="739be-136">*pCommitID*</span><span class="sxs-lookup"><span data-stu-id="739be-136">*pCommitID*</span></span>

<span data-ttu-id="739be-137">與此認可記錄相關聯的認可識別碼。</span><span class="sxs-lookup"><span data-stu-id="739be-137">The Commit-ID associated with this commit record.</span></span>

### <a name="return-value"></a><span data-ttu-id="739be-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="739be-138">Return value</span></span>

<span data-ttu-id="739be-139">此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="739be-139">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="739be-140">如需可能的可延伸儲存引擎 (ESE) 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="739be-140">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="739be-141">傳回碼</span><span class="sxs-lookup"><span data-stu-id="739be-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="739be-142">Description</span><span class="sxs-lookup"><span data-stu-id="739be-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="739be-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="739be-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="739be-144">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="739be-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="739be-145">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="739be-145">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="739be-146">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因為呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a> 函數。</span><span class="sxs-lookup"><span data-stu-id="739be-146">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="739be-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="739be-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="739be-148">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="739be-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="739be-149">此錯誤只會由 windows XP 開頭的 Windows 作業系統版本傳回。</span><span class="sxs-lookup"><span data-stu-id="739be-149">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="739be-150">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="739be-150">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="739be-151">其中一個要求的選項無效或未執行。</span><span class="sxs-lookup"><span data-stu-id="739be-151">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="739be-152">當發生下列情況時， <strong>JetCommitTransaction2</strong> 函式會傳回這個錯誤：</span><span class="sxs-lookup"><span data-stu-id="739be-152">This error will be returned by the <strong>JetCommitTransaction2</strong> function when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="739be-153">指定了不合法的 <em>grbit</em> 。</span><span class="sxs-lookup"><span data-stu-id="739be-153">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="739be-154">JET_bitWaitLastLevel0Commit 已與另一個 <em>grbit</em>一起指定。</span><span class="sxs-lookup"><span data-stu-id="739be-154">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="739be-155">JET_bitWaitAllLevel0Commit 已與另一個 <em>grbit</em>一起指定。</span><span class="sxs-lookup"><span data-stu-id="739be-155">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="739be-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="739be-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="739be-157">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="739be-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="739be-158">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="739be-158">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="739be-159">作業失敗，因為指定的會話不在交易中。</span><span class="sxs-lookup"><span data-stu-id="739be-159">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="739be-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="739be-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="739be-161">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="739be-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="739be-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="739be-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="739be-163">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="739be-163">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="739be-164">此錯誤只會由 windows XP 開頭的 Windows 作業系統版本傳回。</span><span class="sxs-lookup"><span data-stu-id="739be-164">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="739be-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="739be-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="739be-166">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="739be-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="739be-167">成功時，將會認可指定會話目前儲存點期間對資料庫所做的任何變更，而且儲存點將會結束。</span><span class="sxs-lookup"><span data-stu-id="739be-167">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="739be-168">如果會話的最後一個儲存點已結束，則交易會選擇性地排清至交易記錄檔，而且會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="739be-168">If the last save point for the session was ended, the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="739be-169">失敗時，會話的交易式狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="739be-169">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="739be-170">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="739be-170">No change to the database state will occur.</span></span> <span data-ttu-id="739be-171">應用程式應該呼叫 [JetRollback](./jetrollback-function.md) 函數來中止交易。</span><span class="sxs-lookup"><span data-stu-id="739be-171">The application should call the [JetRollback](./jetrollback-function.md) function to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="739be-172">備註</span><span class="sxs-lookup"><span data-stu-id="739be-172">Remarks</span></span>

<span data-ttu-id="739be-173">必須呼叫 **JetCommitTransaction2** 或 [JetRollback](./jetrollback-function.md) ，以比對指定會話的每個 [JetBeginTransaction](./jetbegintransaction-function.md) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="739be-173">There must be one call to **JetCommitTransaction2** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="739be-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="739be-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="739be-175"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="739be-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="739be-176">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="739be-176">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="739be-177"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="739be-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="739be-178">需要 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="739be-178">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="739be-179"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="739be-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="739be-180">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="739be-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="739be-181"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="739be-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="739be-182">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="739be-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="739be-183"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="739be-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="739be-184">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="739be-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="739be-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="739be-185">See also</span></span>

[<span data-ttu-id="739be-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="739be-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="739be-187">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="739be-187">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="739be-188">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="739be-188">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="739be-189">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="739be-189">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="739be-190">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="739be-190">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="739be-191">JetRollback</span><span class="sxs-lookup"><span data-stu-id="739be-191">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="739be-192">JetStopService</span><span class="sxs-lookup"><span data-stu-id="739be-192">JetStopService</span></span>](./jetstopservice-function.md)
