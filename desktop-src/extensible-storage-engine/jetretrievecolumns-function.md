---
description: 深入瞭解： JetRetrieveColumns 函數
title: JetRetrieveColumns 函式
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194873"
---
# <a name="jetretrievecolumns-function"></a><span data-ttu-id="95b83-103">JetRetrieveColumns 函式</span><span class="sxs-lookup"><span data-stu-id="95b83-103">JetRetrieveColumns Function</span></span>


<span data-ttu-id="95b83-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="95b83-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumns-function"></a><span data-ttu-id="95b83-105">JetRetrieveColumns 函式</span><span class="sxs-lookup"><span data-stu-id="95b83-105">JetRetrieveColumns Function</span></span>

<span data-ttu-id="95b83-106">**JetRetrieveColumns** 函數會從單一作業中的目前記錄抓取多個資料行值。</span><span class="sxs-lookup"><span data-stu-id="95b83-106">The **JetRetrieveColumns** function retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="95b83-107">[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)結構的陣列用來描述要抓取的資料行值集合，以及描述要抓取之每個資料行值的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="95b83-107">An array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="95b83-108">參數</span><span class="sxs-lookup"><span data-stu-id="95b83-108">Parameters</span></span>

<span data-ttu-id="95b83-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="95b83-109">*sesid*</span></span>

<span data-ttu-id="95b83-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="95b83-110">The session to use for this call.</span></span>

<span data-ttu-id="95b83-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="95b83-111">*tableid*</span></span>

<span data-ttu-id="95b83-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="95b83-112">The cursor to use for this call.</span></span>

<span data-ttu-id="95b83-113">*pretrievecolumn*</span><span class="sxs-lookup"><span data-stu-id="95b83-113">*pretrievecolumn*</span></span>

<span data-ttu-id="95b83-114">一或多個 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) 結構的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="95b83-114">A pointer to an array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="95b83-115">每個結構都包含要取得的資料行值的描述，以及要在哪裡儲存傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="95b83-115">Each structure includes descriptions of which column value to retrieve and where to store returned data.</span></span>

<span data-ttu-id="95b83-116">*cretrievecolumn*</span><span class="sxs-lookup"><span data-stu-id="95b83-116">*cretrievecolumn*</span></span>

<span data-ttu-id="95b83-117">*Pretrievecolumn* 所指定之陣列中的 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)結構數目。</span><span class="sxs-lookup"><span data-stu-id="95b83-117">The number of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures in the array given by *pretrievecolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="95b83-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="95b83-118">Return Value</span></span>

