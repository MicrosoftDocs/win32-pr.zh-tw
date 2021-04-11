---
description: 深入瞭解： JetEnumerateColumns 函數
title: JetEnumerateColumns 函式
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b913fb970232ca6f0fc21eb846df85e1db684f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193797"
---
# <a name="jetenumeratecolumns-function"></a><span data-ttu-id="d12de-103">JetEnumerateColumns 函式</span><span class="sxs-lookup"><span data-stu-id="d12de-103">JetEnumerateColumns Function</span></span>


<span data-ttu-id="d12de-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d12de-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenumeratecolumns-function"></a><span data-ttu-id="d12de-105">JetEnumerateColumns 函式</span><span class="sxs-lookup"><span data-stu-id="d12de-105">JetEnumerateColumns Function</span></span>

<span data-ttu-id="d12de-106">**JetEnumerateColumns** 函式會從資料指標的目前記錄或該資料指標的複製緩衝區，有效率地取出一組資料行和其值。</span><span class="sxs-lookup"><span data-stu-id="d12de-106">The **JetEnumerateColumns** function efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="d12de-107">您可以使用資料行識別碼、 *itagSequence* 數位和其他特性的清單來限制抓取的資料行和值。</span><span class="sxs-lookup"><span data-stu-id="d12de-107">The columns and values retrieved can be restricted by a list of column IDs, *itagSequence* numbers, and other characteristics.</span></span> <span data-ttu-id="d12de-108">此資料行抓取 API 是唯一的，因為它會將資訊傳回給動態配置的記憶體，而這些記憶體是使用使用者提供的 [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) 相容回呼所取得。</span><span class="sxs-lookup"><span data-stu-id="d12de-108">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="d12de-109">這項新的彈性可讓您有效率地抓取具有特定特性 (的資料行資料，例如呼叫端未知) 大小和多重性。</span><span class="sxs-lookup"><span data-stu-id="d12de-109">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="d12de-110">如此一來，就不需要使用 [JetRetrieveColumn](./jetretrievecolumn-function.md) 的探索模式來判斷這些特性，以便設定 [JetRetrieveColumn](./jetretrievecolumn-function.md) 的最後一個呼叫，以成功取得所需的資料。</span><span class="sxs-lookup"><span data-stu-id="d12de-110">This eliminates the need for the use of the discovery modes of [JetRetrieveColumn](./jetretrievecolumn-function.md) to determine those characteristics in order to setup a final call to [JetRetrieveColumn](./jetretrievecolumn-function.md) that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="d12de-111">**Windows xp： JetEnumerateColumns** 是在 windows xp 中引進的。</span><span class="sxs-lookup"><span data-stu-id="d12de-111">**Windows XP:  JetEnumerateColumns** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d12de-112">參數</span><span class="sxs-lookup"><span data-stu-id="d12de-112">Parameters</span></span>

<span data-ttu-id="d12de-113">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d12de-113">*sesid*</span></span>

<span data-ttu-id="d12de-114">此呼叫所要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="d12de-114">The session to use for this call.</span></span>

<span data-ttu-id="d12de-115">*tableid*</span><span class="sxs-lookup"><span data-stu-id="d12de-115">*tableid*</span></span>

<span data-ttu-id="d12de-116">要用於此呼叫的資料指標。</span><span class="sxs-lookup"><span data-stu-id="d12de-116">The cursor to use for this call.</span></span>

<span data-ttu-id="d12de-117">*cEnumColumnId*</span><span class="sxs-lookup"><span data-stu-id="d12de-117">*cEnumColumnId*</span></span>

<span data-ttu-id="d12de-118">資料行識別碼的陣列，每個都有一個選擇性的 *itagSequence* 數位陣列來列舉。</span><span class="sxs-lookup"><span data-stu-id="d12de-118">An array of column IDs, each with an optional array of *itagSequence* numbers to enumerate.</span></span>

