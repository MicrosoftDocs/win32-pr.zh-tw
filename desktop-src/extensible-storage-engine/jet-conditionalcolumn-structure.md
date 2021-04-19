---
description: 深入瞭解： JET_CONDITIONALCOLUMN 結構
title: JET_CONDITIONALCOLUMN 結構
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979015"
---
# <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="2a38c-103">JET_CONDITIONALCOLUMN 結構</span><span class="sxs-lookup"><span data-stu-id="2a38c-103">JET_CONDITIONALCOLUMN Structure</span></span>


<span data-ttu-id="2a38c-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2a38c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="2a38c-105">JET_CONDITIONALCOLUMN 結構</span><span class="sxs-lookup"><span data-stu-id="2a38c-105">JET_CONDITIONALCOLUMN Structure</span></span>

<span data-ttu-id="2a38c-106">**JET_CONDITIONALCOLUMN** 結構定義如何針對指定的索引執行條件式索引編制。</span><span class="sxs-lookup"><span data-stu-id="2a38c-106">The **JET_CONDITIONALCOLUMN** structure defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="2a38c-107">條件式索引僅包含符合指定條件之資料列的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="2a38c-107">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="2a38c-108">不過，條件資料行不是索引索引鍵的一部分，而只會控制索引項目是否存在。</span><span class="sxs-lookup"><span data-stu-id="2a38c-108">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a><span data-ttu-id="2a38c-109">成員</span><span class="sxs-lookup"><span data-stu-id="2a38c-109">Members</span></span>

<span data-ttu-id="2a38c-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="2a38c-110">**cbStruct**</span></span>

<span data-ttu-id="2a38c-111">此欄位必須初始化為 sizeof ( JET_CONDITIONALCOLUMN ) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2a38c-111">This field must be initialized to sizeof( JET_CONDITIONALCOLUMN ), in bytes.</span></span>

<span data-ttu-id="2a38c-112">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="2a38c-112">**szColumnName**</span></span>

<span data-ttu-id="2a38c-113">資料行的名稱，此資料行包含資料庫引擎有條件地索引資料列的資料。</span><span class="sxs-lookup"><span data-stu-id="2a38c-113">The name of the column that contains the data on which the database engine is conditionally indexing the row.</span></span>

<span data-ttu-id="2a38c-114">**grbit** 提供條件式索引選項的位群組。</span><span class="sxs-lookup"><span data-stu-id="2a38c-114">**grbit** A group of bits that gives the options for the conditional index.</span></span> <span data-ttu-id="2a38c-115">傳入零或邏輯 **或** ed 值對於 **JET_CONDITIONALCOLUMN** 無效。</span><span class="sxs-lookup"><span data-stu-id="2a38c-115">Passing in zero or logically-**OR** ed values is not valid for **JET_CONDITIONALCOLUMN**.</span></span> <span data-ttu-id="2a38c-116">位欄位必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="2a38c-116">The bit field must be exactly one of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a38c-117">值</span><span class="sxs-lookup"><span data-stu-id="2a38c-117">Value</span></span></p></th>
<th><p><span data-ttu-id="2a38c-118">意義</span><span class="sxs-lookup"><span data-stu-id="2a38c-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a38c-119">JET_bitIndexColumnMustBeNull</span><span class="sxs-lookup"><span data-stu-id="2a38c-119">JET_bitIndexColumnMustBeNull</span></span></p></td>
<td><p><span data-ttu-id="2a38c-120"><em>SzColumnName</em>參數所指定的資料行必須是 Null，指定資料列的索引項目才會出現在此索引中。</span><span class="sxs-lookup"><span data-stu-id="2a38c-120">The column specified by the <em>szColumnName</em> parameter must be NULL for an index entry for a given row to appear in this index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a38c-121">JET_bitIndexColumnMustBeNonNull</span><span class="sxs-lookup"><span data-stu-id="2a38c-121">JET_bitIndexColumnMustBeNonNull</span></span></p></td>
<td><p><span data-ttu-id="2a38c-122"><em>SzColumnName</em>參數所指定的資料行必須是索引項目的非 Null，才能讓指定的資料列出現在此索引中。</span><span class="sxs-lookup"><span data-stu-id="2a38c-122">The column specified by the <em>szColumnName</em> parameter must be non-NULL for an index entry in order for a given row to appear in this index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="2a38c-123">備註</span><span class="sxs-lookup"><span data-stu-id="2a38c-123">Remarks</span></span>

<span data-ttu-id="2a38c-124">條件式索引僅包含符合指定條件之資料列的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="2a38c-124">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="2a38c-125">例如，資料行可以命名為「標記」，而當資料列被標記時，資料行會設定為非 Null 值。</span><span class="sxs-lookup"><span data-stu-id="2a38c-125">For example, a column could be named "Marked", and when a row is marked, the column is set to a non-NULL value.</span></span> <span data-ttu-id="2a38c-126">這個資料行上的 JET_bitIndexColumnMustBeNonNull 條件式索引會顯示所有標記的資料列，而 JET_bitIndexColumnMustBeNull 的條件索引會顯示未標記的資料列。</span><span class="sxs-lookup"><span data-stu-id="2a38c-126">A JET_bitIndexColumnMustBeNonNull conditional index on this column will show all rows that are marked, and a JET_bitIndexColumnMustBeNull conditional index will show rows that are not marked.</span></span> <span data-ttu-id="2a38c-127">這也是執行旗標刪除和垃圾收集索引的便利方式。</span><span class="sxs-lookup"><span data-stu-id="2a38c-127">This is also a convenient way to perform a flag deletion and garbage collecting index.</span></span>

### <a name="requirements"></a><span data-ttu-id="2a38c-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a38c-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a38c-129"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="2a38c-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2a38c-130">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="2a38c-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a38c-131"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="2a38c-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2a38c-132">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="2a38c-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a38c-133"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="2a38c-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2a38c-134">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="2a38c-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a38c-135"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2a38c-135"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2a38c-136">實作為 <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) 和 <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI) 。</span><span class="sxs-lookup"><span data-stu-id="2a38c-136">Implemented as <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) and <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2a38c-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a38c-137">See Also</span></span>

[<span data-ttu-id="2a38c-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2a38c-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2a38c-139">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="2a38c-139">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)
