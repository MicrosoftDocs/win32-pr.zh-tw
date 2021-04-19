---
description: 深入瞭解： JetRenameColumn 函數
title: JetRenameColumn 函式
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ab2dee1895e4148bb2ea0600464d7e9c4a6a358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988393"
---
# <a name="jetrenamecolumn-function"></a><span data-ttu-id="c85e1-103">JetRenameColumn 函式</span><span class="sxs-lookup"><span data-stu-id="c85e1-103">JetRenameColumn Function</span></span>


<span data-ttu-id="c85e1-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c85e1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenamecolumn-function"></a><span data-ttu-id="c85e1-105">JetRenameColumn 函式</span><span class="sxs-lookup"><span data-stu-id="c85e1-105">JetRenameColumn Function</span></span>

<span data-ttu-id="c85e1-106">**JetRenameColumn** 函數可以用來變更資料表中現有資料行的名稱。</span><span class="sxs-lookup"><span data-stu-id="c85e1-106">The **JetRenameColumn** function can be used to change the name of an existing column on a table.</span></span>

<span data-ttu-id="c85e1-107">**Windows xp：**  **JetRenameColumn** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="c85e1-107">**Windows XP:**  **JetRenameColumn** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c85e1-108">參數</span><span class="sxs-lookup"><span data-stu-id="c85e1-108">Parameters</span></span>

<span data-ttu-id="c85e1-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c85e1-109">*sesid*</span></span>

<span data-ttu-id="c85e1-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="c85e1-110">The session to use for this call.</span></span>

<span data-ttu-id="c85e1-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="c85e1-111">*tableid*</span></span>

<span data-ttu-id="c85e1-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="c85e1-112">The cursor to use for this call.</span></span>

<span data-ttu-id="c85e1-113">*szName*</span><span class="sxs-lookup"><span data-stu-id="c85e1-113">*szName*</span></span>

<span data-ttu-id="c85e1-114">要重新命名之資料行的目前名稱。</span><span class="sxs-lookup"><span data-stu-id="c85e1-114">The current name of the column that will be renamed.</span></span>

<span data-ttu-id="c85e1-115">*szNameNew*</span><span class="sxs-lookup"><span data-stu-id="c85e1-115">*szNameNew*</span></span>

<span data-ttu-id="c85e1-116">將重新命名之資料行的新名稱。</span><span class="sxs-lookup"><span data-stu-id="c85e1-116">The new name for the column that will be renamed.</span></span>

<span data-ttu-id="c85e1-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c85e1-117">*grbit*</span></span>

<span data-ttu-id="c85e1-118">此參數必須為0。</span><span class="sxs-lookup"><span data-stu-id="c85e1-118">This parameter must be 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="c85e1-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="c85e1-119">Return Value</span></span>

