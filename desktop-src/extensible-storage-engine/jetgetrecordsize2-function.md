---
description: 深入瞭解： JetGetRecordSize2 函數
title: JetGetRecordSize2 函式
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c68eafaaa53b5b88e6b003bdbafce287035cbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981699"
---
# <a name="jetgetrecordsize2-function"></a><span data-ttu-id="7fd7e-103">JetGetRecordSize2 函式</span><span class="sxs-lookup"><span data-stu-id="7fd7e-103">JetGetRecordSize2 Function</span></span>


<span data-ttu-id="7fd7e-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7fd7e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordsize2-function"></a><span data-ttu-id="7fd7e-105">JetGetRecordSize2 函式</span><span class="sxs-lookup"><span data-stu-id="7fd7e-105">JetGetRecordSize2 Function</span></span>

<span data-ttu-id="7fd7e-106">**JetGetRecordSize2** 函數會從所需的位置抓取記錄大小資訊。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-106">The **JetGetRecordSize2** function retrieves record size information from the desired location.</span></span>

<span data-ttu-id="7fd7e-107">**Windows 7： JetGetRecordSize2** 是在 windows 7 作業系統中引進。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-107">**Windows 7:  JetGetRecordSize2** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="7fd7e-108">參數</span><span class="sxs-lookup"><span data-stu-id="7fd7e-108">Parameters</span></span>

<span data-ttu-id="7fd7e-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="7fd7e-109">*sesid*</span></span>

<span data-ttu-id="7fd7e-110">識別將用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="7fd7e-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="7fd7e-111">*tableid*</span></span>

<span data-ttu-id="7fd7e-112">識別將用於 API 呼叫的資料表或資料指標。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-112">Identifies the table or cursor that will be used for the API call.</span></span> <span data-ttu-id="7fd7e-113">資料指標必須放置在記錄上，或已備妥更新。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-113">The cursor must be positioned on a record, or have an update prepared.</span></span>

<span data-ttu-id="7fd7e-114">*precsize*</span><span class="sxs-lookup"><span data-stu-id="7fd7e-114">*precsize*</span></span>

<span data-ttu-id="7fd7e-115">[JET_RECSIZE2](./jet-recsize2-structure.md)結構之輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-115">A pointer to an output buffer for the [JET_RECSIZE2](./jet-recsize2-structure.md) structure.</span></span>

<span data-ttu-id="7fd7e-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="7fd7e-116">*grbit*</span></span>

<span data-ttu-id="7fd7e-117">這是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-117">This is one or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7fd7e-118">值</span><span class="sxs-lookup"><span data-stu-id="7fd7e-118">Value</span></span></p></th>
<th><p><span data-ttu-id="7fd7e-119">意義</span><span class="sxs-lookup"><span data-stu-id="7fd7e-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7fd7e-120">JET_bitRecordSizeInCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="7fd7e-120">JET_bitRecordSizeInCopyBuffer</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-121">這會抓取已準備進行更新的複製緩衝區中記錄的大小。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-121">This retrieves the size of the record that is in the copy buffer prepared for update.</span></span> <span data-ttu-id="7fd7e-122">否則， <em>tableid</em> 或資料指標必須放置在記錄上，而且將會使用該記錄。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-122">Otherwise, the <em>tableid</em> or cursor must be positioned on a record, and that record will be used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fd7e-123">JET_bitRecordSizeRunningTotal</span><span class="sxs-lookup"><span data-stu-id="7fd7e-123">JET_bitRecordSizeRunningTotal</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-124">當指定這個位時，在填滿內容之前， <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> 不會歸零，可有效地做為已造訪或已更新之多筆記錄的統計資料累積。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-124">When this bit is specified, the <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fd7e-125">JET_bitRecordSizeLocal</span><span class="sxs-lookup"><span data-stu-id="7fd7e-125">JET_bitRecordSizeLocal</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-126">這會導致 API 忽略非內建函式的 Long 值。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-126">This causes the API to ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="7fd7e-127">例如，只會使用頁面上的本機記錄。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-127">For example, only the local record on the page will be used.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="7fd7e-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="7fd7e-128">Return Value</span></span>

