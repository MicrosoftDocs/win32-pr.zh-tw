---
description: 深入瞭解： JetOpenTable 函數
title: JetOpenTable 函式
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689531"
---
# <a name="jetopentable-function"></a><span data-ttu-id="d6fb3-103">JetOpenTable 函式</span><span class="sxs-lookup"><span data-stu-id="d6fb3-103">JetOpenTable Function</span></span>


<span data-ttu-id="d6fb3-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d6fb3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentable-function"></a><span data-ttu-id="d6fb3-105">JetOpenTable 函式</span><span class="sxs-lookup"><span data-stu-id="d6fb3-105">JetOpenTable Function</span></span>

<span data-ttu-id="d6fb3-106">**JetOpenTable** 函數會在先前建立的資料表上開啟資料指標。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-106">The **JetOpenTable** function opens a cursor on a previously created table.</span></span>

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="d6fb3-107">參數</span><span class="sxs-lookup"><span data-stu-id="d6fb3-107">Parameters</span></span>

<span data-ttu-id="d6fb3-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d6fb3-108">*sesid*</span></span>

<span data-ttu-id="d6fb3-109">要使用的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-109">The database session context to use.</span></span>

<span data-ttu-id="d6fb3-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="d6fb3-110">*dbid*</span></span>

<span data-ttu-id="d6fb3-111">用來尋找資料表的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-111">The database identifier to use to find the table.</span></span>

<span data-ttu-id="d6fb3-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="d6fb3-112">*szTableName*</span></span>

<span data-ttu-id="d6fb3-113">要開啟之資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-113">The name of the table to open.</span></span>

<span data-ttu-id="d6fb3-114">*pvParameters*</span><span class="sxs-lookup"><span data-stu-id="d6fb3-114">*pvParameters*</span></span>

<span data-ttu-id="d6fb3-115">已取代。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-115">Deprecated.</span></span> <span data-ttu-id="d6fb3-116">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-116">Set to **NULL**.</span></span>

<span data-ttu-id="d6fb3-117">*cbParameters*</span><span class="sxs-lookup"><span data-stu-id="d6fb3-117">*cbParameters*</span></span>

<span data-ttu-id="d6fb3-118">已取代。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-118">Deprecated.</span></span> <span data-ttu-id="d6fb3-119">設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-119">Set to 0 (zero).</span></span>

<span data-ttu-id="d6fb3-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d6fb3-120">*grbit*</span></span>

<span data-ttu-id="d6fb3-121">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6fb3-122">值</span><span class="sxs-lookup"><span data-stu-id="d6fb3-122">Value</span></span></p></th>
<th><p><span data-ttu-id="d6fb3-123">意義</span><span class="sxs-lookup"><span data-stu-id="d6fb3-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6fb3-124">JET_bitTableDenyRead</span><span class="sxs-lookup"><span data-stu-id="d6fb3-124">JET_bitTableDenyRead</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-125">資料表無法由另一個資料庫會話開啟以供讀取存取。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-125">The table cannot be opened for read-access by another database session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6fb3-126">JET_bitTableDenyWrite</span><span class="sxs-lookup"><span data-stu-id="d6fb3-126">JET_bitTableDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-127">資料表無法由另一個資料庫會話開啟以供寫入存取。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-127">The table cannot be opened for write-access by another database session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6fb3-128">JET_bitTableNoCache</span><span class="sxs-lookup"><span data-stu-id="d6fb3-128">JET_bitTableNoCache</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-129">不要快取此資料表的頁面。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-129">Do not cache the pages for this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6fb3-130">JET_bitTablePermitDDL</span><span class="sxs-lookup"><span data-stu-id="d6fb3-130">JET_bitTablePermitDDL</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-131">允許對標示為 FixedDDL 的資料表進行 DDL 修改。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-131">Allows DDL modification on tables flagged as FixedDDL.</span></span> <span data-ttu-id="d6fb3-132">此選項必須與 JET_bitTableDenyRead 選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-132">This option must be used with the JET_bitTableDenyRead option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6fb3-133">JET_bitTablePreread</span><span class="sxs-lookup"><span data-stu-id="d6fb3-133">JET_bitTablePreread</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-134">提供資料表可能不在緩衝區快取中的提示，而且預先讀取可能會對效能有所説明。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-134">Provides a hint that the table is probably not in the buffer cache, and that pre-reading may be beneficial to performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6fb3-135">JET_bitTableReadOnly</span><span class="sxs-lookup"><span data-stu-id="d6fb3-135">JET_bitTableReadOnly</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-136">要求資料表的唯讀存取權。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-136">Requests read-only access to the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6fb3-137">JET_bitTableSequential</span><span class="sxs-lookup"><span data-stu-id="d6fb3-137">JET_bitTableSequential</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-138">因為應用程式會依序掃描，所以資料表應該非常積極地從磁片中預先提取。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-138">The table should be very aggressively prefetched from disk because the application will be scanning it sequentially.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6fb3-139">JET_bitTableUpdatable</span><span class="sxs-lookup"><span data-stu-id="d6fb3-139">JET_bitTableUpdatable</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-140">要求資料表的寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-140">Requests write-access to the table.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d6fb3-141">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="d6fb3-141">*ptableid*</span></span>

