---
description: 深入瞭解： JetCreateIndex4W 函數
title: JetCreateIndex4W 函式
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a4c7671cbe361b6214552f4c611cd1706c0e48d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980573"
---
# <a name="jetcreateindex4w-function"></a><span data-ttu-id="1fdb1-103">JetCreateIndex4W 函式</span><span class="sxs-lookup"><span data-stu-id="1fdb1-103">JetCreateIndex4W Function</span></span>


<span data-ttu-id="1fdb1-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1fdb1-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="1fdb1-105">**JetCreateIndex4W** 函式會在可延伸儲存引擎中的資料上建立索引， (ESE) 資料庫，可用來快速找出特定資料。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-105">The **JetCreateIndex4W** function creates indexes over data in an Extensible Storage Engine (ESE) database, which can be used to locate specific data quickly.</span></span>

<span data-ttu-id="1fdb1-106">**JetCreateIndex4W** 函式是在 Windows 8 作業系統中引進的。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-106">The **JetCreateIndex4W** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a><span data-ttu-id="1fdb1-107">參數</span><span class="sxs-lookup"><span data-stu-id="1fdb1-107">Parameters</span></span>

<span data-ttu-id="1fdb1-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1fdb1-108">*sesid*</span></span>

<span data-ttu-id="1fdb1-109">要用於 API 呼叫的資料庫會話內容。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="1fdb1-110">*tableid*</span><span class="sxs-lookup"><span data-stu-id="1fdb1-110">*tableid*</span></span>

<span data-ttu-id="1fdb1-111">將在其上建立索引的資料表。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-111">The table on which the index will be created.</span></span>

<span data-ttu-id="1fdb1-112">*pindexcreate*</span><span class="sxs-lookup"><span data-stu-id="1fdb1-112">*pindexcreate*</span></span>

<span data-ttu-id="1fdb1-113">[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)結構的陣列，其中每個結構會定義要建立的索引。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-113">An array of [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structures, each of which defines an index to be created.</span></span>

<span data-ttu-id="1fdb1-114">*cIndexCreate*</span><span class="sxs-lookup"><span data-stu-id="1fdb1-114">*cIndexCreate*</span></span>

<span data-ttu-id="1fdb1-115">*Pindexcreate* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-115">The number of elements in the *pindexcreate* array.</span></span>

### <a name="return-value"></a><span data-ttu-id="1fdb1-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1fdb1-116">Return value</span></span>

