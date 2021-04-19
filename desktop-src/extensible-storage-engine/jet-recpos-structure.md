---
description: 深入瞭解： JET_RECPOS 結構
title: JET_RECPOS 結構
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990344"
---
# <a name="jet_recpos-structure"></a><span data-ttu-id="29092-103">JET_RECPOS 結構</span><span class="sxs-lookup"><span data-stu-id="29092-103">JET_RECPOS Structure</span></span>


<span data-ttu-id="29092-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="29092-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recpos-structure"></a><span data-ttu-id="29092-105">JET_RECPOS 結構</span><span class="sxs-lookup"><span data-stu-id="29092-105">JET_RECPOS Structure</span></span>

<span data-ttu-id="29092-106">**JET_RECPOS** 結構包含整數的集合，代表索引中的小數位置。</span><span class="sxs-lookup"><span data-stu-id="29092-106">The **JET_RECPOS** structure contains a collection of integers that represent a fractional position within an index.</span></span> <span data-ttu-id="29092-107">**centriesLT** 是小於目前索引鍵的索引項目數目。</span><span class="sxs-lookup"><span data-stu-id="29092-107">**centriesLT** is the number of index entries less than the current index key.</span></span> <span data-ttu-id="29092-108">**centriesInRange** 是等於目前索引鍵的索引項目數目。</span><span class="sxs-lookup"><span data-stu-id="29092-108">**centriesInRange** is the number of index entries equal to the current key.</span></span> <span data-ttu-id="29092-109">**centriesInRange** 不受支援，而且一律會傳回為1。</span><span class="sxs-lookup"><span data-stu-id="29092-109">**centriesInRange** is not supported and is always returned as 1.</span></span> <span data-ttu-id="29092-110">**centriesTotal** 是索引中的索引項目數目。</span><span class="sxs-lookup"><span data-stu-id="29092-110">**centriesTotal** is the number of index entries in the index.</span></span> <span data-ttu-id="29092-111">所有值都是近似值，無法保證精確度。</span><span class="sxs-lookup"><span data-stu-id="29092-111">All values are approximations with no guarantee of accuracy.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a><span data-ttu-id="29092-112">成員</span><span class="sxs-lookup"><span data-stu-id="29092-112">Members</span></span>

<span data-ttu-id="29092-113">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="29092-113">**cbStruct**</span></span>

<span data-ttu-id="29092-114">[JET_RETINFO](./jet-retinfo-structure.md)結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="29092-114">The size of the [JET_RETINFO](./jet-retinfo-structure.md) structure, in bytes.</span></span> <span data-ttu-id="29092-115">此值會確認下欄欄位是否存在。</span><span class="sxs-lookup"><span data-stu-id="29092-115">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="29092-116">**centriesLT**</span><span class="sxs-lookup"><span data-stu-id="29092-116">**centriesLT**</span></span>

<span data-ttu-id="29092-117">索引項目的近似數目小於目前的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="29092-117">The approximate number of index entries less than the current key.</span></span>

<span data-ttu-id="29092-118">**centriesInRange**</span><span class="sxs-lookup"><span data-stu-id="29092-118">**centriesInRange**</span></span>

<span data-ttu-id="29092-119">索引項目目的大約數目等於目前的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="29092-119">The approximate number of index entries equal to the current key.</span></span> <span data-ttu-id="29092-120">無論實際等於目前索引鍵的索引項目數目為何，這個欄位一律會設定為1。</span><span class="sxs-lookup"><span data-stu-id="29092-120">This field is always set to 1, regardless of the number of index entries that are actually equal to the current key.</span></span>

<span data-ttu-id="29092-121">**centriesTotal**</span><span class="sxs-lookup"><span data-stu-id="29092-121">**centriesTotal**</span></span>

<span data-ttu-id="29092-122">索引中的大約專案數。</span><span class="sxs-lookup"><span data-stu-id="29092-122">The approximate number of entries in the index.</span></span>

### <a name="requirements"></a><span data-ttu-id="29092-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="29092-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29092-124"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="29092-124"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="29092-125">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="29092-125">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29092-126"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="29092-126"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="29092-127">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="29092-127">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29092-128"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="29092-128"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="29092-129">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="29092-129">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="29092-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29092-130">See Also</span></span>

[<span data-ttu-id="29092-131">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="29092-131">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="29092-132">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="29092-132">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)