<span data-ttu-id="d12de-119">如果 *cEnumColumnId* 為 0 (零) 則會忽略 *rgEnumColumnId* 並列舉所有資料行值，並將其傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="d12de-119">If *cEnumColumnId* is 0 (zero) then *rgEnumColumnId* is ignored and all column values are enumerated and returned to the caller.</span></span> <span data-ttu-id="d12de-120">如果資料行識別碼陣列的元素參考到 0 (零的資料行識別碼) 則會略過該資料行的列舉，並且會產生輸出中的對應位置，並將資料行狀態設為 JET_wrnColumnSkipped。</span><span class="sxs-lookup"><span data-stu-id="d12de-120">If an element of the column ID array refers to a column ID of 0 (zero) then enumeration of that column is skipped and a corresponding slot in the output will be generated with a column status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="d12de-121">如果 *ctagSequence* 為 0 (零) 用於資料行識別碼陣列的指定元素，則會忽略 *rgtagSequence* ，並且會列舉該資料行識別碼的所有資料行值，並將其傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="d12de-121">If *ctagSequence* is 0 (zero) for a given element of the column ID array then *rgtagSequence* is ignored and all column values for that column ID are enumerated and returned to the caller.</span></span> <span data-ttu-id="d12de-122">如果 *itagSequence* 數位陣列的元素參考 *itagSequence* 數位 0 () 零，則會略過該 *itagSequence* 數位的列舉，並且會產生輸出中的對應位置，並將資料行值狀態設為 JET_wrnColumnSkipped。</span><span class="sxs-lookup"><span data-stu-id="d12de-122">If an element of an *itagSequence* number array refers to a *itagSequence* number of 0 (zero) then the enumeration of that *itagSequence* number is skipped and a corresponding slot in the output will be generated with a column value status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="d12de-123">*rgEnumColumnId*</span><span class="sxs-lookup"><span data-stu-id="d12de-123">*rgEnumColumnId*</span></span>

<span data-ttu-id="d12de-124">請參閱 *cEnumColumnId*。</span><span class="sxs-lookup"><span data-stu-id="d12de-124">See *cEnumColumnId*.</span></span>

<span data-ttu-id="d12de-125">*pcEnumColumn*</span><span class="sxs-lookup"><span data-stu-id="d12de-125">*pcEnumColumn*</span></span>

<span data-ttu-id="d12de-126">在透過提供的 *itagSequence* 相容回呼所配置的記憶體中，傳回資料行的列舉陣列和其值。</span><span class="sxs-lookup"><span data-stu-id="d12de-126">Returns the enumerated array of columns and their values in memory allocated through the provided *itagSequence* compatible callback.</span></span>

<span data-ttu-id="d12de-127">如果在輸入上要求資料行識別碼的陣列，則輸出陣列的順序和大小會反映輸入陣列的順序和大小。</span><span class="sxs-lookup"><span data-stu-id="d12de-127">If an array of column IDs is requested on input then the order and size of the output array will reflect the order and size of the input array.</span></span> <span data-ttu-id="d12de-128">同樣地，如果在輸入時要求特定資料行識別碼的 *itagSequence* 數位陣列，則該資料行之資料行值的輸出陣列順序和大小將會反映輸入陣列的順序和大小。</span><span class="sxs-lookup"><span data-stu-id="d12de-128">Similarly, if an array of *itagSequence* numbers is requested for a particular column ID on input then the order and size of the output array of column values for that column will reflect the order and size of the input array.</span></span>

<span data-ttu-id="d12de-129">輸出參數會設定為 0 (零) ，而且除了 JET_errBadColumnId 和 JET_errColumnNotFound 以外的任何錯誤都是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d12de-129">The output parameters are set to 0 (zero) and **NULL** on any error except for JET_errBadColumnId and JET_errColumnNotFound.</span></span> <span data-ttu-id="d12de-130">傳回這些錯誤時，除了受影響的資料行識別碼之外，輸出資料是有效且完整的。</span><span class="sxs-lookup"><span data-stu-id="d12de-130">When these errors are returned, the output data is valid and complete for all but the affected column IDs.</span></span> <span data-ttu-id="d12de-131">每個受影響資料行識別碼的狀態碼會設定為其中一個錯誤，因此呼叫者可以判斷哪些資料行識別碼不正確，並可能採取矯正措施。</span><span class="sxs-lookup"><span data-stu-id="d12de-131">The status code for each of the affected column IDs is set to one of these errors so that the caller may determine which column IDs were bad and potentially take corrective action.</span></span>

