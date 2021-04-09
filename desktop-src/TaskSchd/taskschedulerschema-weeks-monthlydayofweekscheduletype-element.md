---
title: MonthlyDayOfWeekScheduleType) 元素 (周
description: 指定執行工作的月份周數。
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- 周元素工作排程器
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e032b936353d2c89a84b5da684f681ea3c2b6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686360"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a><span data-ttu-id="d4300-104">MonthlyDayOfWeekScheduleType) 元素 (周</span><span class="sxs-lookup"><span data-stu-id="d4300-104">Weeks (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="d4300-105">指定執行工作的月份周數。</span><span class="sxs-lookup"><span data-stu-id="d4300-105">Specifies the weeks of the month in which the task is run.</span></span>

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

<span data-ttu-id="d4300-106">**周** 元素是由 [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="d4300-106">The **Weeks** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d4300-107">父元素</span><span class="sxs-lookup"><span data-stu-id="d4300-107">Parent element</span></span>



| <span data-ttu-id="d4300-108">元素</span><span class="sxs-lookup"><span data-stu-id="d4300-108">Element</span></span>                                                                                                      | <span data-ttu-id="d4300-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="d4300-109">Derived from</span></span>                                                                                         | <span data-ttu-id="d4300-110">Description</span><span class="sxs-lookup"><span data-stu-id="d4300-110">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4300-111">**ScheduleByMonthDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="d4300-111">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="d4300-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="d4300-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="d4300-113">指定在每月一周的排程上啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="d4300-113">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="d4300-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d4300-114">Child elements</span></span>



| <span data-ttu-id="d4300-115">元素</span><span class="sxs-lookup"><span data-stu-id="d4300-115">Element</span></span>                                                    | <span data-ttu-id="d4300-116">類型</span><span class="sxs-lookup"><span data-stu-id="d4300-116">Type</span></span>                                                        | <span data-ttu-id="d4300-117">Description</span><span class="sxs-lookup"><span data-stu-id="d4300-117">Description</span></span>                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="d4300-118">**週**</span><span class="sxs-lookup"><span data-stu-id="d4300-118">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="d4300-119">**weekType**</span><span class="sxs-lookup"><span data-stu-id="d4300-119">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="d4300-120">指定當月的特定周。</span><span class="sxs-lookup"><span data-stu-id="d4300-120">Specifies a specific week of the month.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d4300-121">備註</span><span class="sxs-lookup"><span data-stu-id="d4300-121">Remarks</span></span>

<span data-ttu-id="d4300-122">針對開發腳本，會使用 [**MonthlyDOWTrigger WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) 屬性指定月份的周數。</span><span class="sxs-lookup"><span data-stu-id="d4300-122">For scripting development, the weeks of the month are specified using the [**MonthlyDOWTrigger.WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) property.</span></span>

<span data-ttu-id="d4300-123">若是 c + + 開發，則會使用 [**IMonthlyDOWTrigger：： WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) 屬性指定月份的周數。</span><span class="sxs-lookup"><span data-stu-id="d4300-123">For C++ development, the weeks of the month are specified using the [**IMonthlyDOWTrigger::WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) property.</span></span>

<span data-ttu-id="d4300-124">指定月中的周時，請使用1-4 來指定當月的前四周，或使用 "Last" 字串來指出上周（無論是哪一周）。</span><span class="sxs-lookup"><span data-stu-id="d4300-124">When specifying the weeks of the month, use 1-4 to specify the first four weeks of the month or use the string "Last" to indicate the last week regardless of which week it is.</span></span>

## <a name="examples"></a><span data-ttu-id="d4300-125">範例</span><span class="sxs-lookup"><span data-stu-id="d4300-125">Examples</span></span>

<span data-ttu-id="d4300-126">下列 XML 會定義每月的每週工作日行事曆，此日曆會在每個月的第一周的星期一開始工作。</span><span class="sxs-lookup"><span data-stu-id="d4300-126">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d4300-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4300-127">Requirements</span></span>



| <span data-ttu-id="d4300-128">需求</span><span class="sxs-lookup"><span data-stu-id="d4300-128">Requirement</span></span> | <span data-ttu-id="d4300-129">值</span><span class="sxs-lookup"><span data-stu-id="d4300-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d4300-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4300-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d4300-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4300-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d4300-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4300-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d4300-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4300-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4300-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4300-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4300-135">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="d4300-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d4300-136">工作排程器</span><span class="sxs-lookup"><span data-stu-id="d4300-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





