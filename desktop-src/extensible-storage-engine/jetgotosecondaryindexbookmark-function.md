---
description: 深入瞭解： JetGotoSecondaryIndexBookmark 函數
title: JetGotoSecondaryIndexBookmark 函式
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893833fd1770fe3d972033a4d10f9047b0f61dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944395"
---
# <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="7bf0f-103">JetGotoSecondaryIndexBookmark 函式</span><span class="sxs-lookup"><span data-stu-id="7bf0f-103">JetGotoSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="7bf0f-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7bf0f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="7bf0f-105">JetGotoSecondaryIndexBookmark 函式</span><span class="sxs-lookup"><span data-stu-id="7bf0f-105">JetGotoSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="7bf0f-106">**JetGotoSecondaryIndexBookmark** 函式會將游標放在與指定次要索引書簽相關聯的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-106">The **JetGotoSecondaryIndexBookmark** function positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="7bf0f-107">次要索引書簽必須與原始抓取的相同資料表上的相同索引一起使用。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-107">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="7bf0f-108">您可以使用 **JetGotoSecondaryIndexBookmark** 來取出索引項目的次要索引書簽。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-108">The secondary index bookmark for an index entry can be retrieved using **JetGotoSecondaryIndexBookmark**.</span></span>

<span data-ttu-id="7bf0f-109">**Windows xp：**  **JetGotoSecondaryIndexBookmark** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-109">**Windows XP:**  **JetGotoSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="7bf0f-110">參數</span><span class="sxs-lookup"><span data-stu-id="7bf0f-110">Parameters</span></span>

<span data-ttu-id="7bf0f-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="7bf0f-111">*sesid*</span></span>

<span data-ttu-id="7bf0f-112">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-112">The session to use for this call.</span></span>

<span data-ttu-id="7bf0f-113">*tableid*</span><span class="sxs-lookup"><span data-stu-id="7bf0f-113">*tableid*</span></span>

<span data-ttu-id="7bf0f-114">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-114">The cursor to use for this call.</span></span>

<span data-ttu-id="7bf0f-115">*pvSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="7bf0f-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="7bf0f-116">緩衝區，其中包含要用來放置游標的次要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-116">The buffer that contains the secondary key to use to position the cursor.</span></span>

<span data-ttu-id="7bf0f-117">*cbSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="7bf0f-117">*cbSecondaryKey*</span></span>

<span data-ttu-id="7bf0f-118">緩衝區中次要索引鍵的大小。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-118">The size of the secondary key in the buffer.</span></span>

<span data-ttu-id="7bf0f-119">*pvPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="7bf0f-119">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="7bf0f-120">包含要用來放置游標之主鍵書簽的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-120">The buffer that contains the primary key bookmark to use to position the cursor.</span></span>

<span data-ttu-id="7bf0f-121">*cbPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="7bf0f-121">*cbPrimaryBookmark*</span></span>

<span data-ttu-id="7bf0f-122">緩衝區中主鍵書簽的大小。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-122">The size of the primary key bookmark in the buffer.</span></span>

<span data-ttu-id="7bf0f-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="7bf0f-123">*grbit*</span></span>

<span data-ttu-id="7bf0f-124">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-124">A group of bits that specifies zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bf0f-125">值</span><span class="sxs-lookup"><span data-stu-id="7bf0f-125">Value</span></span></p></th>
<th><p><span data-ttu-id="7bf0f-126">意義</span><span class="sxs-lookup"><span data-stu-id="7bf0f-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bf0f-127">JET_bitBookmarkPermitVirtualCurrency</span><span class="sxs-lookup"><span data-stu-id="7bf0f-127">JET_bitBookmarkPermitVirtualCurrency</span></span></p></td>
<td><p><span data-ttu-id="7bf0f-128">如果找不到索引項目，就會將游標放在先前找到索引項目的位置。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-128">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="7bf0f-129">作業仍會因為 JET_errRecordDeleted 而失敗;不過，您可以移至下一個或上一個索引項目（相對於現在遺漏的索引項目）。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-129">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="7bf0f-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="7bf0f-130">Return Value</span></span>

