---
description: 深入瞭解： JetCreateIndex2 函數
title: JetCreateIndex2 函式
TOCTitle: JetCreateIndex2 Function
ms:assetid: 8810eaed-40cb-4561-aafc-9a9bbdb0d05b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269324(v=EXCHG.10)
ms:contentKeyID: 32765614
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex2W
- JetCreateIndex2A
- JetCreateIndex2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42c1eb8fa1bb7fa880cf7286a1ec472ddc7ba7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971512"
---
# <a name="jetcreateindex2-function"></a><span data-ttu-id="0f75c-103">JetCreateIndex2 函式</span><span class="sxs-lookup"><span data-stu-id="0f75c-103">JetCreateIndex2 Function</span></span>


<span data-ttu-id="0f75c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0f75c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateindex2-function"></a><span data-ttu-id="0f75c-105">JetCreateIndex2 函式</span><span class="sxs-lookup"><span data-stu-id="0f75c-105">JetCreateIndex2 Function</span></span>

<span data-ttu-id="0f75c-106">**JetCreateIndex2** 函式會在 ESE 資料庫中建立資料的索引，可用來快速找出特定資料。</span><span class="sxs-lookup"><span data-stu-id="0f75c-106">The **JetCreateIndex2** function creates indexes over data in an ESE database, which can be used to locate specific data quickly.</span></span>

