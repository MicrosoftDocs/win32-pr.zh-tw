---
description: 深入瞭解： JetCreateTable 函數
title: JetCreateTable 函式
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f385cfd668af934bfde2669277db7ed048a1fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980073"
---
# <a name="jetcreatetable-function"></a><span data-ttu-id="58538-103">JetCreateTable 函式</span><span class="sxs-lookup"><span data-stu-id="58538-103">JetCreateTable Function</span></span>


<span data-ttu-id="58538-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="58538-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetable-function"></a><span data-ttu-id="58538-105">JetCreateTable 函式</span><span class="sxs-lookup"><span data-stu-id="58538-105">JetCreateTable Function</span></span>

<span data-ttu-id="58538-106">**JetCreateTable** 函數會在 ESE 資料庫中建立空的資料表。</span><span class="sxs-lookup"><span data-stu-id="58538-106">The **JetCreateTable** function creates an empty table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a><span data-ttu-id="58538-107">參數</span><span class="sxs-lookup"><span data-stu-id="58538-107">Parameters</span></span>

<span data-ttu-id="58538-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="58538-108">*sesid*</span></span>

<span data-ttu-id="58538-109">要使用的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="58538-109">The database session context to use.</span></span>

<span data-ttu-id="58538-110">*dbid*</span><span class="sxs-lookup"><span data-stu-id="58538-110">*dbid*</span></span>

<span data-ttu-id="58538-111">要使用的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="58538-111">The database identifier to use.</span></span>

<span data-ttu-id="58538-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="58538-112">*szTableName*</span></span>

<span data-ttu-id="58538-113">要建立之索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="58538-113">The name of the index to create.</span></span>

<span data-ttu-id="58538-114">名稱必須根據下列規則來格式化：</span><span class="sxs-lookup"><span data-stu-id="58538-114">The name must be formatted according to the following rules:</span></span>

  - <span data-ttu-id="58538-115">小於 JET_cbNameMost，不包括終止的 Null。</span><span class="sxs-lookup"><span data-stu-id="58538-115">Be less than JET_cbNameMost, not including the terminating NULL.</span></span>

  - <span data-ttu-id="58538-116">由下列一組字元組成：0到9、A 到 Z、a 到 z，以及 "" 以外的所有其他標點符號 \!</span><span class="sxs-lookup"><span data-stu-id="58538-116">Be made of the following set of characters: 0 through 9, A through Z, a through z, and all other punctuation except for "\!"</span></span> <span data-ttu-id="58538-117"> (驚嘆號) 、"、" (逗號) 、" \[ " (左括弧) 和 " \] " (右括弧) —也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c、0x5d 到0x7f。</span><span class="sxs-lookup"><span data-stu-id="58538-117">(exclamation point), "," (comma), "\[" (opening bracket), and "\]" (closing bracket) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="58538-118">不是以空格開頭。</span><span class="sxs-lookup"><span data-stu-id="58538-118">Not begin with a space.</span></span>

  - <span data-ttu-id="58538-119">至少要有一個非空白字元。</span><span class="sxs-lookup"><span data-stu-id="58538-119">Be made of at least one non-space character.</span></span>

<span data-ttu-id="58538-120">*lPages*</span><span class="sxs-lookup"><span data-stu-id="58538-120">*lPages*</span></span>

<span data-ttu-id="58538-121">要配置給資料表的初始資料庫頁面數目。</span><span class="sxs-lookup"><span data-stu-id="58538-121">The initial number of database pages to allocate for the table.</span></span> <span data-ttu-id="58538-122">如果有多個資料列插入此資料表中，指定大於1的數位可以減少片段。</span><span class="sxs-lookup"><span data-stu-id="58538-122">Specifying a number larger than one can reduce fragmentation if many rows are inserted into this table.</span></span>

<span data-ttu-id="58538-123">*lDensity*</span><span class="sxs-lookup"><span data-stu-id="58538-123">*lDensity*</span></span>

<span data-ttu-id="58538-124">資料表密度（以百分比為單位）。</span><span class="sxs-lookup"><span data-stu-id="58538-124">The table density, in percentage points.</span></span> <span data-ttu-id="58538-125">此數位必須是0或20到100的範圍。</span><span class="sxs-lookup"><span data-stu-id="58538-125">The number must be either 0 or in the range of 20 through 100.</span></span> <span data-ttu-id="58538-126">傳遞0表示應該使用預設值。</span><span class="sxs-lookup"><span data-stu-id="58538-126">Passing 0 means that the default value should be used.</span></span> <span data-ttu-id="58538-127">預設值為80。</span><span class="sxs-lookup"><span data-stu-id="58538-127">The default is 80.</span></span>

