---
description: 深入瞭解： JetDelete 函數
title: JetDelete 函式
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996871"
---
# <a name="jetdelete-function"></a><span data-ttu-id="bdd86-103">JetDelete 函式</span><span class="sxs-lookup"><span data-stu-id="bdd86-103">JetDelete Function</span></span>


<span data-ttu-id="bdd86-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bdd86-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdelete-function"></a><span data-ttu-id="bdd86-105">JetDelete 函式</span><span class="sxs-lookup"><span data-stu-id="bdd86-105">JetDelete Function</span></span>

<span data-ttu-id="bdd86-106">**JetDelete** 函數會刪除資料庫資料表中的目前記錄。</span><span class="sxs-lookup"><span data-stu-id="bdd86-106">The **JetDelete** function deletes the current record in a database table.</span></span>

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="bdd86-107">參數</span><span class="sxs-lookup"><span data-stu-id="bdd86-107">Parameters</span></span>

<span data-ttu-id="bdd86-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="bdd86-108">*sesid*</span></span>

<span data-ttu-id="bdd86-109">將用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="bdd86-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="bdd86-110">*tableid*</span><span class="sxs-lookup"><span data-stu-id="bdd86-110">*tableid*</span></span>

<span data-ttu-id="bdd86-111">資料庫資料表上的資料指標。</span><span class="sxs-lookup"><span data-stu-id="bdd86-111">The cursor on a database table.</span></span> <span data-ttu-id="bdd86-112">將會刪除目前的資料列。</span><span class="sxs-lookup"><span data-stu-id="bdd86-112">The current row will be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="bdd86-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bdd86-113">Return Value</span></span>

<span data-ttu-id="bdd86-114">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="bdd86-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bdd86-115">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="bdd86-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bdd86-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bdd86-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="bdd86-117">Description</span><span class="sxs-lookup"><span data-stu-id="bdd86-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdd86-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bdd86-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bdd86-119">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="bdd86-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdd86-120">JET_errCallbackFailed</span><span class="sxs-lookup"><span data-stu-id="bdd86-120">JET_errCallbackFailed</span></span></p></td>
<td><p><span data-ttu-id="bdd86-121">回呼函式的運作方式失敗。</span><span class="sxs-lookup"><span data-stu-id="bdd86-121">The callback function failed in some manner.</span></span> <span data-ttu-id="bdd86-122">例如，會攔截回回呼函式中的存取違規，並將其轉譯成 JET_errCallbackFailed。</span><span class="sxs-lookup"><span data-stu-id="bdd86-122">For example, access violations in callback functions are caught and translated into JET_errCallbackFailed.</span></span> <span data-ttu-id="bdd86-123">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="bdd86-123">This error will only be returned by Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdd86-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bdd86-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bdd86-125">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="bdd86-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdd86-126">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="bdd86-126">JET_errIllegalOperation</span></span></p></td>
<td><p><span data-ttu-id="bdd86-127"><em>Tableid</em>所指定的資料指標不支援刪除。</span><span class="sxs-lookup"><span data-stu-id="bdd86-127">The cursor specified by <em>tableid</em> does not support deletion.</span></span> <span data-ttu-id="bdd86-128">請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="bdd86-128">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdd86-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bdd86-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bdd86-130">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="bdd86-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="bdd86-131">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="bdd86-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdd86-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="bdd86-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="bdd86-133"><em>Tableid</em>指定的資料指標不在記錄上。</span><span class="sxs-lookup"><span data-stu-id="bdd86-133">The cursor specified by <em>tableid</em> is not on a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdd86-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bdd86-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bdd86-135">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="bdd86-135">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdd86-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bdd86-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bdd86-137">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="bdd86-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdd86-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="bdd86-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="bdd86-139">資料庫引擎沒有足夠的許可權可刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="bdd86-139">The database engine does not have sufficient permissions to delete the record.</span></span> <span data-ttu-id="bdd86-140">如果資料庫檔案以唯讀存取權開啟，就可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="bdd86-140">This may happen if the database file was opened with read-only access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdd86-141">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="bdd86-141">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="bdd86-142">更新緩衝區 (看到 <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) 存在，但不是對 JET_coltypLongBinary 類型的資料 JET_coltypLongText 行所做的所有變更，也可能會回復類型的資料行。</span><span class="sxs-lookup"><span data-stu-id="bdd86-142">An update buffer (see <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) exists, but not all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary could be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdd86-143">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="bdd86-143">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="bdd86-144">同時從一個以上的執行緒使用相同的會話是不合法的。</span><span class="sxs-lookup"><span data-stu-id="bdd86-144">It is illegal to use the same session from more than one thread at the same time.</span></span> <span data-ttu-id="bdd86-145">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="bdd86-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdd86-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bdd86-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bdd86-147">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="bdd86-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdd86-148">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="bdd86-148">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="bdd86-149">交易是唯讀交易，不支援刪除。</span><span class="sxs-lookup"><span data-stu-id="bdd86-149">The transaction is a read-only transaction, and does not support deletes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdd86-150">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="bdd86-150">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="bdd86-151">作業失敗，因為沒有足夠的記憶體可保留有關更新的交易資訊。</span><span class="sxs-lookup"><span data-stu-id="bdd86-151">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdd86-152">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="bdd86-152">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="bdd86-153">另一個會話先前已鎖定記錄以進行更新。</span><span class="sxs-lookup"><span data-stu-id="bdd86-153">Another session has previously locked the record for update.</span></span> <span data-ttu-id="bdd86-154">此會話嘗試的更新將會失敗。</span><span class="sxs-lookup"><span data-stu-id="bdd86-154">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bdd86-155">成功時，會將貨幣保留在下一筆記錄的正上方。</span><span class="sxs-lookup"><span data-stu-id="bdd86-155">On success, the currency is left just before the next record.</span></span> <span data-ttu-id="bdd86-156">如果刪除的記錄是資料表中的最後一個，則會將貨幣留在資料表的結尾 (也就是在新的最後一筆記錄) 之後。</span><span class="sxs-lookup"><span data-stu-id="bdd86-156">If the deleted record was the last in the table, the currency is left at the end of the table (that is, after the new last record).</span></span> <span data-ttu-id="bdd86-157">如果刪除的記錄是資料表中唯一的記錄，則會將貨幣設定為開頭。</span><span class="sxs-lookup"><span data-stu-id="bdd86-157">If the deleted record was the only record in the table, the currency is set to the beginning.</span></span>

