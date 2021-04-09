---
title: ScheduleByMonthDayOfWeek (calendarTriggerType) 元素
description: 指定每週的星期幾排程。
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- ScheduleByMonthDayOfWeek 元素工作排程器
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e92d6ad530466a2238c8239c9e262f85ae361d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686255"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a><span data-ttu-id="058d5-104">ScheduleByMonthDayOfWeek (calendarTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="058d5-104">ScheduleByMonthDayOfWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="058d5-105">指定每週的星期幾排程。</span><span class="sxs-lookup"><span data-stu-id="058d5-105">Specifies a monthly day-of-week schedule.</span></span> <span data-ttu-id="058d5-106">例如，工作會在一周的特定日子、每月的周數，以及當年的月份開始。</span><span class="sxs-lookup"><span data-stu-id="058d5-106">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span>

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

<span data-ttu-id="058d5-107">**ScheduleByMonthDayOfWeek** 元素是由 [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="058d5-107">The **ScheduleByMonthDayOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="058d5-108">父元素</span><span class="sxs-lookup"><span data-stu-id="058d5-108">Parent element</span></span>



| <span data-ttu-id="058d5-109">元素</span><span class="sxs-lookup"><span data-stu-id="058d5-109">Element</span></span>                                                                             | <span data-ttu-id="058d5-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="058d5-110">Derived from</span></span>                                                                       | <span data-ttu-id="058d5-111">Description</span><span class="sxs-lookup"><span data-stu-id="058d5-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="058d5-112">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="058d5-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="058d5-113">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="058d5-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="058d5-114">指定每日、每週、每月或每週 (DOW) 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="058d5-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="058d5-115">子元素</span><span class="sxs-lookup"><span data-stu-id="058d5-115">Child elements</span></span>



| <span data-ttu-id="058d5-116">元素</span><span class="sxs-lookup"><span data-stu-id="058d5-116">Element</span></span>                                                                                   | <span data-ttu-id="058d5-117">類型</span><span class="sxs-lookup"><span data-stu-id="058d5-117">Type</span></span>                                                                     | <span data-ttu-id="058d5-118">Description</span><span class="sxs-lookup"><span data-stu-id="058d5-118">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="058d5-119">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="058d5-119">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="058d5-120">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="058d5-120">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="058d5-121">指定工作執行的星期幾。</span><span class="sxs-lookup"><span data-stu-id="058d5-121">Specifies the days of the week in which the task runs.</span></span><br/>       |
| [<span data-ttu-id="058d5-122">**月**</span><span class="sxs-lookup"><span data-stu-id="058d5-122">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="058d5-123">**monthsType**</span><span class="sxs-lookup"><span data-stu-id="058d5-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="058d5-124">指定執行工作的年份月份。</span><span class="sxs-lookup"><span data-stu-id="058d5-124">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="058d5-125">**星期**</span><span class="sxs-lookup"><span data-stu-id="058d5-125">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | <span data-ttu-id="058d5-126">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="058d5-126">unsignedByte</span></span>                                                             | <span data-ttu-id="058d5-127">指定排程中周之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="058d5-127">Specifies the interval between the weeks in the schedule.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="058d5-128">備註</span><span class="sxs-lookup"><span data-stu-id="058d5-128">Remarks</span></span>

<span data-ttu-id="058d5-129">工作開始的當日時間是由 [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) 元素設定。</span><span class="sxs-lookup"><span data-stu-id="058d5-129">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="058d5-130">針對開發腳本，會使用 [**MonthlyDOWTrigger**](monthlydowtrigger.md) 物件來指定每月的每週工作日觸發程式。</span><span class="sxs-lookup"><span data-stu-id="058d5-130">For scripting development, a monthly day-of-week trigger is specified using the [**MonthlyDOWTrigger**](monthlydowtrigger.md) object.</span></span>

<span data-ttu-id="058d5-131">針對 c + + 開發，會使用 [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) 介面來指定每週的星期幾觸發程式。</span><span class="sxs-lookup"><span data-stu-id="058d5-131">For C++ development, a monthly day-of-week trigger is specified using the [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) interface.</span></span>

<span data-ttu-id="058d5-132">上方所列的子專案是由 [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) 複雜元素類型所定義。</span><span class="sxs-lookup"><span data-stu-id="058d5-132">The child elements listed above are defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="058d5-133">範例</span><span class="sxs-lookup"><span data-stu-id="058d5-133">Examples</span></span>

<span data-ttu-id="058d5-134">下列 XML 會定義每月星期幾行事曆觸發程式，此觸發程式會在一年的每個月的第一周星期一，于) 上午8:00 點開始工作 (。</span><span class="sxs-lookup"><span data-stu-id="058d5-134">The following XML defines a monthly day of week calendar trigger that starts a task ( at 8:00 AM) on Monday of the first week for each month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonthDayOfWeek>
        <Weeks>
            <Week>1</Week>
        </Weeks>
        <DaysOfWeek>
            <Monday/>
        </DaysOfWeek>
        <Months>
            <January/>
            <February/>
            <March/>
            <April/>
            <May/>
            <June/>
            <July/>
            <August/>
            <September/>
            <October/>
            <November/>
            <December/>
        <Months>
    </ScheduleByMonthDayOfWeek>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="058d5-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="058d5-135">Requirements</span></span>



| <span data-ttu-id="058d5-136">需求</span><span class="sxs-lookup"><span data-stu-id="058d5-136">Requirement</span></span> | <span data-ttu-id="058d5-137">值</span><span class="sxs-lookup"><span data-stu-id="058d5-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="058d5-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="058d5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="058d5-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="058d5-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="058d5-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="058d5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="058d5-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="058d5-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="058d5-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="058d5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="058d5-143">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="058d5-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="058d5-144">工作排程器</span><span class="sxs-lookup"><span data-stu-id="058d5-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





