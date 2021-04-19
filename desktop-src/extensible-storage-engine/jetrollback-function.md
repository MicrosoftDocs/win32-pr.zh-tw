---
description: 深入瞭解： JetRollback 函數
title: JetRollback 函式
TOCTitle: JetRollback Function
ms:assetid: 685c51f4-8fe4-47cc-8a8e-c42014431b8b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269273(v=EXCHG.10)
ms:contentKeyID: 32765575
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRollback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eda0c8947e9609717bbb3f1a16999b450d7e4882
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991925"
---
# <a name="jetrollback-function"></a><span data-ttu-id="eda13-103">JetRollback 函式</span><span class="sxs-lookup"><span data-stu-id="eda13-103">JetRollback Function</span></span>


<span data-ttu-id="eda13-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="eda13-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrollback-function"></a><span data-ttu-id="eda13-105">JetRollback 函式</span><span class="sxs-lookup"><span data-stu-id="eda13-105">JetRollback Function</span></span>

<span data-ttu-id="eda13-106">**JetRollback** 函式會復原對資料庫狀態所做的變更，並返回到最後一個儲存點。</span><span class="sxs-lookup"><span data-stu-id="eda13-106">The **JetRollback** function undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="eda13-107">**JetRollback** 也會關閉儲存點期間開啟的任何資料指標。</span><span class="sxs-lookup"><span data-stu-id="eda13-107">**JetRollback** will also close any cursors opened during the save point.</span></span> <span data-ttu-id="eda13-108">如果最外層的儲存點復原，會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="eda13-108">If the outermost save point is undone, the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetRollback(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="eda13-109">參數</span><span class="sxs-lookup"><span data-stu-id="eda13-109">Parameters</span></span>

<span data-ttu-id="eda13-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="eda13-110">*sesid*</span></span>

<span data-ttu-id="eda13-111">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="eda13-111">The session to use for this call.</span></span>

<span data-ttu-id="eda13-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="eda13-112">*grbit*</span></span>

<span data-ttu-id="eda13-113">位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列各項：</span><span class="sxs-lookup"><span data-stu-id="eda13-113">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eda13-114">值</span><span class="sxs-lookup"><span data-stu-id="eda13-114">Value</span></span></p></th>
<th><p><span data-ttu-id="eda13-115">意義</span><span class="sxs-lookup"><span data-stu-id="eda13-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eda13-116">JET_bitRollbackAll</span><span class="sxs-lookup"><span data-stu-id="eda13-116">JET_bitRollbackAll</span></span></p></td>
<td><p><span data-ttu-id="eda13-117">此選項會要求所有儲存點在所有儲存點都復原時，對資料庫狀態所進行的所有變更。</span><span class="sxs-lookup"><span data-stu-id="eda13-117">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="eda13-118">因此，會話將會結束交易。</span><span class="sxs-lookup"><span data-stu-id="eda13-118">As a result, the session will exit the transaction.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="eda13-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="eda13-119">Return Value</span></span>

<span data-ttu-id="eda13-120">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="eda13-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="eda13-121">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="eda13-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eda13-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="eda13-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="eda13-123">Description</span><span class="sxs-lookup"><span data-stu-id="eda13-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eda13-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="eda13-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="eda13-125">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="eda13-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eda13-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="eda13-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="eda13-127">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="eda13-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eda13-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="eda13-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="eda13-129">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="eda13-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="eda13-130">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="eda13-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eda13-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="eda13-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="eda13-132">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="eda13-132">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eda13-133">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="eda13-133">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="eda13-134">作業失敗，因為指定的會話不在交易中。</span><span class="sxs-lookup"><span data-stu-id="eda13-134">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eda13-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="eda13-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="eda13-136">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="eda13-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eda13-137">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="eda13-137">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="eda13-138">因為發生嚴重錯誤，所以無法復原變更。</span><span class="sxs-lookup"><span data-stu-id="eda13-138">It was not possible to rollback the changes due to a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eda13-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="eda13-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="eda13-140">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="eda13-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="eda13-141">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="eda13-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eda13-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="eda13-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="eda13-143">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="eda13-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eda13-144">成功時，指定會話目前儲存點期間對資料庫所做的任何變更都會復原，而且儲存點將會結束。</span><span class="sxs-lookup"><span data-stu-id="eda13-144">On success, any changes made to the database during the current save point for the given session will be undone and that save point will be ended.</span></span> <span data-ttu-id="eda13-145">如果會話的最後一個儲存點已結束，則會話會結束交易。</span><span class="sxs-lookup"><span data-stu-id="eda13-145">If the last save point for the session was ended then the session will exit the transaction.</span></span>

<span data-ttu-id="eda13-146">失敗時，會話的交易式狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="eda13-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="eda13-147">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="eda13-147">No change to the database state will occur.</span></span> <span data-ttu-id="eda13-148">復原期間的失敗會視為嚴重的資料庫錯誤。</span><span class="sxs-lookup"><span data-stu-id="eda13-148">A failure during rollback is considered to be a catastrophic database error.</span></span>

#### <a name="remarks"></a><span data-ttu-id="eda13-149">備註</span><span class="sxs-lookup"><span data-stu-id="eda13-149">Remarks</span></span>

<span data-ttu-id="eda13-150">必須呼叫 [JetCommitTransaction](./jetcommittransaction-function.md) 或 **JetRollback** ，以比對指定會話的每個 [JetBeginTransaction](./jetbegintransaction-function.md) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="eda13-150">There must be one call to [JetCommitTransaction](./jetcommittransaction-function.md) or **JetRollback** to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

<span data-ttu-id="eda13-151">如果 (使用 [JetOpenTable](./jetopentable-function.md)開啟任何資料指標，例如在要復原的儲存點期間) ，則會關閉該資料指標。</span><span class="sxs-lookup"><span data-stu-id="eda13-151">If any cursors were opened (using [JetOpenTable](./jetopentable-function.md), for example) during a save point that is being rolled back then that cursor will be closed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="eda13-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="eda13-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eda13-153"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="eda13-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="eda13-154">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="eda13-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eda13-155"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="eda13-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="eda13-156">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="eda13-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eda13-157"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="eda13-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="eda13-158">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="eda13-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eda13-159"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="eda13-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="eda13-160">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="eda13-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eda13-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="eda13-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="eda13-162">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="eda13-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="eda13-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eda13-163">See Also</span></span>

[<span data-ttu-id="eda13-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="eda13-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="eda13-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="eda13-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="eda13-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="eda13-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="eda13-167">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="eda13-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="eda13-168">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="eda13-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
