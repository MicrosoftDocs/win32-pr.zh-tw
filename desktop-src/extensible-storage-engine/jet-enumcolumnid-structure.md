---
description: 深入瞭解： JET_ENUMCOLUMNID 結構
title: JET_ENUMCOLUMNID 結構
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
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
ms.openlocfilehash: 356b2a31c682a6ed0392a875c606cfaf20f1aeea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511384"
---
# <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="ac641-103">JET_ENUMCOLUMNID 結構</span><span class="sxs-lookup"><span data-stu-id="ac641-103">JET_ENUMCOLUMNID Structure</span></span>


<span data-ttu-id="ac641-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ac641-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="ac641-105">JET_ENUMCOLUMNID 結構</span><span class="sxs-lookup"><span data-stu-id="ac641-105">JET_ENUMCOLUMNID Structure</span></span>

<span data-ttu-id="ac641-106">當使用 [JetEnumerateColumns](./jetenumeratecolumns-function.md)函式時， **JET_ENUMCOLUMNID** 結構會列舉一組特定的資料行，並選擇性地列舉這些資料行的一組特定的多個值。</span><span class="sxs-lookup"><span data-stu-id="ac641-106">The **JET_ENUMCOLUMNID** structure enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="ac641-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) 會傳回 **JET_ENUMCOLUMNID** 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="ac641-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNID** structures.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a><span data-ttu-id="ac641-108">成員</span><span class="sxs-lookup"><span data-stu-id="ac641-108">Members</span></span>

<span data-ttu-id="ac641-109">**columnid**</span><span class="sxs-lookup"><span data-stu-id="ac641-109">**columnid**</span></span>

<span data-ttu-id="ac641-110">要列舉的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac641-110">The column ID to enumerate.</span></span>

<span data-ttu-id="ac641-111">如果資料行識別碼為 0 (零) 則會略過此資料行的列舉，而 [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) 結構輸出陣列中的對應位置將會產生 JET_wrnColumnSkipped 的資料行狀態。</span><span class="sxs-lookup"><span data-stu-id="ac641-111">If the column ID is 0 (zero) then the enumeration of this column is skipped and a corresponding slot in the output array of [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) structures will be generated with a column state of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="ac641-112">**ctagSequence**</span><span class="sxs-lookup"><span data-stu-id="ac641-112">**ctagSequence**</span></span>

<span data-ttu-id="ac641-113">選擇性地識別資料行值的陣列，此陣列 (由一) 的索引，以列舉指定的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac641-113">Optionally identifies an array of column values (by one-based index) to enumerate for the specified column ID.</span></span>

<span data-ttu-id="ac641-114">如果 **ctagSequence** 為 0 (零) 則會忽略 **rgtagSequence** ，並且會列舉指定之資料行識別碼的所有資料行值。</span><span class="sxs-lookup"><span data-stu-id="ac641-114">If **ctagSequence** is 0 (zero) then **rgtagSequence** is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="ac641-115">如果 **rgtagSequence** 的元素為 0 (零) ，則會略過以一個索引)  (的該資料行值的列舉。</span><span class="sxs-lookup"><span data-stu-id="ac641-115">If an element of **rgtagSequence** is 0 (zero), then the enumeration of that column value (by one-based index) will be skipped.</span></span> <span data-ttu-id="ac641-116">**JET_ENUMCOLUMNID** 結構之輸出陣列中的對應位置將會產生 JET_wrnColumnSkipped 的資料行狀態值。</span><span class="sxs-lookup"><span data-stu-id="ac641-116">A corresponding slot in the output array of the **JET_ENUMCOLUMNID** structure will be generated with a column status value of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="ac641-117">**rgtagSequence**</span><span class="sxs-lookup"><span data-stu-id="ac641-117">**rgtagSequence**</span></span>

<span data-ttu-id="ac641-118">給定資料行的資料行值陣列中，以一個為基底的索引陣列。</span><span class="sxs-lookup"><span data-stu-id="ac641-118">An array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="ac641-119">單一元素是 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)中定義的 **itagSequence** 。</span><span class="sxs-lookup"><span data-stu-id="ac641-119">A single element is an **itagSequence** which is defined in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="ac641-120">**ItagSequence** 0 (零) 表示「略過」。</span><span class="sxs-lookup"><span data-stu-id="ac641-120">An **itagSequence** of 0 (zero) means "skip".</span></span> <span data-ttu-id="ac641-121">1的 **itagSequence** 表示會傳回資料行的第一個資料行值，2表示第二個數據行的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="ac641-121">An **itagSequence** of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

### <a name="requirements"></a><span data-ttu-id="ac641-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac641-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac641-123"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="ac641-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ac641-124">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="ac641-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac641-125"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="ac641-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ac641-126">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="ac641-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac641-127"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="ac641-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ac641-128">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="ac641-128">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ac641-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac641-129">See Also</span></span>

[<span data-ttu-id="ac641-130">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="ac641-130">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="ac641-131">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="ac641-131">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="ac641-132">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="ac641-132">JET_ENUMCOLUMNID</span></span>]()  
[<span data-ttu-id="ac641-133">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="ac641-133">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="ac641-134">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="ac641-134">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
