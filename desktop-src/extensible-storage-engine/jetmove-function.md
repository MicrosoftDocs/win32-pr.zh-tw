---
description: 深入瞭解： JetMove 函數
title: JetMove 函式
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e42cb2258d373f8c4edb96309c6db0853eab4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191127"
---
# <a name="jetmove-function"></a><span data-ttu-id="95815-103">JetMove 函式</span><span class="sxs-lookup"><span data-stu-id="95815-103">JetMove Function</span></span>


<span data-ttu-id="95815-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="95815-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetmove-function"></a><span data-ttu-id="95815-105">JetMove 函式</span><span class="sxs-lookup"><span data-stu-id="95815-105">JetMove Function</span></span>

<span data-ttu-id="95815-106">**JetMove** 函式會將游標放在索引的開頭或結尾，然後將該索引中的專案向前或向後移動。</span><span class="sxs-lookup"><span data-stu-id="95815-106">The **JetMove** function positions a cursor at the start or end of an index and traverses the entries in that index either forward or backward.</span></span> <span data-ttu-id="95815-107">您也可以在目前索引上，以指定的索引項目數目向前或向後移動游標。</span><span class="sxs-lookup"><span data-stu-id="95815-107">It is also possible to move the cursor forward or backward on the current index by a specified number of index entries.</span></span> <span data-ttu-id="95815-108">另一種方法是使用 [JetSetIndexRange](./jetsetindexrange-function.md)在資料指標上設定索引範圍，藉此限制可使用 **JetMove** 列舉的索引項目。</span><span class="sxs-lookup"><span data-stu-id="95815-108">Another approach is to artificially limit the index entries that can be enumerated using **JetMove** by setting up an index range on the cursor using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="95815-109">參數</span><span class="sxs-lookup"><span data-stu-id="95815-109">Parameters</span></span>

<span data-ttu-id="95815-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="95815-110">*sesid*</span></span>

<span data-ttu-id="95815-111">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="95815-111">The session to use for this call.</span></span>

<span data-ttu-id="95815-112">*tableid*</span><span class="sxs-lookup"><span data-stu-id="95815-112">*tableid*</span></span>

<span data-ttu-id="95815-113">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="95815-113">The cursor to use for this call.</span></span>

<span data-ttu-id="95815-114">*烏鴉*</span><span class="sxs-lookup"><span data-stu-id="95815-114">*cRow*</span></span>

<span data-ttu-id="95815-115">任意位移，表示所需的資料指標在目前索引上的移動。</span><span class="sxs-lookup"><span data-stu-id="95815-115">An arbitrary offset that indicates the desired movement of the cursor on the current index.</span></span>

