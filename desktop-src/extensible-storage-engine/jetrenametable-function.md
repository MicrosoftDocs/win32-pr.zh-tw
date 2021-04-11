---
description: 深入瞭解： JetRenameTable 函數
title: JetRenameTable 函式
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 624b194a1cad836b8927e6e7e4b8490fcad250b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320483"
---
# <a name="jetrenametable-function"></a><span data-ttu-id="ee249-103">JetRenameTable 函式</span><span class="sxs-lookup"><span data-stu-id="ee249-103">JetRenameTable Function</span></span>


<span data-ttu-id="ee249-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ee249-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrenametable-function"></a><span data-ttu-id="ee249-105">JetRenameTable 函式</span><span class="sxs-lookup"><span data-stu-id="ee249-105">JetRenameTable Function</span></span>

<span data-ttu-id="ee249-106">**JetRenameTable** 函數可以用來變更現有資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee249-106">The **JetRenameTable** function can be used to change the name of an existing table.</span></span>

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a><span data-ttu-id="ee249-107">參數</span><span class="sxs-lookup"><span data-stu-id="ee249-107">Parameters</span></span>

<span data-ttu-id="ee249-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="ee249-108">*sesid*</span></span>

<span data-ttu-id="ee249-109">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="ee249-109">The session to use for this call.</span></span>

<span data-ttu-id="ee249-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="ee249-110">*dbid*</span></span>

<span data-ttu-id="ee249-111">此呼叫所要使用的資料庫。</span><span class="sxs-lookup"><span data-stu-id="ee249-111">The database to use for this call.</span></span>

<span data-ttu-id="ee249-112">*szName*</span><span class="sxs-lookup"><span data-stu-id="ee249-112">*szName*</span></span>

<span data-ttu-id="ee249-113">即將重新命名之資料表的目前名稱。</span><span class="sxs-lookup"><span data-stu-id="ee249-113">The current name of the table that will be renamed.</span></span>

<span data-ttu-id="ee249-114">*szNameNew*</span><span class="sxs-lookup"><span data-stu-id="ee249-114">*szNameNew*</span></span>

<span data-ttu-id="ee249-115">將重新命名之資料表的新名稱。</span><span class="sxs-lookup"><span data-stu-id="ee249-115">The new name for the table that will be renamed.</span></span>

### <a name="return-value"></a><span data-ttu-id="ee249-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee249-116">Return Value</span></span>

