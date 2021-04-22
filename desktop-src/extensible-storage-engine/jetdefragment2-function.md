---
description: 深入瞭解： JetDefragment2 函數
title: JetDefragment2 函式
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bcde8d55032d2e07466668b5a4d96b9a447d843
ms.sourcegitcommit: 35baf9ba19918a38c4ca8714f88c004af0c6f518
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107838802"
---
# <a name="jetdefragment2-function"></a><span data-ttu-id="a725d-103">JetDefragment2 函式</span><span class="sxs-lookup"><span data-stu-id="a725d-103">JetDefragment2 Function</span></span>


<span data-ttu-id="a725d-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a725d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment2-function"></a><span data-ttu-id="a725d-105">JetDefragment2 函式</span><span class="sxs-lookup"><span data-stu-id="a725d-105">JetDefragment2 Function</span></span>

<span data-ttu-id="a725d-106">**JetDefragment2** 函式會啟動並停止資料庫重組工作，這些工作會改善資料庫中的資料組織，並提供回呼參數以報告磁碟重組的進度。</span><span class="sxs-lookup"><span data-stu-id="a725d-106">The **JetDefragment2** function starts and stops database defragmentation tasks which improves data organization within a database, with a callback parameter available to report the progress of the defragmentation.</span></span> <span data-ttu-id="a725d-107">這樣做的目的是要在資料庫內更有效率地使用現有的磁片配置，以限制資料庫成長。</span><span class="sxs-lookup"><span data-stu-id="a725d-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="a725d-108">它也可以確保資料更緊密地封裝，藉此減少工作集。</span><span class="sxs-lookup"><span data-stu-id="a725d-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="a725d-109">最後，它可以透過更妥善的資料組織來加速一般作業，藉以改善應用程式效能。</span><span class="sxs-lookup"><span data-stu-id="a725d-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="a725d-110">**Windows xp：**  **JetDefragment2** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="a725d-110">**Windows XP:**  **JetDefragment2** is introduced in Windows XP.</span></span>

<span data-ttu-id="a725d-111">**JetDefragment2** 也包含回呼函式參數，可用來報告磁碟重組程式的進度。</span><span class="sxs-lookup"><span data-stu-id="a725d-111">**JetDefragment2** also contains a callback function parameter that is used to report on the progress of the defragmentation process.</span></span>

<span data-ttu-id="a725d-112">資料庫磁碟重組是一項線上作業，不會中斷一般資料庫活動，例如查詢作業或資料更新。</span><span class="sxs-lookup"><span data-stu-id="a725d-112">Database defragmentation is an online operation and does not interrupt regular database activity such as query operations or data updates.</span></span> <span data-ttu-id="a725d-113">**JetDefragment2** 也不會建立所有現有資料的複本。</span><span class="sxs-lookup"><span data-stu-id="a725d-113">**JetDefragment2** also does not make a copy of all existing data.</span></span> <span data-ttu-id="a725d-114">相反地，它會將資料庫重組。</span><span class="sxs-lookup"><span data-stu-id="a725d-114">Instead, it defragments a database in place.</span></span> <span data-ttu-id="a725d-115">最後， **JetDefragment2** 會復原內部資料庫空間以便重複使用，但不會釋出超過作業系統檔案系統的空間。</span><span class="sxs-lookup"><span data-stu-id="a725d-115">Lastly, **JetDefragment2** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="a725d-116">產生的資料格式可能更有效率，但通常不是最佳的。</span><span class="sxs-lookup"><span data-stu-id="a725d-116">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="a725d-117">磁碟重組僅限於釋出資料庫頁面以供重複使用，其中包含已經過邏輯刪除的資料。</span><span class="sxs-lookup"><span data-stu-id="a725d-117">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="a725d-118">磁碟重組也可讓資料庫頁面在某些情況下可供重複使用，方法是合併兩個頁面的資料以容納在單一頁面上。</span><span class="sxs-lookup"><span data-stu-id="a725d-118">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="a725d-119">這項作業不同于 [JetCompact](./jetcompact-function.md) ，這會讓唯讀資料庫的複本成為高度最佳的格式。</span><span class="sxs-lookup"><span data-stu-id="a725d-119">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="a725d-120">參數</span><span class="sxs-lookup"><span data-stu-id="a725d-120">Parameters</span></span>

