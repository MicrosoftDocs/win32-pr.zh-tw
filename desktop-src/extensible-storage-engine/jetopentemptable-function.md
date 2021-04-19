---
description: 深入瞭解： JetOpenTempTable 函數
title: JetOpenTempTable 函式
TOCTitle: JetOpenTempTable Function
ms:assetid: 29261333-a1bc-4159-9046-c32c36f47410
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269211(v=EXCHG.10)
ms:contentKeyID: 32765514
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66c58abc5cff433bb4d944e39c283ba712d7cebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970570"
---
# <a name="jetopentemptable-function"></a><span data-ttu-id="012de-103">JetOpenTempTable 函式</span><span class="sxs-lookup"><span data-stu-id="012de-103">JetOpenTempTable Function</span></span>


<span data-ttu-id="012de-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="012de-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable-function"></a><span data-ttu-id="012de-105">JetOpenTempTable 函式</span><span class="sxs-lookup"><span data-stu-id="012de-105">JetOpenTempTable Function</span></span>

<span data-ttu-id="012de-106">**JetOpenTempTable** 函式會建立具有單一索引的臨時表。</span><span class="sxs-lookup"><span data-stu-id="012de-106">The **JetOpenTempTable** function creates a temporary table with a single index.</span></span> <span data-ttu-id="012de-107">臨時表會儲存和抓取記錄，就像使用 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)建立的一般資料表一樣。</span><span class="sxs-lookup"><span data-stu-id="012de-107">A temporary table stores and retrieves records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="012de-108">不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。</span><span class="sxs-lookup"><span data-stu-id="012de-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="012de-109">它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。</span><span class="sxs-lookup"><span data-stu-id="012de-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="012de-110">參數</span><span class="sxs-lookup"><span data-stu-id="012de-110">Parameters</span></span>

<span data-ttu-id="012de-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="012de-111">*sesid*</span></span>

<span data-ttu-id="012de-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="012de-112">The session to use.</span></span>

<span data-ttu-id="012de-113">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="012de-113">*prgcolumndef*</span></span>

<span data-ttu-id="012de-114">在臨時表中建立之資料行的資料行定義。</span><span class="sxs-lookup"><span data-stu-id="012de-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="012de-115">用於臨時表的資料行定義選項有 **重要** 的限制。</span><span class="sxs-lookup"><span data-stu-id="012de-115">**Important**   limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="012de-116">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="012de-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="012de-117">除了一般資料行定義選項之外，也可以指定零或多個下列選項，這些選項只與臨時表的內容有關。</span><span class="sxs-lookup"><span data-stu-id="012de-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="012de-118">值</span><span class="sxs-lookup"><span data-stu-id="012de-118">Value</span></span></p></th>
<th><p><span data-ttu-id="012de-119">意義</span><span class="sxs-lookup"><span data-stu-id="012de-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="012de-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="012de-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="012de-121">臨時表之索引鍵資料行的排序次序應該是遞減的，而不是遞增的。</span><span class="sxs-lookup"><span data-stu-id="012de-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="012de-122">如果指定這個選項但未指定 JET_bitColumnTTKey 則會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="012de-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="012de-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="012de-124">資料行將是臨時表的索引鍵資料行。</span><span class="sxs-lookup"><span data-stu-id="012de-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="012de-125">在輸入陣列中指定此選項的資料行定義順序，將會決定臨時表的每個索引鍵資料行的優先順序。</span><span class="sxs-lookup"><span data-stu-id="012de-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="012de-126">陣列中具有這個選項組的第一個資料行定義將是最重要的索引鍵資料行，依此類推。</span><span class="sxs-lookup"><span data-stu-id="012de-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="012de-127">如果要求的索引鍵資料行數目超過 database engine 所能支援的數量，則會忽略不受支援索引鍵資料行的這個選項。</span><span class="sxs-lookup"><span data-stu-id="012de-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="012de-128">*ccolumn*</span><span class="sxs-lookup"><span data-stu-id="012de-128">*ccolumn*</span></span>

<span data-ttu-id="012de-129">請參閱 *prgcolumndef*。</span><span class="sxs-lookup"><span data-stu-id="012de-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="012de-130">*grbit*</span><span class="sxs-lookup"><span data-stu-id="012de-130">*grbit*</span></span>

