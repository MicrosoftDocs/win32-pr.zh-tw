---
description: 深入瞭解： JetUpdate 函數
title: JetUpdate 函式
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38e17c5bc5ac32ab3b904456f2d97aa465fca670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848178"
---
# <a name="jetupdate-function"></a><span data-ttu-id="47546-103">JetUpdate 函式</span><span class="sxs-lookup"><span data-stu-id="47546-103">JetUpdate Function</span></span>


<span data-ttu-id="47546-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="47546-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate-function"></a><span data-ttu-id="47546-105">JetUpdate 函式</span><span class="sxs-lookup"><span data-stu-id="47546-105">JetUpdate Function</span></span>

<span data-ttu-id="47546-106">**JetUpdate** 函式會執行更新作業，包括將新的資料列插入資料表或更新現有的資料列。</span><span class="sxs-lookup"><span data-stu-id="47546-106">The **JetUpdate** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="47546-107">藉由呼叫 [JetDelete](./jetdelete-function.md)來執行刪除資料表資料列。</span><span class="sxs-lookup"><span data-stu-id="47546-107">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="47546-108">**JetUpdate** 是執行插入或更新的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="47546-108">**JetUpdate** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="47546-109">此更新的開始方式是呼叫 [JetPrepareUpdate](./jetprepareupdate-function.md) ，然後呼叫 [JetSetColumn](./jetsetcolumn-function.md) 或 [JetSetColumns](./jetsetcolumns-function.md) 一或多次來設定記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="47546-109">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="47546-110">最後，會呼叫 **JetUpdate** 來完成更新作業。</span><span class="sxs-lookup"><span data-stu-id="47546-110">Finally, **JetUpdate** is called to complete the update operation.</span></span> <span data-ttu-id="47546-111">只有 **JetUpdate** 或 [JetUpdate2](./jetupdate2-function.md)才會更新索引，而不是在 [JetSetColumn](./jetsetcolumn-function.md) 或 [JetSetColumns](./jetsetcolumns-function.md)期間更新。</span><span class="sxs-lookup"><span data-stu-id="47546-111">Indexes are updated only by **JetUpdate** or [JetUpdate2](./jetupdate2-function.md), and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="47546-112">參數</span><span class="sxs-lookup"><span data-stu-id="47546-112">Parameters</span></span>

<span data-ttu-id="47546-113">*sesid*</span><span class="sxs-lookup"><span data-stu-id="47546-113">*sesid*</span></span>

<span data-ttu-id="47546-114">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="47546-114">The session to use for this call.</span></span>

<span data-ttu-id="47546-115">*tableid*</span><span class="sxs-lookup"><span data-stu-id="47546-115">*tableid*</span></span>

<span data-ttu-id="47546-116">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="47546-116">The cursor to use for this call.</span></span>

<span data-ttu-id="47546-117">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="47546-117">*pvBookmark*</span></span>

<span data-ttu-id="47546-118">插入之資料列的傳回書簽指標。</span><span class="sxs-lookup"><span data-stu-id="47546-118">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="47546-119">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="47546-119">*cbBookmark*</span></span>

<span data-ttu-id="47546-120">*PvBookmark* 所指向的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="47546-120">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="47546-121">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="47546-121">*pcbActual*</span></span>

<span data-ttu-id="47546-122">在 *pvBookmark* 中傳回的插入資料列之書簽的傳回大小。</span><span class="sxs-lookup"><span data-stu-id="47546-122">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

### <a name="return-value"></a><span data-ttu-id="47546-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="47546-123">Return Value</span></span>

