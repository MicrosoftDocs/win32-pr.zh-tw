---
description: 深入瞭解： JetSeek 函數
title: JetSeek 函式
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c386ae3af5353b95d9d1d3c67df4d680c52bff68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988420"
---
# <a name="jetseek-function"></a><span data-ttu-id="26de0-103">JetSeek 函式</span><span class="sxs-lookup"><span data-stu-id="26de0-103">JetSeek Function</span></span>


<span data-ttu-id="26de0-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="26de0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetseek-function"></a><span data-ttu-id="26de0-105">JetSeek 函式</span><span class="sxs-lookup"><span data-stu-id="26de0-105">JetSeek Function</span></span>

<span data-ttu-id="26de0-106">**JetSeek** 函式會有效率地將資料指標放在索引項目目，以符合該資料指標中的搜尋索引鍵所指定的搜尋條件，以及指定的不相等。</span><span class="sxs-lookup"><span data-stu-id="26de0-106">The **JetSeek** function efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="26de0-107">搜尋金鑰必須先前已使用 [JetMakeKey](./jetmakekey-function.md)來建立。</span><span class="sxs-lookup"><span data-stu-id="26de0-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="26de0-108">參數</span><span class="sxs-lookup"><span data-stu-id="26de0-108">Parameters</span></span>

<span data-ttu-id="26de0-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="26de0-109">*sesid*</span></span>

<span data-ttu-id="26de0-110">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="26de0-110">The session to use for this call.</span></span>

<span data-ttu-id="26de0-111">*tableid*</span><span class="sxs-lookup"><span data-stu-id="26de0-111">*tableid*</span></span>

<span data-ttu-id="26de0-112">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="26de0-112">The cursor to use for this call.</span></span>

<span data-ttu-id="26de0-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="26de0-113">*grbit*</span></span>