<span data-ttu-id="95815-116">除了標準位移之外，也可以使用下列其中一個選項來設定此參數。</span><span class="sxs-lookup"><span data-stu-id="95815-116">In addition to standard offsets, this parameter can also be set with one of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95815-117">值</span><span class="sxs-lookup"><span data-stu-id="95815-117">Value</span></span></p></th>
<th><p><span data-ttu-id="95815-118">意義</span><span class="sxs-lookup"><span data-stu-id="95815-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95815-119">JET_MoveFirst</span><span class="sxs-lookup"><span data-stu-id="95815-119">JET_MoveFirst</span></span></p></td>
<td><p><span data-ttu-id="95815-120">將游標移至索引 (中的第一個索引項目目（如果有的話) ）。</span><span class="sxs-lookup"><span data-stu-id="95815-120">Moves the cursor to the first index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="95815-121"><strong>注意</strong>   -2147483648 的常值會用來表示這個選項。</span><span class="sxs-lookup"><span data-stu-id="95815-121"><strong>Note</strong>   The literal value of -2147483648 is used to denote this option.</span></span> <span data-ttu-id="95815-122">請勿使用此值做為一般位移或可能導致非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="95815-122">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95815-123">JET_MoveLast</span><span class="sxs-lookup"><span data-stu-id="95815-123">JET_MoveLast</span></span></p></td>
<td><p><span data-ttu-id="95815-124">將游標移至索引 (中的最後一個索引項目目（如果有的話）) 。</span><span class="sxs-lookup"><span data-stu-id="95815-124">Moves the cursor to the last index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="95815-125"><strong>注意</strong>   2147483647的常值會用來表示這個選項。</span><span class="sxs-lookup"><span data-stu-id="95815-125"><strong>Note</strong>   The literal value of 2147483647 is used to denote this option.</span></span> <span data-ttu-id="95815-126">請勿使用此值做為一般位移或可能導致非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="95815-126">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95815-127">JET_MoveNext</span><span class="sxs-lookup"><span data-stu-id="95815-127">JET_MoveNext</span></span></p></td>
<td><p><span data-ttu-id="95815-128">將游標移至索引 (中的下一個索引項目（如果有的話) ）。</span><span class="sxs-lookup"><span data-stu-id="95815-128">Moves the cursor to the next index entry in the index (if one exists).</span></span> <span data-ttu-id="95815-129">此值完全等於 + 1 的一般位移。</span><span class="sxs-lookup"><span data-stu-id="95815-129">This value is exactly equal to an ordinary offset of +1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95815-130">JET_MovePrevious</span><span class="sxs-lookup"><span data-stu-id="95815-130">JET_MovePrevious</span></span></p></td>
<td><p><span data-ttu-id="95815-131">將游標移至索引 (中的前一個索引項目目（如果有的話) ）。</span><span class="sxs-lookup"><span data-stu-id="95815-131">Moves the cursor to the previous index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="95815-132">此值完全等於-1 的一般位移，或 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="95815-132">This value is exactly equal to an ordinary offset of -1, or 0 (Zero).</span></span></p>
<p><span data-ttu-id="95815-133">游標會保持在目前的邏輯位置，並且會測試對應至該邏輯位置的索引項目目是否存在。</span><span class="sxs-lookup"><span data-stu-id="95815-133">The cursor remains at the current logical position and the existence of the index entry that corresponds to that logical position will be tested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="95815-134">*grbit*</span><span class="sxs-lookup"><span data-stu-id="95815-134">*grbit*</span></span>

<span data-ttu-id="95815-135">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="95815-135">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95815-136">值</span><span class="sxs-lookup"><span data-stu-id="95815-136">Value</span></span></p></th>
<th><p><span data-ttu-id="95815-137">意義</span><span class="sxs-lookup"><span data-stu-id="95815-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95815-138">JET_bitMoveKeyNE</span><span class="sxs-lookup"><span data-stu-id="95815-138">JET_bitMoveKeyNE</span></span></p></td>
<td><p><span data-ttu-id="95815-139">向前或向後移動游標，以略過索引中所遇到的索引鍵值數目。</span><span class="sxs-lookup"><span data-stu-id="95815-139">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="95815-140">這會將具有重複索引鍵值的索引項目轉換成單一索引項目的效果。</span><span class="sxs-lookup"><span data-stu-id="95815-140">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span> <span data-ttu-id="95815-141">通常，位移會將游標移至指定的索引項目數目，而不論其索引鍵值為何。</span><span class="sxs-lookup"><span data-stu-id="95815-141">Ordinarily, an offset will move the cursor by the specified number of index entries regardless of their key values.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="95815-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="95815-142">Return Value</span></span>

