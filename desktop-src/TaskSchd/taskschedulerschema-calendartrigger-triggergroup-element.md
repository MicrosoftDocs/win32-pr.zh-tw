---
title: CalendarTrigger (triggerGroup) 元素
description: 指定每日、每週、每月或每週 (DOW) 觸發程式。
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- 行事曆觸發程式工作排程器、XML 元素
- CalendarTrigger 元素工作排程器
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02c061d8821dffa82eca8756ab26acadc6bb9281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968366"
---
# <a name="calendartrigger-triggergroup-element"></a><span data-ttu-id="dd4c2-105">CalendarTrigger (triggerGroup) 元素</span><span class="sxs-lookup"><span data-stu-id="dd4c2-105">CalendarTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="dd4c2-106">指定每日、每週、每月或每週 (DOW) 觸發程式。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-106">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span>

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

<span data-ttu-id="dd4c2-107">**CalendarTrigger** 元素是由 [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-107">The **CalendarTrigger** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dd4c2-108">父元素</span><span class="sxs-lookup"><span data-stu-id="dd4c2-108">Parent element</span></span>



| <span data-ttu-id="dd4c2-109">元素</span><span class="sxs-lookup"><span data-stu-id="dd4c2-109">Element</span></span>                                                           | <span data-ttu-id="dd4c2-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="dd4c2-110">Derived from</span></span>                                                         | <span data-ttu-id="dd4c2-111">Description</span><span class="sxs-lookup"><span data-stu-id="dd4c2-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="dd4c2-112">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="dd4c2-113">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="dd4c2-114">指定啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="dd4c2-115">子元素</span><span class="sxs-lookup"><span data-stu-id="dd4c2-115">Child elements</span></span>



| <span data-ttu-id="dd4c2-116">元素</span><span class="sxs-lookup"><span data-stu-id="dd4c2-116">Element</span></span>                                                                                                                            | <span data-ttu-id="dd4c2-117">類型</span><span class="sxs-lookup"><span data-stu-id="dd4c2-117">Type</span></span>                                                                                                 | <span data-ttu-id="dd4c2-118">Description</span><span class="sxs-lookup"><span data-stu-id="dd4c2-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd4c2-119">**已啟用 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-119">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | <span data-ttu-id="dd4c2-120">boolean</span><span class="sxs-lookup"><span data-stu-id="dd4c2-120">boolean</span></span>                                                                                              | <span data-ttu-id="dd4c2-121">指定啟用觸發程序。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-121">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="dd4c2-122">**EndBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-122">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | <span data-ttu-id="dd4c2-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="dd4c2-123">dateTime</span></span>                                                                                             | <span data-ttu-id="dd4c2-124">指定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-124">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="dd4c2-125">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-125">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="dd4c2-126">**ExecutionTimeLimit (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-126">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | <span data-ttu-id="dd4c2-127">duration</span><span class="sxs-lookup"><span data-stu-id="dd4c2-127">duration</span></span>                                                                                             | <span data-ttu-id="dd4c2-128">指定觸發程式可啟動工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-128">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="dd4c2-129">**重複 (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [<span data-ttu-id="dd4c2-130">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md)                             | <span data-ttu-id="dd4c2-131">指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="dd4c2-132">**ScheduleByDay (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-132">**ScheduleByDay (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="dd4c2-133">**dailyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-133">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="dd4c2-134">指定每日排程。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-134">Specifies a daily schedule.</span></span><br/>                                                                                             |
| [<span data-ttu-id="dd4c2-135">**ScheduleByMonth (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-135">**ScheduleByMonth (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="dd4c2-136">**monthlyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-136">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="dd4c2-137">指定每月排程。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-137">Specifies a monthly schedule.</span></span><br/>                                                                                           |
| [<span data-ttu-id="dd4c2-138">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-138">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="dd4c2-139">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-139">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="dd4c2-140">指定在每月一周的排程上啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-140">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/>                                                |
| [<span data-ttu-id="dd4c2-141">**ScheduleByWeek (calendarTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-141">**ScheduleByWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="dd4c2-142">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-142">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="dd4c2-143">指定每週排程。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-143">Specifies a weekly schedule.</span></span><br/>                                                                                            |
| [<span data-ttu-id="dd4c2-144">**StartBoundary (triggerBaseType)**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-144">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | <span data-ttu-id="dd4c2-145">dateTime</span><span class="sxs-lookup"><span data-stu-id="dd4c2-145">dateTime</span></span>                                                                                             | <span data-ttu-id="dd4c2-146">指定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-146">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="dd4c2-147">這個元素是必要的。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-147">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="dd4c2-148">屬性</span><span class="sxs-lookup"><span data-stu-id="dd4c2-148">Attributes</span></span>



| <span data-ttu-id="dd4c2-149">名稱</span><span class="sxs-lookup"><span data-stu-id="dd4c2-149">Name</span></span> | <span data-ttu-id="dd4c2-150">類型</span><span class="sxs-lookup"><span data-stu-id="dd4c2-150">Type</span></span> | <span data-ttu-id="dd4c2-151">Description</span><span class="sxs-lookup"><span data-stu-id="dd4c2-151">Description</span></span>                               |
|------|------|-------------------------------------------|
| <span data-ttu-id="dd4c2-152">識別碼</span><span class="sxs-lookup"><span data-stu-id="dd4c2-152">Id</span></span>   | <span data-ttu-id="dd4c2-153">識別碼</span><span class="sxs-lookup"><span data-stu-id="dd4c2-153">ID</span></span>   | <span data-ttu-id="dd4c2-154">觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-154">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dd4c2-155">備註</span><span class="sxs-lookup"><span data-stu-id="dd4c2-155">Remarks</span></span>

<span data-ttu-id="dd4c2-156">[**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)元素是時間和行事曆觸發程式的必要元素， ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)和 **CalendarTrigger**) 。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-156">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and **CalendarTrigger**).</span></span>

<span data-ttu-id="dd4c2-157">上方所列的子專案是由 [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) 和 [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) 複雜元素類型所定義。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-157">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex element types.</span></span>

<span data-ttu-id="dd4c2-158">針對腳本開發，行事曆觸發程式是使用下列其中一個物件指定的。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-158">For script development, calendar triggers are specified using one of the following objects.</span></span>

-   [<span data-ttu-id="dd4c2-159">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-159">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="dd4c2-160">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-160">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="dd4c2-161">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-161">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="dd4c2-162">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-162">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)

<span data-ttu-id="dd4c2-163">針對 c + + 開發，行事曆觸發程式是使用下列其中一個介面指定的。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-163">For C++ development, calendar triggers are specified using one of the following interfaces.</span></span>

-   [<span data-ttu-id="dd4c2-164">**IDailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-164">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="dd4c2-165">**IWeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-165">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [<span data-ttu-id="dd4c2-166">**IMonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-166">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="dd4c2-167">**IMonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="dd4c2-167">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a><span data-ttu-id="dd4c2-168">範例</span><span class="sxs-lookup"><span data-stu-id="dd4c2-168">Examples</span></span>

<span data-ttu-id="dd4c2-169">如需指定行事曆觸發程式之工作的完整 XML 範例，請參閱 [ (xml) 的每日觸發程式範例 ](daily-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="dd4c2-169">For a complete example of the XML for a task that specifies a calendar trigger, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd4c2-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd4c2-170">Requirements</span></span>



| <span data-ttu-id="dd4c2-171">需求</span><span class="sxs-lookup"><span data-stu-id="dd4c2-171">Requirement</span></span> | <span data-ttu-id="dd4c2-172">值</span><span class="sxs-lookup"><span data-stu-id="dd4c2-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd4c2-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd4c2-173">Minimum supported client</span></span><br/> | <span data-ttu-id="dd4c2-174">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd4c2-174">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dd4c2-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd4c2-175">Minimum supported server</span></span><br/> | <span data-ttu-id="dd4c2-176">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd4c2-176">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd4c2-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd4c2-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd4c2-178">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="dd4c2-178">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="dd4c2-179">工作排程器</span><span class="sxs-lookup"><span data-stu-id="dd4c2-179">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





