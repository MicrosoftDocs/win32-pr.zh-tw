---
description: 深入瞭解： JetDupCursor 函數
title: JetDupCursor 函式
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 590b9b08c5386aaf1cd2dd541ac496a5fa0871d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978121"
---
# <a name="jetdupcursor-function"></a><span data-ttu-id="8c6e3-103">JetDupCursor 函式</span><span class="sxs-lookup"><span data-stu-id="8c6e3-103">JetDupCursor Function</span></span>


<span data-ttu-id="8c6e3-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8c6e3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupcursor-function"></a><span data-ttu-id="8c6e3-105">JetDupCursor 函式</span><span class="sxs-lookup"><span data-stu-id="8c6e3-105">JetDupCursor Function</span></span>

<span data-ttu-id="8c6e3-106">**JetDupCursor** 函式會重複開啟的資料指標，並將控制碼傳回至重複的資料指標。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-106">The **JetDupCursor** function duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="8c6e3-107">如果複製的資料指標是唯讀資料指標，則重復資料指標也是唯讀資料指標。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-107">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="8c6e3-108">任何與建立搜尋索引鍵或更新記錄相關的狀態都不會複製到重複的資料指標中。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-108">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="8c6e3-109">此外，原始資料指標的位置不會複製到重複的資料指標中。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-109">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="8c6e3-110">重複的資料指標一律會在叢集索引上開啟，而且其位置一律會在資料表的第一個資料列上。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-110">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="8c6e3-111">參數</span><span class="sxs-lookup"><span data-stu-id="8c6e3-111">Parameters</span></span>

<span data-ttu-id="8c6e3-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8c6e3-112">*sesid*</span></span>

<span data-ttu-id="8c6e3-113">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-113">The session to use for this call.</span></span>

<span data-ttu-id="8c6e3-114">*tableid*</span><span class="sxs-lookup"><span data-stu-id="8c6e3-114">*tableid*</span></span>

<span data-ttu-id="8c6e3-115">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-115">The cursor to use for this call.</span></span>

<span data-ttu-id="8c6e3-116">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="8c6e3-116">*ptableid*</span></span>

<span data-ttu-id="8c6e3-117">*Tableid* 的指標。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-117">Pointer to *tableid*.</span></span>

<span data-ttu-id="8c6e3-118">*grbit*</span><span class="sxs-lookup"><span data-stu-id="8c6e3-118">*grbit*</span></span>

<span data-ttu-id="8c6e3-119">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-119">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="8c6e3-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c6e3-120">Return Value</span></span>

<span data-ttu-id="8c6e3-121">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8c6e3-122">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c6e3-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8c6e3-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="8c6e3-124">Description</span><span class="sxs-lookup"><span data-stu-id="8c6e3-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c6e3-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8c6e3-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8c6e3-126">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6e3-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8c6e3-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8c6e3-128">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6e3-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8c6e3-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8c6e3-130">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="8c6e3-131">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6e3-132">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8c6e3-132">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8c6e3-133">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-133">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6e3-134">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="8c6e3-134">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="8c6e3-135">沒有任何可用的資料指標資源存在。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-135">No available cursor resources exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6e3-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8c6e3-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8c6e3-137">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6e3-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="8c6e3-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="8c6e3-139">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-139">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="8c6e3-140">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-140">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6e3-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8c6e3-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8c6e3-142">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-142">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8c6e3-143">成功時， *ptableid* 會設定為重複的資料指標。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-143">On success, *ptableid* is set to a duplicated cursor.</span></span>

<span data-ttu-id="8c6e3-144">失敗時，不會進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-144">On failure, no changes are made.</span></span> <span data-ttu-id="8c6e3-145">*Tableid* 的狀態不變。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-145">The state of *tableid* is unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8c6e3-146">備註</span><span class="sxs-lookup"><span data-stu-id="8c6e3-146">Remarks</span></span>

<span data-ttu-id="8c6e3-147">重複的資料指標沒有複製整個資料指標狀態。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-147">The duplicated cursor does not have the entire cursor state copied.</span></span> <span data-ttu-id="8c6e3-148">重復資料指標的位置（包括目前的索引）通常與指定的資料指標不同。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-148">The location of the duplicated cursor, including the current index, is usually different from the given cursor.</span></span> <span data-ttu-id="8c6e3-149">在叢集索引和資料表的第一個資料列上，一律會傳回重複的資料指標。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-149">The duplicated cursor is always returned on the clustered index and on the first row in the table.</span></span> <span data-ttu-id="8c6e3-150">如果資料表是空的，則重複的資料指標不會在任何資料列上。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-150">If the table is empty, the duplicated cursor is not on any row.</span></span>

<span data-ttu-id="8c6e3-151">使用 **JetDupCursor** 開啟的資料表通常應該以 [JetCloseTable](./jetclosetable-function.md)關閉。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-151">Tables opened with **JetDupCursor** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="8c6e3-152">在交易中呼叫 **JetDupCursor** 時，就會發生此規則的例外狀況，且會使用 [JetRollback](./jetrollback-function.md)) 將交易回復 (。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-152">The exception to this rule happens when **JetDupCursor** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="8c6e3-153">回復交易時，資料指標會自動關閉。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-153">When rolling back a transaction, the cursor is automatically closed.</span></span> <span data-ttu-id="8c6e3-154">在此情況下，使用 [JetCloseTable](./jetclosetable-function.md)關閉資料表是錯誤的。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-154">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="8c6e3-155">可以同時開啟的資料表數目會直接受到 [JET_paramMaxOpenTables](./resource-parameters.md)的影響。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-155">The number of tables that can be opened simultaneously is affected directly by [JET_paramMaxOpenTables](./resource-parameters.md).</span></span> <span data-ttu-id="8c6e3-156">如需詳細資訊，請參閱 [系統參數](./extensible-storage-engine-system-parameters.md) 。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-156">See [System Parameters](./extensible-storage-engine-system-parameters.md) for details.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8c6e3-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c6e3-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c6e3-158"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="8c6e3-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6e3-159">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-159">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6e3-160"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="8c6e3-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6e3-161">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-161">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6e3-162"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="8c6e3-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6e3-163">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6e3-164"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="8c6e3-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6e3-165">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6e3-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8c6e3-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6e3-167">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="8c6e3-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8c6e3-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c6e3-168">See Also</span></span>

[<span data-ttu-id="8c6e3-169">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8c6e3-169">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8c6e3-170">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8c6e3-170">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8c6e3-171">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8c6e3-171">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8c6e3-172">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="8c6e3-172">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="8c6e3-173">JetRollback</span><span class="sxs-lookup"><span data-stu-id="8c6e3-173">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="8c6e3-174">JetStopService</span><span class="sxs-lookup"><span data-stu-id="8c6e3-174">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="8c6e3-175">系統參數</span><span class="sxs-lookup"><span data-stu-id="8c6e3-175">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
