---
description: 深入瞭解： JET_ENUMCOLUMN 結構
title: JET_ENUMCOLUMN 結構
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
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
ms.openlocfilehash: ca204fef4e67e6883584511b1ac424149a137b79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112108"
---
# <a name="jet_enumcolumn-structure"></a><span data-ttu-id="ee2ed-103">JET_ENUMCOLUMN 結構</span><span class="sxs-lookup"><span data-stu-id="ee2ed-103">JET_ENUMCOLUMN Structure</span></span>


<span data-ttu-id="ee2ed-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ee2ed-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumn-structure"></a><span data-ttu-id="ee2ed-105">JET_ENUMCOLUMN 結構</span><span class="sxs-lookup"><span data-stu-id="ee2ed-105">JET_ENUMCOLUMN Structure</span></span>

<span data-ttu-id="ee2ed-106">使用 [JetEnumerateColumns](./jetenumeratecolumns-function.md)函數時， **JET_ENUMCOLUMN** 結構會列舉記錄的資料行值。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-106">The **JET_ENUMCOLUMN** structure enumerates the column values of a record when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="ee2ed-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) 會傳回 **JET_ENUMCOLUMN** 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMN** structures.</span></span> <span data-ttu-id="ee2ed-108">陣列會在記憶體中傳回，此記憶體是使用提供給該 API 的 [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) 相容回呼來配置。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-108">The array is returned in memory that is allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that API.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a><span data-ttu-id="ee2ed-109">成員</span><span class="sxs-lookup"><span data-stu-id="ee2ed-109">Members</span></span>

<span data-ttu-id="ee2ed-110">**columnid**</span><span class="sxs-lookup"><span data-stu-id="ee2ed-110">**columnid**</span></span>

<span data-ttu-id="ee2ed-111">列舉的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-111">The column ID that was enumerated.</span></span>

<span data-ttu-id="ee2ed-112">**犯 錯**</span><span class="sxs-lookup"><span data-stu-id="ee2ed-112">**err**</span></span>

<span data-ttu-id="ee2ed-113">由資料行列舉所產生的資料行狀態碼。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-113">The column status code that results from the enumeration of the column.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee2ed-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ee2ed-114">Error Codes</span></span></p></th>
<th><p><span data-ttu-id="ee2ed-115">意義</span><span class="sxs-lookup"><span data-stu-id="ee2ed-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee2ed-116">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="ee2ed-116">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="ee2ed-117">資料行識別碼超出資料行識別碼的合法限制。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-117">The column ID is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee2ed-118">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="ee2ed-118">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="ee2ed-119">資料行識別碼所描述的資料行不存在於資料表中。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-119">The column described by the column ID does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee2ed-120">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="ee2ed-120">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="ee2ed-121">此資料行的所有值都是 Null。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-121">All values for this column are NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee2ed-122">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="ee2ed-122">JET_wrnColumnPresent</span></span></p></td>
<td><p><span data-ttu-id="ee2ed-123">指定了 JET_bitEnumeratePresenceOnly，而且此資料行至少有一個非 Null 的資料行值會傳回。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-123">JET_bitEnumeratePresenceOnly was specified and at least one non-NULL column value would have been returned for this column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee2ed-124">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="ee2ed-124">JET_wrnColumnSingleValue</span></span></p></td>
<td><p><span data-ttu-id="ee2ed-125">已指定 JET_bitEnumerateCompressOutput，且已為此資料行傳回剛好一個非 Null 的資料行值。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-125">JET_bitEnumerateCompressOutput was specified and exactly one non-NULL column value has been returned for this column.</span></span> <span data-ttu-id="ee2ed-126">如此一來，就會傳回壓縮格式的 <strong>JET_ENUMCOLUMN</strong> 。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-126">As a result, the compressed form of <strong>JET_ENUMCOLUMN</strong> has been returned.</span></span> <span data-ttu-id="ee2ed-127">如需詳細資訊，請參閱 <strong>JET_ENUMCOLUMN</strong> 。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-127">See <strong>JET_ENUMCOLUMN</strong> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee2ed-128">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="ee2ed-128">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="ee2ed-129">對應至此<strong>JET_ENUMCOLUMN</strong>結構的<a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a>結構中的資料行識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-129">The column ID in the <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> struct corresponding to this <strong>JET_ENUMCOLUMN</strong> struct was zero.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ee2ed-130">**cEnumColumnValue**</span><span class="sxs-lookup"><span data-stu-id="ee2ed-130">**cEnumColumnValue**</span></span>

