---
description: 深入瞭解： JetCreateTableColumnIndex 函數
title: JetCreateTableColumnIndex 函式
TOCTitle: JetCreateTableColumnIndex Function
ms:assetid: 9192614b-20a6-40fb-906a-51fc057e7483
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269343(v=EXCHG.10)
ms:contentKeyID: 32765632
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndexA
- JetCreateTableColumnIndexW
- JetCreateTableColumnIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aea9f79617c35c5a956f0cd5f621c7faadffe668
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996872"
---
# <a name="jetcreatetablecolumnindex-function"></a><span data-ttu-id="f2e64-103">JetCreateTableColumnIndex 函式</span><span class="sxs-lookup"><span data-stu-id="f2e64-103">JetCreateTableColumnIndex Function</span></span>


<span data-ttu-id="f2e64-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f2e64-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetablecolumnindex-function"></a><span data-ttu-id="f2e64-105">JetCreateTableColumnIndex 函式</span><span class="sxs-lookup"><span data-stu-id="f2e64-105">JetCreateTableColumnIndex Function</span></span>

<span data-ttu-id="f2e64-106">**JetCreateTableColumnIndex** 函式會在 ESE 資料庫中建立一個資料表，其中包含一組初始的索引，以及一組 [JET_TABLECREATE](./jet-tablecreate-structure.md)結構陣列的初始資料行。</span><span class="sxs-lookup"><span data-stu-id="f2e64-106">The **JetCreateTableColumnIndex** function creates a table in an ESE database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE](./jet-tablecreate-structure.md) structures.</span></span> <span data-ttu-id="f2e64-107">名稱 **JetCreateTableColumnIndex** 來自物件的建立順序。</span><span class="sxs-lookup"><span data-stu-id="f2e64-107">The name **JetCreateTableColumnIndex** comes from the order of creation of the objects.</span></span> <span data-ttu-id="f2e64-108">它會先建立資料表、資料行，最後再建立索引。</span><span class="sxs-lookup"><span data-stu-id="f2e64-108">It first creates a table, columns, and then finally indexes.</span></span>

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE* ptablecreate
    );