<span data-ttu-id="7fd7e-129">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7fd7e-130">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7fd7e-131">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7fd7e-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="7fd7e-132">Description</span><span class="sxs-lookup"><span data-stu-id="7fd7e-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7fd7e-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7fd7e-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-134">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fd7e-135">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="7fd7e-135">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-136">其中一個要求的選項無效或未執行。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-136">One of the requested options was invalid or not implemented.</span></span> <span data-ttu-id="7fd7e-137">當指定了不合法的<em>grbit</em>時， <strong>JetGetRecordSize2</strong>函數會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-137">This error will be returned by the <strong>JetGetRecordSize2</strong> function when an illegal <em>grbit</em> is specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fd7e-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7fd7e-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-139">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-139">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fd7e-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7fd7e-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-141">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fd7e-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7fd7e-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-143">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="7fd7e-144"><strong>WINDOWS XP：  </strong>只有 Windows XP 作業系統和更新版本的 Windows 才會傳回 JET_errInstanceUnavailable。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-144"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by the Windows XP operating system and later versions of Windows.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fd7e-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7fd7e-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-146">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-146">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fd7e-147">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7fd7e-147">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-148">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-148">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fd7e-149">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="7fd7e-149">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-150">同時針對多個執行緒使用相同的會話是不合法的。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-150">It is illegal to use the same session for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="7fd7e-151"><strong>WINDOWS XP：  </strong>只有 Windows XP 和更新版的 Windows 才會傳回 JET_errInstanceUnavailable。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-151"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by Windows XP and later versions of Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fd7e-152">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="7fd7e-152">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-153">如果資料指標的定位不正確，就可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-153">This can happen if the cursor was positioned incorrectly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fd7e-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="7fd7e-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-155">如果資料指標未放置於交易中，如果另一個執行緒從這個會話下刪除記錄，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-155">If the cursor was not positioned in a transaction, this can happen if another thread deletes the record out from under this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fd7e-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7fd7e-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7fd7e-157">如果傳遞的是 <strong>Null</strong><em>precsize</em> ，則可以傳回。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-157">This can be returned if a <strong>NULL</strong><em>precsize</em> was passed.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="7fd7e-158">備註</span><span class="sxs-lookup"><span data-stu-id="7fd7e-158">Remarks</span></span>

<span data-ttu-id="7fd7e-159">[JET_RECSIZE2](./jet-recsize2-structure.md)的 **cbOverhead** 欄位中累積的金鑰大小會受到 JET_bitRecordSizeInCopyBuffer 的影響。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-159">The size of the key accumulated in the **cbOverhead** field of [JET_RECSIZE2](./jet-recsize2-structure.md), is affected by JET_bitRecordSizeInCopyBuffer.</span></span> <span data-ttu-id="7fd7e-160">如果指定了此位，則在 **cbOverhead** 欄位中累積的索引鍵大小會是完整的金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-160">If this bit is specified, the key size accumulated in the **cbOverhead** field is the full key size.</span></span> <span data-ttu-id="7fd7e-161">如果未使用此位，累積的金鑰大小將不會包含任何因金鑰首碼壓縮而儲存的大小。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-161">If this bit is not used, the key size accumulated will not include any size saved due to key prefix compression.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7fd7e-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="7fd7e-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7fd7e-163"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="7fd7e-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7fd7e-164">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-164">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fd7e-165"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="7fd7e-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7fd7e-166">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-166">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fd7e-167"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="7fd7e-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7fd7e-168">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fd7e-169"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="7fd7e-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7fd7e-170">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fd7e-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7fd7e-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7fd7e-172">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="7fd7e-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7fd7e-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fd7e-173">See Also</span></span>

[<span data-ttu-id="7fd7e-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7fd7e-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7fd7e-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7fd7e-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7fd7e-176">JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="7fd7e-176">JET_RECSIZE</span></span>](./jet-recsize-structure.md)  
[<span data-ttu-id="7fd7e-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7fd7e-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7fd7e-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7fd7e-178">JET_TABLEID</span></span>](./jet-tableid.md)