<span data-ttu-id="ee2ed-131">針對資料行列舉的資料行值陣列。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-131">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="ee2ed-132">輸出緩衝區會在記憶體中傳回，該記憶體是使用提供給[JetEnumerateColumns](./jetenumeratecolumns-function.md)的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼來配置。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-132">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="ee2ed-133">當資料行狀態碼不等於 JET_wrnColumnSingleValue 時，會使用這個輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-133">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="ee2ed-134">如需詳細資訊，請參閱 [JetEnumerateColumns](./jetenumeratecolumns-function.md)。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-134">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="ee2ed-135">如果 "err = JET_wrnColumnSingleValue"，則會傳回 \! 。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-135">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="ee2ed-136">**rgEnumColumnValue**</span><span class="sxs-lookup"><span data-stu-id="ee2ed-136">**rgEnumColumnValue**</span></span>

<span data-ttu-id="ee2ed-137">針對資料行列舉的資料行值陣列。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-137">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="ee2ed-138">輸出緩衝區會在記憶體中傳回，該記憶體是使用提供給[JetEnumerateColumns](./jetenumeratecolumns-function.md)的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼來配置。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-138">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="ee2ed-139">當資料行狀態碼不等於 JET_wrnColumnSingleValue 時，會使用這個輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-139">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="ee2ed-140">如需詳細資訊，請參閱 [JetEnumerateColumns](./jetenumeratecolumns-function.md)。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-140">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="ee2ed-141">如果 "err = JET_wrnColumnSingleValue"，則會傳回 \! 。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-141">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="ee2ed-142">**cbData**</span><span class="sxs-lookup"><span data-stu-id="ee2ed-142">**cbData**</span></span>

<span data-ttu-id="ee2ed-143">為數據行列舉的資料行值。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-143">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="ee2ed-144">輸出緩衝區會在記憶體中傳回，該記憶體是使用提供給[JetEnumerateColumns](./jetenumeratecolumns-function.md)的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼來配置。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-144">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="ee2ed-145">只有在 JET_wrnColumnSingleValue 資料行狀態碼時，才會使用此輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-145">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="ee2ed-146">如需詳細資訊，請參閱 [JetEnumerateColumns](./jetenumeratecolumns-function.md)。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-146">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="ee2ed-147">如果 "err = = JET_wrnColumnSingleValue"，則會傳回。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-147">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="ee2ed-148">**pvData**</span><span class="sxs-lookup"><span data-stu-id="ee2ed-148">**pvData**</span></span>

<span data-ttu-id="ee2ed-149">為數據行列舉的資料行值。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-149">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="ee2ed-150">輸出緩衝區會在記憶體中傳回，該記憶體是使用提供給[JetEnumerateColumns](./jetenumeratecolumns-function.md)的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼來配置。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-150">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="ee2ed-151">只有在 JET_wrnColumnSingleValue 資料行狀態碼時，才會使用此輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-151">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="ee2ed-152">如需詳細資訊，請參閱 [JetEnumerateColumns](./jetenumeratecolumns-function.md)。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-152">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="ee2ed-153">如果 "err = = JET_wrnColumnSingleValue"，則會傳回。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-153">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

### <a name="requirements"></a><span data-ttu-id="ee2ed-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee2ed-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee2ed-155"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="ee2ed-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ee2ed-156">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-156">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee2ed-157"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="ee2ed-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ee2ed-158">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-158">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee2ed-159"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="ee2ed-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ee2ed-160">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="ee2ed-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ee2ed-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee2ed-161">See Also</span></span>

[<span data-ttu-id="ee2ed-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="ee2ed-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="ee2ed-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ee2ed-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ee2ed-164">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="ee2ed-164">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="ee2ed-165">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="ee2ed-165">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="ee2ed-166">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="ee2ed-166">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="ee2ed-167">realloc</span><span class="sxs-lookup"><span data-stu-id="ee2ed-167">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
