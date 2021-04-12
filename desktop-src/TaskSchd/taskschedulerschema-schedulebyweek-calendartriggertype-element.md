---
title: ScheduleByWeek (calendarTriggerType) 元素
description: 指定每週排程。
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- 每週觸發程式工作排程器、XML 元素
- ScheduleByWeek 元素工作排程器
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385182"
---
# <a name="schedulebyweek-calendartriggertype-element"></a><span data-ttu-id="626d4-105">ScheduleByWeek (calendarTriggerType) 元素</span><span class="sxs-lookup"><span data-stu-id="626d4-105">ScheduleByWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="626d4-106">指定每週排程。</span><span class="sxs-lookup"><span data-stu-id="626d4-106">Specifies a weekly schedule.</span></span> <span data-ttu-id="626d4-107">例如，工作會在每週的特定一天或每隔一周的特定一天，于上午8:00 開始。</span><span class="sxs-lookup"><span data-stu-id="626d4-107">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span>

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

<span data-ttu-id="626d4-108">**ScheduleByWeek** 元素是由 [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="626d4-108">The **ScheduleByWeek** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="626d4-109">父元素</span><span class="sxs-lookup"><span data-stu-id="626d4-109">Parent element</span></span>



| <span data-ttu-id="626d4-110">元素</span><span class="sxs-lookup"><span data-stu-id="626d4-110">Element</span></span>                                                                             | <span data-ttu-id="626d4-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="626d4-111">Derived from</span></span>                                                                       | <span data-ttu-id="626d4-112">Description</span><span class="sxs-lookup"><span data-stu-id="626d4-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="626d4-113">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="626d4-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="626d4-114">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="626d4-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="626d4-115">指定每日、每週、每月或每週 (DOW) 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="626d4-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="626d4-116">子元素</span><span class="sxs-lookup"><span data-stu-id="626d4-116">Child elements</span></span>



| <span data-ttu-id="626d4-117">元素</span><span class="sxs-lookup"><span data-stu-id="626d4-117">Element</span></span>                                                                               | <span data-ttu-id="626d4-118">類型</span><span class="sxs-lookup"><span data-stu-id="626d4-118">Type</span></span>                                                                     | <span data-ttu-id="626d4-119">Description</span><span class="sxs-lookup"><span data-stu-id="626d4-119">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="626d4-120">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="626d4-120">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="626d4-121">**daysOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="626d4-121">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="626d4-122">指定工作執行的星期幾。</span><span class="sxs-lookup"><span data-stu-id="626d4-122">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="626d4-123">**WeeksInterval**</span><span class="sxs-lookup"><span data-stu-id="626d4-123">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | <span data-ttu-id="626d4-124">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="626d4-124">unsignedByte</span></span>                                                             | <span data-ttu-id="626d4-125">指定排程中周之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="626d4-125">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="626d4-126">備註</span><span class="sxs-lookup"><span data-stu-id="626d4-126">Remarks</span></span>

<span data-ttu-id="626d4-127">上方所列的子專案是由 [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) 複雜元素類型所定義。</span><span class="sxs-lookup"><span data-stu-id="626d4-127">The child elements listed above are defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="626d4-128">工作開始的當日時間是由 [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) 元素設定。</span><span class="sxs-lookup"><span data-stu-id="626d4-128">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="626d4-129">針對開發腳本，會使用 [**WeeklyTrigger**](weeklytrigger.md) 物件指定每週觸發程式。</span><span class="sxs-lookup"><span data-stu-id="626d4-129">For scripting development, a weekly trigger is specified using the [**WeeklyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="626d4-130">針對 c + + 開發，每週觸發程式都是使用 [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) 介面指定。</span><span class="sxs-lookup"><span data-stu-id="626d4-130">For C++ development, a weekly trigger is specified using the [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="626d4-131">範例</span><span class="sxs-lookup"><span data-stu-id="626d4-131">Examples</span></span>

<span data-ttu-id="626d4-132">下列 XML 定義每週的行事曆觸發程式，從星期一到星期五的上午 8:00 (開始工作) 。</span><span class="sxs-lookup"><span data-stu-id="626d4-132">The following XML defines a weekly calendar trigger that starts a task Monday through Friday (at 8:00 AM) every week.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="626d4-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="626d4-133">Requirements</span></span>



| <span data-ttu-id="626d4-134">需求</span><span class="sxs-lookup"><span data-stu-id="626d4-134">Requirement</span></span> | <span data-ttu-id="626d4-135">值</span><span class="sxs-lookup"><span data-stu-id="626d4-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="626d4-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="626d4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="626d4-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="626d4-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="626d4-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="626d4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="626d4-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="626d4-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="626d4-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="626d4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="626d4-141">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="626d4-141">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="626d4-142">工作排程器</span><span class="sxs-lookup"><span data-stu-id="626d4-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





