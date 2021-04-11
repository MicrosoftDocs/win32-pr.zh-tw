---
description: 深入瞭解： JetSetColumnDefaultValue 函數
title: JetSetColumnDefaultValue 函式
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f50d30b2edeca716895d8dd2339d659f0e1382f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847830"
---
# <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="19b26-103">JetSetColumnDefaultValue 函式</span><span class="sxs-lookup"><span data-stu-id="19b26-103">JetSetColumnDefaultValue Function</span></span>


<span data-ttu-id="19b26-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="19b26-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumndefaultvalue-function"></a><span data-ttu-id="19b26-105">JetSetColumnDefaultValue 函式</span><span class="sxs-lookup"><span data-stu-id="19b26-105">JetSetColumnDefaultValue Function</span></span>

<span data-ttu-id="19b26-106">**JetSetColumnDefaultValue** 函數可以用來變更現有資料行的預設值。</span><span class="sxs-lookup"><span data-stu-id="19b26-106">The **JetSetColumnDefaultValue** function can be used to change the default value of an existing column.</span></span>

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="19b26-107">參數</span><span class="sxs-lookup"><span data-stu-id="19b26-107">Parameters</span></span>

<span data-ttu-id="19b26-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="19b26-108">*sesid*</span></span>

<span data-ttu-id="19b26-109">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="19b26-109">The session to use for this call.</span></span>

<span data-ttu-id="19b26-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="19b26-110">*dbid*</span></span>

<span data-ttu-id="19b26-111">此呼叫所要使用的資料庫。</span><span class="sxs-lookup"><span data-stu-id="19b26-111">The database to use for this call.</span></span>

<span data-ttu-id="19b26-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="19b26-112">*szTableName*</span></span>

<span data-ttu-id="19b26-113">包含將受影響之資料行的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="19b26-113">The name of the table containing the column that will be affected.</span></span>

<span data-ttu-id="19b26-114">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="19b26-114">*szColumnName*</span></span>

<span data-ttu-id="19b26-115">將變更其預設值的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="19b26-115">The name of the column whose default value will be changed.</span></span>

<span data-ttu-id="19b26-116">*pvData*</span><span class="sxs-lookup"><span data-stu-id="19b26-116">*pvData*</span></span>

<span data-ttu-id="19b26-117">包含新預設值的輸入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="19b26-117">The input buffer containing the new default value.</span></span>

<span data-ttu-id="19b26-118">*cbData*</span><span class="sxs-lookup"><span data-stu-id="19b26-118">*cbData*</span></span>

<span data-ttu-id="19b26-119">包含新預設值的輸入緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="19b26-119">The size of the input buffer containing the new default value.</span></span>

<span data-ttu-id="19b26-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="19b26-120">*grbit*</span></span>

<span data-ttu-id="19b26-121">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="19b26-121">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="19b26-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="19b26-122">Return Value</span></span>