<span data-ttu-id="47546-124">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="47546-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="47546-125">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="47546-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47546-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="47546-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="47546-127">Description</span><span class="sxs-lookup"><span data-stu-id="47546-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47546-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="47546-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="47546-129">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="47546-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47546-130">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="47546-130">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="47546-131">記錄書簽的指定緩衝區不夠大，無法儲存記錄書簽。</span><span class="sxs-lookup"><span data-stu-id="47546-131">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47546-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="47546-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="47546-133">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="47546-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47546-134">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="47546-134">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="47546-135">與 JET_errNullInvalid 相同。</span><span class="sxs-lookup"><span data-stu-id="47546-135">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47546-136">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="47546-136">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="47546-137">更新作業需要資料庫檔案成長或記錄檔配置，但是資料庫檔案或記錄檔所在的磁片磁碟機已滿。</span><span class="sxs-lookup"><span data-stu-id="47546-137">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="47546-138">或者，資料庫檔案位於 FAT32 格式化的磁片區上，且資料庫檔案已4GBytes，也就是針對 FAT32 的每個檔案限制。</span><span class="sxs-lookup"><span data-stu-id="47546-138">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47546-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="47546-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="47546-140">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="47546-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="47546-141"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="47546-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47546-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="47546-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="47546-143"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>函式中指定的<em>準備</em>參數不是有效的旗標。</span><span class="sxs-lookup"><span data-stu-id="47546-143">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47546-144">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="47546-144">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="47546-145">此記錄的索引鍵是資料表中已經有另一筆記錄的另一個索引鍵重複的索引鍵，且索引不允許重複。</span><span class="sxs-lookup"><span data-stu-id="47546-145">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47546-146">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="47546-146">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="47546-147">插入或更新的記錄有一或多個索引，而產生的索引鍵會超過允許的大小上限。</span><span class="sxs-lookup"><span data-stu-id="47546-147">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="47546-148">因此，作業無法防止金鑰截斷。</span><span class="sxs-lookup"><span data-stu-id="47546-148">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47546-149">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="47546-149">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="47546-150">插入或更新的記錄中有一個索引多值資料行，其中有兩個以上的值，在為索引設定的最大長度索引鍵大小中都相同。</span><span class="sxs-lookup"><span data-stu-id="47546-150">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="47546-151">如此一來，該記錄在索引中會有兩個相同的專案無效。</span><span class="sxs-lookup"><span data-stu-id="47546-151">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47546-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="47546-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="47546-153">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="47546-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47546-154">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="47546-154">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="47546-155">要插入之記錄中的一個或多個資料行，或在要取代之記錄的更新狀態為 <strong>Null</strong> ，這違反了這些資料行的定義條件約束。</span><span class="sxs-lookup"><span data-stu-id="47546-155">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47546-156">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="47546-156">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="47546-157">定義了一或多個索引，不允許 <strong>Null</strong> 索引鍵，而且所取代之記錄的插入或更新狀態違反了此定義的條件約束。</span><span class="sxs-lookup"><span data-stu-id="47546-157">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47546-158">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="47546-158">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="47546-159">記錄取代作業已更新 primary key。</span><span class="sxs-lookup"><span data-stu-id="47546-159">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="47546-160">主鍵資料行的更新必須透過刪除現有的記錄，並使用所需的資料插入新記錄來完成。</span><span class="sxs-lookup"><span data-stu-id="47546-160">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47546-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="47546-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="47546-162">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="47546-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47546-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="47546-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="47546-164">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="47546-164">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="47546-165"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="47546-165"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47546-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="47546-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="47546-167">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="47546-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47546-168">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="47546-168">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="47546-169">在唯讀交易範圍內嘗試進行更新是不合法的。</span><span class="sxs-lookup"><span data-stu-id="47546-169">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="47546-170">「唯讀交易」（read only transaction）是指使用 JET_bitTransactionReadOnly 呼叫 <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> 來啟動的交易。</span><span class="sxs-lookup"><span data-stu-id="47546-170">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="47546-171"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="47546-171"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47546-172">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="47546-172">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="47546-173">使用 JET_prepCancel 呼叫<a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> ，但資料指標不是處於已備妥的狀態。</span><span class="sxs-lookup"><span data-stu-id="47546-173"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47546-174">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="47546-174">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="47546-175">作業失敗，因為沒有足夠的記憶體可保留有關更新的交易資訊。</span><span class="sxs-lookup"><span data-stu-id="47546-175">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47546-176">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="47546-176">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="47546-177">另一個會話先前已鎖定記錄以進行更新。</span><span class="sxs-lookup"><span data-stu-id="47546-177">Another session has previously locked the record for update.</span></span> <span data-ttu-id="47546-178">此會話嘗試的更新將會失敗。</span><span class="sxs-lookup"><span data-stu-id="47546-178">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="47546-179">成功時，資料指標上的開啟更新作業已完成。</span><span class="sxs-lookup"><span data-stu-id="47546-179">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="47546-180">如果為數據表定義了自動遞增資料行，就會針對插入的記錄設定這個值。</span><span class="sxs-lookup"><span data-stu-id="47546-180">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="47546-181">如果為數據表定義了版本資料行，則會為新插入的記錄初始化其值，或在每次取代記錄時遞增。</span><span class="sxs-lookup"><span data-stu-id="47546-181">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="47546-182">所有索引（包括叢集和非叢集索引）都會更新。</span><span class="sxs-lookup"><span data-stu-id="47546-182">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="47546-183">失敗時，不會對資料庫進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="47546-183">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="47546-184">在插入之前和取代回呼函式之前，可能已經呼叫，但是在插入之後和取代的回呼都不會被呼叫，因為後者無法使更新失敗。</span><span class="sxs-lookup"><span data-stu-id="47546-184">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="47546-185">資料指標複製緩衝區會留在它的備妥狀態，如此一來，就有機會以累加方式更正造成錯誤的問題，然後重試更新作業。</span><span class="sxs-lookup"><span data-stu-id="47546-185">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="47546-186">備註</span><span class="sxs-lookup"><span data-stu-id="47546-186">Remarks</span></span>

