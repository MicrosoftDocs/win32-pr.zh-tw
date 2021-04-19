---
title: DaysOfMonth (monthlyScheduleType) 元素
description: 指定工作執行的當月天數。
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- DaysOfMonth 元素工作排程器
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965120"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a><span data-ttu-id="31e15-104">DaysOfMonth (monthlyScheduleType) 元素</span><span class="sxs-lookup"><span data-stu-id="31e15-104">DaysOfMonth (monthlyScheduleType) Element</span></span>

<span data-ttu-id="31e15-105">指定工作執行的當月天數。</span><span class="sxs-lookup"><span data-stu-id="31e15-105">Specifies the days of the month during which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

<span data-ttu-id="31e15-106">**DaysOfMonth** 元素是由 [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="31e15-106">The **DaysOfMonth** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="31e15-107">父元素</span><span class="sxs-lookup"><span data-stu-id="31e15-107">Parent element</span></span>



| <span data-ttu-id="31e15-108">元素</span><span class="sxs-lookup"><span data-stu-id="31e15-108">Element</span></span>                                                                                    | <span data-ttu-id="31e15-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="31e15-109">Derived from</span></span>                                                                                         | <span data-ttu-id="31e15-110">Description</span><span class="sxs-lookup"><span data-stu-id="31e15-110">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="31e15-111">**ScheduleByMonth**</span><span class="sxs-lookup"><span data-stu-id="31e15-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="31e15-112">**monthlyDayOfWeekScheduleType**</span><span class="sxs-lookup"><span data-stu-id="31e15-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="31e15-113">指定啟動工作的觸發程式，此觸發程式會每個月的每週工作日排程。</span><span class="sxs-lookup"><span data-stu-id="31e15-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="31e15-114">子元素</span><span class="sxs-lookup"><span data-stu-id="31e15-114">Child elements</span></span>



| <span data-ttu-id="31e15-115">元素</span><span class="sxs-lookup"><span data-stu-id="31e15-115">Element</span></span>                                                        | <span data-ttu-id="31e15-116">類型</span><span class="sxs-lookup"><span data-stu-id="31e15-116">Type</span></span>                                                                    | <span data-ttu-id="31e15-117">Description</span><span class="sxs-lookup"><span data-stu-id="31e15-117">Description</span></span>                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="31e15-118">**天**</span><span class="sxs-lookup"><span data-stu-id="31e15-118">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="31e15-119">**dayOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="31e15-119">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="31e15-120">指定執行工作的月份日期。</span><span class="sxs-lookup"><span data-stu-id="31e15-120">Specifies a day of the month during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="31e15-121">備註</span><span class="sxs-lookup"><span data-stu-id="31e15-121">Remarks</span></span>

<span data-ttu-id="31e15-122">針對腳本開發，系統會使用 [**MonthlyTrigger. DaysOfMonth**](monthlytrigger-daysofmonth.md) 屬性指定該排程的當月天數。</span><span class="sxs-lookup"><span data-stu-id="31e15-122">For script development, the days of the month for the schedule are specified using the [**MonthlyTrigger.DaysOfMonth**](monthlytrigger-daysofmonth.md) property.</span></span>

<span data-ttu-id="31e15-123">針對 c + + 開發，會使用 [**IMonthlyTrigger：:D aysofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) 屬性來指定排程的當月天數。</span><span class="sxs-lookup"><span data-stu-id="31e15-123">For C++ development, the days of the month for the schedule are specified using the [**IMonthlyTrigger::DaysOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) property.</span></span>

<span data-ttu-id="31e15-124">工作要執行的每個月的每一天都必須重複子項目。</span><span class="sxs-lookup"><span data-stu-id="31e15-124">The child element must be repeated for each day of the month the task is to run.</span></span>

## <a name="examples"></a><span data-ttu-id="31e15-125">範例</span><span class="sxs-lookup"><span data-stu-id="31e15-125">Examples</span></span>

<span data-ttu-id="31e15-126">下列 XML 會定義每月的行事曆觸發程式，此觸發程式會在每個月的第一天) 的上午8:30 開始工作 (。</span><span class="sxs-lookup"><span data-stu-id="31e15-126">The following XML defines a monthly calendar trigger that starts a task (at 8:30 AM) on the 1st day of every month.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="31e15-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="31e15-127">Requirements</span></span>



| <span data-ttu-id="31e15-128">需求</span><span class="sxs-lookup"><span data-stu-id="31e15-128">Requirement</span></span> | <span data-ttu-id="31e15-129">值</span><span class="sxs-lookup"><span data-stu-id="31e15-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="31e15-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31e15-130">Minimum supported client</span></span><br/> | <span data-ttu-id="31e15-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31e15-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="31e15-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31e15-132">Minimum supported server</span></span><br/> | <span data-ttu-id="31e15-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31e15-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31e15-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31e15-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e15-135">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="31e15-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="31e15-136">工作排程器</span><span class="sxs-lookup"><span data-stu-id="31e15-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





