---
description: 深入瞭解： JetRetrieveKey 函數
title: JetRetrieveKey 函式
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e560d28447b7e5d3798949f47dcadf259e49d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027431"
---
# <a name="jetretrievekey-function"></a><span data-ttu-id="f2c5c-103">JetRetrieveKey 函式</span><span class="sxs-lookup"><span data-stu-id="f2c5c-103">JetRetrieveKey Function</span></span>


<span data-ttu-id="f2c5c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f2c5c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievekey-function"></a><span data-ttu-id="f2c5c-105">JetRetrieveKey 函式</span><span class="sxs-lookup"><span data-stu-id="f2c5c-105">JetRetrieveKey Function</span></span>

<span data-ttu-id="f2c5c-106">**JetRetrieveKey** 函式會在資料指標的目前位置，抓取索引項目的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-106">The **JetRetrieveKey** function retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="f2c5c-107">這類金鑰是由呼叫 [JetMakeKey](./jetmakekey-function.md)所構成。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-107">Such keys are constructed by calls to [JetMakeKey](./jetmakekey-function.md).</span></span> <span data-ttu-id="f2c5c-108">然後，您可以使用抓取的金鑰，藉由呼叫 [JetSeek](./jetseek-function.md)，有效率地將該資料指標傳回相同的索引項目。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-108">The retrieved key can then be used to efficiently return that cursor to the same index entry by a call to [JetSeek](./jetseek-function.md).</span></span>

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f2c5c-109">參數</span><span class="sxs-lookup"><span data-stu-id="f2c5c-109">Parameters</span></span>

<span data-ttu-id="f2c5c-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f2c5c-110">*sesid*</span></span>

<span data-ttu-id="f2c5c-111">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-111">The session to use for this call.</span></span>

<span data-ttu-id="f2c5c-112">*tableid*</span><span class="sxs-lookup"><span data-stu-id="f2c5c-112">*tableid*</span></span>

<span data-ttu-id="f2c5c-113">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-113">The cursor to use for this call.</span></span>

<span data-ttu-id="f2c5c-114">*pvData*</span><span class="sxs-lookup"><span data-stu-id="f2c5c-114">*pvData*</span></span>

<span data-ttu-id="f2c5c-115">將接收金鑰的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-115">The output buffer that will receive the key.</span></span>

<span data-ttu-id="f2c5c-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="f2c5c-116">*cbMax*</span></span>

<span data-ttu-id="f2c5c-117">輸出緩衝區的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-117">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="f2c5c-118">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="f2c5c-118">*pcbActual*</span></span>

<span data-ttu-id="f2c5c-119">接收金鑰的實際大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-119">Receives the actual size in bytes of the key.</span></span>

<span data-ttu-id="f2c5c-120">如果這個參數為 Null，則不會傳回實際的索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-120">If this parameter is NULL then the actual size of the key will not be returned.</span></span>

<span data-ttu-id="f2c5c-121">如果輸出緩衝區太小，則仍會傳回實際的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-121">If the output buffer is too small, then the actual size of the key will still be returned.</span></span> <span data-ttu-id="f2c5c-122">這表示這個數位會大於輸出緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-122">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="f2c5c-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f2c5c-123">*grbit*</span></span>

<span data-ttu-id="f2c5c-124">位群組，其中包含要用於此呼叫的選項，包括下列零或多個。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-124">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2c5c-125">值</span><span class="sxs-lookup"><span data-stu-id="f2c5c-125">Value</span></span></p></th>
<th><p><span data-ttu-id="f2c5c-126">意義</span><span class="sxs-lookup"><span data-stu-id="f2c5c-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2c5c-127">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="f2c5c-127">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="f2c5c-128">當指定時，引擎會傳回資料指標的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-128">When specified, the engine will return the search key for the cursor.</span></span> <span data-ttu-id="f2c5c-129">搜尋索引鍵是使用一或多個先前的 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 呼叫來建立的，目的是要使用 <a href="gg294103(v=exchg.10).md">JetSeek</a> 來搜尋該金鑰，或使用 <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>設定索引範圍。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-129">The search key is built up using one or more prior calls to <a href="gg269329(v=exchg.10).md">JetMakeKey</a> for the purposes of seeking to that key using <a href="gg294103(v=exchg.10).md">JetSeek</a> or setting an index range using <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f2c5c-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2c5c-130">Return Value</span></span>

