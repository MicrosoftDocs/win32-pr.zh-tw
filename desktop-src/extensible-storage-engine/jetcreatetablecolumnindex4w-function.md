---
description: 深入瞭解： JetCreateTableColumnIndex4W 函數
title: JetCreateTableColumnIndex4W 函式
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ebdb8cf62123febe2d44b5a638c285c180062c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988476"
---
# <a name="jetcreatetablecolumnindex4w-function"></a><span data-ttu-id="d928f-103">JetCreateTableColumnIndex4W 函式</span><span class="sxs-lookup"><span data-stu-id="d928f-103">JetCreateTableColumnIndex4W Function</span></span>


<span data-ttu-id="d928f-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d928f-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="d928f-105">**JetCreateTableColumnIndex4W** 函式會在可延伸的儲存引擎中建立資料表， (ESE ( 資料庫與一組初始的索引，以及一組 [JET_TABLECREATE3](./jet-tablecreate3-structure.md)結構的初始資料行。</span><span class="sxs-lookup"><span data-stu-id="d928f-105">The **JetCreateTableColumnIndex4W** function creates a table in an Extensible Storage Engine (ESE( database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structures.</span></span> <span data-ttu-id="d928f-106">[JET_TABLECREATE3](./jet-tablecreate3-structure.md)結構允許指定回呼函數。</span><span class="sxs-lookup"><span data-stu-id="d928f-106">The [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="d928f-107">**JetCreateTableColumnIndex4W** 函式是在 Windows 8 作業系統中引進的。</span><span class="sxs-lookup"><span data-stu-id="d928f-107">The **JetCreateTableColumnIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a><span data-ttu-id="d928f-108">參數</span><span class="sxs-lookup"><span data-stu-id="d928f-108">Parameters</span></span>

<span data-ttu-id="d928f-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d928f-109">*sesid*</span></span>

<span data-ttu-id="d928f-110">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="d928f-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="d928f-111">*dbid*</span><span class="sxs-lookup"><span data-stu-id="d928f-111">*dbid*</span></span>

<span data-ttu-id="d928f-112">用於 API 呼叫的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="d928f-112">The database identifier to use for the API call.</span></span>

<span data-ttu-id="d928f-113">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="d928f-113">*ptablecreate*</span></span>

