---
description: 已取代。 指定用於調整 CALDATETIME 結構的日期單位。
ms.assetid: 20d0cd7a-6e6b-4c82-9cfa-e4f4315d6362
title: CALDATETIME_DATEUNIT 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME_DATEUNIT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6ce1f8929dd6e2f7de59d32d66229f73c062505c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972026"
---
# <a name="caldatetime_dateunit-enumeration"></a><span data-ttu-id="379cb-104">CALDATETIME \_ DATEUNIT 列舉</span><span class="sxs-lookup"><span data-stu-id="379cb-104">CALDATETIME\_DATEUNIT enumeration</span></span>

<span data-ttu-id="379cb-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="379cb-105">Deprecated.</span></span> <span data-ttu-id="379cb-106">指定用於調整 [**CALDATETIME**](caldatetime.md) 結構的日期單位。</span><span class="sxs-lookup"><span data-stu-id="379cb-106">Specifies the date units for adjusting the [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="379cb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="379cb-107">Syntax</span></span>


```C++
enum CALDATETIME_DATEUNIT {
  EraUnit, 
  YearUnit, 
  MonthUnit, 
  WeekUnit, 
  DayUnit, 
  HourUnit, 
  MinuteUnit, 
  SecondUnit, 
  TickUnit 

};
```



## <a name="constants"></a><span data-ttu-id="379cb-108">常數</span><span class="sxs-lookup"><span data-stu-id="379cb-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="379cb-109"><span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**EraUnit**</span><span class="sxs-lookup"><span data-stu-id="379cb-109"><span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**EraUnit**</span></span>
</dt> <dd>

<span data-ttu-id="379cb-110">紀元日期時間單位。</span><span class="sxs-lookup"><span data-stu-id="379cb-110">The era date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="379cb-111"><span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**YearUnit**</span><span class="sxs-lookup"><span data-stu-id="379cb-111"><span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**YearUnit**</span></span>
</dt> <dd>

<span data-ttu-id="379cb-112">年份日期時間單位。</span><span class="sxs-lookup"><span data-stu-id="379cb-112">The year date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="379cb-113"><span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**MonthUnit**</span><span class="sxs-lookup"><span data-stu-id="379cb-113"><span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**MonthUnit**</span></span>
</dt> <dd>

<span data-ttu-id="379cb-114">月份日期時間單位。</span><span class="sxs-lookup"><span data-stu-id="379cb-114">The month date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="379cb-115"><span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**WeekUnit**</span><span class="sxs-lookup"><span data-stu-id="379cb-115"><span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**WeekUnit**</span></span>
</dt> <dd>

<span data-ttu-id="379cb-116">周日期時間單位。</span><span class="sxs-lookup"><span data-stu-id="379cb-116">The week date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="379cb-117"><span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**DayUnit**</span><span class="sxs-lookup"><span data-stu-id="379cb-117"><span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**DayUnit**</span></span>
</dt> <dd>

<span data-ttu-id="379cb-118">日期日期時間單位。</span><span class="sxs-lookup"><span data-stu-id="379cb-118">The day date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="379cb-119"><span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**HourUnit**</span><span class="sxs-lookup"><span data-stu-id="379cb-119"><span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**HourUnit**</span></span>
</dt> <dd>

<span data-ttu-id="379cb-120">小時的日期時間單位。</span><span class="sxs-lookup"><span data-stu-id="379cb-120">The hour date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="379cb-121"><span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**MinuteUnit**</span><span class="sxs-lookup"><span data-stu-id="379cb-121"><span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**MinuteUnit**</span></span>
</dt> <dd>

<span data-ttu-id="379cb-122">分鐘的日期時間單位。</span><span class="sxs-lookup"><span data-stu-id="379cb-122">The minute date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="379cb-123"><span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**SecondUnit**</span><span class="sxs-lookup"><span data-stu-id="379cb-123"><span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**SecondUnit**</span></span>
</dt> <dd>

<span data-ttu-id="379cb-124">第二個日期時間單位。</span><span class="sxs-lookup"><span data-stu-id="379cb-124">The second date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="379cb-125"><span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**TickUnit**</span><span class="sxs-lookup"><span data-stu-id="379cb-125"><span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**TickUnit**</span></span>
</dt> <dd>

<span data-ttu-id="379cb-126">刻度日期時間單位。</span><span class="sxs-lookup"><span data-stu-id="379cb-126">The tick date time unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="379cb-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="379cb-127">Requirements</span></span>



| <span data-ttu-id="379cb-128">需求</span><span class="sxs-lookup"><span data-stu-id="379cb-128">Requirement</span></span> | <span data-ttu-id="379cb-129">值</span><span class="sxs-lookup"><span data-stu-id="379cb-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="379cb-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="379cb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="379cb-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="379cb-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="379cb-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="379cb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="379cb-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="379cb-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="379cb-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="379cb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="379cb-135">國家語言支援列舉類型</span><span class="sxs-lookup"><span data-stu-id="379cb-135">National Language Support Enumeration Types</span></span>](national-language-support-enumeration-types.md)
</dt> </dl>

 

 