<span data-ttu-id="f2c5c-131">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f2c5c-132">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2c5c-133">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f2c5c-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="f2c5c-134">Description</span><span class="sxs-lookup"><span data-stu-id="f2c5c-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2c5c-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f2c5c-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f2c5c-136">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c5c-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f2c5c-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f2c5c-138">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-138">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c5c-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f2c5c-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f2c5c-140">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="f2c5c-141">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c5c-142">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="f2c5c-142">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="f2c5c-143">沒有目前的資料指標搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-143">There is no current search key for the cursor.</span></span> <span data-ttu-id="f2c5c-144">如果指定 JET_bitRetrieveCopy，且尚未使用先前的<a href="gg269329(v=exchg.10).md">JetMakeKey</a>呼叫來為此資料指標建立搜尋索引鍵<strong>，則會</strong>發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-144">This will happen for <strong>JetRetrieveKey</strong> if JET_bitRetrieveCopy is specified and a search key has not been constructed for this cursor using a prior call to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span> <span data-ttu-id="f2c5c-145">搜尋索引鍵將會由先前呼叫 <a href="gg294117(v=exchg.10).md">JetMove</a>以外的資料指標上的任何導覽 API 來刪除。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-145">The search key will be deleted by a prior call to any navigational API on the cursor other than <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c5c-146">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="f2c5c-146">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="f2c5c-147">資料指標未放置在記錄上。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-147">The cursor is not positioned on a record.</span></span> <span data-ttu-id="f2c5c-148">此情況具有許多不同的原因。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-148">This can happen for many different reasons.</span></span> <span data-ttu-id="f2c5c-149">例如，如果資料指標目前位於目前索引的最後一筆記錄之後，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-149">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c5c-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f2c5c-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f2c5c-151">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c5c-152">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f2c5c-152">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f2c5c-153">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-153">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c5c-154">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f2c5c-154">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="f2c5c-155">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-155">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="f2c5c-156">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-156">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c5c-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f2c5c-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f2c5c-158">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c5c-159">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="f2c5c-159">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="f2c5c-160">作業已順利完成，但輸出緩衝區太小，無法接收整個金鑰。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-160">The operation completed successfully, but the output buffer was too small to receive the entire key.</span></span> <span data-ttu-id="f2c5c-161">輸出緩衝區已填滿最適合的索引鍵數量。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-161">The output buffer has been filled with as much of the key as would fit.</span></span> <span data-ttu-id="f2c5c-162">如果要求，也會傳回實際的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-162">The actual size of the key has also been returned, if requested.</span></span></p>
<p><span data-ttu-id="f2c5c-163"><strong>注意</strong>   如果指定 JET_bitRetrieveCopy，將不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-163"><strong>Note</strong>   This error will not be returned if JET_bitRetrieveCopy is specified.</span></span> <span data-ttu-id="f2c5c-164">如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-164">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f2c5c-165">成功時，會在輸出緩衝區中傳回索引項目在資料指標目前位置的索引鍵索引鍵。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-165">On success, the key for the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="f2c5c-166">如果傳回 JET_wrnBufferTruncated，輸出緩衝區將會包含所提供空間中最多的索引鍵，而且金鑰的實際大小將會正確。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-166">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the key as will fit in the space provided and the actual size of the key will be accurate.</span></span> <span data-ttu-id="f2c5c-167">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-167">No change to the database state will occur.</span></span>

<span data-ttu-id="f2c5c-168">失敗時，輸出緩衝區的狀態和金鑰的實際大小將會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-168">On failure, the state of the output buffer and the actual size of the key will be undefined.</span></span> <span data-ttu-id="f2c5c-169">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-169">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f2c5c-170">備註</span><span class="sxs-lookup"><span data-stu-id="f2c5c-170">Remarks</span></span>

