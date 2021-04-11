---
description: 深入瞭解： JetCreateTableColumnIndex2 函數
title: JetCreateTableColumnIndex2 函式
TOCTitle: JetCreateTableColumnIndex2 Function
ms:assetid: ad9caaf3-8cd2-453f-894d-8ac438c50b73
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294057(v=EXCHG.10)
ms:contentKeyID: 32765672
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex2W
- JetCreateTableColumnIndex2
- JetCreateTableColumnIndex2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51a1789fe050ddd62990f6561ddeb01363d69f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027553"
---
# <a name="jetcreatetablecolumnindex2-function"></a><span data-ttu-id="17a39-103">JetCreateTableColumnIndex2 函式</span><span class="sxs-lookup"><span data-stu-id="17a39-103">JetCreateTableColumnIndex2 Function</span></span>


<span data-ttu-id="17a39-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="17a39-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreatetablecolumnindex2-function"></a><span data-ttu-id="17a39-105">JetCreateTableColumnIndex2 函式</span><span class="sxs-lookup"><span data-stu-id="17a39-105">JetCreateTableColumnIndex2 Function</span></span>

<span data-ttu-id="17a39-106">**JetCreateTableColumnIndex2** 函式會在 ESE 資料庫中建立一個資料表，其中包含一組初始的索引，以及一組 [JET_TABLECREATE2](./jet-tablecreate2-structure.md)結構陣列的初始資料行。</span><span class="sxs-lookup"><span data-stu-id="17a39-106">The **JetCreateTableColumnIndex2** function creates a table in an ESE database with an initial set of indexes and an initial set of columns from an array of [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structures.</span></span> <span data-ttu-id="17a39-107">[JET_TABLECREATE2](./jet-tablecreate2-structure.md)結構允許指定回呼函數。</span><span class="sxs-lookup"><span data-stu-id="17a39-107">The [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure allows a callback function to be specified.</span></span>

<span data-ttu-id="17a39-108">**Windows xp： JetCreateTableColumnIndex2** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="17a39-108">**Windows XP:  JetCreateTableColumnIndex2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex2(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE2* ptablecreate
    );
```

### <a name="parameters"></a><span data-ttu-id="17a39-109">參數</span><span class="sxs-lookup"><span data-stu-id="17a39-109">Parameters</span></span>

<span data-ttu-id="17a39-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="17a39-110">*sesid*</span></span>

<span data-ttu-id="17a39-111">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="17a39-111">The database session context to use for the API call.</span></span>

<span data-ttu-id="17a39-112">*dbid*</span><span class="sxs-lookup"><span data-stu-id="17a39-112">*dbid*</span></span>

<span data-ttu-id="17a39-113">用於 API 呼叫的資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="17a39-113">The database identifier to use for the API call.</span></span>

<span data-ttu-id="17a39-114">*ptablecreate*</span><span class="sxs-lookup"><span data-stu-id="17a39-114">*ptablecreate*</span></span>

<span data-ttu-id="17a39-115">[JET_TABLECREATE2](./jet-tablecreate2-structure.md)結構的指標，此結構會定義要建立的資料表。</span><span class="sxs-lookup"><span data-stu-id="17a39-115">A pointer to a [JET_TABLECREATE2](./jet-tablecreate2-structure.md) structure which defines the table to be created.</span></span> <span data-ttu-id="17a39-116">如需詳細資訊，請參閱 [JET_TABLECREATE2](./jet-tablecreate2-structure.md) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-116">See [JET_TABLECREATE2](./jet-tablecreate2-structure.md) for more details.</span></span>

### <a name="return-value"></a><span data-ttu-id="17a39-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="17a39-117">Return Value</span></span>

<span data-ttu-id="17a39-118">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="17a39-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="17a39-119">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="17a39-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="17a39-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="17a39-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="17a39-121">Description</span><span class="sxs-lookup"><span data-stu-id="17a39-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17a39-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="17a39-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="17a39-123">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="17a39-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-124">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="17a39-124">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="17a39-125">無法解析回呼函數。</span><span class="sxs-lookup"><span data-stu-id="17a39-125">The callback function could not be resolved.</span></span> <span data-ttu-id="17a39-126">可能找不到 DLL，或可能找不到 DLL 中的函數。</span><span class="sxs-lookup"><span data-stu-id="17a39-126">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="17a39-127">啟用足夠記錄之後，事件記錄檔將會提供更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="17a39-127">With sufficient logging enabled, the event log will provide more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-128">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="17a39-128">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="17a39-129">嘗試透過「正在進行」（update）或 SLV 資料行來編制索引， (請注意，SLV 資料行已被取代) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-129">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-130">JET_errCannotNestDDL</span><span class="sxs-lookup"><span data-stu-id="17a39-130">JET_errCannotNestDDL</span></span></p></td>
<td><p><span data-ttu-id="17a39-131">如果 ptablecreate- &gt; grbit 指定 JET_bitTableCreateTemplateTable，但 ptablecreate- &gt; szTemplateTableName 設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="17a39-131">If ptablecreate-&gt;grbit specifies JET_bitTableCreateTemplateTable, but ptablecreate-&gt;szTemplateTableName is set to NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-132">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="17a39-132">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="17a39-133">資料行已經存在。</span><span class="sxs-lookup"><span data-stu-id="17a39-133">A column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-134">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="17a39-134">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="17a39-135">嘗試在不存在的資料行上建立索引。</span><span class="sxs-lookup"><span data-stu-id="17a39-135">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="17a39-136">嘗試在不存在的資料行上有條件地編制索引，也會產生這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="17a39-136">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-137">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="17a39-137">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="17a39-138">嘗試加入重複的資料行。</span><span class="sxs-lookup"><span data-stu-id="17a39-138">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="17a39-139">應該不會有一個以上的自動遞增資料行，而且每個資料表不能有一個以上的版本資料行。</span><span class="sxs-lookup"><span data-stu-id="17a39-139">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-140">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="17a39-140">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="17a39-141">如果<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>ulDensity</strong>成員設定為小於20或超過100的數位，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="17a39-141">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-142">JET_errDDLNotInheritable</span><span class="sxs-lookup"><span data-stu-id="17a39-142">JET_errDDLNotInheritable</span></span></p></td>
<td><p><span data-ttu-id="17a39-143">表示<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>結構的<strong>szTemplateTableName</strong>成員中所命名的資料表不是標示為樣板資料表 (也就是說，該資料表沒有 JET_bitTableCreateTemplateTable 設定) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-143">Signifies that the table named in the <strong>szTemplateTableName</strong> member of the <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> structure was not a marked as a template table (that is, that table did not have JET_bitTableCreateTemplateTable set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-144">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="17a39-144">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="17a39-145">嘗試定義兩個相同的索引。</span><span class="sxs-lookup"><span data-stu-id="17a39-145">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-146">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="17a39-146">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="17a39-147">嘗試為數據表指定一個以上的主要索引。</span><span class="sxs-lookup"><span data-stu-id="17a39-147">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="17a39-148">資料表必須只有一個主要索引。</span><span class="sxs-lookup"><span data-stu-id="17a39-148">A table must have exactly one primary index.</span></span> <span data-ttu-id="17a39-149">如果未指定任何主要索引，database engine 將會以透明方式建立一個索引。</span><span class="sxs-lookup"><span data-stu-id="17a39-149">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-150">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="17a39-150">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="17a39-151">指定了不正確索引定義。</span><span class="sxs-lookup"><span data-stu-id="17a39-151">An invalid index definition was specified.</span></span> <span data-ttu-id="17a39-152">收到此錯誤的部分可能原因包括：</span><span class="sxs-lookup"><span data-stu-id="17a39-152">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="17a39-153">主要索引是條件式 (也就是， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexPrimary 設定，而<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cConditionalColumn</strong>成員大於零) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-153">A primary index is conditional (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexPrimary set, and <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="17a39-154">Windows Server 2003 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="17a39-154">Windows Server 2003 and later.</span></span> <span data-ttu-id="17a39-155">嘗試建立具有元組限制的元組索引，但未在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構中傳遞<strong>ptuplelimits</strong>成員 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexTupleLimits 設定，但<strong>ptuplelimits</strong>指標為 Null) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-155">Attempting to create a tuple index with tuple limits, but without passing the <strong>ptuplelimits</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="17a39-156">在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>szKey</strong>成員中傳入不正確索引鍵定義。</span><span class="sxs-lookup"><span data-stu-id="17a39-156">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="17a39-157">如需有效定義的討論，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</span><span class="sxs-lookup"><span data-stu-id="17a39-157">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="17a39-158">將<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>中的<strong>cbVarSegMac</strong>成員設定為大於主要索引的 JET_cbPrimaryKeyMost () 或大於次要索引 JET_cbSecondaryKeyMost 的 () 。</span><span class="sxs-lookup"><span data-stu-id="17a39-158">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="17a39-159">傳遞不正確使用者定義 Unicode 索引組合， (在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>) 的<strong>grbit</strong>成員中設定 JET_bitIndexUnicode 位。</span><span class="sxs-lookup"><span data-stu-id="17a39-159">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="17a39-160">某些常見的原因包括<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>PIDXUNICODE</strong>成員為 Null，或<strong>PIDXUNICODE</strong>結構中指定的 LCID 無效。</span><span class="sxs-lookup"><span data-stu-id="17a39-160">Some common causes include the <strong>pidxunicode</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the <strong>pidxunicode</strong> structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="17a39-161">指定主要索引的多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="17a39-161">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="17a39-162">正在嘗試編制太多條件式資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="17a39-162">Trying to index too many conditional columns.</span></span> <span data-ttu-id="17a39-163"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cConditionalColumn</strong>成員不得大於 JET_ccolKeyMost。</span><span class="sxs-lookup"><span data-stu-id="17a39-163">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-164">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="17a39-164">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="17a39-165">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="17a39-165">Windows XP and later.</span></span> <span data-ttu-id="17a39-166">已指定 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，但不支援其限制。</span><span class="sxs-lookup"><span data-stu-id="17a39-166">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="17a39-167">請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="17a39-167">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-168">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="17a39-168">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="17a39-169">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="17a39-169">Windows XP and later.</span></span> <span data-ttu-id="17a39-170">元組索引不可以是唯一的 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<em>grbit</em>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexUnique 設定) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-170">A tuple index cannot be unique (that is, the <em>grbit</em> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-171">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="17a39-171">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="17a39-172">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="17a39-172">Windows XP and later.</span></span> <span data-ttu-id="17a39-173">元組索引只能在單一資料行上 (也就是，如果<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已設定 JET_bitIndexTuples，且<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>szKey</strong>成員指定了一個以上的資料行) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-173">A tuple index can only be over a single column (that is, if the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-174">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="17a39-174">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="17a39-175">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="17a39-175">Windows XP and later.</span></span> <span data-ttu-id="17a39-176">元組索引不可以是主要索引 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexTuples 設定) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-176">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-177">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="17a39-177">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="17a39-178">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="17a39-178">Windows XP and later.</span></span> <span data-ttu-id="17a39-179">元組索引只能位於 text 或 Unicode 資料行上。</span><span class="sxs-lookup"><span data-stu-id="17a39-179">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="17a39-180">嘗試將其他資料行的索引 (例如二進位資料行) 會導致 JET_errIndexTuplesTextColumnsOnly。</span><span class="sxs-lookup"><span data-stu-id="17a39-180">An attempt to index other columns (such as binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-181">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="17a39-181">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="17a39-182">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="17a39-182">Windows XP and later.</span></span> <span data-ttu-id="17a39-183">元組索引不允許設定<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbVarSegMac</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="17a39-183">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-184">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="17a39-184">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="17a39-185">嘗試在交易中建立沒有版本資訊的索引。</span><span class="sxs-lookup"><span data-stu-id="17a39-185">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-186">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="17a39-186">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="17a39-187"><a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cp</strong>成員未設定為有效的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="17a39-187">The <strong>cp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="17a39-188">Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-188">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="17a39-189">0值表示預設值將使用 (英文、1252) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-189">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-190">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="17a39-190">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="17a39-191"><a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>coltyp</strong>成員未設定為有效的資料行類型。</span><span class="sxs-lookup"><span data-stu-id="17a39-191">The <strong>coltyp</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-192">JET_errInvalidCreateIndex</span><span class="sxs-lookup"><span data-stu-id="17a39-192">JET_errInvalidCreateIndex</span></span></p></td>
<td><p><span data-ttu-id="17a39-193">可能會發生此錯誤的部分原因：</span><span class="sxs-lookup"><span data-stu-id="17a39-193">Some of the reasons this error may occur:</span></span></p>
<ul>
<li><p><span data-ttu-id="17a39-194"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgindexcreate</strong>成員已設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="17a39-194">The <strong>rgindexcreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="17a39-195"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgcolumncreate</strong>成員已設定為 Null。</span><span class="sxs-lookup"><span data-stu-id="17a39-195">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was set to NULL.</span></span></p></li>
<li><p><span data-ttu-id="17a39-196"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbStruct</strong>成員未設定為有效的值。</span><span class="sxs-lookup"><span data-stu-id="17a39-196">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure was not set to a valid value.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="17a39-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="17a39-198"><a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>或<a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>中指定了不正確<strong>grbit</strong>成員組合。</span><span class="sxs-lookup"><span data-stu-id="17a39-198">An invalid combination of <strong>grbit</strong> members was specified in <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> or <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>.</span></span></p>
<p><span data-ttu-id="17a39-199">因為 <strong>grbit</strong> 成員包含不一致的值，所以索引定義無效。</span><span class="sxs-lookup"><span data-stu-id="17a39-199">The index definition is invalid because the <strong>grbit</strong> member contains inconsistent values.</span></span> <span data-ttu-id="17a39-200">可能的原因如下：</span><span class="sxs-lookup"><span data-stu-id="17a39-200">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="17a39-201">主要索引具有指定的略過位 (也就是，JET_bitIndexPrimary 是以 JET_bitIndexIgnoreNull、JET_bitIndexIgnoreAnyNull 或 JET_bitIndexIgnoreFirstNull) 傳遞。</span><span class="sxs-lookup"><span data-stu-id="17a39-201">A primary index had an ignore bit specified (that is, JET_bitIndexPrimary was passed with JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="17a39-202">空白索引不會忽略任何 Null 成員 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexEmpty 設定，但沒有 JET_bitIndexIgnoreAnyNull 設定) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-202">An empty index does not ignore any NULL members (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="17a39-203">傳入具有無效<strong>grbit</strong>成員的<a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>結構。</span><span class="sxs-lookup"><span data-stu-id="17a39-203">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-204">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="17a39-204">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="17a39-205">在 (中傳遞不正確地區設定識別碼 (LCID) ，方法是透過<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構中的<strong>pidxunicode</strong>成員所指向的<a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a>結構的<strong>lcid</strong>成員，或透過<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構) 的<strong>lcid</strong>欄位來傳遞。</span><span class="sxs-lookup"><span data-stu-id="17a39-205">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member of the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure which is pointed to by the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure, or through the <strong>lcid</strong> field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-206">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="17a39-206">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="17a39-207">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="17a39-207">An invalid parameter was given.</span></span> <span data-ttu-id="17a39-208">可能的原因如下：</span><span class="sxs-lookup"><span data-stu-id="17a39-208">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="17a39-209"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>RGCOLUMNCREATE</strong>成員為 Null。</span><span class="sxs-lookup"><span data-stu-id="17a39-209">The <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure is NULL.</span></span></p></li>
<li><p><span data-ttu-id="17a39-210"><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgcolumncreate</strong>成員中指定的其中一個<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( JET_COLUMNCREATE ) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-210">The <strong>cbStruct</strong> member of one of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structures given in the <strong>rgcolumncreate</strong> member of the <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> structure was not set to sizeof( JET_COLUMNCREATE ).</span></span></p></li>
<li><p><span data-ttu-id="17a39-211"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbKey</strong>成員設定為零。</span><span class="sxs-lookup"><span data-stu-id="17a39-211">The <strong>cbKey</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="17a39-212"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( JET_INDEXCREATE ) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-212">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof( JET_INDEXCREATE ).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-213">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="17a39-213">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="17a39-214">記錄太大。</span><span class="sxs-lookup"><span data-stu-id="17a39-214">The record is too big.</span></span> <span data-ttu-id="17a39-215">所有固定資料行之<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cbMax</strong>成員總和不得超過某個值。</span><span class="sxs-lookup"><span data-stu-id="17a39-215">The sum of the <strong>cbMax</strong> member of the <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> structure for all fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-216">JET_errTableDuplicate</span><span class="sxs-lookup"><span data-stu-id="17a39-216">JET_errTableDuplicate</span></span></p></td>
<td><p><span data-ttu-id="17a39-217">資料表已經存在。</span><span class="sxs-lookup"><span data-stu-id="17a39-217">The table already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-218">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="17a39-218">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="17a39-219">嘗試將過多的資料行新增至資料表。</span><span class="sxs-lookup"><span data-stu-id="17a39-219">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="17a39-220">資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="17a39-220">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-221">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="17a39-221">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="17a39-222">嘗試將 Unicode 資料行正規化時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="17a39-222">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="17a39-223">這可能是因為系統資源不足所造成。</span><span class="sxs-lookup"><span data-stu-id="17a39-223">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="17a39-224">備註</span><span class="sxs-lookup"><span data-stu-id="17a39-224">Remarks</span></span>

<span data-ttu-id="17a39-225">名稱 **JetCreateTableColumnIndex2** 來自物件的建立順序：它會先建立資料表、資料行，最後再建立索引。</span><span class="sxs-lookup"><span data-stu-id="17a39-225">The name **JetCreateTableColumnIndex2** comes from the order of creation of the objects: It first creates a table, columns, and then finally indexes.</span></span> <span data-ttu-id="17a39-226">**JetCreateTableColumnIndex2** 會建立一份資料表，其中包含一組初始的資料行和索引。</span><span class="sxs-lookup"><span data-stu-id="17a39-226">**JetCreateTableColumnIndex2** creates a table with an initial set of columns and indexes.</span></span> <span data-ttu-id="17a39-227">您可以使用 [JetAddColumn](./jetaddcolumn-function.md)、 [JetDeleteColumn](./jetdeletecolumn-function.md)、 [JetDeleteColumn2](./jetdeletecolumn2-function.md)、 [JetCreateIndex](./jetcreateindex-function.md)、 [JetCreateIndex2](./jetcreateindex2-function.md)和 [JetDeleteIndex](./jetdeleteindex-function.md)，動態地新增和移除其他資料行和索引。</span><span class="sxs-lookup"><span data-stu-id="17a39-227">Additional columns and indexes can be added and removed dynamically with [JetAddColumn](./jetaddcolumn-function.md), [JetDeleteColumn](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [JetCreateIndex](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), and [JetDeleteIndex](./jetdeleteindex-function.md).</span></span>

<span data-ttu-id="17a39-228">如同 [JetOpenTable](./jetopentable-function.md)，當應用程式使用傳回的 *tableid* 完成時，通常應該會以 [JetCloseTable](./jetclosetable-function.md)來關閉它。</span><span class="sxs-lookup"><span data-stu-id="17a39-228">Like [JetOpenTable](./jetopentable-function.md), when the application is done using the returned *tableid*, it should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="17a39-229">規格需求</span><span class="sxs-lookup"><span data-stu-id="17a39-229">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17a39-230"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="17a39-230"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="17a39-231">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="17a39-231">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-232"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="17a39-232"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="17a39-233">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="17a39-233">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-234"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="17a39-234"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="17a39-235">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="17a39-235">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-236"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="17a39-236"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="17a39-237">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="17a39-237">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17a39-238"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="17a39-238"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="17a39-239">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="17a39-239">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17a39-240"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="17a39-240"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="17a39-241">實作為 <strong>JetCreateTableColumnIndex2W</strong> (Unicode) 和 <strong>JetCreateTableColumnIndex2A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="17a39-241">Implemented as <strong>JetCreateTableColumnIndex2W</strong> (Unicode) and <strong>JetCreateTableColumnIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="17a39-242">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17a39-242">See Also</span></span>

[<span data-ttu-id="17a39-243">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="17a39-243">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="17a39-244">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="17a39-244">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="17a39-245">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="17a39-245">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="17a39-246">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="17a39-246">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="17a39-247">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="17a39-247">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="17a39-248">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="17a39-248">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="17a39-249">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="17a39-249">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="17a39-250">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="17a39-250">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="17a39-251">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="17a39-251">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="17a39-252">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="17a39-252">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="17a39-253">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="17a39-253">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="17a39-254">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="17a39-254">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="17a39-255">JetCreateIndex2</span><span class="sxs-lookup"><span data-stu-id="17a39-255">JetCreateIndex2</span></span>](./jetcreateindex2-function.md)  
[<span data-ttu-id="17a39-256">JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="17a39-256">JetCreateTable</span></span>](./jetcreatetable-function.md)  
[<span data-ttu-id="17a39-257">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="17a39-257">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="17a39-258">JetDeleteColumn</span><span class="sxs-lookup"><span data-stu-id="17a39-258">JetDeleteColumn</span></span>](./jetdeletecolumn-function.md)  
[<span data-ttu-id="17a39-259">JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="17a39-259">JetDeleteColumn2</span></span>](./jetdeletecolumn2-function.md)
