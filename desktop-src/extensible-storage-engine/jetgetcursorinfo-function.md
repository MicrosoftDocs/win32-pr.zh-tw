---
description: 深入瞭解： JetGetCursorInfo 函數
title: JetGetCursorInfo 函式
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998005"
---
# <a name="jetgetcursorinfo-function"></a><span data-ttu-id="1a967-103">JetGetCursorInfo 函式</span><span class="sxs-lookup"><span data-stu-id="1a967-103">JetGetCursorInfo Function</span></span>


<span data-ttu-id="1a967-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1a967-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcursorinfo-function"></a><span data-ttu-id="1a967-105">JetGetCursorInfo 函式</span><span class="sxs-lookup"><span data-stu-id="1a967-105">JetGetCursorInfo Function</span></span>

<span data-ttu-id="1a967-106">**JetGetCursorInfo** 函數是用來判斷資料指標的目前記錄更新是否會根據記錄的目前更新狀態而產生寫入衝突。</span><span class="sxs-lookup"><span data-stu-id="1a967-106">The **JetGetCursorInfo** function is used to determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="1a967-107">即使 **JetGetCursorInfo** 傳回 JET_errSuccess，還是可能會傳回寫入衝突，因為另一個會話可能會在目前的會話更新相同記錄之前更新記錄。</span><span class="sxs-lookup"><span data-stu-id="1a967-107">It is possible that a write conflict will ultimately be returned even if **JetGetCursorInfo** returns JET_errSuccess, because another session may update the record before the current session is able to update the same record.</span></span>

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="1a967-108">參數</span><span class="sxs-lookup"><span data-stu-id="1a967-108">Parameters</span></span>

<span data-ttu-id="1a967-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1a967-109">*sesid*</span></span>

<span data-ttu-id="1a967-110">此呼叫將使用的會話。</span><span class="sxs-lookup"><span data-stu-id="1a967-110">The session that will be used for this call.</span></span>

<span data-ttu-id="1a967-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="1a967-111">*tableid*</span></span>

<span data-ttu-id="1a967-112">將用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="1a967-112">The cursor that will be used for this call.</span></span>

<span data-ttu-id="1a967-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="1a967-113">*pvResult*</span></span>

<span data-ttu-id="1a967-114">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="1a967-114">Reserved for future use.</span></span>

<span data-ttu-id="1a967-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="1a967-115">*cbMax*</span></span>

<span data-ttu-id="1a967-116">必須設定為 0 (零) ，否則未使用。</span><span class="sxs-lookup"><span data-stu-id="1a967-116">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="1a967-117">它存在於未來的功能。</span><span class="sxs-lookup"><span data-stu-id="1a967-117">It is present for future functionality.</span></span>

<span data-ttu-id="1a967-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="1a967-118">*InfoLevel*</span></span>

<span data-ttu-id="1a967-119">必須設定為 0 (零) ，否則未使用。</span><span class="sxs-lookup"><span data-stu-id="1a967-119">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="1a967-120">它存在於未來的功能。</span><span class="sxs-lookup"><span data-stu-id="1a967-120">It is present for future functionality.</span></span>

### <a name="return-value"></a><span data-ttu-id="1a967-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a967-121">Return Value</span></span>