<span data-ttu-id="bdd86-158">系統會自動更新適當的索引。</span><span class="sxs-lookup"><span data-stu-id="bdd86-158">The appropriate indexes are automatically updated.</span></span>

<span data-ttu-id="bdd86-159">如果已備妥更新 (使用 [JetPrepareUpdate](./jetprepareupdate-function.md)) ，將會取消該更新。</span><span class="sxs-lookup"><span data-stu-id="bdd86-159">If an update is prepared (using [JetPrepareUpdate](./jetprepareupdate-function.md)), it will be canceled.</span></span> <span data-ttu-id="bdd86-160">更新緩衝區將會重設。</span><span class="sxs-lookup"><span data-stu-id="bdd86-160">The update buffer will be reset.</span></span>

<span data-ttu-id="bdd86-161">失敗時，貨幣會維持不變。</span><span class="sxs-lookup"><span data-stu-id="bdd86-161">On failure, the currency remains unchanged.</span></span> <span data-ttu-id="bdd86-162">如果已備妥更新 (請參閱 [JetPrepareUpdate](./jetprepareupdate-function.md)) ，更新緩衝區可能會重設。</span><span class="sxs-lookup"><span data-stu-id="bdd86-162">If an update is prepared (see [JetPrepareUpdate](./jetprepareupdate-function.md)), the update buffer may be reset.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bdd86-163">備註</span><span class="sxs-lookup"><span data-stu-id="bdd86-163">Remarks</span></span>