<span data-ttu-id="58538-128">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="58538-128">*ptableid*</span></span>

<span data-ttu-id="58538-129">成功時，會在此欄位中傳回資料表識別碼。</span><span class="sxs-lookup"><span data-stu-id="58538-129">On success, the table identifier is returned in this field.</span></span> <span data-ttu-id="58538-130">如果 API 未傳回 JET_errSuccess，此值為未定義。</span><span class="sxs-lookup"><span data-stu-id="58538-130">The value is undefined if the API does not return JET_errSuccess.</span></span>

### <a name="return-value"></a><span data-ttu-id="58538-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="58538-131">Return Value</span></span>

<span data-ttu-id="58538-132">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="58538-132">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="58538-133">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="58538-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="58538-134">傳回碼</span><span class="sxs-lookup"><span data-stu-id="58538-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="58538-135">Description</span><span class="sxs-lookup"><span data-stu-id="58538-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58538-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="58538-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="58538-137">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="58538-137">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-138">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="58538-138">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="58538-139">無法解析回呼函數。</span><span class="sxs-lookup"><span data-stu-id="58538-139">The callback function could not be resolved.</span></span> <span data-ttu-id="58538-140">可能找不到 DLL，或可能找不到 DLL 中的函數。</span><span class="sxs-lookup"><span data-stu-id="58538-140">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="58538-141">啟用足夠記錄之後，事件記錄檔將會提供更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="58538-141">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-142">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="58538-142">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="58538-143">嘗試透過「正在進行」（update）或 SLV 資料行來編制索引， (請注意，SLV 資料行已被取代) 。</span><span class="sxs-lookup"><span data-stu-id="58538-143">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-144">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="58538-144">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="58538-145">如果 ptablecreate- &gt; grbit 指定 JET_bitTableCreateTemplateTable，但 ptablecreate- &gt; szTemplateTableName 設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="58538-145">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-146">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="58538-146">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="58538-147">資料行已經存在。</span><span class="sxs-lookup"><span data-stu-id="58538-147">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-148">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="58538-148">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="58538-149">嘗試在不存在的資料行上建立索引。</span><span class="sxs-lookup"><span data-stu-id="58538-149">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="58538-150">嘗試在不存在的資料行上有條件地編制索引，也會產生這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="58538-150">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-151">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="58538-151">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="58538-152">嘗試加入重複的資料行。</span><span class="sxs-lookup"><span data-stu-id="58538-152">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="58538-153">應該不會有一個以上的自動遞增資料行，而且每個資料表不能有一個以上的版本資料行。</span><span class="sxs-lookup"><span data-stu-id="58538-153">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-154">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="58538-154">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="58538-155">在<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>或<a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<em>ulDensity</em>成員中傳遞了不正確密度。</span><span class="sxs-lookup"><span data-stu-id="58538-155">An invalid density was passed in the <em>ulDensity</em> member in the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-156">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="58538-156">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="58538-157">表示<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>結構的<strong>szTemplateTableName</strong>成員中所命名的資料表不是標示為樣板資料表 (也就是說，該資料表沒有 JET_bitTableCreateTemplateTable 設定) 。</span><span class="sxs-lookup"><span data-stu-id="58538-157">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not a marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-158">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="58538-158">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="58538-159">嘗試定義兩個相同的索引。</span><span class="sxs-lookup"><span data-stu-id="58538-159">An attempt was made to define two identical indexes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-160">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="58538-160">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="58538-161">嘗試為數據表指定一個以上的主要索引。</span><span class="sxs-lookup"><span data-stu-id="58538-161">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="58538-162">資料表必須只有一個主要索引。</span><span class="sxs-lookup"><span data-stu-id="58538-162">A table must have exactly one primary index.</span></span> <span data-ttu-id="58538-163">如果未指定任何主要索引，database engine 將會以透明方式建立一個索引。</span><span class="sxs-lookup"><span data-stu-id="58538-163">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-164">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="58538-164">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="58538-165">指定了不正確索引定義。</span><span class="sxs-lookup"><span data-stu-id="58538-165">An invalid index definition was specified.</span></span> <span data-ttu-id="58538-166">收到此錯誤的部分可能原因包括：</span><span class="sxs-lookup"><span data-stu-id="58538-166">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="58538-167">主要索引是條件式 (也就是， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexPrimary 設定，而<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cConditionalColumn</strong>成員大於零) 。</span><span class="sxs-lookup"><span data-stu-id="58538-167">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="58538-168">Windows Server 2003 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="58538-168">Windows Server 2003 and later.</span></span> <span data-ttu-id="58538-169">嘗試建立具有元組限制的元組索引，但未在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構中傳遞<strong>ptuplelimits</strong>成員 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexTupleLimits 設定，但<strong>ptuplelimits</strong>指標為 Null) 。</span><span class="sxs-lookup"><span data-stu-id="58538-169">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="58538-170">在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>szKey</strong>成員中傳入不正確索引鍵定義。</span><span class="sxs-lookup"><span data-stu-id="58538-170">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="58538-171">如需有效定義的討論，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</span><span class="sxs-lookup"><span data-stu-id="58538-171">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="58538-172">將<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>中的<strong>cbVarSegMac</strong>成員設定為大於主要索引的 JET_cbPrimaryKeyMost () 或大於次要索引 JET_cbSecondaryKeyMost 的 () 。</span><span class="sxs-lookup"><span data-stu-id="58538-172">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="58538-173">傳遞不正確使用者定義 Unicode 索引組合， (在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>) 的<strong>grbit</strong>成員中設定 JET_bitIndexUnicode 位。</span><span class="sxs-lookup"><span data-stu-id="58538-173">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="58538-174">某些常見的原因包括<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>PIDXUNICODE</strong>成員為 Null，或<strong>PIDXUNICODE</strong>結構中指定的 LCID 無效。</span><span class="sxs-lookup"><span data-stu-id="58538-174">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="58538-175">指定主要索引的多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="58538-175">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="58538-176">正在嘗試編制太多條件式資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="58538-176">Trying to index too many conditional columns.</span></span> <span data-ttu-id="58538-177"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cConditionalColumn</strong>成員不得大於 JET_ccolKeyMost。</span><span class="sxs-lookup"><span data-stu-id="58538-177">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-178">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="58538-178">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="58538-179">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="58538-179">Windows XP and later.</span></span> <span data-ttu-id="58538-180">已指定 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，但不支援其限制。</span><span class="sxs-lookup"><span data-stu-id="58538-180">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="58538-181">請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="58538-181">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-182">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="58538-182">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="58538-183">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="58538-183">Windows XP and later.</span></span> <span data-ttu-id="58538-184">元組索引不可以是唯一的 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<em>grbit</em>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexUnique 設定) 。</span><span class="sxs-lookup"><span data-stu-id="58538-184">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-185">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="58538-185">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="58538-186">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="58538-186">Windows XP and later.</span></span> <span data-ttu-id="58538-187">元組索引只能在單一資料行上 (也就是，如果<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已設定 JET_bitIndexTuples，且<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>szKey</strong>成員指定了一個以上的資料行) 。</span><span class="sxs-lookup"><span data-stu-id="58538-187">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-188">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="58538-188">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="58538-189">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="58538-189">Windows XP and later.</span></span> <span data-ttu-id="58538-190">元組索引不可以是主要索引 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexTuples 設定) 。</span><span class="sxs-lookup"><span data-stu-id="58538-190">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-191">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="58538-191">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="58538-192">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="58538-192">Windows XP and later.</span></span> <span data-ttu-id="58538-193">元組索引不允許設定<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbVarSegMac</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="58538-193">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-194">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="58538-194">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="58538-195">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="58538-195">Windows XP and later.</span></span> <span data-ttu-id="58538-196">元組索引只能位於 text 或 Unicode 資料行上。</span><span class="sxs-lookup"><span data-stu-id="58538-196">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="58538-197">嘗試將其他資料行的索引 (例如二進位資料行) 會導致 JET_errIndexTuplesTextColumnsOnly。</span><span class="sxs-lookup"><span data-stu-id="58538-197">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-198">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="58538-198">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="58538-199">嘗試在交易中建立沒有版本資訊的索引。</span><span class="sxs-lookup"><span data-stu-id="58538-199">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-200">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="58538-200">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="58538-201"><a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cp</strong>成員未設定為有效的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="58538-201">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="58538-202">Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。</span><span class="sxs-lookup"><span data-stu-id="58538-202">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="58538-203">0值表示預設值將使用 (英文、1252) 。</span><span class="sxs-lookup"><span data-stu-id="58538-203">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-204">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="58538-204">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="58538-205"><a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>coltyp</strong>成員未設定為有效的資料行類型。</span><span class="sxs-lookup"><span data-stu-id="58538-205">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-206">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="58538-206">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="58538-207">可能會發生此錯誤的部分原因：</span><span class="sxs-lookup"><span data-stu-id="58538-207">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="58538-208"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgindexcreate</strong>成員已設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="58538-208">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="58538-209"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgcolumncreate</strong>成員已設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="58538-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="58538-210"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbStruct</strong>成員未設定為有效的值。</span><span class="sxs-lookup"><span data-stu-id="58538-210">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-211">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="58538-211">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="58538-212"><a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>或<a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>中指定了不正確<strong>grbit</strong>成員組合。</span><span class="sxs-lookup"><span data-stu-id="58538-212">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="58538-213">因為 <strong>grbit</strong> 成員包含不一致的值，所以索引定義無效。</span><span class="sxs-lookup"><span data-stu-id="58538-213">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="58538-214">可能的原因如下：</span><span class="sxs-lookup"><span data-stu-id="58538-214">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="58538-215">主要索引具有指定的略過位 (也就是，JET_bitIndexPrimary 是以 JET_bitIndexIgnoreNull、JET_bitIndexIgnoreAnyNull 或 JET_bitIndexIgnoreFirstNull) 傳遞。</span><span class="sxs-lookup"><span data-stu-id="58538-215">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="58538-216">空白索引不會忽略任何 Null 成員 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexEmpty 設定，但沒有 JET_bitIndexIgnoreAnyNull 設定) 。</span><span class="sxs-lookup"><span data-stu-id="58538-216">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="58538-217">傳入具有無效<strong>grbit</strong>成員的<a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>結構。</span><span class="sxs-lookup"><span data-stu-id="58538-217">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-218">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="58538-218">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="58538-219">在 (中傳遞不正確地區設定識別碼 (LCID) ，方法是透過<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構中的<strong>pidxunicode</strong>成員所指向的<a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a>結構的<strong>lcid</strong>成員，或透過<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構) 的<strong>lcid</strong>欄位來傳遞。</span><span class="sxs-lookup"><span data-stu-id="58538-219">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-220">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="58538-220">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="58538-221">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="58538-221">An invalid parameter was given.</span></span> <span data-ttu-id="58538-222">可能的原因如下：</span><span class="sxs-lookup"><span data-stu-id="58538-222">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="58538-223"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>RGCOLUMNCREATE</strong>成員為 Null。</span><span class="sxs-lookup"><span data-stu-id="58538-223">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="58538-224"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgcolumncreate</strong>成員中指定的其中一個<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( JET_COLUMNCREATE ) 。</span><span class="sxs-lookup"><span data-stu-id="58538-224">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="58538-225"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbKey</strong>成員設定為零。</span><span class="sxs-lookup"><span data-stu-id="58538-225">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="58538-226"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( JET_INDEXCREATE ) 。</span><span class="sxs-lookup"><span data-stu-id="58538-226">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-227">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="58538-227">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="58538-228">記錄太大。</span><span class="sxs-lookup"><span data-stu-id="58538-228">The record is too big.</span></span> <span data-ttu-id="58538-229">所有固定資料行之<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cbMax</strong>成員總和不得超過某個值。</span><span class="sxs-lookup"><span data-stu-id="58538-229">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-230">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="58538-230">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="58538-231">資料表已經存在。</span><span class="sxs-lookup"><span data-stu-id="58538-231">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-232">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="58538-232">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="58538-233">嘗試將過多的資料行新增至資料表。</span><span class="sxs-lookup"><span data-stu-id="58538-233">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="58538-234">資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="58538-234">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-235">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="58538-235">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="58538-236">嘗試將 Unicode 資料行正規化時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="58538-236">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="58538-237">這可能是因為系統資源不足所造成。</span><span class="sxs-lookup"><span data-stu-id="58538-237">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="58538-238">備註</span><span class="sxs-lookup"><span data-stu-id="58538-238">Remarks</span></span>