<span data-ttu-id="d12de-132">*prgEnumColumn*</span><span class="sxs-lookup"><span data-stu-id="d12de-132">*prgEnumColumn*</span></span>

<span data-ttu-id="d12de-133">請參閱 *pcEnumColumn*。</span><span class="sxs-lookup"><span data-stu-id="d12de-133">See *pcEnumColumn*.</span></span>

<span data-ttu-id="d12de-134">*pfnRealloc*</span><span class="sxs-lookup"><span data-stu-id="d12de-134">*pfnRealloc*</span></span>

<span data-ttu-id="d12de-135">識別與 [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) 相容的回呼，以及選用的內容指標，用來為數據行的輸出陣列和其值配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="d12de-135">Identifies a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback and an optional context pointer used to allocate memory for the output array of columns and their values.</span></span>

<span data-ttu-id="d12de-136">*pvReallocCoNtext*</span><span class="sxs-lookup"><span data-stu-id="d12de-136">*pvReallocContext*</span></span>

<span data-ttu-id="d12de-137">請參閱 *pfnRealloc*。</span><span class="sxs-lookup"><span data-stu-id="d12de-137">See *pfnRealloc*.</span></span>

<span data-ttu-id="d12de-138">*cbDataMost*</span><span class="sxs-lookup"><span data-stu-id="d12de-138">*cbDataMost*</span></span>

<span data-ttu-id="d12de-139">設定要從長文字或長二進位資料行傳回的資料量上限。</span><span class="sxs-lookup"><span data-stu-id="d12de-139">Sets a cap on the amount of data to return from a long text or long binary column.</span></span>

<span data-ttu-id="d12de-140">您可以使用這個參數來防止列舉非常大的資料行值。</span><span class="sxs-lookup"><span data-stu-id="d12de-140">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span> <span data-ttu-id="d12de-141">一般來說，這類列舉可能會使 API 呼叫失敗，並 JET_errOutOfMemory。</span><span class="sxs-lookup"><span data-stu-id="d12de-141">Ordinarily, such an enumeration might fail the API call with JET_errOutOfMemory.</span></span> <span data-ttu-id="d12de-142">如果以這種方式截斷大型資料行值，則資料行值的狀態將會是 JET_wrnColumnTruncated。</span><span class="sxs-lookup"><span data-stu-id="d12de-142">If a large column value is truncated in such a manner then the column value's status will be JET_wrnColumnTruncated.</span></span>

<span data-ttu-id="d12de-143">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d12de-143">*grbit*</span></span>