<span data-ttu-id="a725d-121">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a725d-121">*sesid*</span></span>

<span data-ttu-id="a725d-122">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="a725d-122">The session to use for this call.</span></span>

<span data-ttu-id="a725d-123">*dbid*</span><span class="sxs-lookup"><span data-stu-id="a725d-123">*dbid*</span></span>

<span data-ttu-id="a725d-124">要重組的資料庫。</span><span class="sxs-lookup"><span data-stu-id="a725d-124">The database to defragment.</span></span>

<span data-ttu-id="a725d-125">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="a725d-125">*szTableName*</span></span>

<span data-ttu-id="a725d-126">有時 *szTableName* 是必要的，有時會被禁止：</span><span class="sxs-lookup"><span data-stu-id="a725d-126">Sometimes *szTableName* is required, and sometimes it is forbidden:</span></span>

| <span data-ttu-id="a725d-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a725d-127">*grbit*</span></span> | <span data-ttu-id="a725d-128">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="a725d-128">*szTableName*</span></span> |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | <span data-ttu-id="a725d-129">必須是 `NULL`。</span><span class="sxs-lookup"><span data-stu-id="a725d-129">Must be `NULL`.</span></span> |
| `JET_bitDefragmentBTree` | <span data-ttu-id="a725d-130">指定要重組的資料表/BTree 表名稱。</span><span class="sxs-lookup"><span data-stu-id="a725d-130">Specifies the name of the table/BTree to defragment.</span></span> |
| <span data-ttu-id="a725d-131">*其他*</span><span class="sxs-lookup"><span data-stu-id="a725d-131">*other*</span></span> | <span data-ttu-id="a725d-132">必須是 `NULL`。</span><span class="sxs-lookup"><span data-stu-id="a725d-132">Must be `NULL`.</span></span> |
 
<span data-ttu-id="a725d-133">針對指定資料庫識別碼所描述的整個資料庫執行磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="a725d-133">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="a725d-134">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="a725d-134">*pcPasses*</span></span>

<span data-ttu-id="a725d-135">開始進行線上磁碟重組工作時，此選擇性的輸入參數會設定磁碟重組傳遞的最大數目。</span><span class="sxs-lookup"><span data-stu-id="a725d-135">When starting an online defragmentation task, this optional input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="a725d-136">停止線上磁碟重組工作時，此選擇性輸出緩衝區會設定為執行的行程數目。</span><span class="sxs-lookup"><span data-stu-id="a725d-136">When stopping an online defragmentation task, this optional output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="a725d-137">當此參數設定為 Null 時，線上磁碟重組傳遞的數目是無限制的。</span><span class="sxs-lookup"><span data-stu-id="a725d-137">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="a725d-138">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="a725d-138">*pcSeconds*</span></span>

<span data-ttu-id="a725d-139">開始進行線上磁碟重組工作時，此選擇性的輸入參數會設定磁碟重組的最長時間。</span><span class="sxs-lookup"><span data-stu-id="a725d-139">When starting an online defragmentation task, this optional input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="a725d-140">停止線上磁碟重組工作時，此選擇性輸出緩衝區會設定為用於重組的時間長度。</span><span class="sxs-lookup"><span data-stu-id="a725d-140">When stopping an online defragmentation task, this optional output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="a725d-141">當此參數設定為 Null 或 *pcSeconds* 指向負值時，重組的最長時間是無限制的。</span><span class="sxs-lookup"><span data-stu-id="a725d-141">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="a725d-142">*回撥*</span><span class="sxs-lookup"><span data-stu-id="a725d-142">*callback*</span></span>

<span data-ttu-id="a725d-143">可定期重組呼叫以報告進度的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="a725d-143">Callback function that defragmentation calls regularly to report progress.</span></span>

| <span data-ttu-id="a725d-144">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a725d-144">*grbit*</span></span> | <span data-ttu-id="a725d-145">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="a725d-145">*szTableName*</span></span> |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | <span data-ttu-id="a725d-146">必須是 `NULL`。</span><span class="sxs-lookup"><span data-stu-id="a725d-146">Must be `NULL`.</span></span> |
| `JET_bitDefragmentBTree` | <span data-ttu-id="a725d-147">必須是 `NULL`。</span><span class="sxs-lookup"><span data-stu-id="a725d-147">Must be `NULL`.</span></span> |
| <span data-ttu-id="a725d-148">*其他*</span><span class="sxs-lookup"><span data-stu-id="a725d-148">*other*</span></span> | <span data-ttu-id="a725d-149">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a725d-149">Optional.</span></span>


