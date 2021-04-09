---
description: 深入瞭解： JET_LOGTIME 結構
title: JET_LOGTIME 結構
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
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
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103696895"
---
# <a name="jet_logtime-structure"></a><span data-ttu-id="3c703-103">JET_LOGTIME 結構</span><span class="sxs-lookup"><span data-stu-id="3c703-103">JET_LOGTIME Structure</span></span>


<span data-ttu-id="3c703-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3c703-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_logtime-structure"></a><span data-ttu-id="3c703-105">JET_LOGTIME 結構</span><span class="sxs-lookup"><span data-stu-id="3c703-105">JET_LOGTIME Structure</span></span>

<span data-ttu-id="3c703-106">**JET_LOGTIME** 結構會保存事件日期和時間的元素。</span><span class="sxs-lookup"><span data-stu-id="3c703-106">The **JET_LOGTIME** structure holds elements of the date and time of an event.</span></span>

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a><span data-ttu-id="3c703-107">成員</span><span class="sxs-lookup"><span data-stu-id="3c703-107">Members</span></span>

<span data-ttu-id="3c703-108">**bSeconds**</span><span class="sxs-lookup"><span data-stu-id="3c703-108">**bSeconds**</span></span>

<span data-ttu-id="3c703-109">事件的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3c703-109">The time of the event in seconds.</span></span> <span data-ttu-id="3c703-110">這個值可以是0到59。</span><span class="sxs-lookup"><span data-stu-id="3c703-110">This value can be 0 to 59.</span></span> <span data-ttu-id="3c703-111">當結構為 null 時，就會使用0。</span><span class="sxs-lookup"><span data-stu-id="3c703-111">0 is used when the structure is null.</span></span>

<span data-ttu-id="3c703-112">**bMinutes**</span><span class="sxs-lookup"><span data-stu-id="3c703-112">**bMinutes**</span></span>

<span data-ttu-id="3c703-113">事件的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="3c703-113">The time of the event in minutes.</span></span> <span data-ttu-id="3c703-114">這個值可以是0到59。</span><span class="sxs-lookup"><span data-stu-id="3c703-114">This value can be 0 to 59.</span></span> <span data-ttu-id="3c703-115">當結構為 null 時，就會使用0。</span><span class="sxs-lookup"><span data-stu-id="3c703-115">0 is used when the structure is null.</span></span>

<span data-ttu-id="3c703-116">**bHours**</span><span class="sxs-lookup"><span data-stu-id="3c703-116">**bHours**</span></span>

<span data-ttu-id="3c703-117">事件的時間（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="3c703-117">The time of the event in hours.</span></span> <span data-ttu-id="3c703-118">這個值可以是0到23。</span><span class="sxs-lookup"><span data-stu-id="3c703-118">This value can be 0 to 23.</span></span> <span data-ttu-id="3c703-119">當結構為 null 時，就會使用0。</span><span class="sxs-lookup"><span data-stu-id="3c703-119">0 is used when the structure is null.</span></span>

<span data-ttu-id="3c703-120">**bDay**</span><span class="sxs-lookup"><span data-stu-id="3c703-120">**bDay**</span></span>

<span data-ttu-id="3c703-121">事件月份的日期。</span><span class="sxs-lookup"><span data-stu-id="3c703-121">The day of the month of the event.</span></span> <span data-ttu-id="3c703-122">這個值可以是0到31。</span><span class="sxs-lookup"><span data-stu-id="3c703-122">This value can be 0 to 31.</span></span> <span data-ttu-id="3c703-123">當結構為 null 時，就會使用0。</span><span class="sxs-lookup"><span data-stu-id="3c703-123">0 is used when the structure is null.</span></span>

<span data-ttu-id="3c703-124">**bMonth**</span><span class="sxs-lookup"><span data-stu-id="3c703-124">**bMonth**</span></span>

<span data-ttu-id="3c703-125">活動年度的月份。</span><span class="sxs-lookup"><span data-stu-id="3c703-125">The month of the year of the event.</span></span> <span data-ttu-id="3c703-126">這個值可以是0到12。</span><span class="sxs-lookup"><span data-stu-id="3c703-126">This value can be 0 to 12.</span></span> <span data-ttu-id="3c703-127">當結構為 null 時，就會使用0。</span><span class="sxs-lookup"><span data-stu-id="3c703-127">0 is used when the structure is null.</span></span>

<span data-ttu-id="3c703-128">**bYear**</span><span class="sxs-lookup"><span data-stu-id="3c703-128">**bYear**</span></span>

<span data-ttu-id="3c703-129">事件的年份 (以 1900) 位移。</span><span class="sxs-lookup"><span data-stu-id="3c703-129">The year of the event (offset by 1900).</span></span> <span data-ttu-id="3c703-130">若要達到實際年份，請將1900新增至此值。</span><span class="sxs-lookup"><span data-stu-id="3c703-130">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="3c703-131">當結構為 null 時，就會使用0。</span><span class="sxs-lookup"><span data-stu-id="3c703-131">0 is used when the structure is null.</span></span>

<span data-ttu-id="3c703-132">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="3c703-132">**bFiller1**</span></span>

<span data-ttu-id="3c703-133">應忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="3c703-133">This field should be ignored.</span></span>

<span data-ttu-id="3c703-134">**fTimeIsUTC**</span><span class="sxs-lookup"><span data-stu-id="3c703-134">**fTimeIsUTC**</span></span>

<span data-ttu-id="3c703-135">時間是採用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="3c703-135">The time is in UTC format.</span></span>

<span data-ttu-id="3c703-136">**fUnused**</span><span class="sxs-lookup"><span data-stu-id="3c703-136">**fUnused**</span></span>

<span data-ttu-id="3c703-137">應忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="3c703-137">This field should be ignored.</span></span>

<span data-ttu-id="3c703-138">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="3c703-138">**bFiller2**</span></span>

<span data-ttu-id="3c703-139">應忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="3c703-139">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="3c703-140">備註</span><span class="sxs-lookup"><span data-stu-id="3c703-140">Remarks</span></span>

<span data-ttu-id="3c703-141">此結構主要是用於偵錯工具中的使用方式。</span><span class="sxs-lookup"><span data-stu-id="3c703-141">This structure is meant primarily for usage in debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="3c703-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c703-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c703-143"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="3c703-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3c703-144">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="3c703-144">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c703-145"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="3c703-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3c703-146">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="3c703-146">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c703-147"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="3c703-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3c703-148">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="3c703-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3c703-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c703-149">See Also</span></span>

[<span data-ttu-id="3c703-150">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="3c703-150">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
