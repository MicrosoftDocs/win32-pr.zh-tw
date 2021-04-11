---
description: 深入瞭解： JetUpdate2 函數
title: JetUpdate2 函式
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc08b26ebff33a68654ed33a2cb0539af1fa2a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689915"
---
# <a name="jetupdate2-function"></a><span data-ttu-id="4de2b-103">JetUpdate2 函式</span><span class="sxs-lookup"><span data-stu-id="4de2b-103">JetUpdate2 Function</span></span>


<span data-ttu-id="4de2b-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4de2b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate2-function"></a><span data-ttu-id="4de2b-105">JetUpdate2 函式</span><span class="sxs-lookup"><span data-stu-id="4de2b-105">JetUpdate2 Function</span></span>

<span data-ttu-id="4de2b-106">**JetUpdate2** 函式會執行更新作業，包括將新的資料列插入資料表或更新現有的資料列。</span><span class="sxs-lookup"><span data-stu-id="4de2b-106">The **JetUpdate2** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="4de2b-107">此函式包含在執行更新時可設定的 *grbit* 選項清單。</span><span class="sxs-lookup"><span data-stu-id="4de2b-107">This function contains a list of *grbit* options that can be set while performing an update.</span></span> <span data-ttu-id="4de2b-108">藉由呼叫 [JetDelete](./jetdelete-function.md)來執行刪除資料表資料列。</span><span class="sxs-lookup"><span data-stu-id="4de2b-108">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="4de2b-109">**Windows server 2003： JetUpdate2** 是在 windows server 2003 中引進。</span><span class="sxs-lookup"><span data-stu-id="4de2b-109">**Windows Server 2003:  JetUpdate2** is introduced in Windows Server 2003.</span></span>

<span data-ttu-id="4de2b-110">**JetUpdate2** 是執行插入或更新的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="4de2b-110">**JetUpdate2** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="4de2b-111">此更新的開始方式是呼叫 [JetPrepareUpdate](./jetprepareupdate-function.md) ，然後呼叫 [JetSetColumn](./jetsetcolumn-function.md) 或 [JetSetColumns](./jetsetcolumns-function.md) 一或多次來設定記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="4de2b-111">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="4de2b-112">最後，會呼叫 **JetUpdate2** 來完成更新作業。</span><span class="sxs-lookup"><span data-stu-id="4de2b-112">Finally, **JetUpdate2** is called to complete the update operation.</span></span> <span data-ttu-id="4de2b-113">只有 [JetUpdate](./jetupdate-function.md) 或 **JetUpdate2** 才會更新索引，而不是在 [JetSetColumn](./jetsetcolumn-function.md) 或 [JetSetColumns](./jetsetcolumns-function.md)期間更新。</span><span class="sxs-lookup"><span data-stu-id="4de2b-113">Indexes are updated only by [JetUpdate](./jetupdate-function.md) or **JetUpdate2**, and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="4de2b-114">參數</span><span class="sxs-lookup"><span data-stu-id="4de2b-114">Parameters</span></span>

<span data-ttu-id="4de2b-115">*sesid*</span><span class="sxs-lookup"><span data-stu-id="4de2b-115">*sesid*</span></span>

<span data-ttu-id="4de2b-116">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="4de2b-116">The session to use for this call.</span></span>

<span data-ttu-id="4de2b-117">*tableid*</span><span class="sxs-lookup"><span data-stu-id="4de2b-117">*tableid*</span></span>

<span data-ttu-id="4de2b-118">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="4de2b-118">The cursor to use for this call.</span></span>

<span data-ttu-id="4de2b-119">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="4de2b-119">*pvBookmark*</span></span>

<span data-ttu-id="4de2b-120">插入之資料列的傳回書簽指標。</span><span class="sxs-lookup"><span data-stu-id="4de2b-120">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="4de2b-121">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="4de2b-121">*cbBookmark*</span></span>

<span data-ttu-id="4de2b-122">*PvBookmark* 所指向的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="4de2b-122">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="4de2b-123">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="4de2b-123">*pcbActual*</span></span>

<span data-ttu-id="4de2b-124">在 *pvBookmark* 中傳回的插入資料列之書簽的傳回大小。</span><span class="sxs-lookup"><span data-stu-id="4de2b-124">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

<span data-ttu-id="4de2b-125">*grbit*</span><span class="sxs-lookup"><span data-stu-id="4de2b-125">*grbit*</span></span>

