---
description: 深入瞭解： JET_ENUMCOLUMNVALUE 結構
title: JET_ENUMCOLUMNVALUE 結構
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
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
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980605"
---
# <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="c8c36-103">JET_ENUMCOLUMNVALUE 結構</span><span class="sxs-lookup"><span data-stu-id="c8c36-103">JET_ENUMCOLUMNVALUE Structure</span></span>


<span data-ttu-id="c8c36-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c8c36-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="c8c36-105">JET_ENUMCOLUMNVALUE 結構</span><span class="sxs-lookup"><span data-stu-id="c8c36-105">JET_ENUMCOLUMNVALUE Structure</span></span>

<span data-ttu-id="c8c36-106">**JET_ENUMCOLUMNVALUE** 結構會使用 [JetEnumerateColumns](./jetenumeratecolumns-function.md)函數來列舉記錄的資料行值。</span><span class="sxs-lookup"><span data-stu-id="c8c36-106">The **JET_ENUMCOLUMNVALUE** structure enumerates the column values of a record using the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function.</span></span> <span data-ttu-id="c8c36-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) 會傳回 **JET_ENUMCOLUMNVALUE** 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="c8c36-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNVALUE** structures.</span></span> <span data-ttu-id="c8c36-108">陣列會在使用提供給該函式之 [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) 相容回呼所配置的記憶體中傳回。</span><span class="sxs-lookup"><span data-stu-id="c8c36-108">The array is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that function.</span></span>

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a><span data-ttu-id="c8c36-109">成員</span><span class="sxs-lookup"><span data-stu-id="c8c36-109">Members</span></span>

<span data-ttu-id="c8c36-110">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="c8c36-110">**itagSequence**</span></span>

<span data-ttu-id="c8c36-111">以一為基礎的索引) 所 (的資料行值。</span><span class="sxs-lookup"><span data-stu-id="c8c36-111">The column value (by one-based index) that was enumerated.</span></span>

<span data-ttu-id="c8c36-112">**犯 錯**</span><span class="sxs-lookup"><span data-stu-id="c8c36-112">**err**</span></span>

<span data-ttu-id="c8c36-113">由資料行值列舉所產生的資料行狀態碼。</span><span class="sxs-lookup"><span data-stu-id="c8c36-113">The column status code resulting from the enumeration of the column value.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8c36-114">值</span><span class="sxs-lookup"><span data-stu-id="c8c36-114">Value</span></span></p></th>
<th><p><span data-ttu-id="c8c36-115">意義</span><span class="sxs-lookup"><span data-stu-id="c8c36-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8c36-116">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="c8c36-116">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="c8c36-117">要求的資料行值為 Null。</span><span class="sxs-lookup"><span data-stu-id="c8c36-117">The requested column value is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8c36-118">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="c8c36-118">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="c8c36-119">在對應于此<strong>JET_ENUMCOLUMNVALUE</strong>結構的<a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a>結構中，于<em>rgtagSequence</em>陣列的元素中指定的<em>itagSequence</em>為零。</span><span class="sxs-lookup"><span data-stu-id="c8c36-119">The <em>itagSequence</em> that is specified in the element of the <em>rgtagSequence</em> array in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> struct corresponding to this <strong>JET_ENUMCOLUMNVALUE</strong> struct was zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8c36-120">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="c8c36-120">JET_wrnColumnTruncated</span></span></p></td>
<td><p><span data-ttu-id="c8c36-121">要求的資料行值在傳回之前已被截斷為指定的大小。</span><span class="sxs-lookup"><span data-stu-id="c8c36-121">The requested column value was truncated to the specified size before being returned.</span></span></p>
<p><span data-ttu-id="c8c36-122">只有包含大量資料的長文字和長二進位資料行才會發生截斷。</span><span class="sxs-lookup"><span data-stu-id="c8c36-122">This truncation occurs only for long text and long binary columns that contain large amounts of data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8c36-123">**cbData**</span><span class="sxs-lookup"><span data-stu-id="c8c36-123">**cbData**</span></span>

<span data-ttu-id="c8c36-124">為數據行列舉的資料行值。</span><span class="sxs-lookup"><span data-stu-id="c8c36-124">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="c8c36-125">輸出緩衝區會在記憶體中傳回，該記憶體是使用提供給[JetEnumerateColumns](./jetenumeratecolumns-function.md)的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼來配置。</span><span class="sxs-lookup"><span data-stu-id="c8c36-125">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="c8c36-126">**pvData**</span><span class="sxs-lookup"><span data-stu-id="c8c36-126">**pvData**</span></span>

<span data-ttu-id="c8c36-127">為數據行列舉的資料行值。</span><span class="sxs-lookup"><span data-stu-id="c8c36-127">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="c8c36-128">輸出緩衝區會在記憶體中傳回，該記憶體是使用提供給[JetEnumerateColumns](./jetenumeratecolumns-function.md)的[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)相容回呼來配置。</span><span class="sxs-lookup"><span data-stu-id="c8c36-128">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="c8c36-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8c36-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8c36-130"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="c8c36-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c8c36-131">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="c8c36-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8c36-132"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="c8c36-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c8c36-133">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="c8c36-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8c36-134"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="c8c36-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c8c36-135">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="c8c36-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c8c36-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8c36-136">See Also</span></span>

[<span data-ttu-id="c8c36-137">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="c8c36-137">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="c8c36-138">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="c8c36-138">JET_ENUMCOLUMNVALUE</span></span>]()  
[<span data-ttu-id="c8c36-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c8c36-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c8c36-140">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="c8c36-140">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="c8c36-141">realloc</span><span class="sxs-lookup"><span data-stu-id="c8c36-141">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