<span data-ttu-id="d6fb3-142">成功時，指向資料表的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-142">On success, points to the identifier of the table.</span></span> <span data-ttu-id="d6fb3-143">失敗時， *ptableid* 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-143">On failure, the contents for *ptableid* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="d6fb3-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6fb3-144">Return Value</span></span>

<span data-ttu-id="d6fb3-145">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-145">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d6fb3-146">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-146">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6fb3-147">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d6fb3-147">Return code</span></span></p></th>
<th><p><span data-ttu-id="d6fb3-148">Description</span><span class="sxs-lookup"><span data-stu-id="d6fb3-148">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6fb3-149">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d6fb3-149">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-150">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-150">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6fb3-151">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="d6fb3-151">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-152"><em>dbid</em> 不是有效的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-152"><em>dbid</em> is not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6fb3-153">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="d6fb3-153">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-154">傳入了不正確的 <em>grbit</em> 組合。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-154">A bad combination of <em>grbit</em> was passed in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6fb3-155">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="d6fb3-155">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-156"><em>SzTableName</em>中提供的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-156">The name given in <em>szTableName</em> is invalid.</span></span></p>
<p><span data-ttu-id="d6fb3-157">如需有效資料表名稱的詳細資訊，請參閱<a href="gg269210(v=exchg.10).md">JetCreateTable</a>中的<em>szTableName</em>參數。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-157">For more information about valid table names, see the <em>szTableName</em> parameter in <a href="gg269210(v=exchg.10).md">JetCreateTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6fb3-158">JET_errObjectNotFound</span><span class="sxs-lookup"><span data-stu-id="d6fb3-158">JET_errObjectNotFound</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-159">嘗試開啟不存在於資料庫中的資料表。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-159">An attempt was made to open a table that does not exist in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6fb3-160">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="d6fb3-160">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-161">作業失敗，因為引擎無法配置開啟新資料指標所需的資源。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-161">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="d6fb3-162">請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-162">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6fb3-163">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="d6fb3-163">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-164">資料表正由另一個資料庫作業使用中。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-164">The table is being used by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6fb3-165">JET_wrnTableInUseBySystem</span><span class="sxs-lookup"><span data-stu-id="d6fb3-165">JET_wrnTableInUseBySystem</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-166">非嚴重警告，指出系統正在使用該資料表。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-166">A nonfatal warning indicating that the table is being used by the system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6fb3-167">JET_errTableLocked</span><span class="sxs-lookup"><span data-stu-id="d6fb3-167">JET_errTableLocked</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-168">資料表已由另一個資料庫操作鎖定。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-168">The table is locked by another database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6fb3-169">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="d6fb3-169">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="d6fb3-170">嘗試一次開啟太多唯一資料表。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-170">An attempt was made to open too many unique tables at once.</span></span> <span data-ttu-id="d6fb3-171">請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-171">See the Remarks section.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="d6fb3-172">備註</span><span class="sxs-lookup"><span data-stu-id="d6fb3-172">Remarks</span></span>