<span data-ttu-id="95815-143">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="95815-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="95815-144">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="95815-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95815-145">傳回碼</span><span class="sxs-lookup"><span data-stu-id="95815-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="95815-146">Description</span><span class="sxs-lookup"><span data-stu-id="95815-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95815-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="95815-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="95815-148">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="95815-148">The operation completed successfully.</span></span> <span data-ttu-id="95815-149">若為 <strong>JetMove</strong>，這表示在要求的位置或在目前索引的位移上找到索引項目。</span><span class="sxs-lookup"><span data-stu-id="95815-149">For <strong>JetMove</strong>, this means that an index entry was found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95815-150">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="95815-150">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="95815-151">無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</span><span class="sxs-lookup"><span data-stu-id="95815-151">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95815-152">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="95815-152">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="95815-153">作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="95815-153">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="95815-154"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="95815-154"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95815-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="95815-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="95815-156">資料指標目前不在索引項目上。</span><span class="sxs-lookup"><span data-stu-id="95815-156">The cursor is not currently positioned on an index entry.</span></span> <span data-ttu-id="95815-157">若為 <strong>JetMove</strong>，這表示在要求的位置或在目前索引的位移處找不到索引項目。</span><span class="sxs-lookup"><span data-stu-id="95815-157">For <strong>JetMove</strong>, this means that an index entry was not found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95815-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="95815-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="95815-159">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="95815-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95815-160">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="95815-160">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="95815-161">資料指標目前以邏輯方式放置於對應至已刪除之記錄的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="95815-161">The cursor is currently logically positioned on an index entry that corresponds to a record that has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95815-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="95815-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="95815-163">作業無法完成，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="95815-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95815-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="95815-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="95815-165">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="95815-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="95815-166"><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</span><span class="sxs-lookup"><span data-stu-id="95815-166"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95815-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="95815-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="95815-168">無法完成作業，因為與會話相關聯的實例正在關閉中。</span><span class="sxs-lookup"><span data-stu-id="95815-168">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="95815-169">如果此函式成功，游標將定位於符合所要求位置或位移的索引項目。</span><span class="sxs-lookup"><span data-stu-id="95815-169">If this function succeeds, the cursor will be positioned at an index entry that matches the requested location or offset.</span></span> <span data-ttu-id="95815-170">如果已備妥記錄以進行更新，就會取消該更新。</span><span class="sxs-lookup"><span data-stu-id="95815-170">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="95815-171">如果索引範圍有效，且已指定 JET_MoveFirst 或 JET_MoveLast，將會取消該索引範圍。</span><span class="sxs-lookup"><span data-stu-id="95815-171">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="95815-172">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="95815-172">No change to the database state will occur.</span></span>

<span data-ttu-id="95815-173">如果此函式失敗，除非傳回 JET_errNoCurrentRecord，否則資料指標的位置會保持不變。</span><span class="sxs-lookup"><span data-stu-id="95815-173">If this function fails, the position of the cursor will remain unchanged unless JET_errNoCurrentRecord was returned.</span></span> <span data-ttu-id="95815-174">在此情況下，游標將放置於符合所要求位置或位移的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="95815-174">In that case, the cursor will be positioned where the index entry that matches the requested location or offset would have been.</span></span> <span data-ttu-id="95815-175">資料指標可以相對於該位置移動，但仍不在有效的索引項目上。</span><span class="sxs-lookup"><span data-stu-id="95815-175">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="95815-176">如果已備妥記錄以進行更新，就會取消該更新。</span><span class="sxs-lookup"><span data-stu-id="95815-176">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="95815-177">如果索引範圍有效，且已指定 JET_MoveFirst 或 JET_MoveLast，將會取消該索引範圍。</span><span class="sxs-lookup"><span data-stu-id="95815-177">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="95815-178">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="95815-178">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="95815-179">備註</span><span class="sxs-lookup"><span data-stu-id="95815-179">Remarks</span></span>