<span data-ttu-id="26de0-114">位群組，其中包含要用於此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="26de0-114">A group of bits that contain the options to be used for this call.</span></span> <span data-ttu-id="26de0-115">*Grbit* 必須為非零值，而且必須包含下表所列的一或多個值。</span><span class="sxs-lookup"><span data-stu-id="26de0-115">*Grbit* must be nonzero and must include one or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26de0-116">值</span><span class="sxs-lookup"><span data-stu-id="26de0-116">Value</span></span></p></th>
<th><p><span data-ttu-id="26de0-117">意義</span><span class="sxs-lookup"><span data-stu-id="26de0-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26de0-118">JET_bitCheckUniqueness</span><span class="sxs-lookup"><span data-stu-id="26de0-118">JET_bitCheckUniqueness</span></span></p></td>
<td><p><span data-ttu-id="26de0-119">如果低廉價格判斷出只有一個符合搜尋索引鍵的索引項目，就會傳回特殊的錯誤碼（JET_wrnUniqueKey）。</span><span class="sxs-lookup"><span data-stu-id="26de0-119">A special error code, JET_wrnUniqueKey, will be returned if it can be cheaply determined that there is exactly one index entry that matches the search key.</span></span></p>
<p><span data-ttu-id="26de0-120">除非也指定了 JET_bitSeekEQ，否則會忽略這個選項。</span><span class="sxs-lookup"><span data-stu-id="26de0-120">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p>
<p><span data-ttu-id="26de0-121">此選項僅適用于 Windows Server 2003 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="26de0-121">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26de0-122">JET_bitSeekEQ</span><span class="sxs-lookup"><span data-stu-id="26de0-122">JET_bitSeekEQ</span></span></p></td>
<td><p><span data-ttu-id="26de0-123">資料指標將定位於最接近索引開頭的索引項目目，此索引項目目完全符合搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="26de0-123">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span> <span data-ttu-id="26de0-124">索引的開頭是移至該索引中的第一筆記錄時，所找到的索引項目。</span><span class="sxs-lookup"><span data-stu-id="26de0-124">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="26de0-125">索引的開頭與索引的下限不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</span><span class="sxs-lookup"><span data-stu-id="26de0-125">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="26de0-126">將此選項與使用 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵搭配使用萬用字元選項沒有意義。</span><span class="sxs-lookup"><span data-stu-id="26de0-126">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26de0-127">JET_bitSeekGE</span><span class="sxs-lookup"><span data-stu-id="26de0-127">JET_bitSeekGE</span></span></p></td>
<td><p><span data-ttu-id="26de0-128">資料指標將定位於最接近索引開頭的索引項目目，此索引項目目大於或等於符合搜尋條件的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="26de0-128">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="26de0-129">索引的開頭是移至該索引中的第一筆記錄時，所找到的索引項目。</span><span class="sxs-lookup"><span data-stu-id="26de0-129">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="26de0-130">索引的開頭與索引的下限不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</span><span class="sxs-lookup"><span data-stu-id="26de0-130">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="26de0-131">將此選項與使用 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵搭配使用，並使用萬用字元選項來尋找最接近索引結尾的索引項目，並沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="26de0-131">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26de0-132">JET_bitSeekGT</span><span class="sxs-lookup"><span data-stu-id="26de0-132">JET_bitSeekGT</span></span></p></td>
<td><p><span data-ttu-id="26de0-133">資料指標將放置在索引項目目的開頭最接近索引的開頭，而該索引項目大於符合搜尋準則的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="26de0-133">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="26de0-134">索引的開頭是移至該索引中的第一筆記錄時，所找到的索引項目。</span><span class="sxs-lookup"><span data-stu-id="26de0-134">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="26de0-135">索引的開頭與索引的下限不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</span><span class="sxs-lookup"><span data-stu-id="26de0-135">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="26de0-136">搭配使用 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵，並不適合用來尋找最接近索引開頭的索引項目的萬用字元選項，這是使用此選項的意義。</span><span class="sxs-lookup"><span data-stu-id="26de0-136">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26de0-137">JET_bitSeekLE</span><span class="sxs-lookup"><span data-stu-id="26de0-137">JET_bitSeekLE</span></span></p></td>
<td><p><span data-ttu-id="26de0-138">資料指標將定位於最接近索引結尾的索引項目目，這個專案小於或等於符合搜尋準則的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="26de0-138">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="26de0-139">索引的結尾是移至該索引中的最後一筆記錄時，所找到的索引項目。</span><span class="sxs-lookup"><span data-stu-id="26de0-139">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="26de0-140">索引的結尾與索引的高端不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</span><span class="sxs-lookup"><span data-stu-id="26de0-140">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="26de0-141">搭配使用 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵，並不適合用來尋找最接近索引開頭的索引項目的萬用字元選項，這是使用此選項的意義。</span><span class="sxs-lookup"><span data-stu-id="26de0-141">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26de0-142">JET_bitSeekLT</span><span class="sxs-lookup"><span data-stu-id="26de0-142">JET_bitSeekLT</span></span></p></td>
<td><p><span data-ttu-id="26de0-143">資料指標將放置在最接近索引結尾的索引項目目，此索引項目目小於符合搜尋條件的索引項目。</span><span class="sxs-lookup"><span data-stu-id="26de0-143">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="26de0-144">索引的結尾是移至該索引中的最後一筆記錄時，所找到的索引項目。</span><span class="sxs-lookup"><span data-stu-id="26de0-144">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="26de0-145">索引的結尾與索引的高端不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</span><span class="sxs-lookup"><span data-stu-id="26de0-145">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="26de0-146">將此選項與使用 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵搭配使用，並使用萬用字元選項來尋找最接近索引結尾的索引項目，並沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="26de0-146">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26de0-147">JET_bitSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="26de0-147">JET_bitSetIndexRange</span></span></p></td>
<td><p><span data-ttu-id="26de0-148">將會針對完全符合搜尋索引鍵的所有索引鍵，自動設定索引範圍。</span><span class="sxs-lookup"><span data-stu-id="26de0-148">An index range will automatically be setup for all keys that exactly match the search key.</span></span> <span data-ttu-id="26de0-149">產生的索引範圍等同于使用 JET_bitRangeInclusive 和 JET_bitRangeUpperLimit 選項呼叫 <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> 所建立的索引範圍。</span><span class="sxs-lookup"><span data-stu-id="26de0-149">The resulting index range is identical to one that would have otherwise been created by a call to <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> with the JET_bitRangeInclusive and JET_bitRangeUpperLimit options.</span></span> <span data-ttu-id="26de0-150">如需詳細資訊，請參閱 <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> 。</span><span class="sxs-lookup"><span data-stu-id="26de0-150">See <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> for more information.</span></span></p>
<p><span data-ttu-id="26de0-151">這是一種方便的方法，可讓您探索符合相同搜尋條件的所有索引項目。</span><span class="sxs-lookup"><span data-stu-id="26de0-151">This is a convenient method for discovering all the index entries that match the same search criteria.</span></span></p>
<p><span data-ttu-id="26de0-152">除非也指定了 JET_bitSeekEQ，否則會忽略這個選項。</span><span class="sxs-lookup"><span data-stu-id="26de0-152">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="26de0-153">傳回值</span><span class="sxs-lookup"><span data-stu-id="26de0-153">Return Value</span></span>