<span data-ttu-id="bdd86-164">並非所有資料表都支援刪除資料列。</span><span class="sxs-lookup"><span data-stu-id="bdd86-164">Not all tables support deletion of rows.</span></span> <span data-ttu-id="bdd86-165">臨時表通常不支援刪除資料列。</span><span class="sxs-lookup"><span data-stu-id="bdd86-165">A temporary table does not normally support deletion of rows.</span></span> <span data-ttu-id="bdd86-166">可能會因為許多原因而對臨時表啟用刪除記錄，其中一些原因如下：</span><span class="sxs-lookup"><span data-stu-id="bdd86-166">Deletion of records may be enabled on temporary tables for many reasons, some of which are:</span></span>

  - <span data-ttu-id="bdd86-167">建立期間指定了 JET_bitTTUpdatable。</span><span class="sxs-lookup"><span data-stu-id="bdd86-167">JET_bitTTUpdatable was specified during creation.</span></span>

  - <span data-ttu-id="bdd86-168">如果大型臨時表是使用 JET_bitTTScrollable 或 JET_bitTTIndexed 所建立，則可以支援刪除。</span><span class="sxs-lookup"><span data-stu-id="bdd86-168">Large temporary tables can support deletion if they were created with JET_bitTTScrollable or JET_bitTTIndexed.</span></span> <span data-ttu-id="bdd86-169">臨時表變成「大型」的臨界值目前為 64 kb，但在未來的版本中可能會變更。</span><span class="sxs-lookup"><span data-stu-id="bdd86-169">The threshold at which a temporary table becomes "large" is currently 64 kilobytes, but it may be changed in future releases.</span></span>

<span data-ttu-id="bdd86-170">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="bdd86-170">Windows XP and later.</span></span> <span data-ttu-id="bdd86-171">**JetDelete** 可叫用回呼函式，包括 JET_cbtypBeforeDelete 和 JET_cbtypAfterDelete。</span><span class="sxs-lookup"><span data-stu-id="bdd86-171">Callback functions can be invoked by **JetDelete**, including JET_cbtypBeforeDelete and JET_cbtypAfterDelete.</span></span>

<span data-ttu-id="bdd86-172">請務必瞭解在單一交易內執行大量更新作業的影響。</span><span class="sxs-lookup"><span data-stu-id="bdd86-172">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="bdd86-173">資料庫引擎必須在版本存放區中追蹤資料庫的每個更新。</span><span class="sxs-lookup"><span data-stu-id="bdd86-173">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="bdd86-174">版本存放區會保留資料庫中每個記錄或索引項目目之所有不同版本的即時記錄，以供所有使用中的交易看到。</span><span class="sxs-lookup"><span data-stu-id="bdd86-174">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="bdd86-175">這些版本是用來支援資料庫引擎使用的多版本並行控制，以支援使用快照集隔離的交易。</span><span class="sxs-lookup"><span data-stu-id="bdd86-175">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="bdd86-176">一旦資料庫引擎耗盡用來儲存這些版本的資源之後，就無法再接受進一步的變更，直到某些交易已結束，才能回收這些資源。</span><span class="sxs-lookup"><span data-stu-id="bdd86-176">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="bdd86-177">當引擎處於這種狀態時，所有更新都會失敗並 JET_errVersionStoreOutOfMemory。</span><span class="sxs-lookup"><span data-stu-id="bdd86-177">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="bdd86-178">資料庫引擎用來儲存這些版本的資源，可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 *JET_paramMaxVerPages* 和 *JET_paramGlobalMinVerPages* 來控制。</span><span class="sxs-lookup"><span data-stu-id="bdd86-178">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxVerPages* and *JET_paramGlobalMinVerPages*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bdd86-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdd86-179">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdd86-180"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="bdd86-180"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bdd86-181">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="bdd86-181">Requires Windows Vista, Windows XP or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdd86-182"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="bdd86-182"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bdd86-183">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="bdd86-183">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdd86-184"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="bdd86-184"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bdd86-185">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="bdd86-185">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdd86-186"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="bdd86-186"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bdd86-187">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="bdd86-187">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdd86-188"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bdd86-188"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bdd86-189">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="bdd86-189">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bdd86-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdd86-190">See Also</span></span>

[<span data-ttu-id="bdd86-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bdd86-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bdd86-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bdd86-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bdd86-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="bdd86-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="bdd86-194">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="bdd86-194">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="bdd86-195">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="bdd86-195">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="bdd86-196">系統參數</span><span class="sxs-lookup"><span data-stu-id="bdd86-196">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