<span data-ttu-id="012de-131">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="012de-131">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="012de-132">值</span><span class="sxs-lookup"><span data-stu-id="012de-132">Value</span></span></p></th>
<th><p><span data-ttu-id="012de-133">意義</span><span class="sxs-lookup"><span data-stu-id="012de-133">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="012de-134">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="012de-134">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="012de-135">任何嘗試插入具有與先前所插入記錄相同索引鍵的記錄，都會立即失敗，並 JET_errKeyDuplicate。</span><span class="sxs-lookup"><span data-stu-id="012de-135">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="012de-136">如果未要求這個選項，則會立即偵測到重複的情況，並會失敗，或根據資料庫引擎根據所要求的功能來執行臨時表所選擇的策略，以無訊息方式移除。</span><span class="sxs-lookup"><span data-stu-id="012de-136">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="012de-137">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="012de-137">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="012de-138">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="012de-138">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-139">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="012de-139">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="012de-140">強制臨時表管理員放棄搜尋，以使用管理將會導致效能提高的臨時表的最佳策略。</span><span class="sxs-lookup"><span data-stu-id="012de-140">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-141">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="012de-141">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="012de-142">只有當臨時表管理員可以使用針對中繼查詢結果優化的執行時，才會建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="012de-142">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="012de-143">如果臨時表的任何特性會防止使用這項優化，則作業會失敗並 JET_errCannotMaterializeForwardOnlySort。</span><span class="sxs-lookup"><span data-stu-id="012de-143">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="012de-144">此選項的副作用是允許臨時表包含具有重複索引鍵的記錄。</span><span class="sxs-lookup"><span data-stu-id="012de-144">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="012de-145">如需詳細資訊，請參閱 JET_bitTTUnique。</span><span class="sxs-lookup"><span data-stu-id="012de-145">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="012de-146">此選項僅適用于 Windows Server 2003 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="012de-146">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-147">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="012de-147">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="012de-148">此選項會要求臨時表具有足夠的彈性，可允許使用 <a href="gg294103(v=exchg.10).md">JetSeek</a> 依據索引鍵來查閱記錄。</span><span class="sxs-lookup"><span data-stu-id="012de-148">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="012de-149">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="012de-149">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="012de-150">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="012de-150">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-151">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="012de-151">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="012de-152">會從臨時表的最後一組記錄中，移除具有重複索引鍵的記錄。</span><span class="sxs-lookup"><span data-stu-id="012de-152">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="012de-153">在 Windows Server 2003 之前，資料庫引擎一律會假設這個選項有作用，因為所有叢集索引也必須是主鍵，因此必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="012de-153">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="012de-154">從 Windows Server 2003 開始，當同時指定 JET_bitTTForwardOnly 選項時，現在可以建立不會移除重複專案的臨時表。</span><span class="sxs-lookup"><span data-stu-id="012de-154">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="012de-155">一般情況下，不可能知道哪些複製成功，以及哪些重複專案會被捨棄。</span><span class="sxs-lookup"><span data-stu-id="012de-155">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="012de-156">不過，當要求 JET_bitTTErrorOnDuplicateInsertion 選項時，具有要插入至臨時表之指定索引鍵的第一個記錄一律會成功。</span><span class="sxs-lookup"><span data-stu-id="012de-156">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-157">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="012de-157">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="012de-158">要求臨時表有足夠的彈性，可讓之前插入的記錄之後變更。</span><span class="sxs-lookup"><span data-stu-id="012de-158">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="012de-159">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="012de-159">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="012de-160">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="012de-160">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-161">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="012de-161">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="012de-162">要求臨時表具有足夠的彈性，可讓您以任意順序和使用 <a href="gg294117(v=exchg.10).md">JetMove</a>的方向來掃描記錄。</span><span class="sxs-lookup"><span data-stu-id="012de-162">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="012de-163">如果不需要這項功能，最好不要要求。</span><span class="sxs-lookup"><span data-stu-id="012de-163">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="012de-164">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="012de-164">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-165">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="012de-165">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="012de-166">要求 Null 索引鍵資料行值的排序比非 Null 索引鍵資料行值更接近索引的結尾。</span><span class="sxs-lookup"><span data-stu-id="012de-166">Requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-167">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="012de-167">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="012de-168">要求只允許內建的 long 值。</span><span class="sxs-lookup"><span data-stu-id="012de-168">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="012de-169"><strong>Windows 7</strong>： <strong>JET_bitTTIntrinsicLVsOnly</strong> 是在 windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="012de-169"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="012de-170">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="012de-170">*ptableid*</span></span>