<span data-ttu-id="f2c5c-171">金鑰通常應該視為不透明的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-171">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="f2c5c-172">不應嘗試利用此資料的內部結構。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-172">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="f2c5c-173">不過，您可以知道所有 ESENT 機碼的下列屬性：</span><span class="sxs-lookup"><span data-stu-id="f2c5c-173">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="f2c5c-174">您可以使用 [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) 函式，將索引鍵與其他索引鍵進行比較，以在來源索引項目資料表的原始索引中建立其相對順序。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-174">Keys may be compared against each other using [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) function to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="f2c5c-175">將索引項目的索引鍵與不同索引的索引鍵進行比較是無意義的。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-175">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="f2c5c-176">在 Windows Vista 之前，索引鍵一律小於或等於 JET_cbKeyMost (255) 位元組。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-176">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="f2c5c-177">在 Windows Vista 和更新版本中，金鑰可以更大。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-177">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="f2c5c-178">索引鍵的大小上限等於 JET_paramKeyMost 目前的值。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-178">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

<span data-ttu-id="f2c5c-179">除了上述的 ESENT 按鍵屬性之外，請務必注意，搜尋索引鍵與索引項目的索引鍵不同。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-179">In addition to the above properties of ESENT keys in general, it is important to note that a search key is different from the key for an index entry.</span></span> <span data-ttu-id="f2c5c-180">具體而言，搜尋索引鍵的長度可能會超過一般的按鍵。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-180">Specifically, a search key may be longer than an ordinary key.</span></span> <span data-ttu-id="f2c5c-181">當您在建立搜尋索引鍵時使用萬用字元選項時，就會發生這個額外的長度。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-181">This extra length occurs when a wildcard option is used while constructing the search key.</span></span> <span data-ttu-id="f2c5c-182">如需詳細資訊，請參閱 [JetMakeKey](./jetmakekey-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-182">See [JetMakeKey](./jetmakekey-function.md) for more information.</span></span>

<span data-ttu-id="f2c5c-183">此 API 存在所有版本中的重要 bug。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-183">There is an important bug in this API that is present in all releases.</span></span> <span data-ttu-id="f2c5c-184">如果使用 JET_bitRetrieveCopy 來要求搜尋索引鍵，而且輸出緩衝區太小而無法接收整個金鑰，則不會傳回 JET_wrnBufferTruncated。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-184">If the search key is requested using the use of JET_bitRetrieveCopy and the output buffer is too small to receive the entire key then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="f2c5c-185">將會改為傳回 JET_errSuccess。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-185">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="f2c5c-186">請務必確認使用 *pcbActual* 所傳回之金鑰的實際大小，是否小於或等於輸出緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-186">It is important to verify that the actual size of the key as returned using *pcbActual* is less than or equal to the size of the output buffer.</span></span> <span data-ttu-id="f2c5c-187">如果實際大小大於輸出緩衝區的大小，則 **JetRetrieveKey** 的呼叫端應該會回應，如同改為傳回 JET_wrnBufferTruncated。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-187">If the actual size is larger than the size of the output buffer, then the caller of **JetRetrieveKey** should react as if JET_wrnBufferTruncated were returned instead.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f2c5c-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2c5c-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2c5c-189"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="f2c5c-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f2c5c-190">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c5c-191"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="f2c5c-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f2c5c-192">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c5c-193"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="f2c5c-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f2c5c-194">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2c5c-195"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="f2c5c-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f2c5c-196">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2c5c-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f2c5c-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f2c5c-198">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="f2c5c-198">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f2c5c-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2c5c-199">See Also</span></span>

[<span data-ttu-id="f2c5c-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f2c5c-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f2c5c-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f2c5c-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f2c5c-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f2c5c-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f2c5c-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f2c5c-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f2c5c-204">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="f2c5c-204">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="f2c5c-205">JetSeek</span><span class="sxs-lookup"><span data-stu-id="f2c5c-205">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="f2c5c-206">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="f2c5c-206">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
