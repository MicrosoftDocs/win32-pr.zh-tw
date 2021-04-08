---
description: 深入瞭解： JET_RECORDLIST 結構
title: JET_RECORDLIST 結構
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852256"
---
# <a name="jet_recordlist-structure"></a><span data-ttu-id="f9e69-103">JET_RECORDLIST 結構</span><span class="sxs-lookup"><span data-stu-id="f9e69-103">JET_RECORDLIST Structure</span></span>


<span data-ttu-id="f9e69-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f9e69-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recordlist-structure"></a><span data-ttu-id="f9e69-105">JET_RECORDLIST 結構</span><span class="sxs-lookup"><span data-stu-id="f9e69-105">JET_RECORDLIST Structure</span></span>

<span data-ttu-id="f9e69-106">**JET_RECORDLIST** 結構會在與 [JetIntersectIndexes](./jetintersectindexes-function.md)函數搭配使用時，尋找位於指定索引範圍交集內的記錄。</span><span class="sxs-lookup"><span data-stu-id="f9e69-106">The **JET_RECORDLIST** structure finds records that are in the intersection of specified index ranges when they are used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a><span data-ttu-id="f9e69-107">成員</span><span class="sxs-lookup"><span data-stu-id="f9e69-107">Members</span></span>

<span data-ttu-id="f9e69-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="f9e69-108">**cbStruct**</span></span>

<span data-ttu-id="f9e69-109">**JET_RECORDLIST** 結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f9e69-109">The size of the **JET_RECORDLIST** structure, in bytes.</span></span>

<span data-ttu-id="f9e69-110">**tableid**</span><span class="sxs-lookup"><span data-stu-id="f9e69-110">**tableid**</span></span>

<span data-ttu-id="f9e69-111">臨時表的資料表識別碼，包含查詢結果的書簽。</span><span class="sxs-lookup"><span data-stu-id="f9e69-111">The table identifier of a temporary table that contains the bookmarks for the results of the query.</span></span> <span data-ttu-id="f9e69-112">如果使用 [JetRollback](./jetrollback-function.md)復原目前的交易，則會自動關閉資料表;否則，必須使用 [JetCloseTable](./jetclosetable-function.md)來關閉它。</span><span class="sxs-lookup"><span data-stu-id="f9e69-112">The table will automatically be closed if the current transaction is rolled back with [JetRollback](./jetrollback-function.md); otherwise, it must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="f9e69-113">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="f9e69-113">**cRecord**</span></span>

<span data-ttu-id="f9e69-114">臨時表中的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="f9e69-114">The number of rows in the temporary table.</span></span>

<span data-ttu-id="f9e69-115">**columnidBookmark**</span><span class="sxs-lookup"><span data-stu-id="f9e69-115">**columnidBookmark**</span></span>

<span data-ttu-id="f9e69-116">臨時表中書簽資料行的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9e69-116">The column identifier of the bookmark column in the temporary table.</span></span>

### <a name="remarks"></a><span data-ttu-id="f9e69-117">備註</span><span class="sxs-lookup"><span data-stu-id="f9e69-117">Remarks</span></span>

<span data-ttu-id="f9e69-118">**Tableid** 所識別的臨時表具有單一資料行。</span><span class="sxs-lookup"><span data-stu-id="f9e69-118">The temporary table that is identified by **tableid** has a single column.</span></span> <span data-ttu-id="f9e69-119">該單一資料行包含書簽，而且每一筆記錄都應符合 JET_cbBookmarkMost 位元組大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f9e69-119">That single column holds bookmarks, and each record should fit in a buffer of size JET_cbBookmarkMost bytes.</span></span>

### <a name="requirements"></a><span data-ttu-id="f9e69-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9e69-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9e69-121"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="f9e69-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f9e69-122">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="f9e69-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9e69-123"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="f9e69-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f9e69-124">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="f9e69-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9e69-125"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="f9e69-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f9e69-126">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="f9e69-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f9e69-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9e69-127">See Also</span></span>

[<span data-ttu-id="f9e69-128">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="f9e69-128">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="f9e69-129">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f9e69-129">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f9e69-130">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f9e69-130">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f9e69-131">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="f9e69-131">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="f9e69-132">JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="f9e69-132">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="f9e69-133">JetRollback</span><span class="sxs-lookup"><span data-stu-id="f9e69-133">JetRollback</span></span>](./jetrollback-function.md)
