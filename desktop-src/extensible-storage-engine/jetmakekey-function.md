---
description: 深入瞭解： JetMakeKey 函數
title: JetMakeKey 函式
TOCTitle: JetMakeKey Function
ms:assetid: 8c1cff2f-2f24-4990-a9d8-fb4f822e50b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269329(v=EXCHG.10)
ms:contentKeyID: 32765619
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMakeKey
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e3d121ed83f096baad249aab8677bb9f5e72e301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194595"
---
# <a name="jetmakekey-function"></a><span data-ttu-id="c84be-103">JetMakeKey 函式</span><span class="sxs-lookup"><span data-stu-id="c84be-103">JetMakeKey Function</span></span>


<span data-ttu-id="c84be-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c84be-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetmakekey-function"></a><span data-ttu-id="c84be-105">JetMakeKey 函式</span><span class="sxs-lookup"><span data-stu-id="c84be-105">JetMakeKey Function</span></span>

<span data-ttu-id="c84be-106">**JetMakeKey** 函式會先建立搜尋索引鍵，然後在索引鍵資料行值上使用一些簡單的搜尋準則來尋找索引中的一組專案。</span><span class="sxs-lookup"><span data-stu-id="c84be-106">The **JetMakeKey** function constructs search keys that may then be used to find a set of entries in an index by some simple search criteria on their key column values.</span></span> <span data-ttu-id="c84be-107">搜尋索引鍵也是資料指標的其中一個內建屬性，並由 [JetSeek](./jetseek-function.md) 和 [JetSetIndexRange](./jetsetindexrange-function.md) 作業用來尋找符合該資料指標目前索引之這些搜尋準則的索引項目。</span><span class="sxs-lookup"><span data-stu-id="c84be-107">A search key is also one of the intrinsic properties of a cursor and is used by the [JetSeek](./jetseek-function.md) and [JetSetIndexRange](./jetsetindexrange-function.md) operations to locate index entries matching these search criteria on the current index of that cursor.</span></span> <span data-ttu-id="c84be-108">完整的搜尋索引鍵會在一系列的 **JetMakeKey** 呼叫中建立，其中每個呼叫都是用來載入資料指標目前索引之下一個索引鍵資料行的資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-108">A complete search key is built up in a series of **JetMakeKey** calls where each call is used to load the column value for the next key column of the current index of a cursor.</span></span> <span data-ttu-id="c84be-109">您也可以載入先前使用 [JetRetrieveKey](./jetretrievekey-function.md)從資料指標抓取的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c84be-109">It is also possible to load a previously constructed search key that has been retrieved from the cursor using [JetRetrieveKey](./jetretrievekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetMakeKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c84be-110">參數</span><span class="sxs-lookup"><span data-stu-id="c84be-110">Parameters</span></span>

<span data-ttu-id="c84be-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c84be-111">*sesid*</span></span>

<span data-ttu-id="c84be-112">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="c84be-112">The session to use for this call.</span></span>

<span data-ttu-id="c84be-113">*tableid*</span><span class="sxs-lookup"><span data-stu-id="c84be-113">*tableid*</span></span>

<span data-ttu-id="c84be-114">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="c84be-114">The cursor to use for this call.</span></span>

<span data-ttu-id="c84be-115">*pvData*</span><span class="sxs-lookup"><span data-stu-id="c84be-115">*pvData*</span></span>

<span data-ttu-id="c84be-116">輸入緩衝區，其中包含要為其建立搜尋索引鍵之資料指標目前索引鍵資料行的資料行資料。</span><span class="sxs-lookup"><span data-stu-id="c84be-116">The input buffer containing the column data for the current key column of the current index of the cursor for which the search key is being constructed.</span></span>

<span data-ttu-id="c84be-117">輸入緩衝區中資料行資料的資料類型必須完全符合目前索引鍵資料行之資料行定義的資料類型和其他屬性。</span><span class="sxs-lookup"><span data-stu-id="c84be-117">The data type of the column data in the input buffer must exactly match the data type and other properties of the column definition of the current key column.</span></span> <span data-ttu-id="c84be-118">在資料行資料上不會執行任何類型強制型轉。</span><span class="sxs-lookup"><span data-stu-id="c84be-118">No type coercion is performed on the column data whatsoever.</span></span>

<span data-ttu-id="c84be-119">如果在 *grbit* 參數中指定 JET_bitNormalizedKey，輸入緩衝區必須包含先前已建立的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c84be-119">If JET_bitNormalizedKey is specified in the *grbit* parameter, the input buffer must contain a previously constructed search key.</span></span> <span data-ttu-id="c84be-120">這類金鑰是使用 [JetRetrieveKey](./jetretrievekey-function.md)呼叫所取得。</span><span class="sxs-lookup"><span data-stu-id="c84be-120">Such keys are obtained using a call to [JetRetrieveKey](./jetretrievekey-function.md).</span></span>

<span data-ttu-id="c84be-121">*cbData*</span><span class="sxs-lookup"><span data-stu-id="c84be-121">*cbData*</span></span>

<span data-ttu-id="c84be-122">輸入緩衝區中提供之資料行資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c84be-122">The size in bytes of the column data provided in the input buffer.</span></span>

<span data-ttu-id="c84be-123">如果在 *grbit* 參數中指定 JET_bitNormalizedKey，這就是輸入緩衝區中提供的搜尋索引鍵大小。</span><span class="sxs-lookup"><span data-stu-id="c84be-123">If JET_bitNormalizedKey is specified in the *grbit* parameter, this is the size of the search key provided in the input buffer.</span></span>

<span data-ttu-id="c84be-124">如果資料行資料的大小為零，則會忽略輸入緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="c84be-124">If the size of the column data is zero then the contents of the input buffer are ignored.</span></span> <span data-ttu-id="c84be-125">如果在 *grbit* 參數中指定了 JET_bitKeyDataZeroLength，而且目前的資料指標索引鍵資料行是可變長度資料行，則輸入資料行的資料會假設為零長度的值。</span><span class="sxs-lookup"><span data-stu-id="c84be-125">If JET_bitKeyDataZeroLength is specified in the *grbit* parameter and the current key column of the current index of the cursor is a variable length column, the input column data is presumed to be a zero length value.</span></span> <span data-ttu-id="c84be-126">否則，輸入資料行資料會假設為 Null 值。</span><span class="sxs-lookup"><span data-stu-id="c84be-126">Otherwise, the input column data is presumed to be a NULL value.</span></span>

<span data-ttu-id="c84be-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c84be-127">*grbit*</span></span>

<span data-ttu-id="c84be-128">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="c84be-128">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c84be-129">值</span><span class="sxs-lookup"><span data-stu-id="c84be-129">Value</span></span></p></th>
<th><p><span data-ttu-id="c84be-130">意義</span><span class="sxs-lookup"><span data-stu-id="c84be-130">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c84be-131">JET_bitFullColumnEndLimit</span><span class="sxs-lookup"><span data-stu-id="c84be-131">JET_bitFullColumnEndLimit</span></span></p></td>
<td><p><span data-ttu-id="c84be-132">搜尋索引鍵的建立方式，是在目前的索引鍵資料行之後的任何索引鍵資料行都會被視為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="c84be-132">The search key should be constructed in such a way that any key columns that come after the current key column are considered to be wildcards.</span></span> <span data-ttu-id="c84be-133">這表示，您可以使用已建立的搜尋索引鍵來比對具有下列專案的索引項目：</span><span class="sxs-lookup"><span data-stu-id="c84be-133">This means that the constructed search key can be used to match index entries that have the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c84be-134">為此索引鍵資料行和所有先前的索引鍵資料行提供的確切資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-134">The exact column values provided for this key column and all previous key columns.</span></span></p></li>
<li><p><span data-ttu-id="c84be-135">後續索引鍵資料行所需的任何資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-135">Any column values needed for subsequent key columns.</span></span></p></li>
</ul>
<p><span data-ttu-id="c84be-136">建立萬用字元搜尋索引鍵以用來尋找最接近索引結尾的索引項目時，應使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-136">This option should be used when building wildcard search keys to use for finding index entries closest to the end of an index.</span></span> <span data-ttu-id="c84be-137">索引的結尾是移至該索引中的最後一筆記錄時，所找到的索引項目。</span><span class="sxs-lookup"><span data-stu-id="c84be-137">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="c84be-138">索引的結尾與索引的高端不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</span><span class="sxs-lookup"><span data-stu-id="c84be-138">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="c84be-139">此選項僅適用于 Windows XP 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="c84be-139">This option is only available on Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-140">JETbitFullColumnStartLimit</span><span class="sxs-lookup"><span data-stu-id="c84be-140">JETbitFullColumnStartLimit</span></span></p></td>
<td><p><span data-ttu-id="c84be-141">應將搜尋索引鍵的結構化，以便在目前的索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="c84be-141">The search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span> <span data-ttu-id="c84be-142">這表示，您可以使用已建立的搜尋索引鍵來比對具有下列專案的索引項目：</span><span class="sxs-lookup"><span data-stu-id="c84be-142">This means that the constructed search key can be used to match index entries that have the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c84be-143">為此索引鍵資料行和所有先前的索引鍵資料行提供的確切資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-143">The exact column values provided for this key column and all previous key columns.</span></span></p></li>
<li><p><span data-ttu-id="c84be-144">後續索引鍵資料行所需的任何資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-144">Any column values needed for subsequent key columns.</span></span></p></li>
</ul>
<p><span data-ttu-id="c84be-145">建立萬用字元搜尋索引鍵以用來尋找最接近索引開頭的索引項目時，應使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-145">This option should be used when building wildcard search keys to use for finding index entries closest to the start of an index.</span></span> <span data-ttu-id="c84be-146">索引的開頭是移至該索引中的第一筆記錄時，所找到的索引項目。</span><span class="sxs-lookup"><span data-stu-id="c84be-146">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="c84be-147">索引的開頭與索引的下限不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</span><span class="sxs-lookup"><span data-stu-id="c84be-147">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="c84be-148">此選項僅適用于 Windows XP 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="c84be-148">This option is only available on Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84be-149">JET_bitKeyDataZeroLength</span><span class="sxs-lookup"><span data-stu-id="c84be-149">JET_bitKeyDataZeroLength</span></span></p></td>
<td><p><span data-ttu-id="c84be-150">如果輸入緩衝區的大小為零，且目前的索引鍵資料行是可變長度資料行，則此選項表示輸入緩衝區包含零長度的值。</span><span class="sxs-lookup"><span data-stu-id="c84be-150">If the size of the input buffer is zero and the current key column is a variable length column, this option indicates that the input buffer contains a zero length value.</span></span> <span data-ttu-id="c84be-151">否則，輸入緩衝區大小為零會指出 Null 值。</span><span class="sxs-lookup"><span data-stu-id="c84be-151">Otherwise, an input buffer size of zero would indicate a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-152">JET_bitNewKey</span><span class="sxs-lookup"><span data-stu-id="c84be-152">JET_bitNewKey</span></span></p></td>
<td><p><span data-ttu-id="c84be-153">應建立新的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c84be-153">A new search key should be constructed.</span></span> <span data-ttu-id="c84be-154">任何先前現有的搜尋金鑰都會被捨棄。</span><span class="sxs-lookup"><span data-stu-id="c84be-154">Any previously existing search key is discarded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84be-155">JET_bitNormalizedKey</span><span class="sxs-lookup"><span data-stu-id="c84be-155">JET_bitNormalizedKey</span></span></p></td>
<td><p><span data-ttu-id="c84be-156">指定此選項時，會忽略所有其他選項，任何先前現有的搜尋金鑰都會被捨棄，而輸入緩衝區的內容會載入為新的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c84be-156">When this option is specified, all other options are ignored, any previously existing search key is discarded, and the contents of the input buffer are loaded as the new search key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-157">JET_bitPartialColumnEndLimit</span><span class="sxs-lookup"><span data-stu-id="c84be-157">JET_bitPartialColumnEndLimit</span></span></p></td>
<td><p><span data-ttu-id="c84be-158">應建立搜尋索引鍵，讓目前的索引鍵資料行被視為首碼萬用字元，且在目前索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="c84be-158">The search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span> <span data-ttu-id="c84be-159">這表示，您可以使用已建立的搜尋索引鍵來比對具有下列專案的索引項目：</span><span class="sxs-lookup"><span data-stu-id="c84be-159">This means that the constructed search key can be used to match index entries that have the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c84be-160">為此索引鍵資料行和所有先前的索引鍵資料行提供的確切資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-160">The exact column values provided for this key column and all previous key columns.</span></span></p></li>
<li><p><span data-ttu-id="c84be-161">後續索引鍵資料行所需的任何資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-161">Any column values needed for subsequent key columns.</span></span></p></li>
</ul>
<p><span data-ttu-id="c84be-162">建立萬用字元搜尋索引鍵以用來尋找最接近索引結尾的索引項目時，應使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-162">This option should be used when building wildcard search keys to use for finding index entries closest to the end of an index.</span></span> <span data-ttu-id="c84be-163">索引的結尾是移至該索引中的最後一筆記錄時，所找到的索引項目。</span><span class="sxs-lookup"><span data-stu-id="c84be-163">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="c84be-164">索引的結尾與索引的高端不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</span><span class="sxs-lookup"><span data-stu-id="c84be-164">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="c84be-165">當目前的索引鍵資料行不是文字資料行或變數二進位資料行時，就無法使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-165">This option cannot be used when the current key column is not a text column or a variable binary column.</span></span> <span data-ttu-id="c84be-166">如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</span><span class="sxs-lookup"><span data-stu-id="c84be-166">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p>
<p><span data-ttu-id="c84be-167">此選項僅適用于 Windows XP 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="c84be-167">This option is only available on Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84be-168">JET_bitPartialColumnStartLimit</span><span class="sxs-lookup"><span data-stu-id="c84be-168">JET_bitPartialColumnStartLimit</span></span></p></td>
<td><p><span data-ttu-id="c84be-169">此選項表示應建立搜尋索引鍵，讓目前的索引鍵資料行被視為首碼萬用字元，且在目前索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="c84be-169">This option indicates that the search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span> <span data-ttu-id="c84be-170">這表示，您可以使用已建立的搜尋索引鍵來比對具有下列專案的索引項目：</span><span class="sxs-lookup"><span data-stu-id="c84be-170">This means that the constructed search key can be used to match index entries that have the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c84be-171">為此索引鍵資料行和所有先前的索引鍵資料行提供的確切資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-171">The exact column values provided for this key column and all previous key columns.</span></span></p></li>
<li><p><span data-ttu-id="c84be-172">後續索引鍵資料行所需的任何資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-172">Any column values needed for subsequent key columns.</span></span></p></li>
</ul>
<p><span data-ttu-id="c84be-173">建立萬用字元搜尋索引鍵以用來尋找最接近索引開頭的索引項目時，應使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-173">This option should be used when building wildcard search keys to use for finding index entries closest to the start of an index.</span></span> <span data-ttu-id="c84be-174">索引的開頭是移至該索引中的第一筆記錄時，所找到的索引項目。</span><span class="sxs-lookup"><span data-stu-id="c84be-174">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="c84be-175">索引的開頭與索引的下限不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</span><span class="sxs-lookup"><span data-stu-id="c84be-175">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="c84be-176">當目前的索引鍵資料行不是文字資料行或變數二進位資料行時，就無法使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-176">This option cannot be used when the current key column is not a text column or a variable binary column.</span></span> <span data-ttu-id="c84be-177">如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</span><span class="sxs-lookup"><span data-stu-id="c84be-177">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p>
<p><span data-ttu-id="c84be-178">此選項僅適用于 Windows XP 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="c84be-178">This option is only available on Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-179">JET_bitStrLimit</span><span class="sxs-lookup"><span data-stu-id="c84be-179">JET_bitStrLimit</span></span></p></td>
<td><p><span data-ttu-id="c84be-180">此選項表示應建立搜尋索引鍵，以便將目前索引鍵資料行後面的任何索引鍵資料行視為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="c84be-180">This option indicates that the search key should be constructed such that any key columns that come after the current key column should be considered to be wildcards.</span></span> <span data-ttu-id="c84be-181">這表示，您可以使用已建立的搜尋索引鍵來比對具有下列專案的索引項目：</span><span class="sxs-lookup"><span data-stu-id="c84be-181">This means that the constructed search key can be used to match index entries that have the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c84be-182">為此索引鍵資料行和所有先前的索引鍵資料行提供的確切資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-182">The exact column values provided for this key column and all previous key columns.</span></span></p></li>
<li><p><span data-ttu-id="c84be-183">後續索引鍵資料行所需的任何資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-183">Any column values needed for subsequent key columns.</span></span></p></li>
</ul>
<p><span data-ttu-id="c84be-184">建立萬用字元搜尋索引鍵以用來尋找最接近索引結尾的索引項目時，應使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-184">This option should be used when building wildcard search keys to use for finding index entries closest to the end of an index.</span></span> <span data-ttu-id="c84be-185">索引的結尾是移至該索引中的最後一筆記錄時，所找到的索引項目。</span><span class="sxs-lookup"><span data-stu-id="c84be-185">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="c84be-186">索引的結尾與索引的高端不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</span><span class="sxs-lookup"><span data-stu-id="c84be-186">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="c84be-187">當這個選項與 JET_bitSubStrLimit 一起指定，且目前的索引鍵資料行是文字資料行時，將會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-187">When this option is specified in combination with JET_bitSubStrLimit and the current key column is a text column, this option will be ignored.</span></span> <span data-ttu-id="c84be-188">此行為是為了允許在建立搜尋索引鍵時，推斷目前索引鍵資料行的類型。</span><span class="sxs-lookup"><span data-stu-id="c84be-188">This behavior is intended to allow the type of the current key column to be inferred when building the search key.</span></span></p>
<p><span data-ttu-id="c84be-189">如果您想要針對索引的開頭建立類似的搜尋索引鍵，則應該對不是萬用字元的最後一個索引鍵資料行進行類似的 <strong>JetMakeKey</strong> 呼叫，但不指定萬用字元選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-189">If you want to build a similar search key for the start of an index, a similar call to <strong>JetMakeKey</strong> should be made for the last key column that is not a wildcard, but with no wildcard options specified.</span></span> <span data-ttu-id="c84be-190">搜尋金鑰接著會處於適當的狀態，以用於這類搜尋。</span><span class="sxs-lookup"><span data-stu-id="c84be-190">The search key is then in an appropriate state to use for such a search.</span></span> <span data-ttu-id="c84be-191">這類似于使用 JET_bitFullColumnStartLimit，不同之處在于搜尋索引鍵未完全完成，因為它是在使用萬用字元選項之後。</span><span class="sxs-lookup"><span data-stu-id="c84be-191">This is analogous to using JET_bitFullColumnStartLimit, except that the search key is not cleanly finished as it is after the use of a wildcard option.</span></span></p>
<p><span data-ttu-id="c84be-192">此選項已在 Windows XP 和更新版本中被取代，以解決這項棘手的語義。</span><span class="sxs-lookup"><span data-stu-id="c84be-192">This option has been deprecated for Windows XP and later releases in order to address this awkward semantic.</span></span> <span data-ttu-id="c84be-193">應該盡可能使用 JET_bitFullColumnStartLimit 和 JET_bitFullColumnEndLimit。</span><span class="sxs-lookup"><span data-stu-id="c84be-193">JET_bitFullColumnStartLimit and JET_bitFullColumnEndLimit should be used instead wherever possible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84be-194">JET_bitSubStrLimit</span><span class="sxs-lookup"><span data-stu-id="c84be-194">JET_bitSubStrLimit</span></span></p></td>
<td><p><span data-ttu-id="c84be-195">此選項表示應建立搜尋索引鍵，讓目前的索引鍵資料行被視為首碼萬用字元，且在目前索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="c84be-195">This option indicates that the search key should be constructed such that the current key column is considered to be a prefix wildcard and that any key columns that come after the current key column should be considered to be wildcards.</span></span> <span data-ttu-id="c84be-196">這表示，您可以使用已建立的搜尋索引鍵來比對具有下列專案的索引項目：</span><span class="sxs-lookup"><span data-stu-id="c84be-196">This means that the constructed search key can be used to match index entries that have the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c84be-197">針對所有先前的索引鍵資料行提供的確切資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-197">The exact column values provided for all previous key columns.</span></span></p></li>
<li><p><span data-ttu-id="c84be-198">指定的資料行資料，做為目前索引鍵資料行之資料行值的前置詞。</span><span class="sxs-lookup"><span data-stu-id="c84be-198">The specified column data as a prefix of their column value for the current key column.</span></span></p></li>
<li><p><span data-ttu-id="c84be-199">後續索引鍵資料行的任何資料行值。</span><span class="sxs-lookup"><span data-stu-id="c84be-199">Any column values for subsequent key columns.</span></span></p></li>
</ul>
<p><span data-ttu-id="c84be-200">建立萬用字元搜尋索引鍵以用來尋找最接近索引結尾的索引項目時，應使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-200">This option should be used when building wildcard search keys to use for finding index entries closest to the end of an index.</span></span> <span data-ttu-id="c84be-201">索引的結尾是移至該索引中的最後一筆記錄時，所找到的索引項目。</span><span class="sxs-lookup"><span data-stu-id="c84be-201">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="c84be-202">索引的結尾與索引的高端不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</span><span class="sxs-lookup"><span data-stu-id="c84be-202">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="c84be-203">當這個選項與 JET_bitStrLimit 一起指定，且目前的索引鍵資料行是文字資料行時，就會優先使用此選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-203">When this option is specified in combination with JET_bitStrLimit and the current key column is a text column, this option will take precedence.</span></span> <span data-ttu-id="c84be-204">當目前的索引鍵資料行不是文字資料行時，就會忽略這個選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-204">This option is ignored when the current key column is not a text column.</span></span> <span data-ttu-id="c84be-205">此行為是為了允許在建立搜尋索引鍵時，推斷目前索引鍵資料行的類型。</span><span class="sxs-lookup"><span data-stu-id="c84be-205">This behavior is intended to allow the type of the current key column to be inferred when building the search key.</span></span></p>
<p><span data-ttu-id="c84be-206">如果您想要針對索引的開頭建立類似的搜尋索引鍵，則應該針對要做為前置詞萬用字元的索引鍵資料行進行類似的 <strong>JetMakeKey</strong> 呼叫，但未指定萬用字元選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-206">If you want to build a similar search key for the start of an index, a similar call to <strong>JetMakeKey</strong> should be made for the key column that is to be the prefix wildcard, but with that no wildcard options specified.</span></span> <span data-ttu-id="c84be-207">搜尋金鑰接著會處於適當的狀態，以用於這類搜尋。</span><span class="sxs-lookup"><span data-stu-id="c84be-207">The search key is then in an appropriate state to use for such a search.</span></span> <span data-ttu-id="c84be-208">這類似于使用 JET_bitPartialColumnStartLimit，不同之處在于搜尋索引鍵未完全完成，因為它是在使用萬用字元選項之後。</span><span class="sxs-lookup"><span data-stu-id="c84be-208">This is analogous to using JET_bitPartialColumnStartLimit, except that the search key is not cleanly finished as it is after the use of a wildcard option.</span></span></p>
<p><span data-ttu-id="c84be-209">此選項已在 Windows XP 和更新版本中被取代，以解決這項棘手的語義。</span><span class="sxs-lookup"><span data-stu-id="c84be-209">This option has been deprecated for Windows XP and later releases in order to address this awkward semantic.</span></span> <span data-ttu-id="c84be-210">如果可能的話，應該改用 JET_bitPartialColumnStartLimit 和 JET_bitPartialColumnEndLimit。</span><span class="sxs-lookup"><span data-stu-id="c84be-210">JET_bitPartialColumnStartLimit and JET_bitPartialColumnEndLimit should be used instead, when possible.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c84be-211">傳回值</span><span class="sxs-lookup"><span data-stu-id="c84be-211">Return Value</span></span>

<span data-ttu-id="c84be-212">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="c84be-212">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c84be-213">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="c84be-213">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c84be-214">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c84be-214">Return code</span></span></p></th>
<th><p><span data-ttu-id="c84be-215">Description</span><span class="sxs-lookup"><span data-stu-id="c84be-215">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c84be-216">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c84be-216">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c84be-217">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="c84be-217">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-218">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c84be-218">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c84be-219">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="c84be-219">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84be-220">JET_errIndexTuplesKeyTooSmall</span><span class="sxs-lookup"><span data-stu-id="c84be-220">JET_errIndexTuplesKeyTooSmall</span></span></p></td>
<td><p><span data-ttu-id="c84be-221">提供的資料行資料太小，無法為目前的索引建立有效的索引鍵，因為該索引是元組索引，且最小的元組大小大於所提供的資料行資料。</span><span class="sxs-lookup"><span data-stu-id="c84be-221">The provided column data was too small to build a valid key for the current index because that index is a tuple index and the minimum tuple size was larger than the provided column data.</span></span> <span data-ttu-id="c84be-222">如需元組索引的詳細資訊，請參閱 <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> 。</span><span class="sxs-lookup"><span data-stu-id="c84be-222">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more information on tuple indexes.</span></span> <span data-ttu-id="c84be-223">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c84be-223">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-224">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c84be-224">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c84be-225">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="c84be-225">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c84be-226">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c84be-226">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84be-227">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="c84be-227">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="c84be-228">提供的資料行資料不符合資料行定義所需的大小。</span><span class="sxs-lookup"><span data-stu-id="c84be-228">The column data provided did not match the size required by the column definition.</span></span> <span data-ttu-id="c84be-229">如果資料行的資料類型本質上是特定大小，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="c84be-229">This can happen if the column's data type is intrinsically a certain size.</span></span> <span data-ttu-id="c84be-230">如果資料行的資料類型本質上不是特定大小，但是資料行的定義宣告為固定長度，也會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="c84be-230">This can also happen if the column's data type is not intrinsically a certain size but the column's definition declares it to be of fixed length.</span></span> <span data-ttu-id="c84be-231">其中一個例外狀況是，如果為固定長度的文字資料行提供太少資料，將不會發生此錯誤，因為任何遺漏的資料都會自動填補空格。</span><span class="sxs-lookup"><span data-stu-id="c84be-231">One exception to this is that this error will not occur when too little data is provided for a fixed length text column because any missing data will be automatically padded with spaces.</span></span> <span data-ttu-id="c84be-232">第二個例外狀況是，如果為固定長度的二進位資料行提供太少資料，將不會發生此錯誤，因為遺漏的資料將會自動填補零。</span><span class="sxs-lookup"><span data-stu-id="c84be-232">A second exception to this is that this error will not occur when too little data is provided for a fixed length binary column because any missing data will be automatically padded with zeroes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-233">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="c84be-233">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="c84be-234">其中一個要求的選項無效、以不合法的方式使用，或未執行。</span><span class="sxs-lookup"><span data-stu-id="c84be-234">One of the options requested was invalid, used in an illegal manner, or not implemented.</span></span> <span data-ttu-id="c84be-235">在下列情況下， <strong>JetMakeKey</strong> 可能會發生：</span><span class="sxs-lookup"><span data-stu-id="c84be-235">This can happen for <strong>JetMakeKey</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="c84be-236">指定 JET_bitPartialColumnStartLimit 或 JET_bitPartialColumnEndLimit，而且對應的索引鍵資料行不是文字資料行，而且不是可變長度的二進位資料行。</span><span class="sxs-lookup"><span data-stu-id="c84be-236">JET_bitPartialColumnStartLimit or JET_bitPartialColumnEndLimit are specified and the corresponding key column is not a text column and is not a variable length binary column.</span></span> <span data-ttu-id="c84be-237">這種情況只會發生在 Windows XP 和更新版本上。</span><span class="sxs-lookup"><span data-stu-id="c84be-237">This case only occurs on Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="c84be-238">嘗試同時使用下列一個以上的選項： JET_bitPartialColumnStartLimit、JET_bitPartialColumnEndLimit、JET_bitFullColumnStartLimit 和 JET_bitFullColumnEndLimit。</span><span class="sxs-lookup"><span data-stu-id="c84be-238">An attempt is made to use more than one of the following options together: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit, and JET_bitFullColumnEndLimit.</span></span> <span data-ttu-id="c84be-239">這種情況只會發生在 Windows XP 和更新版本上。</span><span class="sxs-lookup"><span data-stu-id="c84be-239">This case only occurs on Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="c84be-240">使用下列其中一個選項時，會嘗試使用 JET_bitStrLimit 或 JET_bitSubStrLimit： JET_bitPartialColumnStartLimit、JET_bitPartialColumnEndLimit、JET_bitFullColumnStartLimit 和 JET_bitFullColumnEndLimit。</span><span class="sxs-lookup"><span data-stu-id="c84be-240">An attempt is made to use JET_bitStrLimit or JET_bitSubStrLimit when one of the following options is used: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit and JET_bitFullColumnEndLimit.</span></span> <span data-ttu-id="c84be-241">這種情況只會發生在 Windows XP 和更新版本上。</span><span class="sxs-lookup"><span data-stu-id="c84be-241">This case only occurs on Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84be-242">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c84be-242">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c84be-243">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="c84be-243">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p>
<p><span data-ttu-id="c84be-244">當指定 JET_bitNormalizedKey，且輸入緩衝區中提供的值太大而無法成為有效的搜尋索引鍵時， <strong>JetMakeKey</strong> 就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="c84be-244">This can happen for <strong>JetMakeKey</strong> when JET_bitNormalizedKey was specified and the value provided in the input buffer was too large to be a valid search key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-245">JET_errKeyIsMade</span><span class="sxs-lookup"><span data-stu-id="c84be-245">JET_errKeyIsMade</span></span></p></td>
<td><p><span data-ttu-id="c84be-246">提供給 <strong>JetMakeKey</strong> 的資料行資料遭到拒絕，因為目前索引中的所有索引鍵資料行都已提供資料行資料。</span><span class="sxs-lookup"><span data-stu-id="c84be-246">The column data provided to <strong>JetMakeKey</strong> was rejected because column data has already been provided for all the key columns in the current index.</span></span> <span data-ttu-id="c84be-247">這可能會以三種方式發生。</span><span class="sxs-lookup"><span data-stu-id="c84be-247">This can happen in three ways.</span></span> <span data-ttu-id="c84be-248">第一種方式是針對目前索引中的每個索引鍵資料行提供資料行資料。</span><span class="sxs-lookup"><span data-stu-id="c84be-248">The first way is if column data is provided for each key column in the current index.</span></span> <span data-ttu-id="c84be-249">第二種方式是，是否已為至少一個索引鍵資料行提供資料行資料，且已為最後一次呼叫選擇萬用字元選項。</span><span class="sxs-lookup"><span data-stu-id="c84be-249">The second way is if column data has been provided for at least one key column and a wildcard option was chosen for the last call.</span></span> <span data-ttu-id="c84be-250">第三種方式是使用 JET_bitNormalizedKey （涵蓋所有索引鍵資料行）來提供先前所建立的搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c84be-250">The third way is if a previously constructed search key was provided using JET_bitNormalizedKey, which covers all key columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84be-251">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="c84be-251">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="c84be-252">沒有目前的資料指標搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c84be-252">There is no current search key for the cursor.</span></span> <span data-ttu-id="c84be-253">如果未指定 JET_bitNewKey，且尚未使用<strong>JetMakeKey</strong>的先前呼叫來為此資料指標建立搜尋索引鍵<strong>，則會</strong>發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="c84be-253">This will happen for <strong>JetMakeKey</strong> if JET_bitNewKey is not specified and a search key has not been constructed for this cursor using a prior call to <strong>JetMakeKey</strong>.</span></span> <span data-ttu-id="c84be-254">搜尋索引鍵將會由先前呼叫 <a href="gg294117(v=exchg.10).md">JetMove</a>以外的資料指標上的任何導覽 API 來刪除。</span><span class="sxs-lookup"><span data-stu-id="c84be-254">The search key will be deleted by a prior call to any navigational API on the cursor other than <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-255">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="c84be-255">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="c84be-256">沒有目前的資料指標索引。</span><span class="sxs-lookup"><span data-stu-id="c84be-256">There is no current index for the cursor.</span></span> <span data-ttu-id="c84be-257">如果資料指標位於資料表的叢集索引、未定義主要索引，且未指定 JET_bitNormalizedKey，就會發生這種<strong>情況。</strong></span><span class="sxs-lookup"><span data-stu-id="c84be-257">This will happen for <strong>JetMakeKey</strong> if the cursor is on the clustered index of a table, a primary index has not been defined, and JET_bitNormalizedKey was not specified.</span></span> <span data-ttu-id="c84be-258">如果資料指標位於沒有任何索引鍵資料行的索引上，除非提供了先前建立的搜尋索引鍵，否則無法建立搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c84be-258">It is not possible to construct a search key if the cursor is on an index that does not have any key columns unless a previously constructed search key is provided.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84be-259">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c84be-259">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c84be-260">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="c84be-260">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-261">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c84be-261">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c84be-262">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="c84be-262">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84be-263">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c84be-263">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c84be-264">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="c84be-264">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="c84be-265">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="c84be-265">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-266">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c84be-266">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c84be-267">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="c84be-267">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c84be-268">成功時，如果未指定 JET_bitNormalizedKey 和 JET_bitNewKey，則會在目前索引中，針對一個以上的索引鍵資料行，以搜尋準則建立搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c84be-268">On success, if JET_bitNormalizedKey and JET_bitNewKey were not specified, the search key will have been built up by the search criteria for one more key column in the current index.</span></span> <span data-ttu-id="c84be-269">如果未指定 JET_bitNormalizedKey，且指定了 JET_bitNewKey，則會捨棄任何先前現有的搜尋索引鍵，並且會由目前索引中第一個索引鍵資料行的搜尋準則來建立新的搜尋金鑰。</span><span class="sxs-lookup"><span data-stu-id="c84be-269">If JET_bitNormalizedKey was not specified and JET_bitNewKey was specified, any previously existing search key was discarded and a new one will have been built up by the search criteria for the first key column in the current index.</span></span> <span data-ttu-id="c84be-270">如果指定 JET_bitNormalizedKey，則會捨棄任何先前現有的搜尋金鑰，並從輸入緩衝區載入新的搜尋金鑰。</span><span class="sxs-lookup"><span data-stu-id="c84be-270">If JET_bitNormalizedKey was specified, any previously existing search key was discarded and a new one loaded from the input buffer.</span></span> <span data-ttu-id="c84be-271">在任何情況下，都不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="c84be-271">In any case, no change to the database state will occur.</span></span>

<span data-ttu-id="c84be-272">失敗時，如果指定了 JET_bitNormalizedKey 或 JET_bitNewKey，則不會定義搜尋索引鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="c84be-272">On failure, if JET_bitNormalizedKey or JET_bitNewKey was specified, the state of the search key is undefined.</span></span> <span data-ttu-id="c84be-273">如果未指定 JET_bitNormalizedKey 或 JET_bitNewKey，將不會對搜尋索引鍵的狀態進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="c84be-273">If neither JET_bitNormalizedKey nor JET_bitNewKey were specified, no change to the state of the search key will occur.</span></span> <span data-ttu-id="c84be-274">在任何情況下，都不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="c84be-274">In any case, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c84be-275">備註</span><span class="sxs-lookup"><span data-stu-id="c84be-275">Remarks</span></span>

<span data-ttu-id="c84be-276">金鑰應該視為不透明的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="c84be-276">Keys should be treated as opaque chunks of data.</span></span> <span data-ttu-id="c84be-277">不應嘗試利用此資料的內部結構。</span><span class="sxs-lookup"><span data-stu-id="c84be-277">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="c84be-278">但是，下列已知所有 ESENT 金鑰：</span><span class="sxs-lookup"><span data-stu-id="c84be-278">However, the following is known about all ESENT keys:</span></span>

  - <span data-ttu-id="c84be-279">您可以使用 [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) 來相互比較索引鍵，以在來源索引項目目的資料表中建立原始索引的相對順序。</span><span class="sxs-lookup"><span data-stu-id="c84be-279">Keys may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="c84be-280">將索引項目的索引鍵與不同索引的索引鍵進行比較是無意義的。</span><span class="sxs-lookup"><span data-stu-id="c84be-280">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="c84be-281">在 Windows Vista 之前，索引鍵一律小於或等於 JET_cbKeyMost (255) 位元組。</span><span class="sxs-lookup"><span data-stu-id="c84be-281">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="c84be-282">在 Windows Vista 和更新版本中，金鑰可以更大。</span><span class="sxs-lookup"><span data-stu-id="c84be-282">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="c84be-283">索引鍵的大小上限等於 JET_paramKeyMost 目前的值。</span><span class="sxs-lookup"><span data-stu-id="c84be-283">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

<span data-ttu-id="c84be-284">如果使用萬用字元選項，搜尋索引鍵的時間可能會較長一位元組。</span><span class="sxs-lookup"><span data-stu-id="c84be-284">Search keys can be one byte longer if a wildcard option was used.</span></span> <span data-ttu-id="c84be-285">在這種情況下，在 Windows Vista 之前的版本中，搜尋金鑰將會 JET_cbLimitKeyMost (256) 個位元組，而 Windows Vista 和更新版本的 JET_paramKeyMost + 1 個位元組。</span><span class="sxs-lookup"><span data-stu-id="c84be-285">In that case, the search key will be up to JET_cbLimitKeyMost (256) bytes for releases prior to Windows Vista and JET_paramKeyMost + 1 bytes for Windows Vista and later releases.</span></span>

<span data-ttu-id="c84be-286">此最大金鑰大小的 ramification 很重要。</span><span class="sxs-lookup"><span data-stu-id="c84be-286">There is a very important ramification to this maximum key size.</span></span> <span data-ttu-id="c84be-287">只要索引項目的資料行值大到足以為該索引產生索引鍵，而該索引大於此大小上限時，就會以無訊息方式截斷該索引鍵的大小上限。</span><span class="sxs-lookup"><span data-stu-id="c84be-287">Whenever there is an index entry that has column values that are large enough to cause a key to be generated for that index that would otherwise be larger than this maximum size, that key is silently truncated at that maximum size.</span></span> <span data-ttu-id="c84be-288">這會導致兩個效果：</span><span class="sxs-lookup"><span data-stu-id="c84be-288">This causes two effects:</span></span>

  - <span data-ttu-id="c84be-289">如果是唯一索引中的專案，則會導致其他唯一的專案宣告為重複專案。</span><span class="sxs-lookup"><span data-stu-id="c84be-289">For entries in a unique index, it will cause entries that would otherwise be unique to be declared as duplicates.</span></span>

  - <span data-ttu-id="c84be-290">對於所有索引中的專案，索引鍵截斷會導致索引項目不符合指定搜尋索引鍵的搜尋準則，以宣告為相符專案。</span><span class="sxs-lookup"><span data-stu-id="c84be-290">For entries in all indexes, key truncation will cause index entries that would otherwise not match the search criteria of a given search key to be declared as matches.</span></span>

<span data-ttu-id="c84be-291">應用程式必須預期此截斷，並避免它或補償其效果。</span><span class="sxs-lookup"><span data-stu-id="c84be-291">Applications must anticipate this truncation and either avoid it or compensate for its effects.</span></span> <span data-ttu-id="c84be-292">在 Windows Vista 中，已加入新的索引旗標 JET_bitIndexDisallowTruncation，讓應用程式更容易防止金鑰截斷。</span><span class="sxs-lookup"><span data-stu-id="c84be-292">In Windows Vista, a new index flag, JET_bitIndexDisallowTruncation, has been added to make it easier for applications to prevent key truncations.</span></span> <span data-ttu-id="c84be-293">如需此索引編制選項的詳細資訊，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="c84be-293">See the [JET_INDEXCREATE](./jet-indexcreate-structure.md) structure for more information on this indexing option.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c84be-294">規格需求</span><span class="sxs-lookup"><span data-stu-id="c84be-294">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c84be-295"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="c84be-295"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c84be-296">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="c84be-296">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-297"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="c84be-297"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c84be-298">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="c84be-298">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84be-299"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="c84be-299"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c84be-300">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="c84be-300">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84be-301"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="c84be-301"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c84be-302">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="c84be-302">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84be-303"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c84be-303"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c84be-304">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="c84be-304">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c84be-305">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c84be-305">See Also</span></span>

[<span data-ttu-id="c84be-306">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c84be-306">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c84be-307">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c84be-307">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c84be-308">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c84be-308">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c84be-309">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c84be-309">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c84be-310">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="c84be-310">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="c84be-311">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="c84be-311">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="c84be-312">JetSeek</span><span class="sxs-lookup"><span data-stu-id="c84be-312">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="c84be-313">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="c84be-313">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