<span data-ttu-id="47546-187">您可以註冊回呼函式，以便在插入之前或之後，以及在更新之前或之後呼叫。</span><span class="sxs-lookup"><span data-stu-id="47546-187">Callback functions can be registered to be called before or after insert, and before or after update.</span></span>

<span data-ttu-id="47546-188">[JetSetColumn](./jetsetcolumn-function.md)會強制執行記錄大小限制，而不是 **JetUpdate** 一般。</span><span class="sxs-lookup"><span data-stu-id="47546-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by **JetUpdate**.</span></span>

<span data-ttu-id="47546-189">請務必瞭解在單一交易內執行大量更新作業的影響。</span><span class="sxs-lookup"><span data-stu-id="47546-189">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="47546-190">資料庫引擎必須在版本存放區中追蹤資料庫的每個更新。</span><span class="sxs-lookup"><span data-stu-id="47546-190">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="47546-191">版本存放區會保留資料庫中每個記錄或索引項目目之所有不同版本的即時記錄，以供所有使用中的交易看到。</span><span class="sxs-lookup"><span data-stu-id="47546-191">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="47546-192">這些版本是用來支援資料庫引擎使用的多版本並行控制，以支援使用快照集隔離的交易。</span><span class="sxs-lookup"><span data-stu-id="47546-192">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="47546-193">一旦資料庫引擎耗盡用來儲存這些版本的資源之後，就無法再接受進一步的變更，直到某些交易已結束，才能回收這些資源。</span><span class="sxs-lookup"><span data-stu-id="47546-193">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="47546-194">當引擎處於這種狀態時，所有更新都會失敗並 JET_errVersionStoreOutOfMemory。</span><span class="sxs-lookup"><span data-stu-id="47546-194">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="47546-195">資料庫引擎用來儲存這些版本的資源，可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 [JET_paramMaxVerPages](./resource-parameters.md) 和 [JET_paramGlobalMinVerPages](./resource-parameters.md)來控制。</span><span class="sxs-lookup"><span data-stu-id="47546-195">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramMaxVerPages](./resource-parameters.md) and [JET_paramGlobalMinVerPages](./resource-parameters.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="47546-196">規格需求</span><span class="sxs-lookup"><span data-stu-id="47546-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47546-197"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="47546-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="47546-198">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="47546-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47546-199"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="47546-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="47546-200">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="47546-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47546-201"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="47546-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="47546-202">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="47546-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47546-203"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="47546-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="47546-204">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="47546-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47546-205"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="47546-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="47546-206">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="47546-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="47546-207">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47546-207">See Also</span></span>

[<span data-ttu-id="47546-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="47546-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="47546-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="47546-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="47546-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="47546-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="47546-211">JetDelete</span><span class="sxs-lookup"><span data-stu-id="47546-211">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="47546-212">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="47546-212">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="47546-213">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="47546-213">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="47546-214">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="47546-214">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="47546-215">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="47546-215">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="47546-216">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="47546-216">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="47546-217">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="47546-217">JetSetColumns</span></span>](./jetsetcolumns-function.md)  
[<span data-ttu-id="47546-218">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="47546-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="47546-219">系統參數</span><span class="sxs-lookup"><span data-stu-id="47546-219">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