```

### <a name="parameters"></a><span data-ttu-id="f2e64-109">參數</span><span class="sxs-lookup"><span data-stu-id="f2e64-109">Parameters</span></span>

<span data-ttu-id="f2e64-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f2e64-110">*sesid*</span></span>

<span data-ttu-id="f2e64-111">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="f2e64-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="f2e64-112">*dbid*</span><span class="sxs-lookup"><span data-stu-id="f2e64-112">*dbid*</span></span>

<span data-ttu-id="f2e64-113">用於 API 呼叫的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2e64-113">The database identifier to use for the API call.</span></span>

<span data-ttu-id="f2e64-114">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="f2e64-114">*ptablecreate*</span></span>

<span data-ttu-id="f2e64-115">[JET_TABLECREATE](./jet-tablecreate-structure.md)結構的指標，此結構會定義要建立的資料表。</span><span class="sxs-lookup"><span data-stu-id="f2e64-115">A pointer to a [JET_TABLECREATE](./jet-tablecreate-structure.md) structure which defines the table to be created.</span></span> <span data-ttu-id="f2e64-116">如需詳細資訊，請參閱 [JET_TABLECREATE](./jet-tablecreate-structure.md) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-116">See [JET_TABLECREATE](./jet-tablecreate-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="f2e64-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2e64-117">Return Value</span></span>

<span data-ttu-id="f2e64-118">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="f2e64-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f2e64-119">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="f2e64-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2e64-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f2e64-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="f2e64-121">Description</span><span class="sxs-lookup"><span data-stu-id="f2e64-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f2e64-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f2e64-123">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f2e64-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-124">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="f2e64-124">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="f2e64-125">無法解析回呼函數。</span><span class="sxs-lookup"><span data-stu-id="f2e64-125">The callback function could not be resolved.</span></span> <span data-ttu-id="f2e64-126">可能找不到 DLL，或可能找不到 DLL 中的函數。</span><span class="sxs-lookup"><span data-stu-id="f2e64-126">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="f2e64-127">啟用足夠記錄之後，事件記錄檔將會提供更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f2e64-127">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-128">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="f2e64-128">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="f2e64-129">嘗試透過「正在進行」（update）或 SLV 資料行來編制索引， (請注意，SLV 資料行已被取代) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-129">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-130">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="f2e64-130">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="f2e64-131">如果 ptablecreate- &gt; grbit 指定 JET_bitTableCreateTemplateTable，但 ptablecreate- &gt; szTemplateTableName 設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="f2e64-131">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-132">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="f2e64-132">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="f2e64-133">資料行已經存在。</span><span class="sxs-lookup"><span data-stu-id="f2e64-133">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-134">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="f2e64-134">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="f2e64-135">嘗試在不存在的資料行上建立索引。</span><span class="sxs-lookup"><span data-stu-id="f2e64-135">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="f2e64-136">嘗試在不存在的資料行上有條件地編制索引，也會產生這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="f2e64-136">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-137">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="f2e64-137">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="f2e64-138">嘗試加入重複的資料行。</span><span class="sxs-lookup"><span data-stu-id="f2e64-138">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="f2e64-139">應該不會有一個以上的自動遞增資料行，而且每個資料表不能有一個以上的版本資料行。</span><span class="sxs-lookup"><span data-stu-id="f2e64-139">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-140">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="f2e64-140">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="f2e64-141">如果<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>ulDensity</strong>成員設定為小於20或超過100的數位，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="f2e64-141">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-142">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="f2e64-142">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="f2e64-143">表示在<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>結構的<strong>szTemplateTableName</strong>成員中命名的資料表未標示為樣板資料表 (也就是說，該資料表沒有 JET_bitTableCreateTemplateTable 設定) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-143">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-144">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="f2e64-144">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="f2e64-145">嘗試定義兩個相同的索引。</span><span class="sxs-lookup"><span data-stu-id="f2e64-145">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-146">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="f2e64-146">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="f2e64-147">嘗試為數據表指定一個以上的主要索引。</span><span class="sxs-lookup"><span data-stu-id="f2e64-147">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="f2e64-148">資料表必須只有一個主要索引。</span><span class="sxs-lookup"><span data-stu-id="f2e64-148">A table must have exactly one primary index.</span></span> <span data-ttu-id="f2e64-149">如果未指定任何主要索引，database engine 將會以透明方式建立一個索引。</span><span class="sxs-lookup"><span data-stu-id="f2e64-149">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-150">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="f2e64-150">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="f2e64-151">指定了不正確索引定義。</span><span class="sxs-lookup"><span data-stu-id="f2e64-151">An invalid index definition was specified.</span></span> <span data-ttu-id="f2e64-152">收到此錯誤的部分可能原因包括：</span><span class="sxs-lookup"><span data-stu-id="f2e64-152">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2e64-153">主要索引是條件式 (也就是， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexPrimary 設定，而<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cConditionalColumn</strong>成員大於零) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-153">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="f2e64-154">Windows Server 2003 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="f2e64-154">Windows Server 2003 and later.</span></span> <span data-ttu-id="f2e64-155">嘗試建立具有元組限制的元組索引，但未在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構中傳遞<strong>ptuplelimits</strong>成員 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexTupleLimits 設定，但<strong>ptuplelimits</strong>指標為 Null) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-155">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="f2e64-156">在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>szKey</strong>成員中傳入不正確索引鍵定義。</span><span class="sxs-lookup"><span data-stu-id="f2e64-156">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="f2e64-157">如需有效定義的討論，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-157">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="f2e64-158">將<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>中的<strong>cbVarSegMac</strong>成員設定為大於主要索引的 JET_cbPrimaryKeyMost () 或大於次要索引 JET_cbSecondaryKeyMost 的 () 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-158">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="f2e64-159">傳遞不正確使用者定義 Unicode 索引組合， (在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>) 的<strong>grbit</strong>成員中設定 JET_bitIndexUnicode 位。</span><span class="sxs-lookup"><span data-stu-id="f2e64-159">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="f2e64-160">某些常見的原因包括<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>PIDXUNICODE</strong>成員為 Null，或<strong>PIDXUNICODE</strong>結構中指定的 LCID 無效。</span><span class="sxs-lookup"><span data-stu-id="f2e64-160">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="f2e64-161">指定主要索引的多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="f2e64-161">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="f2e64-162">正在嘗試編制太多條件式資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="f2e64-162">Trying to index too many conditional columns.</span></span> <span data-ttu-id="f2e64-163"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cConditionalColumn</strong>成員不得大於 JET_ccolKeyMost。</span><span class="sxs-lookup"><span data-stu-id="f2e64-163">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-164">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="f2e64-164">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="f2e64-165">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="f2e64-165">Windows XP and later.</span></span> <span data-ttu-id="f2e64-166">已指定 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，但不支援其限制。</span><span class="sxs-lookup"><span data-stu-id="f2e64-166">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="f2e64-167">請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="f2e64-167">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-168">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="f2e64-168">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="f2e64-169">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="f2e64-169">Windows XP and later.</span></span> <span data-ttu-id="f2e64-170">元組索引不可以是唯一的 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<em>grbit</em>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexUnique 設定) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-170">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-171">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="f2e64-171">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="f2e64-172">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="f2e64-172">Windows XP and later.</span></span> <span data-ttu-id="f2e64-173">元組索引只能在單一資料行上 (也就是，如果<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已設定 JET_bitIndexTuples，且<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>szKey</strong>成員指定了一個以上的資料行) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-173">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-174">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="f2e64-174">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="f2e64-175">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="f2e64-175">Windows XP and later.</span></span> <span data-ttu-id="f2e64-176">元組索引不可以是主要索引 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexTuples 設定) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-176">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-177">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="f2e64-177">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="f2e64-178">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="f2e64-178">Windows XP and later.</span></span> <span data-ttu-id="f2e64-179">元組索引只能位於 text 或 Unicode 資料行上。</span><span class="sxs-lookup"><span data-stu-id="f2e64-179">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="f2e64-180">嘗試將其他資料行的索引 (例如二進位資料行) 會導致 JET_errIndexTuplesTextColumnsOnly。</span><span class="sxs-lookup"><span data-stu-id="f2e64-180">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-181">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="f2e64-181">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="f2e64-182">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="f2e64-182">Windows XP and later.</span></span> <span data-ttu-id="f2e64-183">元組索引不允許設定<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbVarSegMac</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="f2e64-183">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-184">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="f2e64-184">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="f2e64-185">嘗試在交易中建立沒有版本資訊的索引。</span><span class="sxs-lookup"><span data-stu-id="f2e64-185">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-186">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="f2e64-186">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="f2e64-187"><a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cp</strong>成員未設定為有效的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="f2e64-187">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="f2e64-188">Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-188">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="f2e64-189">0值表示預設值將使用 (英文、1252) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-189">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-190">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="f2e64-190">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="f2e64-191"><a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>coltyp</strong>成員未設定為有效的資料行類型。</span><span class="sxs-lookup"><span data-stu-id="f2e64-191">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-192">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="f2e64-192">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="f2e64-193">可能會發生此錯誤的部分原因：</span><span class="sxs-lookup"><span data-stu-id="f2e64-193">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2e64-194"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgindexcreate</strong>成員已設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="f2e64-194">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="f2e64-195"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgcolumncreate</strong>成員已設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="f2e64-195">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="f2e64-196"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbStruct</strong>成員未設定為有效的值。</span><span class="sxs-lookup"><span data-stu-id="f2e64-196">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="f2e64-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="f2e64-198"><a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>或<a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>中指定了不正確<strong>grbit</strong>成員組合。</span><span class="sxs-lookup"><span data-stu-id="f2e64-198">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="f2e64-199">因為 <strong>grbit</strong> 成員包含不一致的值，所以索引定義無效。</span><span class="sxs-lookup"><span data-stu-id="f2e64-199">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="f2e64-200">可能的原因如下：</span><span class="sxs-lookup"><span data-stu-id="f2e64-200">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2e64-201">主要索引具有指定的略過位 (也就是，JET_bitIndexPrimary 是以 JET_bitIndexIgnoreNull、JET_bitIndexIgnoreAnyNull 或 JET_bitIndexIgnoreFirstNull) 傳遞。</span><span class="sxs-lookup"><span data-stu-id="f2e64-201">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="f2e64-202">空白索引不會忽略任何 Null 成員 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexEmpty 設定，但沒有 JET_bitIndexIgnoreAnyNull 設定) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-202">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="f2e64-203">傳入具有無效<strong>grbit</strong>成員的<a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>結構。</span><span class="sxs-lookup"><span data-stu-id="f2e64-203">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-204">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="f2e64-204">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="f2e64-205">在 (中傳遞不正確地區設定識別碼 (LCID) ，方法是透過<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構中的<strong>pidxunicode</strong>成員所指向的<a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a>結構的<strong>lcid</strong>成員，或透過<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構) 的<strong>lcid</strong>欄位來傳遞。</span><span class="sxs-lookup"><span data-stu-id="f2e64-205">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-206">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f2e64-206">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f2e64-207">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="f2e64-207">An invalid parameter was given.</span></span> <span data-ttu-id="f2e64-208">可能的原因如下：</span><span class="sxs-lookup"><span data-stu-id="f2e64-208">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="f2e64-209"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>RGCOLUMNCREATE</strong>成員為 Null。</span><span class="sxs-lookup"><span data-stu-id="f2e64-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="f2e64-210"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgcolumncreate</strong>成員中指定的其中一個<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( JET_COLUMNCREATE) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-210">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE).</span></span></p></li>
<li><p><span data-ttu-id="f2e64-211"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbKey</strong>成員設定為零。</span><span class="sxs-lookup"><span data-stu-id="f2e64-211">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="f2e64-212"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( JET_INDEXCREATE) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-212">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-213">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="f2e64-213">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="f2e64-214">記錄太大。</span><span class="sxs-lookup"><span data-stu-id="f2e64-214">The record is too big.</span></span> <span data-ttu-id="f2e64-215">所有固定資料行之<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cbMax</strong>成員總和不得超過某個值。</span><span class="sxs-lookup"><span data-stu-id="f2e64-215">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-216">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="f2e64-216">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="f2e64-217">資料表已經存在。</span><span class="sxs-lookup"><span data-stu-id="f2e64-217">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-218">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="f2e64-218">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="f2e64-219">嘗試將過多的資料行新增至資料表。</span><span class="sxs-lookup"><span data-stu-id="f2e64-219">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="f2e64-220">資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="f2e64-220">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-221">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="f2e64-221">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="f2e64-222">嘗試將 Unicode 資料行正規化時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="f2e64-222">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="f2e64-223">這可能是因為系統資源不足所造成。</span><span class="sxs-lookup"><span data-stu-id="f2e64-223">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="f2e64-224">備註</span><span class="sxs-lookup"><span data-stu-id="f2e64-224">Remarks</span></span>

<span data-ttu-id="f2e64-225">呼叫 **JetCreateTableColumnIndex** 等同于呼叫 [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)， [JET_TABLECREATE2](./jet-tablecreate2-structure.md) 結構中的每個欄位都包含 [JET_TABLECREATE](./jet-tablecreate-structure.md)的對應欄位值，但有下列例外狀況：</span><span class="sxs-lookup"><span data-stu-id="f2e64-225">Calling **JetCreateTableColumnIndex** is identical to calling [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), with each field in the [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure containing the value of the corresponding field of [JET_TABLECREATE](./jet-tablecreate-structure.md), with the following exceptions:</span></span>

  - <span data-ttu-id="f2e64-226">JET_TABLECREATE2 cbStruct 設定為 sizeof ( JET_TABLECREATE2) </span><span class="sxs-lookup"><span data-stu-id="f2e64-226">JET_TABLECREATE2.cbStruct set to sizeof( JET_TABLECREATE2)</span></span>

  - <span data-ttu-id="f2e64-227">JET_TABLECREATE2 szCallback 設定為 Null</span><span class="sxs-lookup"><span data-stu-id="f2e64-227">JET_TABLECREATE2.szCallback set to NULL</span></span>

  - <span data-ttu-id="f2e64-228">JET_TABLECREATE2 cbtyp 設定為0</span><span class="sxs-lookup"><span data-stu-id="f2e64-228">JET_TABLECREATE2.cbtyp set to 0</span></span>

<span data-ttu-id="f2e64-229">如需詳細資訊，請參閱 [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-229">See [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) for more details.</span></span>

<span data-ttu-id="f2e64-230">如同 [JetOpenTable](./jetopentable-function.md)，當應用程式使用傳回的 *tableid* 完成時，通常應該會以 [JetCloseTable](./jetclosetable-function.md)來關閉它。</span><span class="sxs-lookup"><span data-stu-id="f2e64-230">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned *tableid*, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="f2e64-231">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2e64-231">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-232"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="f2e64-232"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f2e64-233">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="f2e64-233">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-234"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="f2e64-234"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f2e64-235">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="f2e64-235">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-236"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="f2e64-236"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f2e64-237">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="f2e64-237">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-238"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="f2e64-238"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f2e64-239">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="f2e64-239">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2e64-240"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f2e64-240"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f2e64-241">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="f2e64-241">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2e64-242"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f2e64-242"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f2e64-243">實作為 <strong>JetCreateTableColumnIndexW</strong> (Unicode) 和 <strong>JetCreateTableColumnIndexA</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="f2e64-243">Implemented as <strong>JetCreateTableColumnIndexW</strong> (Unicode) and <strong>JetCreateTableColumnIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f2e64-244">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2e64-244">See Also</span></span>

[<span data-ttu-id="f2e64-245">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="f2e64-245">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="f2e64-246">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f2e64-246">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f2e64-247">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f2e64-247">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f2e64-248">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f2e64-248">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f2e64-249">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="f2e64-249">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="f2e64-250">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="f2e64-250">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="f2e64-251">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="f2e64-251">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="f2e64-252">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="f2e64-252">JetCreateTableColumnIndex</span></span>]()  
[<span data-ttu-id="f2e64-253">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="f2e64-253">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
