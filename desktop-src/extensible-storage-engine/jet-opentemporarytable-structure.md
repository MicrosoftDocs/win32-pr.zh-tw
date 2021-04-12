---
description: 深入瞭解： JET_OPENTEMPORARYTABLE 結構
title: JET_OPENTEMPORARYTABLE 結構
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51ae9026098e82538940bde2ef182ba0a7a11c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319319"
---
# <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="9bb9c-103">JET_OPENTEMPORARYTABLE 結構</span><span class="sxs-lookup"><span data-stu-id="9bb9c-103">JET_OPENTEMPORARYTABLE Structure</span></span>


<span data-ttu-id="9bb9c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9bb9c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_opentemporarytable-structure"></a><span data-ttu-id="9bb9c-105">JET_OPENTEMPORARYTABLE 結構</span><span class="sxs-lookup"><span data-stu-id="9bb9c-105">JET_OPENTEMPORARYTABLE Structure</span></span>

<span data-ttu-id="9bb9c-106">**JET_OPENTEMPORARYTABLE** 結構包含可輕鬆擴充的 **JET_OPENTEMPORARYTABLE** 函式參數集合。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-106">The **JET_OPENTEMPORARYTABLE** structure contains an easily extensible collection of parameters for the **JET_OPENTEMPORARYTABLE** function.</span></span> <span data-ttu-id="9bb9c-107">此結構是與 [JET_TABLECREATE](./jet-tablecreate-structure.md) 結構相等的臨時表。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-107">This structure is the temporary table equivalent of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure.</span></span>

<span data-ttu-id="9bb9c-108">**Windows Vista：** 在 Windows Vista 中引進 **JET_OPENTEMPORARYTABLE** 結構。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-108">**Windows Vista:** The **JET_OPENTEMPORARYTABLE** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a><span data-ttu-id="9bb9c-109">成員</span><span class="sxs-lookup"><span data-stu-id="9bb9c-109">Members</span></span>

<span data-ttu-id="9bb9c-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="9bb9c-110">**cbStruct**</span></span>

<span data-ttu-id="9bb9c-111">此結構的大小，以位元組為單位， (未來的擴充) 。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-111">The size of this structure in bytes (for future expansion).</span></span> <span data-ttu-id="9bb9c-112">它必須設定為 sizeof ( JET_TABLECREATE ) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-112">It must be set to sizeof( JET_TABLECREATE ) in bytes.</span></span>

<span data-ttu-id="9bb9c-113">**prgcolumndef**</span><span class="sxs-lookup"><span data-stu-id="9bb9c-113">**prgcolumndef**</span></span>

<span data-ttu-id="9bb9c-114">在臨時表中建立之資料行的資料行定義。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-114">Column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="9bb9c-115">用於臨時表的資料行定義選項有 **重要** 的限制。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-115">**Important** limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="9bb9c-116">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="9bb9c-117">除了一般資料行定義選項之外，也可以指定零或多個下列選項，這些選項只與臨時表的內容有關。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9bb9c-118">值</span><span class="sxs-lookup"><span data-stu-id="9bb9c-118">Value</span></span></p></th>
<th><p><span data-ttu-id="9bb9c-119">意義</span><span class="sxs-lookup"><span data-stu-id="9bb9c-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bb9c-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="9bb9c-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="9bb9c-121">臨時表之索引鍵資料行的排序次序應該是遞減的，而不是遞增的。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="9bb9c-122">如果指定這個選項但未指定 JET_bitColumnTTKey 則會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bb9c-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="9bb9c-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="9bb9c-124">資料行將是臨時表的索引鍵資料行。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="9bb9c-125">在輸入陣列中指定此選項的資料行定義順序，將會決定臨時表的每個索引鍵資料行的優先順序。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="9bb9c-126">陣列中具有這個選項組的第一個資料行定義將是最重要的索引鍵資料行，依此類推。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-126">The first column definition in the array that has this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="9bb9c-127">如果要求的索引鍵資料行數目超過 database engine 所能支援的數量，則會忽略不受支援索引鍵資料行的這個選項。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9bb9c-128">**ccolumn**</span><span class="sxs-lookup"><span data-stu-id="9bb9c-128">**ccolumn**</span></span>

<span data-ttu-id="9bb9c-129">請參閱 *prgcolumndef*。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="9bb9c-130">**pidxunicode**</span><span class="sxs-lookup"><span data-stu-id="9bb9c-130">**pidxunicode**</span></span>