<span data-ttu-id="19b26-123">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="19b26-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="19b26-124">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="19b26-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19b26-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="19b26-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="19b26-126">Description</span><span class="sxs-lookup"><span data-stu-id="19b26-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19b26-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="19b26-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="19b26-128">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="19b26-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b26-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="19b26-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="19b26-130">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="19b26-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19b26-131">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="19b26-131">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="19b26-132">與 JET_errNullInvalid 相同。</span><span class="sxs-lookup"><span data-stu-id="19b26-132">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b26-133">JET_errColumnInUse</span><span class="sxs-lookup"><span data-stu-id="19b26-133">JET_errColumnInUse</span></span></p></td>
<td><p><span data-ttu-id="19b26-134">索引目前正在使用這個指定的資料行。</span><span class="sxs-lookup"><span data-stu-id="19b26-134">This specified column is currently in use by an index.</span></span></p>
<p><span data-ttu-id="19b26-135"><strong>JetSetColumnDefaultValue</strong> 無法變更索引定義中所參考之資料行的預設值。</span><span class="sxs-lookup"><span data-stu-id="19b26-135"><strong>JetSetColumnDefaultValue</strong> cannot change the default value of a column that is referenced in the definition of an index.</span></span> <span data-ttu-id="19b26-136">這是因為這樣做可能會變更索引的內容。</span><span class="sxs-lookup"><span data-stu-id="19b26-136">This is because doing so could change the contents of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19b26-137">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="19b26-137">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="19b26-138">這個資料表的指定資料行不存在。</span><span class="sxs-lookup"><span data-stu-id="19b26-138">This specified column does not exist for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b26-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="19b26-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="19b26-140">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="19b26-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="19b26-141">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="19b26-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19b26-142">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="19b26-142">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="19b26-143">指定的資料庫識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="19b26-143">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b26-144">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="19b26-144">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="19b26-145">其中一個指定的物件名稱無效。</span><span class="sxs-lookup"><span data-stu-id="19b26-145">One of the specified object names was invalid.</span></span> <span data-ttu-id="19b26-146">所有物件名稱都必須符合同一組規則。</span><span class="sxs-lookup"><span data-stu-id="19b26-146">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="19b26-147">這些規則如下：</span><span class="sxs-lookup"><span data-stu-id="19b26-147">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="19b26-148">物件名稱必須由 ASCII 字元組成。</span><span class="sxs-lookup"><span data-stu-id="19b26-148">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="19b26-149">物件名稱的長度必須至少有一個字元。</span><span class="sxs-lookup"><span data-stu-id="19b26-149">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="19b26-150">物件名稱的長度不得超過 JET_cbNameMost (64) 個字元。</span><span class="sxs-lookup"><span data-stu-id="19b26-150">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="19b26-151">物件名稱不能以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="19b26-151">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="19b26-152">物件名稱不能包含 ASCII 控制字元 (0x00 到 0x1F) 。</span><span class="sxs-lookup"><span data-stu-id="19b26-152">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="19b26-153">物件名稱不能包含驚嘆號 (！ ) 、句號 (. ) 、左括弧 ( [) 或右括弧 (] ) 字元。</span><span class="sxs-lookup"><span data-stu-id="19b26-153">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="19b26-154">一旦經過驗證之後，就只會將字串的部分寫入第一個空格 (如果有任何) 將用於物件名稱。</span><span class="sxs-lookup"><span data-stu-id="19b26-154">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="19b26-155">這表示物件名稱不能包含空格。</span><span class="sxs-lookup"><span data-stu-id="19b26-155">This means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19b26-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="19b26-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="19b26-157">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="19b26-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b26-158">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="19b26-158">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="19b26-159">無法將資料行設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="19b26-159">The column could not be set to NULL.</span></span> <span data-ttu-id="19b26-160">這發生于 <strong>JetSetColumnDefaultValue</strong> 的時機：</span><span class="sxs-lookup"><span data-stu-id="19b26-160">This happens for <strong>JetSetColumnDefaultValue</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="19b26-161"><em>cbData</em> 為零。</span><span class="sxs-lookup"><span data-stu-id="19b26-161"><em>cbData</em> is zero.</span></span></p></li>
<li><p><span data-ttu-id="19b26-162"><strong>pvData</strong> 為 Null。</span><span class="sxs-lookup"><span data-stu-id="19b26-162"><strong>pvData</strong> is NULL.</span></span></p></li>
</ul>
<p><span data-ttu-id="19b26-163">因此，您無法將資料行的預設值 () 回 Null 或長度為零的值。</span><span class="sxs-lookup"><span data-stu-id="19b26-163">Therefore, it is not possible to set the default value of a column (back) to NULL or to a zero length value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19b26-164">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="19b26-164">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="19b26-165">此資料庫的指定資料表不存在。</span><span class="sxs-lookup"><span data-stu-id="19b26-165">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b26-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="19b26-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="19b26-167">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="19b26-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19b26-168">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="19b26-168">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="19b26-169">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="19b26-169">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="19b26-170">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="19b26-170">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b26-171">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="19b26-171">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="19b26-172">這個指定的資料表正由另一個會話所使用。</span><span class="sxs-lookup"><span data-stu-id="19b26-172">This specified table is in use by another session.</span></span></p>
<p><span data-ttu-id="19b26-173"><strong>JetSetColumnDefaultValue</strong> 需要資料表的獨佔存取權，才能針對 Windows Server 2003 之前的版本變更資料行的預設值。</span><span class="sxs-lookup"><span data-stu-id="19b26-173"><strong>JetSetColumnDefaultValue</strong> requires exclusive access to a table in order to change the default value of the column for releases prior to Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19b26-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="19b26-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="19b26-175">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="19b26-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b26-176">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="19b26-176">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="19b26-177">在唯讀交易範圍內嘗試進行更新是不合法的。</span><span class="sxs-lookup"><span data-stu-id="19b26-177">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="19b26-178">「唯讀交易」（read only transaction）是指使用 JET_bitTransactionReadOnly 呼叫 <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> 來啟動的交易。</span><span class="sxs-lookup"><span data-stu-id="19b26-178">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span> <span data-ttu-id="19b26-179">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="19b26-179">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19b26-180">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="19b26-180">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="19b26-181">另一個會話先前已鎖定記錄以進行更新。</span><span class="sxs-lookup"><span data-stu-id="19b26-181">Another session has previously locked the record for update.</span></span> <span data-ttu-id="19b26-182">此會話嘗試的更新將會失敗。</span><span class="sxs-lookup"><span data-stu-id="19b26-182">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="19b26-183">成功時，指定資料庫中指定之資料表的指定資料行預設值會永久變更為新的預設值。</span><span class="sxs-lookup"><span data-stu-id="19b26-183">On success, the default value of the specified column in the given table in the given database is permanently changed to the new default value.</span></span>

