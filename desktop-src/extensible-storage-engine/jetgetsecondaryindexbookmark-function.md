---
description: 深入瞭解： JetGetSecondaryIndexBookmark 函數
title: JetGetSecondaryIndexBookmark 函式
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d86b875037982a18ebb9d488c3a05b3123002b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980890"
---
# <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="bc836-103">JetGetSecondaryIndexBookmark 函式</span><span class="sxs-lookup"><span data-stu-id="bc836-103">JetGetSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="bc836-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bc836-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="bc836-105">JetGetSecondaryIndexBookmark 函式</span><span class="sxs-lookup"><span data-stu-id="bc836-105">JetGetSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="bc836-106">**JetGetSecondaryIndexBookmark** 函式會在資料指標目前的位置，抓取次要索引項目的特殊書簽。</span><span class="sxs-lookup"><span data-stu-id="bc836-106">The **JetGetSecondaryIndexBookmark** function retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="bc836-107">然後，您可以使用這個書簽，利用 [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)將該資料指標有效率地重新放置到相同的索引項目。</span><span class="sxs-lookup"><span data-stu-id="bc836-107">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md).</span></span> <span data-ttu-id="bc836-108">當在包含重複索引鍵或包含相同記錄之多個索引項目的次要索引上重新置放時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="bc836-108">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="bc836-109">**Windows xp： JetGetSecondaryIndexBookmark** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="bc836-109">**Windows XP:  JetGetSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="bc836-110">參數</span><span class="sxs-lookup"><span data-stu-id="bc836-110">Parameters</span></span>

<span data-ttu-id="bc836-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="bc836-111">*sesid*</span></span>

<span data-ttu-id="bc836-112">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="bc836-112">The session to use for this call.</span></span>

<span data-ttu-id="bc836-113">*tableid*</span><span class="sxs-lookup"><span data-stu-id="bc836-113">*tableid*</span></span>

<span data-ttu-id="bc836-114">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="bc836-114">The cursor to use for this call.</span></span>

<span data-ttu-id="bc836-115">*pvSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="bc836-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="bc836-116">接收次要金鑰的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bc836-116">The output buffer that receives the secondary key.</span></span>

<span data-ttu-id="bc836-117">*cbSecondaryKeyMax*</span><span class="sxs-lookup"><span data-stu-id="bc836-117">*cbSecondaryKeyMax*</span></span>

<span data-ttu-id="bc836-118">次要索引鍵之輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bc836-118">The maximum size, in bytes, of the output buffer for the secondary key.</span></span>

<span data-ttu-id="bc836-119">*pcbSecondaryKeyActual*</span><span class="sxs-lookup"><span data-stu-id="bc836-119">*pcbSecondaryKeyActual*</span></span>

<span data-ttu-id="bc836-120">接收次要金鑰的實際大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bc836-120">Receives the actual size in bytes of the secondary key.</span></span>

<span data-ttu-id="bc836-121">如果這個參數是 Null，將不會傳回次要索引鍵的實際大小。</span><span class="sxs-lookup"><span data-stu-id="bc836-121">If this parameter is NULL, the actual size of the secondary key will not be returned.</span></span>

<span data-ttu-id="bc836-122">如果輸出緩衝區太小，則仍會傳回次要金鑰的實際大小。</span><span class="sxs-lookup"><span data-stu-id="bc836-122">If the output buffer is too small, the actual size of the secondary key will still be returned.</span></span> <span data-ttu-id="bc836-123">這表示這個數位會大於輸出緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="bc836-123">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="bc836-124">*pvPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="bc836-124">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="bc836-125">接收主要金鑰書簽的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bc836-125">The output buffer that receives the primary key bookmark.</span></span>

<span data-ttu-id="bc836-126">*cbPrimaryBookmarkMax*</span><span class="sxs-lookup"><span data-stu-id="bc836-126">*cbPrimaryBookmarkMax*</span></span>

<span data-ttu-id="bc836-127">主鍵書簽輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bc836-127">The maximum size, in bytes, of the output buffer for the primary key bookmark.</span></span>

<span data-ttu-id="bc836-128">*pcbPrimaryKeyActual*</span><span class="sxs-lookup"><span data-stu-id="bc836-128">*pcbPrimaryKeyActual*</span></span>

<span data-ttu-id="bc836-129">接收主要金鑰書簽的實際大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bc836-129">Receives the actual size, in bytes, of the primary key bookmark.</span></span>

<span data-ttu-id="bc836-130">如果這個參數為 Null，則不會傳回主要索引鍵書簽的實際大小。</span><span class="sxs-lookup"><span data-stu-id="bc836-130">If this parameter is NULL then the actual size of the primary key bookmark will not be returned.</span></span>

