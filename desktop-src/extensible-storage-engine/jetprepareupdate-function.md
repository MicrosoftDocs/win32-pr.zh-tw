---
description: 深入瞭解： JetPrepareUpdate 函數
title: JetPrepareUpdate 函式
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16362463194d945d7b451f784bc0942bda2d03e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997990"
---
# <a name="jetprepareupdate-function"></a><span data-ttu-id="a2816-103">JetPrepareUpdate 函式</span><span class="sxs-lookup"><span data-stu-id="a2816-103">JetPrepareUpdate Function</span></span>


<span data-ttu-id="a2816-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a2816-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprepareupdate-function"></a><span data-ttu-id="a2816-105">JetPrepareUpdate 函式</span><span class="sxs-lookup"><span data-stu-id="a2816-105">JetPrepareUpdate Function</span></span>

<span data-ttu-id="a2816-106">**JetPrepareUpdate** 函式是執行更新的第一個作業，目的是要插入新的記錄，或以新的值取代現有的記錄。</span><span class="sxs-lookup"><span data-stu-id="a2816-106">The **JetPrepareUpdate** function is the first operation in performing an update, for the purposes of inserting a new record or replacing an existing record with new values.</span></span> <span data-ttu-id="a2816-107">更新的完成方式是呼叫 **JetPrepareUpdate**，然後呼叫 [JetSetColumn](./jetsetcolumn-function.md) 或 [JetSetColumns](./jetsetcolumns-function.md) 零次或多次，最後呼叫 [JetUpdate](./jetupdate-function.md) 來完成作業。</span><span class="sxs-lookup"><span data-stu-id="a2816-107">Updates are done by calling **JetPrepareUpdate**, then calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) zero or more times and finally by calling [JetUpdate](./jetupdate-function.md) to complete the operation.</span></span> <span data-ttu-id="a2816-108">**JetPrepareUpdate** 和 [JetUpdate](./jetupdate-function.md) 會設定更新作業的界限，而且只有在索引中輸入記錄的最終更新狀態時很重要。</span><span class="sxs-lookup"><span data-stu-id="a2816-108">**JetPrepareUpdate** and [JetUpdate](./jetupdate-function.md) set the boundaries for an update operation and are important in having only the final update state of a record entered into indexes.</span></span> <span data-ttu-id="a2816-109">這會更有效率，但在資料必須透過超過 set 資料行作業的有效狀態必須符合的情況下，也是必要的。</span><span class="sxs-lookup"><span data-stu-id="a2816-109">This is both more efficient, but also required in cases where data must match a valid state through more than on set column operation.</span></span>

<span data-ttu-id="a2816-110">有幾個不同的選項可用於插入或取代記錄，並且會在下面更詳細地說明。</span><span class="sxs-lookup"><span data-stu-id="a2816-110">There are a few different options for inserting or replacing records and they are described in more detail below.</span></span>

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a><span data-ttu-id="a2816-111">參數</span><span class="sxs-lookup"><span data-stu-id="a2816-111">Parameters</span></span>

<span data-ttu-id="a2816-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a2816-112">*sesid*</span></span>

<span data-ttu-id="a2816-113">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="a2816-113">The session to use for this call.</span></span>

<span data-ttu-id="a2816-114">*tableid*</span><span class="sxs-lookup"><span data-stu-id="a2816-114">*tableid*</span></span>

<span data-ttu-id="a2816-115">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="a2816-115">The cursor to use for this call.</span></span>

<span data-ttu-id="a2816-116">*準備*</span><span class="sxs-lookup"><span data-stu-id="a2816-116">*prep*</span></span>

