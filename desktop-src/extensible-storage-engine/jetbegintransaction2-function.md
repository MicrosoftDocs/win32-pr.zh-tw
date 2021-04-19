---
description: 深入瞭解： JetBeginTransaction2 函數
title: JetBeginTransaction2 函式
TOCTitle: JetBeginTransaction2 Function
ms:assetid: 638af3f1-b342-46bd-9fd0-dc281936355c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269268(v=EXCHG.10)
ms:contentKeyID: 32765570
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d21bb88301a1f5d30df673a56032ef91c3847599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978087"
---
# <a name="jetbegintransaction2-function"></a><span data-ttu-id="26aff-103">JetBeginTransaction2 函式</span><span class="sxs-lookup"><span data-stu-id="26aff-103">JetBeginTransaction2 Function</span></span>


<span data-ttu-id="26aff-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="26aff-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction2-function"></a><span data-ttu-id="26aff-105">JetBeginTransaction2 函式</span><span class="sxs-lookup"><span data-stu-id="26aff-105">JetBeginTransaction2 Function</span></span>

<span data-ttu-id="26aff-106">**JetBeginTransaction2** 函式會讓會話進入交易並建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="26aff-106">The **JetBeginTransaction2** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="26aff-107">您可以在單一會話中多次呼叫此函數，以建立額外的儲存點。</span><span class="sxs-lookup"><span data-stu-id="26aff-107">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="26aff-108">您可以使用這些儲存點，選擇性地保留或捨棄資料庫的變更。</span><span class="sxs-lookup"><span data-stu-id="26aff-108">These save points can be used to selectively to keep or discard changes to the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction2(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="26aff-109">參數</span><span class="sxs-lookup"><span data-stu-id="26aff-109">Parameters</span></span>

<span data-ttu-id="26aff-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="26aff-110">*sesid*</span></span>

<span data-ttu-id="26aff-111">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="26aff-111">The session to use for this call.</span></span>

<span data-ttu-id="26aff-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="26aff-112">*grbit*</span></span>

<span data-ttu-id="26aff-113">位群組，其中包含要用於此呼叫的選項，包括下列零或多個。</span><span class="sxs-lookup"><span data-stu-id="26aff-113">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26aff-114">值</span><span class="sxs-lookup"><span data-stu-id="26aff-114">Value</span></span></p></th>
<th><p><span data-ttu-id="26aff-115">意義</span><span class="sxs-lookup"><span data-stu-id="26aff-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26aff-116">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="26aff-116">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="26aff-117">交易不會修改資料庫。</span><span class="sxs-lookup"><span data-stu-id="26aff-117">The transaction will not modify the database.</span></span> <span data-ttu-id="26aff-118">如果嘗試更新，這項作業將會失敗，並 JET_errTransReadOnly。</span><span class="sxs-lookup"><span data-stu-id="26aff-118">If an update is attempted, that operation will fail with JET_errTransReadOnly.</span></span> <span data-ttu-id="26aff-119">除非指定的會話尚未存在於交易中，否則會忽略這個選項。</span><span class="sxs-lookup"><span data-stu-id="26aff-119">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="26aff-120">此選項僅適用于 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="26aff-120">This option is only available as of Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="26aff-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="26aff-121">Return Value</span></span>

<span data-ttu-id="26aff-122">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="26aff-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="26aff-123">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="26aff-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26aff-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="26aff-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="26aff-125">Description</span><span class="sxs-lookup"><span data-stu-id="26aff-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26aff-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="26aff-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="26aff-127">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="26aff-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26aff-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="26aff-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="26aff-129">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="26aff-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26aff-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="26aff-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="26aff-131">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="26aff-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="26aff-132">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="26aff-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26aff-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="26aff-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="26aff-134">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="26aff-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26aff-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="26aff-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="26aff-136">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="26aff-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26aff-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="26aff-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="26aff-138">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="26aff-138">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="26aff-139">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="26aff-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26aff-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="26aff-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="26aff-141">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="26aff-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26aff-142">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="26aff-142">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="26aff-143">無法啟動新的交易，因為會話已經是 database engine 允許的最大儲存點深度。</span><span class="sxs-lookup"><span data-stu-id="26aff-143">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="26aff-144">成功時，所提供的會話將會在交易內。</span><span class="sxs-lookup"><span data-stu-id="26aff-144">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="26aff-145">如果會話先前是在交易內，則會建立新的儲存點。</span><span class="sxs-lookup"><span data-stu-id="26aff-145">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="26aff-146">失敗時，會話的交易式狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="26aff-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="26aff-147">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="26aff-147">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="26aff-148">備註</span><span class="sxs-lookup"><span data-stu-id="26aff-148">Remarks</span></span>

<span data-ttu-id="26aff-149">如需交易運作方式的詳細資訊，請參閱 [JetBeginTransaction](./jetbegintransaction-function.md)。</span><span class="sxs-lookup"><span data-stu-id="26aff-149">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="26aff-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="26aff-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26aff-151"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="26aff-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="26aff-152">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="26aff-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26aff-153"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="26aff-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="26aff-154">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="26aff-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26aff-155"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="26aff-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="26aff-156">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="26aff-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26aff-157"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="26aff-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="26aff-158">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="26aff-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26aff-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="26aff-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="26aff-160">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="26aff-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="26aff-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26aff-161">See Also</span></span>

[<span data-ttu-id="26aff-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="26aff-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="26aff-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="26aff-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="26aff-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="26aff-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="26aff-165">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="26aff-165">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="26aff-166">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="26aff-166">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="26aff-167">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="26aff-167">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="26aff-168">JetResetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="26aff-168">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="26aff-169">JetRollback</span><span class="sxs-lookup"><span data-stu-id="26aff-169">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="26aff-170">JetSetSessionCoNtext</span><span class="sxs-lookup"><span data-stu-id="26aff-170">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="26aff-171">系統參數</span><span class="sxs-lookup"><span data-stu-id="26aff-171">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