```cpp
    JET_ERR JET_API JetCreateIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a><span data-ttu-id="0f75c-107">參數</span><span class="sxs-lookup"><span data-stu-id="0f75c-107">Parameters</span></span>

<span data-ttu-id="0f75c-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="0f75c-108">*sesid*</span></span>

<span data-ttu-id="0f75c-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="0f75c-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="0f75c-110">*tableid*</span><span class="sxs-lookup"><span data-stu-id="0f75c-110">*tableid*</span></span>

<span data-ttu-id="0f75c-111">將在其上建立索引的資料表。</span><span class="sxs-lookup"><span data-stu-id="0f75c-111">The table on which the index will be created.</span></span>

<span data-ttu-id="0f75c-112">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="0f75c-112">*pindexcreate*</span></span>

<span data-ttu-id="0f75c-113">[JET_INDEXCREATE](./jet-indexcreate-structure.md)結構的陣列，其中每個結構會定義要建立的索引。</span><span class="sxs-lookup"><span data-stu-id="0f75c-113">An array of [JET_INDEXCREATE](./jet-indexcreate-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="0f75c-114">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="0f75c-114">*cIndexCreate*</span></span>

<span data-ttu-id="0f75c-115">*Pindexcreate* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="0f75c-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="0f75c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f75c-116">Return Value</span></span>

<span data-ttu-id="0f75c-117">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="0f75c-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0f75c-118">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="0f75c-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0f75c-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0f75c-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="0f75c-120">Description</span><span class="sxs-lookup"><span data-stu-id="0f75c-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0f75c-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0f75c-122">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="0f75c-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f75c-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="0f75c-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="0f75c-124">嘗試透過「正在進行」（update）或 SLV 資料行來編制索引， (請注意，SLV 資料行已被取代) 。</span><span class="sxs-lookup"><span data-stu-id="0f75c-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="0f75c-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="0f75c-126">嘗試在不存在的資料行上建立索引。</span><span class="sxs-lookup"><span data-stu-id="0f75c-126">An attempt was made to index over a non-existent column.</span></span> <span data-ttu-id="0f75c-127">嘗試在不存在的資料行上有條件地編制索引，也會產生這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="0f75c-127">Attempting to conditionally index over a non-existent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f75c-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="0f75c-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="0f75c-129">如果<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>ulDensity</strong>成員設定為小於20或超過100的數位，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="0f75c-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to a number less than 20 or more than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="0f75c-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="0f75c-131">嘗試定義兩個相同的索引。</span><span class="sxs-lookup"><span data-stu-id="0f75c-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f75c-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="0f75c-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="0f75c-133">嘗試為數據表指定一個以上的主要索引。</span><span class="sxs-lookup"><span data-stu-id="0f75c-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="0f75c-134">資料表必須只有一個主要索引。</span><span class="sxs-lookup"><span data-stu-id="0f75c-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="0f75c-135">如果未指定任何主要索引，database engine 將會以透明方式建立一個索引。</span><span class="sxs-lookup"><span data-stu-id="0f75c-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="0f75c-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="0f75c-137">指定了不正確索引定義。</span><span class="sxs-lookup"><span data-stu-id="0f75c-137">An invalid index definition was specified.</span></span> <span data-ttu-id="0f75c-138">收到此錯誤的部分可能原因包括：</span><span class="sxs-lookup"><span data-stu-id="0f75c-138">Some of the possible reasons for receiving this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="0f75c-139">主要索引是條件式 (<strong>grbit</strong>成員<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>已 JET_bitIndexPrimary 設定，而<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>的<strong>cConditionalColumn</strong>成員大於零) 。</span><span class="sxs-lookup"><span data-stu-id="0f75c-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> has JET_bitIndexPrimary set, and the <strong>cConditionalColumn</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="0f75c-140">Windows Server 2003 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="0f75c-140">Windows Server 2003 and later.</span></span> <span data-ttu-id="0f75c-141">嘗試建立具有元組限制的元組索引，但未在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>中傳遞<strong>ptuplelimits</strong>成員的資訊 (亦即， <em>grbit</em>已 JET_bitIndexTupleLimits 設定，但<strong>ptuplelimits</strong>指標為 Null) 。</span><span class="sxs-lookup"><span data-stu-id="0f75c-141">Attempting to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (that is, <em>grbit</em> has JET_bitIndexTupleLimits set, but the <strong>ptuplelimits</strong> pointer is NULL).</span></span></p></li>
<li><p><span data-ttu-id="0f75c-142">在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>szKey</strong>成員中傳入不正確索引鍵定義。</span><span class="sxs-lookup"><span data-stu-id="0f75c-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure.</span></span> <span data-ttu-id="0f75c-143">如需有效定義的討論，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</span><span class="sxs-lookup"><span data-stu-id="0f75c-143">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for a discussion of valid definitions.</span></span></p></li>
<li><p><span data-ttu-id="0f75c-144">將<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>中的<strong>cbVarSegMac</strong>成員設定為大於主要索引的 JET_cbPrimaryKeyMost () 或大於次要索引 JET_cbSecondaryKeyMost 的 () 。</span><span class="sxs-lookup"><span data-stu-id="0f75c-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> to be greater than JET_cbPrimaryKeyMost (for a primary index) or greater than JET_cbSecondaryKeyMost (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="0f75c-145">傳遞不正確使用者定義 Unicode 索引組合， (在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>) 的<strong>grbit</strong>成員中設定 JET_bitIndexUnicode 位。</span><span class="sxs-lookup"><span data-stu-id="0f75c-145">Passing an invalid combination for a user-defined Unicode index (one which has the JET_bitIndexUnicode bit set in the <strong>grbit</strong> member of <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>).</span></span> <span data-ttu-id="0f75c-146">常見的原因可能是 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 結構的 pidxunicode 欄位為 Null，或 pidxunicode 結構中指定的 LCID 無效。</span><span class="sxs-lookup"><span data-stu-id="0f75c-146">Some common causes may be that the pidxunicode field of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is NULL, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="0f75c-147">指定主要索引的多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="0f75c-147">Specifying a multi-valued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="0f75c-148">正在嘗試編制太多條件式資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="0f75c-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="0f75c-149"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cConditionalColumn</strong>成員不得大於 JET_ccolKeyMost。</span><span class="sxs-lookup"><span data-stu-id="0f75c-149">The <strong>cConditionalColumn</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not be greater than JET_ccolKeyMost.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f75c-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="0f75c-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="0f75c-151">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="0f75c-151">Windows XP and later.</span></span> <span data-ttu-id="0f75c-152">已指定 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，但不支援其限制。</span><span class="sxs-lookup"><span data-stu-id="0f75c-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="0f75c-153">請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="0f75c-153">See the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="0f75c-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="0f75c-155">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="0f75c-155">Windows XP and later.</span></span> <span data-ttu-id="0f75c-156">元組索引不可以是唯一的 (<em>grbit</em> 不能同時有 JET_bitIndexTuples 和 JET_bitIndexUnique 設定) 。</span><span class="sxs-lookup"><span data-stu-id="0f75c-156">A tuple index cannot be unique (<em>grbit</em> must not have both JET_bitIndexTuples and JET_bitIndexUnique set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f75c-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="0f75c-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="0f75c-158">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="0f75c-158">Windows XP and later.</span></span> <span data-ttu-id="0f75c-159">元組索引只能在單一資料行上 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexTuples 設定，而<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>szKey</strong>成員指定了一個以上的資料行) 。</span><span class="sxs-lookup"><span data-stu-id="0f75c-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexTuples set, and the <strong>szKey</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="0f75c-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="0f75c-161">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="0f75c-161">Windows XP and later.</span></span> <span data-ttu-id="0f75c-162">元組索引不可以是主要索引 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexTuples 設定) 。</span><span class="sxs-lookup"><span data-stu-id="0f75c-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure must not have both JET_bitIndexPrimary and JET_bitIndexTuples set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f75c-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="0f75c-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="0f75c-164">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="0f75c-164">Windows XP and later.</span></span> <span data-ttu-id="0f75c-165">元組索引只能位於 text 或 Unicode 資料行上。</span><span class="sxs-lookup"><span data-stu-id="0f75c-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="0f75c-166">嘗試將其他資料行索引 (例如，二進位資料行) 將會導致 JET_errIndexTuplesTextColumnsOnly。</span><span class="sxs-lookup"><span data-stu-id="0f75c-166">An attempt to index other columns (for example, binary columns) will result in JET_errIndexTuplesTextColumnsOnly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="0f75c-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="0f75c-168">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="0f75c-168">Windows XP and later.</span></span> <span data-ttu-id="0f75c-169">元組索引不允許設定<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbVarSegMac</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="0f75c-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f75c-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="0f75c-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="0f75c-171">嘗試在交易中建立沒有版本資訊的索引。</span><span class="sxs-lookup"><span data-stu-id="0f75c-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="0f75c-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="0f75c-173">因為<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員包含不一致的值，所以索引定義無效。</span><span class="sxs-lookup"><span data-stu-id="0f75c-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure contains inconsistent values.</span></span> <span data-ttu-id="0f75c-174">可能的原因如下：</span><span class="sxs-lookup"><span data-stu-id="0f75c-174">Some possible reasons are:</span></span></p>
<ul>
<li><p><span data-ttu-id="0f75c-175">主要索引具有指定的略過位 (JET_bitIndexPrimary 以 JET_bitIndexIgnoreNull、JET_bitIndexIgnoreAnyNull 或 JET_bitIndexIgnoreFirstNull) 之一傳遞。</span><span class="sxs-lookup"><span data-stu-id="0f75c-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull, or JET_bitIndexIgnoreFirstNull).</span></span></p></li>
<li><p><span data-ttu-id="0f75c-176">空白索引不會忽略任何 NULL 欄位 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexEmpty 設定，但沒有 JET_bitIndexIgnoreAnyNull 設定) 。</span><span class="sxs-lookup"><span data-stu-id="0f75c-176">An empty index does not ignore any NULL fields (that is, <strong>grbit</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure has JET_bitIndexEmpty set, but does not have JET_bitIndexIgnoreAnyNull set).</span></span></p></li>
<li><p><span data-ttu-id="0f75c-177">傳入具有無效<strong>grbit</strong>成員的<a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>結構。</span><span class="sxs-lookup"><span data-stu-id="0f75c-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="0f75c-178">請參閱 <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>。</span><span class="sxs-lookup"><span data-stu-id="0f75c-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="0f75c-179">當您一次建立多個索引時 (也就是說，如果 <em>cIndexCreate</em> 參數大於一個) ，則沒有任何索引可以包含下列任何位：</span><span class="sxs-lookup"><span data-stu-id="0f75c-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="0f75c-180">JET_bitIndexPrimary</span><span class="sxs-lookup"><span data-stu-id="0f75c-180">JET_bitIndexPrimary</span></span></p></li>
<li><p><span data-ttu-id="0f75c-181">JET_bitIndexUnversioned</span><span class="sxs-lookup"><span data-stu-id="0f75c-181">JET_bitIndexUnversioned</span></span></p></li>
<li><p><span data-ttu-id="0f75c-182">JET_bitIndexEmpty</span><span class="sxs-lookup"><span data-stu-id="0f75c-182">JET_bitIndexEmpty</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f75c-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="0f75c-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="0f75c-184">不正確地區設定識別碼 (LCID) 是透過<a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a>結構中的<strong>lcid</strong>成員傳遞 (（ <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構中的<strong>pidxunicode</strong>成員包含指向的指標，或透過<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構) 的<strong>lcid</strong>成員）。</span><span class="sxs-lookup"><span data-stu-id="0f75c-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="0f75c-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="0f75c-186">指定了不正確索引名稱。</span><span class="sxs-lookup"><span data-stu-id="0f75c-186">An invalid index name was specified.</span></span> <span data-ttu-id="0f75c-187">如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</span><span class="sxs-lookup"><span data-stu-id="0f75c-187">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f75c-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="0f75c-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="0f75c-189">傳遞至 API 的參數無效。</span><span class="sxs-lookup"><span data-stu-id="0f75c-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="0f75c-190">可能會傳回此錯誤的部分原因包括：</span><span class="sxs-lookup"><span data-stu-id="0f75c-190">Some of the reasons this error may be returned are:</span></span></p>
<ul>
<li><p><span data-ttu-id="0f75c-191"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbKey</strong>欄位設定為零。</span><span class="sxs-lookup"><span data-stu-id="0f75c-191">The <strong>cbKey</strong> field of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="0f75c-192"><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof (<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ) 。</span><span class="sxs-lookup"><span data-stu-id="0f75c-192">The <strong>cbStruct</strong> member of a <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> structure is not set to sizeof(<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="0f75c-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="0f75c-194">嘗試將 Unicode 資料行正規化時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="0f75c-194">An error occurred attempting to normalize a Unicode column.</span></span> <span data-ttu-id="0f75c-195">這可能是因為系統資源不足所造成。</span><span class="sxs-lookup"><span data-stu-id="0f75c-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="0f75c-196">備註</span><span class="sxs-lookup"><span data-stu-id="0f75c-196">Remarks</span></span>

<span data-ttu-id="0f75c-197">當指定的所有索引都成功完成時，就會 JET_errSuccess 傳回值。</span><span class="sxs-lookup"><span data-stu-id="0f75c-197">The return value is JET_errSuccess on successful completion of all indexes specified.</span></span>

<span data-ttu-id="0f75c-198">**JetCreateIndex2** 會逐一查看 **pindexcreate** 中指定的索引，有時會在第一次失敗時中止。</span><span class="sxs-lookup"><span data-stu-id="0f75c-198">**JetCreateIndex2** iterates through the indexes given in **pindexcreate**, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="0f75c-199">即使 [JET_INDEXCREATE](./jet-indexcreate-structure.md)結構的 **err** 成員包含 JET_errSuccess，仍不會嘗試在第一個具有錯誤之索引之後的任何索引。</span><span class="sxs-lookup"><span data-stu-id="0f75c-199">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0f75c-200">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f75c-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-201"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="0f75c-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0f75c-202">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="0f75c-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f75c-203"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="0f75c-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0f75c-204">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="0f75c-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-205"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="0f75c-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0f75c-206">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="0f75c-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f75c-207"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="0f75c-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0f75c-208">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="0f75c-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f75c-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0f75c-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0f75c-210">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="0f75c-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f75c-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="0f75c-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0f75c-212">實作為 <strong>JetCreateIndex2W</strong> (Unicode) 和 <strong>JetCreateIndex2A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="0f75c-212">Implemented as <strong>JetCreateIndex2W</strong> (Unicode) and <strong>JetCreateIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0f75c-213">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f75c-213">See Also</span></span>

[<span data-ttu-id="0f75c-214">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="0f75c-214">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="0f75c-215">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0f75c-215">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0f75c-216">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0f75c-216">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0f75c-217">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="0f75c-217">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="0f75c-218">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="0f75c-218">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="0f75c-219">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="0f75c-219">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="0f75c-220">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="0f75c-220">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="0f75c-221">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="0f75c-221">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="0f75c-222">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="0f75c-222">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