<span data-ttu-id="9bb9c-131">用來比較臨時表中任何 Unicode 索引鍵資料行資料的地區設定識別碼和正規化旗標。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-131">The locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="9bb9c-132">當這個參數不存在，而且沒有 *lcid* 參數時，就會使用預設的 lcid 來比較臨時表中的任何 Unicode 索引鍵資料行。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-132">When this parameter is not present and when the *lcid* parameter is not present, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="9bb9c-133">預設的 LCID 是美國英文地區設定。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-133">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="9bb9c-134">如果這個參數不存在，則會使用預設正規化旗標來比較臨時表中的任何 Unicode 索引鍵資料行資料。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-134">When this parameter is not present, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="9bb9c-135">預設正規化旗標為： NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-135">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="9bb9c-136">**grbit**</span><span class="sxs-lookup"><span data-stu-id="9bb9c-136">**grbit**</span></span>

<span data-ttu-id="9bb9c-137">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-137">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9bb9c-138">值</span><span class="sxs-lookup"><span data-stu-id="9bb9c-138">Value</span></span></p></th>
<th><p><span data-ttu-id="9bb9c-139">意義</span><span class="sxs-lookup"><span data-stu-id="9bb9c-139">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bb9c-140">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="9bb9c-140">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="9bb9c-141">此選項會要求臨時表具有足夠的彈性，可允許使用 <a href="gg294103(v=exchg.10).md">JetSeek</a> 依據索引鍵來查閱記錄。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-141">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="9bb9c-142">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-142">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="9bb9c-143">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-143">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bb9c-144">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="9bb9c-144">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="9bb9c-145">會從臨時表的最後一組記錄中，移除具有重複索引鍵的記錄。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-145">Requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="9bb9c-146">在 Windows Server 2003 之前，資料庫引擎一律會假設這個選項有作用，因為所有叢集索引也必須是主鍵，因此必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-146">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="9bb9c-147">從 Windows Server 2003 開始，當同時指定 JET_bitTTForwardOnly 選項時，現在可以建立不會移除重複專案的臨時表。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-147">As of Windows Server 2003, it is now possible to create a temporary table that does not remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="9bb9c-148">一般情況下，不可能知道哪些複製成功，以及哪些重複專案會被捨棄。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-148">It is not possible to know which duplicate will succeed and which duplicates will be discarded, in general.</span></span> <span data-ttu-id="9bb9c-149">不過，當要求 JET_bitTTErrorOnDuplicateInsertion 選項時，具有要插入至臨時表之指定索引鍵的第一個記錄一律會成功。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-149">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bb9c-150">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="9bb9c-150">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="9bb9c-151">要求臨時表有足夠的彈性，可讓之前插入的記錄之後變更。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-151">Requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="9bb9c-152">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-152">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="9bb9c-153">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-153">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bb9c-154">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="9bb9c-154">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="9bb9c-155">要求臨時表具有足夠的彈性，可讓您以任意順序和使用 <a href="gg294117(v=exchg.10).md">JetMove</a>的方向來掃描記錄。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-155">Requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="9bb9c-156">如果不需要這項功能，最好不要要求。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-156">If this functionality is not required then it is best to not request it.</span></span> <span data-ttu-id="9bb9c-157">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-157">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bb9c-158">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="9bb9c-158">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="9bb9c-159">要求 <strong>Null</strong> 索引鍵資料行值的排序比非 Null 索引鍵資料行值更接近索引的結尾。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-159">Requests that <strong>NULL</strong> key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bb9c-160">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="9bb9c-160">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="9bb9c-161">強制臨時表管理員放棄搜尋，以使用管理將會導致效能提高的臨時表的最佳策略。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-161">Forces the temporary table manager to abandon the search for the best strategy to use managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bb9c-162">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="9bb9c-162">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="9bb9c-163">任何嘗試插入具有與先前所插入記錄相同索引鍵的記錄，都會立即失敗，並 JET_errKeyDuplicate。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-163">Any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="9bb9c-164">如果未要求這個選項，則會立即偵測到重複的情況，並會失敗，或根據資料庫引擎根據所要求的功能來執行臨時表所選擇的策略，以無訊息方式移除。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-164">If this option is not requested then a duplicate is detected immediately and fails, or is silently removed later, depending on the strategy chosen by the database engine to implement the temporary table, based on the requested functionality.</span></span></p>
<p><span data-ttu-id="9bb9c-165">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-165">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="9bb9c-166">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-166">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bb9c-167">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="9bb9c-167">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="9bb9c-168">只有當臨時表管理員可以使用針對中繼查詢結果優化的執行時，才會建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-168">The temporary table is only created if the temporary table manager can use the implementation that is optimized for intermediate query results.</span></span> <span data-ttu-id="9bb9c-169">如果臨時表的任何特性會防止使用這項優化，則作業會失敗並 JET_errCannotMaterializeForwardOnlySort。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-169">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="9bb9c-170">此選項的副作用是允許臨時表包含具有重複索引鍵的記錄。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-170">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="9bb9c-171">如需詳細資訊，請參閱 JET_bitTTUnique。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-171">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="9bb9c-172"><strong>Windows Server 2003：  </strong>此選項僅適用于 Windows Server 2003 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-172"><strong>Windows Server 2003:  </strong>This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9bb9c-173">**prgcolumnid**</span><span class="sxs-lookup"><span data-stu-id="9bb9c-173">**prgcolumnid**</span></span>