<span data-ttu-id="19b26-184">失敗時，將不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="19b26-184">On failure, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="19b26-185">備註</span><span class="sxs-lookup"><span data-stu-id="19b26-185">Remarks</span></span>

<span data-ttu-id="19b26-186">您無法變更範本資料表中之資料行的預設值。</span><span class="sxs-lookup"><span data-stu-id="19b26-186">It is not possible to change the default value of a column in a template table.</span></span>

<span data-ttu-id="19b26-187">資料庫引擎會以無訊息方式將長文字和長二進位資料行的資料行預設值截斷為255個位元組。</span><span class="sxs-lookup"><span data-stu-id="19b26-187">The database engine will silently truncate the default value of a column to 255 bytes for long text and long binary columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="19b26-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="19b26-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19b26-189"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="19b26-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="19b26-190">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="19b26-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b26-191"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="19b26-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="19b26-192">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="19b26-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19b26-193"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="19b26-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="19b26-194">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="19b26-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b26-195"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="19b26-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="19b26-196">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="19b26-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19b26-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="19b26-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="19b26-198">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="19b26-198">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19b26-199"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="19b26-199"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="19b26-200">實作為 <strong>JetSetColumnDefaultValueW</strong> (Unicode) 和 <strong>JetSetColumnDefaultValueA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="19b26-200">Implemented as <strong>JetSetColumnDefaultValueW</strong> (Unicode) and <strong>JetSetColumnDefaultValueA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="19b26-201">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19b26-201">See Also</span></span>

[<span data-ttu-id="19b26-202">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="19b26-202">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="19b26-203">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="19b26-203">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="19b26-204">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="19b26-204">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="19b26-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="19b26-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="19b26-206">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="19b26-206">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)  
[<span data-ttu-id="19b26-207">JetStopService</span><span class="sxs-lookup"><span data-stu-id="19b26-207">JetStopService</span></span>](./jetstopservice-function.md)