<span data-ttu-id="1fdb1-117">此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="1fdb1-118">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1fdb1-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1fdb1-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="1fdb1-120">Description</span><span class="sxs-lookup"><span data-stu-id="1fdb1-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1fdb1-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-122">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdb1-123">JET_errCannotIndex</span><span class="sxs-lookup"><span data-stu-id="1fdb1-123">JET_errCannotIndex</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-124">嘗試透過「正在進行」（update）或 SLV 資料行來編制索引， (請注意，SLV 資料行已被取代) 。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-124">An attempt was made to index over an escrow-update or SLV column (note that SLV columns are deprecated).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-125">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="1fdb1-125">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-126">嘗試在不存在的資料行上建立索引。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-126">An attempt was made to index over a nonexistent column.</span></span> <span data-ttu-id="1fdb1-127">針對不存在的資料行嘗試有條件的索引，也會產生這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-127">An attempt to conditionally index over a nonexistent column can also produce this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdb1-128">JET_errDensityInvalid</span><span class="sxs-lookup"><span data-stu-id="1fdb1-128">JET_errDensityInvalid</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-129">如果<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>ulDensity</strong>成員設定為小於20或大於100的數位，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-129">This error will be returned if the <strong>ulDensity</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to a number less than 20 or greater than 100.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-130">JET_errIndexDuplicate</span><span class="sxs-lookup"><span data-stu-id="1fdb1-130">JET_errIndexDuplicate</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-131">嘗試定義兩個相同的索引。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-131">An attempt to define two identical indexes was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdb1-132">JET_errIndexHasPrimary</span><span class="sxs-lookup"><span data-stu-id="1fdb1-132">JET_errIndexHasPrimary</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-133">嘗試為數據表指定一個以上的主要索引。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-133">An attempt was made to specify more than one primary index for a table.</span></span> <span data-ttu-id="1fdb1-134">資料表必須只有一個主要索引。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-134">A table must have exactly one primary index.</span></span> <span data-ttu-id="1fdb1-135">如果未指定任何主要索引，database engine 將會以透明方式建立一個索引。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-135">If no primary index is specified, the database engine will transparently create one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-136">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="1fdb1-136">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-137">指定了不正確索引定義。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-137">An invalid index definition was specified.</span></span> <span data-ttu-id="1fdb1-138">以下是此錯誤的一些可能原因：</span><span class="sxs-lookup"><span data-stu-id="1fdb1-138">The following are some possible reasons for this error:</span></span></p>
<ul>
<li><p><span data-ttu-id="1fdb1-139">主要索引是條件式 (<strong>grbit</strong>成員<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>已<strong>JET_bitIndexPrimary</strong>設定，而<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>的<strong>cConditionalColumn</strong>成員大於零) 。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-139">A primary index is conditional (<strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> has <strong>JET_bitIndexPrimary</strong> set, and the <strong>cConditionalColumn</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> is greater than zero).</span></span></p></li>
<li><p><span data-ttu-id="1fdb1-140">適用于從 Windows Server 2003 開始的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-140">Applies to versions of Windows starting with Windows Server 2003.</span></span> <span data-ttu-id="1fdb1-141">嘗試建立具有元組限制的元組索引，但未在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>中傳遞<strong>ptuplelimits</strong>成員的資訊 (亦即， <em>grbit</em>已<strong>JET_bitIndexTupleLimits</strong>設定，但<strong>ptuplelimits</strong>指標為 null) 。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-141">An attempt was made to create a tuple index with tuple limits, but without passing information in the <strong>ptuplelimits</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (that is, <em>grbit</em> has <strong>JET_bitIndexTupleLimits</strong> set, but the <strong>ptuplelimits</strong> pointer is null).</span></span></p></li>
<li><p><span data-ttu-id="1fdb1-142">在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>szKey</strong>成員中傳入不正確索引鍵定義。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-142">Passing in an invalid key definition in the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure.</span></span> <span data-ttu-id="1fdb1-143">如需有效定義的詳細資訊，請參閱 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-143">For information about valid definitions, see <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</span></span></p></li>
<li><p><span data-ttu-id="1fdb1-144">將<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>中的<strong>cbVarSegMac</strong>成員設定為大於主要索引的<strong>JET_cbPrimaryKeyMost</strong> () 或大於次要索引 JET_cbSecondaryKeyMost 的<strong> (</strong>) 。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-144">Setting the <strong>cbVarSegMac</strong> member in <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> to be greater than <strong>JET_cbPrimaryKeyMost</strong> (for a primary index) or greater than <strong>JET_cbSecondaryKeyMost</strong> (for a secondary index).</span></span></p></li>
<li><p><span data-ttu-id="1fdb1-145">傳遞不正確使用者定義 Unicode 索引組合， (在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>) 的<strong>grbit</strong>成員中設定<strong>JET_bitIndexUnicode</strong>位。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-145">Passing an invalid combination for a user-defined Unicode index (one which has the <strong>JET_bitIndexUnicode</strong> bit set in the <strong>grbit</strong> member of <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>).</span></span> <span data-ttu-id="1fdb1-146">常見的原因可能是 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> 結構的 pidxunicode 欄位為 null，或 pidxunicode 結構中指定的 LCID 無效。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-146">Some common causes may be that the pidxunicode field of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is null, or the LCID specified in the pidxunicode structure is invalid.</span></span></p></li>
<li><p><span data-ttu-id="1fdb1-147">指定主要索引的多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-147">Specifying a multivalued column for a primary index.</span></span></p></li>
<li><p><span data-ttu-id="1fdb1-148">正在嘗試編制太多條件式資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-148">Trying to index too many conditional columns.</span></span> <span data-ttu-id="1fdb1-149"><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cConditionalColumn</strong>成員不得大於<strong>JET_ccolKeyMost</strong>。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-149">The <strong>cConditionalColumn</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not be greater than <strong>JET_ccolKeyMost</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdb1-150">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="1fdb1-150">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-151">適用于 windows XP 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-151">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="1fdb1-152">已指定 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，但不支援其限制。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-152">A <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure was specified, and its limits are not supported.</span></span> <span data-ttu-id="1fdb1-153">如需詳細資訊，請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-153">For more information, see the remarks section of the <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-154">JET_errIndexTuplesNonUniqueOnly</span><span class="sxs-lookup"><span data-stu-id="1fdb1-154">JET_errIndexTuplesNonUniqueOnly</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-155">適用于 windows XP 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-155">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="1fdb1-156">元組索引不可以是唯一的 (<em>grbit</em> 不能同時有 <strong>JET_bitIndexTuples</strong> 和 <strong>JET_bitIndexUnique</strong> 設定) 。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-156">A tuple index cannot be unique (<em>grbit</em> must not have both <strong>JET_bitIndexTuples</strong> and <strong>JET_bitIndexUnique</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdb1-157">JET_errIndexTuplesOneColumnOnly</span><span class="sxs-lookup"><span data-stu-id="1fdb1-157">JET_errIndexTuplesOneColumnOnly</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-158">適用于 windows XP 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-158">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="1fdb1-159">元組索引只能在單一資料行上 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員已<strong>JET_bitIndexTuples</strong>設定，而<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>szKey</strong>成員指定了一個以上的資料行) 。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-159">A tuple index can only be over a single column (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexTuples</strong> set, and the <strong>szKey</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure specifies more than one column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-160">JET_errIndexTuplesSecondaryIndexOnly</span><span class="sxs-lookup"><span data-stu-id="1fdb1-160">JET_errIndexTuplesSecondaryIndexOnly</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-161">適用于 windows XP 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-161">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="1fdb1-162">元組索引不可以是主要索引 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員不能同時有<strong>JET_bitIndexPrimary</strong>和<strong>JET_bitIndexTuples</strong>設定) 。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-162">A tuple index cannot be a primary index (that is, the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure must not have both <strong>JET_bitIndexPrimary</strong> and <strong>JET_bitIndexTuples</strong> set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdb1-163">JET_errIndexTuplesTextColumnsOnly</span><span class="sxs-lookup"><span data-stu-id="1fdb1-163">JET_errIndexTuplesTextColumnsOnly</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-164">適用于 windows XP 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-164">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="1fdb1-165">元組索引只能位於 text 或 Unicode 資料行上。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-165">A tuple index can only be on a text or Unicode column.</span></span> <span data-ttu-id="1fdb1-166">嘗試將其他資料行索引 (例如，二進位資料行) 將會導致 <strong>JET_errIndexTuplesTextColumnsOnly</strong>。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-166">An attempt to index other columns (for example, binary columns) will result in <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-167">JET_errIndexTuplesVarSegMacNotAllowed</span><span class="sxs-lookup"><span data-stu-id="1fdb1-167">JET_errIndexTuplesVarSegMacNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-168">適用于 windows XP 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-168">Applies to versions of Windows starting with Windows XP.</span></span> <span data-ttu-id="1fdb1-169">元組索引不允許設定<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbVarSegMac</strong>成員。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-169">A tuple index does not allow the <strong>cbVarSegMac</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure to be set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdb1-170">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="1fdb1-170">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-171">嘗試在交易中建立沒有版本資訊的索引。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-171">An attempt was made to create an index without version information while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-172">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="1fdb1-172">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-173">因為<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員包含不一致的值，所以索引定義無效。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-173">The index definition is invalid because the <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains inconsistent values.</span></span> <span data-ttu-id="1fdb1-174">以下是一些可能的原因：</span><span class="sxs-lookup"><span data-stu-id="1fdb1-174">The following are some possible reasons:</span></span></p>
<ul>
<li><p><span data-ttu-id="1fdb1-175">主要索引具有指定的略過位 (JET_bitIndexPrimary 以 <strong>JET_bitIndexIgnoreNull</strong>、 <strong>JET_bitIndexIgnoreAnyNull</strong>或 <strong>JET_bitIndexIgnoreFirstNull</strong>) 之一傳遞。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-175">A primary index had an ignore bit specified (JET_bitIndexPrimary was passed with one of <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>, or <strong>JET_bitIndexIgnoreFirstNull</strong>).</span></span></p></li>
<li><p><span data-ttu-id="1fdb1-176">空白索引不會忽略任何 null 欄位 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員已<strong>JET_bitIndexEmpty</strong>設定，但沒有<strong>JET_bitIndexIgnoreAnyNull</strong>設定) 。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-176">An empty index does not ignore any null fields (that is, <strong>grbit</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure has <strong>JET_bitIndexEmpty</strong> set, but does not have <strong>JET_bitIndexIgnoreAnyNull</strong> set).</span></span></p></li>
<li><p><span data-ttu-id="1fdb1-177">傳入具有無效<strong>grbit</strong>成員的<a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>結構。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-177">Passing in a <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> structure with an invalid <strong>grbit</strong> member.</span></span> <span data-ttu-id="1fdb1-178">請參閱 <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-178">See <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</span></span></p></li>
</ul>
<p><span data-ttu-id="1fdb1-179">當您一次建立多個索引時 (也就是說，如果 <em>cIndexCreate</em> 參數大於一個) ，則沒有任何索引可以包含下列任何位：</span><span class="sxs-lookup"><span data-stu-id="1fdb1-179">When creating several indexes at once (that is, if the <em>cIndexCreate</em> parameter is greater than one), none of the indexes may contain any of the following bits:</span></span></p>
<ul>
<li><p><span data-ttu-id="1fdb1-180"><strong>JET_bitIndexPrimary</strong></span><span class="sxs-lookup"><span data-stu-id="1fdb1-180"><strong>JET_bitIndexPrimary</strong></span></span></p></li>
<li><p><span data-ttu-id="1fdb1-181"><strong>JET_bitIndexUnversioned</strong></span><span class="sxs-lookup"><span data-stu-id="1fdb1-181"><strong>JET_bitIndexUnversioned</strong></span></span></p></li>
<li><p><span data-ttu-id="1fdb1-182"><strong>JET_bitIndexEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="1fdb1-182"><strong>JET_bitIndexEmpty</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdb1-183">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="1fdb1-183">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-184">不正確地區設定識別碼 (LCID) 是透過<a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a>結構中的<strong>lcid</strong>成員傳遞 (（ <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構中的<strong>pidxunicode</strong>成員包含指向的指標，或透過<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構) 的<strong>lcid</strong>成員）。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-184">An invalid Locale ID (LCID) was passed in (either through the <strong>lcid</strong> member in the <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> structure, which the <strong>pidxunicode</strong> member in the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure contains a pointer to, or through the <strong>lcid</strong> member of the <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-185">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="1fdb1-185">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-186">指定了不正確索引名稱。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-186">An invalid index name was specified.</span></span> <span data-ttu-id="1fdb1-187">如需詳細資訊，請參閱 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> 。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-187">See <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdb1-188">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="1fdb1-188">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-189">傳遞至 API 的參數無效。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-189">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="1fdb1-190">以下是可能會傳回此錯誤的一些原因：</span><span class="sxs-lookup"><span data-stu-id="1fdb1-190">The following are some reasons why this error may be returned:</span></span></p>
<ul>
<li><p><span data-ttu-id="1fdb1-191"><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbKey</strong>欄位設定為零。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-191">The <strong>cbKey</strong> field of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is set to zero.</span></span></p></li>
<li><p><span data-ttu-id="1fdb1-192"><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof (JET_INDEXCREATE2) 。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-192">The <strong>cbStruct</strong> member of a <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> structure is not set to sizeof(JET_INDEXCREATE2).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-193">JET_errUnicodeTranslationFail</span><span class="sxs-lookup"><span data-stu-id="1fdb1-193">JET_errUnicodeTranslationFail</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-194">嘗試將 Unicode 資料行標準化時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-194">An error occurred while trying to normalize a Unicode column.</span></span> <span data-ttu-id="1fdb1-195">這可能是因為系統資源不足所造成。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-195">This can be caused by running out of system resources.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdb1-196">JET_errSpaceHintsInvalid</span><span class="sxs-lookup"><span data-stu-id="1fdb1-196">JET_errSpaceHintsInvalid</span></span></p></td>
<td><p><span data-ttu-id="1fdb1-197">JET 空間提示結構的元素不正確或可採取動作。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-197">An element of the JET space hints structure was not correct or actionable.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="1fdb1-198">備註</span><span class="sxs-lookup"><span data-stu-id="1fdb1-198">Remarks</span></span>

