---
description: 已取代。 代表時間的瞬間，通常表示為一天的日期和時間，以及對應的行事曆。
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: CALDATETIME 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992520"
---
# <a name="caldatetime-structure"></a><span data-ttu-id="dc66d-104">CALDATETIME 結構</span><span class="sxs-lookup"><span data-stu-id="dc66d-104">CALDATETIME structure</span></span>

<span data-ttu-id="dc66d-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="dc66d-105">Deprecated.</span></span> <span data-ttu-id="dc66d-106">代表時間的瞬間，通常表示為一天的日期和時間，以及對應的行事曆。</span><span class="sxs-lookup"><span data-stu-id="dc66d-106">Represents an instant in time, typically expressed as a date and time of day and a corresponding calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc66d-107">語法</span><span class="sxs-lookup"><span data-stu-id="dc66d-107">Syntax</span></span>


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a><span data-ttu-id="dc66d-108">成員</span><span class="sxs-lookup"><span data-stu-id="dc66d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc66d-109">**CalId**</span><span class="sxs-lookup"><span data-stu-id="dc66d-109">**CalId**</span></span>
</dt> <dd>

<span data-ttu-id="dc66d-110">瞬間時間的行事 [曆識別碼](calendar-identifiers.md) 。</span><span class="sxs-lookup"><span data-stu-id="dc66d-110">The [calendar identifier](calendar-identifiers.md) for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="dc66d-111">**時代**</span><span class="sxs-lookup"><span data-stu-id="dc66d-111">**Era**</span></span>
</dt> <dd>

<span data-ttu-id="dc66d-112">瞬間的時代資訊。</span><span class="sxs-lookup"><span data-stu-id="dc66d-112">The era information for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="dc66d-113">**年**</span><span class="sxs-lookup"><span data-stu-id="dc66d-113">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="dc66d-114">瞬間的時間。</span><span class="sxs-lookup"><span data-stu-id="dc66d-114">The year for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="dc66d-115">**月**</span><span class="sxs-lookup"><span data-stu-id="dc66d-115">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="dc66d-116">瞬間的時間。</span><span class="sxs-lookup"><span data-stu-id="dc66d-116">The month for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="dc66d-117">**Day**</span><span class="sxs-lookup"><span data-stu-id="dc66d-117">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="dc66d-118">瞬間的當日時間。</span><span class="sxs-lookup"><span data-stu-id="dc66d-118">The day for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="dc66d-119">**DayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="dc66d-119">**DayOfWeek**</span></span>
</dt> <dd>

<span data-ttu-id="dc66d-120">一周中的某一天的當日時間。</span><span class="sxs-lookup"><span data-stu-id="dc66d-120">The day of the week for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="dc66d-121">**小時**</span><span class="sxs-lookup"><span data-stu-id="dc66d-121">**Hour**</span></span>
</dt> <dd>

<span data-ttu-id="dc66d-122">瞬間的時數。</span><span class="sxs-lookup"><span data-stu-id="dc66d-122">The hour for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="dc66d-123">**分鐘**</span><span class="sxs-lookup"><span data-stu-id="dc66d-123">**Minute**</span></span>
</dt> <dd>

<span data-ttu-id="dc66d-124">瞬間時間的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="dc66d-124">The minute for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="dc66d-125">**第二**</span><span class="sxs-lookup"><span data-stu-id="dc66d-125">**Second**</span></span>
</dt> <dd>

<span data-ttu-id="dc66d-126">時間瞬間的第二個。</span><span class="sxs-lookup"><span data-stu-id="dc66d-126">The second for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="dc66d-127">**蜱**</span><span class="sxs-lookup"><span data-stu-id="dc66d-127">**Tick**</span></span>
</dt> <dd>

<span data-ttu-id="dc66d-128">瞬間的時間刻度。</span><span class="sxs-lookup"><span data-stu-id="dc66d-128">The tick for the instant in time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc66d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc66d-129">Requirements</span></span>



| <span data-ttu-id="dc66d-130">需求</span><span class="sxs-lookup"><span data-stu-id="dc66d-130">Requirement</span></span> | <span data-ttu-id="dc66d-131">值</span><span class="sxs-lookup"><span data-stu-id="dc66d-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dc66d-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc66d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dc66d-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc66d-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dc66d-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc66d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dc66d-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc66d-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc66d-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc66d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc66d-137">國家語言支援結構</span><span class="sxs-lookup"><span data-stu-id="dc66d-137">National Language Support Structures</span></span>](national-language-support-structures.md)
</dt> </dl>

 

 