<span data-ttu-id="58538-239">**JetCreateTable** 會建立不包含任何資料行的資料表。</span><span class="sxs-lookup"><span data-stu-id="58538-239">**JetCreateTable** creates a table which does not contain any columns.</span></span> <span data-ttu-id="58538-240">若要加入資料行，請參閱 [JetAddColumn](./jetaddcolumn-function.md)。</span><span class="sxs-lookup"><span data-stu-id="58538-240">To add columns, see [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="58538-241">在內部， **JetCreateTable** 會呼叫 [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)，並使用下列內容填入 [JET_TABLECREATE2](./jet-tablecreate2-structure.md) 結構：</span><span class="sxs-lookup"><span data-stu-id="58538-241">Internally, **JetCreateTable** calls [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), filling in a [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure with:</span></span>

  - <span data-ttu-id="58538-242">JET_TABLECREATE2. cbStruct = sizeof ( JET_TABLECREATE2 ) </span><span class="sxs-lookup"><span data-stu-id="58538-242">JET_TABLECREATE2.cbStruct = sizeof( JET_TABLECREATE2 )</span></span>

  - <span data-ttu-id="58538-243">JET_TABLECREATE2. szTableName = szTableName</span><span class="sxs-lookup"><span data-stu-id="58538-243">JET_TABLECREATE2.szTableName = szTableName</span></span>

  - <span data-ttu-id="58538-244">JET_TABLECREATE2. ulPages = lPage</span><span class="sxs-lookup"><span data-stu-id="58538-244">JET_TABLECREATE2.ulPages = lPage</span></span>

  - <span data-ttu-id="58538-245">JET_TABLECREATE2. ulDensity = lDensity</span><span class="sxs-lookup"><span data-stu-id="58538-245">JET_TABLECREATE2.ulDensity = lDensity</span></span>

  - <span data-ttu-id="58538-246">JET_TABLECREATE2. tableid = JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="58538-246">JET_TABLECREATE2.tableid = JET_tableidNil</span></span>

<span data-ttu-id="58538-247">內部 [JET_TABLECREATE2](./jet-tablecreate2-structure.md) 結構的所有其他欄位都設定為零或 Null。</span><span class="sxs-lookup"><span data-stu-id="58538-247">All the other fields of the internal [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure are set to zero or NULL.</span></span> <span data-ttu-id="58538-248">在輸出時， *ptableid* 會設定為 JET_TABLECREATE2. tableid。</span><span class="sxs-lookup"><span data-stu-id="58538-248">On output, *ptableid* will be set to JET_TABLECREATE2.tableid.</span></span>

<span data-ttu-id="58538-249">如需詳細資訊，請參閱 [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="58538-249">See [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) for more details.</span></span>

<span data-ttu-id="58538-250">如同 [JetOpenTable](./jetopentable-function.md)，當應用程式使用從 [JET_TABLECREATE2](./jet-tablecreate2-structure.md)結構傳回的 **tableid** 成員完成時，通常應該會以 [JetCloseTable](./jetclosetable-function.md)來關閉。</span><span class="sxs-lookup"><span data-stu-id="58538-250">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned **tableid** member from the [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="58538-251">規格需求</span><span class="sxs-lookup"><span data-stu-id="58538-251">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58538-252"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="58538-252"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="58538-253">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="58538-253">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-254"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="58538-254"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="58538-255">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="58538-255">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-256"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="58538-256"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="58538-257">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="58538-257">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-258"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="58538-258"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="58538-259">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="58538-259">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58538-260"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="58538-260"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="58538-261">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="58538-261">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58538-262"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="58538-262"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="58538-263">實作為 <strong>JetCreateTableW</strong> (Unicode) 和 <strong>JetCreateTableA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="58538-263">Implemented as <strong>JetCreateTableW</strong> (Unicode) and <strong>JetCreateTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="58538-264">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58538-264">See Also</span></span>

[<span data-ttu-id="58538-265">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="58538-265">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="58538-266">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="58538-266">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="58538-267">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="58538-267">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="58538-268">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="58538-268">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="58538-269">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="58538-269">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="58538-270">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="58538-270">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="58538-271">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="58538-271">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="58538-272">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="58538-272">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