<span data-ttu-id="95b83-119">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="95b83-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="95b83-120">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="95b83-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95b83-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="95b83-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="95b83-122">Description</span><span class="sxs-lookup"><span data-stu-id="95b83-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95b83-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="95b83-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="95b83-124">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="95b83-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b83-125">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="95b83-125">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="95b83-126">傳遞了不正確多重值資料行序號值給 pretinfo- &gt; itagSequence。</span><span class="sxs-lookup"><span data-stu-id="95b83-126">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="95b83-127">多重值資料行值序號的有效值為1或更大。</span><span class="sxs-lookup"><span data-stu-id="95b83-127">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="95b83-128">值為 0 (零) 對此函數有效，但對 <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>無效。</span><span class="sxs-lookup"><span data-stu-id="95b83-128">A value of 0 (zero) is valid for this function but is invalid for <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b83-129">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="95b83-129">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="95b83-130">提供的資料行識別碼超出資料行識別碼的合法限制。</span><span class="sxs-lookup"><span data-stu-id="95b83-130">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b83-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="95b83-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="95b83-132">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="95b83-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b83-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="95b83-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="95b83-134">給定 <em>columnid</em> 所描述的資料行不存在於資料表中。</span><span class="sxs-lookup"><span data-stu-id="95b83-134">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b83-135">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="95b83-135">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="95b83-136">無法從索引中取出索引為子字串的資料行，因為只有資料行的一小部分通常會出現在每個索引項目目中。</span><span class="sxs-lookup"><span data-stu-id="95b83-136">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b83-137">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="95b83-137">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="95b83-138">在某些情況下，為抓取資料行提供的緩衝區必須夠大，才能傳回任何數量的資料行值。</span><span class="sxs-lookup"><span data-stu-id="95b83-138">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="95b83-139">例如，將可更新的可更新資料行調整為在呼叫會話的交易內容中保持一致，而且這項調整需要呼叫端所提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="95b83-139">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="95b83-140">如果提供的緩衝區空間不足，則會傳回 JET_errInvalidBufferSize，且不會傳回任何資料行資料。</span><span class="sxs-lookup"><span data-stu-id="95b83-140">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b83-141">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="95b83-141">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="95b83-142">提供的選項未知，或已知位設定的不合法組合。</span><span class="sxs-lookup"><span data-stu-id="95b83-142">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b83-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="95b83-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="95b83-144">指定的一個或多個參數不正確。</span><span class="sxs-lookup"><span data-stu-id="95b83-144">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="95b83-145">如果 retinfo 的大小小於 <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>的大小，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="95b83-145">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b83-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="95b83-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="95b83-147">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="95b83-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="95b83-148"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="95b83-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b83-149">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="95b83-149">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="95b83-150">資料指標未放置在記錄上。</span><span class="sxs-lookup"><span data-stu-id="95b83-150">The cursor is not positioned on a record.</span></span> <span data-ttu-id="95b83-151">此情況具有許多不同的原因。</span><span class="sxs-lookup"><span data-stu-id="95b83-151">This can happen for many different reasons.</span></span> <span data-ttu-id="95b83-152">例如，如果資料指標目前位於目前索引的最後一筆記錄之後，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="95b83-152">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b83-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="95b83-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="95b83-154">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="95b83-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b83-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="95b83-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="95b83-156">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="95b83-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b83-157">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="95b83-157">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="95b83-158">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="95b83-158">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="95b83-159"><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="95b83-159"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b83-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="95b83-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="95b83-161">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="95b83-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b83-162">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="95b83-162">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="95b83-163">無法取出整個資料行值，因為指定的緩衝區小於資料行的大小。</span><span class="sxs-lookup"><span data-stu-id="95b83-163">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="95b83-164">成功時，會在提供的緩衝區中傳回資料行資料和資料行大小， [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) 結構的陣列中所述。</span><span class="sxs-lookup"><span data-stu-id="95b83-164">On success, columns data and column size are returned in provided buffers described in array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="95b83-165">如果 *itagSequence* 設定為 0 (零) 表示需要多值欄位的實例數目而非資料行資料，則會在 *itagSequence* 欄位本身傳回多值資料行的實例數目。</span><span class="sxs-lookup"><span data-stu-id="95b83-165">If an *itagSequence* was set to 0 (zero) to indicate that the number of instances of a multi-valued field was desired instead of column data, then the number of instances of a multi-valued column is returned in the *itagSequence* field itself.</span></span> <span data-ttu-id="95b83-166">每個 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) 結構都有一個錯誤欄位，其中包含所抓取資料行的警告。</span><span class="sxs-lookup"><span data-stu-id="95b83-166">Each [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure has an error field that contains warnings for the column retrieved.</span></span> <span data-ttu-id="95b83-167">如果資料行是 **Null** 值，則錯誤碼會設定為 JET_wrnColumnNull。</span><span class="sxs-lookup"><span data-stu-id="95b83-167">If the column was **NULL** valued, then the error code will be set to JET_wrnColumnNull.</span></span>

<span data-ttu-id="95b83-168">失敗時，資料指標位置會保持不變，且不會將任何資料複製到提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="95b83-168">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="95b83-169">備註</span><span class="sxs-lookup"><span data-stu-id="95b83-169">Remarks</span></span>