<span data-ttu-id="a2816-117">可以用來準備更新的選項，包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="a2816-117">The options that can be used to prepare for an update, which include the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2816-118">值</span><span class="sxs-lookup"><span data-stu-id="a2816-118">Value</span></span></p></th>
<th><p><span data-ttu-id="a2816-119">意義</span><span class="sxs-lookup"><span data-stu-id="a2816-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2816-120">JET_prepCancel</span><span class="sxs-lookup"><span data-stu-id="a2816-120">JET_prepCancel</span></span></p></td>
<td><p><span data-ttu-id="a2816-121">此旗標會使 <strong>JetPrepareUpdate</strong> 取消此資料指標的更新。</span><span class="sxs-lookup"><span data-stu-id="a2816-121">This flag causes <strong>JetPrepareUpdate</strong> to cancel the update for this cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2816-122">JET_prepInsert</span><span class="sxs-lookup"><span data-stu-id="a2816-122">JET_prepInsert</span></span></p></td>
<td><p><span data-ttu-id="a2816-123">此旗標會讓資料指標準備插入新的記錄。</span><span class="sxs-lookup"><span data-stu-id="a2816-123">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="a2816-124">所有資料都會初始化為記錄的預設狀態。</span><span class="sxs-lookup"><span data-stu-id="a2816-124">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="a2816-125">如果資料表具有自動遞增資料行，就會將新的值指派給此記錄，而不論更新最終成功、失敗或已取消。</span><span class="sxs-lookup"><span data-stu-id="a2816-125">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2816-126">JET_prepInsertCopy</span><span class="sxs-lookup"><span data-stu-id="a2816-126">JET_prepInsertCopy</span></span></p></td>
<td><p><span data-ttu-id="a2816-127">此旗標會讓資料指標準備插入現有記錄的複本。</span><span class="sxs-lookup"><span data-stu-id="a2816-127">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="a2816-128">如果使用此選項，則必須要有目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a2816-128">There must be a current record if this option is used.</span></span> <span data-ttu-id="a2816-129">新記錄的初始狀態會從目前記錄複製。</span><span class="sxs-lookup"><span data-stu-id="a2816-129">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="a2816-130">幾乎會複製儲存在登出的 Long 值。</span><span class="sxs-lookup"><span data-stu-id="a2816-130">Long values that are stored off-record are virtually copied.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2816-131">JET_prepInsertCopyDeleteOriginal</span><span class="sxs-lookup"><span data-stu-id="a2816-131">JET_prepInsertCopyDeleteOriginal</span></span></p></td>
<td><p><span data-ttu-id="a2816-132">此旗標會讓資料指標準備插入相同的記錄，以及刪除或原始記錄。</span><span class="sxs-lookup"><span data-stu-id="a2816-132">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="a2816-133">當主要金鑰已變更時，就會使用它。</span><span class="sxs-lookup"><span data-stu-id="a2816-133">It is used in cases in which the primary key has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2816-134">JET_prepReplace</span><span class="sxs-lookup"><span data-stu-id="a2816-134">JET_prepReplace</span></span></p></td>
<td><p><span data-ttu-id="a2816-135">此旗標會讓資料指標準備取代目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a2816-135">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="a2816-136">如果資料表有版本資料行，則 [版本] 欄會設定為其序列中的下一個值。</span><span class="sxs-lookup"><span data-stu-id="a2816-136">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="a2816-137">如果此更新未完成，則記錄中的版本值不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="a2816-137">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="a2816-138">記錄上會執行更新鎖定，以防止其他會話在此會話完成之前更新此記錄。</span><span class="sxs-lookup"><span data-stu-id="a2816-138">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2816-139">JET_prepReplaceNoLock</span><span class="sxs-lookup"><span data-stu-id="a2816-139">JET_prepReplaceNoLock</span></span></p></td>
<td><p><span data-ttu-id="a2816-140">此旗標類似于 JET_prepReplace，但不會採取任何鎖定來防止其他會話更新此記錄。</span><span class="sxs-lookup"><span data-stu-id="a2816-140">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="a2816-141">相反地，此會話可能會在呼叫 <a href="gg269288(v=exchg.10).md">JetUpdate</a> 來完成更新時收到 JET_errWriteConflict。</span><span class="sxs-lookup"><span data-stu-id="a2816-141">Instead, this session may receive JET_errWriteConflict when it calls <a href="gg269288(v=exchg.10).md">JetUpdate</a> to complete the update.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a2816-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2816-142">Return Value</span></span>