<span data-ttu-id="d928f-114">[JET_TABLECREATE3](./jet-tablecreate3-structure.md)結構的指標，此結構會定義要建立的資料表。</span><span class="sxs-lookup"><span data-stu-id="d928f-114">A pointer to a [JET_TABLECREATE3](./jet-tablecreate3-structure.md) structure that defines the table to be created.</span></span> <span data-ttu-id="d928f-115">如需詳細資訊，請參閱 [JET_TABLECREATE3](./jet-tablecreate3-structure.md) 。</span><span class="sxs-lookup"><span data-stu-id="d928f-115">See [JET_TABLECREATE3](./jet-tablecreate3-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="d928f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d928f-116">Return value</span></span>

<span data-ttu-id="d928f-117">此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="d928f-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="d928f-118">如需有關可能的可延伸儲存體 Enginge (ESE) 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="d928f-118">For more information about the possible Extensible Storage Enginge (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d928f-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d928f-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="d928f-120">Description</span><span class="sxs-lookup"><span data-stu-id="d928f-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d928f-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d928f-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d928f-122">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="d928f-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-123">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="d928f-123">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="d928f-124">無法解析回呼函數。</span><span class="sxs-lookup"><span data-stu-id="d928f-124">The callback function could not be resolved.</span></span> <span data-ttu-id="d928f-125">可能找不到 DLL，或可能找不到 DLL 中的函數。</span><span class="sxs-lookup"><span data-stu-id="d928f-125">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="d928f-126">啟用足夠記錄之後，事件記錄檔將會提供更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d928f-126">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-127">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="d928f-127">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="d928f-128">嘗試透過「正在進行」（update）或 SLV 資料行來編制索引， (請注意，SLV 資料行已被取代) 。</span><span class="sxs-lookup"><span data-stu-id="d928f-128">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-129">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="d928f-129">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="d928f-130">如果 <em>ptablecreate- &gt; grbit</em> 參數指定 JET_bitTableCreateTemplateTable 值，但 <em>ptablecreate- &gt; szTemplateTableName</em> 參數設定為 null，則會傳回。</span><span class="sxs-lookup"><span data-stu-id="d928f-130">Returned if the <em>ptablecreate-&gt;grbit</em> parameter specifies the JET_bitTableCreateTemplateTable value, but the <em>ptablecreate-&gt;szTemplateTableName</em> parameter is set to null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-131">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="d928f-131">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="d928f-132">資料行已經存在。</span><span class="sxs-lookup"><span data-stu-id="d928f-132">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="d928f-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="d928f-134">嘗試在不存在的資料行上建立索引。</span><span class="sxs-lookup"><span data-stu-id="d928f-134">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="d928f-135">針對不存在的資料行嘗試有條件的索引，也會產生這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="d928f-135">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-136">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="d928f-136">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="d928f-137">嘗試加入重複的資料行。</span><span class="sxs-lookup"><span data-stu-id="d928f-137">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="d928f-138">應該不會有一個以上的自動遞增資料行存在，而且每個資料表都不能有一個以上的版本資料行。</span><span class="sxs-lookup"><span data-stu-id="d928f-138">No more than one autoincrement column should exist, and no more than one version column should exist per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-139">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="d928f-139">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="d928f-140">如果<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>ulDensity</strong>成員設定為小於20或超過100的數位，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="d928f-140">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-141">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="d928f-141">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="d928f-142">表示在<a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>結構的<strong>szTemplateTableName</strong>成員中命名的資料表未標示為樣板資料表 (也就是說，該資料表未設定) 的 JET_bitTableCreateTemplateTable 參數值。</span><span class="sxs-lookup"><span data-stu-id="d928f-142">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure was not marked as a template table (that is, that table did not have the JET_bitTableCreateTemplateTable parameter value set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-143">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="d928f-143">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="d928f-144">嘗試定義兩個相同的索引。</span><span class="sxs-lookup"><span data-stu-id="d928f-144">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-145">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="d928f-145">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="d928f-146">嘗試為數據表指定一個以上的主要索引。</span><span class="sxs-lookup"><span data-stu-id="d928f-146">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="d928f-147">資料表必須只有一個主要索引。</span><span class="sxs-lookup"><span data-stu-id="d928f-147">A table must have exactly one primary index.</span></span> <span data-ttu-id="d928f-148">如果未指定任何主要索引，database engine 將會以透明方式建立一個索引。</span><span class="sxs-lookup"><span data-stu-id="d928f-148">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-149">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="d928f-149">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="d928f-150">指定了不正確索引定義。</span><span class="sxs-lookup"><span data-stu-id="d928f-150">An invalid index definition was specified.</span></span> <span data-ttu-id="d928f-151">以下是此錯誤的一些可能原因：</span><span class="sxs-lookup"><span data-stu-id="d928f-151">The following are some of the possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="d928f-152">主要索引是條件式 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員已設定 JET_bitIndexPrimary 值，而且<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cConditionalColumn</strong>成員大於零) 。</span><span class="sxs-lookup"><span data-stu-id="d928f-152">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexPrimary value set, and the <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="d928f-153">適用于從 Windows Server 2003 開始的 Windows Server 作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="d928f-153">Applies to versions of the Windows Server operating system starting with Windows Server 2003.</span></span> <span data-ttu-id="d928f-154">嘗試建立具有元組限制的元組索引，但未在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構中傳遞<strong>ptuplelimits</strong>成員 (也就是說， <strong>JET_INDEXCREATE2</strong>結構的<strong>grbit</strong>成員已設定 JET_bitIndexTupleLimits 值，但<strong>ptuplelimits</strong>指標為 null) 。</span><span class="sxs-lookup"><span data-stu-id="d928f-154">An attempt to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure (that is, the <strong>grbit</strong> member of the <strong>JET_INDEXCREATE2</strong> structure has JET_bitIndexTupleLimits value set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="d928f-155">在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>szKey</strong>成員中傳入不正確索引鍵定義。</span><span class="sxs-lookup"><span data-stu-id="d928f-155">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="d928f-156">如需有效定義的詳細資訊，請參閱 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>。</span><span class="sxs-lookup"><span data-stu-id="d928f-156">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="d928f-157">將<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>中的<strong>cbVarSegMac</strong>成員設定為大於主要索引的 JET_cbPrimaryKeyMost 值 () 或大於次要索引 JET_cbSecondaryKeyMost 的 (值) 。</span><span class="sxs-lookup"><span data-stu-id="d928f-157">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than the JET_cbPrimaryKeyMost value (for a primary index) or greater than the JET_cbSecondaryKeyMost value (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="d928f-158">傳遞不正確使用者自訂 Unicode 索引組合， (在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構) 的<strong>grbit</strong>成員中設定 JET_bitIndexUnicode 值位的一個。</span><span class="sxs-lookup"><span data-stu-id="d928f-158">Passing an invalid combination for a user-defined Unicode index (one that has the JET_bitIndexUnicode value bit set in the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span> <span data-ttu-id="d928f-159">某些常見的原因包括<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>pidxunicode</strong>成員為 null，或<strong>PIDXUNICODE</strong>結構中指定的 LCID 無效。</span><span class="sxs-lookup"><span data-stu-id="d928f-159">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="d928f-160">指定主要索引的多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="d928f-160">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="d928f-161">正在嘗試編制太多條件式資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="d928f-161">Trying to index too many conditional columns.</span></span> <span data-ttu-id="d928f-162"><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cConditionalColumn</strong>成員不得大於<strong>JET_ccolKeyMost</strong>。</span><span class="sxs-lookup"><span data-stu-id="d928f-162">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-163">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="d928f-163">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="d928f-164">適用于 windows XP 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="d928f-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="d928f-165">已指定 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，但不支援其限制。</span><span class="sxs-lookup"><span data-stu-id="d928f-165">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="d928f-166">如需詳細資訊，請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="d928f-166">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-167">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="d928f-167">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="d928f-168">適用于 windows XP 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="d928f-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="d928f-169">元組索引不可以是唯一的 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<em>grbit</em>成員不能同時設定) 的 JET_bitIndexPrimary 和 JET_bitIndexUnique 值。</span><span class="sxs-lookup"><span data-stu-id="d928f-169">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique values set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-170">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="d928f-170">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="d928f-171">適用于 windows XP 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="d928f-171">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="d928f-172">元組索引只能在單一資料行上 (也就是，如果<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員已設定 JET_bitIndexTuples 值，而且<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>szKey</strong>成員指定了一個以上的資料行) 。</span><span class="sxs-lookup"><span data-stu-id="d928f-172">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has JET_bitIndexTuples value set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-173">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="d928f-173">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="d928f-174">適用于 windows XP 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="d928f-174">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="d928f-175">元組索引不可以是主要索引 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexTuples 設定) 。</span><span class="sxs-lookup"><span data-stu-id="d928f-175">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-176">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="d928f-176">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="d928f-177">適用于 windows XP 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="d928f-177">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="d928f-178">元組索引只能位於 text 或 Unicode 資料行上。</span><span class="sxs-lookup"><span data-stu-id="d928f-178">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="d928f-179">嘗試將其他資料行的索引 (例如二進位資料行) ，將會產生 JET_errIndexTuplesTextColumnsOnly 的回應碼。</span><span class="sxs-lookup"><span data-stu-id="d928f-179">An attempt to index other columns (such as binary columns) will result in a JET_errIndexTuplesTextColumnsOnly response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-180">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="d928f-180">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="d928f-181">適用于 windows XP 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="d928f-181">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="d928f-182">元組索引不允許設定<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbVarSegMac</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="d928f-182">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-183">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="d928f-183">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="d928f-184">嘗試在交易中建立沒有版本資訊的索引。</span><span class="sxs-lookup"><span data-stu-id="d928f-184">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-185">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="d928f-185">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="d928f-186"><a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cp</strong>成員未設定為有效的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="d928f-186">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="d928f-187">Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。</span><span class="sxs-lookup"><span data-stu-id="d928f-187">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="d928f-188">0值表示預設值將使用 (英文、1252) 。</span><span class="sxs-lookup"><span data-stu-id="d928f-188">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-189">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="d928f-189">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="d928f-190"><a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>coltyp</strong>成員未設定為有效的資料行類型。</span><span class="sxs-lookup"><span data-stu-id="d928f-190">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-191">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="d928f-191">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="d928f-192">以下是可能發生此錯誤的一些原因：</span><span class="sxs-lookup"><span data-stu-id="d928f-192">The following are some reasons why this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="d928f-193"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgindexcreate</strong>成員已設定為 null。</span><span class="sxs-lookup"><span data-stu-id="d928f-193">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="d928f-194"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgcolumncreate</strong>成員已設定為 null。</span><span class="sxs-lookup"><span data-stu-id="d928f-194">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to null.</span></span></p></li>
<li><p><span data-ttu-id="d928f-195"><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbStruct</strong>成員未設定為有效的值。</span><span class="sxs-lookup"><span data-stu-id="d928f-195">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-196">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="d928f-196">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="d928f-197">在<a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>結構中指定了不正確<strong>grbit</strong>成員組合。</span><span class="sxs-lookup"><span data-stu-id="d928f-197">An invalid combination of <strong>grbit</strong> members was specified in the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure.</span></span></p>
<p><span data-ttu-id="d928f-198">因為 <strong>grbit</strong> 成員包含不一致的值，所以索引定義無效。</span><span class="sxs-lookup"><span data-stu-id="d928f-198">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="d928f-199">以下是一些可能的原因：</span><span class="sxs-lookup"><span data-stu-id="d928f-199">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="d928f-200">主要索引具有指定的略過位 (也就是說，JET_bitIndexPrimary 值是 JET_bitIndexIgnoreNull、JET_bitIndexIgnoreAnyNull 或 JET_bitIndexIgnoreFirstNull 值) 傳遞。</span><span class="sxs-lookup"><span data-stu-id="d928f-200">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary value was passed with the JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull values).</span></span></p></li>
<li><p><span data-ttu-id="d928f-201">空的索引不會忽略任何 null 成員 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員已設定 JET_bitIndexEmpty 值，但未) JET_bitIndexIgnoreAnyNull 值設定。</span><span class="sxs-lookup"><span data-stu-id="d928f-201">An empty index does not ignore any null members (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has the JET_bitIndexEmpty value set, but does not have JET_bitIndexIgnoreAnyNull value set).</span></span></p></li>
<li><p><span data-ttu-id="d928f-202">傳入具有無效<strong>grbit</strong>成員的<a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>結構。</span><span class="sxs-lookup"><span data-stu-id="d928f-202">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="d928f-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="d928f-204">在 (中傳遞了不正確地區設定識別碼 (LCID) ，方法是透過<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構中的<strong>pidxunicode</strong>成員指向之<a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a>結構的<strong>lcid</strong>成員，或透過<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構) 的<strong>lcid</strong>欄位。</span><span class="sxs-lookup"><span data-stu-id="d928f-204">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure that the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure points to, or through the <strong>lcid</strong> field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-205">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d928f-205">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d928f-206">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="d928f-206">An invalid parameter was given.</span></span> <span data-ttu-id="d928f-207">以下是一些可能的原因：</span><span class="sxs-lookup"><span data-stu-id="d928f-207">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="d928f-208"><a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>結構的<strong>rgcolumncreate</strong>成員為 null。</span><span class="sxs-lookup"><span data-stu-id="d928f-208">The <strong>rgcolumncreate</strong> member of the <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> structure is null.</span></span></p></li>
<li><p><span data-ttu-id="d928f-209"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgcolumncreate</strong>成員中指定的其中一個<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( JET_COLUMNCREATE ) 。</span><span class="sxs-lookup"><span data-stu-id="d928f-209">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="d928f-210"><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbKey</strong>成員設定為零。</span><span class="sxs-lookup"><span data-stu-id="d928f-210">The <strong>cbKey</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="d928f-211"><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( JET_INDEXCREATE2 ) 。</span><span class="sxs-lookup"><span data-stu-id="d928f-211">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof( JET_INDEXCREATE2 ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-212">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="d928f-212">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="d928f-213">記錄太大。</span><span class="sxs-lookup"><span data-stu-id="d928f-213">The record is too big.</span></span> <span data-ttu-id="d928f-214">所有固定資料行之<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cbMax</strong>成員總和不得超過某個值。</span><span class="sxs-lookup"><span data-stu-id="d928f-214">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-215">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="d928f-215">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="d928f-216">資料表已經存在。</span><span class="sxs-lookup"><span data-stu-id="d928f-216">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-217">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="d928f-217">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="d928f-218">嘗試將過多的資料行新增至資料表。</span><span class="sxs-lookup"><span data-stu-id="d928f-218">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="d928f-219">資料表不能超過 <strong>JET_ccolFixedMost</strong> 固定資料行，不能超過 <strong>JET_ccolVarMost</strong> 的可變長度資料行，且不能超過 <strong>JET_ccolTaggedMost</strong> 標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="d928f-219">A table can have no more than <strong>JET_ccolFixedMost</strong> fixed columns, no more than <strong>JET_ccolVarMost</strong> variable-length columns, and no more than <strong>JET_ccolTaggedMost</strong> tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-220">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="d928f-220">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="d928f-221">嘗試將 Unicode 資料行正規化時，發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="d928f-221">An error occurred when an attempt was made to normalize a Unicode column.</span></span> <span data-ttu-id="d928f-222">這可能是因為系統資源不足所造成。</span><span class="sxs-lookup"><span data-stu-id="d928f-222">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-223">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="d928f-223">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="d928f-224">JET 空間提示結構的元素不正確或可採取動作。</span><span class="sxs-lookup"><span data-stu-id="d928f-224">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="d928f-225">備註</span><span class="sxs-lookup"><span data-stu-id="d928f-225">Remarks</span></span>

<span data-ttu-id="d928f-226">**JetCreateTableColumnIndex4W** 函式會建立一個資料表，其中包含一組初始的資料行和索引。</span><span class="sxs-lookup"><span data-stu-id="d928f-226">The **JetCreateTableColumnIndex4W** function creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="d928f-227">您可以透過 [JetAddColumn](./jetaddcolumn-function.md)、 [JetDeleteColumn](./jetdeletecolumn-function.md)、 [JetDeleteColumn2](./jetdeletecolumn2-function.md)、 [JetCreateIndex](./jetcreateindex-function.md)、 [JetCreateIndex2](./jetcreateindex2-function.md)、 [JetCreateIndex3](./jetcreateindex3-function.md)、 [JetCreateIndex4W](./jetcreateindex4w-function.md)和 [JetDeleteIndex](./jetdeleteindex-function.md) 函數，以動態方式加入和移除其他資料行和索引。</span><span class="sxs-lookup"><span data-stu-id="d928f-227">Additional columns and indexes can be added and removed dynamically by means of the [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md) functions.</span></span>

<span data-ttu-id="d928f-228">如同 [JetOpenTable](./jetopentable-function.md) 函式，當應用程式使用傳回的 *tableid* 完成時， [JetCloseTable](./jetclosetable-function.md) 函式應該會關閉應用程式。</span><span class="sxs-lookup"><span data-stu-id="d928f-228">As with the [JetOpenTable](./jetopentable-function.md) function, when the application is done using the returned *tableid*, the [JetCloseTable](./jetclosetable-function.md) function should close the application.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d928f-229">規格需求</span><span class="sxs-lookup"><span data-stu-id="d928f-229">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d928f-230"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="d928f-230"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d928f-231">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="d928f-231">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-232"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="d928f-232"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d928f-233">需要 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="d928f-233">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-234"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="d928f-234"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d928f-235">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="d928f-235">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d928f-236"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="d928f-236"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d928f-237">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="d928f-237">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d928f-238"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d928f-238"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d928f-239">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="d928f-239">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d928f-240">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d928f-240">See also</span></span>

[<span data-ttu-id="d928f-241">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="d928f-241">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="d928f-242">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="d928f-242">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="d928f-243">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d928f-243">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d928f-244">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d928f-244">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d928f-245">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="d928f-245">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="d928f-246">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="d928f-246">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="d928f-247">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d928f-247">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d928f-248">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d928f-248">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d928f-249">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="d928f-249">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="d928f-250">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="d928f-250">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)  
[<span data-ttu-id="d928f-251">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="d928f-251">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="d928f-252">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="d928f-252">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="d928f-253">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="d928f-253">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="d928f-254">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="d928f-254">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="d928f-255">JetCreateIndex3</span><span class="sxs-lookup"><span data-stu-id="d928f-255">JetCreateIndex3</span></span>](./jetcreateindex3-function.md)  
[<span data-ttu-id="d928f-256">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="d928f-256">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="d928f-257">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="d928f-257">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="d928f-258">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="d928f-258">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="d928f-259">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="d928f-259">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