<span data-ttu-id="d12de-144">指定零或多個下列選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="d12de-144">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d12de-145">值</span><span class="sxs-lookup"><span data-stu-id="d12de-145">Value</span></span></p></th>
<th><p><span data-ttu-id="d12de-146">意義</span><span class="sxs-lookup"><span data-stu-id="d12de-146">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d12de-147">JET_bitEnumerateCompressOutput</span><span class="sxs-lookup"><span data-stu-id="d12de-147">JET_bitEnumerateCompressOutput</span></span></p></td>
<td><p><span data-ttu-id="d12de-148">列舉資料行值時，我們將會以壓縮格式傳回所有資料行，而這些資料行只會傳回一個非 Null 資料行值。</span><span class="sxs-lookup"><span data-stu-id="d12de-148">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="d12de-149">這類資料行的狀態將會設定為 JET_wrnColumnSingleValue，且資料行值和包含資料行值的記憶體大小將直接在 <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> 結構中傳回。</span><span class="sxs-lookup"><span data-stu-id="d12de-149">The status for such columns will be set to JET_wrnColumnSingleValue and the size of the column value and the memory containing the column value will be returned directly in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="d12de-150">不保證會以這種方式壓縮所有合格的資料行。</span><span class="sxs-lookup"><span data-stu-id="d12de-150">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="d12de-151">如需詳細資訊，請參閱 <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> 。</span><span class="sxs-lookup"><span data-stu-id="d12de-151">See <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d12de-152">JET_bitEnumerateCopy</span><span class="sxs-lookup"><span data-stu-id="d12de-152">JET_bitEnumerateCopy</span></span></p></td>
<td><p><span data-ttu-id="d12de-153">此選項表示應該列舉記錄的已修改資料行值，而不是原始資料行值。</span><span class="sxs-lookup"><span data-stu-id="d12de-153">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="d12de-154">如果資料行值尚未修改，則會列舉原始資料行值。</span><span class="sxs-lookup"><span data-stu-id="d12de-154">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="d12de-155">如此一來，插入或更新記錄時，可能會列舉尚未插入或更新的資料行值。</span><span class="sxs-lookup"><span data-stu-id="d12de-155">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span></p>
<p><span data-ttu-id="d12de-156">與 <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> 或 <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>搭配使用時，此選項等同于 JET_bitRetrieveCopy。</span><span class="sxs-lookup"><span data-stu-id="d12de-156">This option is identical to JET_bitRetrieveCopy when used with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d12de-157">JET_bitEnumerateIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="d12de-157">JET_bitEnumerateIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="d12de-158">如果指定的資料行不存在於記錄中，則不會傳回任何資料行值。</span><span class="sxs-lookup"><span data-stu-id="d12de-158">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="d12de-159">一般來說，在此案例中會傳回資料行的預設值（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d12de-159">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="d12de-160">如果資料行設定為與預設值不同的值，則會傳回不同的值 (也就是說，如果具有預設值的資料行明確設定為 <strong>null</strong> ，則會傳回 <strong>null</strong> 做為該資料行的值) 。</span><span class="sxs-lookup"><span data-stu-id="d12de-160">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to <strong>NULL</strong> then a <strong>NULL</strong> will be returned as the value for that column).</span></span> <span data-ttu-id="d12de-161">請注意，即使已要求此選項，仍然可以看到剛好等於預設值的資料行值。</span><span class="sxs-lookup"><span data-stu-id="d12de-161">Note that, even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="d12de-162">移除符合其預設值的資料行值不會進行任何工作。</span><span class="sxs-lookup"><span data-stu-id="d12de-162">No effort is made to remove column values that match their default values.</span></span></p>
<p><span data-ttu-id="d12de-163">請務必注意，當使用 JET_bitEnumeratePresenceOnly 或 JET_bitEnumerateTaggedOnly 時，此選項會影響 <strong>JetEnumerateColumns</strong> 的輸出。</span><span class="sxs-lookup"><span data-stu-id="d12de-163">It is important to note that this option affects the output of <strong>JetEnumerateColumns</strong> when used with JET_bitEnumeratePresenceOnly or JET_bitEnumerateTaggedOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d12de-164">JET_bitEnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="d12de-164">JET_bitEnumerateIgnoreUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="d12de-165">如果指定的資料行不存在於記錄中，而且它具有使用者定義的預設值，則不會傳回任何資料行值。</span><span class="sxs-lookup"><span data-stu-id="d12de-165">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="d12de-166">此選項可防止在列舉該資料行的值時，計算資料行之使用者定義預設值的回呼。</span><span class="sxs-lookup"><span data-stu-id="d12de-166">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></p>
<p><span data-ttu-id="d12de-167"><strong>Windows Server 2003 及更早版本：  </strong>若為 Windows Server 2003 及更早版本，此作業將會失敗，並 JET_errCallbackFailed。</span><span class="sxs-lookup"><span data-stu-id="d12de-167"><strong>Windows Server 2003 and earlier:  </strong>For Windows Server 2003 and earlier releases, the operation will fail with JET_errCallbackFailed.</span></span></p>
<p><span data-ttu-id="d12de-168"><strong>Windows Server 2003 SP1：  </strong>此可能值僅適用于 Windows Server 2003 SP1 和更新版本的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d12de-168"><strong>Windows Server 2003 SP1:  </strong>This possible value is only available for Windows Server 2003 SP1 and later operating systems.</span></span> <span data-ttu-id="d12de-169">如果指定了此可能的值，且資料表包含具有使用者定義之預設值的資料行，則作業會失敗並出現 JET_errCallbackFailed。</span><span class="sxs-lookup"><span data-stu-id="d12de-169">If this possible value is specified and the table contains a column that has a user defined default value, then the operation will fail with JET_errCallbackFailed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d12de-170">JET_bitEnumeratePresenceOnly</span><span class="sxs-lookup"><span data-stu-id="d12de-170">JET_bitEnumeratePresenceOnly</span></span></p></td>
<td><p><span data-ttu-id="d12de-171">如果要求的資料行或資料行值有非 Null 的值，則不會傳回相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="d12de-171">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="d12de-172">相反地，該資料行或資料行值的關聯狀態將會設定為 JET_wrnColumnPresent。</span><span class="sxs-lookup"><span data-stu-id="d12de-172">Instead, the associated status for that column or column value will be set to JET_wrnColumnPresent.</span></span> <span data-ttu-id="d12de-173">如果資料行或資料行值為 <strong>Null</strong> ，則會如往常般傳回 JET_wrnColumnNull。</span><span class="sxs-lookup"><span data-stu-id="d12de-173">If the column or column value is <strong>NULL</strong> then JET_wrnColumnNull will be returned as usual.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d12de-174">JET_bitEnumerateTaggedOnly</span><span class="sxs-lookup"><span data-stu-id="d12de-174">JET_bitEnumerateTaggedOnly</span></span></p></td>
<td><p><span data-ttu-id="d12de-175">列舉記錄中的所有資料行值時 (例如，當 <em>cEnumColumnId</em> 為零) 時，只會傳回已標記的資料行值。</span><span class="sxs-lookup"><span data-stu-id="d12de-175">When enumerating all column values in the record (for example,that is when <em>cEnumColumnId</em> is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="d12de-176">列舉資料行識別碼的特定陣列時，不允許使用這個選項。</span><span class="sxs-lookup"><span data-stu-id="d12de-176">This option is not allowed when enumerating a specific array of column IDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d12de-177">JET_bitEnumerateInRecordOnly</span><span class="sxs-lookup"><span data-stu-id="d12de-177">JET_bitEnumerateInRecordOnly</span></span></p></td>
<td><p><span data-ttu-id="d12de-178"><strong>Windows 7：  </strong>JET_bitEnumerateInRecordOnly 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="d12de-178"><strong>Windows 7:  </strong>JET_bitEnumerateInRecordOnly is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d12de-179">傳回值</span><span class="sxs-lookup"><span data-stu-id="d12de-179">Return Value</span></span>

<span data-ttu-id="d12de-180">此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="d12de-180">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d12de-181">如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="d12de-181">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d12de-182">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d12de-182">Return code</span></span></p></th>
<th><p><span data-ttu-id="d12de-183">Description</span><span class="sxs-lookup"><span data-stu-id="d12de-183">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d12de-184">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d12de-184">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d12de-185">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="d12de-185">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d12de-186">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="d12de-186">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="d12de-187">提供的資料行識別碼超出資料行識別碼的合法限制。</span><span class="sxs-lookup"><span data-stu-id="d12de-187">The column ID given is outside the legal limits of a column ID.</span></span> <span data-ttu-id="d12de-188">如果要求了特定的資料行識別碼、其中一個資料行識別碼無效，且第一個不正確資料行識別碼因為其資料行狀態碼的錯誤而失敗，則 <strong>JetEnumerateColumns</strong> 會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="d12de-188">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column ids were requested, one of those column ids was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d12de-189">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d12de-189">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d12de-190">無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</span><span class="sxs-lookup"><span data-stu-id="d12de-190">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d12de-191">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="d12de-191">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="d12de-192">給定資料行識別碼所描述的資料行不存在於資料表中。</span><span class="sxs-lookup"><span data-stu-id="d12de-192">The column described by the given column ID does not exist in the table.</span></span> <span data-ttu-id="d12de-193">如果要求了特定的資料行識別碼、其中一個資料行識別碼無效，且第一個不正確資料行識別碼因為其資料行狀態碼的錯誤而失敗，則 <strong>JetEnumerateColumns</strong> 會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="d12de-193">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column IDs were requested, one of those column IDs was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d12de-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d12de-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d12de-195">無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</span><span class="sxs-lookup"><span data-stu-id="d12de-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d12de-196"><strong>WINDOWS XP：  </strong>只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="d12de-196"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d12de-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="d12de-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="d12de-198">其中一個要求的選項無效或未執行。</span><span class="sxs-lookup"><span data-stu-id="d12de-198">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="d12de-199"><strong>JetEnumerateColumns</strong>會在下列情況傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="d12de-199">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="d12de-200">已指定 JET_bitEnumerateLocal。</span><span class="sxs-lookup"><span data-stu-id="d12de-200">JET_bitEnumerateLocal is specified.</span></span></p></li>
<li><p><span data-ttu-id="d12de-201">指定了不合法的 <em>grbit</em> 。</span><span class="sxs-lookup"><span data-stu-id="d12de-201">An illegal <em>grbit</em> is specified.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d12de-202">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d12de-202">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d12de-203">提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</span><span class="sxs-lookup"><span data-stu-id="d12de-203">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="d12de-204"><strong>JetEnumerateColumns</strong>會在下列情況傳回此錯誤：</span><span class="sxs-lookup"><span data-stu-id="d12de-204">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="d12de-205"><em>pcEnumColumn</em> 為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="d12de-205"><em>pcEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="d12de-206"><em>prgEnumColumn</em> 為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="d12de-206"><em>prgEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="d12de-207"><em>pfnRealloc</em> 為 <strong>Null</strong>。</span><span class="sxs-lookup"><span data-stu-id="d12de-207"><em>pfnRealloc</em> is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d12de-208">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="d12de-208">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="d12de-209">資料指標未放置在記錄上。</span><span class="sxs-lookup"><span data-stu-id="d12de-209">The cursor is not positioned on a record.</span></span> <span data-ttu-id="d12de-210">此情況具有許多不同的原因。</span><span class="sxs-lookup"><span data-stu-id="d12de-210">This can happen for many different reasons.</span></span> <span data-ttu-id="d12de-211">例如，如果資料指標目前位於目前索引的最後一筆記錄之後，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="d12de-211">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d12de-212">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d12de-212">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d12de-213">無法完成作業，因為與會話相關聯的實例尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="d12de-213">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d12de-214">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="d12de-214">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="d12de-215">游標位於已刪除的記錄上。</span><span class="sxs-lookup"><span data-stu-id="d12de-215">The cursor is positioned on a record that has been deleted.</span></span> <span data-ttu-id="d12de-216">此情況具有許多不同的原因。</span><span class="sxs-lookup"><span data-stu-id="d12de-216">This can happen for many different reasons.</span></span> <span data-ttu-id="d12de-217">最常見的原因是會話不在交易中、資料指標位於記錄上、刪除記錄，然後資料指標嘗試參考該記錄。</span><span class="sxs-lookup"><span data-stu-id="d12de-217">The most common reason is that the session is not in a transaction, the cursor was positioned on a record, that record was deleted, and then the cursor attempted to reference that record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d12de-218">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d12de-218">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d12de-219">無法完成作業，因為與會話相關聯的實例正在進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="d12de-219">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d12de-220">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d12de-220">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d12de-221">相同的會話無法同時用於一個以上的執行緒。</span><span class="sxs-lookup"><span data-stu-id="d12de-221">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d12de-222"><strong>WINDOWS XP：  </strong>只有 Windows XP 和更新版本才會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="d12de-222"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d12de-223">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d12de-223">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d12de-224">無法完成作業，因為與會話相關聯的實例正在關閉。</span><span class="sxs-lookup"><span data-stu-id="d12de-224">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d12de-225">成功時，會在輸出緩衝區中傳回所要求的資料。</span><span class="sxs-lookup"><span data-stu-id="d12de-225">On success, the requested data will be returned in the output buffers.</span></span> <span data-ttu-id="d12de-226">呼叫端必須負責釋放由此回呼配置並在輸出緩衝區中傳回的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="d12de-226">It is the caller's responsibility to free any memory allocated by this callback and returned in the output buffers.</span></span> <span data-ttu-id="d12de-227">您應該透過提供的 [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) 相容回呼來釋放該記憶體。</span><span class="sxs-lookup"><span data-stu-id="d12de-227">That memory should be freed through the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="d12de-228">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="d12de-228">No change to the database state will occur.</span></span>

<span data-ttu-id="d12de-229">失敗時，將不會傳回任何要求的資料。</span><span class="sxs-lookup"><span data-stu-id="d12de-229">On failure, none of the requested data will be returned.</span></span> <span data-ttu-id="d12de-230">在呼叫期間配置的任何記憶體都會使用提供的 [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) 相容回呼自動釋放。</span><span class="sxs-lookup"><span data-stu-id="d12de-230">Any memory that was allocated during the call will be freed automatically using the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="d12de-231">不會變更資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="d12de-231">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d12de-232">備註</span><span class="sxs-lookup"><span data-stu-id="d12de-232">Remarks</span></span>

<span data-ttu-id="d12de-233">如果您要列舉記錄中的所有資料行值，但未指定 JET_bitEnumerateIgnoreDefaults，則您無法假設您永遠不會看到狀態碼為 JET_wrnColumnNull 的資料行或資料行值。</span><span class="sxs-lookup"><span data-stu-id="d12de-233">If you are enumerating all column values in the record and you did not specify JET_bitEnumerateIgnoreDefaults then you cannot assume that you will never see a column or column value with a status code of JET_wrnColumnNull.</span></span> <span data-ttu-id="d12de-234">如果資料行有預設值，而且明確設定為 **Null** ，或者資料行是非稀疏資料行 (例如，固定或變數資料行) ，您就可以看到此狀態碼。</span><span class="sxs-lookup"><span data-stu-id="d12de-234">You can see this status code if a column has a default value and was explicitly set to **NULL** or if the column is a non-sparse column (for example, a fixed or variable column).</span></span>

<span data-ttu-id="d12de-235">*CbDataMost* 參數不適用於所有資料行值。</span><span class="sxs-lookup"><span data-stu-id="d12de-235">The *cbDataMost* parameter does not apply to all column values.</span></span> <span data-ttu-id="d12de-236">此參數只會截斷長文字和長二進位資料行值，而這些值很大，因此與記錄分開儲存。</span><span class="sxs-lookup"><span data-stu-id="d12de-236">This parameter will only truncate long text and long binary column values that are so large that they have been stored separately from the record.</span></span>

<span data-ttu-id="d12de-237">如果 **JetEnumerateColumns** 在其輸出參數中傳回資料，則呼叫端會負責釋放陣列中的記憶體，以及內嵌在該陣列中的指標所參考的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="d12de-237">If **JetEnumerateColumns** returns data in its output parameters then the caller is responsible for freeing the memory in the array as well as any memory referred to by pointers embedded in that array.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d12de-238">規格需求</span><span class="sxs-lookup"><span data-stu-id="d12de-238">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d12de-239"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="d12de-239"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d12de-240">需要 Windows Vista 或 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="d12de-240">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d12de-241"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="d12de-241"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d12de-242">需要 Windows Server 2008 或 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="d12de-242">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d12de-243"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="d12de-243"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d12de-244">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="d12de-244">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d12de-245"><strong>程式庫</strong></span><span class="sxs-lookup"><span data-stu-id="d12de-245"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d12de-246">使用 ESENT。</span><span class="sxs-lookup"><span data-stu-id="d12de-246">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d12de-247"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d12de-247"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d12de-248">需要 ESENT.dll。</span><span class="sxs-lookup"><span data-stu-id="d12de-248">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d12de-249">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d12de-249">See Also</span></span>

[<span data-ttu-id="d12de-250">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d12de-250">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d12de-251">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d12de-251">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d12de-252">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d12de-252">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d12de-253">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d12de-253">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d12de-254">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="d12de-254">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="d12de-255">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="d12de-255">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="d12de-256">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="d12de-256">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="d12de-257">JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="d12de-257">JET_PFNREALLOC</span></span>](./jet-pfnrealloc-callback-function.md)  
[<span data-ttu-id="d12de-258">realloc</span><span class="sxs-lookup"><span data-stu-id="d12de-258">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[<span data-ttu-id="d12de-259">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="d12de-259">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="d12de-260">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="d12de-260">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
