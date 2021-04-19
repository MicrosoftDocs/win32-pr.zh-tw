---
description: 深入瞭解： JET_INDEXID 結構
title: JET_INDEXID 結構
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
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
ms.openlocfilehash: e1a9c6a971e44604240d750163f0570937f9d4db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999954"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="cf35d-103">JET_INDEXID 結構</span><span class="sxs-lookup"><span data-stu-id="cf35d-103">JET_INDEXID Structure</span></span>


<span data-ttu-id="cf35d-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cf35d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexid-structure"></a><span data-ttu-id="cf35d-105">JET_INDEXID 結構</span><span class="sxs-lookup"><span data-stu-id="cf35d-105">JET_INDEXID Structure</span></span>

<span data-ttu-id="cf35d-106">**JET_INDEXID** 結構會保存索引識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf35d-106">The **JET_INDEXID** structure holds an index ID.</span></span> <span data-ttu-id="cf35d-107">索引識別碼是用來加速使用 [JetSetCurrentIndex](./jetsetcurrentindex-function.md)來選取目前索引的提示。</span><span class="sxs-lookup"><span data-stu-id="cf35d-107">An index ID is a hint that is used to accelerate the selection of the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="cf35d-108">當資料表的索引數量非常龐大時，最有用。</span><span class="sxs-lookup"><span data-stu-id="cf35d-108">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="cf35d-109">您可以使用 [JetGetIndexInfo](./jetgetindexinfo-function.md) 或 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)來取出索引識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf35d-109">The index ID can be retrieved using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a><span data-ttu-id="cf35d-110">成員</span><span class="sxs-lookup"><span data-stu-id="cf35d-110">Members</span></span>

<span data-ttu-id="cf35d-111">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="cf35d-111">**cbStruct**</span></span>

<span data-ttu-id="cf35d-112">索引識別碼的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cf35d-112">The size, in bytes, of the index ID.</span></span>

<span data-ttu-id="cf35d-113">這是在 [JetGetIndexInfo](./jetgetindexinfo-function.md) 或 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)輸出緩衝區中傳回的索引識別碼實際大小。</span><span class="sxs-lookup"><span data-stu-id="cf35d-113">This is the actual size of the index ID that is returned in the output buffer from [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

<span data-ttu-id="cf35d-114">**rgbIndexId**</span><span class="sxs-lookup"><span data-stu-id="cf35d-114">**rgbIndexId**</span></span>

<span data-ttu-id="cf35d-115">引擎用來快速識別其架構快取中索引的不透明資訊 BLOB。</span><span class="sxs-lookup"><span data-stu-id="cf35d-115">An opaque BLOB of information that is used by the engine to quickly identify an index in its schema cache.</span></span>

<span data-ttu-id="cf35d-116">請勿嘗試解讀資訊的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="cf35d-116">Do not attempt to interpret the BLOB of information.</span></span> <span data-ttu-id="cf35d-117">它不是設定的大小。</span><span class="sxs-lookup"><span data-stu-id="cf35d-117">It is not a set size.</span></span>

### <a name="requirements"></a><span data-ttu-id="cf35d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf35d-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf35d-119"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="cf35d-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cf35d-120">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="cf35d-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf35d-121"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="cf35d-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cf35d-122">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="cf35d-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf35d-123"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="cf35d-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cf35d-124">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="cf35d-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="cf35d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf35d-125">See Also</span></span>

[<span data-ttu-id="cf35d-126">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="cf35d-126">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="cf35d-127">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="cf35d-127">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="cf35d-128">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="cf35d-128">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="cf35d-129">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="cf35d-129">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