<span data-ttu-id="95b83-170">**JetRetrieveColumns** 支援 [JetRetrieveColumn](./jetretrievecolumn-function.md) 不支援的其中一項功能。</span><span class="sxs-lookup"><span data-stu-id="95b83-170">**JetRetrieveColumns** supports one feature that [JetRetrieveColumn](./jetretrievecolumn-function.md) does not.</span></span> <span data-ttu-id="95b83-171">這是捕獲多值資料行實例數目的能力。</span><span class="sxs-lookup"><span data-stu-id="95b83-171">This is the ability to retrieve the number of instances of a multi-valued column.</span></span> <span data-ttu-id="95b83-172">這項功能的目的是讓應用程式取出資料行的所有值。</span><span class="sxs-lookup"><span data-stu-id="95b83-172">The purpose of this feature is to allow an application to retrieve all values of a column.</span></span> <span data-ttu-id="95b83-173">這可以藉由先判斷資料行具有的值數目來完成。</span><span class="sxs-lookup"><span data-stu-id="95b83-173">This can be done by first determining the number of values that a column has.</span></span> <span data-ttu-id="95b83-174">接下來，您可以使用為每個值配置的一個 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)結構，再次呼叫 **JetRetrieveColumns** 來判斷資料行資料的長度，藉以判斷其長度。</span><span class="sxs-lookup"><span data-stu-id="95b83-174">Next, their lengths can be determined by calling **JetRetrieveColumns** again with one [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure allocated for each value to determine the length of column data.</span></span> <span data-ttu-id="95b83-175">這可以藉由傳遞 *cbMax* 為 0 () 零的 **Null**_pvData_ 指標來完成，並在 *cbActual* 中抓取資料行長度。</span><span class="sxs-lookup"><span data-stu-id="95b83-175">This can be done by passing **NULL**_pvData_ pointers with *cbMax* of 0 (zero) and retrieving the column length in *cbActual*.</span></span> <span data-ttu-id="95b83-176">第三個和最後一個呼叫可以使用配置的記憶體做為資料行值資料。</span><span class="sxs-lookup"><span data-stu-id="95b83-176">The third and last call can be made with allocated memory for the column value data.</span></span>

<span data-ttu-id="95b83-177">如果任何資料行由於長度不足的緩衝區而遭到截斷，則 API 會傳回 JET_wrnBufferTruncated。</span><span class="sxs-lookup"><span data-stu-id="95b83-177">If any column retrieved is truncated due to an insufficient length buffer, then the API will return JET_wrnBufferTruncated.</span></span> <span data-ttu-id="95b83-178">不過，其他錯誤 JET_wrnColumnNull 只會在 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)的 [錯誤] 欄位中傳回。</span><span class="sxs-lookup"><span data-stu-id="95b83-178">However, other errors, JET_wrnColumnNull are returned only in the error field in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="95b83-179">這是因為應用程式通常會想要確保所有的資料都已從 **JetRetrieveColumns** 中取出並傳回此錯誤，以促進這項理解。</span><span class="sxs-lookup"><span data-stu-id="95b83-179">The reason for this is that applications often want to ensure that all data has been retrieved and returning this error from **JetRetrieveColumns** facilitates this understanding.</span></span>

#### <a name="requirements"></a><span data-ttu-id="95b83-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="95b83-180">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95b83-181"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="95b83-181"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="95b83-182">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="95b83-182">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b83-183"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="95b83-183"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="95b83-184">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="95b83-184">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b83-185"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="95b83-185"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="95b83-186">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="95b83-186">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95b83-187"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="95b83-187"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="95b83-188">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="95b83-188">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95b83-189"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="95b83-189"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="95b83-190">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="95b83-190">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="95b83-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95b83-191">See Also</span></span>

[<span data-ttu-id="95b83-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="95b83-192">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="95b83-193">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="95b83-193">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="95b83-194">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="95b83-194">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="95b83-195">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="95b83-195">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="95b83-196">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="95b83-196">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="95b83-197">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="95b83-197">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="95b83-198">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="95b83-198">JetSetColumns</span></span>](./jetsetcolumns-function.md)