<span data-ttu-id="ee249-117">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="ee249-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ee249-118">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="ee249-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee249-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ee249-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="ee249-120">Description</span><span class="sxs-lookup"><span data-stu-id="ee249-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee249-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ee249-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ee249-122">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="ee249-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee249-123">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ee249-123">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ee249-124">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="ee249-124">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee249-125">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ee249-125">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ee249-126">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="ee249-126">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="ee249-127">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="ee249-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee249-128">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="ee249-128">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="ee249-129">指定的資料庫無效。</span><span class="sxs-lookup"><span data-stu-id="ee249-129">The specified database was invalid.</span></span></p>
<p><span data-ttu-id="ee249-130">此錯誤只會在暫存資料庫上嘗試資料表重新命名作業時，在 Windows 2000 中傳回。</span><span class="sxs-lookup"><span data-stu-id="ee249-130">This error is only returned in Windows 2000 when a table rename operation is attempted on the temporary database.</span></span> <span data-ttu-id="ee249-131">在稍後的版本中，會傳回此案例的 JET_errInvalidDatabaseId。</span><span class="sxs-lookup"><span data-stu-id="ee249-131">JET_errInvalidDatabaseId is returned for this case in later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee249-132">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="ee249-132">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="ee249-133">指定的資料庫識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="ee249-133">The specified database ID was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee249-134">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="ee249-134">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="ee249-135">其中一個指定的物件名稱無效。</span><span class="sxs-lookup"><span data-stu-id="ee249-135">One of the specified object names was invalid.</span></span> <span data-ttu-id="ee249-136">所有物件名稱都必須符合同一組規則。</span><span class="sxs-lookup"><span data-stu-id="ee249-136">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="ee249-137">這些規則如下：</span><span class="sxs-lookup"><span data-stu-id="ee249-137">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="ee249-138">物件名稱必須由 ASCII 字元組成。</span><span class="sxs-lookup"><span data-stu-id="ee249-138">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="ee249-139">物件名稱的長度必須至少有一個字元。</span><span class="sxs-lookup"><span data-stu-id="ee249-139">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="ee249-140">物件名稱的長度不得超過 JET_cbNameMost (64) 個字元。</span><span class="sxs-lookup"><span data-stu-id="ee249-140">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="ee249-141">物件名稱不能以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="ee249-141">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="ee249-142">物件名稱不能包含 ASCII 控制字元 (0x00 到 0x1F) 。</span><span class="sxs-lookup"><span data-stu-id="ee249-142">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="ee249-143">物件名稱不能包含驚嘆號 (！ ) ，句號 (。 ) ，左括弧 ( [) ，或右括弧 (]，只有在驗證後，才會將字串的部分設為第一個空格 ) 如果有任何 (將用於物件名稱。</span><span class="sxs-lookup"><span data-stu-id="ee249-143">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character - once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="ee249-144">這實際上是指物件名稱不能包含空格。</span><span class="sxs-lookup"><span data-stu-id="ee249-144">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee249-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ee249-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ee249-146">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="ee249-146">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="ee249-147">在下列情況下， <strong>JetRenameTable</strong> 可能會發生：</span><span class="sxs-lookup"><span data-stu-id="ee249-147">This can happen for <strong>JetRenameTable</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="ee249-148"><em>>szname</em> 為 Null。</span><span class="sxs-lookup"><span data-stu-id="ee249-148"><em>szName</em> is NULL.</span></span></p></li>
<li><p><span data-ttu-id="ee249-149"><em>szNameNew</em> 為 Null。</span><span class="sxs-lookup"><span data-stu-id="ee249-149"><em>szNameNew</em> is NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee249-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ee249-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ee249-151">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="ee249-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee249-152">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="ee249-152">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="ee249-153">此資料庫的指定資料表不存在。</span><span class="sxs-lookup"><span data-stu-id="ee249-153">This specified table does not exist for this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee249-154">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ee249-154">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ee249-155">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="ee249-155">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee249-156">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="ee249-156">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="ee249-157">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="ee249-157">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="ee249-158">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="ee249-158">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee249-159">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ee249-159">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ee249-160">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="ee249-160">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee249-161">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="ee249-161">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="ee249-162">無法在唯讀交易範圍內完成更新。</span><span class="sxs-lookup"><span data-stu-id="ee249-162">An update cannot be done while inside the scope of a read-only transaction.</span></span> <span data-ttu-id="ee249-163">唯讀交易是指使用 JET_bitTransactionReadOnly 呼叫 <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> 來啟動的交易。</span><span class="sxs-lookup"><span data-stu-id="ee249-163">A read-only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="ee249-164">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="ee249-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ee249-165">成功時，指定資料庫中指定之資料表的名稱會永久變更為新的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee249-165">On success, the name of the specified table in the given database is permanently changed to the new name.</span></span>

<span data-ttu-id="ee249-166">失敗時，將不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="ee249-166">On failure, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="ee249-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee249-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee249-168"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="ee249-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ee249-169">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="ee249-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee249-170"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="ee249-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ee249-171">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="ee249-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee249-172"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="ee249-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ee249-173">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="ee249-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee249-174"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="ee249-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ee249-175">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="ee249-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee249-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ee249-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ee249-177">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="ee249-177">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee249-178"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ee249-178"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ee249-179">實作為 <strong>JetRenameTableW</strong> (Unicode) 和 <strong>JetRenameTableA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="ee249-179">Implemented as <strong>JetRenameTableW</strong> (Unicode) and <strong>JetRenameTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ee249-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee249-180">See Also</span></span>

[<span data-ttu-id="ee249-181">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="ee249-181">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="ee249-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ee249-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ee249-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ee249-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ee249-184">JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="ee249-184">JetBeginTransaction2</span></span>](./jetbegintransaction2-function.md)
