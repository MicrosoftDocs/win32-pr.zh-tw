---
description: 深入瞭解： JET_SETINFO 結構
title: JET_SETINFO 結構
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 69602aad89142d9f5dc202074ca54cf278767892
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104514737"
---
# <a name="jet_setinfo-structure"></a><span data-ttu-id="0466e-103">JET_SETINFO 結構</span><span class="sxs-lookup"><span data-stu-id="0466e-103">JET_SETINFO Structure</span></span>


<span data-ttu-id="0466e-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0466e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setinfo-structure"></a><span data-ttu-id="0466e-105">JET_SETINFO 結構</span><span class="sxs-lookup"><span data-stu-id="0466e-105">JET_SETINFO Structure</span></span>

<span data-ttu-id="0466e-106">**JET_SETINFO** 結構包含 [JetSetColumn](./jetsetcolumn-function.md)的選擇性輸入參數。</span><span class="sxs-lookup"><span data-stu-id="0466e-106">The **JET_SETINFO** structure contains optional input parameters for [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="0466e-107">如果要傳遞此結構的指標，則可以傳遞 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="0466e-107">A **NULL** pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="0466e-108">傳遞 **Null** 的意義等同于傳遞 **JET_SETINFO** ，並將 **cbStruct** 設定為 Sizeof (JET_SETINFO) ，將 **ibLongValue** 設定為 0 (零) ， **itagSequence** 設定為1。</span><span class="sxs-lookup"><span data-stu-id="0466e-108">The meaning of passing a **NULL** is the same as passing **JET_SETINFO** with **cbStruct** set to sizeof(JET_SETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a><span data-ttu-id="0466e-109">成員</span><span class="sxs-lookup"><span data-stu-id="0466e-109">Members</span></span>

<span data-ttu-id="0466e-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="0466e-110">**cbStruct**</span></span>

<span data-ttu-id="0466e-111">**JET_SETINFO** 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0466e-111">The size, in bytes, of the **JET_SETINFO**.</span></span> <span data-ttu-id="0466e-112">此值會確認下欄欄位是否存在。</span><span class="sxs-lookup"><span data-stu-id="0466e-112">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="0466e-113">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="0466e-113">**ibLongValue**</span></span>

<span data-ttu-id="0466e-114">要在類型 [JET_coltypLongBinary](./jet-coltyp.md) 或 [JET_coltypLongText](./jet-coltyp.md)的資料行中設定之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="0466e-114">The offset to the first byte to be set in a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="0466e-115">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="0466e-115">**itagSequence**</span></span>

<span data-ttu-id="0466e-116">描述要設定之多重值資料行中的值順序。</span><span class="sxs-lookup"><span data-stu-id="0466e-116">Describes the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="0466e-117">值的陣列是以一為基礎。</span><span class="sxs-lookup"><span data-stu-id="0466e-117">The array of values is one-based.</span></span> <span data-ttu-id="0466e-118">第一個值是 sequence 1，而不是 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="0466e-118">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="0466e-119">如果 [記錄] 資料行只有一個值，則如果要取代該值，則應將1當作 **itagSequence** 傳遞。</span><span class="sxs-lookup"><span data-stu-id="0466e-119">If the record column has only one value then 1 should be passed as the **itagSequence** if that value is being replaced.</span></span> <span data-ttu-id="0466e-120">值為 0 (零) 表示將新的資料行值實例加入至資料行值序列的結尾。</span><span class="sxs-lookup"><span data-stu-id="0466e-120">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="0466e-121">使用可包含多個值的資料行時，您只能在 [JetSetColumn](./jetsetcolumn-function.md) 和 [JetRetrieveColumn](./jetretrievecolumn-function.md) 中使用大於1的序號，或使用 [JetSetColumn](./jetsetcolumn-function.md)中的0。</span><span class="sxs-lookup"><span data-stu-id="0466e-121">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="0466e-122">在目前的引擎執行中，使用 JET_bitColumnTagged 建立的任何資料行都可以包含多個值。</span><span class="sxs-lookup"><span data-stu-id="0466e-122">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="0466e-123">使用 JET_bitColumnMultiValued 所建立的資料行，與多值標記的資料行的索引編制方式不同。</span><span class="sxs-lookup"><span data-stu-id="0466e-123">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="0466e-124">如需詳細資訊，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 。</span><span class="sxs-lookup"><span data-stu-id="0466e-124">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

### <a name="requirements"></a><span data-ttu-id="0466e-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0466e-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0466e-126"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="0466e-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0466e-127">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="0466e-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0466e-128"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="0466e-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0466e-129">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="0466e-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0466e-130"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="0466e-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0466e-131">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="0466e-131">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0466e-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0466e-132">See Also</span></span>

[<span data-ttu-id="0466e-133">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="0466e-133">JetSetColumn</span></span>](./jetsetcolumn-function.md)