<span data-ttu-id="012de-171">輸出緩衝區，會接收新建立的臨時表上開啟的新資料指標。</span><span class="sxs-lookup"><span data-stu-id="012de-171">The output buffer that receives the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="012de-172">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="012de-172">*prgcolumnid*</span></span>

<span data-ttu-id="012de-173">輸出緩衝區，接收在建立臨時表期間所產生的資料行識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="012de-173">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="012de-174">此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。</span><span class="sxs-lookup"><span data-stu-id="012de-174">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="012de-175">因此，這個緩衝區的大小必須對應到輸入陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="012de-175">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="012de-176">傳回值</span><span class="sxs-lookup"><span data-stu-id="012de-176">Return Value</span></span>

<span data-ttu-id="012de-177">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="012de-177">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="012de-178">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="012de-178">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="012de-179">傳回碼</span><span class="sxs-lookup"><span data-stu-id="012de-179">Return code</span></span></p></th>
<th><p><span data-ttu-id="012de-180">Description</span><span class="sxs-lookup"><span data-stu-id="012de-180">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="012de-181">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="012de-181">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="012de-182">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="012de-182">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-183">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="012de-183">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="012de-184"><strong>JetOpenTempTable</strong> 失敗，因為指定了 JET_bitTTForwardOnly，而且無法使用順向優化來建立指定的臨時表。</span><span class="sxs-lookup"><span data-stu-id="012de-184"><strong>JetOpenTempTable</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="012de-185">只有 Windows Server 2003 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="012de-185">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-186">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="012de-186">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="012de-187">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="012de-187">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-188">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="012de-188">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="012de-189">無法建立索引，因為指定了不正確索引定義。</span><span class="sxs-lookup"><span data-stu-id="012de-189">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="012de-190"><strong>JetOpenTempTable</strong> 會在下列情況傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="012de-190"><strong>JetOpenTempTable</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="012de-191">指定了中性語言的地區設定。</span><span class="sxs-lookup"><span data-stu-id="012de-191">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="012de-192">指定了不正確正規化旗標集合。</span><span class="sxs-lookup"><span data-stu-id="012de-192">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="012de-193">此錯誤只會由 Windows 2000 傳回。</span><span class="sxs-lookup"><span data-stu-id="012de-193">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="012de-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="012de-195">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="012de-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="012de-196">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="012de-196">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-197">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="012de-197">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="012de-198"><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>的 [cp] 欄位未設定為有效的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="012de-198">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="012de-199">Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。</span><span class="sxs-lookup"><span data-stu-id="012de-199">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="012de-200">0值表示預設值將使用 (英文、1252) 。</span><span class="sxs-lookup"><span data-stu-id="012de-200">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-201">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="012de-201">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="012de-202"><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>的<em>coltyp</em>欄位未設定為有效的資料行類型。</span><span class="sxs-lookup"><span data-stu-id="012de-202">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-203">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="012de-203">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="012de-204">無法建立索引，因為嘗試使用不正確地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="012de-204">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="012de-205">地區設定識別碼可能完全無效，或可能未安裝相關聯的語言套件。</span><span class="sxs-lookup"><span data-stu-id="012de-205">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-206">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="012de-206">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="012de-207">無法建立索引，因為嘗試使用一組不正確正規化旗標。</span><span class="sxs-lookup"><span data-stu-id="012de-207">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="012de-208">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="012de-208">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="012de-209">在 Windows 2000 上，不正確正規化旗標會改為產生 JET_errIndexInvalidDef。</span><span class="sxs-lookup"><span data-stu-id="012de-209">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-210">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="012de-210">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="012de-211">會話控制碼無效或參考已關閉的會話。</span><span class="sxs-lookup"><span data-stu-id="012de-211">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="012de-212"><strong>注意</strong>  在所有情況下，都不會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="012de-212"><strong>Note</strong>  This error is not returned under all circumstances.</span></span> <span data-ttu-id="012de-213">控制碼只會根據最大努力進行驗證。</span><span class="sxs-lookup"><span data-stu-id="012de-213">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-214">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="012de-214">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="012de-215">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="012de-215">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-216">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="012de-216">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="012de-217">作業失敗，因為引擎無法配置開啟新資料指標所需的資源。</span><span class="sxs-lookup"><span data-stu-id="012de-217">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="012de-218">資料指標資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>進行設定。</span><span class="sxs-lookup"><span data-stu-id="012de-218">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-219">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="012de-219">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="012de-220">作業失敗，因為無法配置足夠的記憶體來完成。</span><span class="sxs-lookup"><span data-stu-id="012de-220">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="012de-221">如果主機進程的位址空間變得太分散， <strong>JetOpenTempTable</strong>可能會傳回 JET_errOutOfMemory。</span><span class="sxs-lookup"><span data-stu-id="012de-221"><strong>JetOpenTempTable</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="012de-222">無論要儲存的資料量為何，臨時表管理員一律會為每個建立的臨時表配置1MB 的位址空間區塊。</span><span class="sxs-lookup"><span data-stu-id="012de-222">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-223">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="012de-223">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="012de-224">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="012de-224">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-225">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="012de-225">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="012de-226">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="012de-226">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="012de-227">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="012de-227">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-228">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="012de-228">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="012de-229">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="012de-229">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-230">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="012de-230">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="012de-231">嘗試將過多的資料行新增至資料表。</span><span class="sxs-lookup"><span data-stu-id="012de-231">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="012de-232">資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="012de-232">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-233">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="012de-233">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="012de-234">作業失敗，因為引擎無法配置快取資料表索引所需的資源。</span><span class="sxs-lookup"><span data-stu-id="012de-234">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="012de-235">您可以使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>，設定可以快取架構的索引數目。</span><span class="sxs-lookup"><span data-stu-id="012de-235">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-236">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="012de-236">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="012de-237">作業失敗，因為引擎無法配置快取資料表架構所需的資源。</span><span class="sxs-lookup"><span data-stu-id="012de-237">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="012de-238">您可以使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>，設定可以快取架構的資料表數目。</span><span class="sxs-lookup"><span data-stu-id="012de-238">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-239">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="012de-239">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="012de-240">作業失敗，因為引擎無法配置建立臨時表所需的資源。</span><span class="sxs-lookup"><span data-stu-id="012de-240">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="012de-241">臨時表資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>進行設定。</span><span class="sxs-lookup"><span data-stu-id="012de-241">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="012de-242">成功時，會傳回在新建立的臨時表上開啟的資料指標。</span><span class="sxs-lookup"><span data-stu-id="012de-242">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="012de-243">暫存資料庫的狀態將準備好包含新的臨時表。</span><span class="sxs-lookup"><span data-stu-id="012de-243">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="012de-244">資料庫引擎所使用之任何一般資料庫的狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="012de-244">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="012de-245">失敗時，將不會建立臨時表，也不會傳回資料指標。</span><span class="sxs-lookup"><span data-stu-id="012de-245">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="012de-246">暫存資料庫的狀態可能會變更。</span><span class="sxs-lookup"><span data-stu-id="012de-246">The state of the temporary database may be changed.</span></span> <span data-ttu-id="012de-247">資料庫引擎所使用之任何一般資料庫的狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="012de-247">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="012de-248">備註</span><span class="sxs-lookup"><span data-stu-id="012de-248">Remarks</span></span>

