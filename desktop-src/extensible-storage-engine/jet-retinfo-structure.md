---
description: 深入瞭解： JET_RETINFO 結構
title: JET_RETINFO 結構
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: 3452c4fab7155ea33b556ac7aa2c777b11a3f954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848215"
---
# <a name="jet_retinfo-structure"></a><span data-ttu-id="42cbf-103">JET_RETINFO 結構</span><span class="sxs-lookup"><span data-stu-id="42cbf-103">JET_RETINFO Structure</span></span>


<span data-ttu-id="42cbf-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="42cbf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retinfo-structure"></a><span data-ttu-id="42cbf-105">JET_RETINFO 結構</span><span class="sxs-lookup"><span data-stu-id="42cbf-105">JET_RETINFO Structure</span></span>

<span data-ttu-id="42cbf-106">**JET_RETINFO** 結構包含 [JetRetrieveColumn](./jetretrievecolumn-function.md)的選擇性輸入和輸出參數。</span><span class="sxs-lookup"><span data-stu-id="42cbf-106">The **JET_RETINFO** structure contains optional input and output parameters for [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span> <span data-ttu-id="42cbf-107">如果要傳遞此結構的指標，則可以傳遞 null 指標。</span><span class="sxs-lookup"><span data-stu-id="42cbf-107">A null pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="42cbf-108">傳遞 null **指標和傳遞** **JET_RETINFO** 設定為 sizeof (JET_RETINFO) ， **ibLongValue** 設定為 0 (零) ， **itagSequence** 設定為1。</span><span class="sxs-lookup"><span data-stu-id="42cbf-108">Passing a null pointer is the same as passing **JET_RETINFO** with **cbStruct** set to sizeof(JET_RETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a><span data-ttu-id="42cbf-109">成員</span><span class="sxs-lookup"><span data-stu-id="42cbf-109">Members</span></span>

<span data-ttu-id="42cbf-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="42cbf-110">**cbStruct**</span></span>

<span data-ttu-id="42cbf-111">必須設定為 **JET_RETINFO** 結構的大小（以位元組為單位），而且可以用來確認下欄欄位是否存在。</span><span class="sxs-lookup"><span data-stu-id="42cbf-111">Must be set to the size of the **JET_RETINFO** structure, in bytes, and serves to confirm the presence of the following fields.</span></span>

<span data-ttu-id="42cbf-112">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="42cbf-112">**ibLongValue**</span></span>

<span data-ttu-id="42cbf-113">從 [JET_coltypLongBinary](./jet-coltyp.md)或 [JET_coltypLongText](./jet-coltyp.md)類型的資料行抓取的第一個位元組位移。</span><span class="sxs-lookup"><span data-stu-id="42cbf-113">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span> <span data-ttu-id="42cbf-114">請注意，從這個位移取出的資料量是輸出緩衝區大小的下限，以及此位移之後的實際值中的資料大小。</span><span class="sxs-lookup"><span data-stu-id="42cbf-114">Note that the amount of data retrieved from this offset is the lower of the size of the output buffer and the size of data in the actual value after this offset.</span></span>

<span data-ttu-id="42cbf-115">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="42cbf-115">**itagSequence**</span></span>

<span data-ttu-id="42cbf-116">描述多重值資料行中值的序號。</span><span class="sxs-lookup"><span data-stu-id="42cbf-116">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="42cbf-117">請注意，值的陣列是以一為基礎。</span><span class="sxs-lookup"><span data-stu-id="42cbf-117">Note that the array of values is one-based.</span></span> <span data-ttu-id="42cbf-118">第一個值是 sequence 1，不是0。</span><span class="sxs-lookup"><span data-stu-id="42cbf-118">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="42cbf-119">如果 [記錄] 資料行只有一個值，則應將1傳遞為 **itagSequence**</span><span class="sxs-lookup"><span data-stu-id="42cbf-119">If the record column has only one value then 1 should be passed as the **itagSequence**</span></span>

<span data-ttu-id="42cbf-120">使用可包含多個值的資料行時，您只能在 [JetSetColumn](./jetsetcolumn-function.md) 和 [JetRetrieveColumn](./jetretrievecolumn-function.md) 中使用大於1的序號，或使用 [JetSetColumn](./jetsetcolumn-function.md)中的0。</span><span class="sxs-lookup"><span data-stu-id="42cbf-120">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="42cbf-121">在目前的引擎執行中，使用 JET_bitColumnTagged 建立的任何資料行都可以包含多個值。</span><span class="sxs-lookup"><span data-stu-id="42cbf-121">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="42cbf-122">使用 JET_bitColumnMultiValued 所建立的資料行，與多值標記的資料行的索引編制方式不同。</span><span class="sxs-lookup"><span data-stu-id="42cbf-122">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="42cbf-123">如需詳細資訊，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 。</span><span class="sxs-lookup"><span data-stu-id="42cbf-123">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

<span data-ttu-id="42cbf-124">**columnidNextTagged**</span><span class="sxs-lookup"><span data-stu-id="42cbf-124">**columnidNextTagged**</span></span>

<span data-ttu-id="42cbf-125">藉由將0傳遞為 [JetRetrieveColumn](./jetretrievecolumn-function.md)的 columnid，來抓取所有標記的資料行時，傳回已標記、多重值或稀疏資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="42cbf-125">Returns the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="42cbf-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="42cbf-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42cbf-127"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="42cbf-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="42cbf-128">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="42cbf-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42cbf-129"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="42cbf-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="42cbf-130">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="42cbf-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42cbf-131"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="42cbf-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="42cbf-132">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="42cbf-132">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="42cbf-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42cbf-133">See Also</span></span>

[<span data-ttu-id="42cbf-134">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="42cbf-134">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="42cbf-135">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="42cbf-135">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="42cbf-136">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="42cbf-136">JET_RETINFO</span></span>]()  
[<span data-ttu-id="42cbf-137">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="42cbf-137">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)