<span data-ttu-id="bc836-131">如果輸出緩衝區太小，則仍會傳回主要金鑰書簽的實際大小。</span><span class="sxs-lookup"><span data-stu-id="bc836-131">If the output buffer is too small, the actual size of the primary key bookmark will still be returned.</span></span> <span data-ttu-id="bc836-132">這表示這個數位會大於輸出緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="bc836-132">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="bc836-133">*grbit*</span><span class="sxs-lookup"><span data-stu-id="bc836-133">*grbit*</span></span>

<span data-ttu-id="bc836-134">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="bc836-134">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="bc836-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc836-135">Return Value</span></span>

<span data-ttu-id="bc836-136">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="bc836-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bc836-137">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="bc836-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc836-138">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bc836-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="bc836-139">Description</span><span class="sxs-lookup"><span data-stu-id="bc836-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc836-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bc836-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bc836-141">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="bc836-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc836-142">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="bc836-142">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="bc836-143">作業已順利完成，但其中一個輸出緩衝區太小，無法接收要求的資料。</span><span class="sxs-lookup"><span data-stu-id="bc836-143">The operation completed successfully, but one of the output buffers was too small to receive the requested data.</span></span></p>
<p><span data-ttu-id="bc836-144">輸出緩衝區已填滿適當的書簽。</span><span class="sxs-lookup"><span data-stu-id="bc836-144">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="bc836-145">如果要求，也會傳回書簽的實際大小。</span><span class="sxs-lookup"><span data-stu-id="bc836-145">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc836-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bc836-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bc836-147">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="bc836-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc836-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bc836-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bc836-149">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="bc836-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="bc836-150">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="bc836-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc836-151">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="bc836-151">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="bc836-152">資料指標目前不在次要索引上。</span><span class="sxs-lookup"><span data-stu-id="bc836-152">The cursor is not currently on a secondary index.</span></span></p>
<p><span data-ttu-id="bc836-153">當資料指標目前未使用次要索引時，抓取次要索引書簽並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="bc836-153">It is not meaningful to retrieve a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="bc836-154">當資料指標不在次要索引上時，應使用<a href="gg269221(v=exchg.10).md">JetGetBookmark</a> 。</span><span class="sxs-lookup"><span data-stu-id="bc836-154"><a href="gg269221(v=exchg.10).md">JetGetBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc836-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="bc836-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="bc836-156">資料指標未放置在記錄上。</span><span class="sxs-lookup"><span data-stu-id="bc836-156">The cursor is not positioned on a record.</span></span></p>
<p><span data-ttu-id="bc836-157">此情況具有許多不同的原因。</span><span class="sxs-lookup"><span data-stu-id="bc836-157">This can happen for many different reasons.</span></span> <span data-ttu-id="bc836-158">例如，如果資料指標目前位於目前索引的最後一筆記錄之後，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="bc836-158">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc836-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bc836-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bc836-160">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="bc836-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc836-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bc836-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bc836-162">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="bc836-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc836-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="bc836-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="bc836-164">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="bc836-164">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="bc836-165">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="bc836-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc836-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bc836-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bc836-167">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="bc836-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bc836-168">成功時，會在輸出緩衝區中傳回索引項目在資料指標目前位置的次要索引書簽。</span><span class="sxs-lookup"><span data-stu-id="bc836-168">On success, the secondary index bookmark for the index entry at the current position of a cursor will be returned in the output buffers.</span></span> <span data-ttu-id="bc836-169">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="bc836-169">No change to the database state will occur.</span></span>

<span data-ttu-id="bc836-170">失敗時，除非傳回 JET_errBufferTooSmall，否則輸出緩衝區的狀態和次要索引書簽的實際大小將會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="bc836-170">On failure, the state of the output buffers and the actual size of the secondary index bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="bc836-171">在傳回 JET_errBufferTooSmall 的事件中，輸出緩衝區會包含最多的次要索引書簽，以容納提供的空間，而次要索引書簽的實際大小將會是正確的。</span><span class="sxs-lookup"><span data-stu-id="bc836-171">In the event that JET_errBufferTooSmall is returned, the output buffers will contain as much of the secondary index bookmark as will fit in the space provided and the actual size of the secondary index bookmark will be accurate.</span></span> <span data-ttu-id="bc836-172">在任何情況下，都不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="bc836-172">In any case, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bc836-173">備註</span><span class="sxs-lookup"><span data-stu-id="bc836-173">Remarks</span></span>