<span data-ttu-id="012de-249">臨時表不支援資料庫引擎通常支援之資料行定義選項的完整補充。</span><span class="sxs-lookup"><span data-stu-id="012de-249">Temporary tables do not support the full complement of column definition options that are ordinarily supported by the database engine.</span></span> <span data-ttu-id="012de-250">事實上，只支援 JET_bitColumnFixed 和 JET_bitColumnTagged。</span><span class="sxs-lookup"><span data-stu-id="012de-250">In fact, only JET_bitColumnFixed and JET_bitColumnTagged are supported.</span></span> <span data-ttu-id="012de-251">這表示不可能在臨時表中建立自動遞增、版本或多重值資料行。</span><span class="sxs-lookup"><span data-stu-id="012de-251">This means that it is not possible to create an auto-increment, version, or multi-valued column in a temporary table.</span></span> <span data-ttu-id="012de-252">最後，不支援保管更新資料行，因為它們在臨時表中並不實用，因為它們一次只能由一個會話使用。</span><span class="sxs-lookup"><span data-stu-id="012de-252">Finally, escrow update columns are not supported because they are not useful in a temporary table since they can only be used by one session at a time.</span></span> <span data-ttu-id="012de-253">如果要求這些選項中的任何一項，則會忽略這些選項。</span><span class="sxs-lookup"><span data-stu-id="012de-253">If any of these options are requested then they will be ignored.</span></span>