<span data-ttu-id="4de2b-126">位群組，其中包含要用於此呼叫的選項，包括下列零或多個。</span><span class="sxs-lookup"><span data-stu-id="4de2b-126">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4de2b-127">值</span><span class="sxs-lookup"><span data-stu-id="4de2b-127">Value</span></span></p></th>
<th><p><span data-ttu-id="4de2b-128">意義</span><span class="sxs-lookup"><span data-stu-id="4de2b-128">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-129">JET_bitUpdateCheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="4de2b-129">JET_bitUpdateCheckESE97Compatibility</span></span></p></td>
<td><p><span data-ttu-id="4de2b-130">如果在 Windows 2000 版的 ESE 中不可能進行更新，此旗標會導致更新傳回錯誤，這會在每一筆記錄中強制執行較小數目的多重值資料行實例，而不是較新的 ESE 版本。</span><span class="sxs-lookup"><span data-stu-id="4de2b-130">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="4de2b-131">這僅適用于想要在 Windows 2000 上裝載的應用程式與 Windows Server 2003 或更新版本的 ESE 上裝載的應用程式之間複寫資料的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4de2b-131">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows Server 2003, or later versions of ESE.</span></span> <span data-ttu-id="4de2b-132">大部分的應用程式都不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="4de2b-132">It should not be necessary for most applications.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="4de2b-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="4de2b-133">Return Value</span></span>

<span data-ttu-id="4de2b-134">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="4de2b-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4de2b-135">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="4de2b-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4de2b-136">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4de2b-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="4de2b-137">Description</span><span class="sxs-lookup"><span data-stu-id="4de2b-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4de2b-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4de2b-139">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="4de2b-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de2b-140">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="4de2b-140">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="4de2b-141">記錄書簽的指定緩衝區不夠大，無法儲存記錄書簽。</span><span class="sxs-lookup"><span data-stu-id="4de2b-141">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-142">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4de2b-142">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4de2b-143">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="4de2b-143">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de2b-144">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="4de2b-144">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="4de2b-145">更新作業需要資料庫檔案成長或記錄檔配置，但是資料庫檔案或記錄檔所在的磁片磁碟機已滿。</span><span class="sxs-lookup"><span data-stu-id="4de2b-145">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="4de2b-146">或者，資料庫檔案位於 FAT32 格式化的磁片區上，且資料庫檔案已4GBytes，也就是針對 FAT32 的每個檔案限制。</span><span class="sxs-lookup"><span data-stu-id="4de2b-146">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4de2b-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4de2b-148">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="4de2b-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="4de2b-149"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="4de2b-149"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de2b-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4de2b-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4de2b-151"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>函式中指定的<em>準備</em>參數不是有效的旗標。</span><span class="sxs-lookup"><span data-stu-id="4de2b-151">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-152">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="4de2b-152">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="4de2b-153">此記錄的索引鍵是資料表中已經有另一筆記錄的另一個索引鍵重複的索引鍵，且索引不允許重複。</span><span class="sxs-lookup"><span data-stu-id="4de2b-153">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de2b-154">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="4de2b-154">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="4de2b-155">插入或更新的記錄有一或多個索引，而產生的索引鍵會超過允許的大小上限。</span><span class="sxs-lookup"><span data-stu-id="4de2b-155">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="4de2b-156">因此，作業無法防止金鑰截斷。</span><span class="sxs-lookup"><span data-stu-id="4de2b-156">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-157">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="4de2b-157">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="4de2b-158">插入或更新的記錄中有一個索引多值資料行，其中有兩個以上的值，在為索引設定的最大長度索引鍵大小中都相同。</span><span class="sxs-lookup"><span data-stu-id="4de2b-158">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="4de2b-159">如此一來，該記錄在索引中會有兩個相同的專案無效。</span><span class="sxs-lookup"><span data-stu-id="4de2b-159">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de2b-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4de2b-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4de2b-161">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="4de2b-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-162">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="4de2b-162">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="4de2b-163">要插入之記錄中的一個或多個資料行，或在要取代之記錄的更新狀態為 <strong>Null</strong> ，這違反了這些資料行的定義條件約束。</span><span class="sxs-lookup"><span data-stu-id="4de2b-163">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de2b-164">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="4de2b-164">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="4de2b-165">定義了一或多個索引，不允許 <strong>Null</strong> 索引鍵，而且所取代之記錄的插入或更新狀態違反了此定義的條件約束。</span><span class="sxs-lookup"><span data-stu-id="4de2b-165">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-166">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="4de2b-166">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="4de2b-167">記錄取代作業已更新 primary key。</span><span class="sxs-lookup"><span data-stu-id="4de2b-167">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="4de2b-168">主鍵資料行的更新必須透過刪除現有的記錄，並使用所需的資料插入新記錄來完成。</span><span class="sxs-lookup"><span data-stu-id="4de2b-168">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de2b-169">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4de2b-169">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4de2b-170">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="4de2b-170">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-171">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4de2b-171">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4de2b-172">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="4de2b-172">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="4de2b-173"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="4de2b-173"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de2b-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4de2b-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4de2b-175">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="4de2b-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-176">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="4de2b-176">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="4de2b-177">使用 JET_prepCancel 呼叫<a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> ，但資料指標不是處於已備妥的狀態。</span><span class="sxs-lookup"><span data-stu-id="4de2b-177"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de2b-178">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="4de2b-178">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="4de2b-179">尚未配置寫入鎖定的記錄取代作業，在更新時可能會發生寫入衝突。</span><span class="sxs-lookup"><span data-stu-id="4de2b-179">A record replacement operation for which a write lock was not already allocated can encounter a write conflict at the time of update.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4de2b-180">成功時，資料指標上的開啟更新作業已完成。</span><span class="sxs-lookup"><span data-stu-id="4de2b-180">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="4de2b-181">如果為數據表定義了自動遞增資料行，就會針對插入的記錄設定這個值。</span><span class="sxs-lookup"><span data-stu-id="4de2b-181">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="4de2b-182">如果為數據表定義了版本資料行，則會為新插入的記錄初始化其值，或在每次取代記錄時遞增。</span><span class="sxs-lookup"><span data-stu-id="4de2b-182">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="4de2b-183">所有索引（包括叢集和非叢集索引）都會更新。</span><span class="sxs-lookup"><span data-stu-id="4de2b-183">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="4de2b-184">失敗時，不會對資料庫進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="4de2b-184">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="4de2b-185">在插入之前和取代回呼函式之前，可能已經呼叫，但是在插入之後和取代的回呼都不會被呼叫，因為後者無法使更新失敗。</span><span class="sxs-lookup"><span data-stu-id="4de2b-185">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="4de2b-186">資料指標複製緩衝區會留在它的備妥狀態，如此一來，就有機會以累加方式更正造成錯誤的問題，然後重試更新作業。</span><span class="sxs-lookup"><span data-stu-id="4de2b-186">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4de2b-187">備註</span><span class="sxs-lookup"><span data-stu-id="4de2b-187">Remarks</span></span>