<span data-ttu-id="9bb9c-174">輸出緩衝區，接收在建立臨時表期間所產生的資料行識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-174">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="9bb9c-175">此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-175">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="9bb9c-176">因此，這個緩衝區的大小必須對應到輸入陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-176">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

<span data-ttu-id="9bb9c-177">**cbKeyMost**</span><span class="sxs-lookup"><span data-stu-id="9bb9c-177">**cbKeyMost**</span></span>

<span data-ttu-id="9bb9c-178">代表指定資料列之索引鍵的大小上限。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-178">The maximum size for a key representing a given row.</span></span>

<span data-ttu-id="9bb9c-179">您可以設定最大索引鍵大小來控制如何截斷金鑰。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-179">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="9bb9c-180">金鑰截斷很重要，因為它可能會影響資料列視為相異的時間。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-180">Key truncation is important because it can affect when rows are considered to be distinct.</span></span>

<span data-ttu-id="9bb9c-181">如果此參數設定為0或 JET_cbKeyMostMin (255) 那麼，最大金鑰大小及其語義將會與 Windows Server 2003 和舊版所支援的最大金鑰大小保持一致。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-181">If this parameter is set to 0 or JET_cbKeyMostMin (255) then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003 and previous releases.</span></span> <span data-ttu-id="9bb9c-182">此參數也可以設定為較大的值，做為實例 (JET_paramDatabasePageSize) 之資料庫頁面大小的功能。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-182">This parameter may also be set to a larger value as a function of the database page size for the instance (JET_paramDatabasePageSize).</span></span> <span data-ttu-id="9bb9c-183">如需詳細資訊，請參閱 JET_paramKeyMost。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-183">See JET_paramKeyMost for more information.</span></span>

<span data-ttu-id="9bb9c-184">**cbVarSegMac**</span><span class="sxs-lookup"><span data-stu-id="9bb9c-184">**cbVarSegMac**</span></span>

<span data-ttu-id="9bb9c-185">將從任何可變長度資料行使用的最大資料量，以針對指定的資料列來建立索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-185">The maximum amount of data that will be used from any variable length column to construct a key for a given row.</span></span>

<span data-ttu-id="9bb9c-186">此參數可用來控制任何指定的索引鍵資料行所耗用的金鑰空間量。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-186">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="9bb9c-187">這項限制是以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-187">This limit is in bytes.</span></span> <span data-ttu-id="9bb9c-188">如果此參數為零或與 *cbKeyMost* 參數相同，則沒有作用中的限制。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-188">If this parameter is zero or is the same as the *cbKeyMost* parameter then no limit is in effect.</span></span>

<span data-ttu-id="9bb9c-189">**tableid**</span><span class="sxs-lookup"><span data-stu-id="9bb9c-189">**tableid**</span></span>

<span data-ttu-id="9bb9c-190">由於成功呼叫 [JetOpenTemporaryTable](./jetopentemporarytable-function.md)而建立之臨時表的資料表控制碼。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-190">The table handle for the temporary table created as a result of a successful call to [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="9bb9c-191">規格需求</span><span class="sxs-lookup"><span data-stu-id="9bb9c-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bb9c-192"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="9bb9c-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9bb9c-193">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-193">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bb9c-194"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="9bb9c-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9bb9c-195">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-195">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bb9c-196"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="9bb9c-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9bb9c-197">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="9bb9c-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9bb9c-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bb9c-198">See Also</span></span>

[<span data-ttu-id="9bb9c-199">JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="9bb9c-199">JET_TABLECREATE</span></span>](./jet-tablecreate-structure.md)  
[<span data-ttu-id="9bb9c-200">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="9bb9c-200">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="9bb9c-201">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="9bb9c-201">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="9bb9c-202">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9bb9c-202">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9bb9c-203">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9bb9c-203">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="9bb9c-204">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9bb9c-204">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9bb9c-205">JetOpenTemporaryTable</span><span class="sxs-lookup"><span data-stu-id="9bb9c-205">JetOpenTemporaryTable</span></span>](./jetopentemporarytable-function.md)  
[<span data-ttu-id="9bb9c-206">可擴充儲存引擎系統參數</span><span class="sxs-lookup"><span data-stu-id="9bb9c-206">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