<span data-ttu-id="012de-254">臨時表不支援預設值。</span><span class="sxs-lookup"><span data-stu-id="012de-254">Temporary tables do not support default values.</span></span> <span data-ttu-id="012de-255">如果提供的資料行定義包含預設值規格，則會忽略該規格。</span><span class="sxs-lookup"><span data-stu-id="012de-255">If a column definition is provided that contains a default value specification then that specification will be ignored.</span></span>

<span data-ttu-id="012de-256">由於許多不同的 ESE 函數，臨時表會傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="012de-256">Temporary tables are returned to the caller as a result of many different ESE functions.</span></span> <span data-ttu-id="012de-257">例如，在 *InfoLevel* 參數中設定 JET_IdxInfo 選項的 [JetGetIndexInfo](./jetgetindexinfo-function.md) ，將會傳回臨時表，其中包含給定索引中所有索引鍵資料行的清單。</span><span class="sxs-lookup"><span data-stu-id="012de-257">For example, [JetGetIndexInfo](./jetgetindexinfo-function.md) with the JET_IdxInfo option set in the *InfoLevel* parameter will return a temporary table containing a list of all the key columns in a given index.</span></span> <span data-ttu-id="012de-258">臨時表會遵循與一般臨時表相同的生命週期規則，如下所述。</span><span class="sxs-lookup"><span data-stu-id="012de-258">The temporary tables follow the same lifecycle rules as ordinary temporary tables as described here.</span></span>

<span data-ttu-id="012de-259">資料庫引擎也會在內部使用臨時表來進行許多工。</span><span class="sxs-lookup"><span data-stu-id="012de-259">Temporary tables are also used internally by the database engine for many tasks.</span></span> <span data-ttu-id="012de-260">這些工作中最重要的就是在現有的資料表上建立索引。</span><span class="sxs-lookup"><span data-stu-id="012de-260">The most important of these tasks is the creation of an index over an existing table.</span></span> <span data-ttu-id="012de-261">臨時表將用來排序用來建立索引的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="012de-261">A temporary table will be used to sort the index keys used to construct that index.</span></span>

<span data-ttu-id="012de-262">所有臨時表都會儲存在暫存資料庫中。</span><span class="sxs-lookup"><span data-stu-id="012de-262">All temporary tables are stored in the temporary database.</span></span> <span data-ttu-id="012de-263">暫存資料庫是一個特殊的資料庫檔案，會在 ESE 實例的存留期內進行維護，當該實例關閉或重新開機時，就會將其刪除。</span><span class="sxs-lookup"><span data-stu-id="012de-263">The temporary database is a special database file that is maintained during the lifetime of an ESE instance and is deleted when that instance is shut down or restarted.</span></span> <span data-ttu-id="012de-264">您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 [JET_paramTempPath](./temporary-database-parameters.md)來設定暫存資料庫的位置。</span><span class="sxs-lookup"><span data-stu-id="012de-264">The location of the temporary database can be configured using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramTempPath](./temporary-database-parameters.md).</span></span> <span data-ttu-id="012de-265">如果您的應用程式大量使用臨時表或經常建立索引，則相對於交易記錄檔和資料庫檔案的暫存資料庫放置在磁片上可能很重要。</span><span class="sxs-lookup"><span data-stu-id="012de-265">Placement of the temporary database on disk relative to your transaction log files and database files may be important if your application makes heavy use of temporary tables or creates indexes frequently.</span></span>

