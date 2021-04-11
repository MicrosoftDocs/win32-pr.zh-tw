---
description: 深入瞭解： JetSetIndexRange 函數
title: JetSetIndexRange 函式
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883085633bebf25180c82f0f8917f6fa31fe7304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191499"
---
# <a name="jetsetindexrange-function"></a><span data-ttu-id="3a578-103">JetSetIndexRange 函式</span><span class="sxs-lookup"><span data-stu-id="3a578-103">JetSetIndexRange Function</span></span>


<span data-ttu-id="3a578-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3a578-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetindexrange-function"></a><span data-ttu-id="3a578-105">JetSetIndexRange 函式</span><span class="sxs-lookup"><span data-stu-id="3a578-105">JetSetIndexRange Function</span></span>

<span data-ttu-id="3a578-106">**JetSetIndexRange** 函式會暫時限制索引項目的索引項目目集合，而資料指標可使用 [JetMove](./jetmove-function.md) ，從目前的索引項目目開始，然後結束于符合該資料指標中搜尋索引鍵所指定的搜尋條件，以及指定的系結準則中的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="3a578-106">The **JetSetIndexRange** function temporarily limits the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="3a578-107">搜尋金鑰必須先前已使用 [JetMakeKey](./jetmakekey-function.md)來建立。</span><span class="sxs-lookup"><span data-stu-id="3a578-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="3a578-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a578-108">Parameters</span></span>

<span data-ttu-id="3a578-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="3a578-109">*sesid*</span></span>

<span data-ttu-id="3a578-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="3a578-110">The session to use for this call.</span></span>

<span data-ttu-id="3a578-111">*tableidSrc*</span><span class="sxs-lookup"><span data-stu-id="3a578-111">*tableidSrc*</span></span>

<span data-ttu-id="3a578-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="3a578-112">The cursor to use for this call.</span></span>

<span data-ttu-id="3a578-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="3a578-113">*grbit*</span></span>