<span data-ttu-id="d6fb3-173">使用 **JetOpenTable** 開啟的資料表通常應該以 [JetCloseTable](./jetclosetable-function.md)關閉。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-173">Tables opened with **JetOpenTable** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="d6fb3-174">在交易中呼叫 **JetOpenTable** 時，就會發生此規則的例外狀況，且會使用 [JetRollback](./jetrollback-function.md)) 將交易回復 (。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-174">The exception to this rule happens when **JetOpenTable** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="d6fb3-175">回復交易時，資料表會自動關閉。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-175">When rolling back a transaction, the table is automatically closed.</span></span> <span data-ttu-id="d6fb3-176">在此情況下，使用 [JetCloseTable](./jetclosetable-function.md)關閉資料表是錯誤的。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-176">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="d6fb3-177">以 **JetOpenTable** (（例如 MSysObjects、MSysUnicodeFixup) ）來開啟系統資料表是合法的。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-177">It is legal to open system tables with **JetOpenTable** (for example, MSysObjects, MSysUnicodeFixup).</span></span> <span data-ttu-id="d6fb3-178">系統資料表的架構可能會變更，因此不建議存取系統資料表。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-178">The schema of the system tables may change, so accessing system tables is discouraged.</span></span> <span data-ttu-id="d6fb3-179">可以同時開啟的唯一資料表數目，會直接受到 *JET_paramMaxOpenTables* 的影響。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-179">The number of unique tables that can be opened simultaneously is affected directly by *JET_paramMaxOpenTables*.</span></span> <span data-ttu-id="d6fb3-180">如果資料表目前為開啟狀態，則會在資料表上建立新的資料指標。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-180">If the table is currently open then a new cursor will be created on the table.</span></span> <span data-ttu-id="d6fb3-181">資料指標資源是使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 *JET_paramMaxCursors* 進行設定。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-181">Cursor resources are configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxCursors*.</span></span> <span data-ttu-id="d6fb3-182">另請參閱 [JetDupCursor](./jetdupcursor-function.md)。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-182">Also see [JetDupCursor](./jetdupcursor-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="d6fb3-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6fb3-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6fb3-184"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="d6fb3-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d6fb3-185">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6fb3-186"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="d6fb3-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d6fb3-187">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6fb3-188"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="d6fb3-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d6fb3-189">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6fb3-190"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="d6fb3-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d6fb3-191">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6fb3-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d6fb3-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d6fb3-193">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6fb3-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="d6fb3-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d6fb3-195">實作為 <strong>JetOpenTableW</strong> (Unicode) 和 <strong>JetOpenTableA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="d6fb3-195">Implemented as <strong>JetOpenTableW</strong> (Unicode) and <strong>JetOpenTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d6fb3-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6fb3-196">See Also</span></span>

[<span data-ttu-id="d6fb3-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d6fb3-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d6fb3-198">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d6fb3-198">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d6fb3-199">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d6fb3-199">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d6fb3-200">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d6fb3-200">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d6fb3-201">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="d6fb3-201">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="d6fb3-202">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="d6fb3-202">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="d6fb3-203">JetRollback</span><span class="sxs-lookup"><span data-stu-id="d6fb3-203">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="d6fb3-204">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="d6fb3-204">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="d6fb3-205">資源參數</span><span class="sxs-lookup"><span data-stu-id="d6fb3-205">Resource Parameters</span></span>](./resource-parameters.md)