<span data-ttu-id="1a967-122">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="1a967-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1a967-123">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="1a967-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a967-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1a967-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="1a967-125">Description</span><span class="sxs-lookup"><span data-stu-id="1a967-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a967-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1a967-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1a967-127">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="1a967-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a967-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1a967-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1a967-129">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="1a967-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a967-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1a967-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1a967-131">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="1a967-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="1a967-132">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="1a967-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a967-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1a967-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1a967-134">可能是 <em>cbMax</em> 不是 0 (零) 或 <em>InfoLevel</em> 不是 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="1a967-134">Either <em>cbMax</em> is not 0 (zero) or <em>InfoLevel</em> is not 0 (zero).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a967-135">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="1a967-135">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="1a967-136">資料指標目前不在記錄上，因此無法傳回邏輯記錄的資訊。</span><span class="sxs-lookup"><span data-stu-id="1a967-136">The cursor is not currently on a record and information on a logical record cannot be returned as a result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a967-137">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1a967-137">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1a967-138">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="1a967-138">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a967-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1a967-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1a967-140">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="1a967-140">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a967-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1a967-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1a967-142">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="1a967-142">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="1a967-143">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="1a967-143">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a967-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1a967-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1a967-145">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="1a967-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a967-146">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="1a967-146">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="1a967-147">資料指標目前的記錄已由另一個會話更新，且此會話的此記錄更新會導致寫入衝突。</span><span class="sxs-lookup"><span data-stu-id="1a967-147">The current record of the cursor has been updated by another session and an update of this record by this session will result in a write conflict.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1a967-148">成功時，此作業對資料指標的位置沒有任何作用，但只表示沒有任何其他會話目前已更新此記錄。</span><span class="sxs-lookup"><span data-stu-id="1a967-148">On success, this operation has no effect on the location of the cursor but only indicates that no other session has currently updated this record.</span></span>

<span data-ttu-id="1a967-149">失敗時，如果傳回負錯誤碼，則資料指標或資料庫不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="1a967-149">On failure, if a negative error code is returned there are no effects to the cursor or the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1a967-150">備註</span><span class="sxs-lookup"><span data-stu-id="1a967-150">Remarks</span></span>

<span data-ttu-id="1a967-151">這項作業不會影響資料指標或資料的狀態。</span><span class="sxs-lookup"><span data-stu-id="1a967-151">This operation does not affect the state of the cursor or the data.</span></span> <span data-ttu-id="1a967-152">它只會傳回錯誤碼，描述呼叫會話的目前記錄更新是否已知為產生 JET_errWriteConflict，或未知而無法傳回 JET_errWriteConflict。</span><span class="sxs-lookup"><span data-stu-id="1a967-152">It only returns an error code describing whether an update to the current record by the calling session is known to result in a JET_errWriteConflict, or is unknown to return JET_errWriteConflict.</span></span> <span data-ttu-id="1a967-153">如果另一個會話已更新此記錄以使用此記錄，將會確定此會話的這項記錄更新會導致寫入衝突。</span><span class="sxs-lookup"><span data-stu-id="1a967-153">If another session has already updated this record to use it is certain that an update of this record by this session will result in a write conflict.</span></span> <span data-ttu-id="1a967-154">在此會話認可或回復交易至交易層級 0 (零) 之前，這會是正確的。</span><span class="sxs-lookup"><span data-stu-id="1a967-154">This will be true until this session commits or rolls back its transactions to transaction level 0 (zero).</span></span> <span data-ttu-id="1a967-155">但是，如果 **JetGetCursorInfo** 傳回 JET_errSuccess，則在目前的會話之前，另一個會話仍可能更新此記錄，因此在目前的交易中，此會話的目前記錄更新仍可能會導致寫入衝突。</span><span class="sxs-lookup"><span data-stu-id="1a967-155">However, if **JetGetCursorInfo** returns JET_errSuccess, it is still possible for another session to update this record before the current session and thus it is still possible that an update of the current record by this session in its current transaction will result in a write conflict.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1a967-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a967-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a967-157"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="1a967-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1a967-158">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="1a967-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a967-159"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="1a967-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1a967-160">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="1a967-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a967-161"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="1a967-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1a967-162">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="1a967-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a967-163"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="1a967-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1a967-164">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="1a967-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a967-165"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1a967-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1a967-166">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="1a967-166">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1a967-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a967-167">See Also</span></span>

[<span data-ttu-id="1a967-168">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1a967-168">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1a967-169">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1a967-169">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1a967-170">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1a967-170">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1a967-171">JetGetLock</span><span class="sxs-lookup"><span data-stu-id="1a967-171">JetGetLock</span></span>](./jetgetlock-function.md)  
[<span data-ttu-id="1a967-172">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="1a967-172">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="1a967-173">JetStopService</span><span class="sxs-lookup"><span data-stu-id="1a967-173">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="1a967-174">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="1a967-174">JetUpdate</span></span>](./jetupdate-function.md)