<span data-ttu-id="bc836-174">書簽通常應該視為不透明的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="bc836-174">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="bc836-175">不應嘗試利用此資料的內部結構。</span><span class="sxs-lookup"><span data-stu-id="bc836-175">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="bc836-176">不過，您可以知道所有 ESENT 書簽的下列屬性：</span><span class="sxs-lookup"><span data-stu-id="bc836-176">However, the following properties can be known about all ESENT bookmarks:</span></span>

  - <span data-ttu-id="bc836-177">書簽可唯一識別指定資料表中的記錄。</span><span class="sxs-lookup"><span data-stu-id="bc836-177">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="bc836-178">在記錄的存留期內，記錄的書簽不會變更。</span><span class="sxs-lookup"><span data-stu-id="bc836-178">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="bc836-179">記錄的書簽與包含該記錄之資料表的主要索引索引鍵相同。</span><span class="sxs-lookup"><span data-stu-id="bc836-179">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="bc836-180">如果未在該資料表上定義任何主要索引，database engine 將會為該記錄建立自己的書簽。</span><span class="sxs-lookup"><span data-stu-id="bc836-180">If no primary index is defined over that table, the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="bc836-181">您可以使用 memcmp，在來源記錄的資料表中建立主要索引的相對順序，以使用[](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))來比較書簽。</span><span class="sxs-lookup"><span data-stu-id="bc836-181">Bookmarks may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="bc836-182">如果未在該資料表上定義任何主要索引，則該資料表中的書簽相對順序將沒有意義。</span><span class="sxs-lookup"><span data-stu-id="bc836-182">If no primary index is defined over that table, the relative ordering of bookmarks from that table is not meaningful.</span></span>

  - <span data-ttu-id="bc836-183">比較不同資料表中的記錄書簽是無意義的。</span><span class="sxs-lookup"><span data-stu-id="bc836-183">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="bc836-184">在 Windows Vista 之前，書簽一律小於或等於 JET_cbBookmarkMost (256) 位元組。</span><span class="sxs-lookup"><span data-stu-id="bc836-184">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="bc836-185">在 Windows Vista 和更新版本中，書簽可以更大。</span><span class="sxs-lookup"><span data-stu-id="bc836-185">On Windows Vista and later releases, bookmarks can be larger.</span></span> <span data-ttu-id="bc836-186">書簽的大小上限等於 JET_paramKeyMost + 1 目前的值。</span><span class="sxs-lookup"><span data-stu-id="bc836-186">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

<span data-ttu-id="bc836-187">金鑰通常應該視為不透明的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="bc836-187">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="bc836-188">不應嘗試利用此資料的內部結構。</span><span class="sxs-lookup"><span data-stu-id="bc836-188">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="bc836-189">不過，您可以知道所有 ESENT 機碼的下列屬性：</span><span class="sxs-lookup"><span data-stu-id="bc836-189">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="bc836-190">您可以使用 [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) 來相互比較索引鍵，以在來源索引項目目的資料表中建立原始索引的相對順序。</span><span class="sxs-lookup"><span data-stu-id="bc836-190">Keys may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="bc836-191">將索引項目的索引鍵與不同索引的索引鍵進行比較是無意義的。</span><span class="sxs-lookup"><span data-stu-id="bc836-191">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="bc836-192">在 Windows Vista 之前，索引鍵一律小於或等於 JET_cbKeyMost (255) 位元組。</span><span class="sxs-lookup"><span data-stu-id="bc836-192">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="bc836-193">在 Windows Vista 和更新版本中，金鑰可以更大。</span><span class="sxs-lookup"><span data-stu-id="bc836-193">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="bc836-194">索引鍵的大小上限等於 JET_paramKeyMost 目前的值。</span><span class="sxs-lookup"><span data-stu-id="bc836-194">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bc836-195">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc836-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc836-196"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="bc836-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bc836-197">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="bc836-197">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc836-198"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="bc836-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bc836-199">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="bc836-199">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc836-200"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="bc836-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bc836-201">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="bc836-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc836-202"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="bc836-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bc836-203">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="bc836-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc836-204"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bc836-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bc836-205">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="bc836-205">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bc836-206">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc836-206">See Also</span></span>

[<span data-ttu-id="bc836-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bc836-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bc836-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="bc836-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="bc836-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bc836-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bc836-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="bc836-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="bc836-211">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="bc836-211">JetGetBookmark</span></span>](./jetgetbookmark-function.md)  
[<span data-ttu-id="bc836-212">JetGotoSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="bc836-212">JetGotoSecondaryIndexBookmark</span></span>](./jetgotosecondaryindexbookmark-function.md)  
[<span data-ttu-id="bc836-213">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="bc836-213">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
<span data-ttu-id="bc836-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="bc836-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>