<span data-ttu-id="012de-266">臨時表的生命週期會系結至參考它的資料指標。</span><span class="sxs-lookup"><span data-stu-id="012de-266">The lifecycle of a temporary table is tied to the cursors that reference it.</span></span> <span data-ttu-id="012de-267">如果參考臨時表的所有資料指標都是以隱含或明確的方式關閉，則會刪除臨時表。</span><span class="sxs-lookup"><span data-stu-id="012de-267">If all the cursors that reference a temporary table are closed, either implicitly or explicitly, then the temporary table will be deleted.</span></span> <span data-ttu-id="012de-268">如果在交易內建立臨時表，而且之後復原該交易，則會刪除該臨時表，因為此時參考該資料表的任何資料指標都會以隱含方式關閉。</span><span class="sxs-lookup"><span data-stu-id="012de-268">If a temporary table is created inside a transaction and that transaction is subsequently rolled back then the temporary table will be deleted because any cursors that referenced it at this time will be implicitly closed.</span></span> <span data-ttu-id="012de-269">新的資料指標可能只會透過使用 [JetDupCursor](./jetdupcursor-function.md)來參考臨時表。</span><span class="sxs-lookup"><span data-stu-id="012de-269">New cursors may reference a temporary table only through the use of [JetDupCursor](./jetdupcursor-function.md).</span></span> <span data-ttu-id="012de-270">在此情況下，新的資料指標將定位於臨時表的第一個索引項目目。</span><span class="sxs-lookup"><span data-stu-id="012de-270">In this case, the new cursors will be positioned on the first index entry of the temporary table.</span></span> <span data-ttu-id="012de-271">[JetDupCursor](./jetdupcursor-function.md) 僅適用于臨時表的特定使用階段。</span><span class="sxs-lookup"><span data-stu-id="012de-271">[JetDupCursor](./jetdupcursor-function.md) will only work during certain phases of use for the temporary table.</span></span> <span data-ttu-id="012de-272">如需詳細資訊，請參閱關於臨時表資料指標功能的備註。</span><span class="sxs-lookup"><span data-stu-id="012de-272">See the remarks concerning temporary table cursor capabilities for more information.</span></span> <span data-ttu-id="012de-273">一次只能從一個以上的會話參考臨時表。</span><span class="sxs-lookup"><span data-stu-id="012de-273">It is not possible to reference a temporary table from more than one session at a time.</span></span>

<span data-ttu-id="012de-274">[JetDupCursor](./jetdupcursor-function.md)中有一個會影響臨時表的重要問題。</span><span class="sxs-lookup"><span data-stu-id="012de-274">There is an important problem in [JetDupCursor](./jetdupcursor-function.md) that affects temporary tables.</span></span> <span data-ttu-id="012de-275">如果嘗試複製處於順向模式的臨時表，則會無法正確建立產生的資料指標，而且會發生故障。</span><span class="sxs-lookup"><span data-stu-id="012de-275">If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="012de-276">在具體化的臨時表上重復資料指標仍然是安全的。</span><span class="sxs-lookup"><span data-stu-id="012de-276">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

<span data-ttu-id="012de-277">臨時表管理員可能會選擇以三種方式來執行臨時表。</span><span class="sxs-lookup"><span data-stu-id="012de-277">The temporary table manager may choose to implement a temporary table in three ways.</span></span> <span data-ttu-id="012de-278">第一個方法是維護記憶體中的資料表。</span><span class="sxs-lookup"><span data-stu-id="012de-278">The first method is to maintain an in-memory table.</span></span> <span data-ttu-id="012de-279">這是最快的策略，但只能用於小型、簡單的臨時表。</span><span class="sxs-lookup"><span data-stu-id="012de-279">This strategy is the fastest but can only be used for small, simple temporary tables.</span></span> <span data-ttu-id="012de-280">第二種方法是建立以磁片為基礎的排序，該排序可使用順向反覆運算器驅動。</span><span class="sxs-lookup"><span data-stu-id="012de-280">The second method is to create a disk-based sort that can be driven using a forward-only iterator.</span></span> <span data-ttu-id="012de-281">這項策略只能在特定情況下使用，而且是從非常大的資料集排序和移除重複專案的最快速方式。</span><span class="sxs-lookup"><span data-stu-id="012de-281">This strategy can only be used under certain circumstances and is the fastest way to sort and remove duplicates from a very large data set.</span></span> <span data-ttu-id="012de-282">第三種方法是在暫存資料庫中建立 B + 樹狀結構，以保存臨時表。</span><span class="sxs-lookup"><span data-stu-id="012de-282">The third method is to create a B+ Tree in the temporary database to hold the temporary table.</span></span> <span data-ttu-id="012de-283">這個策略是最慢的，但最多用途，而且稱為具體化臨時表。</span><span class="sxs-lookup"><span data-stu-id="012de-283">This strategy is the slowest, but the most versatile, and is referred to as a materialized temporary table.</span></span> <span data-ttu-id="012de-284">這些策略可組合使用，以最終達成臨時表所要求的功能。</span><span class="sxs-lookup"><span data-stu-id="012de-284">These strategies may be used in combination to ultimately achieve the functionality requested of the temporary table.</span></span>