<span data-ttu-id="a2816-143">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="a2816-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a2816-144">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="a2816-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2816-145">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a2816-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="a2816-146">Description</span><span class="sxs-lookup"><span data-stu-id="a2816-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2816-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a2816-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a2816-148">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="a2816-148">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2816-149">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="a2816-149">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="a2816-150">已使用有效的準備旗標呼叫<strong>JetPrepareUpdate</strong> ，但未 JET_prepCancel，且資料指標已處於備妥狀態。</span><span class="sxs-lookup"><span data-stu-id="a2816-150"><strong>JetPrepareUpdate</strong> was called with a valid flag for prep but not JET_prepCancel and the cursor was already in the prepared state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2816-151">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a2816-151">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a2816-152">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="a2816-152">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2816-153">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a2816-153">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a2816-154">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="a2816-154">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a2816-155">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a2816-155">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2816-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a2816-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a2816-157">指定的準備旗標不是有效的旗標。</span><span class="sxs-lookup"><span data-stu-id="a2816-157">The given prep flag is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2816-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a2816-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a2816-159">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="a2816-159">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2816-160">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="a2816-160">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="a2816-161">呼叫<strong>JetPrepareUpdate</strong>來取代具有 SLV 資料行的記錄。</span><span class="sxs-lookup"><span data-stu-id="a2816-161"><strong>JetPrepareUpdate</strong> was called to replace a record which had SLV columns.</span></span> <span data-ttu-id="a2816-162">SLV 資料行。</span><span class="sxs-lookup"><span data-stu-id="a2816-162">SLV columns.</span></span> <span data-ttu-id="a2816-163">請注意，SLV 資料行是不適合一般使用的功能。</span><span class="sxs-lookup"><span data-stu-id="a2816-163">Please note that SLV columns are a feature not intended for general usage.</span></span> <span data-ttu-id="a2816-164">這項功能是用來支援 Microsoft Exchange 基礎結構，而且不適合在您的應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="a2816-164">This feature is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2816-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a2816-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a2816-166">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="a2816-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2816-167">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="a2816-167">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="a2816-168">使用 JET_prepCancel 呼叫<strong>JetPrepareUpdate</strong> ，但無法復原 JET_coltypLongBinary 類型 JET_coltypLongText 和/或資料行的資料行所做的所有變更。</span><span class="sxs-lookup"><span data-stu-id="a2816-168"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but could not rollback all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2816-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a2816-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a2816-170">此旗標不能同時與多個執行緒中的相同會話一起使用。</span><span class="sxs-lookup"><span data-stu-id="a2816-170">This flag cannot be used with the same session from more than one thread at the same time.</span></span> <span data-ttu-id="a2816-171">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a2816-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2816-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a2816-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a2816-173">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="a2816-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2816-174">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="a2816-174">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="a2816-175">使用 JET_prepCancel 呼叫<strong>JetPrepareUpdate</strong> ，但資料指標不是處於已備妥的狀態。</span><span class="sxs-lookup"><span data-stu-id="a2816-175"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a2816-176">成功時，資料指標會針對所需的更新目的變更為備妥狀態，或者，如果是 JET_prepCancel，則會將資料指標還原為未備妥狀態，並捨棄任何變更。</span><span class="sxs-lookup"><span data-stu-id="a2816-176">On success, the cursor is changed to the prepared state for the purpose of the desired update, or in the case of JET_prepCancel, the cursor is reverted to the non-prepared state and any changes are discarded.</span></span>