<span data-ttu-id="3a578-114">位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列各項：</span><span class="sxs-lookup"><span data-stu-id="3a578-114">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a578-115">值</span><span class="sxs-lookup"><span data-stu-id="3a578-115">Value</span></span></p></th>
<th><p><span data-ttu-id="3a578-116">意義</span><span class="sxs-lookup"><span data-stu-id="3a578-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a578-117">JET_bitRangeInclusive</span><span class="sxs-lookup"><span data-stu-id="3a578-117">JET_bitRangeInclusive</span></span></p></td>
<td><p><span data-ttu-id="3a578-118">此選項的存在或不存在，表示索引範圍的界限準則。</span><span class="sxs-lookup"><span data-stu-id="3a578-118">This presence or absence of this option indicates the boundary criteria of the index range.</span></span> <span data-ttu-id="3a578-119">如果有的話，這個選項會指出索引範圍的限制是內含的。</span><span class="sxs-lookup"><span data-stu-id="3a578-119">When present, this option indicates that the limit of the index range is inclusive.</span></span> <span data-ttu-id="3a578-120">如果不存在，此選項表示索引範圍的限制為獨佔。</span><span class="sxs-lookup"><span data-stu-id="3a578-120">When absent, this option indicates that the limit of the index range is exclusive.</span></span> <span data-ttu-id="3a578-121">當索引範圍的限制為包含時，與搜尋準則完全相符的任何索引項目都會包含在範圍內。</span><span class="sxs-lookup"><span data-stu-id="3a578-121">When the limit of the index range is inclusive then any index entries exactly matching the search criteria are included in the range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a578-122">JET_bitRangeInstantDuration</span><span class="sxs-lookup"><span data-stu-id="3a578-122">JET_bitRangeInstantDuration</span></span></p></td>
<td><p><span data-ttu-id="3a578-123">此選項會要求在建立索引範圍時立即予以移除。</span><span class="sxs-lookup"><span data-stu-id="3a578-123">This option requests that the index range be removed as soon as it has been established.</span></span> <span data-ttu-id="3a578-124">作業的所有其他層面都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="3a578-124">All other aspects of the operation remain unchanged.</span></span> <span data-ttu-id="3a578-125">這適合用來測試符合搜尋準則的索引項目是否存在。</span><span class="sxs-lookup"><span data-stu-id="3a578-125">This is useful for testing for the existence of index entries that match the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a578-126">JET_bitRangeRemove</span><span class="sxs-lookup"><span data-stu-id="3a578-126">JET_bitRangeRemove</span></span></p></td>
<td><p><span data-ttu-id="3a578-127">此選項會要求取消資料指標上的現有索引範圍。</span><span class="sxs-lookup"><span data-stu-id="3a578-127">This option requests that an existing index range on the cursor be canceled.</span></span> <span data-ttu-id="3a578-128">一旦取消索引範圍後，就可以使用 <a href="gg294117(v=exchg.10).md">JetMove</a>移至索引範圍結尾以外的範圍。</span><span class="sxs-lookup"><span data-stu-id="3a578-128">Once the index range is canceled, it will be possible to move beyond the end of the index range using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span> <span data-ttu-id="3a578-129">如果索引範圍尚未生效， <strong>JetSetIndexRange</strong> 將會失敗，並 JET_errInvalidOperation。</span><span class="sxs-lookup"><span data-stu-id="3a578-129">If an index range is not already in effect, then <strong>JetSetIndexRange</strong> will fail with JET_errInvalidOperation.</span></span></p>
<p><span data-ttu-id="3a578-130">指定此選項時，會忽略所有其他選項。</span><span class="sxs-lookup"><span data-stu-id="3a578-130">When this option is specified, all other options are ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a578-131">JET_bitRangeUpperLimit</span><span class="sxs-lookup"><span data-stu-id="3a578-131">JET_bitRangeUpperLimit</span></span></p></td>
<td><p><span data-ttu-id="3a578-132">如果使用此選項，則資料指標中的搜尋索引鍵代表索引項目的搜尋準則，最接近索引的結尾會符合索引範圍。</span><span class="sxs-lookup"><span data-stu-id="3a578-132">If this option is used, then the search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span> <span data-ttu-id="3a578-133">索引範圍將會建立在目前的資料指標位置與此索引項目之間，以便找到所有相符專案，方法是使用 <a href="gg294117(v=exchg.10).md">JetMove</a> 搭配 JET_MoveNext 或正位移向前移動索引。</span><span class="sxs-lookup"><span data-stu-id="3a578-133">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking forward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MoveNext or a positive offset.</span></span></p>
<p><span data-ttu-id="3a578-134">搭配使用 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵，並不適合用來尋找最接近索引開頭的索引項目的萬用字元選項，這是使用此選項的意義。</span><span class="sxs-lookup"><span data-stu-id="3a578-134">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p>
<p><span data-ttu-id="3a578-135">如果省略這個選項，則資料指標中的搜尋索引鍵代表索引項目的搜尋準則，最接近索引的開頭會符合索引範圍。</span><span class="sxs-lookup"><span data-stu-id="3a578-135">If this option is omitted, then the search key in the cursor represents the search criteria for the index entry closest to the start of the index that will match the index range.</span></span> <span data-ttu-id="3a578-136">索引範圍將會建立在目前的資料指標位置與此索引項目之間，以便找到所有相符專案，方法是使用 <a href="gg294117(v=exchg.10).md">JetMove</a> 搭配 JET_MovePrevious 或負位移，在索引上向前移動。</span><span class="sxs-lookup"><span data-stu-id="3a578-136">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking backward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MovePrevious or a negative offset.</span></span></p>
<p><span data-ttu-id="3a578-137">使用透過 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵，並使用萬用字元選項來尋找最接近索引結尾的索引項目，以省略此選項的意義。</span><span class="sxs-lookup"><span data-stu-id="3a578-137">It is not meaningful to omit this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="3a578-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a578-138">Return Value</span></span>

