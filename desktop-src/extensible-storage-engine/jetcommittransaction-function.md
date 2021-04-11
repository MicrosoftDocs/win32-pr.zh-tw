---
description: 深入瞭解： JetCommitTransaction 函數
title: JetCommitTransaction 函式
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2fe42891aa916a428d63fb68c99f42f38e78993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945177"
---
# <a name="jetcommittransaction-function"></a><span data-ttu-id="56bd4-103">JetCommitTransaction 函式</span><span class="sxs-lookup"><span data-stu-id="56bd4-103">JetCommitTransaction Function</span></span>


<span data-ttu-id="56bd4-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="56bd4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcommittransaction-function"></a><span data-ttu-id="56bd4-105">JetCommitTransaction 函式</span><span class="sxs-lookup"><span data-stu-id="56bd4-105">JetCommitTransaction Function</span></span>

<span data-ttu-id="56bd4-106">**JetCommitTransaction** 函式會在目前的儲存點期間認可對資料庫狀態所做的變更，並將其遷移至先前的儲存點。</span><span class="sxs-lookup"><span data-stu-id="56bd4-106">The **JetCommitTransaction** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="56bd4-107">如果已認可最外層的儲存點，則在該儲存點期間所做的變更將會認可至資料庫的狀態，而會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="56bd4-107">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="56bd4-108">參數</span><span class="sxs-lookup"><span data-stu-id="56bd4-108">Parameters</span></span>

<span data-ttu-id="56bd4-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="56bd4-109">*sesid*</span></span>

<span data-ttu-id="56bd4-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="56bd4-110">The session to use for this call.</span></span>

<span data-ttu-id="56bd4-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="56bd4-111">*grbit*</span></span>

<span data-ttu-id="56bd4-112">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="56bd4-112">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56bd4-113">值</span><span class="sxs-lookup"><span data-stu-id="56bd4-113">Value</span></span></p></th>
<th><p><span data-ttu-id="56bd4-114">意義</span><span class="sxs-lookup"><span data-stu-id="56bd4-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56bd4-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="56bd4-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="56bd4-116">交易會正常認可，但此 API 不會等到交易被排清到交易記錄檔，然後再傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="56bd4-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="56bd4-117">這可大幅減少認可作業的持續時間，代價是持久性。</span><span class="sxs-lookup"><span data-stu-id="56bd4-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="56bd4-118">在下次呼叫 <a href="gg294068(v=exchg.10).md">JetInit</a>期間，任何未在損毀之前排清到記錄檔的交易都會自動中止。</span><span class="sxs-lookup"><span data-stu-id="56bd4-118">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to <a href="gg294068(v=exchg.10).md">JetInit</a>.</span></span></p>
<p><span data-ttu-id="56bd4-119">如果指定 JET_bitWaitLastLevel0Commit 或 JET_bitWaitAllLevel0Commit，則會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="56bd4-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="56bd4-120">如果這個 <strong>JetCommitTransaction</strong> 呼叫與此會話的第一次呼叫 <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> 不相符，則會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="56bd4-120">If this call to <strong>JetCommitTransaction</strong> does not match the first call to <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> for this session, this option is ignored.</span></span> <span data-ttu-id="56bd4-121">這是因為在最外層儲存點上發生的最後一個動作，就是整個交易實際上是否認可到磁片的決定因素。</span><span class="sxs-lookup"><span data-stu-id="56bd4-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56bd4-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="56bd4-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="56bd4-123">所有先前由尚未排清至交易記錄檔的會話所認可的交易，都會立即進行清除。</span><span class="sxs-lookup"><span data-stu-id="56bd4-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="56bd4-124">此 API 會等到交易已排清之後，再返回呼叫端。</span><span class="sxs-lookup"><span data-stu-id="56bd4-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="56bd4-125">即使會話目前不在交易中，也可以使用此選項。</span><span class="sxs-lookup"><span data-stu-id="56bd4-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="56bd4-126">此選項不能與任何其他選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="56bd4-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="56bd4-127">此選項僅適用于 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="56bd4-127">This option is only available as of Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56bd4-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="56bd4-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="56bd4-129">如果會話先前已認可任何交易，而且它們尚未排清到交易記錄檔，則應該立即排清它們。</span><span class="sxs-lookup"><span data-stu-id="56bd4-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="56bd4-130">此 API 會等到交易已排清之後，再返回呼叫端。</span><span class="sxs-lookup"><span data-stu-id="56bd4-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="56bd4-131">如果應用程式先前已使用 JET_bitCommitLazyFlush 認可數筆交易，而現在想要將所有交易排清到磁片上，這項功能就很有用。</span><span class="sxs-lookup"><span data-stu-id="56bd4-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="56bd4-132">即使會話目前不在交易中，也可以使用此選項。</span><span class="sxs-lookup"><span data-stu-id="56bd4-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="56bd4-133">此選項不能與任何其他選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="56bd4-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="56bd4-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="56bd4-134">Return Value</span></span>

