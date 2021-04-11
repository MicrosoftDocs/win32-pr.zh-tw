---
description: 深入瞭解： JetGetBookmark 函數
title: JetGetBookmark 函式
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a27ce474a8f021ff9039a07d7542b194e72e262a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115845"
---
# <a name="jetgetbookmark-function"></a><span data-ttu-id="e2497-103">JetGetBookmark 函式</span><span class="sxs-lookup"><span data-stu-id="e2497-103">JetGetBookmark Function</span></span>


<span data-ttu-id="e2497-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e2497-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetbookmark-function"></a><span data-ttu-id="e2497-105">JetGetBookmark 函式</span><span class="sxs-lookup"><span data-stu-id="e2497-105">JetGetBookmark Function</span></span>

<span data-ttu-id="e2497-106">**JetGetBookmark** 函式會在資料指標目前位置的索引項目目相關聯的記錄中，抓取與該記錄相關聯的書簽。</span><span class="sxs-lookup"><span data-stu-id="e2497-106">The **JetGetBookmark** function retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="e2497-107">然後，您可以使用這個書簽，將該資料指標重新放置到使用 [JetGoToBookmark](./jetgotobookmark-function.md)的相同記錄。</span><span class="sxs-lookup"><span data-stu-id="e2497-107">This bookmark can then be used to reposition that cursor back to the same record using [JetGoToBookmark](./jetgotobookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="e2497-108">參數</span><span class="sxs-lookup"><span data-stu-id="e2497-108">Parameters</span></span>

<span data-ttu-id="e2497-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e2497-109">*sesid*</span></span>

<span data-ttu-id="e2497-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="e2497-110">The session to use for this call.</span></span>

<span data-ttu-id="e2497-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="e2497-111">*tableid*</span></span>

<span data-ttu-id="e2497-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="e2497-112">The cursor to use for this call.</span></span>

<span data-ttu-id="e2497-113">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="e2497-113">*pvBookmark*</span></span>

<span data-ttu-id="e2497-114">接收書簽的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e2497-114">The output buffer that receives the bookmark.</span></span>

<span data-ttu-id="e2497-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="e2497-115">*cbMax*</span></span>

<span data-ttu-id="e2497-116">輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2497-116">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="e2497-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="e2497-117">*pcbActual*</span></span>

<span data-ttu-id="e2497-118">書簽的實際大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2497-118">The actual size, in bytes, of the bookmark.</span></span>

<span data-ttu-id="e2497-119">如果這個參數為 **Null** ，則不會傳回書簽的實際大小。</span><span class="sxs-lookup"><span data-stu-id="e2497-119">If this parameter is **NULL** then the actual size of the bookmark will not be returned.</span></span>

<span data-ttu-id="e2497-120">如果輸出緩衝區太小，則仍會傳回書簽的實際大小。</span><span class="sxs-lookup"><span data-stu-id="e2497-120">If the output buffer is too small, the actual size of the bookmark will still be returned.</span></span> <span data-ttu-id="e2497-121">這表示這個數位會大於輸出緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="e2497-121">That means that this number will be larger than the size of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="e2497-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2497-122">Return Value</span></span>

<span data-ttu-id="e2497-123">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="e2497-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e2497-124">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="e2497-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2497-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e2497-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="e2497-126">Description</span><span class="sxs-lookup"><span data-stu-id="e2497-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2497-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e2497-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e2497-128">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="e2497-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2497-129">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="e2497-129">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="e2497-130">作業已順利完成，但輸出緩衝區太小，無法接收整個書簽。</span><span class="sxs-lookup"><span data-stu-id="e2497-130">The operation completed successfully, but the output buffer was too small to receive the entire bookmark.</span></span> <span data-ttu-id="e2497-131">輸出緩衝區已填滿適當的書簽。</span><span class="sxs-lookup"><span data-stu-id="e2497-131">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="e2497-132">如果要求，也會傳回書簽的實際大小。</span><span class="sxs-lookup"><span data-stu-id="e2497-132">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2497-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e2497-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e2497-134">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="e2497-134">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2497-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e2497-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e2497-136">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="e2497-136">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="e2497-137"><strong>WINDOWS XP：  </strong>此傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="e2497-137"><strong>Windows XP:  </strong>This return values is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2497-138">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="e2497-138">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="e2497-139">資料指標未放置在記錄上。</span><span class="sxs-lookup"><span data-stu-id="e2497-139">The cursor is not positioned on a record.</span></span> <span data-ttu-id="e2497-140">此情況具有許多不同的原因。</span><span class="sxs-lookup"><span data-stu-id="e2497-140">This can happen for many different reasons.</span></span> <span data-ttu-id="e2497-141">例如，如果游標位於目前索引的最後一筆記錄之後，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="e2497-141">For example, this will happen if the cursor is positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2497-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e2497-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e2497-143">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="e2497-143">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2497-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e2497-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e2497-145">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="e2497-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2497-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e2497-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e2497-147">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="e2497-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="e2497-148"><strong>WINDOWS XP：  </strong>這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="e2497-148"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2497-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e2497-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e2497-150">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="e2497-150">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2497-151">如果此函式成功，則會在輸出緩衝區中傳回與資料指標目前位置的索引項目目相關聯之記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="e2497-151">If this function succeeds, the bookmark for the record that is associated with the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="e2497-152">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="e2497-152">No change to the database state will occur.</span></span>

<span data-ttu-id="e2497-153">如果此函式失敗，除非傳回 JET_errBufferTooSmall，否則輸出緩衝區的狀態和書簽的實際大小將會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="e2497-153">If this function fails, the state of the output buffer and the actual size of the bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="e2497-154">在傳回 JET_errBufferTooSmall 的事件中，輸出緩衝區將會包含所提供空間中最多的書簽，而且書簽的實際大小將會正確。</span><span class="sxs-lookup"><span data-stu-id="e2497-154">In the event that JET_errBufferTooSmall is returned, the output buffer will contain as much of the bookmark as will fit in the space provided and the actual size of the bookmark will be accurate.</span></span> <span data-ttu-id="e2497-155">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="e2497-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e2497-156">備註</span><span class="sxs-lookup"><span data-stu-id="e2497-156">Remarks</span></span>

<span data-ttu-id="e2497-157">書簽通常應該視為不透明的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="e2497-157">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="e2497-158">不應嘗試利用此資料的內部結構。</span><span class="sxs-lookup"><span data-stu-id="e2497-158">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="e2497-159">但是，下列條件適用于所有的 ESENT 書簽：</span><span class="sxs-lookup"><span data-stu-id="e2497-159">However, the following conditions are true of all ESENT bookmarks:</span></span>

  - <span data-ttu-id="e2497-160">書簽可唯一識別指定資料表中的記錄。</span><span class="sxs-lookup"><span data-stu-id="e2497-160">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="e2497-161">在記錄的存留期內，記錄的書簽不會變更。</span><span class="sxs-lookup"><span data-stu-id="e2497-161">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="e2497-162">記錄的書簽與包含該記錄之資料表的主要索引索引鍵相同。</span><span class="sxs-lookup"><span data-stu-id="e2497-162">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="e2497-163">如果未在該資料表上定義任何主要索引，database engine 將會為該記錄建立自己的書簽。</span><span class="sxs-lookup"><span data-stu-id="e2497-163">If no primary index is defined over that table the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="e2497-164">您可以使用 [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) 函式來相互比較書簽，以便在來源記錄的資料表上建立主要索引的相對順序。</span><span class="sxs-lookup"><span data-stu-id="e2497-164">Bookmarks can be compared against each other using the [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) function to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="e2497-165">如果未在該資料表上定義任何主要索引，則使用該資料表中書簽的相對順序並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="e2497-165">If no primary index is defined over that table, it is not meaningful to use the relative ordering of bookmarks from that table.</span></span>

  - <span data-ttu-id="e2497-166">比較不同資料表中的記錄書簽是無意義的。</span><span class="sxs-lookup"><span data-stu-id="e2497-166">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="e2497-167">在 Windows Vista 之前，書簽一律會小於或等於 JET_cbBookmarkMost (256) 位元組長度。</span><span class="sxs-lookup"><span data-stu-id="e2497-167">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length, prior to Windows Vista.</span></span>
    
<span data-ttu-id="e2497-168">**Windows Vista：** 在 Windows Vista 和更新版本中，書簽可能會大於 JET_cbBookmarkMost (256) 個位元組。</span><span class="sxs-lookup"><span data-stu-id="e2497-168">**Windows Vista:** On Windows Vista and later releases, bookmarks can be larger than JET_cbBookmarkMost (256) bytes.</span></span> <span data-ttu-id="e2497-169">書簽的大小上限等於 JET_paramKeyMost + 1 目前的值。</span><span class="sxs-lookup"><span data-stu-id="e2497-169">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e2497-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2497-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2497-171"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="e2497-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e2497-172">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="e2497-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2497-173"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="e2497-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e2497-174">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="e2497-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2497-175"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="e2497-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e2497-176">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="e2497-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2497-177"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="e2497-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e2497-178">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="e2497-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2497-179"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e2497-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e2497-180">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="e2497-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e2497-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2497-181">See Also</span></span>

[<span data-ttu-id="e2497-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e2497-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e2497-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e2497-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e2497-184">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e2497-184">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e2497-185">JetGoToBookmark</span><span class="sxs-lookup"><span data-stu-id="e2497-185">JetGoToBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="e2497-186">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e2497-186">JetStopService</span></span>](./jetstopservice-function.md)  
<span data-ttu-id="e2497-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="e2497-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>