<span data-ttu-id="a725d-150">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a725d-150">*grbit*</span></span>

<span data-ttu-id="a725d-151">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="a725d-151">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a725d-152">值</span><span class="sxs-lookup"><span data-stu-id="a725d-152">Value</span></span></p></th>
<th><p><span data-ttu-id="a725d-153">意義</span><span class="sxs-lookup"><span data-stu-id="a725d-153">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a725d-154">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="a725d-154">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="a725d-155">此選項可用來重組 ESE 資料庫空間配置的可用空間部分。</span><span class="sxs-lookup"><span data-stu-id="a725d-155">This option is used to defragment the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="a725d-156">資料庫空間分為兩種類型：擁有的空間和可用空間。</span><span class="sxs-lookup"><span data-stu-id="a725d-156">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="a725d-157">擁有的空間會配置給資料表或索引，而可用空間可供在資料表或索引內使用。</span><span class="sxs-lookup"><span data-stu-id="a725d-157">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="a725d-158">可用空間的行為更動態，而且需要進行線上磁碟重組，而非擁有的空間或資料表或索引資料。</span><span class="sxs-lookup"><span data-stu-id="a725d-158">Available space is much more dynamic in behavior and requires online defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a725d-159">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="a725d-159">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="a725d-160">此選項可用來啟動新的磁碟重組工作。</span><span class="sxs-lookup"><span data-stu-id="a725d-160">This option is used to start a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a725d-161">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="a725d-161">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="a725d-162">此選項可用來停止現有的已啟動磁碟重組工作。</span><span class="sxs-lookup"><span data-stu-id="a725d-162">This option is used to stop an existing started defragmentation task.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a725d-163">JET_bitDefragmentBTree</span><span class="sxs-lookup"><span data-stu-id="a725d-163">JET_bitDefragmentBTree</span></span></p></td>
<td><p><span data-ttu-id="a725d-164">此選項是用來重組 szTableName 所指定的 B 型樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="a725d-164">This option is used to defrag a B-Tree, specified by szTableName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a725d-165">JET_bitDefragmentBTreeBatch</span><span class="sxs-lookup"><span data-stu-id="a725d-165">JET_bitDefragmentBTreeBatch</span></span></p></td>
<td><p><span data-ttu-id="a725d-166">這個選項是用來呼叫整個資料庫上的 OLD2。</span><span class="sxs-lookup"><span data-stu-id="a725d-166">This option is used to call OLD2 on the entire database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a725d-167">傳回值</span><span class="sxs-lookup"><span data-stu-id="a725d-167">Return Value</span></span>

<span data-ttu-id="a725d-168">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="a725d-168">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a725d-169">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="a725d-169">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a725d-170">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a725d-170">Return code</span></span></p></th>
<th><p><span data-ttu-id="a725d-171">Description</span><span class="sxs-lookup"><span data-stu-id="a725d-171">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a725d-172">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a725d-172">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a725d-173">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="a725d-173">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a725d-174">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a725d-174">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a725d-175">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="a725d-175">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a725d-176">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="a725d-176">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="a725d-177">針對磁碟重組選擇的資料庫是唯讀的，而且無法以任何方式更新，包括磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="a725d-177">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a725d-178">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="a725d-178">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="a725d-179">指定的會話處於 [準備認可] 狀態，直到目前的交易認可或回復時，才會開始新的更新。</span><span class="sxs-lookup"><span data-stu-id="a725d-179">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a725d-180">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a725d-180">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a725d-181">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="a725d-181">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a725d-182">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a725d-182">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a725d-183">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="a725d-183">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="a725d-184">給定的資料庫識別碼與實例中的已知資料庫不相符。</span><span class="sxs-lookup"><span data-stu-id="a725d-184">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a725d-185">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a725d-185">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a725d-186">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="a725d-186">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a725d-187">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a725d-187">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a725d-188">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="a725d-188">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a725d-189">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a725d-189">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a725d-190">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="a725d-190">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="a725d-191">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a725d-191">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a725d-192">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a725d-192">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a725d-193">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="a725d-193">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a725d-194">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="a725d-194">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="a725d-195">指定的會話僅具有唯讀許可權，無法啟動可能執行更新的工作，包括磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="a725d-195">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a725d-196">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a725d-196">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="a725d-197">當版本存放區的設定大小不足以保存所有未處理的更新時，就會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a725d-197">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a725d-198">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="a725d-198">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="a725d-199">已通過 JET_bitDefragmentBatchStart 選項，但是磁碟重組工作已在指定的資料庫上執行磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="a725d-199">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a725d-200">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="a725d-200">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="a725d-201">已通過 JET_bitDefragmentBatchStop 選項，但目前沒有正在執行的磁碟重組工作。</span><span class="sxs-lookup"><span data-stu-id="a725d-201">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a725d-202">成功時，會執行要求的動作，以指定的選項針對指定的資料啟動磁碟重組工作，或執行停止現有磁碟重組工作的動作。</span><span class="sxs-lookup"><span data-stu-id="a725d-202">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="a725d-203">失敗時，啟動或停止線上磁碟重組作業所要求的動作不會完成。</span><span class="sxs-lookup"><span data-stu-id="a725d-203">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="a725d-204">不會發生其他副作用。</span><span class="sxs-lookup"><span data-stu-id="a725d-204">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a725d-205">備註</span><span class="sxs-lookup"><span data-stu-id="a725d-205">Remarks</span></span>