<span data-ttu-id="95815-180">您可以使用 **JetMove**，在第一個和最後一個之後，將資料指標移至兩個特殊位置。</span><span class="sxs-lookup"><span data-stu-id="95815-180">A cursor can be moved to two special positions using **JetMove**, Before First and After Last.</span></span> <span data-ttu-id="95815-181">如果資料指標是在資料表中的第一個索引項目目上，而 **JetMove** 是以 JET_MovePrevious 呼叫，則呼叫會失敗併發生 JET_errNoCurrentRecord，而且資料指標會在邏輯上定位於索引中的第一個專案之前。</span><span class="sxs-lookup"><span data-stu-id="95815-181">If the cursor is on the first index entry in the table and **JetMove** is called with JET_MovePrevious, the call will fail with JET_errNoCurrentRecord and the cursor will be logically positioned before the first entry in the index.</span></span> <span data-ttu-id="95815-182">即使在索引中的第一個專案之前插入另一個索引項目，仍會維護此邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="95815-182">This logical position is maintained even if another index entry is inserted prior to the first entry in the index.</span></span> <span data-ttu-id="95815-183">在最後一次相對於索引結尾之後，就會發生類似的情況。</span><span class="sxs-lookup"><span data-stu-id="95815-183">An analogous situation occurs for After Last relative to the end of the index.</span></span> <span data-ttu-id="95815-184">當您設定要使用 **JetMove** 逐一查看的索引項目範圍時，在第一個和最後一個之前，最有用的是使用反覆運算器模型，該模型預期會在使用該專案之前，一律移至下一個 (或先前的) 元素。</span><span class="sxs-lookup"><span data-stu-id="95815-184">Before First and After Last are most useful when setting up a range of index entries to be iterated using **JetMove**, using an iterator model that expects to always move to the next (or previous) element prior to using that element.</span></span>

