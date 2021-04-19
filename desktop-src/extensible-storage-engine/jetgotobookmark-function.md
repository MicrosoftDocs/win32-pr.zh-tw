---
description: 深入瞭解： JetGotoBookmark 函數
title: JetGotoBookmark 函式
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 89dde261648b396bcfc9532911c0d4acd3c88828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983882"
---
# <a name="jetgotobookmark-function"></a><span data-ttu-id="a8944-103">JetGotoBookmark 函式</span><span class="sxs-lookup"><span data-stu-id="a8944-103">JetGotoBookmark Function</span></span>


<span data-ttu-id="a8944-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a8944-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotobookmark-function"></a><span data-ttu-id="a8944-105">JetGotoBookmark 函式</span><span class="sxs-lookup"><span data-stu-id="a8944-105">JetGotoBookmark Function</span></span>

<span data-ttu-id="a8944-106">**JetGotoBookmark** 函式會將游標放置在與指定書簽相關聯之記錄的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="a8944-106">The **JetGotoBookmark** function positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="a8944-107">書簽可以搭配資料表上定義的任何索引使用。</span><span class="sxs-lookup"><span data-stu-id="a8944-107">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="a8944-108">您可以使用 [JetGetBookmark](./jetgetbookmark-function.md)來取出記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="a8944-108">The bookmark for a record can be retrieved using [JetGetBookmark](./jetgetbookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a><span data-ttu-id="a8944-109">參數</span><span class="sxs-lookup"><span data-stu-id="a8944-109">Parameters</span></span>

<span data-ttu-id="a8944-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a8944-110">*sesid*</span></span>

<span data-ttu-id="a8944-111">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="a8944-111">The session to use for this call.</span></span>

<span data-ttu-id="a8944-112">*tableid*</span><span class="sxs-lookup"><span data-stu-id="a8944-112">*tableid*</span></span>

<span data-ttu-id="a8944-113">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="a8944-113">The cursor to use for this call.</span></span>

<span data-ttu-id="a8944-114">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="a8944-114">*pvBookmark*</span></span>

<span data-ttu-id="a8944-115">包含要用來放置游標之書簽的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a8944-115">The buffer that contains the bookmark to use to position the cursor.</span></span>

<span data-ttu-id="a8944-116">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="a8944-116">*cbBookmark*</span></span>

<span data-ttu-id="a8944-117">緩衝區中書簽的大小。</span><span class="sxs-lookup"><span data-stu-id="a8944-117">The size of the bookmark in the buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="a8944-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8944-118">Return Value</span></span>

<span data-ttu-id="a8944-119">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="a8944-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a8944-120">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="a8944-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8944-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a8944-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="a8944-122">Description</span><span class="sxs-lookup"><span data-stu-id="a8944-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8944-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a8944-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a8944-124">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="a8944-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8944-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a8944-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a8944-126">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="a8944-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8944-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a8944-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a8944-128">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="a8944-128">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a8944-129"><strong>WINDOWS XP：</strong>   這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="a8944-129"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8944-130">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="a8944-130">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="a8944-131">提供的書簽無效。</span><span class="sxs-lookup"><span data-stu-id="a8944-131">The bookmark that was provided is invalid.</span></span> <span data-ttu-id="a8944-132">發生這種情況的原因可能是書簽的大小為零，或書簽緩衝區指標為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="a8944-132">This might have occurred because the size of the bookmark is zero or the bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8944-133">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="a8944-133">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="a8944-134">資料指標位於次要索引上，而且找不到與書簽相關聯之記錄的索引項目。</span><span class="sxs-lookup"><span data-stu-id="a8944-134">The cursor is on a secondary index and no index entry could be found for the record that is associated with the bookmark.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8944-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a8944-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a8944-136">無法完成作業，因為與該會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="a8944-136">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8944-137">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="a8944-137">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="a8944-138">找不到與書簽相關聯的記錄。</span><span class="sxs-lookup"><span data-stu-id="a8944-138">The record that is associated with the bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8944-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a8944-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a8944-140">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="a8944-140">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8944-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a8944-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a8944-142">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="a8944-142">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="a8944-143"><strong>WINDOWS XP：</strong>   這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="a8944-143"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8944-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a8944-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a8944-145">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="a8944-145">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a8944-146">如果此函式成功，游標將放置在與指定書簽相關聯之記錄的索引項目上。</span><span class="sxs-lookup"><span data-stu-id="a8944-146">If this function succeeds, the cursor will be positioned at an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="a8944-147">如果已備妥記錄以進行更新，就會取消該更新。</span><span class="sxs-lookup"><span data-stu-id="a8944-147">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="a8944-148">如果索引範圍有效，就會取消該索引範圍。</span><span class="sxs-lookup"><span data-stu-id="a8944-148">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="a8944-149">如果已針對資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a8944-149">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="a8944-150">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="a8944-150">No change to the database state will occur.</span></span>

<span data-ttu-id="a8944-151">如果此函式失敗，則資料指標的位置會保持不變。</span><span class="sxs-lookup"><span data-stu-id="a8944-151">If this function fails, the position of the cursor will remain unchanged.</span></span> <span data-ttu-id="a8944-152">如果已備妥記錄以進行更新，就會取消該更新。</span><span class="sxs-lookup"><span data-stu-id="a8944-152">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="a8944-153">如果索引範圍有效，就會取消該索引範圍。</span><span class="sxs-lookup"><span data-stu-id="a8944-153">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="a8944-154">如果已針對資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a8944-154">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="a8944-155">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="a8944-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a8944-156">備註</span><span class="sxs-lookup"><span data-stu-id="a8944-156">Remarks</span></span>

<span data-ttu-id="a8944-157">使用書簽將游標放在索引上的方式有兩種。</span><span class="sxs-lookup"><span data-stu-id="a8944-157">There are two ways to use a bookmark to position a cursor on an index.</span></span> <span data-ttu-id="a8944-158">第一個是使用書簽直接在記錄上定位。</span><span class="sxs-lookup"><span data-stu-id="a8944-158">The first is to use the bookmark to position on the record directly.</span></span> <span data-ttu-id="a8944-159">當目前的資料指標索引為主要索引時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="a8944-159">This occurs when the current index of the cursor is the primary index.</span></span> <span data-ttu-id="a8944-160">這項技術的運作方式是因為 ESENT 書簽與相關記錄的主鍵相同。</span><span class="sxs-lookup"><span data-stu-id="a8944-160">This technique works because an ESENT bookmark is the same as the associated record's primary key.</span></span>

<span data-ttu-id="a8944-161">使用書簽的第二種方式是將它放在次要索引的專案上，其對應于與該書簽相關聯的記錄。</span><span class="sxs-lookup"><span data-stu-id="a8944-161">The second way to use a bookmark is to position it on an entry in a secondary index that corresponds to the record that is associated with that bookmark.</span></span> <span data-ttu-id="a8944-162">在這個過程中，引擎會使用主要索引上的書簽來查閱實際記錄。</span><span class="sxs-lookup"><span data-stu-id="a8944-162">During this process, the engine looks up the actual record using the bookmark on the primary index.</span></span> <span data-ttu-id="a8944-163">然後，它會使用記錄資料和次要索引定義，將索引鍵計算到指向記錄的次要索引。</span><span class="sxs-lookup"><span data-stu-id="a8944-163">It then uses the record data and the secondary index definition to compute a key into the secondary index that points to the record.</span></span> <span data-ttu-id="a8944-164">然後，它會將游標放在該索引鍵的索引項目上。</span><span class="sxs-lookup"><span data-stu-id="a8944-164">It then positions the cursor on the index entry for that key.</span></span> <span data-ttu-id="a8944-165">如果資料指標目前位於一個或多個多重值索引鍵資料行的次要索引上，則資料指標將定位於對應于每個索引鍵資料行之第一個多重值的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="a8944-165">If the cursor is currently on a secondary index over one or more multi-valued key columns, the cursor will be positioned on the index entry corresponding to the first multi-value of each of those key columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a8944-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8944-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8944-167"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="a8944-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a8944-168">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="a8944-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8944-169"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="a8944-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a8944-170">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="a8944-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8944-171"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="a8944-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a8944-172">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="a8944-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8944-173"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="a8944-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a8944-174">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="a8944-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8944-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a8944-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a8944-176">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="a8944-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a8944-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8944-177">See Also</span></span>

[<span data-ttu-id="a8944-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a8944-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a8944-179">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a8944-179">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a8944-180">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a8944-180">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a8944-181">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="a8944-181">JetGetBookmark</span></span>](./jetgetbookmark-function.md)