<span data-ttu-id="56bd4-135">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="56bd4-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="56bd4-136">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="56bd4-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="56bd4-137">傳回碼</span><span class="sxs-lookup"><span data-stu-id="56bd4-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="56bd4-138">Description</span><span class="sxs-lookup"><span data-stu-id="56bd4-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56bd4-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="56bd4-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="56bd4-140">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="56bd4-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56bd4-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="56bd4-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="56bd4-142">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="56bd4-142">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56bd4-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="56bd4-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="56bd4-144">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="56bd4-144">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="56bd4-145">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="56bd4-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56bd4-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="56bd4-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="56bd4-147">其中一個要求的選項無效或未執行。</span><span class="sxs-lookup"><span data-stu-id="56bd4-147">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="56bd4-148"><strong>JetCommitTransaction</strong>會在下列情況傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="56bd4-148">This error will be returned by <strong>JetCommitTransaction</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="56bd4-149">指定了不合法的 <em>grbit</em> 。</span><span class="sxs-lookup"><span data-stu-id="56bd4-149">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="56bd4-150">JET_bitWaitLastLevel0Commit 已與另一個 <em>grbit</em>一起指定。</span><span class="sxs-lookup"><span data-stu-id="56bd4-150">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="56bd4-151">JET_bitWaitAllLevel0Commit 已與另一個 <em>grbit</em>一起指定。</span><span class="sxs-lookup"><span data-stu-id="56bd4-151">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56bd4-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="56bd4-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="56bd4-153">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="56bd4-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56bd4-154">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="56bd4-154">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="56bd4-155">作業失敗，因為指定的會話不在交易中。</span><span class="sxs-lookup"><span data-stu-id="56bd4-155">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56bd4-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="56bd4-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="56bd4-157">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="56bd4-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56bd4-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="56bd4-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="56bd4-159">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="56bd4-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="56bd4-160">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="56bd4-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56bd4-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="56bd4-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="56bd4-162">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="56bd4-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="56bd4-163">成功時，將會認可指定會話目前儲存點期間對資料庫所做的任何變更，而且儲存點將會結束。</span><span class="sxs-lookup"><span data-stu-id="56bd4-163">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="56bd4-164">如果會話的最後一個儲存點已結束，則交易會選擇性地排清至交易記錄檔，而且會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="56bd4-164">If the last save point for the session was ended then the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="56bd4-165">失敗時，會話的交易式狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="56bd4-165">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="56bd4-166">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="56bd4-166">No change to the database state will occur.</span></span> <span data-ttu-id="56bd4-167">應用程式應該呼叫 [JetRollback](./jetrollback-function.md) 來中止交易。</span><span class="sxs-lookup"><span data-stu-id="56bd4-167">The application should call [JetRollback](./jetrollback-function.md) to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="56bd4-168">備註</span><span class="sxs-lookup"><span data-stu-id="56bd4-168">Remarks</span></span>

<span data-ttu-id="56bd4-169">必須呼叫 **JetCommitTransaction** 或 [JetRollback](./jetrollback-function.md) ，以比對指定會話的每個 [JetBeginTransaction](./jetbegintransaction-function.md) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="56bd4-169">There must be one call to **JetCommitTransaction** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="56bd4-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="56bd4-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56bd4-171"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="56bd4-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="56bd4-172">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="56bd4-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56bd4-173"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="56bd4-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="56bd4-174">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="56bd4-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56bd4-175"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="56bd4-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="56bd4-176">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="56bd4-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56bd4-177"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="56bd4-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="56bd4-178">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="56bd4-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56bd4-179"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="56bd4-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="56bd4-180">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="56bd4-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="56bd4-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56bd4-181">See Also</span></span>

[<span data-ttu-id="56bd4-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="56bd4-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="56bd4-183">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="56bd4-183">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="56bd4-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="56bd4-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="56bd4-185">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="56bd4-185">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="56bd4-186">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="56bd4-186">JetCommitTransaction</span></span>]()  
[<span data-ttu-id="56bd4-187">JetRollback</span><span class="sxs-lookup"><span data-stu-id="56bd4-187">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="56bd4-188">JetStopService</span><span class="sxs-lookup"><span data-stu-id="56bd4-188">JetStopService</span></span>](./jetstopservice-function.md)
