---
description: 深入瞭解： JET_INDEXRANGE 結構
title: JET_INDEXRANGE 結構
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
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
ms.openlocfilehash: ecbd8151be8ef278fc1bddc12323f41abd05b09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997840"
---
# <a name="jet_indexrange-structure"></a><span data-ttu-id="405dd-103">JET_INDEXRANGE 結構</span><span class="sxs-lookup"><span data-stu-id="405dd-103">JET_INDEXRANGE Structure</span></span>


<span data-ttu-id="405dd-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="405dd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexrange-structure"></a><span data-ttu-id="405dd-105">JET_INDEXRANGE 結構</span><span class="sxs-lookup"><span data-stu-id="405dd-105">JET_INDEXRANGE Structure</span></span>

<span data-ttu-id="405dd-106">使用 [JetIntersectIndexes](./jetintersectindexes-function.md)函式時， **JET_INDEXRANGE** 結構會識別索引範圍。</span><span class="sxs-lookup"><span data-stu-id="405dd-106">The **JET_INDEXRANGE** structure identifies an index range when it is used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a><span data-ttu-id="405dd-107">成員</span><span class="sxs-lookup"><span data-stu-id="405dd-107">Members</span></span>

<span data-ttu-id="405dd-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="405dd-108">**cbStruct**</span></span>

<span data-ttu-id="405dd-109">**JET_INDEXRANGE** 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="405dd-109">The size, in bytes, of the **JET_INDEXRANGE**.</span></span>

<span data-ttu-id="405dd-110">**tableid**</span><span class="sxs-lookup"><span data-stu-id="405dd-110">**tableid**</span></span>

<span data-ttu-id="405dd-111">先前已有索引範圍設定為 [JetSetIndexRange](./jetsetindexrange-function.md)的資料指標。</span><span class="sxs-lookup"><span data-stu-id="405dd-111">A cursor that has previously had an index range set with [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="405dd-112">**grbit**</span><span class="sxs-lookup"><span data-stu-id="405dd-112">**grbit**</span></span>

<span data-ttu-id="405dd-113">僅由下列其中一項組成的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="405dd-113">A bitmask composed of exactly one of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="405dd-114">值</span><span class="sxs-lookup"><span data-stu-id="405dd-114">Value</span></span></p></th>
<th><p><span data-ttu-id="405dd-115">意義</span><span class="sxs-lookup"><span data-stu-id="405dd-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="405dd-116">JET_bitRecordInIndex</span><span class="sxs-lookup"><span data-stu-id="405dd-116">JET_bitRecordInIndex</span></span></p></td>
<td><p><span data-ttu-id="405dd-117">指定索引範圍應正常處理。</span><span class="sxs-lookup"><span data-stu-id="405dd-117">Specifies that the index range should be treated normally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="405dd-118">JET_bitRecordNotInIndex</span><span class="sxs-lookup"><span data-stu-id="405dd-118">JET_bitRecordNotInIndex</span></span></p></td>
<td><p><span data-ttu-id="405dd-119">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="405dd-119">Reserved for future use.</span></span> <span data-ttu-id="405dd-120">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="405dd-120">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="405dd-121">備註</span><span class="sxs-lookup"><span data-stu-id="405dd-121">Remarks</span></span>

<span data-ttu-id="405dd-122">傳遞至 [JetIntersectIndexes](./jetintersectindexes-function.md)的每個 **JET_INDEXRANGE** 結構代表一個索引範圍，此範圍將由 API 呼叫來交集。</span><span class="sxs-lookup"><span data-stu-id="405dd-122">Each **JET_INDEXRANGE** structure that is passed to [JetIntersectIndexes](./jetintersectindexes-function.md) represents an index range, which will be intersected by the API call.</span></span> <span data-ttu-id="405dd-123">**JET_INDEXRANGE** 中提供的資料指標必須已經設定有效的索引範圍，且成功呼叫 [JetSetIndexRange](./jetsetindexrange-function.md)。</span><span class="sxs-lookup"><span data-stu-id="405dd-123">The cursor that is given in **JET_INDEXRANGE** must have a valid index range set on it already, with a successful call to [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="405dd-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="405dd-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="405dd-125"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="405dd-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="405dd-126">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="405dd-126">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="405dd-127"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="405dd-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="405dd-128">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="405dd-128">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="405dd-129"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="405dd-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="405dd-130">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="405dd-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="405dd-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="405dd-131">See Also</span></span>

[<span data-ttu-id="405dd-132">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="405dd-132">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="405dd-133">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="405dd-133">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="405dd-134">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="405dd-134">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="405dd-135">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="405dd-135">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="405dd-136">JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="405dd-136">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="405dd-137">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="405dd-137">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
