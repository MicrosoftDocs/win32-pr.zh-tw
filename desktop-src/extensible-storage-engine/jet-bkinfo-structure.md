---
description: 深入瞭解： JET_BKINFO 結構
title: JET_BKINFO 結構
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194614"
---
# <a name="jet_bkinfo-structure"></a><span data-ttu-id="a2e1b-103">JET_BKINFO 結構</span><span class="sxs-lookup"><span data-stu-id="a2e1b-103">JET_BKINFO Structure</span></span>


<span data-ttu-id="a2e1b-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a2e1b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bkinfo-structure"></a><span data-ttu-id="a2e1b-105">JET_BKINFO 結構</span><span class="sxs-lookup"><span data-stu-id="a2e1b-105">JET_BKINFO Structure</span></span>

<span data-ttu-id="a2e1b-106">**JET_BKINFO** 結構會保存有關特定備份事件的資料集合。</span><span class="sxs-lookup"><span data-stu-id="a2e1b-106">The **JET_BKINFO** structure holds a collection of data about a specific backup event.</span></span>

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a><span data-ttu-id="a2e1b-107">成員</span><span class="sxs-lookup"><span data-stu-id="a2e1b-107">Members</span></span>

<span data-ttu-id="a2e1b-108">**lgposMark**</span><span class="sxs-lookup"><span data-stu-id="a2e1b-108">**lgposMark**</span></span>

<span data-ttu-id="a2e1b-109">此備份的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2e1b-109">The ID of this backup.</span></span>

<span data-ttu-id="a2e1b-110">**logtimeMark**</span><span class="sxs-lookup"><span data-stu-id="a2e1b-110">**logtimeMark**</span></span>

<span data-ttu-id="a2e1b-111">此備份事件的時間。</span><span class="sxs-lookup"><span data-stu-id="a2e1b-111">The time of this backup event.</span></span>

<span data-ttu-id="a2e1b-112">**bklogtimeMark**</span><span class="sxs-lookup"><span data-stu-id="a2e1b-112">**bklogtimeMark**</span></span>

<span data-ttu-id="a2e1b-113">此備份事件的時間，以及表示快照集備份的其他位。</span><span class="sxs-lookup"><span data-stu-id="a2e1b-113">The time of this backup event, with additional bits to indicate a snapshot backup.</span></span>

<span data-ttu-id="a2e1b-114">**Windows vista： bklogtimeMark** 是在 windows vista 中引進的。</span><span class="sxs-lookup"><span data-stu-id="a2e1b-114">**Windows Vista:  bklogtimeMark** is introduced in Windows Vista.</span></span>

<span data-ttu-id="a2e1b-115">**genLow**</span><span class="sxs-lookup"><span data-stu-id="a2e1b-115">**genLow**</span></span>

<span data-ttu-id="a2e1b-116">與此備份事件相關聯的低記錄產生編號。</span><span class="sxs-lookup"><span data-stu-id="a2e1b-116">The low log generation number associated with this backup event.</span></span>

<span data-ttu-id="a2e1b-117">**genHigh**</span><span class="sxs-lookup"><span data-stu-id="a2e1b-117">**genHigh**</span></span>

<span data-ttu-id="a2e1b-118">與此備份事件相關聯的高記錄產生編號。</span><span class="sxs-lookup"><span data-stu-id="a2e1b-118">The high log generation number associated with this backup event.</span></span>

### <a name="remarks"></a><span data-ttu-id="a2e1b-119">備註</span><span class="sxs-lookup"><span data-stu-id="a2e1b-119">Remarks</span></span>

<span data-ttu-id="a2e1b-120">此結構是在 [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) 結構內用來表示有關資料庫備份事件的資料。</span><span class="sxs-lookup"><span data-stu-id="a2e1b-120">This structure is used inside the [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) structure to represent data about the database backup event.</span></span>

### <a name="requirements"></a><span data-ttu-id="a2e1b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2e1b-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2e1b-122"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="a2e1b-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a2e1b-123">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="a2e1b-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2e1b-124"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="a2e1b-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a2e1b-125">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="a2e1b-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2e1b-126"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="a2e1b-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a2e1b-127">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="a2e1b-127">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="a2e1b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2e1b-128">See Also</span></span>

[<span data-ttu-id="a2e1b-129">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="a2e1b-129">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="a2e1b-130">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="a2e1b-130">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="a2e1b-131">JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="a2e1b-131">JET_BKLOGTIME</span></span>](./jet-bklogtime-structure.md)  
[<span data-ttu-id="a2e1b-132">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="a2e1b-132">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
