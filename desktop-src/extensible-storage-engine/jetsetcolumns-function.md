---
description: 深入瞭解： JetSetColumns 函數
title: JetSetColumns 函式
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112044"
---
# <a name="jetsetcolumns-function"></a><span data-ttu-id="6508c-103">JetSetColumns 函式</span><span class="sxs-lookup"><span data-stu-id="6508c-103">JetSetColumns Function</span></span>


<span data-ttu-id="6508c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6508c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumns-function"></a><span data-ttu-id="6508c-105">JetSetColumns 函式</span><span class="sxs-lookup"><span data-stu-id="6508c-105">JetSetColumns Function</span></span>

<span data-ttu-id="6508c-106">**JetSetColumns** 函式與 [JetSetColumn](./jetsetcolumn-function.md)的行為類似，但是可讓應用程式在單一作業中設定多個資料行值。</span><span class="sxs-lookup"><span data-stu-id="6508c-106">The **JetSetColumns** function is similar in behavior to [JetSetColumn](./jetsetcolumn-function.md) but allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="6508c-107">[JET_SETCOLUMN](./jet-setcolumn-structure.md)結構的陣列用來描述要設定的資料行值集合，以及描述要設定之每個資料行值的輸入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6508c-107">An array of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="6508c-108">參數</span><span class="sxs-lookup"><span data-stu-id="6508c-108">Parameters</span></span>

<span data-ttu-id="6508c-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="6508c-109">*sesid*</span></span>

<span data-ttu-id="6508c-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="6508c-110">The session to use for this call.</span></span>

<span data-ttu-id="6508c-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="6508c-111">*tableid*</span></span>

<span data-ttu-id="6508c-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="6508c-112">The cursor to use for this call.</span></span>

<span data-ttu-id="6508c-113">*psetcolumn*</span><span class="sxs-lookup"><span data-stu-id="6508c-113">*psetcolumn*</span></span>

