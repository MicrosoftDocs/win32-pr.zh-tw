---
description: 深入瞭解： JetGetCurrentIndex 函數
title: JetGetCurrentIndex 函式
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3337ddaefbea803a137ad8366d2e3df665bacd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001400"
---
# <a name="jetgetcurrentindex-function"></a><span data-ttu-id="192a8-103">JetGetCurrentIndex 函式</span><span class="sxs-lookup"><span data-stu-id="192a8-103">JetGetCurrentIndex Function</span></span>


<span data-ttu-id="192a8-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="192a8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcurrentindex-function"></a><span data-ttu-id="192a8-105">JetGetCurrentIndex 函式</span><span class="sxs-lookup"><span data-stu-id="192a8-105">JetGetCurrentIndex Function</span></span>

<span data-ttu-id="192a8-106">**JetGetCurrentIndex** 函式會判斷指定之資料指標目前索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="192a8-106">The **JetGetCurrentIndex** function determines the name of the current index of a given cursor.</span></span> <span data-ttu-id="192a8-107">此名稱也用來在稍後使用 [JetSetCurrentIndex](./jetsetcurrentindex-function.md)重新選取該索引做為目前的索引。</span><span class="sxs-lookup"><span data-stu-id="192a8-107">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="192a8-108">它也可以用來使用 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)探索該索引的屬性。</span><span class="sxs-lookup"><span data-stu-id="192a8-108">It can also be used to discover the properties of that index using [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="192a8-109">參數</span><span class="sxs-lookup"><span data-stu-id="192a8-109">Parameters</span></span>

<span data-ttu-id="192a8-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="192a8-110">*sesid*</span></span>

<span data-ttu-id="192a8-111">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="192a8-111">The session to use for this call.</span></span>

<span data-ttu-id="192a8-112">*tableid*</span><span class="sxs-lookup"><span data-stu-id="192a8-112">*tableid*</span></span>

<span data-ttu-id="192a8-113">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="192a8-113">The cursor to use for this call.</span></span>

<span data-ttu-id="192a8-114">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="192a8-114">*szIndexName*</span></span>

<span data-ttu-id="192a8-115">輸出緩衝區，可接收資料指標目前索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="192a8-115">The output buffer that receives the name of the current index of the cursor.</span></span>

<span data-ttu-id="192a8-116">*cchIndexName*</span><span class="sxs-lookup"><span data-stu-id="192a8-116">*cchIndexName*</span></span>

<span data-ttu-id="192a8-117">輸出緩衝區的大小上限（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="192a8-117">The maximum size in characters of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="192a8-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="192a8-118">Return Value</span></span>

<span data-ttu-id="192a8-119">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="192a8-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="192a8-120">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="192a8-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="192a8-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="192a8-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="192a8-122">Description</span><span class="sxs-lookup"><span data-stu-id="192a8-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="192a8-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="192a8-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="192a8-124">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="192a8-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="192a8-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="192a8-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="192a8-126">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="192a8-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="192a8-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="192a8-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="192a8-128">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="192a8-128">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="192a8-129">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="192a8-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="192a8-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="192a8-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="192a8-131">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="192a8-131">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="192a8-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="192a8-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="192a8-133">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="192a8-133">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="192a8-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="192a8-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="192a8-135">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="192a8-135">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="192a8-136">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="192a8-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="192a8-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="192a8-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="192a8-138">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="192a8-138">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="192a8-139">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="192a8-139">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="192a8-140">作業已順利完成，但輸出緩衝區太小，無法接收整個索引名稱。</span><span class="sxs-lookup"><span data-stu-id="192a8-140">The operation completed successfully, but the output buffer was too small to receive the entire index name.</span></span></p>
<p><span data-ttu-id="192a8-141">輸出緩衝區已填滿適當的索引名稱。</span><span class="sxs-lookup"><span data-stu-id="192a8-141">The output buffer has been filled with as much of the index name as would fit.</span></span> <span data-ttu-id="192a8-142">如果輸出緩衝區的長度至少要有一個字元，則該輸出緩衝區中的字串會以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="192a8-142">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="192a8-143"><strong>注意  </strong>如果 cchIndexName 為零，則不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="192a8-143"><strong>Note  </strong>This error will not be returned if cchIndexName is zero.</span></span> <span data-ttu-id="192a8-144">如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="192a8-144">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="192a8-145">成功時，會在輸出緩衝區中傳回指定資料指標目前索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="192a8-145">On success, the name of the current index of the given cursor will be returned in the output buffer.</span></span> <span data-ttu-id="192a8-146">如果傳回 JET_wrnBufferTruncated，輸出緩衝區將會包含所提供空間中的最多索引名稱。</span><span class="sxs-lookup"><span data-stu-id="192a8-146">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the index name as will fit in the space provided.</span></span> <span data-ttu-id="192a8-147">如果輸出緩衝區的長度至少要有一個字元，則在該緩衝區中傳回的字串將會以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="192a8-147">If the output buffer is at least one character in length then the string returned in that buffer will be null terminated.</span></span> <span data-ttu-id="192a8-148">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="192a8-148">No change to the database state will occur.</span></span>

<span data-ttu-id="192a8-149">失敗時，輸出緩衝區的狀態將會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="192a8-149">On failure, the state of the output buffer will be undefined.</span></span> <span data-ttu-id="192a8-150">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="192a8-150">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="192a8-151">備註</span><span class="sxs-lookup"><span data-stu-id="192a8-151">Remarks</span></span>

<span data-ttu-id="192a8-152">如果沒有目前的資料指標索引，則會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="192a8-152">If there is no current index for the cursor then an empty string will be returned.</span></span> <span data-ttu-id="192a8-153">當資料指標位於資料表的叢集索引，但未定義任何主要索引時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="192a8-153">This can happen when the cursor is on the clustered index of the table and no primary index was defined.</span></span> <span data-ttu-id="192a8-154">此索引稱為資料表的連續索引，且沒有任何定義。</span><span class="sxs-lookup"><span data-stu-id="192a8-154">This index is known as the sequential index of the table and has no definition.</span></span> <span data-ttu-id="192a8-155">在任何情況下，使用 [JetSetCurrentIndex](./jetsetcurrentindex-function.md) 將目前的索引設定為空字串，將會選取叢集索引，不論主要索引定義是否存在。</span><span class="sxs-lookup"><span data-stu-id="192a8-155">In any case, setting the current index to an empty string using [JetSetCurrentIndex](./jetsetcurrentindex-function.md) will select the clustered index regardless of the presence of a primary index definition.</span></span>

<span data-ttu-id="192a8-156">在此函式中，有一個重要的 bug 存在於所有版本中。</span><span class="sxs-lookup"><span data-stu-id="192a8-156">There is an important bug in this function that is present in all releases.</span></span> <span data-ttu-id="192a8-157">如果輸出緩衝區太小而無法接收整個索引名稱，而且輸出緩衝區的長度至少有一個字元，則不會傳回 JET_wrnBufferTruncated。</span><span class="sxs-lookup"><span data-stu-id="192a8-157">If the output buffer is too small to receive the entire index name and the output buffer is at least one character in length then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="192a8-158">將會改為傳回 JET_errSuccess。</span><span class="sxs-lookup"><span data-stu-id="192a8-158">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="192a8-159">若要避免這個問題，輸出緩衝區的長度應該一律至少 JET_cbNameMost + 1 (65) 個字元。</span><span class="sxs-lookup"><span data-stu-id="192a8-159">To avoid this issue, the output buffer should always be at least JET_cbNameMost + 1 (65) characters in length.</span></span>

#### <a name="requirements"></a><span data-ttu-id="192a8-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="192a8-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="192a8-161"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="192a8-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="192a8-162">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="192a8-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="192a8-163"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="192a8-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="192a8-164">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="192a8-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="192a8-165"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="192a8-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="192a8-166">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="192a8-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="192a8-167"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="192a8-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="192a8-168">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="192a8-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="192a8-169"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="192a8-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="192a8-170">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="192a8-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="192a8-171"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="192a8-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="192a8-172">實作為 <strong>JetGetCurrentIndexW</strong> (Unicode) 和 <strong>JetGetCurrentIndexA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="192a8-172">Implemented as <strong>JetGetCurrentIndexW</strong> (Unicode) and <strong>JetGetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="192a8-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="192a8-173">See Also</span></span>

[<span data-ttu-id="192a8-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="192a8-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="192a8-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="192a8-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="192a8-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="192a8-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="192a8-177">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="192a8-177">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="192a8-178">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="192a8-178">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
