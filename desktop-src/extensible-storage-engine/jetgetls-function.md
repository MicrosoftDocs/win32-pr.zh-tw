---
description: 深入瞭解： JetGetLS 函數
title: JetGetLS 函式
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980676"
---
# <a name="jetgetls-function"></a><span data-ttu-id="07431-103">JetGetLS 函式</span><span class="sxs-lookup"><span data-stu-id="07431-103">JetGetLS Function</span></span>


<span data-ttu-id="07431-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="07431-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetls-function"></a><span data-ttu-id="07431-105">JetGetLS 函式</span><span class="sxs-lookup"><span data-stu-id="07431-105">JetGetLS Function</span></span>

<span data-ttu-id="07431-106">**JetGetLS** 函式可讓應用程式取出與資料指標相關聯的內容控制碼，或與該資料指標相關聯的資料表。</span><span class="sxs-lookup"><span data-stu-id="07431-106">The **JetGetLS** function enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="07431-107">此內容控制碼必須先前已使用 [JetSetLS](./jetsetls-function.md)設定。</span><span class="sxs-lookup"><span data-stu-id="07431-107">This context handle must have been previously set using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="07431-108">**JetGetLS** 也可以用來同時提取資料指標或資料表的目前內容控制碼，並重設該內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="07431-108">**JetGetLS** can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="07431-109">**Windows xp： JetGetLS** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="07431-109">**Windows XP:  JetGetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="07431-110">參數</span><span class="sxs-lookup"><span data-stu-id="07431-110">Parameters</span></span>

<span data-ttu-id="07431-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="07431-111">*sesid*</span></span>

<span data-ttu-id="07431-112">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="07431-112">The session to use for this call.</span></span>

<span data-ttu-id="07431-113">*tableid*</span><span class="sxs-lookup"><span data-stu-id="07431-113">*tableid*</span></span>

<span data-ttu-id="07431-114">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="07431-114">The cursor to use for this call.</span></span>

<span data-ttu-id="07431-115">*pls*</span><span class="sxs-lookup"><span data-stu-id="07431-115">*pls*</span></span>

<span data-ttu-id="07431-116">輸出緩衝區，這個輸出緩衝區會接收目前與資料指標或資料表相關聯的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="07431-116">The output buffer that receives the context handle currently associated with the cursor or table.</span></span>

<span data-ttu-id="07431-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="07431-117">*grbit*</span></span>

<span data-ttu-id="07431-118">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="07431-118">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07431-119">值</span><span class="sxs-lookup"><span data-stu-id="07431-119">Value</span></span></p></th>
<th><p><span data-ttu-id="07431-120">意義</span><span class="sxs-lookup"><span data-stu-id="07431-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07431-121">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="07431-121">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="07431-122">表示應該抓取與指定之資料指標相關聯的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="07431-122">Indicates that the context handle associated with the given cursor should be retrieved.</span></span></p>
<p><span data-ttu-id="07431-123">如果沒有指定 JET_bitLSCursor 或 JET_bitLSTable，則會假設 JET_bitLSCursor。</span><span class="sxs-lookup"><span data-stu-id="07431-123">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="07431-124">此選項不能搭配 JET_bitLSTable 使用。</span><span class="sxs-lookup"><span data-stu-id="07431-124">This option cannot be used with JET_bitLSTable.</span></span> <span data-ttu-id="07431-125">如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</span><span class="sxs-lookup"><span data-stu-id="07431-125">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07431-126">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="07431-126">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="07431-127">表示應該抓取與包含指定資料指標之資料表相關聯的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="07431-127">Indicates that the context handle associated to the table that contains the given cursor should be retrieved.</span></span> <span data-ttu-id="07431-128">搭配 JET_bitLSCursor 使用此選項是不合法的。</span><span class="sxs-lookup"><span data-stu-id="07431-128">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="07431-129">如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</span><span class="sxs-lookup"><span data-stu-id="07431-129">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07431-130">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="07431-130">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="07431-131">指出所選物件的內容控制碼應該重設為 JET_LSNil。</span><span class="sxs-lookup"><span data-stu-id="07431-131">Indicates that the context handle for the chosen object should be reset to JET_LSNil.</span></span> <span data-ttu-id="07431-132">內容控制碼的目前值會在輸出緩衝區中傳回。</span><span class="sxs-lookup"><span data-stu-id="07431-132">The current value of the context handle is returned in the output buffer.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="07431-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="07431-133">Return Value</span></span>

<span data-ttu-id="07431-134">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="07431-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="07431-135">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="07431-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07431-136">傳回碼</span><span class="sxs-lookup"><span data-stu-id="07431-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="07431-137">Description</span><span class="sxs-lookup"><span data-stu-id="07431-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07431-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="07431-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="07431-139">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="07431-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07431-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="07431-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="07431-141">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="07431-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07431-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="07431-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="07431-143">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="07431-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="07431-144">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="07431-144">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07431-145">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="07431-145">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="07431-146">其中一個要求的選項無效、以不合法的方式使用，或未執行。</span><span class="sxs-lookup"><span data-stu-id="07431-146">One of the options requested was invalid, used in an illegal manner, or not implemented.</span></span></p>
<p><span data-ttu-id="07431-147">當 JET_bitLSCursor 和 JET_bitLSTable 都已設定時， <strong>JetGetLS</strong> 就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="07431-147">This can happen for <strong>JetGetLS</strong> when both JET_bitLSCursor and JET_bitLSTable are set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07431-148">JET_errLSNotSet</span><span class="sxs-lookup"><span data-stu-id="07431-148">JET_errLSNotSet</span></span></p></td>
<td><p><span data-ttu-id="07431-149">無法傳回內容控制碼，因為目前沒有任何內容控制碼與要求的物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="07431-149">The context handle could not be returned because no context handle is currently associated with the requested object.</span></span></p>
<p><span data-ttu-id="07431-150"><strong>注意  </strong> 如果指定 JET_bitLSReset 但沒有與要求的物件相關聯的內容控制碼，就不會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="07431-150"><strong>Note  </strong> This error is not returned if JET_bitLSReset is specified yet no context handle was associated with the requested object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07431-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="07431-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="07431-152">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="07431-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07431-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="07431-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="07431-154">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="07431-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07431-155">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="07431-155">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="07431-156">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="07431-156">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="07431-157">成功時，已成功從要求的物件抓取內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="07431-157">On success, the context handle was successfully retrieved from the requested object.</span></span> <span data-ttu-id="07431-158">如果指定 JET_bitLSReset，則也會成功從物件中移除該內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="07431-158">If JET_bitLSReset was specified then that context handle was also successfully removed from the object.</span></span> <span data-ttu-id="07431-159">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="07431-159">No change to the database state will occur.</span></span>

<span data-ttu-id="07431-160">失敗時，不會變更所要求物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="07431-160">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="07431-161">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="07431-161">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="07431-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="07431-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07431-163"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="07431-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="07431-164">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="07431-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07431-165"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="07431-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="07431-166">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="07431-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07431-167"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="07431-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="07431-168">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="07431-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07431-169"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="07431-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="07431-170">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="07431-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07431-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="07431-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="07431-172">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="07431-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="07431-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07431-173">See Also</span></span>

[<span data-ttu-id="07431-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="07431-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="07431-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="07431-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="07431-176">JET_LS</span><span class="sxs-lookup"><span data-stu-id="07431-176">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="07431-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="07431-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="07431-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="07431-178">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="07431-179">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="07431-179">JetSetLS</span></span>](./jetsetls-function.md)
