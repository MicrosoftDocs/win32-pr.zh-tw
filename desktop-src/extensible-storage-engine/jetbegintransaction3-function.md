---
description: 深入瞭解： JetBeginTransaction3 函數
title: JetBeginTransaction3 函式
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b263cb18c09df8205a49e1c4a1a683e339803f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973002"
---
# <a name="jetbegintransaction3-function"></a><span data-ttu-id="9cc9d-103">JetBeginTransaction3 函式</span><span class="sxs-lookup"><span data-stu-id="9cc9d-103">JetBeginTransaction3 Function</span></span>


<span data-ttu-id="9cc9d-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9cc9d-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="9cc9d-105">**JetBeginTransaction3** 函式會讓會話進入交易並建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-105">The **JetBeginTransaction3** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="9cc9d-106">您可以在單一會話中多次呼叫此函數，以建立額外的儲存點。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-106">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="9cc9d-107">您可以使用這些儲存點，選擇性地保留或捨棄資料庫的變更。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-107">These save points can be used to selectively to keep or discard changes to the database.</span></span>

<span data-ttu-id="9cc9d-108">**JetBeginTransaction3** 函式是在 Windows 8 作業系統中引進的。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-108">The **JetBeginTransaction3** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="9cc9d-109">參數</span><span class="sxs-lookup"><span data-stu-id="9cc9d-109">Parameters</span></span>

<span data-ttu-id="9cc9d-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9cc9d-110">*sesid*</span></span>

<span data-ttu-id="9cc9d-111">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-111">The session to use for this call.</span></span>

<span data-ttu-id="9cc9d-112">*trxid*</span><span class="sxs-lookup"><span data-stu-id="9cc9d-112">*trxid*</span></span>

<span data-ttu-id="9cc9d-113">使用者提供的選擇性識別碼，用來識別交易。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-113">An optional identifier supplied by the user to identify the transaction.</span></span>

<span data-ttu-id="9cc9d-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9cc9d-114">*grbit*</span></span>

<span data-ttu-id="9cc9d-115">一組位，指定下表所列的零或多個呼叫選項值。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-115">A group of bits that that specifies zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9cc9d-116">值</span><span class="sxs-lookup"><span data-stu-id="9cc9d-116">Value</span></span></p></th>
<th><p><span data-ttu-id="9cc9d-117">意義</span><span class="sxs-lookup"><span data-stu-id="9cc9d-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9cc9d-118">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="9cc9d-118">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="9cc9d-119">交易不會修改資料庫。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-119">The transaction will not modify the database.</span></span> <span data-ttu-id="9cc9d-120">如果嘗試更新，這項作業將會失敗，並產生 JET_errTransReadOnly 的回應碼。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-120">If an update is attempted, that operation will fail with JET_errTransReadOnly response code.</span></span> <span data-ttu-id="9cc9d-121">除非指定的會話尚未存在於交易中，否則會忽略這個選項。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-121">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="9cc9d-122">從 Windows XP 開始的 Windows 作業系統版本中有提供此選項。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-122">This option is available in versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9cc9d-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="9cc9d-123">Return value</span></span>

<span data-ttu-id="9cc9d-124">此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-124">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="9cc9d-125">如需可能的可延伸儲存引擎 (ESE) 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-125">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9cc9d-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9cc9d-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="9cc9d-127">Description</span><span class="sxs-lookup"><span data-stu-id="9cc9d-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9cc9d-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9cc9d-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9cc9d-129">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9cc9d-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9cc9d-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9cc9d-131">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因為呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a> 函數。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9cc9d-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9cc9d-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9cc9d-133">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9cc9d-134">自 Windows XP 起的 Windows 版本會傳回這個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-134">This return code is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9cc9d-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9cc9d-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9cc9d-136">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9cc9d-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9cc9d-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9cc9d-138">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-138">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9cc9d-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9cc9d-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9cc9d-140">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="9cc9d-141">從 Windows XP 開始的 Windows 版本會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-141">This error is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9cc9d-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9cc9d-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9cc9d-143">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9cc9d-144">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="9cc9d-144">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="9cc9d-145">無法啟動新的交易，因為會話已經是 database engine 允許的最大儲存點深度。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-145">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9cc9d-146">成功時，所提供的會話將會在交易內。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-146">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="9cc9d-147">如果會話先前是在交易內，則會建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-147">If the session was previously inside a transaction, a new save point will be created.</span></span>

<span data-ttu-id="9cc9d-148">失敗時，會話的交易式狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-148">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="9cc9d-149">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-149">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9cc9d-150">備註</span><span class="sxs-lookup"><span data-stu-id="9cc9d-150">Remarks</span></span>

<span data-ttu-id="9cc9d-151">如需交易運作方式的詳細資訊，請參閱 [JetBeginTransaction](./jetbegintransaction-function.md)。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-151">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="9cc9d-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="9cc9d-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9cc9d-153"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="9cc9d-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9cc9d-154">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9cc9d-155"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="9cc9d-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9cc9d-156">需要 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9cc9d-157"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="9cc9d-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9cc9d-158">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9cc9d-159"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="9cc9d-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9cc9d-160">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9cc9d-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9cc9d-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9cc9d-162">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="9cc9d-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9cc9d-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cc9d-163">See also</span></span>

[<span data-ttu-id="9cc9d-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9cc9d-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9cc9d-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9cc9d-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9cc9d-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9cc9d-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9cc9d-167">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="9cc9d-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="9cc9d-168">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="9cc9d-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="9cc9d-169">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="9cc9d-169">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="9cc9d-170">JetResetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="9cc9d-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="9cc9d-171">JetRollback</span><span class="sxs-lookup"><span data-stu-id="9cc9d-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="9cc9d-172">JetSetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="9cc9d-172">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="9cc9d-173">系統參數</span><span class="sxs-lookup"><span data-stu-id="9cc9d-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
