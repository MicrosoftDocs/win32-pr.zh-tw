---
description: 深入瞭解： JET_BKLOGTIME 結構
title: JET_BKLOGTIME 結構
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: 0b3ebfd1c0b807a491695ba18d6735e0230a16fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975844"
---
# <a name="jet_bklogtime-structure"></a><span data-ttu-id="f32c4-103">JET_BKLOGTIME 結構</span><span class="sxs-lookup"><span data-stu-id="f32c4-103">JET_BKLOGTIME Structure</span></span>


<span data-ttu-id="f32c4-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f32c4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bklogtime-structure"></a><span data-ttu-id="f32c4-105">JET_BKLOGTIME 結構</span><span class="sxs-lookup"><span data-stu-id="f32c4-105">JET_BKLOGTIME Structure</span></span>

<span data-ttu-id="f32c4-106">**JET_BKLOGTIME** 結構會保存事件的日期和時間元素。</span><span class="sxs-lookup"><span data-stu-id="f32c4-106">The **JET_BKLOGTIME** structure holds the date and time elements of an event.</span></span> <span data-ttu-id="f32c4-107">它是 [JET_LOGTIME](./jet-logtime-structure.md)的延伸。</span><span class="sxs-lookup"><span data-stu-id="f32c4-107">It is an extension of [JET_LOGTIME](./jet-logtime-structure.md).</span></span>

<span data-ttu-id="f32c4-108">**Windows vista： JET_BKLOGTIME** 是在 windows vista 中引進。</span><span class="sxs-lookup"><span data-stu-id="f32c4-108">**Windows Vista:  JET_BKLOGTIME** is introduced in Windows Vista.</span></span>

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a><span data-ttu-id="f32c4-109">成員</span><span class="sxs-lookup"><span data-stu-id="f32c4-109">Members</span></span>

<span data-ttu-id="f32c4-110">**bSeconds**</span><span class="sxs-lookup"><span data-stu-id="f32c4-110">**bSeconds**</span></span>

<span data-ttu-id="f32c4-111">事件的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f32c4-111">The time of the event in seconds.</span></span> <span data-ttu-id="f32c4-112">這可以是 0 (零) 至60。</span><span class="sxs-lookup"><span data-stu-id="f32c4-112">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="f32c4-113">當 **JET_BKLOGTIME** 結構為 "null" 時，會使用 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f32c4-113">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="f32c4-114">**bMinutes**</span><span class="sxs-lookup"><span data-stu-id="f32c4-114">**bMinutes**</span></span>

<span data-ttu-id="f32c4-115">事件的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="f32c4-115">The time of the event in minutes.</span></span> <span data-ttu-id="f32c4-116">這可以是 0 (零) 至60。</span><span class="sxs-lookup"><span data-stu-id="f32c4-116">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="f32c4-117">當 **JET_BKLOGTIME** 結構為 "null" 時，會使用 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f32c4-117">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="f32c4-118">**bHours**</span><span class="sxs-lookup"><span data-stu-id="f32c4-118">**bHours**</span></span>

<span data-ttu-id="f32c4-119">事件的時間（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="f32c4-119">The time of the event in hours.</span></span> <span data-ttu-id="f32c4-120">這可以是 0 (零) 到24。</span><span class="sxs-lookup"><span data-stu-id="f32c4-120">This can be 0 (zero) to 24.</span></span> <span data-ttu-id="f32c4-121">當 **JET_BKLOGTIME** 結構為 "null" 時，會使用 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f32c4-121">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="f32c4-122">**bDay**</span><span class="sxs-lookup"><span data-stu-id="f32c4-122">**bDay**</span></span>

<span data-ttu-id="f32c4-123">事件月份的日期。</span><span class="sxs-lookup"><span data-stu-id="f32c4-123">The day of the month of the event.</span></span> <span data-ttu-id="f32c4-124">這可以是 0 (零) 到31。</span><span class="sxs-lookup"><span data-stu-id="f32c4-124">This can be 0 (zero) to 31.</span></span> <span data-ttu-id="f32c4-125">當 **JET_BKLOGTIME** 結構為 "null" 時，會使用 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f32c4-125">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="f32c4-126">**bMonth**</span><span class="sxs-lookup"><span data-stu-id="f32c4-126">**bMonth**</span></span>