<span data-ttu-id="a725d-206">線上磁碟重組是透過參數設定以及此 API 來控制。</span><span class="sxs-lookup"><span data-stu-id="a725d-206">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="a725d-207">預設系統參數值為 JET_OnlineDefragAll，表示已針對所有支援的資料結構啟用磁碟重組。</span><span class="sxs-lookup"><span data-stu-id="a725d-207">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="a725d-208">不過，您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md)來停用線上磁碟重組，或選擇性地針對資料庫空間樹狀結構（僅限資料庫）、僅限串流檔案或這些選項的任何組合來啟用它。</span><span class="sxs-lookup"><span data-stu-id="a725d-208">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="a725d-209">如果進行線上磁碟重組的系統設定是過時的設定， **JetDefragment2** 就會將設定視為 JET_OnlineDefragAll。</span><span class="sxs-lookup"><span data-stu-id="a725d-209">If the system setting for on-line defragmentation is to an obsolete setting, **JetDefragment2** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="a725d-210">每個資料庫最多隻能執行一項工作。</span><span class="sxs-lookup"><span data-stu-id="a725d-210">There can at most be one task running for each database.</span></span> <span data-ttu-id="a725d-211">工作會以執行緒的形式在裝載 ESE 的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="a725d-211">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="a725d-212">用來啟動線上磁碟重組工作的會話，可以在磁碟重組工作繼續時用於資料庫作業，因為磁碟重組工作會配置自己的會話。</span><span class="sxs-lookup"><span data-stu-id="a725d-212">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="a725d-213">指定的會話只會用來檢查與工作啟動會話相關聯的許可權，並不會實際用於進行磁碟重組作業。</span><span class="sxs-lookup"><span data-stu-id="a725d-213">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a725d-214">規格需求</span><span class="sxs-lookup"><span data-stu-id="a725d-214">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a725d-215"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="a725d-215"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a725d-216">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="a725d-216">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a725d-217"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="a725d-217"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a725d-218">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="a725d-218">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a725d-219"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="a725d-219"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a725d-220">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="a725d-220">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a725d-221"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="a725d-221"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a725d-222">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="a725d-222">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a725d-223"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a725d-223"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a725d-224">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="a725d-224">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a725d-225"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a725d-225"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a725d-226">實作為 <strong>JetDefragment2W</strong> (Unicode) 和 <strong>JetDefragment2A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="a725d-226">Implemented as <strong>JetDefragment2W</strong> (Unicode) and <strong>JetDefragment2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a725d-227">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a725d-227">See Also</span></span>

[<span data-ttu-id="a725d-228">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a725d-228">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a725d-229">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a725d-229">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a725d-230">JetCompact</span><span class="sxs-lookup"><span data-stu-id="a725d-230">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="a725d-231">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="a725d-231">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="a725d-232">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a725d-232">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="a725d-233">JetStopService</span><span class="sxs-lookup"><span data-stu-id="a725d-233">JetStopService</span></span>](./jetstopservice-function.md)