<span data-ttu-id="6508c-114">一或多個 [JET_SETCOLUMN](./jet-setcolumn-structure.md) 結構的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="6508c-114">A pointer to an array of one or more [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures.</span></span> <span data-ttu-id="6508c-115">每個結構都包含要設定之資料行值的描述，以及要從哪裡取得要設定的資料行資料。</span><span class="sxs-lookup"><span data-stu-id="6508c-115">Each structure includes descriptions of which column value to set and from where to get column data to set.</span></span>

<span data-ttu-id="6508c-116">*csetcolumn*</span><span class="sxs-lookup"><span data-stu-id="6508c-116">*csetcolumn*</span></span>

<span data-ttu-id="6508c-117">*Psetcolumn* 所指定之陣列中的 [JET_SETCOLUMN](./jet-setcolumn-structure.md)結構數目。</span><span class="sxs-lookup"><span data-stu-id="6508c-117">The number of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures in the array given by *psetcolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="6508c-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="6508c-118">Return Value</span></span>

<span data-ttu-id="6508c-119">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="6508c-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6508c-120">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="6508c-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6508c-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6508c-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="6508c-122">Description</span><span class="sxs-lookup"><span data-stu-id="6508c-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6508c-123">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="6508c-123">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="6508c-124">提供的資料行識別碼超出資料行識別碼的合法限制。</span><span class="sxs-lookup"><span data-stu-id="6508c-124">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6508c-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="6508c-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="6508c-126">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="6508c-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6508c-127">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="6508c-127">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="6508c-128">與 JET_errNullInvalid 相同。</span><span class="sxs-lookup"><span data-stu-id="6508c-128">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6508c-129">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="6508c-129">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="6508c-130">給定 <em>columnid</em> 所描述的資料行不存在於資料表中。</span><span class="sxs-lookup"><span data-stu-id="6508c-130">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6508c-131">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="6508c-131">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="6508c-132">在插入複製刪除原始更新作業期間，嘗試更新長值的作業不合法。</span><span class="sxs-lookup"><span data-stu-id="6508c-132">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6508c-133">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="6508c-133">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="6508c-134">輸入緩衝區中提供的指定資料行值資料，超過固定長度資料行的自然大小限制，或是針對固定長度的文字或二進位資料行所設定的大小限制。</span><span class="sxs-lookup"><span data-stu-id="6508c-134">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="6508c-135">針對長資料行傳遞超過1024個位元組的資料，並設定 JET_bitSetIntrinsicLV 旗標時，也會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="6508c-135">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6508c-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="6508c-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="6508c-137">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="6508c-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="6508c-138">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="6508c-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6508c-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="6508c-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="6508c-140">指定的資料行值資料大小不符合固定長度資料類型的自然內容。</span><span class="sxs-lookup"><span data-stu-id="6508c-140">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6508c-141">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="6508c-141">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="6508c-142">在插入或更新作業期間，嘗試更新自動遞增資料行，或在取代作業期間更新版本資料行時，發生不合法的嘗試。</span><span class="sxs-lookup"><span data-stu-id="6508c-142">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6508c-143">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="6508c-143">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="6508c-144">提供的選項未知，或已知位設定的不合法組合。</span><span class="sxs-lookup"><span data-stu-id="6508c-144">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6508c-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="6508c-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="6508c-146">給定的 psetinfo- &gt; cbStruct 不是 <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> 結構的有效大小。</span><span class="sxs-lookup"><span data-stu-id="6508c-146">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6508c-147">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="6508c-147">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="6508c-148">Set column 作業嘗試建立重複的值，並指定 JET_bitSetUniqueMultiValues 或 JET_bitSetUniqueNormalizedMultiValues。</span><span class="sxs-lookup"><span data-stu-id="6508c-148">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6508c-149">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="6508c-149">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="6508c-150">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="6508c-150">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6508c-151">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="6508c-151">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="6508c-152">當呼叫會話不在交易中時，嘗試更新長的資料行值是不合法的。</span><span class="sxs-lookup"><span data-stu-id="6508c-152">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6508c-153">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="6508c-153">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="6508c-154">嘗試將非 Null 資料行設定為 Null 是不合法的。</span><span class="sxs-lookup"><span data-stu-id="6508c-154">An illegal attempt was made to set a non-NULL column to NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6508c-155">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="6508c-155">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="6508c-156">無法將資料行值設定為輸入緩衝區中的值，因為它會導致記錄超過其頁面大小的相關大小限制。</span><span class="sxs-lookup"><span data-stu-id="6508c-156">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="6508c-157"><a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>或<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>類型的資料行可以與剩餘的記錄資料分開儲存。</span><span class="sxs-lookup"><span data-stu-id="6508c-157">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="6508c-158">不過，其他資料行必須與記錄一起儲存，而且可能會導致超過記錄大小限制。</span><span class="sxs-lookup"><span data-stu-id="6508c-158">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="6508c-159">即使長的資料行在記錄內需要5個位元組的空間作為連結，但這也可能導致傳回 JET_errRecordTooBig。</span><span class="sxs-lookup"><span data-stu-id="6508c-159">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6508c-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="6508c-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="6508c-161">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="6508c-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6508c-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="6508c-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="6508c-163">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="6508c-163">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="6508c-164">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="6508c-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6508c-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="6508c-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="6508c-166">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="6508c-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6508c-167">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="6508c-167">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="6508c-168">資料指標目前不在插入新記錄或更新現有記錄的過程中。</span><span class="sxs-lookup"><span data-stu-id="6508c-168">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6508c-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="6508c-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="6508c-170">輸入緩衝區中的資料行值超過可變長度資料行所設定的最大長度，已被截斷。</span><span class="sxs-lookup"><span data-stu-id="6508c-170">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6508c-171">成功時，針對 psetcolumns 中所述的每個資料行，資料行值的所需部分會設定為從輸入緩衝區複製的資料。</span><span class="sxs-lookup"><span data-stu-id="6508c-171">On success, for each column described in the psetcolumns, the desired portion of the column value is set with data copied from the input buffer.</span></span> <span data-ttu-id="6508c-172">如果資料行資料集超過為可變長度資料行指定的最大長度，可能已被截斷。</span><span class="sxs-lookup"><span data-stu-id="6508c-172">The column data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="6508c-173">失敗時，資料指標位置會保持不變，而且複製緩衝區中不會更新任何資料行值資料。</span><span class="sxs-lookup"><span data-stu-id="6508c-173">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6508c-174">備註</span><span class="sxs-lookup"><span data-stu-id="6508c-174">Remarks</span></span>

<span data-ttu-id="6508c-175">如果任何個別的 set 資料行作業傳回錯誤，則整個 **JetSetColumns** 作業將會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6508c-175">If any individual set column operation returns an error then the whole **JetSetColumns** operation will return an error.</span></span> <span data-ttu-id="6508c-176">一般情況下，警告會在 psetcolumns 中傳回 \> ，而不是在此函式的傳回碼中傳回。</span><span class="sxs-lookup"><span data-stu-id="6508c-176">Warnings, in general, are returned in the psetcolumns-\>error and not in the return code from this function.</span></span> <span data-ttu-id="6508c-177">但是，如果最後一個資料行集有警告，則會從 **JetSetColumns** 本身傳回此警告。</span><span class="sxs-lookup"><span data-stu-id="6508c-177">However, if the last column set has a warning, then this warning will be returned from **JetSetColumns** itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6508c-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="6508c-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6508c-179"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="6508c-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6508c-180">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="6508c-180">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6508c-181"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="6508c-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6508c-182">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="6508c-182">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6508c-183"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="6508c-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6508c-184">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="6508c-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6508c-185"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="6508c-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6508c-186">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="6508c-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6508c-187"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6508c-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6508c-188">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="6508c-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6508c-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6508c-189">See Also</span></span>

[<span data-ttu-id="6508c-190">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="6508c-190">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="6508c-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6508c-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6508c-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="6508c-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="6508c-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="6508c-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="6508c-194">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="6508c-194">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="6508c-195">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="6508c-195">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="6508c-196">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="6508c-196">JetSetColumn</span></span>](./jetsetcolumn-function.md)