<span data-ttu-id="f32c4-127">活動年度的月份。</span><span class="sxs-lookup"><span data-stu-id="f32c4-127">The month of the year of the event.</span></span> <span data-ttu-id="f32c4-128">這可以是 0 (零) 到12。</span><span class="sxs-lookup"><span data-stu-id="f32c4-128">This can be 0 (zero) to 12.</span></span> <span data-ttu-id="f32c4-129">當 **JET_BKLOGTIME** 結構為 "null" 時，會使用 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f32c4-129">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="f32c4-130">**bYear**</span><span class="sxs-lookup"><span data-stu-id="f32c4-130">**bYear**</span></span>

<span data-ttu-id="f32c4-131">年份 (事件的 1900) 位移。</span><span class="sxs-lookup"><span data-stu-id="f32c4-131">The year (offset by 1900) of the event.</span></span> <span data-ttu-id="f32c4-132">若要達到實際年份，請將1900新增至此值。</span><span class="sxs-lookup"><span data-stu-id="f32c4-132">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="f32c4-133">當 **JET_BKLOGTIME** 結構為 "null" 時，會使用 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f32c4-133">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="f32c4-134">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="f32c4-134">**bFiller1**</span></span>

<span data-ttu-id="f32c4-135">應忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="f32c4-135">This field should be ignored.</span></span>

<span data-ttu-id="f32c4-136">**fTimeIsUTC**</span><span class="sxs-lookup"><span data-stu-id="f32c4-136">**fTimeIsUTC**</span></span>

<span data-ttu-id="f32c4-137">時間是採用 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="f32c4-137">The time is in UTC format.</span></span>

<span data-ttu-id="f32c4-138">**fUnused**</span><span class="sxs-lookup"><span data-stu-id="f32c4-138">**fUnused**</span></span>

<span data-ttu-id="f32c4-139">應忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="f32c4-139">This field should be ignored.</span></span>

<span data-ttu-id="f32c4-140">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="f32c4-140">**bFiller2**</span></span>

<span data-ttu-id="f32c4-141">應忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="f32c4-141">This field should be ignored.</span></span>

<span data-ttu-id="f32c4-142">**fOSSnapshot**</span><span class="sxs-lookup"><span data-stu-id="f32c4-142">**fOSSnapshot**</span></span>

<span data-ttu-id="f32c4-143">如果此事件是備份，此旗標會包含下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="f32c4-143">If this event is a backup, this flag contains one of the following possible values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f32c4-144">Name</span><span class="sxs-lookup"><span data-stu-id="f32c4-144">Name</span></span></p></th>
<th><p><span data-ttu-id="f32c4-145">值</span><span class="sxs-lookup"><span data-stu-id="f32c4-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f32c4-146">串流備份</span><span class="sxs-lookup"><span data-stu-id="f32c4-146">streaming backup</span></span></p></td>
<td><p><span data-ttu-id="f32c4-147">0 (零)</span><span class="sxs-lookup"><span data-stu-id="f32c4-147">0 (zero)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f32c4-148">快照集備份</span><span class="sxs-lookup"><span data-stu-id="f32c4-148">snapshot backup</span></span></p></td>
<td><p><span data-ttu-id="f32c4-149">1</span><span class="sxs-lookup"><span data-stu-id="f32c4-149">1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f32c4-150">**fReserved**</span><span class="sxs-lookup"><span data-stu-id="f32c4-150">**fReserved**</span></span>

<span data-ttu-id="f32c4-151">應忽略此欄位。</span><span class="sxs-lookup"><span data-stu-id="f32c4-151">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="f32c4-152">備註</span><span class="sxs-lookup"><span data-stu-id="f32c4-152">Remarks</span></span>

<span data-ttu-id="f32c4-153">此結構會在進行偵錯工具時使用。</span><span class="sxs-lookup"><span data-stu-id="f32c4-153">This structure is used when debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="f32c4-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="f32c4-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f32c4-155"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="f32c4-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f32c4-156">需要 Windows Vista。</span><span class="sxs-lookup"><span data-stu-id="f32c4-156">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f32c4-157"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="f32c4-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f32c4-158">需要 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="f32c4-158">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f32c4-159"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="f32c4-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f32c4-160">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="f32c4-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f32c4-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f32c4-161">See Also</span></span>

[<span data-ttu-id="f32c4-162">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="f32c4-162">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="f32c4-163">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="f32c4-163">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