<span data-ttu-id="26de0-154">此函數可讓您傳回此 API 中所定義的任何 [JET_ERRs](./jet-err.md) 。</span><span class="sxs-lookup"><span data-stu-id="26de0-154">This function allows for the return of any [JET_ERRs](./jet-err.md) that are defined in this API.</span></span> <span data-ttu-id="26de0-155">如需有關 Jet 錯誤的詳細資訊，請參閱 [可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="26de0-155">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26de0-156">傳回碼</span><span class="sxs-lookup"><span data-stu-id="26de0-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="26de0-157">Description</span><span class="sxs-lookup"><span data-stu-id="26de0-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26de0-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="26de0-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="26de0-159">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="26de0-159">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="26de0-160">針對 <strong>JetSeek</strong>，這表示找到完全符合搜尋準則的索引項目。</span><span class="sxs-lookup"><span data-stu-id="26de0-160">For <strong>JetSeek</strong>, this means that an index entry was found that exactly matched the search criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26de0-161">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="26de0-161">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="26de0-162">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="26de0-162">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26de0-163">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="26de0-163">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="26de0-164">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="26de0-164">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="26de0-165">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="26de0-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26de0-166">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="26de0-166">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="26de0-167">沒有目前的資料指標搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="26de0-167">There is no current search key for the cursor.</span></span> <span data-ttu-id="26de0-168"><strong>JetSeek</strong> 要求資料指標必須有有效的搜尋索引鍵，因為它會針對用來尋找索引項目的搜尋條件使用該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="26de0-168"><strong>JetSeek</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26de0-169">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="26de0-169">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="26de0-170">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="26de0-170">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26de0-171">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="26de0-171">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="26de0-172">找不到符合搜尋準則的索引項目。</span><span class="sxs-lookup"><span data-stu-id="26de0-172">No index entry was found that matched the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26de0-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="26de0-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="26de0-174">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="26de0-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26de0-175">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="26de0-175">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="26de0-176">找到符合搜尋準則的索引項目。</span><span class="sxs-lookup"><span data-stu-id="26de0-176">An index entry was found that matched the search criteria.</span></span> <span data-ttu-id="26de0-177">但是，該索引項目不完全相符。</span><span class="sxs-lookup"><span data-stu-id="26de0-177">However, that index entry was not an exact match.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26de0-178">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="26de0-178">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="26de0-179">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="26de0-179">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="26de0-180">只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="26de0-180">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26de0-181">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="26de0-181">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="26de0-182">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="26de0-182">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26de0-183">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="26de0-183">JET_wrnUniqueKey</span></span></p></td>
<td><p><span data-ttu-id="26de0-184">找不到完全符合搜尋準則的一個索引項目。</span><span class="sxs-lookup"><span data-stu-id="26de0-184">Exactly one index entry was found that exactly matched the search criteria.</span></span> <span data-ttu-id="26de0-185">只有在指定 JET_bitSeekCheckUniqueness 時，才會傳回此錯誤，而且很便宜地判斷相符的索引項目目是完全符合搜尋準則的唯一索引專案。</span><span class="sxs-lookup"><span data-stu-id="26de0-185">This error will only be returned if JET_bitSeekCheckUniqueness was specified and it was cheap to determine that the matching index entry was the only index entry that exactly matches the search criteria.</span></span></p>
<p><span data-ttu-id="26de0-186">只有 Windows Server 2003 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="26de0-186">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="26de0-187">成功時，游標將定位於符合搜尋準則的索引項目。</span><span class="sxs-lookup"><span data-stu-id="26de0-187">On success, the cursor will be positioned at an index entry that matches the search criteria.</span></span> <span data-ttu-id="26de0-188">如果已準備好要進行更新的記錄，則會取消該更新。</span><span class="sxs-lookup"><span data-stu-id="26de0-188">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="26de0-189">如果索引範圍有效，就會取消該索引範圍。</span><span class="sxs-lookup"><span data-stu-id="26de0-189">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="26de0-190">如果已針對資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="26de0-190">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="26de0-191">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="26de0-191">No change to the database state will occur.</span></span> <span data-ttu-id="26de0-192">當多個索引項目具有相同的值時，一律會選取最接近索引開頭的專案。</span><span class="sxs-lookup"><span data-stu-id="26de0-192">When multiple index entries have the same value, the entry closest to the start of the index is always selected.</span></span>

<span data-ttu-id="26de0-193">失敗時，除非傳回 JET_errRecordNotFound，否則資料指標的位置會保持不變。</span><span class="sxs-lookup"><span data-stu-id="26de0-193">On failure, the position of the cursor will remain unchanged unless JET_errRecordNotFound was returned.</span></span> <span data-ttu-id="26de0-194">在這種情況下，游標將放置於符合該資料指標中搜尋索引鍵所指定之搜尋準則的索引項目目，以及指定的不相等。</span><span class="sxs-lookup"><span data-stu-id="26de0-194">In that case, the cursor will be positioned where the index entry that matched the search criteria specified by the search key in that cursor and the specified inequality would have been.</span></span> <span data-ttu-id="26de0-195">資料指標可以相對於該位置移動，但仍不在有效的索引項目上。</span><span class="sxs-lookup"><span data-stu-id="26de0-195">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="26de0-196">如果已準備好要進行更新的記錄，則會取消該更新。</span><span class="sxs-lookup"><span data-stu-id="26de0-196">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="26de0-197">如果索引範圍有效，就會取消該索引範圍。</span><span class="sxs-lookup"><span data-stu-id="26de0-197">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="26de0-198">如果已針對資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。</span><span class="sxs-lookup"><span data-stu-id="26de0-198">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="26de0-199">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="26de0-199">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="26de0-200">規格需求</span><span class="sxs-lookup"><span data-stu-id="26de0-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26de0-201"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="26de0-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="26de0-202">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="26de0-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26de0-203"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="26de0-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="26de0-204">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="26de0-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26de0-205"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="26de0-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="26de0-206">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="26de0-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26de0-207"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="26de0-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="26de0-208">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="26de0-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26de0-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="26de0-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="26de0-210">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="26de0-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="26de0-211">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26de0-211">See Also</span></span>

[<span data-ttu-id="26de0-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="26de0-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="26de0-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="26de0-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="26de0-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="26de0-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="26de0-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="26de0-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="26de0-216">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="26de0-216">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="26de0-217">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="26de0-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="26de0-218">JetStopService</span><span class="sxs-lookup"><span data-stu-id="26de0-218">JetStopService</span></span>](./jetstopservice-function.md)
