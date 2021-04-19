---
title: DaysOfWeek (weeklyScheduleType) 元素
description: 指定工作執行的星期幾。 |DaysOfWeek (weeklyScheduleType) 元素
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
keywords:
- DaysOfWeek 元素工作排程器
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106998990"
---
# <a name="daysofweek-weeklyscheduletype-element"></a><span data-ttu-id="30e4c-105">DaysOfWeek (weeklyScheduleType) 元素</span><span class="sxs-lookup"><span data-stu-id="30e4c-105">DaysOfWeek (weeklyScheduleType) Element</span></span>

<span data-ttu-id="30e4c-106">指定工作執行的星期幾。</span><span class="sxs-lookup"><span data-stu-id="30e4c-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="30e4c-107">**DaysOfWeek** 元素是由 [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="30e4c-107">The **DaysOfWeek** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="30e4c-108">父元素</span><span class="sxs-lookup"><span data-stu-id="30e4c-108">Parent element</span></span>



| <span data-ttu-id="30e4c-109">元素</span><span class="sxs-lookup"><span data-stu-id="30e4c-109">Element</span></span>                                                                                  | <span data-ttu-id="30e4c-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="30e4c-110">Derived from</span></span>                                                                     | <span data-ttu-id="30e4c-111">Description</span><span class="sxs-lookup"><span data-stu-id="30e4c-111">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="30e4c-112">**ScheduleByWeek**</span><span class="sxs-lookup"><span data-stu-id="30e4c-112">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="30e4c-113">**weeklyScheduleType**</span><span class="sxs-lookup"><span data-stu-id="30e4c-113">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="30e4c-114">指定每週排程。</span><span class="sxs-lookup"><span data-stu-id="30e4c-114">Specifies a weekly schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="30e4c-115">子元素</span><span class="sxs-lookup"><span data-stu-id="30e4c-115">Child elements</span></span>



| <span data-ttu-id="30e4c-116">元素</span><span class="sxs-lookup"><span data-stu-id="30e4c-116">Element</span></span>                                                                   | <span data-ttu-id="30e4c-117">類型</span><span class="sxs-lookup"><span data-stu-id="30e4c-117">Type</span></span> | <span data-ttu-id="30e4c-118">Description</span><span class="sxs-lookup"><span data-stu-id="30e4c-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="30e4c-119">**星期五**</span><span class="sxs-lookup"><span data-stu-id="30e4c-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="30e4c-120">指定工作在星期五執行。</span><span class="sxs-lookup"><span data-stu-id="30e4c-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="30e4c-121">**星期一**</span><span class="sxs-lookup"><span data-stu-id="30e4c-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="30e4c-122">指定工作在星期一執行。</span><span class="sxs-lookup"><span data-stu-id="30e4c-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="30e4c-123">**星期六**</span><span class="sxs-lookup"><span data-stu-id="30e4c-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="30e4c-124">指定工作在星期六執行。</span><span class="sxs-lookup"><span data-stu-id="30e4c-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="30e4c-125">**星期日**</span><span class="sxs-lookup"><span data-stu-id="30e4c-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="30e4c-126">指定工作在星期日執行。</span><span class="sxs-lookup"><span data-stu-id="30e4c-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="30e4c-127">**Thursday**</span><span class="sxs-lookup"><span data-stu-id="30e4c-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="30e4c-128">指定工作在星期四執行。</span><span class="sxs-lookup"><span data-stu-id="30e4c-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="30e4c-129">**Tuesday**</span><span class="sxs-lookup"><span data-stu-id="30e4c-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="30e4c-130">指定工作在星期二執行。</span><span class="sxs-lookup"><span data-stu-id="30e4c-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="30e4c-131">**星期三**</span><span class="sxs-lookup"><span data-stu-id="30e4c-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="30e4c-132">指定工作會在星期三執行。</span><span class="sxs-lookup"><span data-stu-id="30e4c-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="30e4c-133">備註</span><span class="sxs-lookup"><span data-stu-id="30e4c-133">Remarks</span></span>

<span data-ttu-id="30e4c-134">先前的子項目是由 [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="30e4c-134">The previous child elements are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

<span data-ttu-id="30e4c-135">針對腳本開發，每週間隔會使用 [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="30e4c-135">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="30e4c-136">針對 c + + 開發，每週間隔是使用 [**IWeeklyTrigger：： WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="30e4c-136">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="30e4c-137">範例</span><span class="sxs-lookup"><span data-stu-id="30e4c-137">Examples</span></span>

<span data-ttu-id="30e4c-138">下列 XML 會定義每日星期一到星期五 ( 開始工作的每日日曆觸發程式，每週) 上午8:00。</span><span class="sxs-lookup"><span data-stu-id="30e4c-138">The following XML defines a daily calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


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



<span data-ttu-id="30e4c-139">如需使用每週觸發程式之工作的完整 XML 範例，請參閱 [ (xml) 的每週觸發程式範例 ](weekly-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="30e4c-139">For a complete example of the XML for a task that uses a weekly trigger, see [Weekly Trigger Example (XML)](weekly-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30e4c-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="30e4c-140">Requirements</span></span>



| <span data-ttu-id="30e4c-141">需求</span><span class="sxs-lookup"><span data-stu-id="30e4c-141">Requirement</span></span> | <span data-ttu-id="30e4c-142">值</span><span class="sxs-lookup"><span data-stu-id="30e4c-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="30e4c-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30e4c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="30e4c-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30e4c-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="30e4c-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30e4c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="30e4c-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30e4c-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30e4c-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30e4c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30e4c-148">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="30e4c-148">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="30e4c-149">工作排程器</span><span class="sxs-lookup"><span data-stu-id="30e4c-149">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