<span data-ttu-id="012de-285">當臨時表未具體化時，主要是用於兩個主要階段。</span><span class="sxs-lookup"><span data-stu-id="012de-285">When the temporary table is not materialized then it is used in primarily two major phases.</span></span> <span data-ttu-id="012de-286">第一個階段是插入階段，其中資料表會填入其初始資料集。</span><span class="sxs-lookup"><span data-stu-id="012de-286">The first phase is the insertion phase where the table is populated with its initial data set.</span></span> <span data-ttu-id="012de-287">在這個階段中，只允許插入資料。</span><span class="sxs-lookup"><span data-stu-id="012de-287">During this phase, only data insertion is allowed.</span></span> <span data-ttu-id="012de-288">當嘗試使用 [JetMove](./jetmove-function.md) 或 [JetSeek](./jetseek-function.md)移動資料指標時，就會結束這個階段。</span><span class="sxs-lookup"><span data-stu-id="012de-288">This phase ends when an attempt is made to move the cursor using [JetMove](./jetmove-function.md) or [JetSeek](./jetseek-function.md).</span></span> <span data-ttu-id="012de-289">第二個階段是資料解壓縮階段。</span><span class="sxs-lookup"><span data-stu-id="012de-289">The second phase is the data extraction phase.</span></span> <span data-ttu-id="012de-290">在這個階段，儲存在臨時表中的資料，可能會根據建立臨時表時所要求的功能進行解壓縮。</span><span class="sxs-lookup"><span data-stu-id="012de-290">During this phase, the data stored in the temporary table may be extracted according to the capabilities requested when the temporary table was created.</span></span>

<span data-ttu-id="012de-291">**臨時表資料指標功能**</span><span class="sxs-lookup"><span data-stu-id="012de-291">**Temporary Table Cursor Capabilities**</span></span>

<span data-ttu-id="012de-292">當臨時表具體化時，資料指標有下列功能，但可能會進一步受要求的選項限制：</span><span class="sxs-lookup"><span data-stu-id="012de-292">When the temporary table is materialized, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="012de-293">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="012de-293">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="012de-294">JetDelete</span><span class="sxs-lookup"><span data-stu-id="012de-294">JetDelete</span></span>](./jetdelete-function.md)

  - [<span data-ttu-id="012de-295">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="012de-295">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="012de-296">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="012de-296">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="012de-297">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="012de-297">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="012de-298">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="012de-298">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="012de-299">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="012de-299">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="012de-300">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="012de-300">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="012de-301">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="012de-301">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="012de-302">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="012de-302">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="012de-303">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="012de-303">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="012de-304">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="012de-304">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="012de-305">JetMove</span><span class="sxs-lookup"><span data-stu-id="012de-305">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="012de-306">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="012de-306">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="012de-307">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="012de-307">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="012de-308">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="012de-308">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="012de-309">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="012de-309">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="012de-310">JetSeek</span><span class="sxs-lookup"><span data-stu-id="012de-310">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="012de-311">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="012de-311">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="012de-312">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="012de-312">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="012de-313">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="012de-313">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="012de-314">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="012de-314">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="012de-315">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="012de-315">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="012de-316">當臨時表未具體化且在插入階段時，資料指標有下列功能，但可能會進一步限制要求的選項：</span><span class="sxs-lookup"><span data-stu-id="012de-316">When the temporary table is not materialized and is in the insert phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="012de-317">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="012de-317">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="012de-318">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="012de-318">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)

  - [<span data-ttu-id="012de-319">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="012de-319">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="012de-320">JetMove</span><span class="sxs-lookup"><span data-stu-id="012de-320">JetMove</span></span>](./jetmove-function.md)
    
    <span data-ttu-id="012de-321">**注意**  導致轉換成解壓縮階段。</span><span class="sxs-lookup"><span data-stu-id="012de-321">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="012de-322">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="012de-322">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)

  - [<span data-ttu-id="012de-323">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="012de-323">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="012de-324">JetSeek</span><span class="sxs-lookup"><span data-stu-id="012de-324">JetSeek</span></span>](./jetseek-function.md)
    
    <span data-ttu-id="012de-325">**注意**  導致轉換成解壓縮階段。</span><span class="sxs-lookup"><span data-stu-id="012de-325">**Note**  Causes transition to the extract phase.</span></span>

  - [<span data-ttu-id="012de-326">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="012de-326">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="012de-327">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="012de-327">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="012de-328">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="012de-328">JetUpdate</span></span>](./jetupdate-function.md)