<span data-ttu-id="7bf0f-131">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7bf0f-132">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bf0f-133">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7bf0f-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="7bf0f-134">Description</span><span class="sxs-lookup"><span data-stu-id="7bf0f-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bf0f-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7bf0f-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7bf0f-136">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bf0f-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7bf0f-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7bf0f-138">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bf0f-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7bf0f-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7bf0f-140">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-140">The operation cannot complete because is because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="7bf0f-141"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bf0f-142">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="7bf0f-142">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="7bf0f-143">提供的次要索引書簽無效。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-143">The secondary index bookmark that was provided was invalid.</span></span> <span data-ttu-id="7bf0f-144">發生此錯誤的原因可能是次要索引鍵為零，或次要金鑰緩衝區指標為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-144">This error might have occurred because the secondary key is zero or the secondary key buffer pointer is <strong>NULL</strong>.</span></span> <span data-ttu-id="7bf0f-145">發生此錯誤的原因是</span><span class="sxs-lookup"><span data-stu-id="7bf0f-145">This error occurs because</span></span></p>
<ul>
<li><p><span data-ttu-id="7bf0f-146">目前的次要索引沒有唯一性條件約束，且所提供書簽的大小為零。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-146">The current secondary index does not have a uniqueness constraint and the size of the provided bookmark is zero.</span></span></p></li>
<li><p><span data-ttu-id="7bf0f-147">書簽緩衝區指標為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-147">The bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bf0f-148">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="7bf0f-148">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="7bf0f-149">資料指標目前不在次要索引上。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-149">The cursor is not currently on a secondary index.</span></span> <span data-ttu-id="7bf0f-150">當資料指標目前未使用次要索引時，移至次要索引書簽並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-150">It is not meaningful to go to a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="7bf0f-151">當資料指標不在次要索引上時，應使用<a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> 。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-151"><a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bf0f-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7bf0f-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7bf0f-153">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-153">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bf0f-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="7bf0f-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="7bf0f-155">找不到與次要索引書簽相關聯的索引項目。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-155">The index entry that is associated with the secondary index bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bf0f-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7bf0f-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7bf0f-157">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-157">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bf0f-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="7bf0f-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="7bf0f-159">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="7bf0f-160"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-160"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bf0f-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7bf0f-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7bf0f-162">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-162">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7bf0f-163">如果此函式成功，游標將放置於與指定的次要索引書簽相關聯的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-163">If this function succeeds, the cursor will be positioned at an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="7bf0f-164">如果已備妥記錄以進行更新，就會取消該更新。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-164">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="7bf0f-165">如果索引範圍有效，就會取消該索引範圍。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-165">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="7bf0f-166">如果已針對要使用的資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-166">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="7bf0f-167">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-167">No change to the database state will occur.</span></span>

<span data-ttu-id="7bf0f-168">如果此函式失敗，除非傳回 JET_errRecordDeleted 並指定 JET_bitBookmarkPermitVirtualCurrency，否則資料指標的位置會保持不變。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-168">If this function fails, the position of the cursor remains unchanged unless JET_errRecordDeleted is returned and JET_bitBookmarkPermitVirtualCurrency is specified.</span></span> <span data-ttu-id="7bf0f-169">在這種情況下，游標將放置於與指定次要索引書簽相關聯的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-169">In that case, the cursor will be positioned where the index entry that is associated with the specified secondary index bookmark would have been.</span></span> <span data-ttu-id="7bf0f-170">資料指標可以相對於該位置移動，但仍不在有效的索引項目上。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-170">The cursor can be moved relative to that position, but is still not on a valid index entry.</span></span>

<span data-ttu-id="7bf0f-171">如果已備妥記錄以進行更新，就會取消該更新。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-171">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="7bf0f-172">如果索引範圍有效，就會取消該索引範圍。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-172">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="7bf0f-173">如果已針對要使用的資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-173">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="7bf0f-174">在任何情況下，都不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-174">In any case, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7bf0f-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="7bf0f-175">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bf0f-176"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="7bf0f-176"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7bf0f-177">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-177">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bf0f-178"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="7bf0f-178"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7bf0f-179">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-179">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bf0f-180"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="7bf0f-180"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7bf0f-181">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-181">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bf0f-182"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="7bf0f-182"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7bf0f-183">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-183">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bf0f-184"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7bf0f-184"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7bf0f-185">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="7bf0f-185">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7bf0f-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7bf0f-186">See Also</span></span>

[<span data-ttu-id="7bf0f-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7bf0f-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7bf0f-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7bf0f-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7bf0f-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7bf0f-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7bf0f-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7bf0f-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="7bf0f-191">JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="7bf0f-191">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)  
[<span data-ttu-id="7bf0f-192">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="7bf0f-192">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="7bf0f-193">JetStopService</span><span class="sxs-lookup"><span data-stu-id="7bf0f-193">JetStopService</span></span>](./jetstopservice-function.md)
