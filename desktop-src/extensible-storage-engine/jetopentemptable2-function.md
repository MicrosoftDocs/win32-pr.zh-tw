---
description: 深入瞭解： JetOpenTempTable2 函數
title: JetOpenTempTable2 函式
TOCTitle: JetOpenTempTable2 Function
ms:assetid: 788ec4f9-b0c3-409b-850c-7567dec47024
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269302(v=EXCHG.10)
ms:contentKeyID: 32765594
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 324bcde75c0ba9376c8ad9f5e98df585b1d341e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985268"
---
# <a name="jetopentemptable2-function"></a><span data-ttu-id="93e89-103">JetOpenTempTable2 函式</span><span class="sxs-lookup"><span data-stu-id="93e89-103">JetOpenTempTable2 Function</span></span>


<span data-ttu-id="93e89-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="93e89-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopentemptable2-function"></a><span data-ttu-id="93e89-105">JetOpenTempTable2 函式</span><span class="sxs-lookup"><span data-stu-id="93e89-105">JetOpenTempTable2 Function</span></span>

<span data-ttu-id="93e89-106">**JetOpenTempTable2** 函式會建立一個臨時表，其中包含可用於儲存和取出記錄的單一索引，就像使用 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)建立的一般資料表一樣。</span><span class="sxs-lookup"><span data-stu-id="93e89-106">The **JetOpenTempTable2** function creates a temporary table with a single index that can be used to store and retrieve records just like an ordinary table created using [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="93e89-107">此函數也有地區設定識別碼，可用於比較臨時表中的 Unicode 索引鍵資料行資料。</span><span class="sxs-lookup"><span data-stu-id="93e89-107">This function also has a Locale ID that can be used to compare Unicode key column data in the temporary table.</span></span> <span data-ttu-id="93e89-108">不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。</span><span class="sxs-lookup"><span data-stu-id="93e89-108">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="93e89-109">它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。</span><span class="sxs-lookup"><span data-stu-id="93e89-109">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span>

```cpp
    JET_ERR JET_API JetOpenTempTable2(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          unsigned long lcid,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="93e89-110">參數</span><span class="sxs-lookup"><span data-stu-id="93e89-110">Parameters</span></span>

<span data-ttu-id="93e89-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="93e89-111">*sesid*</span></span>

<span data-ttu-id="93e89-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="93e89-112">The session to use.</span></span>

<span data-ttu-id="93e89-113">*prgcolumndef*</span><span class="sxs-lookup"><span data-stu-id="93e89-113">*prgcolumndef*</span></span>

<span data-ttu-id="93e89-114">要在臨時表中建立之資料行的資料行定義。</span><span class="sxs-lookup"><span data-stu-id="93e89-114">The column definitions of the columns to be created in the temporary table.</span></span>

<span data-ttu-id="93e89-115">用於臨時表的資料行定義選項有重要的限制。</span><span class="sxs-lookup"><span data-stu-id="93e89-115">Important limitations exist for the column definition options that are used with a temporary table.</span></span> <span data-ttu-id="93e89-116">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="93e89-116">See the Remarks section for more information.</span></span>

<span data-ttu-id="93e89-117">除了一般資料行定義選項之外，也可以指定零或多個下列選項，這些選項只與臨時表的內容有關。</span><span class="sxs-lookup"><span data-stu-id="93e89-117">In addition to the usual column definition options, zero or more of the following options can also be specified that are relevant only in the context of a temporary table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93e89-118">值</span><span class="sxs-lookup"><span data-stu-id="93e89-118">Value</span></span></p></th>
<th><p><span data-ttu-id="93e89-119">意義</span><span class="sxs-lookup"><span data-stu-id="93e89-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93e89-120">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="93e89-120">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="93e89-121">臨時表之索引鍵資料行的排序次序應該是遞減的，而不是遞增的。</span><span class="sxs-lookup"><span data-stu-id="93e89-121">The sort order of the key column for the temporary table should be descending rather than ascending.</span></span> <span data-ttu-id="93e89-122">如果指定這個選項但未指定 JET_bitColumnTTKey 則會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="93e89-122">If this option is specified without JET_bitColumnTTKey then this option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-123">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="93e89-123">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="93e89-124">資料行將是臨時表的索引鍵資料行。</span><span class="sxs-lookup"><span data-stu-id="93e89-124">The column will be a key column for the temporary table.</span></span></p>
<p><span data-ttu-id="93e89-125">在輸入陣列中指定此選項的資料行定義順序，將會決定臨時表的每個索引鍵資料行的優先順序。</span><span class="sxs-lookup"><span data-stu-id="93e89-125">The order of the column definitions with this option specified in the input array will determine the precedence of each key column for the temporary table.</span></span> <span data-ttu-id="93e89-126">使用這個選項組的陣列中的第一個資料行定義將是最重要的索引鍵資料行，依此類推。</span><span class="sxs-lookup"><span data-stu-id="93e89-126">The first column definition in the array with this option set will be the most significant key column and so on.</span></span> <span data-ttu-id="93e89-127">如果要求的索引鍵資料行數目超過 database engine 所能支援的數量，則會忽略不受支援索引鍵資料行的這個選項。</span><span class="sxs-lookup"><span data-stu-id="93e89-127">If more key columns are requested than can be supported by the database engine then this option is ignored for the unsupportable key columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93e89-128">*ccolumn*</span><span class="sxs-lookup"><span data-stu-id="93e89-128">*ccolumn*</span></span>

<span data-ttu-id="93e89-129">請參閱 *prgcolumndef*。</span><span class="sxs-lookup"><span data-stu-id="93e89-129">See *prgcolumndef*.</span></span>

<span data-ttu-id="93e89-130">*lcid*</span><span class="sxs-lookup"><span data-stu-id="93e89-130">*lcid*</span></span>

<span data-ttu-id="93e89-131">用來比較臨時表中任何 Unicode 索引鍵資料行資料的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="93e89-131">The locale ID to use to compare any Unicode key column data in the temporary table.</span></span>

<span data-ttu-id="93e89-132">只要電腦上已安裝適當的語言套件，即可使用任何地區設定。</span><span class="sxs-lookup"><span data-stu-id="93e89-132">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="93e89-133">其中一個例外狀況是，非語言相關地區設定 (LCID 為零) 不合法。</span><span class="sxs-lookup"><span data-stu-id="93e89-133">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="93e89-134">在 Windows Server 2003 和更新版本中，如果為此參數指定非語言相關地區設定，則會改用預設的地區設定識別碼 (美式英文) 。</span><span class="sxs-lookup"><span data-stu-id="93e89-134">On Windows Server 2003 and later, if the Language Neutral locale is specified for this parameter then the default locale ID (U.S. English) will be used instead.</span></span> <span data-ttu-id="93e89-135">這是為了允許零值表示預設值，而不是不合法的值。</span><span class="sxs-lookup"><span data-stu-id="93e89-135">This is to allow a value of zero to signify the default rather than an illegal value.</span></span>

<span data-ttu-id="93e89-136">如果這個參數不存在，且 *pidxunicode* 參數不存在，則會使用預設的 LCID 來比較臨時表中的任何 Unicode 索引鍵資料行資料。</span><span class="sxs-lookup"><span data-stu-id="93e89-136">When this parameter is not present and when the *pidxunicode* parameter is not present, then the default LCID will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="93e89-137">預設的 LCID 是美國英文地區設定。</span><span class="sxs-lookup"><span data-stu-id="93e89-137">The default LCID is the U.S. English locale.</span></span>

<span data-ttu-id="93e89-138">*grbit*</span><span class="sxs-lookup"><span data-stu-id="93e89-138">*grbit*</span></span>

<span data-ttu-id="93e89-139">位群組，其中包含要用於此呼叫的選項，包括下列零或多個。</span><span class="sxs-lookup"><span data-stu-id="93e89-139">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93e89-140">值</span><span class="sxs-lookup"><span data-stu-id="93e89-140">Value</span></span></p></th>
<th><p><span data-ttu-id="93e89-141">意義</span><span class="sxs-lookup"><span data-stu-id="93e89-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93e89-142">JET_bitTTErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="93e89-142">JET_bitTTErrorOnDuplicateInsertion</span></span></p></td>
<td><p><span data-ttu-id="93e89-143">此選項會要求任何嘗試插入具有與先前所插入記錄相同索引鍵的記錄，但 JET_errKeyDuplicate 會立即失敗。</span><span class="sxs-lookup"><span data-stu-id="93e89-143">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with JET_errKeyDuplicate.</span></span> <span data-ttu-id="93e89-144">如果未要求這個選項，則可能會立即偵測到重複的情況，也可能會在稍後根據資料庫引擎根據所要求的功能來執行臨時表所選擇的策略，而失敗或以無訊息方式移除。</span><span class="sxs-lookup"><span data-stu-id="93e89-144">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span></p>
<p><span data-ttu-id="93e89-145">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="93e89-145">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="93e89-146">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="93e89-146">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-147">JET_bitTTForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="93e89-147">JET_bitTTForceMaterialization</span></span></p></td>
<td><p><span data-ttu-id="93e89-148">此選項會強制臨時表管理員放棄任何嘗試選擇聰明的策略來管理臨時表，以產生增強的效能。</span><span class="sxs-lookup"><span data-stu-id="93e89-148">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-149">JET_bitTTForwardOnly</span><span class="sxs-lookup"><span data-stu-id="93e89-149">JET_bitTTForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="93e89-150">如果臨時表管理員可以使用針對中繼查詢結果優化的執行，此選項會要求只建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="93e89-150">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="93e89-151">如果臨時表的任何特性會防止使用這項優化，則作業會失敗並 JET_errCannotMaterializeForwardOnlySort。</span><span class="sxs-lookup"><span data-stu-id="93e89-151">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span></p>
<p><span data-ttu-id="93e89-152">此選項的副作用是允許臨時表包含具有重複索引鍵的記錄。</span><span class="sxs-lookup"><span data-stu-id="93e89-152">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="93e89-153">如需詳細資訊，請參閱 JET_bitTTUnique。</span><span class="sxs-lookup"><span data-stu-id="93e89-153">See JET_bitTTUnique for more information.</span></span></p>
<p><span data-ttu-id="93e89-154">此選項僅適用于 Windows Server 2003 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="93e89-154">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-155">JET_bitTTIndexed</span><span class="sxs-lookup"><span data-stu-id="93e89-155">JET_bitTTIndexed</span></span></p></td>
<td><p><span data-ttu-id="93e89-156">此選項會要求臨時表具有足夠的彈性，可允許使用 <a href="gg294103(v=exchg.10).md">JetSeek</a> 依據索引鍵來查閱記錄。</span><span class="sxs-lookup"><span data-stu-id="93e89-156">This option requests that the temporary table be flexible enough to permit the use of <a href="gg294103(v=exchg.10).md">JetSeek</a> to look up records by index key.</span></span></p>
<p><span data-ttu-id="93e89-157">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="93e89-157">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="93e89-158">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="93e89-158">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-159">JET_bitTTScrollable</span><span class="sxs-lookup"><span data-stu-id="93e89-159">JET_bitTTScrollable</span></span></p></td>
<td><p><span data-ttu-id="93e89-160">此選項會要求臨時表具有足夠的彈性，可讓您以任意順序和使用 <a href="gg294117(v=exchg.10).md">JetMove</a>的方向來掃描記錄。</span><span class="sxs-lookup"><span data-stu-id="93e89-160">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p>
<p><span data-ttu-id="93e89-161">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="93e89-161">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="93e89-162">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="93e89-162">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-163">JET_bitTTSortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="93e89-163">JET_bitTTSortNullsHigh</span></span></p></td>
<td><p><span data-ttu-id="93e89-164">此選項會要求 Null 索引鍵資料行值的排序比非 Null 索引鍵資料行值更接近索引的結尾。</span><span class="sxs-lookup"><span data-stu-id="93e89-164">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-165">JET_bitTTUnique</span><span class="sxs-lookup"><span data-stu-id="93e89-165">JET_bitTTUnique</span></span></p></td>
<td><p><span data-ttu-id="93e89-166">此選項會要求從臨時表的最後一組記錄中，移除具有重複索引鍵的記錄。</span><span class="sxs-lookup"><span data-stu-id="93e89-166">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span></p>
<p><span data-ttu-id="93e89-167">在 Windows Server 2003 之前，資料庫引擎一律會假設這個選項有作用，因為所有叢集索引也必須是主鍵，因此必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="93e89-167">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="93e89-168">從 Windows Server 2003 開始，當同時指定 JET_bitTTForwardOnly 選項時，現在可以建立不會移除重複專案的臨時表。</span><span class="sxs-lookup"><span data-stu-id="93e89-168">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the JET_bitTTForwardOnly option is also specified.</span></span></p>
<p><span data-ttu-id="93e89-169">您無法知道哪些重複專案會獲勝，哪些重複專案會在一般情況下捨棄。</span><span class="sxs-lookup"><span data-stu-id="93e89-169">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="93e89-170">不過，當要求 JET_bitTTErrorOnDuplicateInsertion 選項時，會永遠贏得具有指定索引鍵的第一個記錄插入臨時表中。</span><span class="sxs-lookup"><span data-stu-id="93e89-170">However, when the JET_bitTTErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-171">JET_bitTTUpdatable</span><span class="sxs-lookup"><span data-stu-id="93e89-171">JET_bitTTUpdatable</span></span></p></td>
<td><p><span data-ttu-id="93e89-172">此選項會要求臨時表具有足夠的彈性，可讓之前插入的記錄之後變更。</span><span class="sxs-lookup"><span data-stu-id="93e89-172">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="93e89-173">如果這項功能不是必要的，則最好不要要求它。</span><span class="sxs-lookup"><span data-stu-id="93e89-173">If this functionality it not required then it is best to not request it.</span></span></p>
<p><span data-ttu-id="93e89-174">如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</span><span class="sxs-lookup"><span data-stu-id="93e89-174">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-175">JET_bitTTIntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="93e89-175">JET_bitTTIntrinsicLVsOnly</span></span></p></td>
<td><p><span data-ttu-id="93e89-176">要求只允許內建的 long 值。</span><span class="sxs-lookup"><span data-stu-id="93e89-176">Requests to permit only intrinsic long values.</span></span></p>
<p><span data-ttu-id="93e89-177"><strong>Windows 7</strong>： <strong>JET_bitTTIntrinsicLVsOnly</strong> 是在 windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="93e89-177"><strong>Windows 7</strong>: <strong>JET_bitTTIntrinsicLVsOnly</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93e89-178">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="93e89-178">*ptableid*</span></span>

<span data-ttu-id="93e89-179">將接收新建立的臨時表上開啟之新資料指標的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="93e89-179">The output buffer that will receive the new cursor opened on the newly created temporary table.</span></span>

<span data-ttu-id="93e89-180">*prgcolumnid*</span><span class="sxs-lookup"><span data-stu-id="93e89-180">*prgcolumnid*</span></span>

<span data-ttu-id="93e89-181">輸出緩衝區，將會接收建立臨時表時所產生之資料行識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="93e89-181">The output buffer that will receive the array of column IDs generated during the creation of the temporary table.</span></span>

<span data-ttu-id="93e89-182">此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。</span><span class="sxs-lookup"><span data-stu-id="93e89-182">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="93e89-183">因此，這個緩衝區的大小必須對應到輸入陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="93e89-183">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

### <a name="return-value"></a><span data-ttu-id="93e89-184">傳回值</span><span class="sxs-lookup"><span data-stu-id="93e89-184">Return Value</span></span>

<span data-ttu-id="93e89-185">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="93e89-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="93e89-186">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="93e89-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93e89-187">傳回碼</span><span class="sxs-lookup"><span data-stu-id="93e89-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="93e89-188">Description</span><span class="sxs-lookup"><span data-stu-id="93e89-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93e89-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="93e89-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="93e89-190">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="93e89-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-191">JET_errCannotMaterializeForwardOnlySort</span><span class="sxs-lookup"><span data-stu-id="93e89-191">JET_errCannotMaterializeForwardOnlySort</span></span></p></td>
<td><p><span data-ttu-id="93e89-192"><strong>JetOpenTempTable2</strong> 失敗，因為指定了 JET_bitTTForwardOnly，而且無法使用順向優化來建立指定的臨時表。</span><span class="sxs-lookup"><span data-stu-id="93e89-192"><strong>JetOpenTempTable2</strong> failed because JET_bitTTForwardOnly was specified and the temporary table as specified could not be created using the forward-only optimization.</span></span> <span data-ttu-id="93e89-193">只有 Windows Server 2003 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="93e89-193">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-194">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="93e89-194">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="93e89-195">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="93e89-195">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-196">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="93e89-196">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="93e89-197">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="93e89-197">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="93e89-198">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="93e89-198">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-199">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="93e89-199">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="93e89-200"><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>的 [cp] 欄位未設定為有效的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="93e89-200">The cp field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid code page.</span></span> <span data-ttu-id="93e89-201">Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。</span><span class="sxs-lookup"><span data-stu-id="93e89-201">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="93e89-202">0值表示預設值將使用 (英文、1252) 。</span><span class="sxs-lookup"><span data-stu-id="93e89-202">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-203">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="93e89-203">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="93e89-204"><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>的<em>coltyp</em>欄位未設定為有效的資料行類型。</span><span class="sxs-lookup"><span data-stu-id="93e89-204">The <em>coltyp</em> field of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-205">JET_errIndexInvalidDef</span><span class="sxs-lookup"><span data-stu-id="93e89-205">JET_errIndexInvalidDef</span></span></p></td>
<td><p><span data-ttu-id="93e89-206">無法建立索引，因為指定了不正確索引定義。</span><span class="sxs-lookup"><span data-stu-id="93e89-206">The index could not be created because an invalid index definition was specified.</span></span></p>
<p><span data-ttu-id="93e89-207"><strong>JetOpenTempTable2</strong> 會在下列情況傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="93e89-207"><strong>JetOpenTempTable2</strong> will return this error when:</span></span></p>
<ul>
<li><p><span data-ttu-id="93e89-208">指定了中性語言的地區設定。</span><span class="sxs-lookup"><span data-stu-id="93e89-208">The Language Neutral locale is specified.</span></span></p></li>
<li><p><span data-ttu-id="93e89-209">指定了不正確正規化旗標集合。</span><span class="sxs-lookup"><span data-stu-id="93e89-209">An invalid set of normalization flags is specified.</span></span></p></li>
</ul>
<p><span data-ttu-id="93e89-210">此錯誤只會由 Windows 2000 傳回。</span><span class="sxs-lookup"><span data-stu-id="93e89-210">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-211">JET_errInvalidLanguageId</span><span class="sxs-lookup"><span data-stu-id="93e89-211">JET_errInvalidLanguageId</span></span></p></td>
<td><p><span data-ttu-id="93e89-212">無法建立索引，因為嘗試使用不正確地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="93e89-212">The index could not be created because an attempt was made to use an invalid locale ID.</span></span> <span data-ttu-id="93e89-213">地區設定識別碼可能完全無效，或可能未安裝相關聯的語言套件。</span><span class="sxs-lookup"><span data-stu-id="93e89-213">The locale ID may either be completely invalid or the associated language pack may not be installed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-214">JET_errInvalidLCMapStringFlags</span><span class="sxs-lookup"><span data-stu-id="93e89-214">JET_errInvalidLCMapStringFlags</span></span></p></td>
<td><p><span data-ttu-id="93e89-215">無法建立索引，因為嘗試使用一組不正確正規化旗標。</span><span class="sxs-lookup"><span data-stu-id="93e89-215">The index could not be created because an attempt was made to use an invalid set of normalization flags.</span></span> <span data-ttu-id="93e89-216">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="93e89-216">This error will only be returned by Windows XP and later releases.</span></span> <span data-ttu-id="93e89-217">在 Windows 2000 上，不正確正規化旗標會改為產生 JET_errIndexInvalidDef。</span><span class="sxs-lookup"><span data-stu-id="93e89-217">On Windows 2000, invalid normalization flags will result in JET_errIndexInvalidDef instead.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-218">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="93e89-218">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="93e89-219">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="93e89-219">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-220">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="93e89-220">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="93e89-221">作業失敗，因為引擎無法配置開啟新資料指標所需的資源。</span><span class="sxs-lookup"><span data-stu-id="93e89-221">The operation failed because the engine cannot allocate the resources required to open a new cursor.</span></span> <span data-ttu-id="93e89-222">資料指標資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>進行設定。</span><span class="sxs-lookup"><span data-stu-id="93e89-222">Cursor resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-223">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="93e89-223">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="93e89-224">作業失敗，因為無法配置足夠的記憶體來完成。</span><span class="sxs-lookup"><span data-stu-id="93e89-224">The operation failed because not enough memory could be allocated to complete it.</span></span></p>
<p><span data-ttu-id="93e89-225">如果主機進程的位址空間變得太分散， <strong>JetOpenTempTable2</strong>可能會傳回 JET_errOutOfMemory。</span><span class="sxs-lookup"><span data-stu-id="93e89-225"><strong>JetOpenTempTable2</strong> can return JET_errOutOfMemory if the address space of the host process becomes too fragmented.</span></span> <span data-ttu-id="93e89-226">無論要儲存的資料量為何，臨時表管理員一律會為每個建立的臨時表配置1MB 的位址空間區塊。</span><span class="sxs-lookup"><span data-stu-id="93e89-226">The temporary table manager will always allocate a 1MB chunk of address space for every temporary table created regardless of the amount of data to be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-227">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="93e89-227">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="93e89-228">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="93e89-228">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-229">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="93e89-229">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="93e89-230">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="93e89-230">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="93e89-231">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="93e89-231">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-232">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="93e89-232">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="93e89-233">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="93e89-233">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-234">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="93e89-234">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="93e89-235">嘗試將過多的資料行新增至資料表。</span><span class="sxs-lookup"><span data-stu-id="93e89-235">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="93e89-236">資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</span><span class="sxs-lookup"><span data-stu-id="93e89-236">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-237">JET_errTooManyOpenIndexes</span><span class="sxs-lookup"><span data-stu-id="93e89-237">JET_errTooManyOpenIndexes</span></span></p></td>
<td><p><span data-ttu-id="93e89-238">作業失敗，因為引擎無法配置快取資料表索引所需的資源。</span><span class="sxs-lookup"><span data-stu-id="93e89-238">The operation failed because the engine cannot allocate the resources required to cache the indexes of the table.</span></span> <span data-ttu-id="93e89-239">您可以使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>，設定可以快取架構的索引數目。</span><span class="sxs-lookup"><span data-stu-id="93e89-239">The number of indexes whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-240">JET_errTooManyOpenTables</span><span class="sxs-lookup"><span data-stu-id="93e89-240">JET_errTooManyOpenTables</span></span></p></td>
<td><p><span data-ttu-id="93e89-241">作業失敗，因為引擎無法配置快取資料表架構所需的資源。</span><span class="sxs-lookup"><span data-stu-id="93e89-241">The operation failed because the engine cannot allocate the resources required to cache the schema of the table.</span></span> <span data-ttu-id="93e89-242">您可以使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>，設定可以快取架構的資料表數目。</span><span class="sxs-lookup"><span data-stu-id="93e89-242">The number of tables whose schema can be cached is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-243">JET_errTooManySorts</span><span class="sxs-lookup"><span data-stu-id="93e89-243">JET_errTooManySorts</span></span></p></td>
<td><p><span data-ttu-id="93e89-244">作業失敗，因為引擎無法配置建立臨時表所需的資源。</span><span class="sxs-lookup"><span data-stu-id="93e89-244">The operation failed because the engine cannot allocate the resources required to create a temporary table.</span></span> <span data-ttu-id="93e89-245">臨時表資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>進行設定。</span><span class="sxs-lookup"><span data-stu-id="93e89-245">Temporary table resources are configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93e89-246">成功時，會傳回在新建立的臨時表上開啟的資料指標。</span><span class="sxs-lookup"><span data-stu-id="93e89-246">On success, a cursor opened on the newly created temporary table will be returned.</span></span> <span data-ttu-id="93e89-247">暫存資料庫的狀態將準備好包含新的臨時表。</span><span class="sxs-lookup"><span data-stu-id="93e89-247">The state of the temporary database will be prepared to contain the new temporary table.</span></span> <span data-ttu-id="93e89-248">資料庫引擎所使用之任何一般資料庫的狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="93e89-248">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

<span data-ttu-id="93e89-249">失敗時，將不會建立臨時表，也不會傳回資料指標。</span><span class="sxs-lookup"><span data-stu-id="93e89-249">On failure, the temporary table will not be created and a cursor will not be returned.</span></span> <span data-ttu-id="93e89-250">暫存資料庫的狀態可能會變更。</span><span class="sxs-lookup"><span data-stu-id="93e89-250">The state of the temporary database may be changed.</span></span> <span data-ttu-id="93e89-251">資料庫引擎所使用之任何一般資料庫的狀態將保持不變。</span><span class="sxs-lookup"><span data-stu-id="93e89-251">The state of any ordinary databases in use by the database engine will remain unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="93e89-252">備註</span><span class="sxs-lookup"><span data-stu-id="93e89-252">Remarks</span></span>

<span data-ttu-id="93e89-253">請參閱 [JetOpenTempTable](./jetopentemptable-function.md)。</span><span class="sxs-lookup"><span data-stu-id="93e89-253">See [JetOpenTempTable](./jetopentemptable-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="93e89-254">規格需求</span><span class="sxs-lookup"><span data-stu-id="93e89-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93e89-255"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="93e89-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="93e89-256">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="93e89-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-257"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="93e89-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="93e89-258">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="93e89-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-259"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="93e89-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="93e89-260">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="93e89-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93e89-261"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="93e89-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="93e89-262">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="93e89-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93e89-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="93e89-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="93e89-264">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="93e89-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="93e89-265">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93e89-265">See Also</span></span>

[<span data-ttu-id="93e89-266">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="93e89-266">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="93e89-267">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="93e89-267">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="93e89-268">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="93e89-268">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="93e89-269">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="93e89-269">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="93e89-270">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="93e89-270">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="93e89-271">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="93e89-271">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="93e89-272">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="93e89-272">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="93e89-273">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="93e89-273">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="93e89-274">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="93e89-274">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="93e89-275">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="93e89-275">JetDupCursor</span></span>](./jetdupcursor-function.md)  
[<span data-ttu-id="93e89-276">JetMove</span><span class="sxs-lookup"><span data-stu-id="93e89-276">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="93e89-277">JetRollback</span><span class="sxs-lookup"><span data-stu-id="93e89-277">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="93e89-278">JetSeek</span><span class="sxs-lookup"><span data-stu-id="93e89-278">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="93e89-279">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="93e89-279">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="93e89-280">系統參數</span><span class="sxs-lookup"><span data-stu-id="93e89-280">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