<span data-ttu-id="c85e1-120">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="c85e1-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c85e1-121">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="c85e1-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c85e1-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c85e1-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="c85e1-123">Description</span><span class="sxs-lookup"><span data-stu-id="c85e1-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c85e1-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c85e1-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c85e1-125">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="c85e1-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c85e1-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c85e1-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c85e1-127">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="c85e1-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c85e1-128">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="c85e1-128">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="c85e1-129">這個資料表的指定資料行不存在。</span><span class="sxs-lookup"><span data-stu-id="c85e1-129">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c85e1-130">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="c85e1-130">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="c85e1-131">其中一個指定的物件名稱無效。</span><span class="sxs-lookup"><span data-stu-id="c85e1-131">One of the specified object names was invalid.</span></span> <span data-ttu-id="c85e1-132">所有物件名稱都必須符合同一組規則。</span><span class="sxs-lookup"><span data-stu-id="c85e1-132">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="c85e1-133">這些規則如下：</span><span class="sxs-lookup"><span data-stu-id="c85e1-133">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="c85e1-134">物件名稱必須由 ASCII 字元組成。</span><span class="sxs-lookup"><span data-stu-id="c85e1-134">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="c85e1-135">物件名稱的長度必須至少有一個字元。</span><span class="sxs-lookup"><span data-stu-id="c85e1-135">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="c85e1-136">物件名稱的長度不得超過 JET_cbNameMost (64) 個字元。</span><span class="sxs-lookup"><span data-stu-id="c85e1-136">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="c85e1-137">物件名稱的開頭不可以是空格-物件名稱不能包含 ASCII 控制字元， (0x00 到 0x1F) 。</span><span class="sxs-lookup"><span data-stu-id="c85e1-137">Object names may not begin with a space - object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="c85e1-138">物件名稱不能包含驚嘆號 (！ ) 、句號 (. ) 、左括弧 ( [) 或右括弧 (] ) 字元。</span><span class="sxs-lookup"><span data-stu-id="c85e1-138">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="c85e1-139">一旦經過驗證之後，就只會將字串的部分寫入第一個空格 (如果有任何) 將用於物件名稱。</span><span class="sxs-lookup"><span data-stu-id="c85e1-139">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="c85e1-140">這實際上是指物件名稱不能包含空格。</span><span class="sxs-lookup"><span data-stu-id="c85e1-140">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c85e1-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c85e1-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c85e1-142">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="c85e1-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="c85e1-143">在下列情況下， <strong>JetRenameColumn</strong> 可能會發生：</span><span class="sxs-lookup"><span data-stu-id="c85e1-143">This can happen for <strong>JetRenameColumn</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="c85e1-144"><em>>szname</em> 為 Null。</span><span class="sxs-lookup"><span data-stu-id="c85e1-144"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="c85e1-145"><em>szNameNew</em> 為 Null。</span><span class="sxs-lookup"><span data-stu-id="c85e1-145"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c85e1-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c85e1-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c85e1-147">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="c85e1-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c85e1-148">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c85e1-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c85e1-149">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="c85e1-149">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="c85e1-150">只有當會話目前不在交易中時，才可以執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="c85e1-150">This operation may only be performed when the session is not currently inside a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c85e1-151">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c85e1-151">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c85e1-152">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="c85e1-152">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c85e1-153">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c85e1-153">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c85e1-154">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="c85e1-154">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c85e1-155">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c85e1-155">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c85e1-156">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="c85e1-156">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="c85e1-157">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c85e1-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c85e1-158">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c85e1-158">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c85e1-159">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="c85e1-159">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c85e1-160">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="c85e1-160">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="c85e1-161">無法在唯讀交易範圍內完成更新。</span><span class="sxs-lookup"><span data-stu-id="c85e1-161">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="c85e1-162">唯讀交易是指使用 JET_bitTransactionReadOnly 呼叫 <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> 來啟動的交易。</span><span class="sxs-lookup"><span data-stu-id="c85e1-162">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="c85e1-163">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c85e1-163">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c85e1-164">成功時，與資料指標相關聯之資料表中指定的資料行名稱會永久變更為新的名稱。</span><span class="sxs-lookup"><span data-stu-id="c85e1-164">On success, the name of the specified column in the table associated with the cursor is permanently changed to the new name.</span></span> <span data-ttu-id="c85e1-165">任何參考該資料行的索引也會更新。</span><span class="sxs-lookup"><span data-stu-id="c85e1-165">Any indexes that reference that column will also be updated.</span></span>

<span data-ttu-id="c85e1-166">失敗時，將不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="c85e1-166">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c85e1-167">備註</span><span class="sxs-lookup"><span data-stu-id="c85e1-167">Remarks</span></span>

<span data-ttu-id="c85e1-168">資料行重新命名作業不尋常，因為與其他架構作業不同的是，它不會做為交易來執行。</span><span class="sxs-lookup"><span data-stu-id="c85e1-168">The column rename operation is unusual because, unlike other schema operations, it is not carried out as a transaction.</span></span> <span data-ttu-id="c85e1-169">當給定資料表中的資料行在某個會話中重新命名時，任何其他使用該資料表的會話都會立即看到變更，即使它們是在交易中，也會導致該會話無法看到執行重新命名作業的會話所做的任何其他變更。</span><span class="sxs-lookup"><span data-stu-id="c85e1-169">When a column in a given table is renamed in one session then any other session using that table will see the change immediately, even if they are in a transaction that would prevent that session from seeing any other change made by the session doing the rename operation.</span></span>

<span data-ttu-id="c85e1-170">重新命名作業不會影響資料行的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="c85e1-170">The column ID of a column is not affected by the rename operation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c85e1-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="c85e1-171">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c85e1-172"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="c85e1-172"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c85e1-173">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="c85e1-173">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c85e1-174"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="c85e1-174"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c85e1-175">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="c85e1-175">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c85e1-176"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="c85e1-176"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c85e1-177">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="c85e1-177">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c85e1-178"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="c85e1-178"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c85e1-179">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="c85e1-179">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c85e1-180"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c85e1-180"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c85e1-181">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="c85e1-181">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c85e1-182"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c85e1-182"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c85e1-183">實作為 <strong>JetRenameColumnW</strong> (Unicode) 和 <strong>JetRenameColumnA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="c85e1-183">Implemented as <strong>JetRenameColumnW</strong> (Unicode) and <strong>JetRenameColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c85e1-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c85e1-184">See Also</span></span>

[<span data-ttu-id="c85e1-185">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c85e1-185">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c85e1-186">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c85e1-186">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c85e1-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c85e1-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c85e1-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c85e1-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c85e1-189">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="c85e1-189">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)