<span data-ttu-id="3a578-139">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="3a578-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3a578-140">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="3a578-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a578-141">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3a578-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="3a578-142">Description</span><span class="sxs-lookup"><span data-stu-id="3a578-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a578-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3a578-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3a578-144">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="3a578-144">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="3a578-145">若為 <strong>JetSetIndexRange</strong>，這表示現有的索引範圍已取消，或索引範圍內至少有一個索引項目目。</span><span class="sxs-lookup"><span data-stu-id="3a578-145">For <strong>JetSetIndexRange</strong>, this means that either an existing index range was canceled or that there is at least one index entry inside of the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a578-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="3a578-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="3a578-147">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="3a578-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a578-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="3a578-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="3a578-149">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="3a578-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="3a578-150">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a578-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a578-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="3a578-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="3a578-152">當指定 JET_bitRangeRemove 且沒有任何索引範圍生效時， <strong>JetSetIndexRange</strong> 會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a578-152">This error will be returned by <strong>JetSetIndexRange</strong> when JET_bitRangeRemove was specified and no index range was in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a578-153">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="3a578-153">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="3a578-154">沒有目前的資料指標搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3a578-154">There is no current search key for the cursor.</span></span> <span data-ttu-id="3a578-155"><strong>JetSetIndexRange</strong> 要求資料指標必須有有效的搜尋索引鍵，因為它會針對用來尋找索引項目的搜尋條件使用該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3a578-155"><strong>JetSetIndexRange</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a578-156">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="3a578-156">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="3a578-157">沒有目前的資料指標索引。</span><span class="sxs-lookup"><span data-stu-id="3a578-157">There is no current index for the cursor.</span></span> <span data-ttu-id="3a578-158">如果資料指標位於資料表的叢集索引，但尚未定義主要索引，就會發生這種<strong>情況。</strong></span><span class="sxs-lookup"><span data-stu-id="3a578-158">This will happen for <strong>JetSetIndexRange</strong> if the cursor is on the clustered index of a table, a primary index has not been defined.</span></span> <span data-ttu-id="3a578-159">不支援設定這類索引的索引範圍。</span><span class="sxs-lookup"><span data-stu-id="3a578-159">Setting an index range over such an index is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a578-160">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="3a578-160">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="3a578-161"><strong>JetSetIndexRange</strong>會傳回此錯誤，表示索引範圍內沒有任何索引項目。</span><span class="sxs-lookup"><span data-stu-id="3a578-161">This error will be returned by <strong>JetSetIndexRange</strong> to indicate that there are no index entries inside the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a578-162">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3a578-162">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3a578-163">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="3a578-163">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a578-164">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3a578-164">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3a578-165">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="3a578-165">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a578-166">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="3a578-166">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="3a578-167">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="3a578-167">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="3a578-168">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a578-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a578-169">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3a578-169">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3a578-170">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="3a578-170">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3a578-171">成功時，如果指定 JET_bitRangeRemove，則會取消目前作用中的索引範圍。</span><span class="sxs-lookup"><span data-stu-id="3a578-171">On success, if JET_bitRangeRemove is specified, then the index range that is currently in effect is canceled.</span></span> <span data-ttu-id="3a578-172">如果未指定 JET_bitRangeRemove，且指定了 JET_bitRangeInstantDuration，則沒有任何索引範圍生效。</span><span class="sxs-lookup"><span data-stu-id="3a578-172">If JET_bitRangeRemove is not specified and JET_bitRangeInstantDuration is specified, then no index range is in effect.</span></span> <span data-ttu-id="3a578-173">如果未指定 JET_bitRangeRemove 或 JET_bitRangeInstantDuration，則新的索引範圍會生效。</span><span class="sxs-lookup"><span data-stu-id="3a578-173">If neither JET_bitRangeRemove nor JET_bitRangeInstantDuration is specified, then a new index range is in effect.</span></span> <span data-ttu-id="3a578-174">此索引範圍會暫時限制索引項目的索引項目集合，資料指標可以使用 [JetMove](./jetmove-function.md) 從目前的索引項目目開始，然後結束于符合搜尋準則的索引項目。</span><span class="sxs-lookup"><span data-stu-id="3a578-174">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="3a578-175">資料指標的位置會保持不變。</span><span class="sxs-lookup"><span data-stu-id="3a578-175">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="3a578-176">如果已針對資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3a578-176">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="3a578-177">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="3a578-177">No change to the database state will occur.</span></span>