<span data-ttu-id="4de2b-188">[JetSetColumn](./jetsetcolumn-function.md)會強制執行記錄大小限制，而不是[JetUpdate](./jetupdate-function.md)一般。</span><span class="sxs-lookup"><span data-stu-id="4de2b-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by [JetUpdate](./jetupdate-function.md).</span></span> <span data-ttu-id="4de2b-189">唯一的例外狀況是使用 JET_bitUpdateCheckESE97Compatibility 相容性旗標時。</span><span class="sxs-lookup"><span data-stu-id="4de2b-189">The only exception is when the JET_bitUpdateCheckESE97Compatibility compatibility flag is being used.</span></span> <span data-ttu-id="4de2b-190">在此情況下，會檢查整個記錄，因為已超過限制的個別 [JetSetColumn](./jetsetcolumn-function.md) 作業可能會由後續的 [JetSetColumn](./jetsetcolumn-function.md)呼叫來補償。</span><span class="sxs-lookup"><span data-stu-id="4de2b-190">In this case, the whole record is checked since an individual [JetSetColumn](./jetsetcolumn-function.md) operation that exceeded the limit may be compensated by a subsequent call to [JetSetColumn](./jetsetcolumn-function.md).</span></span>

<span data-ttu-id="4de2b-191">如需詳細資訊，請參閱 [JetUpdate](./jetupdate-function.md) 中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="4de2b-191">See the Remarks section in [JetUpdate](./jetupdate-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4de2b-192">規格需求</span><span class="sxs-lookup"><span data-stu-id="4de2b-192">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-193"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="4de2b-193"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4de2b-194">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="4de2b-194">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de2b-195"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="4de2b-195"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4de2b-196">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="4de2b-196">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-197"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="4de2b-197"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4de2b-198">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="4de2b-198">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4de2b-199"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="4de2b-199"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4de2b-200">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="4de2b-200">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4de2b-201"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4de2b-201"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4de2b-202">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="4de2b-202">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4de2b-203">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4de2b-203">See Also</span></span>

[<span data-ttu-id="4de2b-204">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4de2b-204">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4de2b-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4de2b-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4de2b-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="4de2b-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="4de2b-207">JetDelete</span><span class="sxs-lookup"><span data-stu-id="4de2b-207">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="4de2b-208">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="4de2b-208">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="4de2b-209">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="4de2b-209">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="4de2b-210">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="4de2b-210">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="4de2b-211">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="4de2b-211">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="4de2b-212">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="4de2b-212">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="4de2b-213">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="4de2b-213">JetSetColumns</span></span>](./jetsetcolumns-function.md)