<span data-ttu-id="95815-185">可以透過在資料指標上設定索引範圍來限制 **JetMove** 可造訪的索引項目集合。</span><span class="sxs-lookup"><span data-stu-id="95815-185">The set of index entries that can be visited by **JetMove** can be limited by setting up an index range on the cursor.</span></span> <span data-ttu-id="95815-186">這對列舉一組索引項目的應用程式很有用，這些專案符合可透過針對該索引所建立的一對搜尋索引鍵來表示的簡單準則。</span><span class="sxs-lookup"><span data-stu-id="95815-186">This is useful for applications that enumerate a set of index entries that match simple criteria that can be expressed through a pair of search keys built for that index.</span></span> <span data-ttu-id="95815-187">如需詳細資訊，請參閱 [JetSetIndexRange](./jetsetindexrange-function.md)。</span><span class="sxs-lookup"><span data-stu-id="95815-187">For more information, see [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="95815-188">在 Windows Server 2003 SP1 之前的版本中，在某些特定情況下的 **JetMove** 發生問題，這會影響 [JetSetIndexRange](./jetsetindexrange-function.md) 函數所設定之索引範圍的正確強制執行。</span><span class="sxs-lookup"><span data-stu-id="95815-188">On releases prior to Windows Server 2003 SP1, there is a problem in **JetMove** that occurs in some specific cases, that affects the correct enforcement of an index range as set up by the [JetSetIndexRange](./jetsetindexrange-function.md) function.</span></span> <span data-ttu-id="95815-189">如果資料指標目前是在第一個索引項目之前，而且索引範圍設定的上限小於第一個索引項目，則下一次呼叫 **JetMove** 時，將會錯誤地移至該索引項目目，而不會如預期般與 JET_errNoCurrentRecord 失敗。</span><span class="sxs-lookup"><span data-stu-id="95815-189">If the cursor is currently before the first index entry and an index range is set with an upper limit that is less than the first index entry, the next call to **JetMove** will erroneously go to that index entry instead of failing with JET_errNoCurrentRecord, as expected.</span></span> <span data-ttu-id="95815-190">從索引結尾開始，類似的情況會發生相同的錯誤。</span><span class="sxs-lookup"><span data-stu-id="95815-190">The same error will happen for the analogous situation starting from the end of the index.</span></span> <span data-ttu-id="95815-191">這種情況可能會發生在設定索引範圍的應用程式中，並使用預期會在第一個索引項目目（其為要列舉之專案集的成員）之前啟動的反覆運算器導覽，而不是從該集合的第一個索引項目目開始。</span><span class="sxs-lookup"><span data-stu-id="95815-191">This situation can occur in an application that sets up an index range and navigates it using an iterator that expects to start before the first index entry that is a member of the set of entries to enumerate, rather than starting on the first index entry of that set.</span></span> <span data-ttu-id="95815-192">這種情況也會發生在類似的情況下，從索引的結尾開始。</span><span class="sxs-lookup"><span data-stu-id="95815-192">This situation also occurs on the analogous case starting from the end of the index.</span></span> <span data-ttu-id="95815-193">因應措施是讓應用程式以手動方式確認取得的索引項目位於索引範圍內，方法是使用 JetRetrieveKey) 來比較目前索引 (項的索引鍵，以使用[](./jetretrievekey-function.md) ，其索引鍵代表目前索引範圍的結尾 (使用 JET_bitRetrieveCopy) 來[JetRetrieveKey](./jetretrievekey-function.md)抓取。</span><span class="sxs-lookup"><span data-stu-id="95815-193">The workaround is for the application to manually verify that the index entry acquired is inside the index range by comparing the key for the current index entry (retrieved using [JetRetrieveKey](./jetretrievekey-function.md)) with the key representing the end of the current index range (retrieved using [JetRetrieveKey](./jetretrievekey-function.md) using JET_bitRetrieveCopy).</span></span>

<span data-ttu-id="95815-194">將計算位移傳遞給 **JetMove** 時，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="95815-194">It is important to be careful when passing computed offsets to **JetMove**.</span></span> <span data-ttu-id="95815-195">如果計算的位移小於或等於 JET_MoveFirst，則該位移必須分割成多個片段，每個片段會分別傳遞至 **JetMove** ，但在單一交易內，以取得所需的效果。</span><span class="sxs-lookup"><span data-stu-id="95815-195">If the computed offset is less than or equal to JET_MoveFirst, that offset must be broken up into multiple pieces, each of which is passed to **JetMove** separately but within a single transaction to get the desired effect.</span></span> <span data-ttu-id="95815-196">大於或等於 JET_MoveNext 的位移也是如此。</span><span class="sxs-lookup"><span data-stu-id="95815-196">The same is true for offsets greater than or equal to JET_MoveNext.</span></span> <span data-ttu-id="95815-197">應用程式不太可能在現實世界中進行這項工作，但在這種情況下，最好是根據 JET_MoveFirst 的不同語義和 JET_MoveLast 的一般位移來進行防禦。</span><span class="sxs-lookup"><span data-stu-id="95815-197">It is unlikely that an application would undergo this in the real world, but it is good to have a defense against this case given the very different semantics of JET_MoveFirst and JET_MoveLast from an ordinary offset.</span></span>

<span data-ttu-id="95815-198">使用非常大的位移呼叫 **JetMove** 時（例如，當魚尾紋參數設定為1000時）， **JetMove** 會將所有1000索引項目移至最後一個位置。</span><span class="sxs-lookup"><span data-stu-id="95815-198">When **JetMove** is called with a very large offset, such as when the cRow parameter is set to 1000, **JetMove** traverses all 1000 index entries to reach the final position.</span></span> <span data-ttu-id="95815-199">目前，ESE API 不會提供有效的方式，透過位移直接移至指定的索引項目，而不會跨越每個索引項目目。</span><span class="sxs-lookup"><span data-stu-id="95815-199">Currently, the ESE API does not provide an efficient way to move directly to a given index entry by offset without traversing each index entry.</span></span>

#### <a name="requirements"></a><span data-ttu-id="95815-200">規格需求</span><span class="sxs-lookup"><span data-stu-id="95815-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95815-201"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="95815-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="95815-202">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="95815-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95815-203"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="95815-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="95815-204">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="95815-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95815-205"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="95815-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="95815-206">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="95815-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95815-207"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="95815-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="95815-208">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="95815-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95815-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="95815-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="95815-210">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="95815-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="95815-211">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95815-211">See Also</span></span>

[<span data-ttu-id="95815-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="95815-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="95815-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="95815-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="95815-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="95815-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="95815-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="95815-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="95815-216">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="95815-216">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="95815-217">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="95815-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