<span data-ttu-id="012de-329">當臨時表未具體化而且在解壓縮階段時，資料指標有下列功能，但可能會進一步受要求的選項限制：</span><span class="sxs-lookup"><span data-stu-id="012de-329">When the temporary table is not materialized and is in the extract phase, the cursor has the following capabilities but may be further limited by the options requested:</span></span>

  - [<span data-ttu-id="012de-330">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="012de-330">JetCloseTable</span></span>](./jetclosetable-function.md)

  - [<span data-ttu-id="012de-331">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="012de-331">JetDupCursor</span></span>](./jetdupcursor-function.md)
    
    <span data-ttu-id="012de-332">**注意**  如果嘗試複製處於順向模式的臨時表，則會無法正確建立產生的資料指標，而且會發生故障。</span><span class="sxs-lookup"><span data-stu-id="012de-332">**Note**  If an attempt is made to duplicate a temporary table that is in forward-only mode then the resulting cursor will not be created properly and will malfunction.</span></span> <span data-ttu-id="012de-333">在具體化的臨時表上重復資料指標仍然是安全的。</span><span class="sxs-lookup"><span data-stu-id="012de-333">It is still safe to duplicate a cursor over a materialized temporary table.</span></span>

  - [<span data-ttu-id="012de-334">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="012de-334">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="012de-335">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="012de-335">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="012de-336">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="012de-336">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="012de-337">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="012de-337">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)

  - [<span data-ttu-id="012de-338">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="012de-338">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="012de-339">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="012de-339">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)

  - [<span data-ttu-id="012de-340">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="012de-340">JetMakeKey</span></span>](./jetmakekey-function.md)

  - [<span data-ttu-id="012de-341">JetMove</span><span class="sxs-lookup"><span data-stu-id="012de-341">JetMove</span></span>](./jetmove-function.md)

  - [<span data-ttu-id="012de-342">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="012de-342">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="012de-343">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="012de-343">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="012de-344">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="012de-344">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="012de-345">JetSeek</span><span class="sxs-lookup"><span data-stu-id="012de-345">JetSeek</span></span>](./jetseek-function.md)

  - [<span data-ttu-id="012de-346">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="012de-346">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)

  - [<span data-ttu-id="012de-347">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="012de-347">JetSetLS</span></span>](./jetsetls-function.md)

#### <a name="requirements"></a><span data-ttu-id="012de-348">規格需求</span><span class="sxs-lookup"><span data-stu-id="012de-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="012de-349"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="012de-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="012de-350">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="012de-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-351"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="012de-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="012de-352">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="012de-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-353"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="012de-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="012de-354">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="012de-354">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="012de-355"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="012de-355"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="012de-356">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="012de-356">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="012de-357"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="012de-357"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="012de-358">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="012de-358">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="012de-359">另請參閱</span><span class="sxs-lookup"><span data-stu-id="012de-359">See Also</span></span>

[<span data-ttu-id="012de-360">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="012de-360">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="012de-361">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="012de-361">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="012de-362">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="012de-362">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="012de-363">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="012de-363">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="012de-364">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="012de-364">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="012de-365">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="012de-365">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="012de-366">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="012de-366">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="012de-367">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="012de-367">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="012de-368">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="012de-368">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="012de-369">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="012de-369">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="012de-370">JetMove</span><span class="sxs-lookup"><span data-stu-id="012de-370">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="012de-371">JetRollback</span><span class="sxs-lookup"><span data-stu-id="012de-371">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="012de-372">JetSeek</span><span class="sxs-lookup"><span data-stu-id="012de-372">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="012de-373">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="012de-373">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="012de-374">暫存資料庫參數</span><span class="sxs-lookup"><span data-stu-id="012de-374">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)