<span data-ttu-id="3a578-178">失敗時，如果未傳回 JET_errNoCurrentRecord，則沒有任何索引範圍生效。</span><span class="sxs-lookup"><span data-stu-id="3a578-178">On failure, if JET_errNoCurrentRecord is not returned, then no index range is in effect.</span></span> <span data-ttu-id="3a578-179">如果傳回 JET_errNoCurrentRecord，則新的索引範圍會生效。</span><span class="sxs-lookup"><span data-stu-id="3a578-179">If JET_errNoCurrentRecord is returned, then a new index range is in effect.</span></span> <span data-ttu-id="3a578-180">此索引範圍會暫時限制索引項目的索引項目集合，資料指標可以使用 [JetMove](./jetmove-function.md) 從目前的索引項目目開始，然後結束于符合搜尋準則的索引項目。</span><span class="sxs-lookup"><span data-stu-id="3a578-180">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="3a578-181">資料指標的位置會保持不變。</span><span class="sxs-lookup"><span data-stu-id="3a578-181">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="3a578-182">如果傳回 JET_errNoCurrentRecord，且已針對資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3a578-182">If JET_errNoCurrentRecord was returned and a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="3a578-183">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="3a578-183">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3a578-184">備註</span><span class="sxs-lookup"><span data-stu-id="3a578-184">Remarks</span></span>

<span data-ttu-id="3a578-185">索引範圍是暫時性的，而且如果在資料指標上執行 [JetMove](./jetmove-function.md) 以外的任何導覽，則會自動取消。</span><span class="sxs-lookup"><span data-stu-id="3a578-185">An index range is volatile and will automatically be canceled if any navigation other than [JetMove](./jetmove-function.md) is performed on the cursor.</span></span>

<span data-ttu-id="3a578-186">索引範圍只能以一個方向運作。</span><span class="sxs-lookup"><span data-stu-id="3a578-186">Index ranges only work in one direction.</span></span> <span data-ttu-id="3a578-187">如果已建立上限，則在到達索引範圍的結尾時，只會使用 [JetMove](./jetmove-function.md) 搭配 JET_MoveNext 或正數位移來轉送動作。</span><span class="sxs-lookup"><span data-stu-id="3a578-187">If an upper limit is established then only forward motion using [JetMove](./jetmove-function.md) with JET_MoveNext or a positive offset will be prevented once the end of the index range has been reached.</span></span> <span data-ttu-id="3a578-188">在此情況下，您仍然可以使用 [JetMove](./jetmove-function.md) 搭配 JET_MovePrevious 或負位移來保留索引範圍。</span><span class="sxs-lookup"><span data-stu-id="3a578-188">It is still possible to leave the index range in this case using [JetMove](./jetmove-function.md) with JET_MovePrevious or a negative offset.</span></span> <span data-ttu-id="3a578-189">較低的限制會發生類似的情況。</span><span class="sxs-lookup"><span data-stu-id="3a578-189">An analogous situation occurs for a lower limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="3a578-190">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a578-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a578-191"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="3a578-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3a578-192">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="3a578-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a578-193"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="3a578-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3a578-194">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="3a578-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a578-195"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="3a578-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3a578-196">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="3a578-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a578-197"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="3a578-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3a578-198">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="3a578-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a578-199"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3a578-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3a578-200">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="3a578-200">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3a578-201">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a578-201">See Also</span></span>

[<span data-ttu-id="3a578-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3a578-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3a578-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3a578-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3a578-204">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3a578-204">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="3a578-205">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="3a578-205">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="3a578-206">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="3a578-206">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="3a578-207">JetMove</span><span class="sxs-lookup"><span data-stu-id="3a578-207">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="3a578-208">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="3a578-208">JetSetIndexRange</span></span>]()  
[<span data-ttu-id="3a578-209">JetStopService</span><span class="sxs-lookup"><span data-stu-id="3a578-209">JetStopService</span></span>](./jetstopservice-function.md)