<span data-ttu-id="1fdb1-199">**JetCreateIndex4W** 函式會逐一查看 *pindexcreate* 參數中指定的索引，有時會在第一次失敗時中止。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-199">The **JetCreateIndex4W** function iterates through the indexes given in the *pindexcreate* parameter, and will sometimes abort on the first failure.</span></span> <span data-ttu-id="1fdb1-200">即使 [JET_INDEXCREATE2](./jet-indexcreate2-structure.md)結構的 **err** 成員包含 JET_errSuccess，仍不會嘗試在第一個具有錯誤之索引之後的任何索引。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-200">Any indexes after the first index with an error may not have been attempted, even though the **err** member of the [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) structure contains JET_errSuccess.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1fdb1-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fdb1-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-202"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="1fdb1-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1fdb1-203">需要 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-203">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdb1-204"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="1fdb1-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1fdb1-205">需要 Windows Server 2012。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-205">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-206"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="1fdb1-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1fdb1-207">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fdb1-208"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="1fdb1-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1fdb1-209">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fdb1-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1fdb1-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1fdb1-211">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="1fdb1-211">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1fdb1-212">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fdb1-212">See also</span></span>

[<span data-ttu-id="1fdb1-213">JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="1fdb1-213">JET_CONDITIONALCOLUMN</span></span>](./jet-conditionalcolumn-structure.md)  
[<span data-ttu-id="1fdb1-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1fdb1-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1fdb1-215">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="1fdb1-215">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="1fdb1-216">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1fdb1-216">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1fdb1-217">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1fdb1-217">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1fdb1-218">JET_INDEXCREATE2</span><span class="sxs-lookup"><span data-stu-id="1fdb1-218">JET_INDEXCREATE2</span></span>](./jet-indexcreate2-structure.md)  
[<span data-ttu-id="1fdb1-219">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="1fdb1-219">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="1fdb1-220">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="1fdb1-220">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="1fdb1-221">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="1fdb1-221">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="1fdb1-222">JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="1fdb1-222">JET_SPACEHINTS</span></span>](./jet-spacehints-structure.md)
