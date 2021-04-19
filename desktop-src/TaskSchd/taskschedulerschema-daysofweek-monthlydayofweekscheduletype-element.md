---
title: DaysOfWeek (monthlyDayOfWeekScheduleType) 元素
description: 指定工作執行的星期幾。 |DaysOfWeek (monthlyDayOfWeekScheduleType) 元素
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
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
ms.openlocfilehash: 3867e08dd001a035a3ab25da056f75c1e73eeeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992278"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a><span data-ttu-id="dbd91-105">DaysOfWeek (monthlyDayOfWeekScheduleType) 元素</span><span class="sxs-lookup"><span data-stu-id="dbd91-105">DaysOfWeek (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="dbd91-106">指定工作執行的星期幾。</span><span class="sxs-lookup"><span data-stu-id="dbd91-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="dbd91-107">**DaysOfWeek** 元素是由 [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="dbd91-107">The **DaysOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dbd91-108">父元素</span><span class="sxs-lookup"><span data-stu-id="dbd91-108">Parent element</span></span>



| <span data-ttu-id="dbd91-109">元素</span><span class="sxs-lookup"><span data-stu-id="dbd91-109">Element</span></span>                                                                                                      | <span data-ttu-id="dbd91-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="dbd91-110">Derived from</span></span>                                                                                         | <span data-ttu-id="dbd91-111">Description</span><span class="sxs-lookup"><span data-stu-id="dbd91-111">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbd91-112">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="dbd91-112">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="dbd91-113">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="dbd91-113">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="dbd91-114">指定啟動工作的觸發程式，此觸發程式會每個月的每週工作日排程。</span><span class="sxs-lookup"><span data-stu-id="dbd91-114">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="dbd91-115">子元素</span><span class="sxs-lookup"><span data-stu-id="dbd91-115">Child elements</span></span>



| <span data-ttu-id="dbd91-116">元素</span><span class="sxs-lookup"><span data-stu-id="dbd91-116">Element</span></span>                                                                   | <span data-ttu-id="dbd91-117">類型</span><span class="sxs-lookup"><span data-stu-id="dbd91-117">Type</span></span> | <span data-ttu-id="dbd91-118">Description</span><span class="sxs-lookup"><span data-stu-id="dbd91-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="dbd91-119">**星期五**</span><span class="sxs-lookup"><span data-stu-id="dbd91-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="dbd91-120">指定工作在星期五執行。</span><span class="sxs-lookup"><span data-stu-id="dbd91-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="dbd91-121">**星期一**</span><span class="sxs-lookup"><span data-stu-id="dbd91-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="dbd91-122">指定工作在星期一執行。</span><span class="sxs-lookup"><span data-stu-id="dbd91-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="dbd91-123">**星期六**</span><span class="sxs-lookup"><span data-stu-id="dbd91-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="dbd91-124">指定工作在星期六執行。</span><span class="sxs-lookup"><span data-stu-id="dbd91-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="dbd91-125">**星期日**</span><span class="sxs-lookup"><span data-stu-id="dbd91-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="dbd91-126">指定工作在星期日執行。</span><span class="sxs-lookup"><span data-stu-id="dbd91-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="dbd91-127">**Thursday**</span><span class="sxs-lookup"><span data-stu-id="dbd91-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="dbd91-128">指定工作在星期四執行。</span><span class="sxs-lookup"><span data-stu-id="dbd91-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="dbd91-129">**Tuesday**</span><span class="sxs-lookup"><span data-stu-id="dbd91-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="dbd91-130">指定工作在星期二執行。</span><span class="sxs-lookup"><span data-stu-id="dbd91-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="dbd91-131">**星期三**</span><span class="sxs-lookup"><span data-stu-id="dbd91-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="dbd91-132">指定工作會在星期三執行。</span><span class="sxs-lookup"><span data-stu-id="dbd91-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dbd91-133">備註</span><span class="sxs-lookup"><span data-stu-id="dbd91-133">Remarks</span></span>

<span data-ttu-id="dbd91-134">針對開發腳本，使用 [**MonthlyDOWTrigger. DaysOfWeek**](monthlydowtrigger-daysofweek.md) 屬性指定每週每月星期幾行事曆的天數。</span><span class="sxs-lookup"><span data-stu-id="dbd91-134">For scripting development, the days of the week for a monthly day-of-week calendar are specified using the [**MonthlyDOWTrigger.DaysOfWeek**](monthlydowtrigger-daysofweek.md) property.</span></span>

<span data-ttu-id="dbd91-135">若是 c + + 開發，則會使用 [**IMonthlyDOWTrigger：:D aysofweek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) 屬性指定每週每週的日曆日。</span><span class="sxs-lookup"><span data-stu-id="dbd91-135">For C++ development, the days of the week for a monthly day-of-week calendar are specified using the [**IMonthlyDOWTrigger::DaysOfWeek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) property.</span></span>

<span data-ttu-id="dbd91-136">上述的子項目是由 [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="dbd91-136">The child elements above are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="dbd91-137">範例</span><span class="sxs-lookup"><span data-stu-id="dbd91-137">Examples</span></span>

<span data-ttu-id="dbd91-138">下列 XML 會定義每月的每週工作日行事曆，此日曆會在每個月的第一周的星期一開始工作。</span><span class="sxs-lookup"><span data-stu-id="dbd91-138">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


```XML
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
```



## <a name="requirements"></a><span data-ttu-id="dbd91-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbd91-139">Requirements</span></span>



| <span data-ttu-id="dbd91-140">需求</span><span class="sxs-lookup"><span data-stu-id="dbd91-140">Requirement</span></span> | <span data-ttu-id="dbd91-141">值</span><span class="sxs-lookup"><span data-stu-id="dbd91-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dbd91-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbd91-142">Minimum supported client</span></span><br/> | <span data-ttu-id="dbd91-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbd91-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dbd91-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbd91-144">Minimum supported server</span></span><br/> | <span data-ttu-id="dbd91-145">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbd91-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dbd91-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbd91-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbd91-147">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="dbd91-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="dbd91-148">工作排程器</span><span class="sxs-lookup"><span data-stu-id="dbd91-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