<span data-ttu-id="a2816-177">失敗時，資料指標狀態會保持不變。</span><span class="sxs-lookup"><span data-stu-id="a2816-177">On failure, the cursor state is left unchanged.</span></span> <span data-ttu-id="a2816-178">如果 JET_errRollbackError 失敗，則資料指標狀態會變更為未就緒狀態，但並非所有變更都已還原。</span><span class="sxs-lookup"><span data-stu-id="a2816-178">If the failure was JET_errRollbackError then the cursor state is changed to the non-prepared state but not all of the changes have been reverted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a2816-179">備註</span><span class="sxs-lookup"><span data-stu-id="a2816-179">Remarks</span></span>

<span data-ttu-id="a2816-180">當記錄共用 JET_coltypLongText 和/或 JET_coltypLongBinary 類型的資料時，插入記錄的副本是很重要的優化。</span><span class="sxs-lookup"><span data-stu-id="a2816-180">Inserting a copy of a record is an important optimization when records share data of type JET_coltypLongText and/or JET_coltypLongBinary.</span></span> <span data-ttu-id="a2816-181">這項資料會在很大的情況下儲存在記錄中，而且可能會有多筆記錄共用相同的資料實體標記法。</span><span class="sxs-lookup"><span data-stu-id="a2816-181">This data is stored off-record when large and it is possible for multiple records to share the same physical representation of the data.</span></span> <span data-ttu-id="a2816-182">在此情況下，資料可以從任一記錄進行更新，但這麼做會導致資料突然增加，讓每一筆記錄都有自己的複本。</span><span class="sxs-lookup"><span data-stu-id="a2816-182">In this case, the data can be updated from either record, but doing so will cause the data to be burst such that each record has its own copy.</span></span> <span data-ttu-id="a2816-183">您無法藉由另一筆記錄的修改來變更某筆記錄中的資料。</span><span class="sxs-lookup"><span data-stu-id="a2816-183">It is not possible to change data in one record by a modification from another record.</span></span> <span data-ttu-id="a2816-184">此外，也無法透過更新另一筆記錄來封鎖某一筆記錄的更新。</span><span class="sxs-lookup"><span data-stu-id="a2816-184">Also, it is not possible to block an update of one record by an update of another record.</span></span> <span data-ttu-id="a2816-185">這是 ESE 的集中功能，也稱為記錄層級鎖定。</span><span class="sxs-lookup"><span data-stu-id="a2816-185">This is a central feature to ESE and is known as Record Level Locking.</span></span>

<span data-ttu-id="a2816-186">失敗的[JetUpdate](./jetupdate-function.md)作業會將資料指標保持在「更新準備」狀態。</span><span class="sxs-lookup"><span data-stu-id="a2816-186">[JetUpdate](./jetupdate-function.md) operations which fail leave the cursor in the update prepared state.</span></span> <span data-ttu-id="a2816-187">這是為了允許更正某些錯誤，例如錯誤的資料行值，而不需要重新建立更新狀態。</span><span class="sxs-lookup"><span data-stu-id="a2816-187">This is to permit correction to some errors, such as a wrong column value, without requiring the update state to be recreated.</span></span> <span data-ttu-id="a2816-188">這表示在所有情況下，如果資料指標放棄更新，它就必須使用 JET_prepCancel 明確地呼叫 **JetPrepareUpdate** 。</span><span class="sxs-lookup"><span data-stu-id="a2816-188">This means that in all cases where a cursor abandons an update, it must explicitly call **JetPrepareUpdate** with JET_prepCancel.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a2816-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2816-189">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2816-190"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="a2816-190"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a2816-191">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="a2816-191">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2816-192"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="a2816-192"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a2816-193">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="a2816-193">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2816-194"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="a2816-194"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a2816-195">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="a2816-195">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2816-196"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="a2816-196"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a2816-197">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="a2816-197">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2816-198"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a2816-198"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a2816-199">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="a2816-199">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a2816-200">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2816-200">See Also</span></span>

[<span data-ttu-id="a2816-201">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a2816-201">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a2816-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a2816-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a2816-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a2816-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a2816-204">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="a2816-204">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="a2816-205">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="a2816-205">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="a2816-206">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="a2816-206">JetUpdate</span></span>](./jetupdate-function.md)
